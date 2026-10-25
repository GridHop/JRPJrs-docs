# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 31 of 35 (1,798 words)

    pm = sum(np.vdot(w, w).real for o, w in full.items()

             if tuple(o[x] for x in I_ideal) == oI)

    devI = max(devI, abs(pI - pm))

print(f"    order ideal {I_ideal}: law from its own instruments vs marginal of full law, "

      f"max diff = {devI:.1e}")

# counterexample: two 'spacelike' slots acting on overlapping qubits

where_bad = {x: slots[x][1] for x in range(len(slots))}; where_bad[1] = 1   # slot 1 on (1,2)

o1 = (0, 1, 2, 3, 4, 5, 6, 7); o2 = (1, 0, 2, 3, 4, 5, 6, 7)

j1, j2 = joint(o1, instr, where_bad), joint(o2, instr, where_bad)

tvb = 0.5*sum(abs(np.vdot(j1[o], j1[o]).real - np.vdot(j2[o], j2[o]).real) for o in j1)

print(f"    non-commuting 'spacelike' pair: total variation between orders = {tvb:.3f}")



# ---- 15. equal ensembles, different realized-history measures (two unravellings)

plus = np.array([1, 1])/np.sqrt(2); minus = np.array([1, -1])/np.sqrt(2)

I1 = [np.diag([1, 0]), np.diag([0, 1])]

I2 = [np.eye(2)/np.sqrt(2), np.diag([1, -1])/np.sqrt(2)]

Xm = [np.outer(plus, plus), np.outer(minus, minus)]

rho = rq.normal(size=(2, 2)) + 1j*rq.normal(size=(2, 2))

rho = rho @ rho.conj().T; rho /= np.trace(rho)

ch = lambda I, r: sum(K @ r @ K.conj().T for K in I)

same_channel = np.allclose(ch(I1, rho), ch(I2, rho))

def jd(I):

    return np.array([[np.linalg.norm(M @ K @ plus)**2 for M in Xm] for K in I])

J1, J2 = jd(I1), jd(I2)

def mi(Jm):

    pa, pb = Jm.sum(1), Jm.sum(0)

    return sum(Jm[i, j]*np.log2(Jm[i, j]/(pa[i]*pb[j])) for i in range(2) for j in range(2)

               if Jm[i, j] > 1e-15)

print(f"15. same channel: {same_channel}; joint law of (first event, later X outcome):")

print(f"    {J1.round(3).tolist()} vs {J2.round(3).tolist()};")

print(f"    mutual information {mi(J1):.3f} vs {mi(J2):.3f} bits")



# ---- 16. imperfect quantum clocks: identity of events vs clock-relative timing

Mc, th = 32, 0.9

Sc = np.roll(np.eye(Mc), 1, axis=0)

Uc = Sc @ expm(-1j*th*(Sc + Sc.T))

step = np.abs(Uc[:, 0])**2                               # law of one recorded clock step

signed = [(m if m <= Mc//2 else m - Mc) for m in range(Mc)]

p_inv = sum(step[m] for m in range(Mc) if signed[m] < 0)

p_stall = step[0]

from scipy.special import jv

bes_inv = (1 - jv(0, 2*th)**2 - 2*jv(1, 2*th)**2)/2; bes_stall = jv(1, 2*th)**2

far = sum(step[m] for m in range(Mc) if abs(signed[m]) >= 8)

print(f"16. drifting quantum clock, exact on the 32-site ring (signed displacement in -15..16):")

print(f"    P(backward) = {p_inv:.9f}, P(no advance) = {p_stall:.9f};")

print(f"    infinite-lattice Bessel values {bes_inv:.9f}, {bes_stall:.9f}")

print(f"    max difference = {max(abs(p_inv-bes_inv), abs(p_stall-bes_stall)):.1e}; "

      f"P(|displacement| >= 8) = {far:.1e}")

per = [n % 2 for n in range(5)]

print(f"    period-2 counter readings at stages 0-4: {per};")

print("    superposed counter: reading at stage n is n or n+4, each with probability 0.5")





# ---- 17. gapless detectors on a free field: three-region (Sorkin-type) signaling test

# two-mode realization of the commutation pattern E_AB = 0, E_AC = E_CB = 1:

# phi_A = q1, phi_C = p1 + q2, phi_B = p2; vacuum state; Fock cutoff nc per mode

def sorkin(nc, lamA=0.9, lamC=0.8, lamB=0.7, kick=1.5):

    am = np.diag(np.sqrt(np.arange(1, nc)), 1); I_ = np.eye(nc)

    qm = (am + am.T)/np.sqrt(2); pm = 1j*(am.T - am)/np.sqrt(2)

    phA, phC, phB = np.kron(qm, I_), np.kron(pm, I_) + np.kron(I_, qm), np.kron(I_, pm)

    v0 = np.zeros(nc*nc, complex); v0[0] = 1

    def fn(Hm, f):

        w, V = np.linalg.eigh(Hm); return (V * f(w)) @ V.conj().T

    det = lambda ph, l: [fn(ph, lambda x: np.cos(l*x)), 1j*fn(ph, lambda x: np.sin(l*x))]

    gg = lambda x: 0.5*(1 + np.tanh(2*x))

    lud = lambda ph: [fn(ph, lambda x: np.sqrt(gg(x))), fn(ph, lambda x: np.sqrt(1 - gg(x)))]

    def bob(KA, KC, KB):

        pb = 0.0

        for Ka in KA:

            va = Ka @ v0

            for Kc in KC: pb += np.linalg.norm(KB[1] @ (Kc @ va))**2

        return pb

    KB = det(phB, lamB); Id = [np.eye(nc*nc)]; kA = [fn(phA, lambda x: np.exp(1j*kick*x))]

    out = {}

    for nm, KC in (('gapless', det(phC, lamC)), ('luders', lud(phC))):

        base = bob(Id, KC, KB)

        out[nm] = (base, bob(det(phA, lamA), KC, KB) - base, bob(kA, KC, KB) - base)

    return out

s40, s50 = sorkin(40), sorkin(50)

ana = 0.5 - 0.5*np.cos(2*0.7*0.8)*np.exp(-0.7**2)

print(f"17. three-region test, Bob's P(b=1) and its shift under Alice's detector / kick:")

print(f"    gapless Charlie: P = {s50['gapless'][0]:.10f} (analytic {ana:.10f}); shifts "

      f"{s50['gapless'][1]:.1e}, {s50['gapless'][2]:.1e}")

print(f"    unsharp Lueders Charlie: P = {s50['luders'][0]:.6f}; shifts "

      f"{s50['luders'][1]:.6f}, {s50['luders'][2]:.6f}")

print(f"    cutoff 40 vs 50: max change = "

      f"{max(abs(s40[k][i] - s50[k][i]) for k in s40 for i in range(3)):.1e}")



# ---- 18. Gaussian collapse of a smeared field at C (Weyl-diagonal): same three-region test

def gauss_test(nc=40, lamA=0.9, lamB=0.7, kick=1.5, sig=0.6, p_hit=1.0, dy=0.02):

    am = np.diag(np.sqrt(np.arange(1, nc)), 1); I_ = np.eye(nc)

    qm = (am + am.T)/np.sqrt(2); pm = 1j*(am.T - am)/np.sqrt(2)

    phA, phC, phB = np.kron(qm, I_), np.kron(pm, I_) + np.kron(I_, qm), np.kron(I_, pm)

    v0 = np.zeros(nc*nc, complex); v0[0] = 1

    def fn(Hm, f):

        w, V = np.linalg.eigh(Hm); return (V * f(w)) @ V.conj().T

    wC, VC = np.linalg.eigh(phC); ys = np.arange(-10, 10 + dy/2, dy)

    KB1 = 1j*fn(phB, lambda x: np.sin(lamB*x))

    def bob(KA):

        pb = 0.0

        for Ka in KA:

            w = VC.conj().T @ (Ka @ v0)

            if p_hit < 1: pb += (1 - p_hit)*np.linalg.norm(KB1 @ (VC @ w))**2

            for y in ys:

                k = (2*np.pi*sig**2)**-0.25*np.exp(-(wC - y)**2/(4*sig**2))

                pb += p_hit*dy*np.linalg.norm(KB1 @ (VC @ (k*w)))**2

        return pb

    detA = [fn(phA, lambda x: np.cos(lamA*x)), 1j*fn(phA, lambda x: np.sin(lamA*x))]

    base = bob([np.eye(nc*nc)])

    ana = 0.5 - 0.5*np.exp(-lamB**2)*((1 - p_hit) + p_hit*np.exp(-lamB**2/(2*sig**2)))

    shifts = (bob(detA) - base, bob([fn(phA, lambda x: np.exp(1j*kick*x))]) - base)

    return base, ana, shifts

for ph in (1.0, 0.4):

    b_, a_, sh = gauss_test(p_hit=ph)

    print(f"18. Gaussian collapse at C (hit probability {ph}): P = {b_:.10f} "

          f"(analytic {a_:.10f});")

    print(f"    shifts under Alice's detector / kick: {sh[0]:.1e}, {sh[1]:.1e}")

import sys, scipy

print(f"Environment: Python {sys.version.split()[0]}, NumPy {np.__version__}, "

      f"SciPy {scipy.__version__}")

print("Seeds: 7 (initial state; present state of item 11); 1000-1199 (item 9); "

      "2026 (items 14-15)")



Output:



1. reductions unitary; V_AB = explicit permutation: True

   groupoid law V_BC V_AB = V_AC: True

2. instrument complete: True | all generators G-invariant: True

3. intertwining V K^A V^dag = K^B for W and every Kraus operator: True

4. 4096 histories of 3 stages; max |p_A-p_B| = 2.78e-17, max |p_A-p_neutral| = 1.39e-17

   max(1-|<V phi_A|phi_B>|) = 6.66e-16, total prob = 1.000000000000

5. naive same-form frame-B rule: total-variation distance from correct record measure = 0.180

6. records [(0, 1, 1), (0, 2, 3)] vs [(0, 2, 3), (0, 1, 1)] -> same present ray: True

7. entanglement entropy: frame A 0.000 bits, frame B 1.000 bits

8. absolute collapse: ||(1-Pi) P_abs Psi|| / ||P_abs Psi|| = 0.894

9. continuous time: 200 trajectories, 1158 events; identical event records in A and B: True

   max(1-|<V psi_A|psi_B>|) at final time = 6.7e-16

10. generic parameters, 4096 three-stage histories: exact coincidences = 0; largest overlap = 0.9852

    minimum error probability for telling that pair apart (Helstrom) = 0.414

11. two different 3-stage histories, same present ray: |<end|Phi>| = 1.000000000000, 1.000000000000

    history probabilities 4.15e-05, 7.62e-05; overlap of the two initial states = 0.552

12a. finite width: both branches end at the same ray (|<end|Phi>| = 1.000000000000, 1.000000000000),

     probabilities 5.04e-05, 1.62e-03; next-event total variation = 0.1000 (lambda/6 = 0.1000)

12b. sharp, fixed initial state: same present ray: True; probabilities 8.254e-04, 1.238e-03;

     next-event total variation = 0.1000

13. conditioned on (1, 2, 0) at stage 3: Doob forward kernel vs conditioned law, max diff = 8.3e-17

14. causally local instruments: all 136 foliations (linear extensions), 256 outcome histories;

    max |p - p'| = 6.9e-18, max state deviation = 4.4e-16

    instruments changed outside the predecessor set of slot 3: max change = 7.8e-16

    order ideal [0, 1, 3]: law from its own instruments vs marginal of full law, max diff = 1.1e-16

    non-commuting 'spacelike' pair: total variation between orders = 0.165

15. same channel: True; joint law of (first event, later X outcome):

    [[0.25, 0.25], [0.25, 0.25]] vs [[0.5, 0.0], [0.0, 0.5]];

    mutual information 0.000 vs 1.000 bits

16. drifting quantum clock, exact on the 32-site ring (signed displacement in -15..16):

    P(backward) = 0.104042655, P(no advance) = 0.338161965;

    infinite-lattice Bessel values 0.104042655, 0.338161965

    max difference = 1.1e-16; P(|displacement| >= 8) = 7.4e-09

    period-2 counter readings at stages 0-4: [0, 1, 0, 1, 0];

    superposed counter: reading at stage n is n or n+4, each with probability 0.5

17. three-region test, Bob's P(b=1) and its shift under Alice's detector / kick:

    gapless Charlie: P = 0.3665447170 (analytic 0.3665447170); shifts -2.2e-16, -6.1e-16

    unsharp Lueders Charlie: P = 0.275038; shifts -0.021492, -0.046628

    cutoff 40 vs 50: max change = 8.8e-08

18. Gaussian collapse at C (hit probability 1.0): P = 0.3449027185 (analytic 0.3449027185);

    shifts under Alice's detector / kick: -3.3e-16, -5.0e-14

18. Gaussian collapse at C (hit probability 0.4): P = 0.2541731691 (analytic 0.2541731691);

    shifts under Alice's detector / kick: -8.3e-16, -2.0e-14

Environment: Python 3.13.16, NumPy 2.5.3, SciPy 1.18.1

Seeds: 7 (initial state; present state of item 11); 1000-1199 (item 9); 2026 (items 14-15)



----------------------------------------------------------------------------------------------------

Appendix C. Verification of the Collapse and Two-Clock Results

----------------------------------------------------------------------------------------------------



The results of §§13.8–13.11 and §14.5 are checked by two separate scripts, one for each branch of

the program, so that each can be rerun and audited independently of Appendix B. As there, the checks

confirm the analytical results in specific instances and guard against sign and ordering errors.

They do not prove anything about all states, all configurations, or the continuum. Table C.1 lists,

for each check, the quantity computed, the identity tested, the result, and the analytical argument

that establishes the identity.



Item  | Quantity and identity tested                   | Result                   | Proved in

------+------------------------------------------------+--------------------------+---------------

C1    | Unread Gaussian channel: Kraus integral and    | max dev 2.4 × 10⁻¹⁴ and  | Prop. 13.15

      | kick mixture vs exp(−(a − a′)²/(8σ²))          | 7.8 × 10⁻¹⁶              |

C2(a) | Position collapse, anharmonic potential: ΔE =  | 12 digits, both states   | Prop. 13.16(a)

      | ħ²/(8mσ²) in the ground state and in a random  | and cutoffs              |

      | state                                          |                          |

C2(b) | Two coupled modes, A linear: ΔE =              | 12 digits, both states   | Prop. 13.16(b)

      | −[A,[A,H]]/(8σ²) in the vacuum and in a random |                          |

      | state                                          |                          |

C2(c) | Lattice field: double commutator vs Fourier    | relative diff. 5 × 10⁻¹⁶ | Prop. 13.16(c)

      | formula                                        |                          |

C2(d) | ΔP(Λh) = Λ ΔP(h) under a boost; ΔP timelike    | 1.3 × 10⁻¹⁶; timelike    | Prop. 13.16(c)

C3(a) | Poisson counts in a box: mean and variance     | 96.00 and 96.35          | Def. 13.20

      | both equal to λ × area = 96                    |                          |

C3(b) | Probability of admissibility against the cell  | below the bound; 0.599   | Prop. 13.22

      | bound                                          | to 0.015                 |

C3(c) | Outcome covariance across linear extensions,   | max diff. 1.8 × 10⁻¹⁵    | Thm 13.21(a)

      | 300 admissible configurations                  |                          |

C3(d) | Direct Hilbert-space history laws: across      | 4.8 × 10⁻¹⁶; 1.8 × 10⁻¹⁴ | Thm 13.21(a)

      | linear extensions; vs closed-form              |                          |

      | characteristic function                        |                          |

C3(e) | Overlapping pair: variance shift E²/(4σ_1²);   | 10 digits; TV 0.057;     | Props 13.23,
