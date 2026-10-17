# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 14 of 40 (1,650 words)

13.2 Hypersurface Evolution and Its Limits



A natural starting point is the Tomonaga–Schwinger equation (Tomonaga 1946; Schwinger 1948),



        i ħ δΨ_Σ / δΣ(x) = H_int(x) Ψ_Σ,



which describes how a state changes under local deformations of a spacelike hypersurface. Its formal

integrability condition is [H_int(x), H_int(y)] = 0 for spacelike-separated x and y. For interacting

fields this expression requires a treatment of operator-valued distributions and their domains; it

is not by itself an existence theorem. CTGP – explained proposes an open-system analogue, δρ_Σ /

δΣ(x) = ℒ_x(ρ_Σ), with conditional integrability (Proposition 17.16) and a conditional continuum

limit (Theorem 17.17). These are valuable starting points, but they are ensemble-level results: they

concern density operators. The next subsection shows why a single-outcome ontology needs more.



13.3 Ensemble Consistency Is Not Realized-History Consistency



Proposition 13.2 (Equal ensembles, different histories). There exist two instrument sequences whose

channels coincide at every stage, so that they assign the same density operator to every stage for

every initial state, but whose realized-history measures differ.



Proof. On a qubit, let the first instrument be either I_1 = { |0⟩⟨0|, |1⟩⟨1| } or I_2 = { 1/√2, Z/√2

}, where Z = |0⟩⟨0| − |1⟩⟨1|, and let the second be the measurement of X with outcomes ±, {|+⟩⟨+|,

|−⟩⟨−|}. Both first instruments implement the complete dephasing channel ρ ↦ |0⟩⟨0|ρ|0⟩⟨0| +

|1⟩⟨1|ρ|1⟩⟨1|, so the averaged states agree at every stage. For the initial state |+⟩, I_1 yields

outcomes 0 and 1 with probability 1/2 each and leaves |0⟩ or |1⟩, after which the X outcome is

uniformly random. I_2 yields its two outcomes with probability 1/2 each and leaves |+⟩ or |−⟩, after

which the X outcome is perfectly correlated with the first outcome. The joint laws of (first event,

second event) are uniform in the first case and perfectly correlated in the second: the mutual

information is 0 bits in one case and 1 bit in the other. □



Proposition 13.2 is an instance of the non-uniqueness of unravellings of a quantum channel (Wiseman

& Milburn 2010). Its consequence for CTGP is direct: a covariant or hypersurface-consistent master

equation does not by itself supply a covariant stochastic ontology. Two theories can agree on every

density operator on every hypersurface and still disagree about the probabilities of the realized

histories that, on CTGP, are what actually happened. Compatibility with a single-outcome ontology

therefore needs a consistency theorem at the level of realized histories, not only at the level of

states.



13.4 A Realized-History Consistency Theorem for Causally Local Instruments



The following theorem is a finite-dimensional analogue of the required relativistic result. Events

occur at a finite set of slots, ordered by a partial order intended to represent causal precedence;

a foliation is any way of advancing through the slots consistently with that order.



Definition 13.3 (Causally local event structure). A causally local event structure consists of a

finite partially ordered set (E, ≺) of event slots, a finite-dimensional Hilbert space H with

initial state Ψ_0, and for each slot x an instrument {K^x_a : a ∈ A_x} on H, such that for every

pair of incomparable (spacelike) slots x and y, every K^x_a commutes with every K^y_b. A foliation

is a linear extension λ = (x_1, …, x_N) of ≺; its successive initial segments {x_1, …, x_j} are the

regions to the past of its successive hypersurfaces. For an outcome assignment α = (a_x)_{x∈E}, set



        v_λ(α) = K^{x_N}_{a_{x_N}} ⋯ K^{x_1}_{a_{x_1}} Ψ_0,     P_λ(α) = ‖v_λ(α)‖².



Theorem 13.4 (Realized-history consistency). In a causally local event structure:



    (a) Foliation independence. v_λ(α) does not depend on the foliation λ. Hence the probability of

    every complete event history, P(α) = P_λ(α), and the corresponding final state are foliation-

    independent, and Σ_α P(α) = 1.



    (b) Consistency on every hypersurface. For every order ideal I ⊆ E (the past of some

    hypersurface) and every assignment α_I of outcomes to the slots in I, the probability of α_I and

    the conditional state on the hypersurface bounding I are the same for every foliation of I, and

    they do not depend on the instruments at slots outside I.



    (c) No dependence on instruments outside the designated predecessor set. For every set X ⊆ E,

    the marginal law of the outcomes in X depends only on the instruments in its predecessor set

    with respect to ≺, ↓X = { y : y ⪯ x for some x ∈ X }. Identifying ↓X with the operationally

    relevant relativistic causal past of X requires additional physical assumptions, discussed after

    Corollary 13.5.



Proof. (a) Any two linear extensions of a finite partial order are connected by a sequence of

adjacent transpositions of incomparable elements. To see this, let λ and λ′ first differ at position

j, where λ′ has x′. In λ, x′ occurs later; every element between position j and x′ in λ precedes x′

in λ, so it is not above x′, and follows x′ in λ′, so it is not below x′; hence it is incomparable

with x′. Moving x′ leftward in λ by adjacent transpositions with these elements yields a linear

extension that agrees with λ′ in one more position, and induction completes the argument. Each such

transposition exchanges two commuting operators and leaves v_λ(α) unchanged. Normalization follows

from Σ_a (K^x_a)† K^x_a = 1 applied slot by slot. (b) Because I is a down-set, any foliation of I

extends to a foliation of E that lists I first, and (a) applied to the sub-order I gives

independence of the foliation of I. Summing ‖v‖² over the outcomes of the slots after I and using

completeness of their instruments gives ‖v_I(α_I)‖², which involves only instruments in I. (c) Apply

(b) with I = ↓X, which is an order ideal containing X; the marginal on X is a marginal of the law of

α_I. □



Corollary 13.5 (Foliation-invisibility of the generative order in causally local finite models). In

a causally local event structure, suppose CTGP’s generative order is one particular foliation λ*.

Then every event proposition about any order ideal has the same probability whether computed along

λ* or along any other foliation. The realized assignment α is a single object, which different

foliations merely order differently; once the truth profile indexes events by slot rather than by

stage number, the complete profile after the whole region has been generated is the same set of

propositions whichever foliation is taken as generative.



Proof. Theorem 13.4(a)–(b). □



Corollary 13.5 is established for finite event structures under the stated locality assumption, not

for arbitrary relativistic quantum dynamics. It is the realized-history counterpart of CTGP’s

observational equivalence (CTGP – explained, §12.1): within causally local finite models, under the

commutation assumption of Definition 13.3, the choice of generative foliation has no empirical

signature, and a single realized history can be represented on any family of hypersurfaces without

multiplying the number of histories. If each K^x_a is invariant under a symmetry group in the sense

of §3, Lemma 3.7 applies slot by slot, and Theorem 13.4 holds in every frame.



Foliation-independent probabilities do not by themselves establish that any foliation is

ontologically privileged. What Corollary 13.5 shows is that privileging one foliation is empirically

invisible under the stated assumptions. That one foliation is in fact generative is CTGP’s

interpretive thesis, supplied separately, in the same way that Thesis 5.10 supplies the ontological

reading of description orbits.



The locality condition cannot be dropped. In the numerical check (Appendix B, item 14), a brickwork

arrangement of eight two-outcome instruments on six qubits has 136 foliations, and all of them

assign identical probabilities to all 256 outcome histories, to within 7 × 10⁻¹⁸. Changing the

instruments outside the predecessor set of a slot changes that slot’s marginal by at most 8 × 10⁻¹⁶.

But if two slots treated as spacelike act on overlapping qubits, so that their operators fail to

commute, the two orders assign history measures that differ by total-variation distance 0.165.



Theorem 13.4 must also be read with a caveat specific to quantum field theory. Part (c) is a

statement about the abstract order ≺: it says that outcomes do not depend on instruments outside a

designated predecessor set, not that relativistic operational no-signaling holds for arbitrary

spacetime regions or measurement procedures. The two coincide only if ≺ is the operationally

relevant causal order. For idealized point-like slots it is. For extended regions, however, the

transitive closure of “overlaps the causal future of” can relate two regions that are in fact

spacelike-separated, and naive local measurement rules then permit superluminal signaling (Sorkin

1993). A relativistic version of the theorem therefore needs a measurement framework in which

operations localized in regions respect relativistic causality; frameworks of this kind exist in

algebraic quantum field theory (Fewster & Verch 2020; Bostelmann, Fewster & Ruep 2021). The finite

theorem is an analogue of the relativistic result, not that result itself.



The relativistic target can now be stated precisely.



Target result 13.6 (Relativistic realized-history consistency). For a regulated relativistic single-

outcome model on a fixed globally hyperbolic background, given by a hypersurface-dependent family of

completely positive maps ℰ_{Σ_1→Σ_2} together with instruments assigning probabilities to realized

events between hypersurfaces, establish: (i) existence and normalization of the event-history

measure; (ii) composition consistency for nested regions; (iii) compatibility of operations in

spacelike-separated regions, in a framework free of Sorkin-type signaling; (iv) consistent

restriction of event histories to overlapping regions; and (v) a well-defined single-outcome

realization. Then prove that the probability of every common event-history proposition is

independent of the admissible intermediate hypersurface decomposition, and that the CTGP truth

profile updates consistently from the realized history.



Theorem 13.4 proves this for finitely many slots and finite-dimensional operators, Proposition 13.7

(§13.5) extends it to countably many slots with finite pasts, and Theorem 13.9 (§13.6) establishes

its measurement-model version for finite networks of gapless detectors on a free relativistic field.

The assumptions of the relativistic version must be made precise enough not to assume the

conclusion.


