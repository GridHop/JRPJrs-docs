# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 29 of 35 (1,799 words)

Krumm, M., Höhn, P. A., & Müller, M. P. (2021). Quantum reference frame transformations as

symmetries and the paradox of the third particle. Quantum, 5, 530.



Kuchař, K. V. (1992). Time and interpretations of quantum gravity. In G. Kunstatter, D. Vincent, &

J. Williams (Eds.), Proceedings of the 4th Canadian Conference on General Relativity and

Relativistic Astrophysics (pp. 211–314). World Scientific.



Last, G., & Penrose, M. (2017). Lectures on the Poisson Process. Cambridge University Press.



Lindblad, G. (1976). On the generators of quantum dynamical semigroups. Communications in

Mathematical Physics, 48, 119–130.



Loveridge, L., Miyadera, T., & Busch, P. (2018). Symmetry, reference frames, and relational

quantities in quantum mechanics. Foundations of Physics, 48, 135–198.



Merricks, T. (2007). Truth and Ontology. Oxford University Press.



Page, D. N., & Wootters, W. K. (1983). Evolution without evolution: Dynamics described by stationary

observables. Physical Review D, 27, 2885–2892.



Palin, J. R., Jr. (2026). Cosmic-Time Generative Presentism (CTGP) – explained. JRPJr’s docs,

https://gridhop.github.io/JRPJrs-docs/.



Palin, J. R., Jr. (2026). More Info: Causation, Information, Identity, and Becoming. JRPJr’s docs,

https://gridhop.github.io/JRPJrs-docs/.



Planck Collaboration (2020). Planck 2018 results. I. Overview and the cosmological legacy of Planck.

Astronomy & Astrophysics, 641, A1.



Polo-Gómez, J., Garay, L. J., & Martín-Martínez, E. (2022). A detector-based measurement theory for

quantum field theory. Physical Review D, 105, 065003.



Procopio, L. M., Moqanaki, A., Araújo, M., Costa, F., Alonso Calafell, I., Dowd, E. G., Hamel,

D. R., Rozema, L. A., Brukner, Č., & Walther, P. (2015). Experimental superposition of orders of

quantum gates. Nature Communications, 6, 7913.



Rideout, D. P., & Sorkin, R. D. (2000). Classical sequential growth dynamics for causal sets.

Physical Review D, 61, 024002.



Schwinger, J. (1948). Quantum electrodynamics. I. A covariant formulation. Physical Review, 74,

1439–1461.



Sider, T. (2001). Four-Dimensionalism: An Ontology of Persistence and Time. Oxford University Press.



Sorkin, R. D. (1993). Impossible measurements on quantum fields. In B. L. Hu & T. A. Jacobson

(Eds.), Directions in General Relativity, Vol. 2 (pp. 293–305). Cambridge University Press.



Tomonaga, S. (1946). On a relativistically invariant formulation of the quantum theory of wave

fields. Progress of Theoretical Physics, 1, 27–42.



Tumulka, R. (2006). A relativistic version of the Ghirardi–Rimini–Weber model. Journal of

Statistical Physics, 125, 821–840.



Vanrietvelde, A., Höhn, P. A., Giacomini, F., & Castro-Ruiz, E. (2020). A change of perspective:

switching quantum reference frames via a perspective-neutral framework. Quantum, 4, 225.



Vilasini, V., & Renner, R. (2024). Fundamental limits for realising quantum processes in spacetime.

Physical Review Letters, 133, 080201.



Wald, R. M. (1994). Quantum Field Theory in Curved Spacetime and Black Hole Thermodynamics.

University of Chicago Press.



Wiseman, H. M., & Milburn, G. J. (2010). Quantum Measurement and Control. Cambridge University

Press.



----------------------------------------------------------------------------------------------------

Appendix A. Frame-Relative Forms in the Ring Model

----------------------------------------------------------------------------------------------------



Frame coordinates: frame A uses (x, y) = (b−a, c−a); frame B uses (u, v) = (a−b, c−b); frame C uses

(p, q) = (a−c, b−c).



Invariant operator      | Frame A form        | Frame B form        | Frame C form

------------------------+---------------------+---------------------+--------------------

P_{AB}(r): b − a = r    | x = r               | u = −r              | q − p = r

P_{AC}(r): c − a = r    | y = r               | v − u = r           | p = −r

P_{BC}(r): c − b = r    | y − x = r           | v = r               | q = −r

S_A (shift A by +1)     | (x, y) → (x−1, y−1) | u → u+1             | p → p+1

S_B (shift B by +1)     | x → x+1             | (u, v) → (u−1, v−1) | q → q+1

S_C (shift C by +1)     | y → y+1             | v → v+1             | (p, q) → (p−1, q−1)



Table A.1. Frame-relative forms of the invariant operators used in the model. Each row is a single

invariant operator; the three entries are its conjugates under the frame changes of §6.2.



Frame changes: V_{A→B}|x, y⟩ = |−x, y−x⟩; V_{B→C}|u, v⟩ = |u−v, −v⟩; V_{A→C}|x, y⟩ = |−y, x−y⟩; and

V_{B→A} = V_{A→B}^{−1} maps |u, v⟩ to |−u, v−u⟩.



----------------------------------------------------------------------------------------------------

Appendix B. Verification Script and Output

----------------------------------------------------------------------------------------------------



The following Python script builds the model of Part III in the kinematical space, constructs the

reduction maps for all three frames, and performs the checks of Table 1. Each frame reduction is

represented by its inverse embedding J_F = R_F^{−1}, so that R_F = J_F† on H_phys. Items 1–8 concern

the discrete-stage model, item 9 the continuous-time model of §9, item 10 generic-parameter non-

injectivity (§8.3), item 11 strong non-supervenience (Proposition 4.12), item 12 the two

constructions of Proposition 11.4 for the history-dependent law of Example 11.3, item 13 the forward

representation of future conditioning (Proposition 11.1), item 14 realized-history consistency for

causally local instruments (Theorem 13.4) and consistency of the laws on nested order ideals

(Proposition 13.7), item 15 the equal-ensemble, different-history example (Proposition 13.2), item

16 the imperfect clocks of Proposition 14.2, with the clock probabilities computed exactly from the

32-site propagator and compared with the infinite-lattice Bessel expressions, item 17 the three-

region test of Theorem 13.9 and Example 13.10, and item 18 the same test with a Gaussian field

collapse at C (Proposition 13.12, Corollary 13.14).



Reproducibility. The script requires Python 3 with NumPy and SciPy; the output below was produced

with Python 3.13.16, NumPy 2.5.3, and SciPy 1.18.1. Random numbers come from NumPy’s default

generator, with seed 7 for the initial state and for the present state used in item 11, seeds

1000–1199 for the 200 trajectories of item 9, and seed 2026 for the random instruments, initial

state, and density operator of items 14 and 15. Parameters: N = 5, λ = 0.6, s = 0.8 (s = 0 and J = 0

in items 6 and 12b), pair weights (1/2, 1/4, 1/4) for the second instrument of item 12, J = 0.7, g =

0.9, τ = 0.5, Λ = 1.2, T = 5, with ħ = 1. Item 14 uses six qubits and eight random two-outcome

instruments arranged as a three-layer brickwork of nearest-neighbour slots; item 16 uses a ring of

32 clock sites with θ = 0.9; item 17 uses two oscillator modes in the vacuum, φ(f_A) = q_1, φ(f_C) =

p_1 + q_2, φ(f_B) = p_2, with λ_A = 0.9, λ_C = 0.8, λ_B = 0.7, kick α = 1.5, and Fock cutoffs of 40

and 50 quanta per mode; item 18 uses the same realization with σ = 0.6, hit probabilities 1 and 0.4,

cutoff 40, and the outcome integral evaluated on a grid of step 0.02 over [−10, 10]. Particles are

indexed 0, 1, 2 for A, B, C, and an event (i, j, d) in the output is a flash on the pair (i, j)

centred at separation d. Analytical results are proved in the text; the script checks them

numerically to double-precision tolerance.



# Numerical checks for the Z_N three-particle QRF model with

# flash-type stochastic collapse (companion to "Quantum Reference Frames

# and the Lucretian Truth Profile in CTGP").

import itertools

import numpy as np

from scipy.linalg import expm



N = 5                      # sites on the ring Z_N

lam = 0.6                  # hit probability per stage

s = 0.8                    # flash width (in lattice units)

Jhop, g, tau = 0.7, 0.9, 0.5

rng = np.random.default_rng(7)



def idx(a, b, c): return ((a % N) * N + (b % N)) * N + (c % N)

def ridx(x, y): return (x % N) * N + (y % N)

D, d2 = N**3, N**2



# global translation U_g and projector onto the invariant (physical) sector

def U(gg):

    M = np.zeros((D, D))

    for a, b, c in itertools.product(range(N), repeat=3):

        M[idx(a+gg, b+gg, c+gg), idx(a, b, c)] = 1

    return M

Pi = sum(U(gg) for gg in range(N)) / N



# embeddings J_F : reduced space of frame F -> physical sector (J_F = R_F^{-1})

def J(frame):

    M = np.zeros((D, d2))

    for f in range(N):

        for x, y in itertools.product(range(N), repeat=2):

            if frame == 'A': k = idx(f, f+x, f+y)      # (x_B, x_C) rel. to A

            if frame == 'B': k = idx(f+x, f, f+y)      # (x_A, x_C) rel. to B

            if frame == 'C': k = idx(f+x, f+y, f)      # (x_A, x_B) rel. to C

            M[k, ridx(x, y)] += 1/np.sqrt(N)

    return M

JA, JB, JC = J('A'), J('B'), J('C')

for M in (JA, JB, JC):

    assert np.allclose(M.T @ M, np.eye(d2)) and np.allclose(M @ M.T, Pi)

V_AB, V_BC, V_AC = JB.T @ JA, JC.T @ JB, JC.T @ JA

perm = np.zeros((d2, d2))

for x, y in itertools.product(range(N), repeat=2):

    perm[ridx(-x, y-x), ridx(x, y)] = 1

print("1. reductions unitary; V_AB = explicit permutation:", np.allclose(V_AB, perm))

print("   groupoid law V_BC V_AB = V_AC:", np.allclose(V_BC @ V_AB, V_AC))



# invariant generators: hopping + relational potential, and relational flashes

def shift(i):

    M = np.zeros((D, D))

    for a, b, c in itertools.product(range(N), repeat=3):

        t = [a, b, c]; t2 = list(t); t2[i] += 1

        M[idx(*t2), idx(*t)] = 1

    return M

def P(i, j, r):            # projector onto x_j - x_i = r (mod N)

    M = np.zeros((D, D))

    for t in itertools.product(range(N), repeat=3):

        if (t[j]-t[i]) % N == r % N: M[idx(*t), idx(*t)] = 1

    return M

pairs = [(0, 1), (0, 2), (1, 2)]                       # (A,B), (A,C), (B,C)

H = sum(-Jhop*(shift(i)+shift(i).T) for i in range(3)) \

    + sum(g*np.cos(2*np.pi*r/N)*P(i, j, r) for (i, j) in pairs for r in range(N))

W = expm(-1j*tau*H)

def wfun(r, width):

    dist = np.minimum(r % N, (-r) % N)

    return np.exp(-dist**2/(2*width**2)) if width > 0 else (dist == 0)*1.0

def kraus(width, lam_=lam):

    ws = np.array([wfun(r, width) for r in range(N)]); ws = ws/ws.sum()

    F = {'none': np.sqrt(1-lam_)*np.eye(D)}

    for (i, j) in pairs:

        for dd in range(N):

            F[(i, j, dd)] = np.sqrt(lam_/3)*sum(np.sqrt(ws[(r-dd) % N])*P(i, j, r)

                                                for r in range(N))

    return F

F = kraus(s)

comp = sum(K.conj().T @ K for K in F.values())

inv = all(np.allclose(U(1) @ K, K @ U(1)) for K in list(F.values()) + [W])

print("2. instrument complete:", np.allclose(comp, np.eye(D)), "| all generators G-invariant:", inv)



red = lambda O, JF: JF.T @ O @ JF

WA, WB = red(W, JA), red(W, JB)

FA = {k: red(K, JA) for k, K in F.items()}; FB = {k: red(K, JB) for k, K in F.items()}

ok = np.allclose(V_AB @ WA @ V_AB.T, WB) and \

     all(np.allclose(V_AB @ FA[k] @ V_AB.T, FB[k]) for k in F)

print("3. intertwining V K^A V^dag = K^B for W and every Kraus operator:", ok)



# exhaustive record distribution over n stages, frame A vs frame B vs neutral

def record_dist(psi0, Wm, Fm, n):

    out = {}

    def rec(psi, hist, p):

        if len(hist) == n: out[hist] = (p, psi); return

        phi = Wm @ psi

        for k, K in Fm.items():

            v = K @ phi; q = np.vdot(v, v).real

            if q > 1e-14: rec(v/np.sqrt(q), hist+(k,), p*q)

    rec(psi0, (), 1.0); return out

phiA0 = rng.normal(size=d2) + 1j*rng.normal(size=d2); phiA0 /= np.linalg.norm(phiA0)
