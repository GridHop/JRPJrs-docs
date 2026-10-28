# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 08 of 25 (1,819 words)

time fixes it uniquely up to relabeling; (ii) “why not any scalar” fails because most scalars are

not monotone on all future-directed causal curves and do not define Cauchy foliations; (iii) “growth

is gauge” fails because the underlying ordering derives from the causal structure of spacetime

itself, not from a choice of coordinates.



6.8 Ontological vs. Dynamical Status of σ

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



A potential source of confusion about CTGP’s theoretical commitments concerns the status of σ: is it

a new dynamical field, a derived scalar, and does it carry independent energy? This subsection

addresses these questions explicitly.



Under the pre-geometric interpretation developed in §10.3, σ plays three distinct roles that should

be explicitly distinguished: (1) as a generation parameter, it labels the sequence of causal stages

that constitute the generated history M(σ), a formal representation rather than an accumulating

region; (2) as an ordering structure, it induces the causal ordering whose continuum limit admits

foliation by generated hypersurfaces; and (3) as a minimal lawful substrate, the primitive

generative ordering represented by σ constitutes the minimal lawful structure required for the

succession of physical states. In the emergent geometric regime, this primitive ordering admits

representation as the σ field, but the field representation is not fundamental.



This three-role structure elevates σ beyond a bookkeeping parameter. The deepest ontological

commitment of CTGP is not that a fundamental scalar field generates reality, but that primitive

generative ordering and its associated causal relations constitute the minimal lawful structure

required for the succession of physical states and for the emergence of effective physical laws.



At the level of continuum dynamics, σ is fixed by the geometry: cosmological time is a functional of

the metric, so σ carries no initial data of its own. The action of §9.1 encodes σ through a Lagrange

multiplier λ enforcing the norm condition ∇_μσ ∇^μσ = −f(σ). The multiplier sector is not inert in

general: as in mimetic gravity, λ contributes a pressureless, dust-like stress-energy whose

amplitude is set by initial data (§6.9). With λ = 0 on an initial surface, it vanishes identically

and the Einstein equations are unmodified. This is the configuration CTGP adopts, because the Layer

2 present is defined by cosmological time without reference to λ.



This status is precisely analogous to several well-understood scalars in GR and thermodynamics.

Proper time τ along a worldline is a derived scalar fixed by the metric and the worldline’s tangent

vector; it introduces no new degrees of freedom and is entirely determined by the existing dynamical

content of GR. Entropy production scalars in relativistic thermodynamics are similarly secondary:

they are constructed from the stress-energy tensor and thermodynamic state variables, track the

causal direction of physical processes, and do not add new fields to the theory. York time in

canonical gravity — the trace of the extrinsic curvature K, used as an intrinsic time variable in

certain foliations — provides perhaps the closest structural analog: it is extracted from the

existing ADM variables, increases monotonically in expanding cosmologies, and defines a foliation

without being an independent physical degree of freedom. σ plays an exactly analogous role: it is a

physically calibrated member of the class of time functions that every globally hyperbolic spacetime

possesses, selected by maximal elapsed proper time rather than stipulated as an independent field,

and smooth wherever τ is differentiable.



The concern that σ “secretly introduces a new field that modifies GR” therefore misreads the

formalism. A new field modifies GR by adding independent degrees of freedom whose dynamics can

diverge from those of the Einstein–matter system; scalar–tensor theories (Brans–Dicke), f(R)

gravity, and quintessence models all do this. σ does not: it is fixed by the metric through

cosmological time, and with λ = 0 the constraint sector carries no stress-energy. CTGP’s ontological

claim — that σ indexes genuine spacetime generation — is interpretive, not dynamical. The physics is

unmodified; the ontological reading of the physics is what CTGP proposes.



In summary, with λ = 0 (§6.9) the continuum generation parameter introduces no new propagating

degrees of freedom and modifies no gravitational dynamics. Physical hypotheses that would give σ

dynamics of its own — density-dependent generation rates and soft completions of the norm condition

— are analyzed in §11; none survives the consistency requirements while producing an observable

effect.



Covariance and compatibility with General Relativity. All quantities introduced in the CTGP

framework are constructed from the metric, its causal structure, and scalar invariants.

Consequently, the theory remains invariant under arbitrary spacetime diffeomorphisms. The Einstein

field equations G_{μν} = 8πG T_{μν} are unchanged (§9.1), and the generative dynamics operate only

at the level of the ontological realization of spacetime events rather than modifying the local

gravitational field equations. In this sense CTGP extends the interpretation of the temporal

progression of spacetime without altering the empirically verified structure of General Relativity.

Within the emergent geometric regime, σ is represented by cosmological time, a geometric scalar, and

therefore transforms covariantly under diffeomorphisms. Fundamentally, however, σ is interpreted as

a pre-geometric generative ordering parameter rather than as a scalar field defined on a

pre-existing manifold. This covariance is guaranteed by construction and does not require additional

assumptions.



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

are the level sets of τ, which are future Cauchy surfaces (Theorem 17.4), and every admissible

generation parameter has the form σ = F(τ) with F strictly increasing. No choice of coordinates,

observers, or matter calibration enters, because τ is defined from the causal and metric structure

alone and is preserved by isometries (Proposition 17.8).



The “arbitrary scalar” objection therefore does not apply. Of the many time functions that a

globally hyperbolic spacetime admits, the generative present is the unique one defined by maximal

elapsed proper time, up to relabeling of its values. The logical chain is: causal geometry →

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

Galloway, and Howard therefore carries over on each side, and the level sets of τ_S are future

(respectively past) Cauchy surfaces (Proposition 17.23).



The settled case. In an exact FLRW universe with a single bounce, the surface at the moment of the

bounce — where the scale factor stops decreasing and begins increasing, ȧ = 0 — has zero mean

curvature, is unique, and is a Cauchy surface. Taking S to be this surface, τ_S is cosmic time

measured from the bounce, and the generative present is well defined through the bounce with no

averaging prescription. The stages before the bounce are simply earlier stages, generated and ceased
