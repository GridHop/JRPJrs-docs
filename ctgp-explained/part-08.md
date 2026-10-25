# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 08 of 25 (1,791 words)

at the level of the ontological realization of spacetime events rather than modifying the local

gravitational field equations. In this sense CTGP extends the interpretation of spacetime evolution

without altering the empirically verified structure of General Relativity. Within the emergent

geometric regime, σ is represented by cosmological time, a geometric scalar, and therefore

transforms covariantly under diffeomorphisms. Fundamentally, however, σ is interpreted as a pre-

geometric generative ordering parameter rather than as a scalar field defined on a pre-existing

manifold. This covariance is guaranteed by construction and does not require additional assumptions.



6.9 Status of the Lagrange Multiplier λ

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The action of §9.1 contains a Lagrange multiplier λ that enforces the norm condition



        ∇_μσ ∇^μσ = −f(σ).



Variation with respect to σ gives the propagation equation



        ∇_μ(λ ∇^μσ) = ½ λ f′(σ),



which is linear and homogeneous in λ and reduces to a conservation law for the current λ∇^μσ when f

is constant. Given σ, it transports λ along the generation flow from its value on an initial

surface.



The multiplier is physically meaningful. Variation with respect to the metric shows that, on the

constraint surface, λ contributes the stress-energy T^{(σ)}_{μν} = 2λ∇_μσ∇_νσ (Proposition 17.7): a

pressureless fluid moving along the generation flow, with energy density proportional to λf. This is

the structure of mimetic gravity (Chamseddine and Mukhanov 2013), in which such a component mimics

cold dark matter; like any pressureless fluid, it develops caustics where its flow lines cross.



CTGP sets λ = 0 on an initial surface. The propagation equation then keeps λ = 0 everywhere, the

constraint sector contributes no stress-energy, and the Einstein–matter system is exactly that of

general relativity. This choice reflects the division of labor in the framework: the Layer 2 present

is defined by cosmological time (§6.1) and needs no dynamical support from λ. A nonzero λ would be a

Layer 3 hypothesis — a dark-matter-like component carried by the generation flow — degenerate at the

background level with ordinary cold dark matter and subject to the caustic problem discussed in

§11.4. CTGP therefore adopts none of the phenomenology associated with mimetic gravity: no dust-like

component, no modification of the expansion history, and no new propagating degree of freedom. The

resemblance is structural only, and it is confined to the form of the constraint.



6.10 Non-Arbitrariness of the Generative Present

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Theorem (Uniqueness of the Cosmological-Time Foliation). Let (M, g) be a spacetime with regular

cosmological time τ. Then the foliation by the level sets of τ is uniquely determined: its leaves

are the level sets of τ, which are Cauchy surfaces (Theorem 17.4), and every admissible generation

parameter has the form σ = F(τ) with F strictly increasing. No choice of coordinates, observers, or

matter calibration enters, because τ is defined from the causal and metric structure alone and is

preserved by isometries (Proposition 17.8).



The “arbitrary scalar” objection therefore does not apply. Of the many Cauchy time functions whose

existence the Bernal–Sánchez theorems guarantee, the generative present is the unique one defined by

maximal elapsed proper time, up to relabeling of its values. The logical chain is: causal geometry →

cosmological time → a distinguished foliation → CTGP’s interpretation of that foliation as

ontological co-presence. The first three links are results of general relativity; the last is CTGP’s

interpretive thesis, not a theorem. Geometric naturalness does not by itself confer ontological

privilege: the geometry makes the identification non-arbitrary, sparing the presentist a choice

among admissible foliations by fiat, but the identification itself is a primitive posit of the

ontology and one of its costs (§16). The theorem’s scope is set by its hypothesis. The present

formulation is a big-bang-origin formulation: regular cosmological time requires a past boundary at

finite proper time, and past-eternal, bouncing, cyclic, and emergent cosmologies lie outside its

scope. §6.10.1 extends the construction to universes with a single uniform bounce; the remaining

cases would require a further generalization. This limitation concerns the continuum representative,

not the ontology. Cosmological time is CTGP’s realization of the primitive generative ordering in

the emergent geometric regime (§10.3), not the ultimate source of that ordering; a generalized

construction would replace it while leaving the ordering itself intact.



6.10.1 Extension Through a Bounce



Cosmological time fails in a bouncing universe without a beginning for a precise reason. (A bounce

whose contracting phase itself began at an earlier singularity still has regular cosmological time,

measured from that singularity.) If the contracting phase extends indefinitely into the past, causal

curves continue through the bounce instead of ending at a past boundary, so τ is infinite everywhere

and both regularity conditions of Theorem 17.4 fail. The construction can nevertheless be extended

when the spacetime supplies a distinguished Cauchy surface to play the role of the initial

singularity.



Definition (Surface-relative time). Let S be a spacelike Cauchy surface. For an event p, let



        τ_S(p) = ± sup { L(γ) : γ a causal curve between S and p },  τ_S = 0 on S,



with the positive sign when p lies to the future of S and the negative sign when it lies to the

past. The sign is fixed by the spacetime’s time orientation, not by an additional convention. On

each side of S, τ_S is cosmological time with S in place of the initial singularity. The one-sided

analogues of the regularity conditions of Theorem 17.4 — τ_S finite, and τ_S → 0 along every causal

curve approaching S — are not additional physical assumptions: in a globally hyperbolic spacetime

they follow from S being a Cauchy surface, since every past-inextendible causal curve on the future

side reaches S and the region between S and any event is compact. The argument of Andersson,

Galloway, and Howard therefore carries over on each side, and the level sets of τ_S are Cauchy

surfaces (Proposition 17.23).



The settled case. In an exact FLRW universe with a single bounce, the surface at the moment of the

bounce — where the scale factor stops decreasing and begins increasing, ȧ = 0 — has zero mean

curvature, is unique, and is a Cauchy surface. Taking S to be this surface, τ_S is cosmic time

measured from the bounce, and the generative present is well defined through the bounce with no

averaging prescription. The stages before the bounce are simply earlier stages, generated and ceased

like any past stage. Such a universe has no first stage; CTGP’s ontology and its tense semantics

(Definition 17.20) do not require the sequence of past stages to be finite.



Scope. Three limits fix the scope of the extension. First, S is an input rather than an output: the

construction presupposes a distinguished Cauchy surface instead of deriving one from the causal

structure alone, as cosmological time does in the big-bang case. Second, in a non-uniform bounce the

regions of zero mean curvature need not join into a single surface, and whether a unique maximal

Cauchy surface exists is open; the existence and uniqueness theorems for such surfaces assume

conditions — compact Cauchy surfaces, symmetries, or energy conditions — that a bounce typically

violates. Third, a cyclic universe has many surfaces of zero mean curvature, and an emergent

universe with an Einstein-static past has zero mean curvature on every slice, so neither supplies a

distinguished S. These cases remain outside the present continuum representative. As before, the

limitation concerns the representative, not the ontology: replacing τ by τ_S where S exists is a

change of representative, not of the Layer 2 claim.



6.11 Admissible Generation Laws

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The kinematic structure of CTGP — a Cauchy foliation by the level sets of cosmological time, aligned

with matter in cosmology — rests on established results: the causal-structure theorems of Appendix

B, the cosmological time function, and the observed CMB rest frame. The generation law is the one

element that could in principle carry new physics: the function f that fixes how fast σ advances.



This freedom is narrower than it appears. Any generation law in which f carries spatial matter

dependence gives the generation flow an acceleration away from free fall, a_μ = −D_μ ln √f

(Proposition 11.1). That acceleration destroys alignment with matter and, in the presence of

structure, the timelike character of the foliation; stable soft completions fare no better (§11.3).

Within the local, stable classes analyzed in §11, the viable generation laws are those of the form f

= f(σ), equivalent to a relabeling of cosmological time: the generation rate may vary with cosmic

epoch but not across space. The choice of generation law is therefore not confined to Layer 3: it is

constrained by the Layer 2 requirement that the present be a well-defined Cauchy surface aligned

with matter.



6.12 Succession of Hypersurfaces

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The ontological dynamic is expressed by the succession relation. In the emergent geometric regime,

this takes the form of successive spacelike hypersurfaces; in the pre-geometric regime, it should be

understood as successive generative stages of the causal ordering:



        Σ_σ → Σ_{σ+Δσ}



Each transition is governed by GR's evolution equations applied to data on Σ_σ without reference to

any data at σ′ > σ. This succession produces the 'lived flow' of time as a real unfolding, not a

representational one.



[FIGURE: Figure 3]

    Figure 3. Hypersurface generation: successive level sets Σ_σ → Σ_{σ+Δσ} produced by lawful

  evolution of data on the present edge. The lapse of the cosmological foliation is constant on each

  level set, so equal steps in σ correspond to equal proper time along the maximizing geodesics;

  systems moving relative to them, including clocks at rest in gravitational wells, accumulate less.



----------------------------------------------------------------------------------------------------

7. General Relativity as Initial-Value Generation

----------------------------------------------------------------------------------------------------



Einstein's equations can be written as a well-posed initial-value problem (under standard

conditions). Given Cauchy data on Σ_σ, the evolution equations determine a unique development — up

to diffeomorphism — in a neighborhood of Σ_σ, without specifying future boundary data. CTGP

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
