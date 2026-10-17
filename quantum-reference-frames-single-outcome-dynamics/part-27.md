# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 27 of 40 (1,518 words)

13.13 Eight Distinctions Any Extension Must Respect



    (D1) Geometric covariance versus physical foliation independence. A foliation defined

    covariantly from the metric is not arbitrary, but a quantum dynamics built around it may still

    produce physically detectable preferred-frame effects. Theorem 13.4 identifies, for finite event

    structures, one sufficient condition under which it does not: causal locality of the realized-

    event dynamics, relative to an order that must itself be shown to be the operationally relevant

    causal order.



    (D2) Ensemble consistency versus realized-history consistency. A covariant master equation does

    not by itself supply a covariant stochastic ontology (Proposition 13.2).



    (D3) Clock neutrality versus absence of ontological ordering. A constrained quantum theory can

    lack a preferred clock variable while still admitting an additional generative interpretation;

    whether that interpretation is consistent must be proved (§14).



    (D4) Conditional compatibility propositions versus completed existence theorems. The

    Tomonaga–Schwinger and continuum-limit results of CTGP – explained (Proposition 17.16 and

    Theorem 17.17) are conditional, and their operator-theoretic and stochastic assumptions require

    further justification before they can count as existence theorems.



    (D5) Selective versus unread updates. Operational no-signaling concerns the unconditioned

    statistics of target outcomes, with the outcomes of all other operations summed over.

    Conditioning on an intermediate outcome is a different question, and Theorem 13.17 does not

    address it.



    (D6) Covariance of a law versus invariance of a realization. A Poisson law for collapse centres

    can be covariant under every isometry, although no realized configuration is invariant, and a

    covariant law for locations does not by itself supply covariant extended events (Theorem

    13.21(d), Proposition 13.24). Likewise, events triggered by the law rather than by an

    experimenter are spontaneous whether or not their locations have a covariant law.



    (D7) Localization of a field amplitude versus localization of matter. A collapse that localizes

    a smeared linear field observable does not thereby localize matter, and macroscopic localization

    is an independent obligation of physical adequacy (L2).



    (D8) Lorentz invariance, covariance with background structure, preferred-frame effects, and

    superluminal signaling. A law can be covariant under all isometries while depending on

    background structure such as cosmological time; such structure can produce preferred-frame

    effects, which are measurable only if an operational prediction shows how they reach a record;

    and a theory with preferred-frame effects need not permit superluminal signaling (§13.11). Each

    of the four must be established or excluded separately.



----------------------------------------------------------------------------------------------------

14. Temporal Quantum Reference Frames

----------------------------------------------------------------------------------------------------



14.1 Clock-Neutral Descriptions



A temporal quantum reference frame is not merely a coordinate clock. It is a quantum subsystem whose

correlations with the rest define the evolution of another subsystem. In a constrained system,

physical states satisfy Ĉ Ψ_phys = 0, and such a state is clock-neutral: it is not yet a description

relative to any particular clock. Choosing clock A yields a conditional description ψ^{(A)}(τ_A) of

the remaining degrees of freedom; choosing clock B yields ψ^{(B)}(τ_B). Höhn, Smith and Lock (2021)

show, for a class of constrained systems whose constraint is a sum of clock and system Hamiltonians,

that three formulations of relational dynamics are equivalent (clock-neutral relational observables,

Page–Wootters conditional states, and quantum deparametrization), and they develop transformations

between temporal frames.



The spatial construction of Part II transfers only in part. Temporal reduction maps R_A and R_B can

be defined, and where their inverses exist on the relevant sectors one can form V_{A→B} = R_B

R_A^{−1}. For realistic clocks, however, these maps involve conditional states, clock POVMs, and

sector restrictions, and they are not in general global unitaries of the kind used in Proposition

3.3. For ideal clocks they are unitary (Proposition 14.5).



14.2 Generation, Clock Readings, and Clock-Conditional Descriptions



Definition 14.1 (Three temporal notions). In a CTGP model with clock subsystems:



    (i) The generative succession is the order of stages, or of event slots, in which the history is

    generated.



    (ii) A clock reading is the value of a clock observable of a physical subsystem at a stage. It

    is a Tier 3 proposition (§5.1) unless a recording event makes it a Tier 1 fact.



    (iii) A clock-conditional description is a description of the rest of the world conditioned on

    the readings of a chosen clock.



CTGP identifies the ontological order of existence with (i) alone. A clock reading is physically

instantiated information about a process, in the sense of the signal-based epistemology discussed in

More Info, not automatically the fundamental ordering of existence.



14.3 A Worked Model With Imperfect Clocks



Proposition 14.2 (Imperfect clocks in a generative model). Consider a model of the kind defined in

Part II whose physical state includes one or more clock subsystems.



    (a) Clock-independence of event identity and probability. The measure over histories of Tier 1

    events is fixed by the law and the complete initial state. Describing those events relative to

    one clock rather than another changes no event label, no stage, and no probability.



    (b) Periodic clocks. A clock of period M takes the same reading at stages σ_n and σ_{n+M}, so

    equal readings do not imply equal stages: τ_A(σ_1) = τ_A(σ_2) is compatible with σ_1 ≠ σ_2. A

    repeated reading means that the clock fails to distinguish two stages, not that generation has

    reversed.



    (c) Temporal delocalization. If a clock is in a superposition of readings at the stage of an

    event, the Tier 3 proposition “the clock read r when the event occurred” has no determinate

    value, although the event and its stage are determinate. For example, a counter prepared in an

    equal superposition of the readings 0 and 4 and advancing by one per stage reads n or n + 4,

    each with probability 1/2, at stage n.



    (d) Clock-relative order can disagree with generative order. If a non-ideal clock’s readings are

    recorded at successive events, the later event can carry an earlier reading. Consider a drifting

    quantum-walk clock on a ring of 32 sites, which advances one site per stage on average under the

    one-step propagator S exp(−i θ (S + S†)) with θ = 0.9. Because a ring has no intrinsic linear

    order, comparing two readings requires a convention: the displacement between consecutive

    readings r_1 and r_2 is the representative m of r_2 − r_1 modulo 32 in {−15, …, 16}, and the

    second reading counts as lower when m < 0 and as equal when m = 0. Assume that each event

    records the clock’s reading by a projective measurement of its position, so that the first

    recording leaves the clock in a definite position state, and that exactly one stage transition

    separates two consecutive recordings. Then, conditional on the first recorded reading, the exact

    probabilities on the 32-site ring are P(m < 0) = 0.104042655 and P(m = 0) = 0.338161965, to nine

    decimal places. They agree to better than 10⁻¹² with the infinite-lattice expressions (1 −

    J_0(1.8)² − 2 J_1(1.8)²)/2 and J_1(1.8)², where J_n are Bessel functions. By translation

    invariance these values do not depend on the first reading. Displacements of eight or more sites

    have total probability below 10⁻⁸, so any comparison convention that agrees with this one on

    displacements of fewer than eight sites gives the same values to that accuracy. The values do

    depend on the preparation and recording procedure: a clock not recorded at the first event, an

    unsharp recording, or a comparison across more than one transition gives different values.



Proof. (a) Clock subsystems are part of the physical state, and the law takes the complete present

state as input; the choice of a subsystem as clock for purposes of description is not an input to

the law. If a clock interacts with the system, event probabilities depend on the clock’s physical

state, but that is a dependence on the present physical state, not on the choice of description. (b)

and (c) follow from the definitions. (d) The first recording projects the clock onto a position

eigenstate |r⟩. During the single intervening transition the clock evolves by the stated propagator.

By the Jacobi–Anger expansion, exp(−i θ (S + S†)) = Σ_{k∈ℤ} (−i)^k J_k(2θ) S^k, so on the infinite

lattice the amplitude to move from r to r + m is, up to a phase, J_{m−1}(2θ). On the ring S^{32} =

1, and the amplitude for displacement m is the sum of the lattice amplitudes for all displacements

congruent to m modulo 32. For m ∈ {−15, …, 16} the additional terms involve J_k(1.8) with |k| ≥ 16,

each of magnitude below 10⁻¹⁴, so the ring probabilities differ from the lattice values

J_{m−1}(1.8)² by less than 10⁻¹² in total. Summing the lattice values over m ≤ −1 gives Σ_{k≥2}

J_k(2θ)² = (1 − J_0(2θ)² − 2 J_1(2θ)²)/2, using Σ_k J_k² = 1 and J_{−k}² = J_k², and m = 0 gives

J_{−1}(2θ)² = J_1(2θ)². The exact ring values were computed directly from the 32-site propagator.

The computation is item 16 of Appendix B. □



Proposition 14.2 has an external generative order built in: the stage index is a parameter of the

model. It therefore shows that the three-way distinction of Definition 14.1 is consistent, and that

clock-relative localization and ordering can differ from generative order without contradiction. It

does not derive a definite generative order from clock-neutral data. That is the task of

§§14.4–14.6.


