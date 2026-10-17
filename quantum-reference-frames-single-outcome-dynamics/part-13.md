# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 13 of 40 (1,624 words)

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

g) with a regular cosmological time function T(p) = sup { L(γ) : γ a past-directed causal curve from

p }, and take the proposed CTGP presents to be the level sets Σ_t = T^{−1}(t).



The relevant regularity results are those of Andersson, Galloway and Howard (1998), and they must be

stated with care. If T is regular, meaning finite everywhere and tending to zero along every past-

inextendible causal curve, then (M, g) is globally hyperbolic; T is a time function, continuous and

strictly increasing along future-directed causal curves; every point p lies at the future end of a

maximal timelike geodesic of length T(p) issuing from the initial singularity; and T is locally

Lipschitz, with first and second derivatives existing almost everywhere. The nonempty level sets are

closed, acausal, edgeless, and future Cauchy surfaces: their future Cauchy horizons are empty

(Andersson, Galloway & Howard 1998, Corollary 2.6). They need not be Cauchy surfaces in the full,

two-sided sense, and the paper says so explicitly. The following proposition states exactly when

they are.



Proposition 13.1 (When a level set is a Cauchy surface). Let T be regular and let S_a = T^{−1}(a) be

nonempty. Then S_a is a Cauchy surface if and only if every future-inextendible causal curve

contains points at which T > a.



Proof. (⇐) Let γ be an inextendible causal curve. By regularity, T tends to zero toward the past end

of γ, and by hypothesis T exceeds a somewhere on γ. Since T is continuous and strictly increasing

along γ, γ meets S_a exactly once. Every inextendible causal curve therefore meets S_a exactly once,

so S_a is a Cauchy surface. (⇒) Suppose some future-inextendible causal curve γ has T ≤ a at all of

its points, and extend it to the past to an inextendible causal curve. Because T is strictly

increasing, T < a along the whole extended curve (were T = a at some point, T would exceed a beyond

it). The curve never meets S_a, so S_a is not a Cauchy surface. □



In FLRW models with a big-bang singularity, whether they expand forever or recollapse, cosmological

time is the FLRW time and every level set is a Cauchy surface. But a causal curve that ends at a

singularity inside a black hole typically has bounded T, and level sets beyond that bound are not

met by it. In universes containing black holes, later level sets can therefore be future Cauchy

surfaces without being Cauchy surfaces. Any CTGP claim that the present is a Cauchy surface should

accordingly be restricted to the level sets satisfying Proposition 13.1, with the future Cauchy

property as the general statement.



For quantum fields on such a background, a state is assigned to each admissible hypersurface, as a

density operator ρ_Σ or a vector state Ψ_Σ in a suitable representation. In curved-spacetime quantum

field theory there is in general no single preferred Fock representation, and the algebraic

formulation, in which states are positive normalized functionals on a net of local observable

algebras, is the more appropriate setting (Wald 1994; Hollands & Wald 2015).


