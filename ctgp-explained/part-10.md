# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 10 of 26 (1,800 words)

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

of the physical laws that generate the present. On CTGP's reading, the Euler–Lagrange equations

derived from this action are accordingly not constraints on a static block but rules by which each

successor state is generated from the present one. The action expresses this reading; it does not

establish it. Because the variation holds M(σ) and its boundary fixed (Proposition 17.7), the action

implements the norm condition and the field equations within a domain that is already specified. It

does not select the boundary Σ_σ, which cosmological time fixes (§6.1), and it does not derive the

advance of the present, which is CTGP's ontological posit (§7). The domain of the action, M(σ), is

the formal representation of the history generated up to the present stage, and the field equations

are defined only over that domain. Because Euler–Lagrange equations are local, this restriction does

not alter the field equations at any point of M(σ); the distinction it draws concerns the domain

over which the laws are defined, not their local form. A completed block would serve as the domain

for an action defined over the whole of M; the CTGP action has no such domain. This distinction is

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

identifies the cosmological foliation as an emergent physical structure: the large-scale matter

distribution shapes the spacetime geometry, and the geometry fixes the foliation.



The logical chain that establishes this is as follows:



        Einstein equations are foliation-neutral → the actual matter distribution fixes the metric → the metric fixes cosmological time τ → on large scales, the level sets of τ coincide with the CMB rest frame



CTGP does not use the cosmological foliation as an external input. Rather, CTGP identifies the

cosmological foliation as an emergent feature of the geometry that the large-scale matter

distribution produces. This framing aligns CTGP with spontaneous symmetry breaking, a mechanism

physicists already accept throughout physics: a rotationally symmetric Lagrangian can produce a

ground state that breaks rotational symmetry, with the symmetry-breaking direction selected by the

physical configuration rather than by the Lagrangian itself. The CMB rest frame is precisely

analogous: the Einstein equations are foliation-neutral, but the physical solution — a universe

filled with matter in a particular configuration — fixes a metric whose cosmological time is, on

large scales, the CMB rest frame.



9.4 Cosmological Simultaneity and Relativistic Locality

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



CTGP distinguishes three senses of “present” that are often conflated in objections to the

framework.



    Local physical present: what an observer experiences at their worldline. This is the

    phenomenological present, dependent on local physical processes and subject to the usual

    relativistic effects of time dilation and gravitational redshift. The local present is the

    observer’s own portion of the ontological present, not a separate present.



    Cosmological present: the current level set of cosmological time τ. The foliation by these level

    sets is fixed by the spacetime geometry; the large-scale matter distribution of the universe

    shapes that geometry through the Einstein equations, and so shapes the foliation without

    defining it (§6.3). Observationally, the foliation is approximated by the CMB rest frame. This

    is a physically grounded quantity, not an observer-dependent one: any observer can in principle

    determine the CMB frame and locate themselves within it.



    Ontological present: the boundary between the generated domain M(σ) and the ungenerated future.

    This is the active edge at which new hypersurfaces are produced, parameterized by σ.



CTGP’s present edge Σ_σ is identified with the cosmological present rather than with Newtonian

absolute simultaneity or with any particular observer’s local present. Consequently, CTGP preserves

local Lorentz invariance while maintaining a physically motivated global generation parameter. The

resulting “universal tick” is therefore not a universal clock visible identically to every observer

but a cosmologically grounded ordering relation associated with the generation of new hypersurfaces.

Nor does “tick” imply discreteness: the ordering is continuous, and no gap separates the level sets

it orders (§3.2). Much confusion disappears once these three senses of present are kept distinct:

local simultaneity is observer-dependent and Lorentz-relative; cosmological simultaneity is fixed by

the geometry that the matter distribution shapes; ontological simultaneity concerns what has been

generated and what has not.



9.4.1 Co-presence, Cosmic Time, and Synchronization



Co-presence is not a relation added to existence but a consequence of it. Since only the present

exists — earlier stages have ceased to exist and later ones are ungenerated — everything that exists

belongs to a single generative stage. This is why CTGP requires a global foliation: existence cannot

be frame-relative, so there must be one fact about which events constitute the present. Cosmological

time specifies which surfaces these are (§6.1).



Membership in Σ_σ is co-presence, and because Σ_σ is a level set of the generation parameter, co-

presence is equality of σ: two co-present events occur at the same cosmological generation stage

because they carry the same value of σ. This is not a correlation between two facts but a single

fact stated twice. In the emergent geometric regime, where σ is a monotone relabeling of

cosmological time (Postulate 3), this is what “same cosmic time” refers to; prior to geometric

emergence σ remains an ordering parameter and the equality still holds, without presupposing proper

time. What does not follow from equality of σ is equality of proper time, which differs between

worldlines under relative motion and differing gravitational conditions; synchronization in any

operational sense, since co-present events may exchange no timing signals and need not be in causal
