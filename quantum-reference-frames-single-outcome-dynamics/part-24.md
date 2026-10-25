# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 24 of 35 (1,798 words)

Proposition 14.2 (Imperfect clocks in a generative model). Consider a model of the kind defined in

Part II whose physical state includes one or more clock subsystems.



    (a) Clock-independence of event identity and probability. The measure over histories of Tier 1

    events is fixed by the law and the complete initial state. Describing those events relative to

    one clock rather than another changes no event label, no stage, and no probability.



    (b) Periodic clocks. A clock of period M takes the same reading at stages σ_n and σ_{n+M}, so

    equal readings do not imply equal stages: τ_A(σ_1) = τ_A(σ_2) is compatible with σ_1 ≠ σ_2. A

    repeated reading means that the clock fails to distinguish two stages, not that generation has

    reversed.



    (c) Temporal delocalization. If a clock is in a superposition of readings at the stage of an

    event, the Tier 3 proposition “the clock read r when the event occurred” has no determinate

    value, although the event and its stage are determinate. For example, a counter prepared in an

    equal superposition of the readings 0 and 4 and advancing by one per stage reads n or n + 4,

    each with probability 1/2, at stage n.



    (d) Clock-relative order can disagree with generative order. If a non-ideal clock’s readings are

    recorded at successive events, the later event can carry an earlier reading. Consider a drifting

    quantum-walk clock on a ring of 32 sites, which advances one site per stage on average under the

    one-step propagator S exp(−i θ (S + S†)) with θ = 0.9. Because a ring has no intrinsic linear

    order, comparing two readings requires a convention: the displacement between consecutive

    readings r_1 and r_2 is the representative m of r_2 − r_1 modulo 32 in {−15, …, 16}, and the

    second reading counts as lower when m < 0 and as equal when m = 0. Assume that each event

    records the clock’s reading by a projective measurement of its position, so that the first

    recording leaves the clock in a definite position state, and that exactly one stage transition

    separates two consecutive recordings. Then, conditional on the first recorded reading, the exact

    probabilities on the 32-site ring are P(m < 0) = 0.104042655 and P(m = 0) = 0.338161965, to nine

    decimal places. They agree to better than 10⁻¹² with the infinite-lattice expressions (1 −

    J_0(1.8)² − 2 J_1(1.8)²)/2 and J_1(1.8)², where J_n are Bessel functions. By translation

    invariance these values do not depend on the first reading. Displacements of eight or more sites

    have total probability below 10⁻⁸, so any comparison convention that agrees with this one on

    displacements of fewer than eight sites gives the same values to that accuracy. The values do

    depend on the preparation and recording procedure: a clock not recorded at the first event, an

    unsharp recording, or a comparison across more than one transition gives different values.



Proof. (a) Clock subsystems are part of the physical state, and the law takes the complete present

state as input; the choice of a subsystem as clock for purposes of description is not an input to

the law. If a clock interacts with the system, event probabilities depend on the clock’s physical

state, but that is a dependence on the present physical state, not on the choice of description. (b)

and (c) follow from the definitions. (d) The first recording projects the clock onto a position

eigenstate |r⟩. During the single intervening transition the clock evolves by the stated propagator.

By the Jacobi–Anger expansion, exp(−i θ (S + S†)) = Σ_{k∈ℤ} (−i)^k J_k(2θ) S^k, so on the infinite

lattice the amplitude to move from r to r + m is, up to a phase, J_{m−1}(2θ). On the ring S^{32} =

1, and the amplitude for displacement m is the sum of the lattice amplitudes for all displacements

congruent to m modulo 32. For m ∈ {−15, …, 16} the additional terms involve J_k(1.8) with |k| ≥ 16,

each of magnitude below 10⁻¹⁴, so the ring probabilities differ from the lattice values

J_{m−1}(1.8)² by less than 10⁻¹² in total. Summing the lattice values over m ≤ −1 gives Σ_{k≥2}

J_k(2θ)² = (1 − J_0(2θ)² − 2 J_1(2θ)²)/2, using Σ_k J_k² = 1 and J_{−k}² = J_k², and m = 0 gives

J_{−1}(2θ)² = J_1(2θ)². The exact ring values were computed directly from the 32-site propagator.

The computation is item 16 of Appendix B. □



Proposition 14.2 has an external generative order built in: the stage index is a parameter of the

model. It therefore shows that the three-way distinction of Definition 14.1 is consistent, and that

clock-relative localization and ordering can differ from generative order without contradiction. It

does not derive a definite generative order from clock-neutral data. That is the task of

§§14.4–14.6.



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


