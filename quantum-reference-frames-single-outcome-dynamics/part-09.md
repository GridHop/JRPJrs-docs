# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 09 of 35 (1,789 words)

with t_0 = 0 and t_{m+1} = ∞, so that the state is right-continuous at each jump.



Proposition 9.4 (Density of the record). The law of the record on [0, t] has density, with respect

to the reference measure,



        p_t(ω) = e^{−Λt} ‖J_{k_m} e^{−iH(t_m − t_{m−1})} ⋯ J_{k_1} e^{−iH t_1} Ψ_0‖².



The admissible records are the positive-density records, 𝒜_t = { ω ∈ Ω_t : p_t(ω) > 0 }.



Proof. The hit times of a Poisson process of rate Λ have density Λ^m e^{−Λt} on ordered m-tuples in

(0, t]. Given the hit times, the labels are drawn successively with probabilities ‖J_{k_j} φ_j‖² /

Λ, where φ_j is the normalized state just before t_j. The product of these probabilities times Λ^m

is Π_j ‖J_{k_j} φ_j‖². Because the evolution between hits is unitary, this product telescopes into

the squared norm of the unnormalized vector shown. □



Definition 9.5 (Continuous-time truth profile). The past-tensed language in continuous time consists

of state propositions Had(s, [Ψ]), read “at time s the state was [Ψ]”, and event propositions Had(s,

k), read “at time s event k occurred”. For ω ∈ 𝒜_t the truth profile at time t is



        L_t(ω) = { Had(s, [Ψ_s(ω)]) : 0 ≤ s < t } ∪ { Had(t_j, k_j) : 1 ≤ j ≤ m }.



An event at time t_m = t is counted as having occurred: it belongs to the generation of the present

state, which is right-continuous.



Remark 9.6 (Pointwise and almost-sure statements). Two kinds of statement about records must be kept

apart. Pointwise statements hold for every record in a specified set: Definitions 9.3 and 9.5 assign

a state path and a truth profile to every record, Theorem 9.7 characterizes the profiles of all

admissible records, and Propositions 9.8 and 9.9 and Theorem 9.10 hold for every admissible record.

Probabilistic statements hold almost surely, that is, outside a set of records of probability zero.

Because p_t is a density, an individual record has probability zero. Admissibility means positive

density, p_t(ω) > 0; it does not mean that ω has positive probability, and positivity of a density

is not in general the same as membership in the topological support of the law. Throughout,

“admissible” is used only in the positive-density sense. In the finite-width model every Kraus

operator is invertible, so every record has positive density. In particular, records with an event

exactly at the terminal time t form a set of probability zero: for a fixed t, the Poisson process

almost surely has no point at t. Such records are admitted so that the profile at time t is defined

for every record, with right-continuous states, and so that the profiles of a single trajectory are

nested at all times; no probabilistic statement depends on them. Since every result in this section

is proved pointwise for all admissible records, it holds in particular almost surely. The

conditional law in Proposition 9.9 is likewise given by an explicit density defined for every

record, which is a version of the conditional distribution; any other version agrees with it almost

surely.



Theorem 9.7 (Admissible continuous-time profiles). A set L of propositions belongs to { L_t(ω) : ω ∈

𝒜_t } if and only if: (o) every element of L is a state proposition Had(s, [Ψ]) with s ≥ 0 or an

event proposition Had(s, k) with s > 0; (a) the event propositions are finitely many, with distinct

times in (0, t]; (b) for each s ∈ [0, t) there is exactly one state proposition with time s, and

none with time s ≥ t; (c) the state proposition at time 0 is Had(0, [Ψ_0]); and (d) if ω is the

record read off from the event propositions, then p_t(ω) > 0 and, for every s ∈ [0, t), the state

proposition at time s is Had(s, [Ψ_s(ω)]). The record is then unique, and profiles are nested: if t

≤ t′, ω′ ∈ 𝒜_{t′}, and ω is the restriction of ω′ to [0, t] (its events with times at most t), then

ω ∈ 𝒜_t and L_t(ω) ⊆ L_{t′}(ω′).



Proof. As for Theorem 4.8. Conditions (o) and (a) determine a unique record ω; (d) states that ω is

admissible and that every state proposition is the one the law assigns along ω; (b) and (o) exclude

anything else. For nesting, the factorization in the proof of Proposition 9.9 gives p_{t′}(ω′) =

p_t(ω) · c with c ≥ 0, so p_{t′}(ω′) > 0 implies p_t(ω) > 0 and hence ω ∈ 𝒜_t. Restriction preserves

the event propositions with times up to t and the states at all times before t, so every element of

L_t(ω) belongs to L_{t′}(ω′); for t < t′ the later profile also contains the state proposition at

time t, which is why the inclusion can be strict. □



Proposition 9.8 (Reconstruction from an earlier time). For 0 ≤ s < t and ω ∈ 𝒜_t, the present state

S_t = [Ψ_t(ω)] is fixed by the state proposition Had(s, [Ψ_s(ω)]), the event propositions with times

in (s, t], and the law: it is obtained by applying to Ψ_s(ω) the unitary evolution between those

events and the corresponding jump operators.



Proof. Definition 9.3, applied from time s rather than time 0. □



Proposition 9.8 avoids any appeal to a “latest” earlier time, which does not exist in continuous

time: any earlier time s, together with the events since s, suffices.



Proposition 9.9 (Dynamical idleness in continuous time). For t < t′, the conditional law of the

record on (t, t′], given the complete state (S_t, L_t), depends only on S_t. Its density is e^{−Λ(t′

− t)} ‖J_{k_r} e^{−iH(t_r − t_{r−1})} ⋯ J_{k_{m+1}} e^{−iH(t_{m+1} − t)} Ψ_t‖², where (t_{m+1},

k_{m+1}), …, (t_r, k_r) are the events in (t, t′].



Proof. Write the unnormalized vector of Proposition 9.4 on [0, t′] as A B Ψ_0, where B carries Ψ_0

to the unnormalized state at time t and A carries the state from t to t′. Then ‖A B Ψ_0‖² = ‖A Ψ_t‖²

‖B Ψ_0‖² with Ψ_t = B Ψ_0 / ‖B Ψ_0‖, and e^{−Λt′} = e^{−Λt} e^{−Λ(t′ − t)}. The density on [0, t′]

therefore factorizes into the density on [0, t] and the stated factor, which depends on the past

only through Ψ_t. □



Theorem 9.10 (Continuous-time covariance, correspondence, and truth preservation). For a frame A,

let the frame-A description at time t be D^A_t = (t, [R_A Ψ_t], τ_A(L_t)), where τ_A maps Had(s,

[Ψ]) to Had(s, [R_A Ψ]) and Had(s, k) to Had(s, k, E^A_k). Then:



    (a) For every record ω, the densities computed in frame A, in frame B, and in the neutral

    description coincide, so the sets 𝒜_t of admissible records coincide in all frames.



    (b) Along every ω ∈ 𝒜_t, the frame states satisfy [R_B Ψ_s(ω)] = [V_{A→B} R_A Ψ_s(ω)] for all s

    ∈ [0, t].



    (c) Criterion 5.5, with stage replaced by time, Theorem 5.6, and Proposition 5.8 hold for

    continuous-time descriptions, and if the descriptions of two frames correspond at time 0, the

    descriptions generated from them correspond at every later time along every admissible record.



    (d) Truth preservation (Theorem 5.16) and no revision across frames (Proposition 5.17) hold at

    every time.



Proof. (a) By Lemma 3.7, R_A J_k = J^A_k R_A and R_A e^{−iHs} = e^{−iH^A s} R_A on H_phys. Hence the

frame-A unnormalized vector of Proposition 9.4, applied to R_A Ψ_0, equals R_A applied to the

neutral one, and its norm is the same because R_A is unitary; likewise for frame B. (b) The same

identities show that the frame-A state at time s is proportional to R_A Ψ_s(ω), and R_B = V_{A→B}

R_A on H_phys. (c) The proofs of Theorem 5.6 and Proposition 5.8 use only the unitarity of the

reductions and the bijectivity of the translations, both of which hold here; preservation of

correspondence follows from (a) and (b), because both frames add, at each time, the translations of

the same neutral propositions. (d) The proofs of Theorem 5.16 and Proposition 5.17 carry over

verbatim, using (c) and the nesting in Theorem 9.7. □



The numerical check (Table 1) simulated 200 trajectories over total time T = 5 in frames A and B

with common random numbers: the 1,158 events, and their times, were identical in the two frames, and

the final states were related by V_{A→B} to machine precision.



The resulting picture matches CTGP’s description of generation: continuous evolution of the present

state, punctuated by discrete primitive events, with each moment’s state and each event passing into

the past-tensed profile.



9.4 What Is Postulated: The Identification of t With Cosmic Time



The continuous parameter t in Definition 9.1 is the time variable of a non-relativistic dynamics.

Identifying it with CTGP’s generation parameter σ, which in the emergent geometric regime is the

cosmological time function (CTGP – explained, §6), is a postulate of the application, not a result.

Nothing in the model derives cosmic time. What the model shows is conditional: if the generation

parameter is a global time with respect to which the present state evolves by a law of this form,

then the continuous-time model has every property established in Part II and §9.3. Deriving the

identification would require at least a relativistic version of the dynamics and an account of how

its time parameter is fixed by the cosmological matter distribution; these are the subjects of §13

and §14, and they remain open (§17.3, O2 and O3). The regularity of cosmological time that the

identification requires is stated precisely in §13.1: the level sets are future Cauchy surfaces in

general, and Cauchy surfaces under the condition of Proposition 13.1.



9.5 The Discrete Stages as a Coarse-Grained Description



The discrete-stage model of Part II is a coarse-grained description of the continuous one. With

stage duration τ and λ = 1 − e^{−Λτ}, the probability of at least one hit in a stage is the same in

both models. The discrete model differs in two respects: it allows at most one event per stage, and

it places each event at the end of its stage. The probability of two or more hits in one stage is of

order (Λτ)², so the discrete model approximates the continuous one when Λτ is small. The discrete

stages are therefore not a claim that generation proceeds in jumps; they are a sampling of a

continuous process, used in Part II because finite induction makes every proof exact.



----------------------------------------------------------------------------------------------------

10. CTGP’s Further Requirements (Task T5)

----------------------------------------------------------------------------------------------------



Cross-frame consistency is not the whole of CTGP’s demands. A QRF-compatible single-outcome model

must also satisfy definite generative ordering and generability. This section checks these and

related requirements.



10.1 Definite Generative Ordering



Proposition 10.1 (Frame changes act within stages and commute with generation). For every admissible
