# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 02 of 35 (1,790 words)

are the same in every frame (§5.3–5.4). And L sits beside the quantum state without driving it: it

is not a function of the present state, the law never takes it as input, and given the law it is

accurate to the state it accompanies (§4.6, §5.6). Part III shows that an explicit dynamics, in

discrete-stage and continuous-time form, has all of these properties.



Part V looks beyond the finite model. Relativistic quantum field theory, temporal quantum reference

frames, and quantum gravity each put CTGP’s commitments under new pressure, and none of them can be

settled by the constructions of Parts II–IV. Part V therefore turns the commitments into an

admissibility criterion and proves what can be proved now. In finite form, this includes a realized-

history consistency theorem under which, in causally local finite models, the choice of generative

foliation is empirically invisible. In relativistic form, it includes networks of gapless detectors

on a free field with operational no-signaling in Sorkin’s configuration, a regulated spontaneous-

collapse network built from Gaussian collapses of smeared fields together with the exact energy cost

of such collapses, a no-signaling criterion that does not depend on free fields, and collapses at

Poisson-distributed locations, conditionally on causally orderable configurations, together with the

obstructions to a fully covariant version and a candidate completion using cosmological time that is

developed but not adopted. For quantum clocks, it includes a construction with two ideal clocks in

which the interventions are part of the constraint. Part V also states the remaining obligations and

possible obstructions precisely, so that each direction can be pursued as a sequence of mathematical

results.



----------------------------------------------------------------------------------------------------

2. Background

----------------------------------------------------------------------------------------------------



2.1 Quantum Reference Frames and the Perspective-Neutral Framework



In standard quantum mechanics, states are written relative to an external classical reference frame:

positions are measured from a fixed origin. If the universe is treated as closed, there is no

external frame, and only relations between subsystems are physical. The perspective-neutral

framework (Vanrietvelde et al. 2020; de la Hamette & Galley 2020; Krumm, Höhn & Müller 2021)

implements this by imposing invariance under a symmetry group G acting on all subsystems at once.

The kinematical Hilbert space H_kin carries a unitary representation U of G, and the physical

(perspective-neutral) Hilbert space H_phys is the subspace of states invariant under every U_g.

These states make no reference to any external frame. Choosing a subsystem as reference frame

defines a reduction map from H_phys to a frame-relative Hilbert space describing the remaining

subsystems relative to that frame, and changes of quantum reference frame are compositions of one

reduction map with the inverse of another. This construction reproduces the frame changes of

Giacomini, Castro-Ruiz and Brukner (2019), and Krumm, Höhn and Müller (2021) show that QRF

transformations are canonically defined on the invariant sector. Related ideas appear in the

literature on reference frames and superselection (Aharonov & Kaufherr 1984; Bartlett, Rudolph &

Spekkens 2007) and on relational quantities (Loveridge, Miyadera & Busch 2018).



Two features matter for CTGP. First, frame changes in this framework are not choices of “whose

facts” to consider; they are changes of description of one invariant state, which is the reading

CTGP needs. Second, operators that are not invariant under G do not in general map H_phys to itself,

so a law written in absolute, non-relational terms is not well defined on physical states. This

constraint does substantive work in §7.4.



2.2 Single-Outcome Dynamics as Quantum Instruments and Jump Processes



A stochastic quantum dynamics with definite outcomes can be written as a sequence of quantum

instruments (Davies & Lewis 1970; Kraus 1983). An instrument is a family of operators {F_k}, indexed

by outcomes k, satisfying the completeness relation Σ_k F_k† F_k = 1. Given a normalized state ψ,

outcome k occurs with probability ‖F_k ψ‖², and the state is updated to F_k ψ / ‖F_k ψ‖. In

continuous time, the corresponding object is a piecewise-deterministic jump process: the state

evolves smoothly between random jump times and jumps by normalized jump operators, and its ensemble

average obeys a Lindblad master equation (Lindblad 1976; Gorini, Kossakowski & Sudarshan 1976;

Dalibard, Castin & Mølmer 1992; Breuer & Petruccione 2002).



Objective-collapse models have this form. In the GRW model, a spontaneous “hit” multiplies the wave

function by a Gaussian of fixed width centred at a random point, with the centre drawn according to

the Born rule, and hits occur at the times of a Poisson process. Bell (1987) proposed taking the hit

events themselves, the “flashes”, as the primitive ontology: the material world consists of the

flashes, and the wave function governs their probabilities. Tumulka (2006) gave a relativistic

version (rGRWf). Allori, Goldstein, Tumulka and Zanghì (2008) analyze the common structure of such

primitive-ontology theories.



The instrument picture gives the generative law a precise meaning. One stage-to-stage transition

applies the deterministic part of the dynamics, then samples an outcome k from the instrument and

updates the state. The pair (new state, outcome) is drawn from a probability kernel that depends

only on the current state, which is the form of law required by CTGP’s generability constraint (CTGP

– explained, §12.2): a law fixing transition probabilities P(S_{σ′} | S_σ) without reference to data

on later stages.



2.3 The CTGP Commitments Used Here



The following CTGP commitments are used below, cited to CTGP – explained and More Info.



    (C-a) Ontological primacy of the present (Postulate 1). Only the current stage exists.



    (C-b) Lucretian truthmakers (§5.2.1; Definition 17.20). “At σ′ it was the case that φ” is true

    at σ iff the present world W_σ instantiates the primitive property Had(σ′, φ). The accuracy

    condition requires that W_σ instantiates Had(σ′, φ) iff W_σ′ ⊨ φ, and past-tensed properties,

    once acquired, are retained (Proposition 17.22, No Revision of the Past).



    (C-c) Non-supervenience. Past-tensed properties do not supervene on the present’s categorical

    physical configuration: two present states could agree in every categorical respect while

    differing in their pasts (§5.2.1).



    (C-d) Single-outcome realism (§10.1). At each stage, each measurement has exactly one realized

    macroscopic outcome. Relational interpretations that make facts relative to observers are not

    available to CTGP.



    (C-e) Definite generative ordering (§6.4). Of two causally related stages, one precedes the

    other.



    (C-f) Generability (§12.2). There is a state S_σ on each stage and a law fixing P(S_{σ′} | S_σ)

    for σ′ > σ without reference to later data. Enlarging the state space is legitimate only if the

    added variables are physically instantiated on the present stage and have dynamics of their own.



    (C-g) Causal inheritance (More Info, §11). Whatever part of history can still affect the future

    must already be physically instantiated in the present; two present states that agree in every

    physically instantiated respect have futures governed identically by the laws, whatever their

    histories.



    (C-h) Continuous generation (CTGP – explained, Abstract and §5.4). Generation is a continuous

    causal-temporal progression, not a succession of disconnected states.



    (C-i) Truth versus recoverability (More Info, §§4, 9–10). Whether something happened is settled

    by the present world’s past-tensed profile; whether anyone can establish that it happened

    depends on surviving records and available signals. Some truths may be structurally unknowable.



    (C-j) Relational descriptive freedom. Different valid reference frames, clocks, and formulations

    may describe the same physical history differently; CTGP requires one history, not one

    description of it.



    (C-k) Emergent classical cosmic time (CTGP – explained, §6). In the general-relativistic regime,

    where the structure exists, the generative present is identified with the level sets of a

    regular cosmological time function. This commitment is conditional on the classical spacetime

    admitting that structure; §13.1 states the regularity results precisely.



    (C-l) No density-weighted generation (CTGP – explained, §11). Generation laws on which regions

    become real at rates set by local matter density fail CTGP’s consistency analysis; the

    generation rate may vary with cosmic epoch but not across space.



One terminological point prevents a misunderstanding. The model below uses relational quantities:

the transition events concern separations between particles, not positions relative to an external

origin. This is not a relational interpretation in the sense rejected by (C-d). Whether a given

event occurred is an absolute, frame-independent fact; what is relational is the quantity the event

concerns, in the same way that “the distance between two stones is one metre” is an absolute fact

about a relational quantity.



====================================================================================================

PART II. The Formalism

====================================================================================================



----------------------------------------------------------------------------------------------------

3. Kinematics: Perspective-Neutral States and Frame Reductions

----------------------------------------------------------------------------------------------------



3.1 The Perspective-Neutral State Space



Let G be a finite group with identity e. Consider M + 1 subsystems labelled 0, 1, …, M, each with

Hilbert space ℓ²(G), the space of complex functions on G, with orthonormal basis {|g⟩ : g ∈ G}. The

basis state |g⟩ represents the subsystem having “orientation” g, for example being at site g of a

lattice. This setting is chosen because every statement in it can be proved exactly.



Definition 3.1 (QRF system). The kinematical space is H_kin = ℓ²(G)^{⊗(M+1)}. The group acts

diagonally by



        U_h |g_0, g_1, …, g_M⟩ = |h g_0, h g_1, …, h g_M⟩,



and the physical, or perspective-neutral, space is the invariant subspace



        H_phys = { Ψ ∈ H_kin : U_h Ψ = Ψ for all h ∈ G },  with projector  Π = (1/|G|) Σ_{h∈G} U_h.



A state Ψ in H_phys assigns amplitudes only to relations among subsystems: its wave function

satisfies Ψ(h g_0, …, h g_M) = Ψ(g_0, …, g_M) for all h.



3.2 Frame Reductions



Definition 3.2 (Frame reduction). Choosing subsystem A as the reference frame, the frame-relative

space is H_A = ℓ²(G)^{⊗M}, describing the other M subsystems relative to A. The reduction map R_A :

H_phys → H_A conditions the frame on the identity orientation and rescales:



        (R_A Ψ)(x_1, …, x_M) = √|G| · Ψ(e, x_1, …, x_M)       (frame A taken as subsystem 0).



Its inverse embeds a frame-relative state into the invariant sector:



        R_A^{−1} φ = |G|^{−1/2} Σ_{a∈G} Σ_{x} φ(x_1, …, x_M) |a, a x_1, …, a x_M⟩.



The same definitions apply with any other subsystem as the frame, with the remaining subsystems

listed in a fixed order.



Proposition 3.3 (Reductions are unitary). For every subsystem A, R_A is a unitary map from H_phys

onto H_A, with inverse given above.



Proof. Let Ψ ∈ H_phys. Invariance gives Ψ(g_0, g_1, …, g_M) = Ψ(e, g_0^{−1} g_1, …, g_0^{−1} g_M).

Write φ(x) = Ψ(e, x_1, …, x_M). Then ‖Ψ‖² = Σ_{g_0} Σ_{x} |φ(x)|² = |G| ‖φ‖², so ‖R_A Ψ‖ = √|G| ‖φ‖

= ‖Ψ‖. Conversely, for any φ ∈ H_A the vector R_A^{−1} φ defined above is invariant (left

multiplication by h permutes the summation index a), and R_A R_A^{−1} φ = φ by direct substitution.

Hence R_A is an isometry onto H_A, that is, unitary. □



Definition 3.4 (Valid frame change). For frames A and B, the frame change is



        V_{A→B} = R_B R_A^{−1} : H_A → H_B.


