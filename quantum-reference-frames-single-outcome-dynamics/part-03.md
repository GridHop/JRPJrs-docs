# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 03 of 35 (1,799 words)

Proposition 3.5 (Groupoid law). V_{A→B} is unitary; V_{A→A} = 1; V_{B→A} = V_{A→B}^{−1}; and V_{B→C}

V_{A→B} = V_{A→C}.



Proof. Immediate from Proposition 3.3 and Definition 3.4: V_{B→C} V_{A→B} = R_C R_B^{−1} R_B

R_A^{−1} = R_C R_A^{−1}. □



Explicit form. If A is subsystem 0 and B is subsystem 1, then frame-A coordinates are x_j = g_0^{−1}

g_j and frame-B coordinates are g_1^{−1} g_j. Substituting, g_1^{−1} g_0 = x_1^{−1} and g_1^{−1} g_j

= x_1^{−1} x_j, so



        V_{A→B} |x_1, x_2, …, x_M⟩ = |x_1^{−1}, x_1^{−1} x_2, …, x_1^{−1} x_M⟩,



where on the right the first slot is subsystem 0 (frame A) described relative to B. V_{A→B} permutes

basis states, so a superposition over x_1 in frame A becomes, relative to B, a correlated state of

frame A and all other subsystems. This is the familiar QRF effect: a frame-A product state can be a

frame-B entangled state (§6.3).



3.3 Invariant Operators and Their Frame Forms



An operator O on H_kin is invariant if U_h O = O U_h for all h. Invariant operators map H_phys to

itself.



Definition 3.6 (Frame form). The frame-A form of an invariant operator O is O^A = R_A O|_{H_phys}

R_A^{−1}, an operator on H_A.



Lemma 3.7 (Intertwining). For every invariant O and all frames A, B: V_{A→B} O^A V_{A→B}^{−1} = O^B.

Moreover, for every Ψ ∈ H_phys, ‖O Ψ‖ = ‖O^A R_A Ψ‖ and ⟨Ψ, O Ψ⟩ = ⟨R_A Ψ, O^A R_A Ψ⟩.



Proof. V_{A→B} O^A V_{A→B}^{−1} = R_B R_A^{−1} R_A O R_A^{−1} R_A R_B^{−1} = R_B O R_B^{−1} = O^B.

The second statement holds because R_A is unitary and O^A R_A = R_A O on H_phys. □



Remark 3.8 (Every frame-A operator is a frame form). Because R_A is unitary, every operator X on H_A

is the frame-A form of an invariant operator, namely R_A^{−1} X R_A on H_phys extended by zero on

the orthogonal complement of H_phys. (This operator commutes with every U_h because U_h acts as the

identity on H_phys and preserves its complement.) The invariance requirement therefore does not

restrict what a single frame can say. It restricts the relation between what different frames say:

if frame A uses X, frame B must use V_{A→B} X V_{A→B}^{−1}, not an operator that merely looks the

same in B’s coordinates. Section 5.3 turns this into the validity condition for frame-relative laws,

and §8 shows numerically that violating it produces a different world.



Remark 3.9 (Covariance is built into the framework, not discovered). By Lemma 3.7 and Remark 3.8,

any law that is well defined on H_phys has frame forms related by the frame-change unitaries. Frame

covariance of the dynamics below is therefore a consequence of the perspective-neutral framework,

not an independent finding. The substantive assumption is that the universe is closed, so that laws

act on H_phys rather than on H_kin with an external frame. The contribution of this preprint lies

elsewhere: in showing that a CTGP interpretation can be placed on such dynamics consistently, in

proving what that interpretation implies, and in identifying what CTGP adds (§11).



----------------------------------------------------------------------------------------------------

4. Dynamics, Ontology, and the Complete State

----------------------------------------------------------------------------------------------------



4.1 The Generative Law



Stages are indexed by σ in a discrete, linearly ordered set, written σ_0 < σ_1 < σ_2 < …, with σ′

denoting the successor of σ. The discrete index is used in Part II because every statement about it

can be proved by finite induction; §9 gives the continuous-time form and states how the two are

related.



Definition 4.1 (Admissible generative law). An admissible generative law consists of an invariant

unitary W on H_kin (the deterministic part of one stage-to-stage transition) and an instrument {F_k

: k ∈ 𝒦} of invariant operators on H_kin with Σ_k F_k† F_k = 1. The outcome set 𝒦 is countable, and

its elements are called transition events.



Definition 4.2 (Generative kernel). For a normalized Ψ_σ ∈ H_phys, the transition to σ′ is the

random pair (k, Ψ_{σ′}) with



        Pr(k | Ψ_σ) = ‖F_k W Ψ_σ‖²,     Ψ_{σ′} = F_k W Ψ_σ / ‖F_k W Ψ_σ‖.



The kernel K(Ψ_{σ′}, k | Ψ_σ) is the joint distribution so defined. Because W and F_k are invariant,

Ψ_{σ′} lies in H_phys again. States are rays: Ψ and e^{iθ} Ψ represent the same state, written Ψ ≐

e^{iθ} Ψ.



A history of length n is a sequence ω = (k_1, …, k_n) of transition events. Its probability given

Ψ_{σ_0} is the product of the successive transition probabilities, equivalently ‖F_{k_n} W ⋯ F_{k_1}

W Ψ_{σ_0}‖².



4.2 Primitive Ontology: What Exists at a Stage



A stochastic outcome label is not by itself an ontology. The following reading states what the

formalism is taken to represent.



Ontological Reading 4.3 (Primitive ontology). At stage σ, the present world consists of:



    (i) the present physical state [Ψ_σ], a ray in H_phys. It is physically real and governs the

    probabilities of all future events, but it is not itself material stuff located in space; it is

    a holistic state of the relational degrees of freedom;



    (ii) the present world’s past-tensed profile L_σ (§4.4).



The material ontology consists of transition events. A transition event is a primitive occurrence:

something that happens, once, in the generation of a stage from its predecessor. When it occurs it

is part of the generating present; at every later stage it is something that was the case, recorded

in L and carried forward causally through its effect on Ψ. Macroscopic facts, such as where a

pointer points, are patterns of transition events.



This is the flash ontology of GRW-type theories, with the wave function read realistically as part

of the present physical state. An alternative reading treats the wave function as nomological, so

that the events are the only physical ontology. On that reading, Tier 2 of the determinacy criterion

(§5.1) would concern the law’s current parameter rather than a physical state, but Tiers 1 and 3 and

every theorem below would be unchanged. Reading 4.3 is adopted because CTGP identifies S_σ as the

present physical state governing successor generation (C-f).



4.3 Primitive Events Versus Sharp Relational Properties



Each transition event k has an associated effect



        E_k = F_k† F_k,



which is a positive operator on H_phys. The effect determines the probability of the event: Pr(k |

Ψ_σ) = ⟨W Ψ_σ, E_k W Ψ_σ⟩. The event and the effect are different kinds of thing. The effect is part

of the law. The event is an additional fact: that, of all the events the law made possible, this one

occurred. That additional fact is what single-outcome realism (C-d) asserts and what Everettian

ontology denies.



In particular, an event concerning a relational quantity need not be the possession of a sharp value

of that quantity. In the model of Part III, an event (i, j, d) is a flash centred on the separation

d between particles i and j, with finite width s. Its occurrence does not make the proposition “the

separation of i and j is d” true.



Proposition 4.4 (Finite-width events do not create sharp values). Let F_k = Σ_r c_k(r) P(r) where

{P(r)} is a complete family of orthogonal invariant projectors and c_k(r) ≠ 0 for every r. If,

before the event, W Ψ_σ is not an eigenvector of a given P(r), then after the event Ψ_{σ′} is not an

eigenvector of P(r) either.



Proof. Since F_k is diagonal in the decomposition {P(r)} with nonzero coefficients, P(r′) Ψ_{σ′} ∝

c_k(r′) P(r′) W Ψ_σ is nonzero exactly when P(r′) W Ψ_σ is nonzero. The set of r′ with nonzero

component is therefore unchanged by the event, and a vector is an eigenvector of P(r) (with

eigenvalue 1 or 0) exactly when that set is {r} or omits r. □



So in the finite-width model the event is a Tier 1 fact, while the sharp-value proposition about

separation remains without a determinate value (Tier 3 of §5.1). The sharp limit s → 0, in which

c_k(r) vanishes for r ≠ d, is the special case in which an event does produce a sharp value. This

distinction answers the objection that a flash ontology merely renames a measurement outcome: the

event is not the readout of a pre-existing value, and not the acquisition of a sharp one, but a

primitive occurrence whose probability the law fixes.



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
