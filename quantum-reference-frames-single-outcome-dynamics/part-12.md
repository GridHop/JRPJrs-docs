# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 12 of 40 (1,698 words)

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

corresponding separation; the probability of ∅ is 1 − λ in both. Summing |λ(q_{ij} − 1/3)| over the

three pairs and over d′ (using Σ_{d′} w = 1) gives λ(1/6 + 1/12 + 1/12) = λ/3, so the total-

variation distance is λ/6.



(b) Take ω = ((A,B,1), (A,C,3)) and ω* = ((A,C,3), (A,B,1)), as in Proposition 8.1. With s = 0 the

Kraus operators of both instruments are multiples of configuration projectors: F_{(i,j,d)} = √(λ/3)

P_{ij}(d) and F″_{(i,j,d)} = √(λ q_{ij}) P_{ij}(d). With J = 0, W is diagonal in the configuration

basis. Under the law, ω applies {F_k} at its second transition (its first event is on (A,B)), and ω*

applies {F″_k} (its first event is on (A,C)). In both cases the second operator is a nonzero

multiple of a configuration projector (√(λ/3) P_{AC}(3) along ω and √(λ/2) P_{AB}(1) along ω*), and

the first is √(λ/3) times the other projector. Since W is diagonal and commutes with both

projectors, and P_{AB}(1) P_{AC}(3) = P_{AC}(3) P_{AB}(1) = |1, 3⟩⟨1, 3| in frame-A coordinates, the

unnormalized final vectors are (λ/3) e^{2iθ(1,3)} ⟨1, 3|ψ_0⟩ |1, 3⟩ and (λ/√6) e^{2iθ(1,3)} ⟨1,

3|ψ_0⟩ |1, 3⟩, which differ only by a positive factor. Hence, as in Proposition 8.1: both histories

have nonzero probability, because the initial state has nonzero amplitude on the configuration (x,

y) = (1, 3), and both reach the present ray [R_A^{−1}|1, 3⟩]. At that ray, W Φ is the configuration

state (1, 3), and the computation in (a) gives next-event distributions differing in total variation

by λ/6. □



The numerical check (Appendix B, item 12) carries out both constructions explicitly at the

parameters of §8.4, with present configuration (x, y) = (1, 3): in each case the two histories end

at the same present ray with nonzero probability, and the next-event distributions differ in total

variation by 0.1000 = λ/6.



Example 11.3 is a genuine failure of generability relative to the model’s physical state space. The

law depends on a past fact that the present state does not carry, so it is not a Markov kernel on

admissible present physical states, whether the comparison is made across initial conditions or with

the initial condition held fixed. It could be made generable only by adding a record variable, such

as a bit registering whether the first event was on the pair (A, B), to the present physical state.

CTGP permits such an enlargement only if the variable is physically instantiated on the present

stage and has dynamics of its own (C-f). The result is then a different theory with an enlarged

physical ontology, not a forward formulation of the original one. In this sense generability does

independent work: it excludes the history-dependent law on H_phys while QRF covariance does not. The

exclusion is an ontological restriction imposed by CTGP, not a mathematical impossibility. Any

history-dependent process becomes Markov on a suitably enlarged state space, for instance by

adjoining a memory bit. What CTGP adds is the requirement that the enlarged state be physically

instantiated in the present, rather than serve as a bookkeeping variable that records the past.



Two further consequences arise from combining CTGP’s commitments with the perspective-neutral

construction. First, requiring every realized event to carry physical states to physical states

makes each collapse operator act on physical states as an invariant, relational operator does

(§7.4). This constrains how a collapse realization of CTGP acts on physical states within the

construction; it does not single out the particular flash ontology of §7.2. Second, for invertible

single-outcome laws the complete past is not a function of the present state (Proposition 4.12),

which gives CTGP’s acknowledged cost (C-c) an exact form.



The answer to the skeptic, then, is that CTGP picks out a proper subclass of QRF-covariant single-

outcome models: those whose laws are Markov kernels on the present physical state, whose determinacy

is frame-invariant, whose truth profiles are admissible and nested, whose events are definitely

ordered, and, within the perspective-neutral construction, whose collapse operators act on physical

states as relational operators do. The model of Part III shows that this subclass is not empty.



====================================================================================================
