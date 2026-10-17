# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 09 of 40 (1,690 words)

8.1 Generative Law and Single Outcome



With the law of §7, one stage-to-stage transition samples exactly one event k ∈ 𝒦 with probability

‖F_k W Ψ_σ‖² and updates the state. The realized history is a single sequence of events. Unrealized

sequences are not facts: they have kernel probabilities before the transition and no Had-properties

afterward. This is single-outcome realism (C-d) at the level of the primitive ontology. Macroscopic

outcomes would be patterns of many flashes, as in Bell’s flash ontology; in a three-particle model,

each flash is already an event.



8.2 Weak Non-Supervenience in the Sharp Regime



Proposition 8.1 (Two histories, one present). Take the sharp limit s → 0 and set J = 0, so that W =

exp(−iτ Σ v(r) P_{ij}(r)) is diagonal in the configuration basis and commutes with every P_{ij}(r).

Let N ≥ 4, and let Ψ_{σ_0} be any state with nonzero amplitude on the configuration b−a = 1, c−a =

3. The histories



        ω = ((A,B,1), (A,C,3))     and     ω* = ((A,C,3), (A,B,1))



both have nonzero probability, and both produce the present state Ψ_{σ_2} ≐ R_A^{−1}|1, 3⟩. The

resulting truth profiles differ: L contains Had(σ_0 → σ_1, (A,B,1)) under ω and Had(σ_0 → σ_1,

(A,C,3)) under ω*.



Proof. In frame-A coordinates the two relevant flash operators are multiples of the projectors

P_{AB}(1) → |x = 1⟩⟨x = 1| and P_{AC}(3) → |y = 3⟩⟨y = 3|. These commute, and their product is the

rank-one projector



        P_{AB}(1) P_{AC}(3) = P_{AC}(3) P_{AB}(1) = |1, 3⟩⟨1, 3|.



With J = 0, W = exp(−iτ Σ v(r) P_{ij}(r)) is diagonal in the configuration basis, W |x, y⟩ =

e^{iθ(x,y)} |x, y⟩, so it commutes with both projectors. Along ω the unnormalized final vector is

therefore (λ/3) P_{AC}(3) W P_{AB}(1) W ψ_0 = (λ/3) P_{AC}(3) P_{AB}(1) W² ψ_0 = (λ/3) e^{2iθ(1,3)}

⟨1, 3|ψ_0⟩ |1, 3⟩. Along ω* the projectors are applied in the opposite order, which by the identity

above gives the same vector. Since ⟨1, 3|ψ_0⟩ ≠ 0, both histories have nonzero probability, and both

final states are the ray [|1, 3⟩], that is, [R_A^{−1}|1, 3⟩] in the neutral description. □



In this regime, the sharp flash (A,B,1) also makes the Tier 3 proposition “B is at separation 1 from

A just after σ_1” determinately true, illustrating the special case noted after Proposition 4.4.



8.3 Generic Parameters



For finite width, the situation divides as follows.



    (i) Strong non-supervenience holds for all parameters with s > 0 and λ < 1, by Proposition 4.12.

    The numerical check (Appendix B, item 11) takes a random present state and two different three-

    stage histories, reconstructs the unique initial state for each, and confirms that both

    histories end in the given present state with nonzero probability.



    (ii) Weak non-supervenience at generic parameters is open. Among all 4,096 three-stage histories

    from one random initial state at the generic parameter values of §8.4, no two distinct histories

    end in exactly the same present ray. This is evidence that fixed-initial-state coincidences are

    non-generic, not a proof.



    (iii) Near-coincidences occur. The largest overlap between the present states of two distinct

    histories in that sample is 0.985, so by Proposition 5.19(iv) no measurement on the present

    state distinguishes them with error probability below 0.414. Distinct histories can thus be

    observationally nearly indistinguishable even when their present states are not equal.



8.4 Numerical Verification



The claims above were checked numerically with N = 5, λ = 0.6, s = 0.8, J = 0.7, g = 0.9, and τ =

0.5 (and, for the continuous-time model of §9, hit rate Λ = 1.2 and total time T = 5), using a

random initial frame-A state; the checks of Theorem 13.4, Proposition 13.2, and Proposition 14.2 use

the separate settings stated in Appendix B. The checks of §§13.8–13.11 and §14.5 are reported

separately, in Table C.1 of Appendix C. The numerical checks confirm the analytical results in a

specific instance and guard against sign and ordering errors; they are not independent proofs.

Agreement “to machine precision” means deviations of order 10⁻¹⁶, the rounding error of double-

precision arithmetic. The script, its output, the software versions, and the random seeds are in

Appendix B.



Check                                          | Status      | Result

-----------------------------------------------+-------------+--------------------------------------

R_A, R_B, R_C unitary onto frame spaces        | Prop. 3.3   | Confirmed (machine precision)

V_{A→B} equals |x,y⟩ ↦ |−x, y−x⟩               | §6.2        | Confirmed

Groupoid law V_{B→C} V_{A→B} = V_{A→C}         | Prop. 3.5   | Confirmed

Instrument complete; W and all F_k invariant   | §7.1–7.2    | Confirmed

V F^A_k V^{−1} = F^B_k and V W^A V^{−1} = W^B  | Lemma 3.7   | Confirmed for all 16 events

Measures over 3 stages (16³ = 4096 histories)  | Thm 5.12(a) | max |p_A − p_B| = 2.8 × 10⁻¹⁷

Frame A vs neutral description                 | Thm 5.12(a) | max |p_A − p_neutral| = 1.4 × 10⁻¹⁷

States along every history                     | Thm 5.12(b) | max (1 − |⟨Vψ^A, ψ^B⟩|) = 6.7 × 10⁻¹⁶

Same-form law in frame B                       | Cor. 5.13   | Total-variation distance 0.180

Two histories, one present (sharp, J = 0)      | Prop. 8.1   | Same present ray; different L

Product state (frame A) → entangled (frame B)  | §6.3        | 0 bits → 1.000 bit

Absolute collapse leakage                      | §7.4        | 0.894 = √(1 − 1/5)

Continuous time: 200 trajectories, 1158 events | Prop. 9.2   | Identical event records in A, B

Continuous time: final states                  | Prop. 9.2   | max (1 − |⟨Vψ^A, ψ^B⟩|) = 6.7 × 10⁻¹⁶

Generic parameters: exact coincidences         | §8.3(ii)    | None among 4096 histories

Generic parameters: largest overlap            | §8.3(iii)   | 0.985; Helstrom error ≥ 0.414

Every history reaches a given present          | Prop. 4.12  | Confirmed for two 3-stage histories

History-dependent law, across initial states   | Prop. 11.4a | Same present ray; TV = 0.1000

History-dependent law, fixed initial state     | Prop. 11.4b | Same present ray; TV = 0.1000

Doob kernel vs future-conditioned measure      | Prop. 11.1  | max diff = 8.3 × 10⁻¹⁷

Foliation independence, causally local         | Thm 13.4(a) | All 136 foliations agree (7 × 10⁻¹⁸)

No dependence outside the predecessor set      | Thm 13.4(c) | max marginal change 8 × 10⁻¹⁶

Order-ideal law vs marginal of full law        | Prop. 13.7  | max diff 1.1 × 10⁻¹⁶

Gapless detectors, three-region test           | Thm 13.9    | No shift (< 10⁻¹⁵); formula (c) met

Unsharp Lüders instrument at C                 | Ex. 13.10   | Shifts −0.0215 and −0.0466

Gaussian field collapse at C                   | Cor. 13.14  | No shift (< 10⁻¹³); formula met

Non-commuting “spacelike” pair                 | §13.4       | Orders differ: TV = 0.165

Same channel, different history measures       | Prop. 13.2  | Mutual information 0 vs 1 bit

Drifting quantum clock, recorded readings      | Prop. 14.2  | P(backward) = 0.104 (exact, ring)



Table 1. Numerical checks of the concrete model (N = 5). The “Status” column names the analytical

result that each check instantiates.



----------------------------------------------------------------------------------------------------

9. Continuous-Time Embedding and the Status of Generative Stages

----------------------------------------------------------------------------------------------------



9.1 The Question



CTGP describes generation as a continuous causal-temporal progression (C-h). Part II uses discrete

stages σ_0 < σ_1 < … with one stochastic transition per stage. A discrete-stage model can represent

selected stages of a continuous process, but it does not by itself establish compatibility with a

continuous generative ontology. This section gives a continuous-time version of the model, proves

that it has the properties of Part II, and states precisely what remains a postulate.



9.2 A Relational Jump Process



Definition 9.1 (Continuous-time relational flash process). Let H be the invariant Hamiltonian of

§7.1, let Λ > 0 be a hit rate, and define jump operators



        J_{(i,j,d)} = √(Λ/3) · Σ_r √(w(r−d)) P_{ij}(r),     so that     Σ_k J_k† J_k = Λ · 1.



The process runs as follows. Hit times t_1 < t_2 < … form a Poisson process of rate Λ. Between hits

the state evolves by exp(−iH(t − t_j)). At a hit time, event k is drawn with probability ‖J_k ψ‖² /

Λ, and the state jumps to J_k ψ / ‖J_k ψ‖.



This is the standard quantum-jump unravelling of a Lindblad equation. Because Σ_k J_k† J_k is

proportional to the identity, the effective non-Hermitian Hamiltonian H_eff = H − (i/2) Σ_k J_k† J_k

= H − (iΛ/2) · 1 differs from H by a constant, so the evolution between hits is unitary up to a

uniform decay of norm, and the hit times are independent of the state. This is precisely the

structure of the original GRW model, here with relational jump operators.



Proposition 9.2 (Well-definedness, invariance, and covariance). (i) The process of Definition 9.1 is

a well-defined piecewise-deterministic Markov process on the unit sphere of H_phys, with almost

surely finitely many hits in any bounded time interval. (ii) Every trajectory remains in H_phys.

(iii) Its ensemble average ρ(t) obeys the Lindblad equation



        dρ/dt = −i [H, ρ] + Σ_k J_k ρ J_k† − Λ ρ,



which preserves the set of density operators supported on H_phys. (iv) The frame-A and frame-B

processes, built from the frame forms H^A, J^A_k and H^B, J^B_k, assign the same probabilities to

every finite sequence of (hit time, event) pairs, and along every trajectory their states satisfy

ψ^B(t) ≐ V_{A→B} ψ^A(t) for all t.



Proof. (i) In finite dimension, with bounded H and state-independent Poisson hit times, the

construction is explicit: a Poisson process of finite rate has almost surely finitely many points in

any bounded interval, and between them the evolution is a fixed unitary flow. (ii) H and every J_k

are invariant, so exp(−iHt) and the normalized jumps map H_phys to itself. (iii) The Lindblad form

follows from averaging the jump process, which is standard; the term −Λρ is −(1/2){Σ_k J_k† J_k, ρ}

with Σ_k J_k† J_k = Λ · 1. Invariance of H and J_k implies that the generator commutes with

conjugation by U_h, so density operators supported on H_phys remain so. (iv) By Lemma 3.7, ‖J^A_k

exp(−iH^A t) R_A Ψ‖ = ‖J_k exp(−iHt) Ψ‖ and likewise for frame B; hit times do not depend on the

state; so the joint law of (hit time, event) sequences is the same in every frame, and induction

over hits gives the state relation, as in Theorem 5.12. □


