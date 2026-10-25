# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 14 of 35 (1,800 words)

each occurring with probability 1/2 in |0⟩. A unitary kick W(α f_j) acts in the same diagonal way:

W(−α f_j) W(g) W(α f_j) = e^{i α E(f_j,g)} W(g).



Theorem 13.9 (Gapless detector networks). In a gapless detector network on a free field, for any

state of the field:



    (a) Realized-history consistency. The probability of every complete outcome history, and the

    corresponding conditional state, are the same for every foliation, that is, for every linear

    extension of ≺.



    (b) Operational no-signaling, including Sorkin configurations. Let X be a set of detectors, and

    let j ∉ X be a detector with E(f_j, f_x) = 0 for every x ∈ X; this holds in particular when no

    causal curve joins O_j to any O_x. Then the joint law of the outcomes of the detectors in X is

    the same whether detector j is operated with any coupling λ_j, replaced by a kick W(α f_j), or

    not operated at all, whatever other detectors are operated before, between, or after them.



    (c) Explicit statistics. If detector B is preceded by detectors j_1, …, j_r whose outcomes are

    not conditioned on, and the field is in a quasi-free state with vanishing one-point function,

    then



        P(B reads 1) = ½ − ½ exp(−2 λ_B² ω(φ(f_B)²))

                         · Π_{k=1}^{r} cos(2 λ_B λ_{j_k} E(f_{j_k}, f_B)).



Proof. (a) If two regions are incomparable, no causal curve joins them, so E(f_i, f_j) = 0, the Weyl

operators W(s f_i) and W(t f_j) commute for all s and t, and so do all bounded functions of φ(f_i)

and φ(f_j). The Kraus operators of incomparable detectors therefore commute. Theorem 13.4 applies,

in the form for bounded Kraus operators noted in the proof of Proposition 13.7, in the GNS

representation of the state.



(b) Compute the joint law of X in the Heisenberg picture, along any foliation. Every detector

outside X is marginalized, so it contributes its nonselective update N_k*. Every detector in X

contributes a selective update K† (·) K with K = cos(λφ(f_x)) or i sin(λφ(f_x)); each of these maps

a Weyl operator W(g) to a linear combination of Weyl operators W(g + c f_x) with real c. Starting

from the identity W(0), the operator under evaluation is therefore at every step a finite linear

combination of Weyl operators W(g) with g in the real span V_X of { f_x : x ∈ X }. Each nonselective

update of a detector k ∉ X multiplies such a W(g) by cos(λ_k E(f_k, g)). For k = j, E(f_j, g) = 0

for every g ∈ V_X by linearity, so the factor is 1, and the same holds for a kick. Detector j

therefore drops out of the joint law of X.



(c) Write sin²(λ_B φ(f_B)) = ½ − ¼ (W(2λ_B f_B) + W(−2λ_B f_B)). Each preceding detector,

marginalized, multiplies W(±2λ_B f_B) by cos(2 λ_B λ_{j_k} E(f_{j_k}, f_B)), and ω(W(±2λ_B f_B)) =

exp(−2 λ_B² ω(φ(f_B)²)). □



Part (b) is the statement that matters for CTGP, and its scope should be stated exactly. It is

state-independent; it holds for arbitrary smooth, compactly supported real smearings within finite,

causally orderable networks, under the free-field and gapless-detector assumptions; and it holds in

Sorkin’s configuration. There, Alice’s region A is causally separated from Bob’s region B, while an

intermediate region C overlaps the causal future of A and the causal past of B. A gapless detector

at C cannot carry Alice’s choice to Bob, because its nonselective update multiplies each Weyl

operator by a number instead of spreading it. Part (c) makes this explicit: Bob’s statistics depend

on a preceding detector only through the factor cos(2 λ_B λ_j E(f_j, f_B)), which equals 1 for every

detector causally separated from B. The essential property is that the nonselective update is

diagonal on Weyl operators. It holds for gapless linear couplings with any such smearing. It can

fail for detectors with internal dynamics during the interaction, and de Ramón, Papageorgiou and

Martín-Martínez (2021) find that spatially extended non-relativistic detector models can propagate a

field’s initial conditions faster than light. The conclusion agrees with detector-based measurement

theory, in which updates induced by local probe couplings avoid Sorkin-type signaling (Polo-Gómez,

Garay & Martín-Martínez 2022; compare Fewster & Verch 2020).



Three things should be distinguished in interpreting the theorem: the spacetime support O_j of the

detector–field interaction; the location and timing of the detector’s readout; and the effective

instrument on the field obtained by conditioning on that readout. Theorem 13.9 concerns the third.

It proves causal properties of the effective field instruments of the network, assuming that each

detector is read out after its interaction and treating the detector as an idealized probe. When a

coupling region is extended, a fully spacetime-local implementation of the detector together with

its readout would require further modeling of the probe itself. This qualification concerns physical

realization; it does not affect the algebraic proof.



Theorem 13.9 is exact within its model, and the numerical checks below only illustrate it. Exactness

within a model is not physical completeness. The model assumes a fixed spacetime, a free field,

externally specified couplings, and detectors with no internal Hamiltonian during the interaction,

and these assumptions are central to the proof. A nonzero energy gap makes the coupled detector

observable time-dependent, and the nonselective update then generally ceases to be diagonal on Weyl

operators. The theorem is therefore not a claim about arbitrary relativistic detector measurements,

realistic detector hardware, or interacting fields.



Example 13.10 (Localized Kraus operators are not enough). Replace the detector at C by the unsharp

Lüders instrument with Kraus operators √(g(φ(f_C))) and √(1 − g(φ(f_C))), where g(x) = (1 + tanh

2x)/2. Its Kraus operators are bounded functions of the smeared field in C, so it satisfies (E2),

and they commute with every operation localized in a region causally separated from C. But its

nonselective update is not diagonal on Weyl operators:



        Σ_s √(g_s(φ(f_C))) W(h) √(g_s(φ(f_C))) = W(h) Σ_s √(g_s(φ(f_C) + E(h, f_C))) √(g_s(φ(f_C))),



with g_+ = g and g_− = 1 − g. The right-hand side is W(h) times a non-constant function of φ(f_C),

which fails to commute with φ(f_A) when E(f_A, f_C) ≠ 0. An operation by Alice can therefore change

Bob’s statistics through C even though A and B are causally separated. This is Sorkin’s problem. A

numerical realization reproduces the commutation pattern of Sorkin’s configuration (E(f_A, f_B) = 0,

E(f_A, f_C) = E(f_C, f_B) = 1) with two oscillator modes in the vacuum state, using λ_A = 0.9, λ_C =

0.8, λ_B = 0.7, and a kick with α = 1.5 (Appendix B, item 17). With a gapless detector at C, Bob’s

probability of reading 1 is 0.3665447170, equal to the formula of Theorem 13.9(c), and neither

Alice’s detector nor her kick changes it by more than 10⁻¹⁵. With the unsharp Lüders instrument at

C, Bob’s probability is 0.275038, and Alice’s detector shifts it by −0.021492 and her kick by

−0.046628. These values change by less than 10⁻⁷ when the Fock cutoff is raised from 40 to 50 quanta

per mode. Because Theorem 13.9(b) is state-independent and uses only the commutation relations, the

two-mode realization is an exact test of the algebraic mechanism, not a computation in a particular

spacetime.



Example 13.10 shows why (E2) and (E3) must be kept separate. Localizing the Kraus operators of each

operation is not enough. Causal admissibility is a property of the actual instruments and of their

composition, and it must be proved for the class of operations in use; Theorem 13.9 proves it for

gapless detector networks on a free field, and Theorem 13.13 for every network of Weyl-diagonal

instruments.



Connection to CTGP. In a gapless detector network the realized detector outcomes are Tier 1 events,

and the complete present state on an admissible hypersurface consists of the field state together

with the detectors’ records. For a specified network, the law of the next outcome depends only on

that present state, so the network is generable in the sense of Definition 12.1, (A2)–(A5). The

truth profile records the realized outcomes and is dynamically idle. Because cosmological time is in

general only locally Lipschitz (§13.1), the construction is formulated for arbitrary admissible

orderings. A generic globally hyperbolic spacetime also admits smooth Cauchy temporal functions

(Bernal & Sánchez 2003, 2005). Whenever the coupling regions can be separated by level sets of the

cosmological time T, ordering them by T is a linear extension of ≺, because T increases strictly

along future-directed causal curves. CTGP’s generative order is then one of the admissible

foliations, and by Theorem 13.9(a) and Corollary 13.5 the history law is the same for it as for any

other. Three steps must be kept apart here. First, the network’s history law is independent of the

admissible ordering of its regions; Theorem 13.9 establishes this. Second, the background spacetime

admits a regular cosmological time whose level sets separate the regions; this is an assumption

about the geometry. Third, those level sets are the ontological presents; this is CTGP’s

interpretation. Theorem 13.9 supports only the first step, which is what makes the other two

consistent with it. Within this class, then, the measurement-model version of Target 13.6 holds for

finite networks: (i)–(v) are satisfied, with (iii) secured by part (b). What remains open is the

spontaneous version, detectors with internal dynamics, interacting fields, and infinitely many or

continuously distributed events, that is, (E4) and (E6).



13.7 Toward Spontaneous Events: Weyl-Diagonal Collapse



The proof of Theorem 13.9(b) uses one property of the gapless detector: its nonselective update

multiplies every Weyl operator by a number. Inserting arbitrary stochastic collapses into the model

would risk reintroducing the signaling of Example 13.10. The natural route toward spontaneous events

is therefore to keep that property and ask which event-generating instruments have it.



Definition 13.11 (Weyl-diagonal instrument). Let O be a bounded spacetime region and H_O a finite-

dimensional space of real test functions supported in O. An instrument with finitely or continuously

many outcomes is a Weyl-diagonal instrument localized in O if (i) its Kraus operators belong to the

von Neumann algebra generated by the Weyl operators W(h), h ∈ H_O, and (ii) its nonselective update

satisfies N*(W(g)) = c(g) W(g) for every test function g, for some function c.



Examples are the gapless detector of Definition 13.8, with c(g) = cos(λ E(f, g)), and the unitary

kick, with c(g) = e^{iαE(f,g)}. The random-displacement channel ρ ↦ ∫ W(h) ρ W(h)* dμ(h), with μ a

probability measure on H_O, is also Weyl-diagonal, with c(g) = ∫ e^{iE(h,g)} dμ(h). The nonselective

gapless detector is exactly the random displacement by +λf or −λf, each with probability 1/2.



Proposition 13.12 (Gaussian collapse of a smeared field). Let h be a real test function supported in

O and σ > 0. The instrument with outcome y ∈ ℝ and Kraus operators



        K_y = (2πσ²)^{−1/4} exp(−(φ(h) − y)² / (4σ²))


