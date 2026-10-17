# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 11 of 40 (1,150 words)

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

law, every pair of frames, and every event k, the frame-A and frame-B single-step maps G^A_k(ψ) =

F^A_k W^A ψ / ‖F^A_k W^A ψ‖ and G^B_k satisfy V_{A→B} ∘ G^A_k ≐ G^B_k ∘ V_{A→B}. The stage index is

unchanged by every frame change. The same holds in continuous time, with hit times unchanged.



Proof. Lemma 3.7, Definition 3.4, and Proposition 9.2(iv). Frame changes are maps H_A → H_B at a

fixed stage or time, and the stage or time index is a parameter of the law, not a quantum degree of

freedom. □



The linear order of stages, and the order of events within a history, are therefore the same in

every frame: event k_j precedes k_{j+1} in every description, and no frame change in this class

superposes the order of events. This satisfies (C-e) for spatial QRFs. The status of this result

should be stated plainly. The ordering is preserved because the stage or time index is a parameter

on which frame changes do not act. That is an assumption of the class of models, not a derivation of

definite order from more basic principles. Whether a definite order can be maintained when the

reference frame is itself a quantum clock is the principal open problem (§14; §17.3, O3).



10.2 Generability



The kernel of Definition 4.2, and the jump process of Definition 9.1, give the distribution of the

next state and event from the present state alone. They use no data from later stages, no final-

state condition, and no global self-consistency condition, so the model is generable in exactly the

sense of (C-f). The state space on which the law acts is H_phys, the physically instantiated present

state. The truth profile is not added to it (Proposition 4.9), so generability’s restriction on

enlarging the state space is respected. By Corollary 5.14, the generability property holds in every

frame. The model is stochastic, which CTGP – explained, §12.2, explicitly allows.



10.3 Open Future and Asymmetry



At stage σ, L_σ contains no proposition about a later stage (Theorem 4.8(e)), and no proposition

about a later stage is determinate (Definition 5.1). Before a transition there are only kernel

probabilities over possible events; after it there is one realized event and its Had-property. This

matches clause (d) of CTGP’s Definition 17.20 and the claim that the future is ungenerated rather

than merely unknown.



10.4 No Relative Facts



Every determinate proposition has the same truth value in every frame (Proposition 5.2 and Theorem

5.16), so the model contains no frame-relative facts. It contains frame-relative descriptions and

relational quantities, which CTGP does not reject (§2.3).



====================================================================================================

PART IV. Evaluation

====================================================================================================



----------------------------------------------------------------------------------------------------

11. What CTGP Adds Beyond QRF Covariance

----------------------------------------------------------------------------------------------------



A skeptic can grant every theorem above and still ask whether CTGP contributes any substantive

constraint beyond the existence of a QRF-covariant, single-outcome stochastic model with an attached

historical truth profile. It does. The test of whether a commitment adds content is whether it

excludes some model that satisfies everything else. Each of the following commitments passes that

test.



CTGP commitment          | Formal content in this framework        | Excludes

-------------------------+-----------------------------------------+-------------------------------

Generability (C-f)       | The law is a Markov kernel on present   | Laws depending on past facts

                         | physical states; Cor. 4.10, Cor. 5.14   | not carried by the present

                         |                                         | state (Example 11.3)

Single-outcome (C-d)     | Exactly one event per transition;       | Everettian readings on which

                         | Theorem 4.8(a)                          | all branches are realized

Frame-invariant          | Determinacy and truth invariant under   | Relational interpretations with

determinacy (C-d)        | all frame changes; Prop. 5.2, Thm 5.16  | frame-relative facts

No revision (C-b)        | Admissible profiles are nested;         | Readings on which later events

                         | Theorem 4.8; Prop. 5.17                 | fix earlier facts

Definite ordering (C-e)  | Events totally ordered, order invariant | Fundamental indefinite causal

                         | under frame changes; Prop. 10.1         | order at the level of stages

Lucretian accuracy (C-b) | Profiles are admissible and accurate;   | Truth profiles inconsistent

                         | Theorem 4.8, Prop. 4.11                 | with the law



Table 2. Constraints CTGP imposes and what each excludes, even among QRF-covariant models.



Generability needs the most care, because a law that looks future-dependent may have an equivalent

forward formulation. CTGP – explained, §12.2, builds this into its criterion: future dependence

counts against generability only if no empirically equivalent generable formulation exists. Three

cases must therefore be distinguished: conditioning on the future as a mathematical operation, a

final-boundary requirement imposed as a fundamental input, and genuine non-generability relative to

the admissible present physical states. The first two are treated by Proposition 11.1 and Example

11.2, the third by Example 11.3.



Proposition 11.1 (Future conditioning has a forward representation). Let E be an event label and n ≥
