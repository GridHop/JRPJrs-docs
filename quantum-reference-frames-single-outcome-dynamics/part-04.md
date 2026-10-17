# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 04 of 40 (1,223 words)

4.4 The Complete Ontological State and the Truth Profile



Definition 4.5 (Complete ontological state). The complete ontological state at stage σ is



        Ω_σ = (S_σ, L_σ),



where S_σ = [Ψ_σ] is the ray of the perspective-neutral state, and L_σ, the Lucretian truth profile,

is a set of past-tensed propositions of two kinds:



    Had(σ″, [Ψ_{σ″}]), read “at stage σ″ the state was [Ψ_{σ″}]”, for σ″ < σ;



    Had(σ″ → σ‴, k), read “in the generation of σ‴ from σ″, transition event k occurred”, for σ‴ ≤

    σ.



The second kind extends the stage-indexed properties Had(σ′, φ) of CTGP – explained, Definition

17.20, to transitions. This adds no commitment: a transition from σ″ to σ‴ is something that

occurred, and the present world can have been such that it occurred.



Definition 4.6 (Truth-profile update). When the transition σ → σ′ realizes event k,



        L_{σ′} = L_σ ∪ ΔL_{σ→σ′},     ΔL_{σ→σ′} = { Had(σ, [Ψ_σ]), Had(σ → σ′, k) }.



The truths acquired in a transition are exactly two: the state that was present has become past, and

the event that occurred in the transition is something that was the case. The initial condition is

L_{σ_0} = ∅ and S_{σ_0} = [Ψ_{σ_0}].



4.5 Admissible Histories



The truth profile is not an arbitrary set of past-tensed propositions. It ranges over a space fixed

by the law.



Histories, actuality, and futurity. Three uses of the word history must be kept apart, because the

mathematics speaks of histories in a sense that carries no ontological commitment. The actual past

history at a stage consists of the states and events that have occurred and are now past. Past

stages do not continue to exist; truths about them are grounded in the present world’s Lucretian

profile. The actual history through the present, where that phrase is needed, adds the presently

existing state to its past; it does not mean that the present has already become past. An admissible

history, by contrast, is a mathematical object: a possible sequence of events permitted by the law,

an element of the probability space defined below. The set of admissible histories lists the

alternatives the law permits. It does not represent alternative histories that exist side by side,

and a probability measure on future trajectories describes possible continuations of the present,

not an existing future.



Within CTGP no state or event exists as future. Each state first exists as the present, and each

realized transition becomes part of the actual past only after it has occurred. The actual past is

therefore not a completed structure containing future events: it grows as successive presents are

generated, without revision of what has occurred. What has occurred cannot later become something

else (C-b), although records, memories, and evidence about it can change, which is the distinction

between truth and recoverability (C-i). Only one history is ever realized. At each stage its actual

past consists exclusively of events that have already occurred, and the other admissible histories

are possibilities represented by the law, not additional existing histories. When the text speaks of

a complete history, completeness is relative to a specified finite stage, or to a trajectory used in

probabilistic analysis; it never means that the future has occurred or exists tenselessly.



Definition 4.7 (Admissible histories and complete states). Fix the law and the initial state

Ψ_{σ_0}. Let



        ℋ_n = { ω ∈ 𝒦^n : Pr(ω | Ψ_{σ_0}) > 0 }



be the set of admissible histories of length n, the possible event sequences of nonzero probability.

For ω ∈ ℋ_n write Ψ_m(ω) for the state after the first m events (Ψ_0(ω) = Ψ_{σ_0}), and define its

truth profile



        L(ω) = { Had(σ_m, [Ψ_m(ω)]) : 0 ≤ m < n } ∪ { Had(σ_{m−1} → σ_m, k_m) : 1 ≤ m ≤ n }.



The admissible truth profiles and admissible complete states at stage σ_n are



        ℒ_n = { L(ω) : ω ∈ ℋ_n },     𝔒_n = { ([Ψ_n(ω)], L(ω)) : ω ∈ ℋ_n }.



Theorem 4.8 (Characterization of admissible profiles). A set L of past-tensed propositions belongs

to ℒ_n if and only if all of the following hold:



    (o) Restricted language. Every element of L is a past-tensed proposition of one of the two forms

    of Definition 4.5: a state proposition Had(σ_m, [Ψ]) with m ≥ 0 and Ψ ∈ H_phys, or a transition

    proposition Had(σ_{m−1} → σ_m, k) with m ≥ 1 and k ∈ 𝒦.



    (a) One event per transition. For each m = 1, …, n, L contains exactly one proposition of the

    form Had(σ_{m−1} → σ_m, k).



    (b) One state per past stage. For each m = 0, …, n−1, L contains exactly one proposition of the

    form Had(σ_m, [Ψ]).



    (c) Correct initial state. The state proposition for σ_0 is Had(σ_0, [Ψ_{σ_0}]).



    (d) Lawful consistency. For each m = 1, …, n−1, if L contains Had(σ_{m−1}, [Ψ]) and Had(σ_{m−1}

    → σ_m, k), then F_k W Ψ ≠ 0 and the state proposition for σ_m is Had(σ_m, [F_k W Ψ]); and, for

    the last event k_n, F_{k_n} W Ψ ≠ 0 where [Ψ] is the state recorded for σ_{n−1}.



    (e) Past-stage restriction. Every state proposition in L is indexed to a past stage σ_m with 0 ≤

    m ≤ n−1, and every transition proposition is indexed to a transition σ_{m−1} → σ_m with 1 ≤ m ≤

    n. Thus L contains no state proposition about the present stage σ_n and no proposition of either

    kind about any later stage.



When these hold, the history ω with L = L(ω) is unique. Moreover, admissible profiles are nested: if

ω ∈ ℋ_n and ω|m is its initial segment of length m ≤ n, then L(ω|m) ⊆ L(ω).



Proof. (⇒) Each condition holds by construction of L(ω) and the definition of ℋ_n. (⇐) By (a),

reading off the event proposition for each transition gives a unique sequence ω = (k_1, …, k_n). By

(c) and (d), induction on m shows that the state proposition for σ_m is Had(σ_m, [Ψ_m(ω)]) and that

each factor of Pr(ω | Ψ_{σ_0}) is nonzero, so ω ∈ ℋ_n. By (o), every element of L is a state or

transition proposition. By (e), its state propositions concern only the stages σ_0, …, σ_{n−1} and

its transition propositions only the n transitions up to σ_n; by (a) and (b), each of these carries

exactly one proposition, namely the one just identified. Hence L = L(ω). Uniqueness follows because

ω is read off from L. Nesting holds because the propositions defining L(ω|m) are among those

defining L(ω). □



Theorem 4.8 makes precise the requirements that a truth profile must meet: propositions of the two

permitted forms only, exactly one realized event per transition, state propositions only about past

stages and consistent with the law, no incompatible state assignments, preservation of acquired

truths, and no claim that an unrealized future event has occurred. The restriction of state

propositions to past stages matters: the present state is part of S, not of the past-tensed profile

L, and a set that added a state proposition about σ_n to an admissible profile would satisfy every

other condition without belonging to ℒ_n. Theorem 4.8 establishes that the Lucretian profile is a

consistent interpretation of the model’s realized histories. It does not establish that Lucretian

properties exist in nature; that is a philosophical thesis of CTGP, which the model shows to be

coherent.


