# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 05 of 40 (1,250 words)

4.6 L and S: Dynamical Idleness, Accuracy, and Non-Supervenience



Proposition 4.9 (Dynamical idleness of L). For any two admissible complete states Ω = (S, L) and Ω*

= (S, L*) with the same S, the joint distribution of the next state and next event is the same.



Proof. The kernel of Definition 4.2 takes Ψ_σ as its only input. □



Corollary 4.10 (The future is conditionally independent of the past given the present). Let 𝔉⁺_σ

denote the possible future trajectory (k_{σ′}, Ψ_{σ′}, k_{σ″}, Ψ_{σ″}, …) after stage σ, regarded as

a random variable. Then for every admissible Ω_σ,



        Pr(𝔉⁺_σ | S_σ, L_σ) = Pr(𝔉⁺_σ | S_σ).



Proof. The distribution of any finite segment of 𝔉⁺_σ is a product of kernels, each depending only

on the preceding state (Proposition 4.9); the full trajectory measure is determined by its finite

segments. □



The measure in Corollary 4.10 is a probability measure over possible continuations of the present

state. Defining it does not presuppose that any future trajectory exists: exactly one continuation

becomes actual, event by event, as the corresponding transitions occur.



Corollary 4.10 is the formal version of (C-g). It separates three things that CTGP holds apart: the

past being ontologically definite (L is determinate), the past being recoverable from present

physical information (a matter of what S encodes, §5.5), and the past having further causal

influence (it has none beyond what S carries). The first does not entail either of the others. L is

part of the complete ontology but not a dynamical variable, so generability’s restriction on

enlarging the state space (C-f) is not triggered: L does not enlarge the space on which the law

acts.



Proposition 4.11 (Accuracy). For n ≥ 1 and ω ∈ ℋ_n, the present state is fixed by the two most

recent entries of L(ω) together with the law: if Had(σ_{n−1}, [Ψ]) and Had(σ_{n−1} → σ_n, k) belong

to L(ω), then S_{σ_n} = [F_k W Ψ]. At the initial stage σ_0, L is empty and S_{σ_0} is an initial

condition not fixed by L.



Proof. Definitions 4.2 and 4.6. □



Proposition 4.11 is a consistency condition, not a dependence of the dynamics on L. Both S_{σ_n} and

ΔL are outputs of the same transition, and L does not select k. Reconstructing S from L uses the

law; reconstructing earlier states uses the initial-state entry Had(σ_0, [Ψ_{σ_0}]) as well.



The non-supervenience thesis (C-c) says that a present state does not fix its past. Under presentism

the initial stage is a past stage like any other, so the past includes the initial state. Two senses

of non-supervenience should therefore be distinguished. The weak sense fixes the initial state and

asks whether different event sequences can end in the same present. The strong sense asks whether

the present state fixes the complete past, including the initial state.



Proposition 4.12 (Strong non-supervenience for invertible laws). Suppose W is unitary and every F_k

is invertible on H_phys. Then for every n ≥ 1, every present ray [Φ] in H_phys, and every sequence ω

∈ 𝒦^n, there is exactly one initial ray [Ψ_{σ_0}], depending on ω, from which ω has nonzero

probability and ends at [Φ]. Consequently, across possible initial conditions, every present ray can

be reached along every finite event sequence, and the complete past, including the initial

condition, is not a function of the present state. The proposition does not assert that a single

fixed initial state reaches a given present ray along every event sequence.



Proof. Define Ψ_{σ_0} ∝ (F_{k_n} W ⋯ F_{k_1} W)^{−1} Φ, which exists because each factor is

invertible. Running ω forward from this state returns a vector proportional to Φ, and each

transition probability is nonzero because an invertible operator annihilates no nonzero vector. Any

other initial ray reaching [Φ] along ω is mapped to the same ray by the invertible product, so it

coincides with this one. □



Proposition 4.13 (Weak non-supervenience in a special regime). In the model of Part III with sharp

flashes (s → 0) and no hopping (J = 0), there exist an initial state and two distinct histories ω ≠

ω* ∈ ℋ_2 that end in the same present ray.



Proof. Proposition 8.1. □



In the model of Part III with finite width s > 0 and hit probability λ < 1, every Kraus operator is

invertible (§7.2), so Proposition 4.12 applies: for all such parameter values, the complete past is

not fixed by the present state, in the strong sense. Weak non-supervenience is established in the

special regime of Proposition 4.13. Whether it holds for generic finite-width parameters is open; a

numerical search over 4,096 three-stage histories at generic parameters found no exact coincidences

(§8.3). Strong non-supervenience is the sense relevant to CTGP, since under presentism the initial

condition is one more fact about the past.



----------------------------------------------------------------------------------------------------

5. The Criteria

----------------------------------------------------------------------------------------------------



5.1 The Determinacy Criterion (Task T1)



Definition 5.1 (Determinate propositions). At stage σ, with complete state Ω_σ = (S_σ, L_σ), the

determinate propositions fall into three tiers.



    Tier 1 (events). For each past transition σ″ → σ‴ with σ‴ ≤ σ and each k ∈ 𝒦, the proposition

    “in the generation of σ‴, event k occurred” is determinate. It is true iff Had(σ″ → σ‴, k) ∈

    L_σ. Boolean combinations of Tier 1 propositions are determinate.



    Tier 2 (states). For each σ″ ≤ σ, the proposition “at σ″ the state was [Ψ]” is determinate. For

    σ″ < σ it is true iff Had(σ″, [Ψ]) ∈ L_σ; for σ″ = σ it is true iff S_σ = [Ψ].



    Tier 3 (sharp properties). For an invariant projector Q and σ″ ≤ σ, the proposition “Q held at

    σ″” is determinately true iff Q Ψ_{σ″} = Ψ_{σ″}, determinately false iff Q Ψ_{σ″} = 0, and

    otherwise has no determinate truth value.



No proposition about a stage later than σ is determinate at σ. Future-directed claims have only the

probabilities assigned by the kernel.



Tier 1 carries single-outcome realism. In a flash ontology the macroscopic world is the pattern of

events, so “the pointer pointed left” is a Tier 1 fact about which events occurred, not a Tier 3

fact about the wave function. This avoids the tails problem of collapse models: collapse never

produces an exact eigenstate of position, so Tier 3 would almost never make a macroscopic position

determinate, but Tier 1 does not depend on exact eigenstates (Proposition 4.4). Tier 3 is included

because sharp-property talk is common and because, in the sharp-flash limit, events do produce sharp

values (§8.2).



Proposition 5.2 (Determinacy is frame-independent). Let τ_A be the frame-A translation of

propositions defined in §5.2. A proposition p is determinate at σ iff its frame-A translation τ_A(p)

is determinate in the frame-A description, with the same truth value, for every frame A.



Proof. Tier 1: τ_A leaves the event label and the stage indices unchanged, and membership in L is

preserved by the definition of τ_A. Tier 2: [Ψ] ↦ [R_A Ψ] is a bijection on rays. Tier 3: Q Ψ = Ψ

iff Q^A R_A Ψ = R_A Ψ, and Q Ψ = 0 iff Q^A R_A Ψ = 0, by Lemma 3.7. □



In this framework, “definite relative to frame A but not relative to frame B” never occurs for the

same proposition. What does occur is that one proposition takes different forms in different frames:

a single-coordinate statement in frame A can be a statement about a correlation between two

coordinates in frame B (§6.3). A different form is not a different fact.


