# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 08 of 40 (1,698 words)

    1 and Tier 2 truth without positing existing past events, at the acknowledged cost that these

    properties do not supervene on the present’s categorical physical state (C-c; Sider 2001).



The independent work done by the Lucretian profile is therefore ontological, not mathematical. Given

presentism together with CTGP’s truthmaker principle, the profile is what makes the truths about

realized events true: what the eternalist locates in existing past flashes, the presentist locates

in the present world’s past-tensed properties. Proposition 5.21 is what one should expect: the

profile carries the same structure as the history it grounds, located in the present rather than

spread across existing times. Within the formalism the profile does two further jobs that any

adequate ontology must assign to something: it settles identity of history across frames when the

present state does not (Proposition 5.9), and it does so without acting dynamically (Theorem 5.20).



The disagreement with eternalism should be stated precisely. Eternalism is not the claim that past,

present, and future times exist simultaneously, which would identify distinct times with one time.

In its standard sense, it holds that entities and events located at different times exist

tenselessly, each at its own time, and their equal ontological status does not make those times

simultaneous. CTGP’s disagreement with eternalism is therefore not that eternalism collapses

different times into one. It is that CTGP denies that past and future stages exist alongside the

present stage in the unrestricted sense that eternalism accepts. Past events are determinate but no

longer exist as stages, future events do not yet exist, the past is grounded in present Lucretian

properties, and the future becomes actual only through generation. This ontological question is

distinct from the questions of objective passage, of A-theoretic versus B-theoretic accounts of

tense, and of how objects persist through time.



Whether CTGP’s presentist reading is preferable to an eternalist flash ontology is not settled by

the model. The two readings are empirically equivalent, as CTGP itself emphasizes (CTGP – explained,

§12.1). The choice rests on CTGP’s independent arguments: explanatory economy, the phenomenological

constraint, and the generability commitment that presentism makes and eternalism does not (CTGP –

explained, §§3, 4.5, and 12.2). What the present construction shows is that the presentist reading

is consistent, precisely specified, and costs nothing empirically.



====================================================================================================

PART III. A Concrete Single-Outcome Model

====================================================================================================



----------------------------------------------------------------------------------------------------

6. Three Particles on a Ring: Kinematics

----------------------------------------------------------------------------------------------------



6.1 The Model



Take G = ℤ_N, the integers modulo N, written additively, and three particles A, B, C, each located

at one of the sites 0, 1, …, N−1 of a ring. Then H_kin = ℓ²(ℤ_N)^{⊗3}, with basis |a, b, c⟩, and the

global translation is



        U_g |a, b, c⟩ = |a+g, b+g, c+g⟩.



H_phys is the N²-dimensional subspace of translation-invariant states. With no external origin, only

the separations b−a, c−a, and c−b are physical.



6.2 Frames and Frame Changes



Frame A uses the coordinates (x, y) = (b−a, c−a), the positions of B and C relative to A. Frame B

uses (u, v) = (a−b, c−b), and frame C uses (p, q) = (a−c, b−c). The reductions are



        (R_A Ψ)(x, y) = √N Ψ(0, x, y),    (R_B Ψ)(u, v) = √N Ψ(u, 0, v),

        (R_C Ψ)(p, q) = √N Ψ(p, q, 0).



By Proposition 3.3 they are unitary. The frame changes are permutations of basis states:



        V_{A→B} |x, y⟩ = |−x, y−x⟩,    V_{B→C} |u, v⟩ = |u−v, −v⟩,    V_{A→C} |x, y⟩ = |−y, x−y⟩.



The groupoid law can be checked directly: V_{B→C} V_{A→B} |x, y⟩ = V_{B→C} |−x, y−x⟩ = |−x−(y−x),

−(y−x)⟩ = |−y, x−y⟩ = V_{A→C} |x, y⟩.



6.3 A Worked Example of Frame-Relative Form



Let the frame-A description be



        ψ^A = (|1, 0⟩ + |2, 0⟩) / √2.



Relative to A, particle C is definitely at separation 0, and B is in an equal superposition of

separations 1 and 2. The state is a product state of B and C relative to A, with zero entanglement.

Applying V_{A→B} gives



        ψ^B = (|−1, −1⟩ + |−2, −2⟩) / √2,



so relative to B, particles A and C are each in a superposition and are perfectly correlated, with

one bit of entanglement.



Consider the Tier 3 proposition “C is at separation 0 from A”, with invariant projector Q onto c−a =

0. In frame A its form is Q^A = projector onto y = 0, and Q^A ψ^A = ψ^A, so the proposition is

determinately true. In frame B its form is Q^B = projector onto v−u = 0, a statement about the

correlation of two frame-B coordinates rather than about a single coordinate, and Q^B ψ^B = ψ^B, so

it is determinately true there as well. By contrast, “B is at separation 1 from A” has no

determinate value in frame A, because x is superposed, and its frame-B form, “A is at separation −1

from B”, has no determinate value in frame B either. Determinacy and truth agree across frames, as

Proposition 5.2 requires, even though one frame represents the situation as a product state and the

other as an entangled state.



----------------------------------------------------------------------------------------------------

7. Dynamics: Relational Flashes

----------------------------------------------------------------------------------------------------



7.1 Deterministic Part



Let S_A, S_B, S_C shift the respective particle by one site, and let P_{ij}(r) be the projector onto

configurations with x_j − x_i = r (mod N) for each ordered pair (i, j) ∈ {(A,B), (A,C), (B,C)}.

Define



        H = −J Σ_{i∈{A,B,C}} (S_i + S_i†) + Σ_{(i,j)} Σ_{r} v(r) P_{ij}(r),     v(r) = g cos(2πr/N),



        W = exp(−i τ H)       (units with ħ = 1; τ is the duration of one stage).



Each S_i commutes with the global translation, because translations on ℤ_N commute, and each

P_{ij}(r) depends only on a separation. So H and W are invariant.



7.2 The Flash Instrument



Let w be a normalized discrete Gaussian on ℤ_N of width s > 0:



        w(r) ∝ exp(−|r|_N² / (2 s²)),     Σ_r w(r) = 1,



where |r|_N is the distance from r to 0 around the ring. Let λ ∈ (0, 1) be the hit probability per

stage. The transition events are 𝒦 = {∅} ∪ {(i, j, d) : (i, j) an ordered pair as above, d ∈ ℤ_N},

with Kraus operators



        F_∅ = √(1−λ) · 1,     F_{(i,j,d)} = √(λ/3) · Σ_r √(w(r−d)) P_{ij}(r).



Event (i, j, d) is a relational flash: an objective event centred on the separation d between

particles i and j. Completeness holds because Σ_d w(r−d) = 1 for every r, so Σ_d F_{(i,j,d)}†

F_{(i,j,d)} = (λ/3) · 1 for each pair, and the three pairs together with F_∅ sum to the identity.

Every F_k is invariant, since it is a function of separations. Because w(r) > 0 for every r and λ <

1, every F_k is invertible, so Proposition 4.12 applies. The sharp limit s → 0 gives w(r) = δ_{r,0},

in which a flash projects exactly onto separation d and is no longer invertible.



7.3 Frame Forms



In frame A the relational projectors take the forms P_{AB}(r) → [x = r], P_{AC}(r) → [y = r],

P_{BC}(r) → [y − x = r]; in frame B they become [u = −r], [v − u = r], [v = r]. Appendix A lists all

three frames. Hopping of the frame particle itself appears as a joint shift of all relative

coordinates: in frame A, moving A one site to the right lowers both x and y by one. This is how

“motion of the reference frame” appears inside the frame’s own description. By Lemma 3.7, each of

these forms is the conjugate of the others by the appropriate V, so the frame-relative laws satisfy

Definition 5.11.



7.4 Why the Flashes Must Be Relational



Suppose one tried to use an absolute collapse operator, for example the projector P_abs onto “C is

at site 0”. P_abs is not invariant. Applied to any Ψ ∈ H_phys, it produces a vector supported on

configurations with c = 0, and its translation-averaged part has squared norm only 1/N of the total,

because the N translates of that support are mutually orthogonal and only the untranslated term

contributes. Hence



        ‖(1 − Π) P_abs Ψ‖ / ‖P_abs Ψ‖ = √(1 − 1/N)



for every Ψ ∈ H_phys with P_abs Ψ ≠ 0, which is about 0.894 for N = 5. Most of the collapsed state

lies outside the physical space, so an absolute collapse operator does not carry physical states to

physical states.



The point generalizes within the perspective-neutral construction. If an operator X maps H_phys into

itself, then for every Ψ ∈ H_phys we have Ψ = Π Ψ and X Ψ = Π X Ψ, so X agrees on H_phys with Π X Π,

which is invariant. Hence, if every realized event is to carry a physical state to a physical state,

as Definition 4.1 requires and as single-outcome realism needs when each event is to be a gauge-

invariant fact, then each Kraus operator must act on physical states exactly as an invariant,

relational operator does.



Two qualifications fix the scope of this conclusion. First, it holds within the chosen framework.

Other formulations require only that an instrument be covariant as a whole, with the symmetry

permuting its Kraus operators; standard GRW, whose collapse centres are absolute positions, is of

this kind. In such formulations the averaged channel can preserve the physical sector even though

individual updates do not, and an account is then owed of what gauge-invariant fact an outcome with

an absolute label records in a closed universe. Second, the CSL equation cited in CTGP – explained,

§10.1, uses smeared mass-density operators A(x) at absolute positions x. Reformulating CSL in terms

of mass densities relative to material frames is a natural route for CTGP’s collapse option (Q2),

but whether CSL must be so reformulated depends on the formulation and would require further

argument. What the present construction establishes is sufficiency: invariant relational collapse

operators provide an explicit, verified realization of QRF-compatible single-outcome dynamics. The

equivalence proved above concerns the action of an operator on physical states; it does not show

that every physically acceptable collapse theory must use the particular relational flash ontology

of §7.2, which is one realization among others.



----------------------------------------------------------------------------------------------------

8. The Criteria in the Model, With Numerical Checks

----------------------------------------------------------------------------------------------------


