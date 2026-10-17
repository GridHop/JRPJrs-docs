# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 28 of 40 (1,614 words)

14.4 A Proposed Temporal Identification Criterion



Definition 14.3 (Temporal cross-frame identification; a proposal). A clock-relative description

consists of a valid clock reduction, which may be partial, state-dependent, or defined only on a

subspace, together with its domain of physical states. Two clock-relative descriptions identify the

same CTGP history when (i) the physical state lies in both domains, (ii) they arise from the same

realized event history, and (iii) they agree on every clock-neutral event proposition, that is,

every Tier 1 proposition stated without reference to clock readings, that can be evaluated in both.

A family of clock-relative descriptions is consistent when every pair satisfies (i)–(iii) on the

intersection of their domains, and when, wherever three descriptions share a domain, the

correspondences between events that they induce compose.



The criterion deliberately does not require that two clocks assign the same time coordinates to

events, nor that their conditional state vectors coincide. It is the temporal counterpart of

Criterion 5.5, with clock-neutral event propositions in place of the translated truth profile.

Criterion 5.5 identifies descriptions through a single global orbit, which presupposes globally

defined unitary reductions. Definition 14.3 replaces that orbit by a family of overlapping

admissible descriptions with consistency conditions on their common domains, which is what is needed

when temporal reductions are partial, state-dependent, or available only locally (§14.1).



Conjecture 14.4 (Clock-neutral realized-history equivalence). For a specified class of constrained

systems with two admissible quantum clocks, possibly imperfect, and a clock-neutral normalized event

instrument whose interventions are represented within the constraint, all valid clock reductions

assign the same probabilities to corresponding finite realized-event histories. Moreover, on the

domains of the reductions, the clock-neutral instrument intertwines with clock-relative instruments,

R_A ∘ ℐ^phys = ℐ^A ∘ R_A and R_B ∘ ℐ^phys = ℐ^B ∘ R_B, for compositions of events as well as single

events. This holds although the two descriptions can assign different temporal localizations, and

different orderings, to the events.



A statement of the conjecture for a given class must specify the domains of the reductions and what

makes events in two descriptions correspond. Agreement of probabilities is not enough, because one

physical state supports many instrument decompositions (Proposition 13.2). The conjecture therefore

concerns a clock-neutral instrument, not merely a clock-neutral effect. A counterexample is

possible: a clock-relative description may admit no globally valid ordering of the events. Section

14.5 proves it for one family of instruments, late-record projective measurements, in a model with

two ideal clocks. A proof for a broader class would establish a realized-history measure shared

across clocks. It would not show that the events are generated in a fundamental succession, which

requires an ordering compatible with the constraint and its gauge symmetries (§14.6).



14.5 Two Ideal Clocks With the Interventions in the Constraint



The construction of this subsection removes the external stage index of Proposition 14.2. The

interventions are part of the constraint, and the events, their probabilities, and their instruments

are defined on the physical Hilbert space.



Setting. Clocks A and B are ideal: each has Hilbert space L²(ℝ) and a canonical pair (T, P) with [T,

P] = i (ħ = 1). The system and its records have a finite-dimensional Hilbert space K and a

Hamiltonian H_S. Interactions k = 1, …, r have Hermitian operators V_k on K and bounded continuous

switching functions g_k supported in [a_k, b_k], and each interaction is keyed to one clock, c(k) ∈

{A, B}. The constraint is



        Ĉ = P_A + P_B + H_S + Σ_k g_k(T_{c(k)}) V_k.



Proposition 14.5 (Two ideal clocks and record events).



    (a) Physical states and reductions. In the representation in which T_A and T_B act by

    multiplication, ĈΨ = 0 is the transport equation i(∂_{t_A} + ∂_{t_B})Ψ = H_Δ(t_A)Ψ along the

    lines of constant offset Δ = t_A − t_B, where



        H_Δ(s) = H_S + Σ_{c(k)=A} g_k(s) V_k + Σ_{c(k)=B} g_k(s − Δ) V_k.



    Its solutions are Ψ(t_A, t_B) = U_Δ(t_A) χ(Δ), with U_Δ(s) the unitary propagator of H_Δ from a

    fixed initial value s_0 and χ: ℝ → K. With the inner product ⟨Ψ, Ψ′⟩ = ∫ ⟨χ(Δ), χ′(Δ)⟩ dΔ, the

    physical Hilbert space is H_phys ≅ L²(ℝ, K). The offset T_A − T_B commutes with Ĉ. For every

    pair of readings τ and τ′, the reductions R_A(τ): Ψ ↦ Ψ(τ, ·) and R_B(τ′): Ψ ↦ Ψ(·, τ′) are

    unitary from H_phys onto L²(ℝ, K).



    (b) Temporal localization. Relative to clock A, interactions keyed to A act at the definite

    A-times [a_k, b_k], and interactions keyed to B act at the A-times [a_k + Δ, b_k + Δ], which are

    spread according to the distribution of the offset in the state. Relative to clock B the roles

    are exchanged.



    (c) Record events. Let E_1, …, E_n be commuting projections on K, each commuting with H_S. Let

    H_phys^I be the subspace of physical states whose offsets lie in a bounded interval I = [δ_−,

    δ_+], and let s* be an A-time after every interaction for every Δ ∈ I, that is, s* ≥ b_k for

    interactions keyed to A and s* ≥ b_k + δ_+ for those keyed to B. Then the operators O_j =

    U_Δ(s*)† E_j U_Δ(s*), acting pointwise in Δ, are commuting projections on H_phys^I, and



        R_A(τ) O_j = E_j R_A(τ)  for τ ≥ s*,     R_B(τ′) O_j = E_j R_B(τ′)  for τ′ ≥ s* − δ_−.



    Every finite history of record outcomes therefore has the same probability in the clock-neutral

    description and in either reduction at late readings. The clock-neutral instruments {O_j, 1 −

    O_j} intertwine with the record measurements {E_j, 1 − E_j} relative to either clock, and they

    compose in any order.



    (d) Superposed order. If an interaction keyed to A and one keyed to B have non-commuting

    operators, the order in which they act depends on Δ. The law of the record outcomes is then the

    mixture ∫ ‖χ(Δ)‖² P_Δ(α) dΔ of the laws P_Δ for the definite orders fixed by each offset, with

    P_Δ computed from χ(Δ)/‖χ(Δ)‖. Interference between the orders appears only in observables that

    are not diagonal in the offset.



    (e) Interference between the orders. Suppose H_S = 0, let f be a wave packet in the offset whose

    translates by δ_1 and δ_2 have disjoint supports in I, let ψ be a unit vector in K, and let χ(Δ)

    = (f(Δ − δ_1) + f(Δ − δ_2)) ψ/√2. Suppose that U_Δ(s*) equals a fixed unitary W_k for every Δ in

    the support of f(· − δ_k), as when each interaction is completed within either branch. Let 𝒰*

    multiply χ(Δ) by U_Δ(s*), let F_+ be the projection onto the offset-coherent wave function f_+ =

    (f(· − δ_1) + f(· − δ_2))/√2, acting trivially on K, and let O_+ = 𝒰*† F_+ 𝒰*. As in (a),

    physical states are represented by their initial data χ, so 𝒰* carries a physical state to its

    late-time data, and O_+ is the late-time projection F_+ expressed in the initial-data

    representation. Then O_+ is a projection on H_phys. Relative to A at τ ≥ s*, and relative to B

    at τ′ ≥ s* − δ_−, it is the projection onto the corresponding coherent superposition of readings

    of the other clock, and



        ⟨Ψ, O_+ Ψ⟩ = ½ (1 + Re⟨W_1 ψ, W_2 ψ⟩).



    For an incoherent mixture of the two offsets the same probability is ½, and when W_1ψ = W_2ψ it

    is 1. Its departure from ½ is half the real part of the overlap of the states produced by the

    two orders of the interactions.



Proof. (a) The operator ∂_{t_A} + ∂_{t_B} differentiates along the lines of constant Δ, with s = t_A

as parameter, so on each line the constraint reads i dΨ/ds = H_Δ(s)Ψ, whose solutions are

U_Δ(s)χ(Δ). The offset commutes with P_A + P_B, since [P_A, T_A] = [P_B, T_B] = −i, and with every

function of T_A and T_B. Relative to A, the conditional state is ψ_A(τ)(t_B) = U_{τ − t_B}(τ) χ(τ −

t_B). Its norm is ∫ ‖χ(Δ)‖² dΔ because each U_Δ(τ) is unitary, and every ψ is attained, with χ(Δ) =

U_Δ(τ)^{−1} ψ(τ − Δ). The argument for B, with ψ_B(τ′)(t_A) = U_{t_A − τ′}(t_A) χ(t_A − τ′), is the

same. (b) This follows from the form of H_Δ, read along the lines t_A = τ (relative to A) or t_B =

τ′ (relative to B). (c) For Δ ∈ I and s ≥ s*, no interaction is active, so U_Δ(s) = e^{−iH_S(s −

s*)} U_Δ(s*), and E_j commutes with the first factor. For τ ≥ s* this gives U_Δ(τ) O_j(Δ) = E_j

U_Δ(τ), pointwise in t_B = τ − Δ, which is the first identity. For τ′ ≥ s* − δ_−, every point t_A =

τ′ + Δ with Δ ∈ I satisfies t_A ≥ s*, and the same computation gives the second. The O_j are

projections that commute because the E_j do, and they preserve H_phys^I because they act pointwise

in Δ. Probabilities agree because the reductions are unitary. (d) Each O_j acts pointwise in Δ, so

‖Π_j O_j^{(α_j)} Ψ‖² = ∫ ‖Π_j O_j^{(α_j)}(Δ) χ(Δ)‖² dΔ. (e) The probability is ⟨χ, 𝒰*† F_+ 𝒰* χ⟩ =

‖F_+ 𝒰* χ‖², in which the evolution 𝒰* is applied once, to the initial data χ = f_+ ⊗ ψ. By

construction 𝒰*χ = (f(· − δ_1) W_1ψ + f(· − δ_2) W_2ψ)/√2, so F_+ 𝒰*χ = f_+ ⊗ (W_1ψ + W_2ψ)/2, whose

squared norm is ½(1 + Re⟨W_1ψ, W_2ψ⟩). Since H_S = 0, U_Δ(s) = U_Δ(s*) for s ≥ s*, so at late

readings R_A(τ) and R_B(τ′) differ from 𝒰* only by relabelling the offset as a reading of the other

clock, which gives the stated forms. For a mixture, each branch has overlap ½ with f_+. □
