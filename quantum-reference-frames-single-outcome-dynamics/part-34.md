# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 34 of 35 (1,800 words)

var_alone = (np.trace(rho @ A2 @ A2) - np.trace(rho @ A2)**2).real

print('   (e) overlapping pair, E(h1, h2) = %.6f:' % E[0, 1])

print('       increase of Var(y2) caused by collapse 1: %.10f; E^2/(4 sigma1^2) = %.10f'

      % (var_after - var_alone, E[0, 1]**2 / (4 * sg[0]**2)))

l12, l21 = binned_law((0, 1), eigs, sg, 2), binned_law((1, 0), eigs, sg, 2)

print('       binned joint laws for the two orders: total-variation distance %.4f'

      % (0.5 * np.abs(l12 - l21).sum()))

A1 = cu[0] * qo + cw[0] * po

r12 = dephase(dephase(rho, A1, sg[0]), A2, sg[1])

r21 = dephase(dephase(rho, A2, sg[1]), A1, sg[0])

print('       unread channels in the two orders: max difference of the final states %.1e'

      % np.abs(r12 - r21).max())

eta, nbad, nchg, maxd = 0.6, 0, 0, 0.0

while nbad < 300:

    pts = rng.uniform(0, 2.0, size=(rng.poisson(6.0), 2))

    if len(pts) < 2 or topo(relation(pts, dl)) is not None:

        continue

    n = len(pts)

    R, E = geometry(pts, dl, scale)

    sg = np.full(n, 0.8)

    Sig = 0.5 * absE(E) + 0.3 * np.eye(n)

    o1 = list(np.argsort(pts[:, 0]))

    o2 = list(np.argsort(np.cosh(eta) * pts[:, 0] - np.sinh(eta) * pts[:, 1]))

    dC = np.abs(cov_closed(o1, E, Sig, sg) - cov_closed(o2, E, Sig, sg)).max()

    nbad, nchg, maxd = nbad + 1, nchg + (dC > 1e-12), max(maxd, dC)

print('   (f) %d non-orderable configurations ordered by centre time in two frames' % nbad)

print('       (relative rapidity 0.6): laws differ in %d, max covariance difference %.3f'

      % (nchg, maxd))

print('   (g) centre-time order is a linear extension of the causal order in %d of the %d'

      % (t_ext, nconf))

print('       orderable configurations of item (c)')





# (h) cosmological-time-ordered collapses on a non-orderable Sorkin-type configuration:

# j (tested operation), c1 and c2 (overlapping law collapses), y (target), applied in order

# of t. Light-cone centres (u, v) give j < c1 < y causally, j and y causally separated.

uvc = np.array([[0.0, 0.0], [-0.525, 1.2], [-0.225, 1.05], [-1.05, 2.3]])

pts = np.column_stack([(uvc[:, 0] + uvc[:, 1]) / 2, (uvc[:, 1] - uvc[:, 0]) / 2])

R, E = geometry(pts, dl, 8.0)

print('   (h) order j, c1, c2, y by t; c1 and c2 overlap; E(h_j, h_c1) = %.4f, E(h_c1, h_y) = %.4f,'

      % (E[0, 1], E[1, 3]))

print('       E(h_c1, h_c2) = %.4f, E(h_j, h_y) = %.1f' % (E[1, 2], abs(E[0, 3])))

gl = lambda x: (1 + np.tanh(2 * x)) / 2

for nc in (36, 44):

    a1, a2 = modes(nc, 2)

    q1, q2 = [(a + a.T) / np.sqrt(2) for a in (a1, a2)]

    p1, p2 = [1j * (a.T - a) / np.sqrt(2) for a in (a1, a2)]

    # two-mode realization of the commutation data with phi_j on mode 1 and phi_y on mode 2

    phis = [q1, E[1, 2] / E[0, 2] * q1 + E[0, 1] * p1 - E[1, 3] * p2,

            E[0, 2] * p1 - E[2, 3] * p2, q2]

    for i in range(4):

        for k in range(4):

            c = (phis[i] @ phis[k] - phis[k] @ phis[i])[:8, :8]

            assert np.abs(c - 1j * E[i, k] * np.eye(8)).max() < 1e-9

    ey = eigh(phis[3])

    w1, V1 = eigh(phis[1])

    w0, V0 = eigh(phis[0])



    def target_law(at_j, luders):

        rho = np.zeros((nc * nc, nc * nc), complex)

        rho[0, 0] = 1

        if at_j == 'kick':

            U = expm(3j * phis[0])

            rho = U @ rho @ U.conj().T

        elif at_j == 'collapse':

            rho = dephase(rho, phis[0], 0.8)

        elif at_j == 'luders':                  # an operation outside the Weyl-diagonal class

            K = [V0 @ np.diag(np.sqrt(gl(w0))) @ V0.conj().T,

                 V0 @ np.diag(np.sqrt(1 - gl(w0))) @ V0.conj().T]

            rho = sum(k @ rho @ k.conj().T for k in K)

        if luders:

            K = [V1 @ np.diag(np.sqrt(gl(w1))) @ V1.conj().T,

                 V1 @ np.diag(np.sqrt(1 - gl(w1))) @ V1.conj().T]

            rho = sum(k @ rho @ k.conj().T for k in K)

        else:

            rho = dephase(rho, phis[1], 0.8)

        rho = dephase(rho, phis[2], 0.9)

        return np.array([bin_probability(rho, ey, b, 1.0) for b in range(4)])



    base = target_law(None, False)

    dk = np.abs(target_law('kick', False) - base).max()

    dc = np.abs(target_law('collapse', False) - base).max()

    lb = target_law(None, True)

    dlk = np.abs(target_law('kick', True) - lb).max()

    print('       cutoff %d: Gaussian c1: change of the target law by a kick at j %.1e,' % (nc, dk))

    dlj = np.abs(target_law('luders', False) - base).max()

    print('       by a collapse at j %.1e; target law sums to %.12f' % (dc, base.sum()))

    print('       unsharp Lueders instrument at j (not Weyl-diagonal): change %.1e' % dlj)

    print('       unsharp Lueders c1 (negative control): change by the kick, largest bin %.7f'

          % dlk)





print('C4. Gapless pointer realization of the collapses (Proposition 13.31)')

# Each collapse is realized by a pointer (q_k, p_k) with no Hamiltonian, coupled through the

# density p_k h_k(x) phi(x). The matrix M below is Gamma_kl = E_ret(h_k, h_l), the retarded

# part of E, with E_ret(t, x) = -theta(u) theta(v)/2, so that E = Gamma - Gamma^T.





def Mret(pts, dl, scale):

    u, v = pts[:, 0] - pts[:, 1], pts[:, 0] + pts[:, 1]

    n = len(pts)

    M = np.zeros((n, n))

    for k in range(n):

        for l in range(n):

            M[k, l] = -scale**2 / 32 * ((1 + Sfun((u[k] - u[l]) / dl))

                                        * (1 + Sfun((v[k] - v[l]) / dl)))

    return M





def ordered_sums(pts, dl, scale, nn, eta):

    """sum of E(x_a - x_b) w_a w_b over node pairs with x_a later than x_b in the time

    cosh(eta) t - sinh(eta) x: the phase of the time-ordered product of the couplings"""

    z, wz = np.polynomial.legendre.leggauss(nn)

    Zu, Zv = np.meshgrid(z, z, indexing='ij')

    w = (scale / 2) * np.outer(beta(z) * wz, beta(z) * wz).ravel()

    nodes = [((t - x) + dl * Zu.ravel(), (t + x) + dl * Zv.ravel()) for t, x in pts]

    T = np.zeros((len(pts), len(pts)))

    for k in range(len(pts)):

        for l in range(len(pts)):

            for c in range(0, len(w), 512):

                du = nodes[k][0][c:c + 512, None] - nodes[l][0][None, :]

                dv = nodes[k][1][c:c + 512, None] - nodes[l][1][None, :]

                later = np.cosh(eta) * (du + dv) - np.sinh(eta) * (dv - du) > 0

                Ev = np.where(later, -(np.sign(du) + np.sign(dv)) / 4, 0.0)

                T[k, l] += w[c:c + 512] @ Ev @ w

    return T





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
