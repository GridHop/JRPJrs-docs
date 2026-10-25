# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 25 of 35 (1,791 words)

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



Proposition 14.5 proves clock-neutral equivalence for a specified family of instruments, late-record

projective measurements built from commuting projections, together with the offset-coherent

projection of part (e), in an ideal two-clock constrained model. It is the ideal-clock case of

Conjecture 14.4 for this family only. It does not establish equivalence for arbitrary clock-neutral

instruments, for events that occur while interactions are active, or for an indefinitely extended

succession of physically generated records, and it is not a general solution of temporal-QRF

compatibility. In the numerical check (Appendix C.2), a record written by an interaction keyed to A,

with the offset spread over [0.06, 1.64], has probability 0.139627690767 in the clock-neutral

description and in both reductions at late readings. Relative to A, the record probability is

exactly zero before A-time 0, the start of the interaction. Relative to B, it is already 0.021 at

B-time −1.0, because in part of the offset distribution the interaction has begun. For these

instruments, the event, its probability, and its instrument are the same in both descriptions; only

its temporal localization differs. With one interaction keyed to each clock and the offset in an

equal superposition of two wave packets centred at −1.6 and +1.6, the record law is 0.706791827009

in all three descriptions. This equals the equal-weight mixture of the two definite-order values,

0.868488 and 0.545095.



Part (e) answers the question that part (d) leaves open: whether the superposition of orders has

operational consequences. It does, for an observable that measures the clocks’ relative offset in a

coherent basis. In the numerical check, this probability is 0.926776695297 in the clock-neutral

description and in both reductions, equal to ½(1 + Re⟨W_1ψ, W_2ψ⟩), whereas an incoherent mixture of

the two offsets gives exactly ½. The statistic depends jointly on both orders. It is reproduced

neither by one definite order common to both offsets, which would give 1, nor by an order correlated

classically with the offset, which would give ½. This is a calculation within the model, not a

device-independent certification of indefinite causal order, which would require a causal witness in

the sense of Araújo et al. (2015).



For CTGP, parts (d) and (e) have a specific lesson. The order of unitary interactions keyed to

different clocks can be indefinite, with operational consequences, as in the analyses of Castro-Ruiz

et al. (2020) and Baumann and Lock (2026). The realized events, the record outcomes and the outcome

of an offset-coherent measurement, nevertheless have clock-neutral identities, probabilities, and

instruments. CTGP’s definite-ordering commitment (C-e) concerns stages and the realized events

located in them, not unitary couplings, so parts (d) and (e) do not conflict with it. What

Proposition 14.5 does not supply is a generative order of the record events. Their instruments

commute, so every order gives the same law, and designating one order as generative is interpretive

in the sense of §14.6. The proposition is also limited by its idealizations. Ideal clocks have

Hamiltonians unbounded below, and for clocks with bounded Hamiltonians the reductions are no longer

unitary (Höhn, Smith & Lock 2021). Events that occur while interactions are active, and

interventions that do not single out one clock, are not covered.



14.6 The Possible Obstruction



A fully relational quantum theory may treat all clock choices as physically equivalent and deny that

any further, objective generative ordering exists. CTGP could then still be added as an ontological

interpretation, but the added structure would have to be compatible with the theory’s constraints

and gauge symmetries. Two cases must be distinguished. If the added ordering has no physical

effects, it is interpretive rather than a new physical variable. If it affects event probabilities,

it is a physical hypothesis subject to empirical test. Section 13.10 meets the same alternative from

the side of collapse dynamics: cosmological time could fix the local frame and the order of

conflicting collapses covariantly, but only as a dynamical ordering (Remark 13.25).



Recent work sharpens the problem. Baumann and Lock (2026) report that, of the ways of modeling

interventions within relational dynamics, only one that builds the interventions into the constraint

remains causally consistent across multiple clocks, that it requires some temporal delocalization,

and that it naturally describes indefinite causal order. CTGP cannot simply stipulate that every

clock-relative temporal ordering is the same. It must identify which physical ordering is

ontologically fundamental and prove that legitimate temporal descriptions can be related to it. If

indefinite causal order turned out to be fundamental, rather than a feature of clock-relative

descriptions, CTGP’s primitive ordering would require generalization (C-e; CTGP – explained, §6.4).



Three claims must be kept apart in assessing this possibility. (i) Every effective quantum operation

has a definite classical order. The quantum switch (Chiribella, D’Ariano, Perinotti & Valiron 2013)

is the standard example of a process for which this fails, and photonic quantum-switch experiments

(Procopio et al. 2015) support processes whose effective operations cannot be represented as

ordinary probabilistic mixtures of fixed orders within the relevant operational framework. (ii) The

finer-grained physical interactions have a definite causal order. A failure of (i) does not

establish a failure of (ii): for realizations in a classical background spacetime, and under

specified assumptions about relativistic causality and the spacetime localization of systems,

Vilasini and Renner (2024) show that such processes admit a fine-grained description with a definite

acyclic causal order. This is not a general theorem that every quantum process has a definite

underlying causal order, and it does not address superpositions of spacetime geometry (§15.1).

(iii) A single history of physical events is realized. Neither (i) nor (ii) supplies this; it

requires single-outcome realism (C-d). In suitable models, Bohmian mechanics supplies definite

trajectories and thereby one realized history; a GRW flash ontology supplies definite flashes, but

those flashes need not identify which effective operation order was realized. These are

illustrations, not established relativistic solutions. CTGP’s definite-ordering commitment (C-e)

concerns stages and the realized events located in them, so operational causal nonseparability alone

neither establishes nor refutes CTGP. The generalization contemplated above would be needed only if

indefinite order proved fundamental, at the level of (ii) or of the generative ordering itself,

rather than a feature of effective operations or clock-relative descriptions.



----------------------------------------------------------------------------------------------------

15. Quantum Gravity

----------------------------------------------------------------------------------------------------



15.1 Fundamental Generative Order Versus Classical Cosmological Time



In the classical regime, CTGP identifies the present with a level set of the cosmological time

T_g(p) = sup { L_g(γ) : γ a past-directed causal curve from p }, subject to the regularity

conditions of §13.1. A fundamental quantum theory of gravity may have no single classical metric. A

state of the schematic form α|g_1⟩ + β|g_2⟩, with g_1 and g_2 inducing different cosmological-time

functions, has no unique classical T. The program therefore distinguishes



        fundamental generative order  ≠  classical cosmological-time function.



The two must agree in the appropriate classical limit, but they need not coincide at the fundamental

level. This develops the distinction between primitive generation and emergent geometry that CTGP

already draws (CTGP – explained, §§10.3–10.4). It also raises a demanding question: what physical

structure carries the objective generative ordering before classical spacetime exists? Naming a

parameter does not answer it.



15.2 Three Pathways


