# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 10 of 35 (1,797 words)

law, every pair of frames, and every event k, the frame-A and frame-B single-step maps G^A_k(ψ) =

F^A_k W^A ψ / ‖F^A_k W^A ψ‖ and G^B_k satisfy V_{A→B} ∘ G^A_k ≐ G^B_k ∘ V_{A→B}. The stage index is

unchanged by every frame change. The same holds in continuous time, with hit times unchanged.



Proof. Lemma 3.7, Definition 3.4, and Proposition 9.2(iv). Frame changes are maps H_A → H_B at a

fixed stage or time, and the stage or time index is a parameter of the law, not a quantum degree of

freedom. □



The linear order of stages, and the order of events within a history, are therefore the same in

every frame: event k_j precedes k_{j+1} in every description, and no frame change in this class

superposes the order of events. This satisfies (C-e) for spatial QRFs. The status of this result

should be stated plainly. The ordering is preserved because the stage or time index is a parameter

on which frame changes do not act. That is an assumption of the class of models, not a derivation of

definite order from more basic principles. Whether a definite order can be maintained when the

reference frame is itself a quantum clock is the principal open problem (§14; §17.3, O3).



10.2 Generability



The kernel of Definition 4.2, and the jump process of Definition 9.1, give the distribution of the

next state and event from the present state alone. They use no data from later stages, no final-

state condition, and no global self-consistency condition, so the model is generable in exactly the

sense of (C-f). The state space on which the law acts is H_phys, the physically instantiated present

state. The truth profile is not added to it (Proposition 4.9), so generability’s restriction on

enlarging the state space is respected. By Corollary 5.14, the generability property holds in every

frame. The model is stochastic, which CTGP – explained, §12.2, explicitly allows.



10.3 Open Future and Asymmetry



At stage σ, L_σ contains no proposition about a later stage (Theorem 4.8(e)), and no proposition

about a later stage is determinate (Definition 5.1). Before a transition there are only kernel

probabilities over possible events; after it there is one realized event and its Had-property. This

matches clause (d) of CTGP’s Definition 17.20 and the claim that the future is ungenerated rather

than merely unknown.



10.4 No Relative Facts



Every determinate proposition has the same truth value in every frame (Proposition 5.2 and Theorem

5.16), so the model contains no frame-relative facts. It contains frame-relative descriptions and

relational quantities, which CTGP does not reject (§2.3).



====================================================================================================

PART IV. Evaluation

====================================================================================================



----------------------------------------------------------------------------------------------------

11. What CTGP Adds Beyond QRF Covariance

----------------------------------------------------------------------------------------------------



A skeptic can grant every theorem above and still ask whether CTGP contributes any substantive

constraint beyond the existence of a QRF-covariant, single-outcome stochastic model with an attached

historical truth profile. It does. The test of whether a commitment adds content is whether it

excludes some model that satisfies everything else. Each of the following commitments passes that

test.



CTGP commitment          | Formal content in this framework        | Excludes

-------------------------+-----------------------------------------+-------------------------------

Generability (C-f)       | The law is a Markov kernel on present   | Laws depending on past facts

                         | physical states; Cor. 4.10, Cor. 5.14   | not carried by the present

                         |                                         | state (Example 11.3)

Single-outcome (C-d)     | Exactly one event per transition;       | Everettian readings on which

                         | Theorem 4.8(a)                          | all branches are realized

Frame-invariant          | Determinacy and truth invariant under   | Relational interpretations with

determinacy (C-d)        | all frame changes; Prop. 5.2, Thm 5.16  | frame-relative facts

No revision (C-b)        | Admissible profiles are nested;         | Readings on which later events

                         | Theorem 4.8; Prop. 5.17                 | fix earlier facts

Definite ordering (C-e)  | Events totally ordered, order invariant | Fundamental indefinite causal

                         | under frame changes; Prop. 10.1         | order at the level of stages

Lucretian accuracy (C-b) | Profiles are admissible and accurate;   | Truth profiles inconsistent

                         | Theorem 4.8, Prop. 4.11                 | with the law



Table 2. Constraints CTGP imposes and what each excludes, even among QRF-covariant models.



Generability needs the most care, because a law that looks future-dependent may have an equivalent

forward formulation. CTGP – explained, §12.2, builds this into its criterion: future dependence

counts against generability only if no empirically equivalent generable formulation exists. Three

cases must therefore be distinguished: conditioning on the future as a mathematical operation, a

final-boundary requirement imposed as a fundamental input, and genuine non-generability relative to

the admissible present physical states. The first two are treated by Proposition 11.1 and Example

11.2, the third by Example 11.3.



Proposition 11.1 (Future conditioning has a forward representation). Let E be an event label and n ≥

1 a stage with Pr(k_n = E | Ψ_{σ_0}) > 0. For m < n define h_m(Ψ) as the probability that k_n = E

given state Ψ at stage σ_m, computed from the kernel K. The measure over histories conditioned on

k_n = E is generated forward by the stage-dependent kernel



        K^h_m(k | Ψ) = K(k | Ψ) · h_{m+1}(Ψ_k) / h_m(Ψ)        for m < n−1,

        K^h_{n−1}(k | Ψ) = K(k | Ψ) · 1[k = E] / h_{n−1}(Ψ),



where Ψ_k = F_k W Ψ / ‖F_k W Ψ‖ and 1[k = E] is 1 if k = E and 0 otherwise. This kernel is Markov in

the present state at each stage, and it is frame-covariant.



Proof. This is the Doob h-transform. The product of the kernels K^h along a history telescopes to

Π_m K(k_{m+1} | Ψ_m) · 1[k_n = E] / h_0(Ψ_{σ_0}), which is the conditioned probability of the

history; the normalization of each K^h_m follows from h_m(Ψ) = Σ_k K(k | Ψ) h_{m+1}(Ψ_k). Frame

covariance holds because K and the h_m are computed from frame-independent probabilities (Theorem

5.12). □



The numerical check (Appendix B, item 13) confirms that the forward kernel reproduces the

conditioned measure over all three-stage histories.



Example 11.2 (What future conditioning does and does not violate). Take the model of Part III and

the event E = (B, C, 0) at stage σ_n.



    (i) As a mathematical operation, conditioning on E computes probabilities given a hypothetical

    later event. It imposes nothing on the world and is not excluded.



    (ii) As a fundamental final-boundary requirement, the theory would consist of the ring dynamics

    together with the stipulation that E occurs at σ_n, imposed as an independent input. The forward

    kernel K^h of Proposition 11.1 exists, but its definition refers to E and n, which are data

    about a later stage. A law of this kind is precisely a final condition imposed as an independent

    input to fix earlier evolution, which CTGP – explained, §12.2, identifies as incompatible with

    presentism.



    (iii) If K^h_m is instead posited directly as a stage-dependent law, with no reference to E, it

    is generable, and CTGP does not exclude it.



Since (ii) and (iii) are empirically equivalent, CTGP’s own criterion does not count finite-stage

future conditioning in this model as a genuine failure of generability: an equivalent forward

formulation exists. What CTGP rejects in case (ii) is the claim that the boundary condition is a

fundamental input, not the probability measure that results. Conditioning is therefore not the right

test case. A genuine failure must be one for which no forward formulation on the admissible present

physical states exists.



Example 11.3 (A QRF-covariant, history-dependent law). Fix the physical state space H_phys of Part

III and a width s ≥ 0, where s = 0 denotes the sharp limit. Besides the flash instrument {F_k} of

§7.2, which chooses each pair with weight 1/3, let {F″_k} be the instrument with the same flashes

but pair weights q_{AB} = 1/2, q_{AC} = q_{BC} = 1/4:



        F″_∅ = √(1−λ) · 1,     F″_{(i,j,d)} = √(λ q_{ij}) · Σ_r √(w(r−d)) P_{ij}(r).



Completeness holds because the weights sum to 1. Define a law that applies {F_k} at the first

transition and, at every later transition, applies {F_k} if the first event was a flash on the pair

(A, B), and {F″_k} otherwise. Both instruments are invariant and the rule consults only an invariant

event label, so the law is QRF-covariant; it is single-outcome; and each history carries a well-

defined truth profile.



The law is not generable on H_phys if two histories of the same length reach the same present ray

while calling for different next-event distributions. Two versions of this claim should be

distinguished: one across possible initial conditions, and one for a single fixed initial condition.

Both hold, and the next proposition proves each by explicit construction.



Proposition 11.4 (The history-dependent law is not generable on H_phys). No kernel on present states

in H_phys, even one allowed to depend on the stage index, reproduces the law of Example 11.3.

Specifically:



    (a) Across initial conditions (s > 0). For every present ray of the form [Φ] with W Φ =

    R_A^{−1}|x, y⟩, there are two histories of length 2, with different initial rays, that both

    reach [Φ] with nonzero probability and whose next-event distributions differ in total variation

    by exactly λ/6.



    (b) With one fixed initial condition (s = 0, J = 0). For every initial state with nonzero

    amplitude on the configuration b−a = 1, c−a = 3 (N ≥ 4), the two histories of Proposition 8.1

    both have nonzero probability under the law of Example 11.3, both reach the same present ray,

    and their next-event distributions again differ in total variation by exactly λ/6.



Proof. A kernel on present states, even a stage-dependent one, assigns the same next-event

distribution to any two histories of equal length that reach the same present ray. It therefore

suffices to exhibit such pairs with different next-event distributions.



(a) Take the histories ω_1 = ((A,B,d), k) and ω_2 = (∅, k) with any d and any flash k. Under the

law, ω_1 applies F_k at its second transition (its first event is on the pair (A,B)), and ω_2

applies F″_k (its first event is ∅). The branch products M_1 = F_k W F_{(A,B,d)} W and M_2 = F″_k W

F_∅ W are invertible, because for s > 0 every Kraus operator of either instrument is invertible

(w(r) > 0 for all r and λ < 1). Define the initial rays [M_1^{−1} Φ] and [M_2^{−1} Φ]. Running each

history from its initial ray returns a vector proportional to Φ, and each transition has nonzero

probability because invertible operators annihilate no nonzero vector. At the present stage, ω_1

calls for {F_k} and ω_2 for {F″_k}. Since W Φ is the configuration state with separations x, y, and

y−x for the pairs (A,B), (A,C), (B,C), the probability of the flash (i, j, d′) is λ · (1/3) ·

w(r_{ij} − d′) under {F_k} and λ · q_{ij} · w(r_{ij} − d′) under {F″_k}, where r_{ij} is the
