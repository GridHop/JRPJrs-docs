# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 19 of 25 (1,793 words)

Proposition 17.6 (Matter-constrained foliation expansion). Let u^μ be the timelike congruence

aligned with the cosmological matter flow, and let θ = ∇_μu^μ denote its expansion scalar. In

globally hyperbolic, irrotational cosmological spacetimes satisfying the Einstein equations, the

evolution of θ is governed by the Raychaudhuri equation: dθ/dτ = −(1/3)θ² − σ_{μν}σ^{μν} +

ω_{μν}ω^{μν} − R_{μν}u^μu^ν + ∇_μa^μ. In the irrotational, geodesic cosmological limit this reduces

to dθ/dτ = −(1/3)θ² − σ_{μν}σ^{μν} − R_{μν}u^μu^ν. Under standard energy conditions, the matter

content constrains the sign and evolution of θ, and hence constrains the geometric extension of the

CTGP foliation. The expansion scalar θ = d(ln √h)/dτ provides the physically grounded local measure

of how the present hypersurface is extending relative to neighboring hypersurfaces in the generated

sequence.



Proposition 17.7 (Variational Derivation of the Norm Condition). The norm condition ∇_μσ ∇^μσ =

−f(σ) is not an independent postulate. The derivation treats σ as a smooth field and therefore

applies on open regions where τ is sufficiently smooth and the other fields satisfy the regularity

assumptions required for the classical variational calculation. Extending it across nonsmooth

regions, including corners of cosmological-time level sets, would require an appropriate weak

formulation, which is not attempted here. Independently of the action, τ is locally Lipschitz

(Theorem 17.4), so for smooth F with F′ > 0, ∇_μσ exists almost everywhere, and Theorem 17.4

together with the chain rule gives the norm condition wherever τ is differentiable, hence almost

everywhere. The two results are distinct: the variational one shows that the norm condition is

required by stationarity of the action with respect to the multiplier, while the geometric one shows

that cosmological time satisfies it. The generative present itself does not depend on the action,

since cosmological time fixes it (§6.3). Consider the CTGP action



        S[g_{μν}, σ, λ] = ∫_{M(σ)} √(−g) [ L_{GR} + λ(∇_μσ ∇^μσ + f(σ)) ] d⁴x



where λ(x) is a Lagrange multiplier scalar field and f(σ) > 0 is the generation law. Because M(σ) is

itself defined through σ, the variation is taken on a fixed domain: the region and its boundary are

held fixed while the fields vary, and variations vanish on the boundary. The three Euler–Lagrange

conditions are as follows.



    (i) Variation with respect to λ: δS/δλ = 0 gives ∇_μσ ∇^μσ + f(σ) = 0, i.e., ∇_μσ ∇^μσ = −f(σ).

    This is the norm condition, established as a necessary condition for stationarity of S.



    (ii) Variation with respect to σ: since ∂/∂σ of the Lagrangian is λf′(σ) and ∂/∂(∂_μσ) is

    2λ∇^μσ, integrating by parts and discarding the boundary term, which vanishes for such

    variations, yields the propagation equation ∇_μ(λ∇^μσ) = ½λf′(σ). It is linear and homogeneous

    in λ, reduces to a conservation law for the current λ∇^μσ when f is constant, and transports λ

    along the generation flow; λ = 0 on an initial surface therefore implies λ ≡ 0.



    (iii) Variation with respect to g^{μν}: the L_{GR} term yields G_{μν} = 8πG T_{μν} as usual. The

    constraint term contributes T^{(σ)}_{μν} = 2λ∇_μσ∇_νσ − λg_{μν}(∇_ρσ∇^ρσ + f), up to the sign

    convention adopted for T_{μν}. On the constraint surface the second term vanishes, leaving

    T^{(σ)}_{μν} = 2λ∇_μσ∇_νσ: a pressureless fluid flowing along ∇^μσ with energy density

    proportional to λf — the structure familiar from mimetic gravity (Chamseddine and Mukhanov

    2013). Because f depends only on σ, no term couples the constraint sector to the matter

    equations. For λ ≡ 0, the Einstein–matter system is exactly that of general relativity.



The significance of this proposition is methodological. A Lagrange multiplier implements a chosen

constraint exactly, so that the condition follows from stationarity of the action rather than being

added separately; it does not by itself explain why that constraint, or that action, should be

selected. The justification for the norm condition is geometric: cosmological time satisfies it

(Theorem 17.4). The proposition shows that the same condition can be expressed within a standard

variational framework without altering the Einstein–matter dynamics, since λ = 0. □



Proposition 17.8 (Geometric invariance of the generative present). Let Φ : (M, g) → (M′, g′) be an

isometry between spacetimes with regular cosmological time. Then τ′ ∘ Φ = τ. Consequently, the

generative present is fixed by the geometry and is not a gauge choice: diffeomorphisms that preserve

the metric map its stages to stages, and no relabeling of coordinates can alter which events are co-

present. The only freedom is the labeling σ = F(τ), which leaves the stages unchanged.



Proof. Isometries map causal curves to causal curves and preserve Lorentzian length, so the supremum

defining τ′(Φ(p)) ranges over the images of exactly the curves defining τ(p). □



Theorem 17.9 (Stage-Relative Representation). Let M(σ) = ⋃_{σ′ < σ} Σ_{σ′} be the domain of the CTGP

action S(σ) (§9.1). If (1) σ is monotonic, (2) Σ_σ obeys hyperbolic evolution, and (3) future

hypersurfaces are excluded from the domain, then the family {M(σ)} is nested, M(σ′) ⊂ M(σ) for σ′ <

σ, and each M(σ) is determined by data on Σ_σ and its causal past alone. The formalism therefore

represents reality stage-relatively, without modifying the field equations. This representation is

not by itself inequivalent to a completed manifold: a block theorist may read each M(σ) as a region

of a pre-existing spacetime. Whether the nested family represents a history generated stage by stage

or a sequence of regions of a fixed whole is settled by an ontological assumption about the

existence of future stages, not by the mathematics. CTGP adopts the first reading; the theorem shows

that its formalism expresses that reading consistently, not that the field equations or observations

favor it (§12.1).



Proposition 17.10 (Domain Restriction and Local Dynamics). Let S_{block} = ∫_M √(−g) L_{GR} d⁴x and

S_{CTGP}(σ₀) = ∫_{M(σ₀)} √(−g) [L_{GR} + λ(∇_μσ ∇^μσ + f(σ))] d⁴x. (i) At every point of M(σ₀), the

Euler–Lagrange equations of S_{CTGP} with λ = 0 coincide with those of S_{block} together with the

norm condition. (ii) M(σ₀) has a future boundary Σ_{σ₀} and M does not, so the two domains are not

diffeomorphic as manifolds with boundary. The domain restriction is therefore not a difference in

local dynamics or in any observable (Proposition 12.1). It is the formal expression of the stage-

relative ontology, and whether the future boundary marks the edge of reality or only the edge of a

description is an interpretive question.



Proof. Part (i) holds because Euler–Lagrange equations are local and the constraint sector

contributes nothing when λ = 0. Part (ii) holds because diffeomorphisms map boundary points to

boundary points. □



Corollary 17.11 (A Formal, Not Empirical, Distinction). The CTGP and block-universe variational

principles differ in domain but not in local field equations or observable consequences. The

distinction they encode is ontological: whether the domain of the laws is the formal history of a

generated present or a fixed manifold. Empirical bearing on that distinction comes only through the

generability constraint (§12.2).



Definition 17.12 (Geometric Growth Measure). Let u^μ be the timelike congruence aligned with the

cosmological matter flow, and let θ = ∇_μu^μ denote its expansion scalar. CTGP identifies θ as the

physically meaningful local measure of geometric growth: it equals d(ln √h)/dτ and thus measures the

fractional rate of change of local hypersurface volume along the matter congruence. Rather than

defining ontological growth as dM/dσ — which treats the generated domain as if it were a scalar

quantity — CTGP uses the foliation expansion to characterize growth. The evolution of θ is governed

by Proposition 17.6; it is constrained directly by matter content through the Einstein equations.

Cosmologically, this yields a physically meaningful picture: in the early dense universe, θ is large

(rapid geometric expansion); in the matter-dominated and late universe, the Raychaudhuri equation

predicts the observed deceleration and re-acceleration through the curvature and energy-condition

terms, without requiring the parameter dM/dσ to be interpreted as a rate of literal spacetime

production.



Proposition 17.13 (Compatibility with Causal-Set Quantum Gravity). Let a discrete causal set (C, ≺)

be generated via sequential growth dynamics in the sense of Rideout and Sorkin (2000). Assume the

continuum limit of (C, ≺) yields a globally hyperbolic spacetime (M, g) with a smooth temporal

function σ whose level sets are spacelike Cauchy hypersurfaces (Bernal–Sánchez). Then: (1) the

directional causal structure — past ⊂ M(σ), future ∉ M(σ) — is preserved in the continuum limit; (2)

every element in the causal set has a finite causal past at any finite stage of growth, and no

future elements are present at that stage; (3) the element-by-element addition of causal elements in

sequential growth dynamics represents one possible discrete realization of CTGP’s fundamentally

continuous generative flow, whose large-N limit may correspond to the continuum σ (§6.2). The

direction of compatibility runs from CTGP’s continuous generative-flow ontology to causal-set models

as discrete instantiations, not the reverse. Therefore, CTGP’s commitment to causality and the

ontologically open future is compatible with at least one well-defined approach to quantum gravity.

The claim that quantum gravity necessarily violates causality is accordingly a contingent

interpretive claim, not a result established by any current quantum-gravity framework with empirical

support. Remark: This result is stated as a compatibility proposition rather than a theorem because

it depends on the unestablished identification of causal set theory as the correct theory of quantum

gravity. Its purpose is to demonstrate that CTGP’s causal commitments are not undermined by quantum-

gravity considerations in at least one well-developed approach.



Because sequential growth dynamics is label-invariant, the birth order of elements is not itself

physical; the compatibility asserted here concerns the directional causal structure of (1) and (2),

not the identification of a global present, which CTGP supplies separately through cosmological time

(§15.2).



Theorem 17.14 (Constraint Stability under CTGP Perturbations). Let U = (h_{ij}, K_{ij}, matter)

denote ADM variables evolving under ∂_t U = ℰ(U) + ε 𝔻(U), where ℰ is the standard Einstein–matter

evolution and ε 𝔻 represents CTGP-induced perturbative corrections. Define the constraint vector C =

(ℋ, ℋ_i). Then the constraint propagation system satisfies ∂_t C = A^i(U)∂_i C + B(U)C + ε S(U). For

Sobolev index s > 5/2 and vanishing initial constraints C(0) = 0, ‖C(t)‖_{Hs-1} ≤ ε e^{Kt} ∫_0^t

‖S(U(τ))‖_{Hs-1} dτ. Constraint violation therefore remains O(ε) in Sobolev norm on finite evolution

intervals. If the source term S(U) lies within the standard gauge sector, the violation is

absorbable by lapse and shift adjustment. The appropriate statement is a Sobolev-norm control bound

rather than a fixed numerical tolerance: CTGP-compatible perturbations preserve constraint structure

to leading order. □



Theorem 17.15 (Constraint-Compatible Foliation Gluing). Let U^{(1)} and U^{(2)} be solutions of the

Einstein–matter system in Sobolev class H^s (s > 5/2 + 1) on overlapping globally hyperbolic charts

V_1, V_2 whose initial data agree on the overlap up to order s. Let χ_1, χ_2 be a partition of unity
