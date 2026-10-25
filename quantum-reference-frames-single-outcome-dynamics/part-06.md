# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 06 of 35 (1,798 words)

distribution in any other frame B, with event labels unchanged and states mapped by V_{A→B}.



Proof. Apply Corollary 4.10 to the frame-A law, which is an admissible law on H_A because W^A is

unitary and the F^A_k form an instrument (Lemma 3.7). The relation between frames follows from

Theorem 5.12(a)–(b), applied from stage σ onward with initial states ψ^A_σ and ψ^B_σ ≐ V_{A→B}

ψ^A_σ. □



Corollary 5.14 connects CTGP’s generability and causal-inheritance commitments directly to the QRF

formalism. It is not merely that the operators transform covariantly: the very property that makes

the law generable from the present, and that makes the past causally idle beyond what the present

carries, holds in every frame and is preserved by every valid frame change.



5.4 Truth Preservation (Task T3)



Definition 5.15 (Truth in a frame description). A frame-A proposition is true in D^A_σ iff it

belongs to L^A_σ (Tiers 1 and 2 for earlier stages), or it is a present-stage Tier 2 proposition

about [ψ^A_σ] that holds, or it is a Tier 3 proposition whose projector Q^A satisfies Q^A ψ^A = ψ^A

at the relevant stage.



Theorem 5.16 (Truth preservation). Suppose D^A_σ and D^B_σ satisfy Criterion 5.5. Then for every

frame-A proposition p that is determinate in D^A_σ, τ_{A→B}(p) is determinate in D^B_σ and has the

same truth value. Moreover, under the generative law, truth preservation continues to hold at every

later stage of every realized history.



Proof. For members of L, (C3) gives p ∈ L^A iff τ_{A→B}(p) ∈ L^B. For present-stage Tier 2

propositions, (C2) gives [ψ^A] = [φ] iff [V_{A→B} ψ^A] = [V_{A→B} φ]. For Tier 3, Q^A ψ^A = ψ^A iff

(V Q^A V^{−1})(V ψ^A) = V ψ^A, and V Q^A V^{−1} = Q^B by Lemma 3.7. The final clause follows from

Theorem 5.12(c). □



Proposition 5.17 (No revision across frames). For σ < σ″ and any frame A, a past-tensed frame-A

proposition about a stage before σ is true in D^A_σ iff it is true in D^A_{σ″}. The same holds for

its translation into any other frame.



Proof. Admissible profiles are nested (Theorem 4.8), and τ_A is applied element-wise. Combine with

Theorem 5.16. □



Proposition 5.17 combines CTGP’s No Revision of the Past (Proposition 17.22) with frame covariance:

changing frames does not revise the past any more than the passage of stages does.



5.5 Ontological Identity, Physical Equivalence, and Observational Indistinguishability



If L is dynamically idle and corresponds to no present observable, how could anyone determine which

history occurred? The answer requires separating three relations that are easily run together.



Definition 5.18 (Three relations between histories). Fix the law. A complete finite history through

stage σ_n, h = (Ψ_{σ_0}, ω), consists of an initial state and an admissible event sequence of length

n, so that it specifies everything from the initial state through σ_n; write S(h) for its present

state and L(h) for its truth profile. For two complete finite histories h_1 and h_2 of the same

length:



    h_1 ∼_phys h_2 (same present physical state) iff S(h_1) = S(h_2);



    h_1 ∼_hist h_2 (same realized history) iff L(h_1) = L(h_2);



    h_1 ∼_obs h_2 relative to a class 𝒪 of observers and a tolerance ε (observationally

    indistinguishable) iff no procedure available to 𝒪 discriminates h_1 from h_2, given equal prior

    probabilities, with error probability below ε.



Proposition 5.19 (How the relations are ordered). Let 𝒪 be any class of observers whose evidence

consists of the outcomes of measurements on the present state.



    (i) ∼_hist implies ∼_phys, by accuracy (Proposition 4.11; for n ≥ 1).



    (ii) ∼_phys implies ∼_obs for every tolerance ε ≤ 1/2, because identical present states yield

    identical statistics for every measurement, so no procedure does better than guessing.



    (iii) ∼_phys does not imply ∼_hist (Propositions 4.12 and 4.13).



    (iv) More generally, if the present states of h_1 and h_2 have overlap |⟨Ψ(h_1), Ψ(h_2)⟩| = c,

    then with equal prior probabilities no measurement on the present state discriminates them with

    error probability below (1 − √(1 − c²)) / 2 (Helstrom 1976). Histories whose present states are

    close are therefore observationally nearly indistinguishable even when they are not physically

    equivalent.



Proof. (i)–(iii) are as stated. (iv) is the Helstrom bound for discriminating two pure states with

equal priors. □



The relations are thus nested in one direction and strictly separated in the other: same history

implies same present, which implies indistinguishability by present observation, and neither

converse holds. In the model with finite-width flashes, Proposition 4.12 shows that a given present

state can be reached along every event sequence from some initial state, so for present-state

observers every fact in L beyond what S encodes is structurally unknowable in the sense of More

Info, §4. The numerical search in §8.3 found two distinct histories whose present states have

overlap 0.985, for which the Helstrom bound gives a minimum error probability of 0.414: the

histories are nearly indistinguishable by any present measurement, though they are different

histories.



This is CTGP’s distinction between truth and recoverability (C-i), stated as a theorem about the

model. It also answers the objection that Criterion 5.5 is not operationally checkable when L is

inaccessible. The reply is that Criterion 5.5 is an exact criterion of ontological identity, not a

decision procedure. Agents in different frames check correspondence through records: present

physical structures that carry evidence about which events occurred. Agreement of records,

translated by τ_{A→B}, is evidence that (C3) holds; disagreement is evidence that it fails. Where

records are erased or never formed, the question has an answer that no one may be able to learn.

This limitation belongs to CTGP itself, not to the criterion: the boundary of knowledge is not the

boundary of fact (More Info, §4).



5.6 Where L Sits Relative to the Quantum State (Task T4)



The preceding results can be collected into a single statement.



Theorem 5.20 (Location of the Lucretian profile). In any model satisfying Definitions 4.1–4.7:



    (i) L is generated, not generating. L_σ is a function of the actual past history, which the

    mathematics represents as an initial segment of a sample path of the kernel K, realized only up

    to the present stage, and K takes only S_σ as input (Proposition 4.9, Corollary 4.10).



    (ii) L ranges over an exactly specified space. The admissible profiles are characterized by

    Theorem 4.8.



    (iii) L is not reducible to S. For invertible laws, every present ray is reachable along every

    finite event sequence from a suitably chosen initial ray, so the complete past is not a function

    of S (Proposition 4.12).



    (iv) L is accurate. Together with the law, L fixes S at every stage after the first (Proposition

    4.11), and Had(σ″, φ) ∈ L_σ iff φ was the case at σ″.



    (v) L is frame-covariant. Its frame-relative forms are related by the translations τ_{A→B}, and

    identity of history across frames is exactly agreement of L modulo translation (Proposition

    5.8).



    (vi) L carries no extra dynamical assumptions. No law refers to L, so including L in the

    complete ontology adds no variable that affects successor generation, and it does not require

    any past-tensed property to correspond to a measurable quantum observable.



Point (vi) answers the concern that including past-tensed properties in the complete ontology might

require treating them as additional variables that influence the dynamics, or might require every

ontologically real property to have an independently measurable observable. Neither follows. Tier 1

truths about which events occurred are not eigenvalues of any present observable: by Proposition

4.12, no present measurement can distinguish the complete histories that end in a given state. They

are nonetheless facts, and they are the facts that distinguish those histories.



Schematically, the order of determination at one transition is:



        S_σ  ──K──▶  k  ──▶  S_{σ′} = [F_k W Ψ_σ]   and   ΔL_{σ→σ′} = { Had(σ, S_σ), Had(σ→σ′, k) }.



The kernel produces the event. The event, together with the law, produces the next state and the

next past-tensed truths. Nothing flows from L back into K.



5.7 Why a Primitive Lucretian Profile Rather Than an Encoding of the Event History



A natural question remains. Why should the truth profile be regarded as a primitive ontological

feature of the present world, rather than as a formal encoding of the realized event history, as it

would be in an ordinary single-outcome flash ontology that simply associates historical propositions

with earlier events? The mathematics cannot answer this question, and it is important to see why.



Proposition 5.21 (Formal equivalence). For fixed law and initial state, the map ω ↦ L(ω) is a

bijection from ℋ_n onto ℒ_n, and it commutes with the frame translations τ_A.



Proof. Surjectivity holds by definition of ℒ_n, and injectivity by the uniqueness clause of Theorem

4.8. Commutation with τ_A holds because τ_A leaves stage indices and event labels unchanged and maps

states by R_A. □



Mathematically, then, the truth profile is interchangeable with the event history: every theorem of

this preprint could be restated with the realized sequence of events in place of L. The difference

between the two readings is not structural but concerns where the truthmakers for past-tense truths

are located, and that is fixed by the background ontology of time.



On an eternalist reading of the flash ontology, past flashes exist, located at earlier times, and

they are the truthmakers for propositions about them; nothing in the present need do that work. A

growing-block reading agrees that past flashes exist. CTGP denies both (C-a): past stages, and the

events that occurred in them, do not exist. CTGP also accepts a truthmaker principle for past-tense

truths: what is true about the past must be grounded in what exists, and on presentism only the

present exists (CTGP – explained, §5.2.1). Not every presentist accepts such a principle; some

reject unrestricted truthmaker requirements for past-tense truths altogether (Merricks 2007). The

argument that follows is therefore conditional: given CTGP’s truthmaker principle, something present

must make past-tense propositions true, and the options are limited.



    (i) Records. Past-tense truths might be grounded in present physical traces. Proposition 4.12

    rules this out within the model: the present physical state is reachable along every event

    sequence from a suitable initial state, so no function of the present physical state, and hence

    no record contained in it, fixes the complete past. Grounding past truths in records would leave

    many of them without truthmakers, and it would make the past revisable whenever records degrade,

    contrary to No Revision (C-b) and to the distinction between truth and recoverability (C-i).



    (ii) Abstract histories. Past-tense truths might be grounded in an abstract representation of

    history, such as an ersatz time series of maximal propositions (Bourne 2006; Crisp 2007). Such a

    representation is formally the event history again. It still requires a fact that selects which

    abstract history is the actual one, and on presentism that fact must be a fact about the
