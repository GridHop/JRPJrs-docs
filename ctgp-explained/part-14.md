# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 14 of 25 (1,793 words)

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



11.5 No Intrinsic Cosmological Axis

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Three directions on the sky must be distinguished. The kinematic dipole n̂_{kin}, near Galactic (l,

b) ≈ (264°, 48°), records the motion of the Solar System relative to the CMB rest frame at about 370

km s⁻¹. The axis n̂_{mod} of the observed large-angle hemispherical power modulation, with amplitude

A ≈ 0.07, lies near (l, b) ≈ (220°, −20°) (Hoftuft et al. 2009; Planck Collaboration 2020b), roughly

70–80° from n̂_{kin}. A third direction, n̂_σ, would be the spatial projection of ∇_μσ on the

present hypersurface, if such a projection existed.



On a homogeneous background it does not: ∇_μσ̄ = (σ̄̇, 0, 0, 0), so the spatial projection vanishes

and n̂_σ is undefined. An intrinsic axis would require a long-wavelength gradient mode of σ, which

by Proposition 11.2 is a tilt of the generation foliation relative to matter. For admissible

generation laws such a tilt decays as 1/a, leaving no intrinsic axis at late times; for density-

weighted laws it grows by a factor of at least order 10²⁶ and is either fine-tuned or runaway.

Superhorizon modes invoked to generate hemispherical asymmetry are further constrained by the low

multipoles they induce through the Grishchuk–Zel’dovich effect (Erickcek, Carroll, and Kamionkowski

2008).



CTGP therefore predicts no intrinsic cosmological axis and offers no explanation of the observed

large-angle anomalies, which remain questions for standard cosmology. This is a consequence of the

framework rather than an omission: the generative present is a geometric structure, and geometry

alone does not single out a spatial direction in a homogeneous, isotropic universe.



----------------------------------------------------------------------------------------------------

12. Empirical Standing of the Ontology

----------------------------------------------------------------------------------------------------



This section states precisely what observation can and cannot establish about CTGP’s ontology. The

results are general: they apply to any presentist reading of physics, not only to CTGP.



12.1 Observational Equivalence

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Proposition 12.1 (Observational equivalence of presentist and eternalist readings). Let P

(presentist) and E (eternalist) be two ontological readings of the same physical content 𝒦 = (M,

g_{μν}, matter fields, dynamical laws, probability measure μ over admissible histories). Call a

quantity *observable* if it is a function of the physical records present to an observer at the

stage where the observation occurs — for the presentist, the records on the present surface Σ_σ.

Then every observable has the same probability distribution under P and under E, and no experiment

can discriminate between them.



Proof. An observation is a physical process, and its outcome is a function of the records present at

the stage where it occurs. Both readings assign the same admissible histories and the same measure

μ, and hence the same distribution of present records at every stage, so each observable has the

same distribution — the pushforward of μ — under both. □



Remark (what is observed). Every observation available to an observer is an observation of present

records. A fossil, a memory, a photograph, a detector event, or a photon from SN1987A carries

information about an earlier state, but information about another time is not the existence of that

time: under CTGP the earlier state has ceased to exist, and a present observer cannot observe it as

a presently existing state — not as a limitation of instruments but because, under CTGP, a presently

existing past state is not there to be observed; the notion of observing one is incoherent within

the ontology. The same holds for the future, which a present observer can predict or represent but

cannot observe, because it has not been generated. This does not break the equivalence; it is the

reason the equivalence holds. Eternalism does not permit observation of another time either: its

earlier events exist, but not at the observer’s location, and an observer interacts only with the

records present there. Neither ontology allows an observer to observe another time as present. They

differ only over whether the unobserved earlier events exist, and present records — the same under

both — cannot decide that. A theory that did allow observation of another time as present would be

different physics, with different records, and would fall under §§12.2–12.3 rather than under this

proposition.



Remark (indeterminism). The result does not depend on determinism. For stochastic laws, E represents

the realized history as one member of the ensemble, weighted by μ; P represents it as generated

stage by stage with the same transition probabilities. The observable statistics coincide.



Remark (scope). The proposition assumes that every observation, including an observer’s reports

about experience, is a physical record. First-person temporal phenomenology is not observable in

this sense; it enters CTGP as an explanatory datum through the Phenomenological Completeness

Principle (§4.5), not as experimental evidence.



Corollary. With the physics held fixed, the ontology cannot be verified by measurement. Empirical

bearing on it must come either from constraints the ontology places on which physics is possible

(§12.2) or from physical content added to 𝒦, which bears directly on that content and only

indirectly on the ontology.



12.2 The Generability Constraint

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Observational equivalence holds for fixed physical content. The two ontologies do not, however, make

the same demands on what that content can be. If only the present exists, each new state must be

producible from the current one alone: the fundamental dynamics must admit a generative initial-

value formulation relative to the existing present, with no dependence on future boundary data and

no global consistency conditions that require the whole history at once. Eternalism carries no such

requirement. A block universe can contain initial-value laws, but it can equally contain laws with

future boundary conditions, final-state constraints, or self-consistency conditions on closed causal

loops.



Let G denote the proposition that the fundamental laws are generable in this sense. Because

generability is part of what CTGP means by presentism, a confirmed failure of G would directly

contradict the ontology, whereas eternalism merely permits generable laws. Finding that our best

theories admit generative initial-value formulations is therefore evidence the ontology could have

failed and did not.



The criterion stated precisely. Generability requires a state S_σ on each level set and a law fixing

the transition probabilities P(S_{σ′} | S_σ) for σ′ > σ — a point mass in the deterministic case —

without reference to data on later level sets. Future dependence counts against generability only if

no empirically equivalent formulation of this kind exists. Enlarging the state space is legitimate

only if the added variables are physically instantiated on Σ_σ and have dynamics of their own, not

if they are defined by reference to later data; without that restriction, any history could be made

generable by encoding its future in the present state. A choice of formulation cannot refute CTGP; a

law with no legitimate generative formulation can. Conditioning a stochastic process on a later

event of nonzero probability can, under suitable assumptions, yield a forward transition law through
