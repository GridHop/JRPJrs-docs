# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 06 of 40 (1,664 words)

5.2 Cross-Frame Identification (Task T2)



Definition 5.3 (Frame description). A frame-A description at stage σ is a triple D^A_σ = (σ, ψ^A_σ,

L^A_σ), where ψ^A_σ is a ray in H_A and L^A_σ is a set of frame-A past-tensed propositions of the

forms Had(σ″, [φ]) with φ ∈ H_A and Had(σ″ → σ‴, k, E^A_k), where E^A_k = (F^A_k)† F^A_k is the

frame-A form of the effect of event k.



Definition 5.4 (Translations). The frame-A translation τ_A maps neutral propositions to frame-A

propositions:



        τ_A Had(σ″, [Ψ]) = Had(σ″, [R_A Ψ]),     τ_A Had(σ″ → σ‴, k) = Had(σ″ → σ‴, k, E^A_k).



Because R_A is unitary and E^A_k is determined by k, τ_A is a bijection. The frame-change

translation is τ_{A→B} = τ_B ∘ τ_A^{−1}; it replaces each state [φ] by [V_{A→B} φ] and each effect

E^A_k by V_{A→B} E^A_k V_{A→B}^{−1} = E^B_k, keeping the stage indices and the event label.



Criterion 5.5 (Cross-frame identification). Frame descriptions D^A_σ and D^B_τ describe the same

present world, with the same realized history, iff



    (C1) Same stage: σ = τ.



    (C2) State correspondence: ψ^B ≐ V_{A→B} ψ^A.



    (C3) History correspondence: L^B = τ_{A→B}(L^A).



Theorem 5.6 (Common perspective-neutral pre-image). D^A_σ and D^B_σ satisfy (C1)–(C3) iff there is a

single neutral complete state Ω_σ = (S_σ, L_σ) with ψ^A ≐ R_A Ψ_σ, ψ^B ≐ R_B Ψ_σ, L^A = τ_A(L_σ),

and L^B = τ_B(L_σ).



Proof. (⇐) Given Ω_σ, ψ^B ≐ R_B Ψ_σ = R_B R_A^{−1} R_A Ψ_σ ≐ V_{A→B} ψ^A, which is (C2), and L^B =

τ_B(L_σ) = τ_B τ_A^{−1} τ_A(L_σ) = τ_{A→B}(L^A), which is (C3). (⇒) Given (C1)–(C3), define Ψ_σ =

R_A^{−1} ψ^A and L_σ = τ_A^{−1}(L^A). Then R_A Ψ_σ = ψ^A by construction, R_B Ψ_σ = V_{A→B} ψ^A ≐

ψ^B by (C2), τ_A(L_σ) = L^A, and τ_B(L_σ) = τ_{A→B}(L^A) = L^B by (C3). □



The content of Theorem 5.6 is clearest when stated in terms of orbits.



Definition 5.7 (Description orbit). Let 𝔉 be the set of admissible frames. For a complete state Ω_σ

= (S_σ, L_σ), its description orbit is



        𝒟(Ω_σ) = { (σ, [R_A Ψ_σ], τ_A(L_σ)) : A ∈ 𝔉 }.



Proposition 5.8 (Orbit identification). (i) Two frame descriptions satisfy Criterion 5.5 iff they

belong to the same description orbit. (ii) Distinct complete states have disjoint orbits, so the

orbits partition the set of frame descriptions. (iii) Consequently, satisfying Criterion 5.5 is an

equivalence relation. (iv) If Ω_σ is admissible (Ω_σ ∈ 𝔒_n), every member of its orbit describes

that admissible complete state.



Proof. (i) is Theorem 5.6 restated in terms of orbits. (ii) Each frame description belongs to the

description space of exactly one frame A. If two complete states Ω and Ω* share an orbit member,

that member is (σ, [R_A Ψ], τ_A(L)) = (σ, [R_A Ψ*], τ_A(L*)) for a single frame A, and injectivity

of R_A and τ_A gives [Ψ] = [Ψ*] and L = L*. (iii) follows from (i) and (ii). (iv) holds by

definition of the orbit. □



Proposition 5.9 ((C3) is not redundant). There exist frame descriptions satisfying (C1) and (C2) but

not (C3); they describe different realized histories with the same present state. More precisely:



    (a) For complete histories, in which the initial condition counts as part of the past, such

    pairs exist for every invertible law.



    (b) Within a single space ℋ_n with a fixed initial state, such pairs exist in the special regime

    of Proposition 4.13. Whether they exist for generic finite-width parameters is open (§8.3).



Proof. (a) By Proposition 4.12, for any present ray [Φ] and two distinct event sequences there are

initial rays from which each sequence ends at [Φ]. The two complete histories have different truth

profiles, since their transition propositions differ. Take the frame-A description of one and the

frame-B description of the other: (C1) and (C2) hold, and (C3) fails. (b) The same argument applies

to the two histories of Proposition 4.13 (Proposition 8.1), which share an initial state. □



Case (a) compares descriptions drawn from admissible spaces with different initial conditions. Under

presentism the initial condition is a past fact like any other, so this is the comparison relevant

to CTGP; case (b) shows that the phenomenon also occurs, in a special regime, with the initial

condition held fixed.



Three levels of identity can now be distinguished, and the point at which interpretation enters can

be located exactly.



    Representational equivalence. Two descriptions are related by a valid QRF transformation: (C1)

    and (C2) hold, so the two quantum states are reductions of one perspective-neutral state. This

    is a mathematical relation between representations.



    Dynamical equivalence. The two frames’ laws are related by the frame-change unitary (Definition

    5.11), so their probability laws and event records transform consistently (Theorem 5.12). This

    is a mathematical relation between laws.



    Ontological identity. The two descriptions concern one realized present and one realized

    history. Within the model, this is membership in one description orbit (Proposition 5.8).



The first two levels are theorems. The step from orbit membership to ontological identity is not a

theorem of quantum mechanics. It is the following interpretive thesis, which is what CTGP adds.



Thesis 5.10 (Orbit realism). Each description orbit of an admissible complete state represents

exactly one realized present together with exactly one realized history. Frame descriptions in one

orbit are descriptions of the same world; descriptions in different orbits are descriptions of

different possible worlds, at most one of which is actual.



Thesis 5.10 gives the precise answer to the question how one can establish that two descriptions

refer to the same realized history rather than assuming it. Four observations make up the answer.



First, given the thesis, identity of history is not an extra posit laid over frame descriptions; it

is a definite condition, (C3), that can fail. Second, it cannot be settled by the quantum state

alone: Proposition 5.9 shows that state correspondence is compatible with different histories, so

identity of history is carried by L, which is a direct argument for including the Lucretian profile

in the complete ontology. Third, correspondence is preserved by the dynamics (Theorem 5.12(c)), so

frames cannot drift into describing different histories, and correspondence is not maintained by

stipulation at each stage. Fourth, whether two descriptions do in fact correspond is an ontological

question, and whether anyone can verify that they do is an epistemic question; §5.5 shows that these

come apart and that Criterion 5.5 is an exact criterion of identity, not in general an

experimentally decidable one.



5.3 Valid Transformations of the Law



Definition 5.11 (Frame-relative laws describing one world). Frame-relative laws (W^A, {F^A_k}) on

H_A and (W^B, {F^B_k}) on H_B describe one world iff W^B = V_{A→B} W^A V_{A→B}^{−1} and F^B_k =

V_{A→B} F^A_k V_{A→B}^{−1} for every k. Equivalently, by Remark 3.8, both are frame forms of one

admissible neutral law.



Theorem 5.12 (Covariance of generation). Let (W, {F_k}) be an admissible neutral law, with frame

forms (W^A, {F^A_k}) and (W^B, {F^B_k}). Let Ψ_{σ_0} ∈ H_phys, ψ^A_{σ_0} = R_A Ψ_{σ_0}, and

ψ^B_{σ_0} = R_B Ψ_{σ_0}. Then:



    (a) For every finite sequence ω = (k_1, …, k_n), the probability of ω is the same whether

    computed in frame A, in frame B, or in the neutral description.



    (b) Along every history ω of nonzero probability, the frame-evolved states satisfy ψ^B_{σ_j} ≐

    V_{A→B} ψ^A_{σ_j} for j = 0, …, n.



    (c) Consequently the probability measure over histories is frame-independent, the sets ℋ_n of

    admissible histories coincide in all frames, and if D^A_{σ_0} and D^B_{σ_0} correspond, then for

    every realized history the descriptions D^A_{σ_n} and D^B_{σ_n} generated from them correspond.



Proof. By induction on n. Suppose ψ^A_{σ_j} ≐ R_A Ψ_{σ_j} and ψ^B_{σ_j} ≐ R_B Ψ_{σ_j}. By Lemma 3.7,

Pr^A(k) = ‖F^A_k W^A R_A Ψ_{σ_j}‖² = ‖R_A F_k W Ψ_{σ_j}‖² = ‖F_k W Ψ_{σ_j}‖², and likewise for frame

B. The updated frame states are R_A Ψ_{σ_{j+1}} and R_B Ψ_{σ_{j+1}} after normalization, which gives

(b). The probability of a sequence is the product of conditional probabilities, which gives (a) and

the equality of the sets ℋ_n. For (c), the truth-profile updates in the two frames add τ_A(ΔL) and

τ_B(ΔL) for the same neutral ΔL, so (C3) is preserved; (C1) is preserved because both frames advance

the same stage index; and (C2) is (b). □



Corollary 5.13 (Failure of same-form laws). If frame B adopts a law with the same matrices as frame

A’s law but written in B’s coordinates, that is, W^B = W^A and F^B_k = F^A_k as matrices, then in

general the two frames assign different probabilities to the same histories and do not describe one

world.



Proof. Such a pair satisfies Definition 5.11 only if W^A and every F^A_k commute with V_{A→B}, which

fails in general. Section 8 gives an instance with total-variation distance 0.180 between the two

measures over histories. □



Corollary 5.13 shows what “valid transformation” excludes: it is not enough for each frame to use a

law that looks natural from its own point of view; the laws must be related by the frame-change

unitary. This is the QRF analogue of requiring that a law be written in covariant form.



Corollary 5.14 (Covariant generability). In every frame A, the future is conditionally independent

of the past given the present:



        Pr^A(𝔉⁺_σ | ψ^A_σ, L^A_σ) = Pr^A(𝔉⁺_σ | ψ^A_σ),



and this conditional distribution is the image under the frame change of the corresponding

distribution in any other frame B, with event labels unchanged and states mapped by V_{A→B}.



Proof. Apply Corollary 4.10 to the frame-A law, which is an admissible law on H_A because W^A is

unitary and the F^A_k form an instrument (Lemma 3.7). The relation between frames follows from

Theorem 5.12(a)–(b), applied from stage σ onward with initial states ψ^A_σ and ψ^B_σ ≐ V_{A→B}

ψ^A_σ. □



Corollary 5.14 connects CTGP’s generability and causal-inheritance commitments directly to the QRF

formalism. It is not merely that the operators transform covariantly: the very property that makes

the law generable from the present, and that makes the past causally idle beyond what the present

carries, holds in every frame and is preserved by every valid frame change.


