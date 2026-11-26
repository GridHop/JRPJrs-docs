# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 20 of 26 (1,790 words)

initial data (h_{ij}, K_{ij}, matter data) that satisfy the Hamiltonian and momentum constraints and

are of sufficient regularity (smooth data, or data of the finite Sobolev regularity required by the

local existence theorems), and let the matter fields obey equations for which the coupled

Einstein–matter system has a well-posed Cauchy problem, as minimally coupled scalar and Maxwell

fields do. Then the Einstein–matter equations determine a development of the data in a neighborhood

of Σ, unique up to diffeomorphism, and a maximal globally hyperbolic development in which Σ is a

Cauchy surface, unique up to isometry (Choquet-Bruhat and Geroch 1969). Where τ is differentiable

and its maximizing geodesics form a single-valued congruence, the level sets Σ_σ are smooth

spacelike hypersurfaces and the proposition applies to them directly. A level set with corners

(§6.1) does not satisfy the smoothness hypothesis, and the proposition does not apply to it as it

stands. The development can still be computed in a smooth foliation (§8), but the stronger statement

that the data on a cornered level set by themselves determine its future domain of dependence would

require an initial-value formulation for nonsmooth hypersurfaces, which is not established here. The

temporal ordering implicit in this initial-value structure is inherited from the causal structure of

spacetime itself.



Corollary 17.3 (No future boundary dependence). The development depends on initial data and

dynamical equations, not on boundary conditions at σ′ > σ. CTGP interprets this as supporting non-

teleological generation: the future is not consulted.



Theorem 17.4 (Cosmological time; Andersson, Galloway, and Howard 1998). Let τ(p) = sup{L(γ) : γ a

past-directed causal curve from p}, and suppose τ is regular: finite everywhere and tending to zero

along every past-inextendible causal curve. Then (i) the spacetime is globally hyperbolic; (ii) τ is

a time function, continuous and strictly increasing along every future-directed causal curve; (iii)

every nonempty level set of τ is a future Cauchy surface, though not necessarily a Cauchy surface

(their Corollary 2.6); (iv) τ is locally Lipschitz; and (v) every event p lies on a timelike

geodesic from the initial singularity whose length equals τ(p). Wherever τ is differentiable, −∇^μτ

is the future-directed unit tangent of that geodesic, so g^{μν}∂_μτ∂_ντ = −1.



Remark. Clause (iii) is the future Cauchy property: for S_a = {τ = a}, D⁺(S_a) = {τ ≥ a}. A nonempty

level set is a Cauchy surface in the full sense exactly when every future-inextendible causal curve

passes beyond it (§6.1). In universes containing black holes, later level sets are therefore future

Cauchy surfaces without being Cauchy surfaces. On the geometric side, generation needs only the

future Cauchy property; that the data on a level set fix their successors is the separate dynamical

requirement of generability (§12.2).



Proposition 17.5 (Existence and monotonicity of σ). (1) Existence: if cosmological time is regular,

then σ = F(τ), with F smooth and F′ > 0, is a time function whose level sets are future Cauchy

surfaces, and ∇_μσ is timelike wherever τ is differentiable. (2) Matter alignment: in FLRW, τ is

cosmic time and the level sets of σ are orthogonal to the comoving matter congruence; beyond FLRW,

alignment holds with the free fall of pressureless matter in single-stream regions at linear order.

(3) Monotonicity: σ is strictly increasing along every future-directed causal curve, independently

of energy conditions.



Proposition 17.6 (Matter-constrained foliation expansion). Let u^μ be the timelike congruence

aligned with the cosmological matter flow, and let θ = ∇_μu^μ denote its expansion scalar. In

globally hyperbolic, irrotational cosmological spacetimes satisfying the Einstein equations, the

change of θ along the flow is governed by the Raychaudhuri equation: dθ/dτ = −(1/3)θ² − σ_{μν}σ^{μν}

+ ω_{μν}ω^{μν} − R_{μν}u^μu^ν + ∇_μa^μ. In the irrotational, geodesic cosmological limit this

reduces to dθ/dτ = −(1/3)θ² − σ_{μν}σ^{μν} − R_{μν}u^μu^ν. Under standard energy conditions, the

matter content constrains the sign and rate of change of θ, and hence constrains the geometric

extension of the CTGP foliation. The expansion scalar θ = d(ln √h)/dτ provides the physically

grounded local measure of how the present hypersurface is extending relative to neighboring

hypersurfaces in the generated sequence.



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

variational framework without altering the Einstein–matter dynamics, since λ = 0. Because the domain

is held fixed during variation, the action also does not select the boundary of M(σ) or derive its

advance; it implements constraints on a domain already specified. Which surface is present is fixed

by cosmological time (§6.1), and that the present advances is CTGP's ontological posit (§7), not a

consequence of the action. □



Proposition 17.8 (Geometric invariance of the generative present). Let Φ : (M, g) → (M′, g′) be an

isometry between spacetimes with regular cosmological time. Then τ′ ∘ Φ = τ. Consequently, the

generative present is fixed by the geometry and is not a gauge choice: diffeomorphisms that preserve

the metric map its stages to stages, and no relabeling of coordinates can alter which events are co-

present. The only freedom is the labeling σ = F(τ), which leaves the stages unchanged.



Proof. Isometries map causal curves to causal curves and preserve Lorentzian length, so the supremum

defining τ′(Φ(p)) ranges over the images of exactly the curves defining τ(p). □



Theorem 17.9 (Stage-Relative Representation). Let M(σ) = ⋃_{σ′ < σ} Σ_{σ′} be the domain of the CTGP

action S(σ) (§9.1). If (1) σ is monotonic, (2) Σ_σ obeys hyperbolic dynamics, and (3) future

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
