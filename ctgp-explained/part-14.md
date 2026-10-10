# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 14 of 26 (1,621 words)

PART III. Physical Realization and Empirical Standing

====================================================================================================



----------------------------------------------------------------------------------------------------

11. Admissible Generation Laws: A Consistency Analysis

----------------------------------------------------------------------------------------------------



The generative present of §6 is fixed by geometry. A natural further hypothesis is that the rate at

which σ advances depends on local physical conditions — in particular, that generation proceeds

faster where matter is denser. Such a law would give the generation parameter physical content

beyond geometry and could in principle imprint new cosmological signatures. This section shows that

the hypothesis is untenable. The exact form of the law destroys the alignment of the present with

matter (§§11.1–11.2); its stable soft completions force a uniform rate inside bound structures and

suppress any cosmological effect far below observability (§11.3). Within the local, stable classes

analyzed, the viable generation laws reduce to functions of σ alone (§6.11), and their residual

caustic problem is resolved at Layer 2 by cosmological time (§11.4). Finally, no admissible law

yields an intrinsic cosmological axis (§11.5). Within those classes, the results hold for general f

and apply to every increasing density dependence, not only to particular choices.



11.1 The Conformal Form of the Norm Condition

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Proposition 11.1 (Conformal form). If g^{μν}∂_μσ∂_νσ = −f with f > 0, then σ has unit-norm gradient

in the conformally related metric g̃ = f g. The normalized generation flow n_μ = −∂_μσ/√f has

acceleration



        a_μ = n^ν∇_ν n_μ = −D_μ ln √f,



where D_μ = (δ_μ^ν + n_μ n^ν)∂_ν is the derivative projected orthogonally to n.



Proof. Using the symmetry of ∇_μ∂_νσ and n^μ n_μ = −1, one finds n^μ∇_ν∂_μσ = ∂_ν√f, and hence

n^μ∇_μ n_ν = −∂_ν ln√f − n_ν n^μ∂_μ ln√f = −D_ν ln√f. □



Two cases follow. If f = f(σ), then D_μf = f′D_μσ = 0, so a_μ = 0: the generation flow is geodesic.

If f carries spatial matter dependence — for example f = ρ_c²/ρ_*² — then a_μ = −D_μ ln ρ_c, and the

flow is pushed down density gradients. In Newtonian terms (c = 1) the generation flow experiences

the effective potential



        Φ_{eff} = Φ + ln(ρ_c/ρ̄).



On sub-horizon scales density contrasts exceed metric potentials by a factor of order (k/aH)², and

inside a galaxy ln ρ_c varies by order ten while Φ ∼ 10⁻⁶. A density-weighted generation flow

therefore responds to matter density far more strongly than to gravity.



11.2 Relative Tilt Between the Generation Flow and Matter

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Linearize about FLRW in longitudinal gauge, with pressureless matter and λ = 0. Write the covariant

velocities of the two flows as u_i = ∂_{iV}, so that V_σ = −δσ/σ̄̇ for the generation flow, while

matter obeys V̇_m = −Φ. The linearized norm condition gives δσ̇ = Φσ̄̇ + δf/(2σ̄̇).



Proposition 11.2 (Relative tilt). The relative tilt T ≡ V_σ − V_m is gauge-invariant and obeys



        Ṫ = −(ḟ/2f̄) T − Δ_f,  Δ_f ≡ δf/(2f̄) + (ḟ/2f̄) V_m,



with the metric potential Φ cancelling identically. For f = f(σ), Δ_f = −(ḟ/2f̄)T and Ṫ = 0, so the

physical relative velocity v = kT/a decays as 1/a. For f = ρ_c²/ρ_*² in the matter era, the equation

becomes Ṫ − 3HT = −Δ_c, where Δ_c is the comoving density contrast, with solution



        T = C a³ + 2Δ_c/H,  v = C k a² + 2 (k/aH) Δ_c.



Two conclusions follow for density weighting. A primordial tilt grows as a² during matter domination

and a³ during radiation domination, a growth factor of order 10²⁶ from the end of inflation to the

present; an intrinsic tilt is therefore either fine-tuned to about one part in 10²⁶ initially or has

already driven the foliation toward null. And structure sources a tilt that exceeds matter peculiar

velocities by a factor of order (k/aH)², so that alignment of the generation flow with matter

survives only on scales comparable to or larger than the horizon.



Corollary 11.3 (Light-crossing bound). Suppose σ advances along matter worldlines at a rate set by

local density, σ = ∫ρ_c dτ, in a quasi-static structure with density scale length L = ρ_c/|∇ρ_c|.

Then σ ≈ ρ_c(x)t, and its level sets are spacelike only for t < L (c = 1). For a galaxy with L ≈ 10

kpc and an age of 10¹⁰ yr this condition is violated by a factor of about 3 × 10⁵. If the exact norm

condition is imposed instead, the generation flow is repelled from density peaks within a light-

crossing time and forms caustics. □



11.3 Soft Completions

~~~~~~~~~~~~~~~~~~~~~



Adding a conventional kinetic term to the exact action changes nothing: a term proportional to

∇_μσ∇^μσ appears in the Lagrangian only in combination with the multiplier term and is absorbed by a

constant shift of λ, at the cost of a term proportional to f. Genuine propagation of σ therefore

requires a Lagrangian nonlinear in X ≡ −½∇_μσ∇^μσ. The natural completion replaces the exact

constraint by a stable-sign preferred norm,



        S_σ = ∫ √(−g) P(X, T) d⁴x,  P = P₀(X) + (κ/2)[X − X⋆(ρ)]²,  κ > 0,



with X⋆ increasing in ρ. The standard k-essence conditions (Garriga and Mukhanov 1999) apply: the

sound speed is c_s² = P_X/(P_X + 2XP_{XX}), absence of ghosts requires P_X + 2XP_{XX} > 0, and

absence of gradient instability requires P_X > 0. The penalty must carry the stable sign shown; the

opposite sign makes P_{XX} negative near the preferred norm and produces a ghost. Because P does not

depend on σ, the field equation is the conserved-current equation ∇_μ(P_X∇^μσ) = 0 with no source

term: matter enters only through the coefficient P_X(X, T). On an FLRW background this gives a³P_Xσ̇

= C, so that near the preferred norm c_s² ≈ C/(2κX a³σ̇). The sound speed is therefore set by an

integration constant rather than predicted, and C = 0 reproduces the pressureless behavior of the

exact constraint, as in ghost condensation (Arkani-Hamed et al. 2004).



Theorem 11.4 (Static rate uniformity). Let the σ-sector be shift-symmetric, S_σ = ∫√(−g) P(X, T)

d⁴x, with T_{μν} depending only on metric and matter fields. Consider a static, asymptotically flat

configuration σ = ωt + φ(x), regular everywhere, and suppose P_X > 0 wherever it is supported. Then

∇φ ≡ 0.



Proof. The spatial equation is ∂_i(√(−g) P_X g^{ij}∂_jφ) = 0. Regularity and the divergence theorem

make the flux through every closed surface vanish, so φ − φ_∞ = O(r⁻²). Multiplying by φ − φ_∞ and

integrating by parts gives ∫√(−g) P_X g^{ij}∂_iφ∂_jφ d³x = lim_{r→∞} ∮(φ − φ_∞)P_X ∇φ · dS = 0. The

integrand is non-negative, so ∇φ = 0. □



Every stable static structure therefore has the same generation rate as its surroundings: σ = ωt,

with X = ω²/(2N²) where N is the lapse. A locally enhanced generation rate inside bound structure is

excluded for the entire class.



Proposition 11.5 (Stability transport bound). Suppose the background evolves near the preferred

norm, X̄ ≈ X⋆(ρ̄). (a) By Theorem 11.4, a static structure containing densities up to ρ_{max} at an

epoch with background norm X₁ is stable only if



        P₀′(X₁) > κ [X⋆(ρ_{max}) − X₁].



(b) Along the background, the no-ghost condition reads d(X^{1/2}P₀′)/dX > −κX^{1/2}. Integrating to

an earlier epoch with X₂ > X₁ gives



        P₀′(X₂) ≳ κ X⋆(ρ_{max}) (X₁/X₂)^{1/2},



provided X⋆(ρ_{max}) X₁^{1/2} ≫ X₂^{3/2}. (c) The fractional modulation of the σ-sector by density

perturbations δ at the earlier epoch is then bounded by



        ε ≡ κ ρ̄ X⋆′(ρ̄) δ / P̄_X ≲ δ · [ρ̄ X⋆′(ρ̄) / X⋆(ρ_{max})] · (X₂/X₁)^{1/2}.



For X⋆ ∝ ρ² this becomes ε ≲ 2δ (ρ̄₂/ρ_{max})² (ρ̄₂/ρ̄₁); the constants κ, the normalization of P₀,

and ρ_* all cancel. At recombination (ρ̄₂ ≈ 4 × 10⁻¹⁸ kg m⁻³, δ ≈ 10⁻⁵), measured against the epoch

at which compact objects first exist (z ≈ 20, ρ̄₂/ρ̄₁ ≈ 1.4 × 10⁵), the bound is ε ≲ 10⁻⁶⁸ with

ρ_{max} ≈ 10¹⁷ kg m⁻³ (neutron stars) and ε ≲ 10⁻⁴⁰ even with ρ_{max} = 10³ kg m⁻³ (ordinary

condensed matter). □



Corollary 11.6 (Exclusion of density weighting). Within the class of local, shift-symmetric, stable-

sign completions, no unsaturated increasing X⋆(ρ) produces an observable density-weighted

cosmological signature. □



Remark (saturation). If X⋆ stops growing above some density ρ_s ≲ ρ̄₂, the bound relaxes to order δ.

This is a distinct, screened model class: it introduces a new density scale tuned to the relevant

epoch, equalizes the generation rate in everything denser than ρ_s — the opposite of density-

weighted generation — and supplies no preferred axis. Its residual effect is proportional to the

σ-sector’s share of the energy budget, which is bounded by constraints on early dark energy.



11.4 Caustics and the Cosmological-Time Completion

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The admissible generation laws f = f(σ) make the generation flow geodesic (Proposition 11.1).

Initialized on the comoving congruence, it coincides with the free fall of pressureless matter, and

pressureless free fall shell-crosses inside every collapsed halo. A smooth scalar σ therefore

develops caustics wherever structure has formed, and any nonzero λ-dust would acquire a divergent

density there. Caustic-free completions of pressureless fluids and k-essence have been studied in

the literature (Babichev and Ramazanov 2017).



CTGP does not need such a completion. The Layer 2 present is defined by cosmological time, which is

the maximal single-valued continuation of the unit-norm solution: where maximizing geodesics cross,

τ loses differentiability, its level sets acquire corners, and they remain Cauchy surfaces (Theorem

17.4). With λ = 0 (§6.9) no divergent stress-energy arises. The generative present is therefore

globally well defined in a universe with nonlinear structure, while the smooth continuum σ-field is

a valid description only where the maximizing congruence is single-valued. Alignment of the present

with matter is correspondingly narrowed: it holds exactly in FLRW and with the free fall of

pressureless matter in single-stream regions, not with pressure-supported components or within

multistream regions.


