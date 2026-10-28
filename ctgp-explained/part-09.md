# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 09 of 25 (1,834 words)

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



The kinematic structure of CTGP — a foliation by the level sets of cosmological time, aligned with

matter in cosmology — rests on established results: the causal-structure theorems of Appendix B, the

cosmological time function, and the observed CMB rest frame. The generation law is the one element

that could in principle carry new physics: the function f that fixes how fast σ advances.



This freedom is narrower than it appears. Any generation law in which f carries spatial matter

dependence gives the generation flow an acceleration away from free fall, a_μ = −D_μ ln √f

(Proposition 11.1). That acceleration destroys alignment with matter and, in the presence of

structure, the timelike character of the foliation; stable soft completions fare no better (§11.3).

Within the local, stable classes analyzed in §11, the viable generation laws are those of the form f

= f(σ), equivalent to a relabeling of cosmological time: the generation rate may vary with cosmic

epoch but not across space. The choice of generation law is therefore not confined to Layer 3: it is

constrained by the Layer 2 requirement that the present be a well-defined future Cauchy surface

aligned with matter.



6.12 Succession of Hypersurfaces

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The ontological dynamic is expressed by the succession relation. In the emergent geometric regime,

this takes the form of successive spacelike hypersurfaces; in the pre-geometric regime, it should be

understood as successive generative stages of the causal ordering:



        Σ_σ → Σ_{σ+Δσ}



Each transition is governed by GR's field equations applied to data on Σ_σ without reference to any

data at σ′ > σ; where Σ_σ has corners, the equations are applied in a smooth foliation covering the

same region, which leaves the development, and therefore which events are co-present, unchanged

(§8). This succession is a real unfolding, not a representational one, and on CTGP it is what the

lived flow of time tracks.



[FIGURE: Figure 3] Figure 3. Hypersurface generation: successive level sets Σ_σ → Σ_{σ+Δσ} produced

    from data on the present edge by lawful dynamics. The lapse of the cosmological foliation is

    constant on each level set, so equal steps in σ correspond to equal proper time along the

    maximizing geodesics; systems moving relative to them, including clocks at rest in gravitational

    wells, accumulate less.



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



The dynamical equations and constraints provide a natural slice-to-slice picture. CTGP maps this to

an ontological claim: Σ_σ is literally produced from Σ_{σ−Δσ} by lawful dynamics, without reference

to a pre-existing future slice. The ADM decomposition presupposes a smooth foliation. The

cosmological foliation is smooth wherever its maximizing geodesics form a single-valued congruence;

where they cross and the level sets acquire corners, the dynamics are computed in a smooth foliation

instead, which always exists in a globally hyperbolic spacetime (Bernal and Sánchez 2003, 2005).

Because the field equations are covariant, the development they determine does not depend on the

slicing used to compute it, so this changes nothing about which events are co-present: the level

sets of τ fix co-presence, and the smooth foliation is a computational device. This concerns

computing the development. The stronger claim that the data on a cornered level set by themselves

determine what comes after it would require an initial-value formulation for nonsmooth

hypersurfaces, which the standard theorems do not supply (Proposition 17.2).



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

τ), and √(−g) d⁴x is the invariant volume element. The integration is restricted to M(σ), so no

future region enters the action. The term λ(∇_μσ ∇^μσ + f(σ)) enforces the norm condition on σ.

Variation with respect to the fields yields the constraint and propagation relations below.



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
