# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 12 of 35 (1,784 words)

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
