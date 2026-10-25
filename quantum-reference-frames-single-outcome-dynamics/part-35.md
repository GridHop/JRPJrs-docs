# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 35 of 35 (1,648 words)

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





print('Case 1: one record written by an interaction keyed to clock A')

HS = kron(0.35 * sz, I2)

V1 = kron(P1, sx) + 0.6 * kron(sx, I2)

g1 = pulse(np.pi / 2)

Us = propagate(lambda s: HS + g1(s) * V1)                  # independent of Delta here

E = kron(I2, P1)                                           # the record reads 1

Ds, chi = packets([0.3, 1.4], 0.25, [system_state(), system_state()])

sstar = 1.0

O = lambda c: Us[at(sstar)].conj().T @ E @ Us[at(sstar)] @ c

P_phys = sum(np.vdot(O(c), O(c)).real for c in chi) * ds





def P_A(tau):        # integral over t_B = tau - Delta of |E Psi(tau, t_B)|^2

    return sum(np.linalg.norm(E @ Us[at(tau)] @ c)**2 for c in chi) * ds





def P_B(taup):       # integral over t_A = taup + Delta of |E Psi(t_A, taup)|^2

    return sum(np.linalg.norm(E @ Us[at(taup + D)] @ c)**2 for D, c in zip(Ds, chi)) * ds





print('   offsets Delta in [%.2f, %.2f]; interaction in A-time [0, 1]' % (Ds.min(), Ds.max()))

print('   P_phys = %.12f   P_A(2.0) = %.12f   P_A(4.0) = %.12f' % (P_phys, P_A(2.0), P_A(4.0)))

print('   P_B(%.2f) = %.12f   P_B(3.0) = %.12f' % (1 - Ds.min(), P_B(1 - Ds.min()), P_B(3.0)))

print('   A-time: ' + ', '.join('P_A(%.1f) = %.6f' % (t, P_A(t)) for t in (-0.5, 0.0, 0.5, 1.0)))

print('   B-time: ' + ', '.join('P_B(%.1f) = %.6f' % (t, P_B(t)) for t in (-1.0, -0.4, 0.2, 0.6)))

print('   O is a projector on the sector: max |O^2 - O| = %.1e'

      % max(np.abs(O(O(c)) - O(c)).max() for c in chi))



print('Case 2: interaction 1 (keyed to A) rotates S; interaction 2 (keyed to B) records S')

V1, V2 = kron(sy, I2), kron(P1, sx)

g1, g2 = pulse(np.pi / 8), pulse(np.pi / 2)

psi_neg, psi_pos = system_state(), system_state()

Ds, chi = packets([-1.6, 1.6], 0.25, [psi_neg, psi_pos])

UD = [propagate(lambda s, D=D: g1(s) * V1 + g2(s - D) * V2) for D in Ds]

sstar = 1.0 + Ds.max()

P_phys = sum(np.linalg.norm(E @ U[at(sstar)] @ c)**2 for U, c in zip(UD, chi)) * ds

PA = sum(np.linalg.norm(E @ U[at(4.0)] @ c)**2 for U, c in zip(UD, chi)) * ds

taup = sstar - Ds.min()

PB = sum(np.linalg.norm(E @ U[at(taup + D)] @ c)**2 for U, D, c in zip(UD, Ds, chi)) * ds

G1, G2 = expm(-1j * np.pi / 8 * V1), expm(-1j * np.pi / 2 * V2)

mu = [np.sum(np.abs(chi[Ds < 0])**2) * ds, np.sum(np.abs(chi[Ds > 0])**2) * ds]

p_rec_first = np.linalg.norm(E @ G1 @ G2 @ psi_neg)**2

p_rot_first = np.linalg.norm(E @ G2 @ G1 @ psi_pos)**2

print('   P_phys = %.12f   P_A(4.0) = %.12f   P_B(%.2f) = %.12f' % (P_phys, PA, taup, PB))

print('   definite orders: record first %.6f (weight %.4f), rotation first %.6f (weight %.4f)'

      % (p_rec_first, mu[0], p_rot_first, mu[1]))

print('   weighted mixture of the two definite orders = %.12f'

      % (mu[0] * p_rec_first + mu[1] * p_rot_first))



print('Case 3: the same interactions, an offset-coherent observable (H_S = 0)')

psi0 = system_state()

Ds, chi = packets([-1.6, 1.6], 0.25, [psi0, psi0])

UD = [propagate(lambda s, D=D: g1(s) * V1 + g2(s - D) * V2) for D in Ds]

fplus = bump((Ds + 1.6) / 0.25) + bump((Ds - 1.6) / 0.25)

fplus = fplus / np.sqrt(np.sum(fplus**2) * ds)                # coherent superposition of offsets

amp_phys = sum(fp * (U[at(sstar)] @ c) for fp, U, c in zip(fplus, UD, chi)) * ds

amp_A = sum(fp * (U[at(4.0)] @ c) for fp, U, c in zip(fplus, UD, chi)) * ds

amp_B = sum(fp * (U[at(taup + D)] @ c) for fp, U, D, c in zip(fplus, UD, Ds, chi)) * ds

W1, W2 = G1 @ G2, G2 @ G1                       # offset -1.6: record first; +1.6: rotation first

pred = 0.5 * (1 + np.vdot(W1 @ psi0, W2 @ psi0).real)

mix = 0.0

for sgn in (-1, 1):                             # incoherent mixture of the two offsets

    sel = np.sign(Ds) == sgn

    ch = chi * sel[:, None] / np.sqrt(np.sum(np.abs(chi[sel])**2) * ds)

    a_ = sum(fp * (U[at(sstar)] @ c) for fp, U, c in zip(fplus, UD, ch)) * ds

    mix += 0.5 * np.vdot(a_, a_).real

print('   P(+): clock-neutral %.12f, relative to A %.12f, relative to B %.12f'

      % (np.vdot(amp_phys, amp_phys).real, np.vdot(amp_A, amp_A).real, np.vdot(amp_B, amp_B).real))

print('   (1 + Re<W1 psi, W2 psi>)/2 = %.12f; incoherent mixture of offsets gives %.12f'

      % (pred, mix))



Output:



Case 1: one record written by an interaction keyed to clock A

   offsets Delta in [0.06, 1.64]; interaction in A-time [0, 1]

   P_phys = 0.139627690767   P_A(2.0) = 0.139627690767   P_A(4.0) = 0.139627690767

   P_B(0.94) = 0.139627690767   P_B(3.0) = 0.139627690767

   A-time: P_A(-0.5) = 0.000000, P_A(0.0) = 0.000000, P_A(0.5) = 0.153583, P_A(1.0) = 0.139628

   B-time: P_B(-1.0) = 0.021295, P_B(-0.4) = 0.032189, P_B(0.2) = 0.145553, P_B(0.6) = 0.144791

   O is a projector on the sector: max |O^2 - O| = 4.0e-15

Case 2: interaction 1 (keyed to A) rotates S; interaction 2 (keyed to B) records S

   P_phys = 0.706791827009   P_A(4.0) = 0.706791827009   P_B(4.68) = 0.706791827009

   definite orders: record first 0.868488 (weight 0.5000), rotation first 0.545095 (weight 0.5000)

   weighted mixture of the two definite orders = 0.706791827009

Case 3: the same interactions, an offset-coherent observable (H_S = 0)

   P(+): clock-neutral 0.926776695297, relative to A 0.926776695297, relative to B 0.926776695297

   (1 + Re<W1 psi, W2 psi>)/2 = 0.926776695297; incoherent mixture of offsets gives 0.500000000000
