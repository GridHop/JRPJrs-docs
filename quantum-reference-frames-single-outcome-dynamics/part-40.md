# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 40 of 40 (862 words)





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
