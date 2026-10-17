# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 39 of 40 (1,588 words)





def coherent_states(alphas, nc):

    C = np.zeros((len(alphas), nc), complex)

    C[:, 0] = np.exp(-np.abs(alphas)**2 / 2)

    for n in range(1, nc):

        C[:, n] = C[:, n - 1] * alphas / np.sqrt(n)

    return C





dp, npg = 0.12, 81

pg = (np.arange(npg) - npg // 2) * dp





def pointer_states(cu, cw, M, sg, chirp):

    """field vector for each pair of pointer momenta after the coupling U, pointers prepared

    in Gaussians of widths sg, pre-chirped by exp(i M_kk p_k^2/2) if chirp"""

    P = np.stack([a.ravel() for a in np.meshgrid(pg, pg, indexing='ij')], 1)

    amp = np.prod((2 * sg**2 / np.pi)**0.25 * np.exp(-sg**2 * P**2), axis=1)

    ph = -0.5 * np.einsum('gk,kl,gl->g', P, M, P) + (0.5 * P**2 @ np.diag(M) if chirp else 0)

    alph = (P @ cw - 1j * (P @ cu)) / np.sqrt(2)       # exp(-i p.phi)|0> is coherent

    return (amp * np.exp(1j * ph))[:, None] * coherent_states(alph, ncut)





def chi_pointer(F, n1, n2):

    """E exp(i s.y) = sum_p <F(p), F(p - s)> for s = (n1, n2) grid steps"""

    G = F.reshape(npg, npg, -1)

    A = G[max(n1, 0):npg + min(n1, 0), max(n2, 0):npg + min(n2, 0)]

    B = G[max(-n1, 0):npg + min(-n1, 0), max(-n2, 0):npg + min(-n2, 0)]

    return np.sum(A.conj() * B) * dp * dp





def chi_sequential(order, eigs, sg, s):

    def ms(m, w_):

        dd, mm = w_[:, None] - w_[None, :], (w_[:, None] + w_[None, :]) / 2

        return np.exp(-dd**2 / (8 * sg[m]**2) + 1j * s[m] * mm - s[m]**2 * sg[m]**2 / 2)

    return run_order(order, eigs, ms)





shifts = [(1, 0), (0, 1), (2, -1), (3, 2), (-2, 4), (5, 3), (-4, -3)]

sg = np.array([0.8, 0.9])

res = {}

for name, pts in (('overlap', np.array([[0.3, 0.1], [0.55, 0.25]])),

                  ('one-way', np.array([[0.0, 0.0], [1.2, 0.3]]))):

    R, E = geometry(pts, dl, scale)

    M = Mret(pts, dl, scale)

    r = {'E': E, 'M': M, 'R': R, 'split': np.abs(M - M.T - E).max()}

    T0 = {nn: ordered_sums(pts, dl, scale, nn, 0.0) for nn in (32, 64)}

    T1 = ordered_sums(pts, dl, scale, 64, 0.6)

    r['fol'] = np.abs(T1 - T0[64]).max()

    r['disc'] = [np.abs(T0[nn] - M).max() for nn in (32, 64)]

    cu, cw = realize(E)

    Sig = 0.5 * np.outer(cu, cu) + 0.5 * np.outer(cw, cw)

    D = np.diag(1 / (4 * sg**2))

    Mo = M - np.diag(np.diag(M))

    r['C'] = Sig + np.diag(sg**2) + Mo @ D @ Mo.T

    r['Cfull'] = Sig + np.diag(sg**2) + M @ D @ M.T

    r['Cord'] = cov_closed([0, 1], E, Sig, sg)

    eigs = [eigh(cu[i] * qo + cw[i] * po) for i in range(2)]

    dev = {}

    for chirp in (True, False):

        F = pointer_states(cu, cw, M, sg, chirp)

        C = r['C'] if chirp else r['Cfull']

        dev[chirp] = max(abs(chi_pointer(F, *n)

                             - np.exp(-0.5 * dp**2 * np.array(n) @ C @ np.array(n)))

                         for n in shifts)

        if chirp:

            r['seq'] = max(abs(chi_pointer(F, *n)

                               - chi_sequential([0, 1], eigs, sg, dp * np.array(n)))

                           for n in shifts)

            rho_p = (F.T @ F.conj()) * dp * dp

            rho0 = np.zeros((ncut, ncut), complex)

            rho0[0, 0] = 1

            rho_s = dephase(dephase(rho0, cu[0] * qo + cw[0] * po, sg[0]),

                            cu[1] * qo + cw[1] * po, sg[1])

            r['unread'] = np.abs(rho_p - rho_s)[:60, :60].max()

            r['trace'] = np.trace(rho_p).real

    r['dev'] = dev

    res[name] = r

ov, ow = res['overlap'], res['one-way']

print('   (a) E = Gamma - Gamma^T: max dev %.1e (overlapping pair), %.1e (one-way pair)'

      % (ov['split'], ow['split']))

print('       overlapping pair: Gamma_12 = %.6f, Gamma_21 = %.6f, Gamma_11 = Gamma_22 = %.6f'

      % (ov['M'][0, 1], ov['M'][1, 0], ov['M'][0, 0]))

print('       phase of the time-ordered product, two foliations (relative rapidity 0.6):')

print('       max difference %.1e and %.1e;' % (ov['fol'], ow['fol']))

print('       deviation from Gamma, 32 and 64 nodes per axis: %.1e, %.1e (overlapping),'

      % tuple(ov['disc']))

print('       %.1e, %.1e (one-way)' % tuple(ow['disc']))

print('   (b) overlapping pair, explicit pointers, characteristic function vs closed form:')

print('       pre-chirped pointers %.1e; without the pre-chirp, full Gamma, %.1e'

      % (ov['dev'][True], ov['dev'][False]))

print('   (c) unread field channel vs two Gaussian collapse channels: max dev %.1e;'

      % ov['unread'])

print('       trace %.12f' % ov['trace'])

print('   (d) one-way pair: pointers vs Gaussian collapses applied in causal order, direct')

print('       characteristic functions: max dev %.1e; closed-form covariances: max diff %.1e'

      % (ow['seq'], np.abs(ow['C'] - ow['Cord']).max()))

dC = ov['C'] - ov['Cord']

print('       overlapping pair, pointer law minus the law of collapses in centre-time order:')

print('       Var(y1) %+.6f, Var(y2) %+.6f, Cov(y1, y2) %+.6f;' % (dC[0, 0], dC[1, 1], dC[0, 1]))

print('       direct characteristic functions differ by up to %.4f' % ov['seq'])



Output:



C1. Random-kick form of the unread Gaussian collapse channel

   Kraus integral over y vs exact multiplier:     max dev 2.4e-14

   Gaussian mixture of kicks vs exact multiplier: max dev 7.8e-16

C2. Energy-momentum cost

   (a) cutoff 140: ground 0.150060024010, random 0.150060024010; 1/(8 m sig^2) = 0.150060024010

   (a) cutoff 180: ground 0.150060024010, random 0.150060024010; 1/(8 m sig^2) = 0.150060024010

   (b) two modes: vacuum 0.126367187500, random 0.126367187500; predicted 0.126367187500

   (c) lattice: canonical 0.041729335207, Fourier formula 0.041729335207, relative diff. 5.0e-16

   (d) Delta P(h) = (0.00710022, 0.00104472), squared invariant mass 0.00004932

       boost of rapidity 0.5: |Delta P(Lambda h) - Lambda Delta P(h)| = 1.3e-16

C3. Poisson-located Gaussian collapses, massless field in 1+1 dimensions

   (a) counts, area 16, intensity 6: mean 96.00, variance 96.35 (expected 96 and 96)

   (b) intensity 1.5, 40000 samples per box:  side  P(orderable)  bound of Prop. 13.22

                                              1.0   0.59905       0.79757

                                              1.5   0.25833       0.60115

                                              2.0   0.08060       0.40465

                                              2.5   0.01510       0.24325

   (c) 300 orderable configurations, 1265 collapses, 1176 linear extensions:

       max covariance difference between linear extensions 1.8e-15

   (d) 4 three-collapse configurations, one-mode realization, Fock cutoff 140:

       characteristic function, direct vs closed form: max dev 1.8e-14

       64-cell binned history laws: max difference between linear extensions 4.8e-16,

       normalization error 3.1e-14

   (e) overlapping pair, E(h1, h2) = 1.099141:

       increase of Var(y2) caused by collapse 1: 0.4719185385; E^2/(4 sigma1^2) = 0.4719185385

       binned joint laws for the two orders: total-variation distance 0.0570

       unread channels in the two orders: max difference of the final states 6.8e-15

   (f) 300 non-orderable configurations ordered by centre time in two frames

       (relative rapidity 0.6): laws differ in 234, max covariance difference 0.701

   (g) centre-time order is a linear extension of the causal order in 300 of the 300

       orderable configurations of item (c)

   (h) order j, c1, c2, y by t; c1 and c2 overlap; E(h_j, h_c1) = 0.2334, E(h_c1, h_y) = 0.2334,

       E(h_c1, h_c2) = 1.2221, E(h_j, h_y) = 0.0

       cutoff 36: Gaussian c1: change of the target law by a kick at j 1.6e-15,

       by a collapse at j 1.1e-16; target law sums to 1.000000000000

       unsharp Lueders instrument at j (not Weyl-diagonal): change 2.8e-16

       unsharp Lueders c1 (negative control): change by the kick, largest bin 0.0008100

       cutoff 44: Gaussian c1: change of the target law by a kick at j 8.9e-16,

       by a collapse at j 1.1e-16; target law sums to 1.000000000000

       unsharp Lueders instrument at j (not Weyl-diagonal): change 1.1e-16

       unsharp Lueders c1 (negative control): change by the kick, largest bin 0.0008100

C4. Gapless pointer realization of the collapses (Proposition 13.31)

   (a) E = Gamma - Gamma^T: max dev 2.2e-16 (overlapping pair), 0.0e+00 (one-way pair)

       overlapping pair: Gamma_12 = -0.060881, Gamma_21 = -1.160022, Gamma_11 = Gamma_22 = -0.500000

       phase of the time-ordered product, two foliations (relative rapidity 0.6):

       max difference 0.0e+00 and 0.0e+00;

       deviation from Gamma, 32 and 64 nodes per axis: 2.8e-02, 9.0e-03 (overlapping),

       1.9e-03, 4.8e-04 (one-way)

   (b) overlapping pair, explicit pointers, characteristic function vs closed form:

       pre-chirped pointers 7.3e-14; without the pre-chirp, full Gamma, 2.0e-13

   (c) unread field channel vs two Gaussian collapse channels: max dev 1.7e-14;

       trace 1.000000000000

   (d) one-way pair: pointers vs Gaussian collapses applied in causal order, direct

       characteristic functions: max dev 1.8e-13; closed-form covariances: max diff 0.0e+00

       overlapping pair, pointer law minus the law of collapses in centre-time order:

       Var(y1) +0.001144, Var(y2) +0.053727, Cov(y1, y2) +0.000000;

       direct characteristic functions differ by up to 0.0049



C.2 Two Ideal Clocks



# Verification of Proposition 14.5 (Appendix C.2): two ideal clocks, interactions in the

# constraint. Physical states are Psi(t_A, t_B) = U_Delta(t_A) chi(Delta), Delta = t_A - t_B,

# where U_Delta solves i dU/ds = H_Delta(s) U from s0 = -2.5, with

# H_Delta(s) = H_S + sum_{k keyed to A} g_k(s) V_k + sum_{k keyed to B} g_k(s - Delta) V_k.

import numpy as np

from scipy.linalg import expm



sx = np.array([[0, 1], [1, 0]], complex)

sy = np.array([[0, -1j], [1j, 0]])

sz = np.diag([1.0, -1.0]).astype(complex)

P1 = np.diag([0.0, 1.0]).astype(complex)

I2 = np.eye(2)

kron = np.kron

bump = lambda z: np.where(np.abs(z) < 1, np.exp(-1 / np.maximum(1 - z**2, 1e-300)), 0.0)



ds, s0, s1 = 0.01, -2.5, 7.0

sgrid = s0 + ds * np.arange(int(round((s1 - s0) / ds)) + 1)

mids = sgrid[:-1] + ds / 2





def pulse(area):

    """switching function supported in [0, 1]; its midpoint sum on the grid equals area"""

    g = lambda s: bump((s - 0.5) / 0.5)

    norm = np.sum(g(np.arange(0, 1, ds) + ds / 2)) * ds

    return lambda s: area * g(s) / norm





def propagate(Hfun):

    """U(s) from s0 at every grid point"""

    U = np.eye(4, dtype=complex)

    out = [U]

    for m in mids:

        U = expm(-1j * ds * Hfun(m)) @ U

        out.append(U)

    return out





at = lambda s: int(round((s - s0) / ds))

rng = np.random.default_rng(5)





def system_state():

    v = rng.normal(size=2) + 1j * rng.normal(size=2)

    return np.kron(v / np.linalg.norm(v), [1, 0])          # record starts in |0>





def packets(centres, width, states):

    """chi(Delta) on a grid of offsets: wave packets in Delta carrying the given states"""

    Ds = np.round(np.arange(-3.0, 3.0 + ds / 2, ds), 10)

    chi = np.zeros((len(Ds), 4), complex)

    for c, st in zip(centres, states):

        chi += bump((Ds - c) / width)[:, None] * st[None, :]

    chi /= np.sqrt(np.sum(np.abs(chi)**2) * ds)

    keep = np.abs(chi).sum(1) > 0

    return Ds[keep], chi[keep]
