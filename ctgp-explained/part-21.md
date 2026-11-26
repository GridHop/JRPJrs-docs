# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 21 of 26 (1,800 words)

physically meaningful local measure of geometric growth: it equals d(ln √h)/dτ and thus measures the

fractional rate of change of local hypersurface volume along the matter congruence. Rather than

defining ontological growth as dM/dσ — which treats the generated domain as if it were a scalar

quantity — CTGP uses the foliation expansion to characterize growth. The change of θ is governed by

Proposition 17.6; it is constrained directly by matter content through the Einstein equations.

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

denote ADM variables governed by ∂_t U = ℰ(U) + ε 𝔻(U), where ℰ is the standard Einstein–matter

dynamics and ε 𝔻 represents CTGP-induced perturbative corrections. Define the constraint vector C =

(ℋ, ℋ_i). Then the constraint propagation system satisfies ∂_t C = A^i(U)∂_i C + B(U)C + ε S(U). For

Sobolev index s > 5/2 and vanishing initial constraints C(0) = 0, ‖C(t)‖_{Hs-1} ≤ ε e^{Kt} ∫_0^t

‖S(U(τ))‖_{Hs-1} dτ. Constraint violation therefore remains O(ε) in Sobolev norm on finite time

intervals. If the source term S(U) lies within the standard gauge sector, the violation is

absorbable by lapse and shift adjustment. The appropriate statement is a Sobolev-norm control bound

rather than a fixed numerical tolerance: CTGP-compatible perturbations preserve constraint structure

to leading order. □



Theorem 17.15 (Constraint-Compatible Foliation Gluing). Let U^{(1)} and U^{(2)} be solutions of the

Einstein–matter system in Sobolev class H^s (s > 5/2 + 1) on overlapping globally hyperbolic charts

V_1, V_2 whose initial data agree on the overlap up to order s. Let χ_1, χ_2 be a partition of unity

subordinate to V_1, V_2 and define blended initial data U_0 = χ_1 U_0^{(1)} + χ_2 U_0^{(2)}. After

projection onto the constraint manifold via the conformal method, provided the constraint mismatch

on the overlap is sufficiently small in H^{s-1}, there exists T > 0 and a unique local solution U ∈

C([0,T], H^s) ∩ C^1([0,T], H^{s-1}) with stability bound ‖U − U^{(a)}‖_{Hs-1(V′a)} ≤ C_T ‖overlap

mismatch‖_{Hs-1(V1 ∩ V2)} on each subpatch V′_a ⋐ V_a. The gluing claim is thereby a standard PDE

construction: local CTGP foliations may be patched only through overlap data first reconciled at the

level of the Einstein constraint equations, after which the hyperbolic dynamics apply to the

corrected blended data. □



Proposition 17.16 (Conditional Tomonaga–Schwinger Integrability). Let {Σ} be a family of smooth

spacelike Cauchy hypersurfaces in a globally hyperbolic spacetime (M,g). Let the density operator

ρ[Σ] be governed by δρ[Σ]/δΣ(x) = ℒ_x(ρ[Σ]), where ℒ_x is a local generator at x ∈ Σ. Assume: (1)

Microcausality — [ℒ_x, ℒ_y]ρ = 0 for spacelike-separated x, y on a common dense invariant domain D;

(2) Energy-boundedness — each smeared generator ℒ(f) = ∫_Σ f(x) ℒ_x dΣ is closable on D and

satisfies ‖ℒ(f)ψ‖ ≤ a‖H_0 ψ‖ + b‖ψ‖ with a < 1; (3) Strong continuity of the generated propagators

on D. Then the propagator between two hypersurfaces depends only on the spacetime region swept out,

not the intermediate foliation: ρ[Σ_2] = U(Σ_2, Σ_1) ρ[Σ_1] is foliation-path-independent. No

superluminal signaling is introduced. CTGP requires only collapse densities built from local

commuting field polynomials or smeared number/energy densities with spacelike-separated supports

commuting in the AQFT sense; this admissible class satisfies the conditions above, making

hypersurface-path independence a conditional theorem rather than an assumed property. □



Theorem 17.17 (Continuum Limit of Local CP Dynamics). Let ℒ^{(n)} be a sequence of Lindblad

generators built from bounded truncations L_α^{(n)} of a local operator family L_α with UV cutoff

Λ_n → ∞. Assume: (1) L_α^{(n)} → L_α strongly on a common dense domain D; (2) ∑_α L_α† L_α ≤ c_1 H_0

+ c_2 I relative to a positive reference Hamiltonian H_0; (3) truncated semigroups e^{tℒ(n)} are

CPTP; (4) initial states satisfy Tr(ρ H_0) < ∞. Then for each finite interval [0,T]: sup_{t ≤ T}

‖e^{tℒ(n)}ρ − e^{tℒ}ρ‖_1 → 0 as n → ∞. The error bound is ‖e^{tℒ(n)}ρ − e^{tℒ}ρ‖_1 ≤ C_T(ε_n(ρ) +

δ_n), where ε_n(ρ) = Tr(ρ Π_{>Λn}) is the UV tail measure and δ_n is the truncation error. The

theorem gives the finite-mode-to-continuum passage the form of a trace-norm convergence statement,

supplying the reference Hamiltonian, common domain, UV tail parameter, and finite-time control that

make the claim a genuine mathematical program. □



Proposition 17.18 (Emergent Status of σ Near Planck Scale). For curvature invariants satisfying

|R_{μνρσ}| ≪ M_{Pl}^2, σ exists as a time function whose level sets are future Cauchy surfaces,

given by cosmological time as in §§6.1–6.3, and it is a smooth temporal scalar field wherever the

maximizing congruence is single-valued. Near Planck curvature, the smooth representation may break

down; CTGP then treats σ as the continuum image of an underlying growth ordering variable, with

causal-set counting as the preferred candidate discrete realization. CTGP is therefore fundamental

at the ordering level, not necessarily at the smooth-manifold level: the smooth σ-field is emergent

in the classical regime, and singular classical regions mark breakdown of the continuum

representation rather than breakdown of temporal ordering itself. This avoids a false dichotomy

between “σ is fundamental as a smooth field everywhere” and “CTGP fails wherever classical GR

fails.” □



Proposition 17.19 (Bridge-Model Identifiability Conditions). Let q = Θ F(X) represent a candidate

mapping from physiological state vector X to phenomenological proxy q. The mapping is empirically

meaningful for CTGP’s psychophysical research program only if: (1) it generalizes to held-out

subjects not used in fitting; (2) it remains predictive after nuisance regression controlling for

arousal, task difficulty, medication status, and global signal; (3) it retains predictive power

under causal perturbation (TMS, anesthesia, sleep-stage shifts, focal lesions); (4) nested model

comparison suggests CTGP-style substrate-sensitive models outperform purely functional baselines;

(5) a primary endpoint is pre-registered. These criteria convert the mapping problem from an

unfalsifiable metaphysical claim into a testable research program. Note that identifiability in this

strong sense is required for the psychophysical extension of Appendix D but is not a prerequisite

for the core spacetime ontology of the main text, which stands on its own physics and philosophy-of-

physics merits. □



Definition 17.20 (Tense Semantics). Let W_σ denote the present world at stage σ, and for σ′ < σ let

Had(σ′, φ) denote the primitive property *having been, at stage σ′, such that φ* (§5.2.1), where φ

ranges over non-tensed propositions.



    (a) *Truth condition.* “At σ′ it was the case that φ” is true at σ iff W_σ instantiates Had(σ′,

    φ).



    (b) *Accuracy condition.* For every σ′ < σ, W_σ instantiates Had(σ′, φ) iff W_σ′ ⊨ φ.



    (c) *Representation.* M(σ) = ⋃_{σ′<σ} Σ_{σ′} is the formal representation of the history carried

    by the present world’s past-tensed profile. For each σ′ < σ, the represented stage Σ_{σ′}

    satisfies φ in M(σ) exactly when W_σ instantiates Had(σ′, φ).



    (d) *Asymmetry.* W_σ instantiates no property grounded in a future stage, since no stage Σ_{σ″}

    with σ″ > σ exists.



Corollary 17.21 (Nesting). For σ < σ″, M(σ) ⊂ M(σ″).



Proof. Every stage in ⋃_{σ′<σ} Σ_{σ′} also lies in ⋃_{σ′<σ″} Σ_{σ′}. Nesting is a property of the

formal representation; it does not imply that earlier stages continue to exist. □



Proposition 17.22 (No Revision of the Past). For σ < σ″ and every σ′ < σ, Σ_{σ′} satisfies φ in M(σ)

iff Σ_{σ′} satisfies φ in M(σ″).



Proof. By (c) and (b), Σ_{σ′} satisfies φ in M(σ) iff W_σ instantiates Had(σ′, φ) iff W_σ′ ⊨ φ. The

same chain holds with σ″ in place of σ. □



Proposition 17.22 is the formal counterpart of the claim in §5.2.1 that losing a record does not

change what happened. Records can degrade between σ and σ″; the represented history of every earlier

stage cannot.



Proposition 17.23 (Surface-Relative Cosmological Time). Let (M, g) be globally hyperbolic and S a

spacelike Cauchy surface, and let τ_S be the signed Lorentzian distance from S (§6.10.1). Then on

each side of S, τ_S is the cosmological time of that region with S as its past (respectively future)

boundary; it is finite, tends to zero on approach to S, and its level sets are future (respectively

past) Cauchy surfaces. Consequently σ = F(τ_S), with F strictly increasing, is an admissible

generation parameter through S. In an exact FLRW universe with a single bounce, taking S to be the

surface of zero mean curvature at the bounce makes τ_S cosmic time measured from the bounce.



Proof sketch. Restrict to the open region I⁺(S), itself globally hyperbolic. Every past-inextendible

causal curve in it approaches S, and J⁻(p) ∩ J⁺(S) is compact for each p, so the supremum defining

τ_S(p) is finite and τ_S → 0 along curves approaching S: the cosmological time of I⁺(S) is regular.

Theorem 17.4 then applies to that region, and the same argument with time reversed applies to I⁻(S).

□



----------------------------------------------------------------------------------------------------
