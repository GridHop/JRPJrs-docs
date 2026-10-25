# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 16 of 35 (1,793 words)

    Minkowski space in its Fock representation, with energy–momentum P^μ, a real test function h

    with Eh ≠ 0, and A = φ(h), every state ρ of finite energy, Tr(ρ H) < ∞, satisfies Tr(N(ρ) P^μ) =

    Tr(ρ P^μ) + ΔP^μ(h) for all four generators, where



        ΔP^μ(h) = (1/(4σ²)) ∫ dμ_m(k) k^μ |ĥ(k)|²,     dμ_m(k) = d³k / ((2π)³ 2ω_k),



    with k⁰ = ω_k = (|k|² + m²)^{1/2} and ĥ(k) = ∫ h(x) e^{ik·x} d⁴x. Equivalently, ΔP^μ(h) is the

    conserved energy–momentum of the classical solution Eh, divided by 4σ². It does not depend on

    the state; it is unchanged when h is translated; it transforms as a four-vector, ΔP(h ∘ Λ^{−1})

    = Λ ΔP(h); and it is future-directed and timelike.



    (d) Curved backgrounds. Let φ be the minimally coupled free scalar field of mass m ≥ 0 on a

    four-dimensional globally hyperbolic spacetime, ω a Hadamard state, and h a real test function.

    Then the state ω_N = ω ∘ N* after an unread Gaussian collapse of φ(h) is Hadamard, its

    symmetrized two-point function is that of ω plus (Eh ⊗ Eh)/(4σ²), and its renormalized

    stress–energy tensor, defined by Hadamard point-splitting, is



        ⟨T_μν⟩_{ω_N} = ⟨T_μν⟩_ω + T^cl_μν[Eh] / (4σ²),



    where T^cl_μν[u] = ∇_μu ∇_νu − ½ g_μν (∇^αu ∇_αu − m²u²) is the classical stress–energy tensor,

    in signature (+, −, −, −).



Proof. In each case N*(B) = ∫ γ(t) e^{itA} B e^{−itA} dt by Proposition 13.15(b). (a) The unitary

e^{−itQ} preserves the form domain: it commutes with V, and the Weyl relation e^{itQ} P e^{−itQ} = P

− ħt gives P e^{−itQ} = e^{−itQ}(P − ħt) on D(P). Hence q(e^{−itQ}ψ) = q(ψ) − (ħt/m)⟨ψ, Pψ⟩ +

ħ²t²‖ψ‖²/(2m), where ⟨ψ, Pψ⟩ is finite on the form domain. The energy functional ℰ is affine, and,

being a supremum of normal functionals given by spectral truncations of the bounded-below operator

H, it satisfies ℰ(∫ γ(t) ρ_t dt) = ∫ γ(t) ℰ(ρ_t) dt by monotone convergence. Averaging over t, with

γ of mean zero and variance 1/(4σ²), gives the result. (b) The unitary e^{itA} is a Weyl operator of

the canonical system. It preserves the form domain of H and shifts R by t times a constant vector s,

so H becomes H + t L + t² H(s), with L linear in R and H(s) the value of the quadratic form on s.

Averaging gives H(s)/(4σ²), and differentiating twice at t = 0 shows that −[A, [A, H]] = 2H(s). (c)

For real t, e^{itφ(h)} φ(f) e^{−itφ(h)} = φ(f) − t E(h, f), so conjugation by e^{itφ(h)} displaces

the field by the classical solution −t Eh. Under a displacement by a classical solution u of finite

energy, the normal-ordered generators transform as P^μ ↦ P^μ + t L^μ + t² P^μ[u], with L^μ linear in

the creation and annihilation operators and P^μ[u] the classical energy–momentum of u. Because ω_k ≥

|k^i| mode by mode, −H ≤ P^i ≤ H as quadratic forms, so a state of finite energy has finite

expectations of all four generators, and N(ρ) again has finite energy. The linear terms have the

form L^μ = a(g_μ) + a(g_μ)*, with ω^{−1/2} g_μ square-integrable because ĥ decays rapidly on the

mass shell, and the bound |Tr(ρ a(g))| ≤ ‖ω^{−1/2} g‖ Tr(ρ H)^{1/2} makes their expectations finite.

Averaging over t therefore gives ΔP^μ = P^μ[Eh]/(4σ²). In the mode expansion, φ(h) = ∫ dμ_m(k)

(ĥ(k)* a_k + ĥ(k) a_k†) with [a_k, a_q†] = (2π)³ 2ω_k δ³(k − q), and the same computation gives the

stated integral. Translating h multiplies ĥ by a phase. Since ĥ ∘ Λ^{−1} is the transform of h ∘

Λ^{−1} and dμ_m is Lorentz-invariant, ΔP transforms as a four-vector. The Fourier transform of Eh is

proportional to ĥ on the mass shell, so Eh ≠ 0 exactly when ĥ is not identically zero there. Then ΔP

is an integral of future-directed causal vectors with a nonnegative weight that is not almost

everywhere zero. For m > 0 these vectors are timelike. For m = 0 they are null, but ĥ is real-

analytic and the future light cone in 3 + 1 dimensions, with its vertex removed, is connected, so ĥ

is nonzero on an open subset of the cone containing non-parallel null directions, and their sum is

timelike. (d) By Proposition 13.12, ω_N(W(f)) = exp(−E(h, f)²/(8σ²)) ω(W(f)). Differentiating

ω_N(W(sf + tg)) twice at s = t = 0 shows that the symmetrized two-point function changes by E(h, f)

E(h, g)/(4σ²), whose integral kernel is (Eh)(x)(Eh)(y)/(4σ²), a smooth function because Eh is a

smooth solution; the antisymmetric part, iE/2, is unchanged. Adding a smooth symmetric kernel

preserves the wavefront-set condition that defines Hadamard states. In Hadamard point-splitting, the

renormalized stress–energy tensor is obtained by applying a fixed bidifferential operator to the

two-point function minus a state-independent Hadamard parametrix, taking the coincidence limit, and

adding local curvature terms that are the same for every state (Wald 1994; Hollands & Wald 2015).

The difference between ω_N and ω is therefore that operator applied to (Eh ⊗ Eh)/(4σ²), whose

coincidence limit is T^cl_μν[Eh]/(4σ²). □



The dimension matters for the last statement of (c). In 1 + 1 dimensions the same formula holds with

d³k/(2π)³ replaced by dk/(2π), and ΔP(h) is timelike if m > 0. For m = 0, however, the light cone

consists of two null rays, ĥ can vanish on one of them, and ΔP(h) is then null.



Three consequences follow. First, the exact cost agrees with the standard collapse-model result.

With σ² = r_C²/2, K_y is the GRW localization operator of width r_C, and part (a) gives 3ħ²/(4m

r_C²) per hit, hence 3λħ²/(4m r_C²) per unit time at hit rate λ (compare Bassi et al. 2013). Second,

part (b) is the exact case of the weak-collapse expansion N* = exp(−ad_A²/(8σ²)), with ad_A(B) = [A,

B], which gives N*(H) − H = −(1/(8σ²)) [A, [A, H]] + O(σ^{−4}) whenever the series makes sense. The

expansion terminates when [A, [A, H]] is a multiple of the identity. Third, the field cost grows as

the collapse region shrinks. For a massless field and h_ℓ(x) = ℓ^{−4} χ(x/ℓ), substituting k → k/ℓ

gives ΔP(h_ℓ) = ℓ^{−3} ΔP(χ) at fixed σ, while the vacuum variance of φ(h_ℓ) scales as ℓ^{−2}. At a

fixed ratio ε of σ to the vacuum spread of φ(h_ℓ), the energy injected per collapse is therefore

proportional to ħc/(ε² ℓ). Part (d) gives the corresponding local statement on a curved background.



In the numerical checks (Appendix C.1, items C1 and C2), the Kraus integral and the Gaussian mixture

of kicks both reproduce the multiplier exp(−(a − a′)²/(8σ²)), to 2.4 × 10⁻¹⁴ and 7.8 × 10⁻¹⁶. For a

particle with an anharmonic potential, the energy increment is ħ²/(8mσ²) to twelve digits, in the

ground state and in a random state alike. On a lattice field, the double-commutator and Fourier

expressions agree to 5 × 10⁻¹⁶. For a massive field in 1 + 1 dimensions, under a boost of rapidity

0.5, ΔP transforms as a four-vector to 1.3 × 10⁻¹⁶.



13.9 Algebra Preservation: A Sufficient Condition for No-Signaling



The proofs of Theorems 13.9(b) and 13.13(b) use the free field only to show that a certain algebra

of observables is carried into itself by the operations between the one being tested and the

targets. That structure can be isolated, and it does not depend on central commutators.



Theorem 13.17 (No-signaling by algebra preservation). Let ω be a normal state on B(H), and let o_1,

…, o_n be operations performed in this order, each a normal instrument I_m with a standard Borel

outcome space (Ω_m, 𝔉_m). Write I_m*(Δ) for the Heisenberg dual of I_m(Δ) and N_m* = I_m*(Ω_m) for

the dual of its unread channel. For a set X of target operations and Borel sets Δ_x, x ∈ X, the

unconditioned joint probability of the target outcomes is



        P(Δ_x : x ∈ X) = ω(T_1*(T_2*(⋯ T_n*(1) ⋯))),



where T_m* = I_m*(Δ_m) if m ∈ X and T_m* = N_m* otherwise, so that the outcomes of all non-target

operations are summed over rather than conditioned on. Fix a non-target operation j, and suppose

there is a linear subspace 𝔐 ⊆ B(H) containing 1 such that:



    (i) I_x*(Δ)(𝔐) ⊆ 𝔐 for every target operation x performed after j and every Δ;



    (ii) N_k*(𝔐) ⊆ 𝔐 for every non-target operation k ≠ j performed after j;



    (iii) N_j*(B) = B for every B ∈ 𝔐.



Then the joint law of the target outcomes is the same whether j is performed, omitted, or replaced

by any other operation satisfying (iii). Condition (iii) holds in particular whenever j has Kraus

operators in the commutant 𝔐′, and operations performed before j are unrestricted.



Proof. Let j be the m-th operation and set B = T_{m+1}*(⋯ T_n*(1) ⋯). Starting from 1 ∈ 𝔐 and

applying the maps T_n*, …, T_{m+1}* in turn, conditions (i) and (ii) keep every intermediate

operator in 𝔐, so B ∈ 𝔐. By (iii), T_j*(B) = N_j*(B) = B, which is the value obtained when j is

omitted, and the same holds for any replacement satisfying (iii). The remaining maps T_{m−1}*, …,

T_1* and the state ω are unchanged. If K_y ∈ 𝔐′ for almost every outcome y of j, then N_j*(B) = ∫

K_y† B K_y dν(y) = B ∫ K_y† K_y dν(y) = B. □



Corollary 13.18 (Random local automorphisms). Suppose that every unread non-target operation k

performed after j is an average of automorphisms, N_k*(B) = ∫ U_k(t)* B U_k(t) dμ_k(t) with

unitaries U_k(t) and a probability measure μ_k, and that 𝔐 is σ-weakly closed and mapped into itself

by B ↦ U_k(t)* B U_k(t) for μ_k-almost every t. Then (ii) holds. For a free field, Gaussian

collapses and random displacements are of this form with U_k(t) = e^{−itφ(h_k)} or W(h), each of

which multiplies every Weyl operator by a phase. They therefore preserve the von Neumann algebra 𝔐_X

generated by { W(g) : g ∈ V_X }, for every target set X, and Theorem 13.17 gives Theorem 13.13(b)

for these operations.



Proof. A weak integral of a bounded measurable family in a σ-weakly closed subspace lies in that

subspace, since a normal functional that vanishes on the subspace vanishes on every member of the

family and hence on the integral. □



The theorem locates the role of relativistic causality exactly. Microcausality supplies (iii): if 𝔐

is generated by observables localized in the target regions and j is localized in a region causally

separated from all of them, the Kraus operators of j commute with 𝔐. It does not supply (ii), which

is a condition on the composed dynamics of the intervening operations. Example 13.10 is a case in

which (ii) fails. The unread Lüders instrument at C maps W(s f_B) to W(s f_B) G(φ(f_C)) for a non-
