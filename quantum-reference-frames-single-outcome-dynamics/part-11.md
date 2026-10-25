# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 11 of 35 (1,792 words)

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

PART V. A Compatibility Program: Quantum Fields, Quantum Clocks, and Quantum Gravity

====================================================================================================



----------------------------------------------------------------------------------------------------

12. The CTGP Admissibility Criterion

----------------------------------------------------------------------------------------------------



Parts II–IV establish compatibility for a finite, non-relativistic model with spatial quantum

reference frames. Part V asks how the same commitments can be carried toward relativistic quantum

field theory (RQFT), temporal quantum reference frames, and quantum gravity. It does not redesign

CTGP. It states the commitments to be preserved, turns them into a single admissibility criterion,

proves the results that can be proved now in finite form, and identifies precisely what would have

to be established, and what would count as an obstruction, in each of the three directions. Results

in this Part are labeled by status: theorems and propositions are proved; definitions marked as

proposals are offered for adoption rather than derived; conjectures and target results are open.



12.1 The Central Principle and the Commitments to Preserve



The organizing principle of the program is this:



    CTGP requires one objectively generated physical history. It does not require every observer,

    clock, quantum representation, or mathematical formulation to describe that history in the same

    way.



The principle is already at work in Parts II–IV: frame descriptions differ, sometimes as product

versus entangled states (§6.3), while determinacy, truth, and the history measure are frame-

independent (Proposition 5.2, Theorems 5.12 and 5.16). It leaves room for relativistic covariance,

for quantum clocks, and potentially for quantum geometry, without abandoning the central ontology.

It does not guarantee success: some quantum-gravity proposals could be fundamentally incompatible

with CTGP, and no rigorous relativistic single-outcome model with CTGP’s structure yet exists.



The commitments to be preserved are those of §2.3, grouped as follows.



    (P1) Presentism (C-a): only the currently generated physical configuration exists.



    (P2) A single realized history (C-d): there is one factual sequence of physical outcomes.



    (P3) Generability (C-f): the complete present physical state and the laws fix the probability

    distribution of successors, without indispensable independent future boundary inputs.



    (P4) Causal inheritance (C-g): whatever part of history can still affect future physics is

    instantiated in present physical variables.



    (P5) Relational descriptive freedom (C-j): different valid reference frames may describe the

    same physical history differently.



    (P6) Emergent classical cosmic time (C-k): in the general-relativistic regime where the required

    structure exists, the objective present corresponds to the level sets of a regular cosmological

    time function.



Commitment (P6) is conditional on the classical spacetime admitting the required structure, and it

should not be imposed unchanged on a quantum regime in which classical geometry is undefined (§15).

CTGP’s negative result on density-weighted generation (C-l) constrains every realization: the

extension must not make different regions become real at rates set by local matter density. Local

matter, fields, clocks, and stochastic events may evolve differently while belonging to one

underlying generative ordering.



12.2 The Criterion



Write the ontological state at a generative stage σ as Ω_σ = (S_σ, L_σ), with S_σ the complete

physically instantiated state and L_σ its primitive past-tensed truth profile. A physical extension

must supply a forward transition law K_{σ,σ′}(S_σ, dS′ de) for σ′ > σ, where e denotes the realized

event data of the transition.



Definition 12.1 (CTGP-admissible theory; a proposal). A physical theory is CTGP-admissible on a

specified domain if it has a formulation with the following features.



    (A1) Present state. A complete, physically instantiated present state S_σ on each stage of a

    generative ordering.



    (A2) Forward law. Transition kernels K_{σ,σ′} that are normalized and satisfy the composition

    relation K_{σ,σ″} = K_{σ′,σ″} ∘ K_{σ,σ′} for σ < σ′ < σ″, with integration over intermediate

    states and concatenation of event data.



    (A3) One realized history. A single realized sample path of events, with the truth profile

    updated from it, L_{σ′} = Update(L_σ, S_σ, e, S_{σ′}).



    (A4) No indispensable future input. No independent future boundary condition is required, in the

    sense of CTGP – explained, §12.2: future dependence disqualifies only if no empirically

    equivalent forward formulation exists (compare §11).



    (A5) Causal idleness of the past. Pr(S_{σ′}, e | S_σ, L_σ) = Pr(S_{σ′}, e | S_σ).



    (A6) Frame and gauge consistency. Admissible reference-frame and gauge transformations preserve

    the probabilities and the identities of realized physical events.



    (A7) Classical realization. Wherever the domain includes the classical general-relativistic

    regime in which CTGP claims (P6), the generative ordering is realized by the level sets of

    regular cosmological time.



Primitive past-tensed truths may be included in the ontology, but by (A5) they supply no causal

input absent from the complete physical state.



Definition 12.1 is a proposal, not a theorem about any interacting relativistic or quantum-

gravitational theory. Its value is that it turns the broad question whether CTGP can be compatible

with quantum physics into a list of precise mathematical obligations.



Proposition 12.2 (The finite model is CTGP-admissible on its domain). The discrete-stage and

continuous-time models of Part III satisfy (A1)–(A6), with (A6) restricted to the spatial QRFs of

§3; (A7) is vacuous on their domain, which contains no classical spacetime.



Proof. (A1): the present state is the ray [Ψ_σ] in H_phys. (A2): the kernels are Markov; in discrete

time, composition is the product of one-step kernels; in continuous time it follows from the

factorization of record densities (Proposition 9.9). (A3): Definition 4.6 and Theorem 4.8;

Definition 9.5 and Theorem 9.7. (A4): §10.2, with §11 for the sense of future dependence. (A5):

Corollary 4.10 and Proposition 9.9. (A6): Theorems 5.12, 5.16, and 9.10. □



12.3 Three Levels of Compatibility



“Compatibility” is used in three distinct senses, and keeping them apart is essential to every claim

in this Part.



Level        | What has been established

-------------+------------------------------------------------------------------------------

Conceptual   | No identified logical contradiction under specified assumptions

Mathematical | A well-defined model satisfies CTGP’s stated compatibility conditions

Physical     | The model reproduces the required observations and survives empirical tests



Table 3. Three levels of compatibility.



The finite model establishes mathematical compatibility on its own domain (Proposition 12.2). It

does not establish physical compatibility, and a mathematically consistent model can be physically

inadequate. The results below for the relativistic, temporal, and gravitational directions are of

three kinds: finite-dimensional theorems that are analogues of the required results, conditional

propositions, and open targets.



12.4 Ontology Versus Implementation



CTGP’s foundational ontology is what (P1)–(P6) assert. A relativistic flash model, a Bohmian field

theory, or a quantum-gravitational causal structure might each satisfy Definition 12.1 by quite

different physical mechanisms. They are therefore candidate realizations to be investigated, not

components of CTGP itself. The same holds for the ring model of Part III: it is one realization,

chosen because every claim about it can be proved.



----------------------------------------------------------------------------------------------------

13. Relativistic Quantum Fields: Realized-History Consistency

----------------------------------------------------------------------------------------------------



13.1 Background Structure



The first construction should not quantize gravity. It should assume a fixed classical spacetime (M,
