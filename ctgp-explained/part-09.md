# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 09 of 25 (1,788 words)

interprets this structure as ontological generation: the next hypersurface is not pre-existing but

is computed from the present one by lawful dynamics.



        G_{μν} = 8πG T_{μν}



The Einstein equation governs the generation of each new slice. On the CTGP reading, this equation

is not a constraint on a pre-existing four-dimensional structure but a production rule: given Σ_σ,

it tells us what Σ_{σ+Δσ} is. The hyperbolic character of the equations — their dependence on

initial data rather than boundary data in the future — supports this reading structurally.



Becoming as primitive. Generation is not an ordinary relation between two coexisting states.

Predecessor and successor are never present together, so there is no stage at which both exist and

one produces the other. On CTGP, generation is primitive and tensed: the present has come to be from

what was present. The division of labor is exact. Cosmological time supplies the ordering and co-

presence of stages (§6.1), and the initial-value formulation supplies the lawful connection between

successive stages. Neither supplies becoming itself, which is the posit that CTGP adds to both.



[FIGURE: Figure 4]

  Figure 4. Minkowski spacetime diagram with the light cone of an event p and simultaneity slices of

  two inertial frames, illustrating the causal structure (I⁺, I⁻) underlying CTGP’s notion of

  generation.



----------------------------------------------------------------------------------------------------

8. ADM Decomposition and Hypersurface Evolution

----------------------------------------------------------------------------------------------------



In ADM form, the spacetime metric is decomposed into lapse N, shift N^i, and the induced 3-metric

h_{ij} on Σ_t. The extrinsic curvature K_{ij} encodes how Σ_t is embedded in the ambient spacetime:



        g_{μν} → (h_{ij}, N, N^i)



        K_{ij} = (1/2N)(∂_t h_{ij} − ∇_i N_j − ∇_j N_i)



The evolution equations and constraints provide a natural slice-to-slice evolution picture. CTGP

maps this to an ontological claim: Σ_σ is literally produced from Σ_{σ−Δσ} by lawful dynamics,

without reference to a pre-existing future slice.



The ADM Hamiltonian and momentum constraints ensure that the generated data on each new Σ_{σ+Δσ} are

consistent with the field equations. These constraints are not boundary conditions from the future

but internal consistency requirements on the present slice, further supporting the generative

interpretation.



----------------------------------------------------------------------------------------------------

9. Action Principle on Generated Domains and Cosmological Foliation

----------------------------------------------------------------------------------------------------



9.1 Action Principle

~~~~~~~~~~~~~~~~~~~~



The action principle for CTGP restricts integration to the generated domain M(σ). Within this action

principle, the kinematic equation governing σ is obtained as an Euler–Lagrange condition rather than

stipulated. The CTGP framework is formulated by requiring the physical generative history to satisfy

the stationary-action condition δS = 0, where the action is taken to be:



        S(σ) = ∫_{M(σ)} √(−g) [ L_{GR} + λ(∇_μσ ∇^μσ + f(σ)) ] d⁴x



where L_{GR} = (R − 2Λ)/16πG + L_{matter} is the Einstein–Hilbert Lagrangian density with matter, λ

is a Lagrange multiplier field, f(σ) > 0 is the generation law (f = 1 for the canonical choice σ =

τ), and √(−g) d⁴x is the invariant volume element. The integration is restricted to M(σ), ensuring

no future teleology. The term λ(∇_μσ ∇^μσ + f(σ)) enforces the norm condition on σ. Variation with

respect to the fields yields the constraint and propagation relations below.



This action and all subsequent variational results are valid within the emergent geometric regime (ρ

≪ ρ_P), where the smooth Lorentzian manifold (M, g_{μν}) is a valid continuum approximation. The

pre-classical regime is addressed in §9.2 and §10.2; the extended action S_{ext}(σ) that models the

crossover via the suppression function α(ρ) is developed in §9.2.



Varying S(σ) with respect to λ yields the Euler–Lagrange condition:



        δS/δλ = 0  ⟹  ∇_μσ ∇^μσ + f(σ) = 0



That is, ∇_μσ ∇^μσ = −f(σ), the norm condition of §6.3, arising here as a necessary condition for

stationarity of S(σ). Varying with respect to σ yields the propagation equation ∇_μ(λ∇^μσ) =

½λf′(σ), which transports λ along the generation flow. Varying with respect to g^{μν} recovers

G_{μν} = 8πG T_{μν} together with the λ-dependent term of Proposition 17.7, which vanishes

identically for the configuration λ = 0 adopted in §6.9.



The variational formulation shows how the norm condition enters a standard action principle: it is

what stationarity with respect to the multiplier requires. It does not by itself explain why σ

should obey that condition; the reason is geometric, since cosmological time satisfies it (§6.3,

Theorem 17.4). The formal statement is given in Proposition 17.7 (§17).



The restriction of the integration domain to M(σ) is the formal expression of the framework’s

central ontological commitment — not merely a heuristic convenience. In the standard block universe

interpretation, the action is implicitly integrated over the entire four-dimensional manifold,

treating all events as equally real elements of the variational principle. By explicitly limiting

the action to M(σ), CTGP asserts that future spacetime regions do not contribute to the dynamical

definition of the theory at stage σ. The future is not simply unknown; it is not part of the domain

of the physical laws that generate the present. This transforms the interpretation from a passive

description of a pre-existing structure to an active generation of new structure. The Euler–Lagrange

equations derived from this action are therefore not constraints on a static block, but rules by

which each successor state is generated from the present one. The domain of the action, M(σ), is the

formal representation of the history generated up to the present stage, and the field equations are

defined only over that domain. Because Euler–Lagrange equations are local, this restriction does not

alter the field equations at any point of M(σ); the distinction it draws concerns the domain over

which the laws are defined, not their local form. A completed block would serve as the domain for an

action defined over the whole of M; the CTGP action has no such domain. This distinction is

formalized in Theorem 17.9 (§17).



9.2 Domain of Validity and the Extended Action

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The effective action S(σ) of §9.1 is valid within a precisely specified domain: the emergent

geometric regime, where ρ ≪ ρ_P (the Planck density), and the smooth Lorentzian manifold (M, g_{μν})

is a valid continuum approximation. Outside this domain — specifically in the pre-geometric regime

where ρ ∼ ρ_P — the continuum integral, the metric volume element √(−g) d⁴x, and the Ricci scalar R

are themselves emergent structures that cannot be taken as primitive inputs to the variational

principle. The two regimes and their respective formal machinery are distinguished as follows:



• Pre-geometric regime (ρ ∼ ρ_P):  σ is primitive; no metric assumed; no continuum action defined;

  causal ordering is the operative structure.

• Emergent geometric regime (ρ ≪ ρ_P):  σ represented by cosmological time; metric available; S(σ)

  applies.



The transition between regimes is not a discontinuity but a crossover parameterized by the

dimensionless ratio ρ/ρ_P. This crossover can be represented in the effective action by introducing

a density-dependent suppression factor α(ρ) on the GR Lagrangian:



        S_{ext}(σ) = ∫_{M(σ)} √(−g) [ α(ρ) L_{GR} + λ(∇_μσ ∇^μσ + f(σ)) ] d⁴x



        α(ρ) = 1 / (1 + (ρ/ρ_P)^n),  n ≥ 1



The suppression function α(ρ) satisfies: α → 1 as ρ/ρ_P → 0 (low-energy limit, GR fully restored),

and α → 0 as ρ/ρ_P → ∞ (Planck regime, GR suppressed). The σ-constraint sector λ(∇_μσ ∇^μσ + f(σ))

is retained at all densities, reflecting the fact that the generative ordering structure of σ is

active across both regimes — it is never suppressed, because it is the structure from which the

geometric regime itself emerges. The exponent n controls the sharpness of the transition; n = 2

gives a smooth crossover centered at ρ = ρ_P.



An important ontological clarification is required by S_{ext}(σ): the metric g_{μν} still appears in

the extended action through √(−g) and the σ-constraint sector. This creates a choice between two

interpretations of the metric’s status in the pre-classical regime. Under the emergent-metric

reading (consistent with §10.3), g_{μν} in S_{ext}(σ) is to be understood as a continuum

approximation that becomes progressively less valid near ρ_P; the action itself is correspondingly

an effective field theory expression whose UV completion lies in the pre-geometric structure. Under

the constrained-metric reading, g_{μν} remains a fundamental but dynamically unconstrained quantity

whose constraints emerge alongside GR as α(ρ) → 1. CTGP adopts the emergent-metric reading as

primary (Emergent Metric Principle, §10.3), treating S_{ext}(σ) as valid only where the continuum

approximation holds. The extended action therefore serves a specific formal function: it models the

crossover continuously rather than imposing a sharp regime boundary, and it identifies α(ρ) as the

natural emergence function for GR within the CTGP framework. S_{ext}(σ) is the candidate effective

action for the crossover regime; its pre-geometric limit is not fully specified by the continuum

formalism alone, and remains subject to the Scope of the Research Program principle of §10.4.



9.3 Cosmological Foliation and the CMB Frame

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



In homogeneous, isotropic cosmology, the FLRW metric provides a preferred foliation by cosmic time

t:



        ds² = −dt² + a(t)² dΩ_k²



This does not violate local Lorentz invariance; rather, it reflects a physical symmetry of our

universe's matter distribution. The CMB frame singles out a preferred rest frame not as a kinematic

artifact but as a physical fact about the distribution of matter and energy. CTGP's global present

Σ_σ is defined by cosmological time, and on large scales it coincides with this frame, providing a

non-absolute but physically grounded global 'now.' Different observers need not synchronize their

local frames; they share the cosmological foliation without needing operational access to it.



[FIGURE: Figure 5]

  Figure 5. FLRW foliation: surfaces of constant cosmic time t, with comoving worldlines diverging

  as the scale factor a(t) grows. The comoving worldlines are the maximizing geodesics that define

  cosmological time and provide the physical basis for CTGP’s global present.



9.3.1 Emergent Cosmological Foliation



A clarification bears on one of the most persistent objections: the charge that CTGP introduces a

preferred frame. The correct response is that CTGP does not introduce a preferred frame — it

identifies the cosmological foliation as an emergent physical structure generated by the large-scale

matter distribution.



The logical chain that establishes this is as follows:



        Einstein equations are foliation-neutral → the actual matter distribution fixes the metric → the metric fixes cosmological time τ → on large scales, the level sets of τ coincide with the CMB rest frame



CTGP does not use the cosmological foliation as an external input. Rather, CTGP identifies the

cosmological foliation as an emergent physical structure generated by the large-scale matter

distribution. This framing aligns CTGP with spontaneous symmetry breaking, a mechanism physicists

already accept throughout physics: a rotationally symmetric Lagrangian can produce a ground state

that breaks rotational symmetry, with the symmetry-breaking direction selected by the physical

configuration rather than by the Lagrangian itself. The CMB rest frame is precisely analogous: the

Einstein equations are foliation-neutral, but the physical solution — a universe filled with matter
