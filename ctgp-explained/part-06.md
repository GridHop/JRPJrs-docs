# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 06 of 25 (1,829 words)

closed timelike curves and laws that allow them. The two views therefore do not make the same claim

about global hyperbolicity, even though both are consistent with the observations to date: CTGP

takes a risk that eternalism does not, which is the same asymmetry that underlies the generability

constraint (§12.2).



Locating the present without the future. Cosmological time is defined on a spacetime (M, g), and the

theorem that its level sets are future Cauchy surfaces concerns the whole manifold. It might

therefore seem that CTGP needs the completed block to say which surface is present. It does not. By

definition, τ(p) is the supremum of the lengths of past-directed causal curves from p, so its value

at p depends only on the causal past J⁻(p); the regularity conditions are likewise past-directed.

Whether an event lies on Σ_σ is therefore fixed by its past alone, and no future region enters. What

makes the lengths of those past curves well defined, although the past does not exist, is what

grounds every past truth (§5.2): τ is itself a past-tensed magnitude of the present, fixed by the

present’s having been preceded by causal histories of those lengths. Global statements about the

full manifold belong to the mathematical representation of the history as it would be generated;

they show that the construction is well behaved, and they do not ground which slice is present. Nor

does locating later stages require anything past-tensed beyond a label. For an event q with τ(q) ≥

a, every past-inextendible causal curve from q meets S_a, and τ(q) = a + d(S_a, q), where d(S_a, q)

is the supremum of the lengths of causal curves from S_a to q. Splitting each past-directed causal

curve from q where it crosses S_a gives one inequality; joining a nearly maximal curve from S_a to q

with nearly maximal past-directed curves from its starting point gives the other. The successor

level sets are therefore the surfaces of constant maximal proper-time separation from the present

level set, fixed by the geometry of its future domain of dependence. The past enters only through

the value a, and since only the level sets are physical, that value is a labeling convention

(Appendix A.3.1).



Clarification on process and representation. Neither Σ_σ nor the union M(σ) should be read as

implying that reality consists of a sequence of discrete, ontologically fundamental temporal slices.

Σ_σ is a mathematical representation of a physical reality in continuous temporal and generative

progression, not a freestanding entity that reality simply “is.” The hypersurfaces function

analogously to the instantaneous configurations used in classical mechanics or field theory: useful

analytical cross-sections of a continuous process, not independently existing states stacked one

against the next. Correspondingly, M(σ) = ⋃_{σ′<σ} Σ_{σ′} is a mathematical reconstruction of

generated history and should not be interpreted as an ontological accumulation of independently

existing temporal slices; it represents a single, continuous causal-temporal process viewed through

a foliation-based description, not a growing pile of spacetime sheets. Reality itself is the

uninterrupted lawful progression connecting these representations — the succession of hypersurfaces

describes one continuous process of becoming, not a series of separately existing states.



Geometric interpretation of the growth hypersurface. In the emergent geometric regime, each

hypersurface Σ_σ is defined as a level set of the scalar field σ(x): Σ_σ = {x ∈ M | σ(x) = const}.

Because σ admits representation as a scalar field in this regime, this construction is covariant

under diffeomorphisms. The hypersurfaces therefore represent a physical ordering of generative

events rather than a coordinate-dependent slicing, and no preferred coordinate frame is introduced;

the foliation is fixed by the level sets of cosmological time, of which σ is a relabeling, and

involves no additional field dynamics. To ensure causal consistency, the gradient ∇_μσ is required

to remain timelike: ∇_μσ ∇^μσ < 0. This condition — guaranteed wherever τ is differentiable, since

∇_μτ is then a unit timelike covector — ensures that the generative ordering corresponds to a

physically admissible temporal direction and that Σ_σ is spacelike wherever τ is differentiable.

CTGP does not claim that general relativity singles out a unique foliation in every spacetime. It

claims that cosmological time, defined from the causal and metric structure alone, supplies a

physically distinguished foliation wherever it is regular, and that in our universe this foliation

approximately coincides, on large scales, with the rest frame of the cosmic matter distribution. The

construction does not presuppose the idealized fundamental observers of standard cosmology: the

maximizing geodesics of cosmological time play the role those observers would play, and they are

fixed by the geometry wherever cosmological time is regular, however lumpy the matter distribution.



This encodes CTGP’s generative temporal asymmetry: future hypersurfaces Σ_{σ′>σ} are excluded from

M(σ). Figure 2 illustrates this structure.



[FIGURE: Figure 2]

  Figure 2. The generated domain M(σ). The present edge Σ_σ is the active boundary of generation;

  earlier stages Σ_{σ′} (σ′ < σ) constitute the formal history M(σ), and future stages are not part

  of the domain. Lines are schematic level sets of σ, not independently existing slices.



6.2 Causal-Theoretic Foundation of the Generation Parameter

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



CTGP introduces a scalar parameter σ intended to index the growth of the generated spacetime domain

M(σ). A natural concern is that any such parameter appears ad hoc: why should the ordering of

ontological generation be determined by a particular scalar rather than another curvature invariant

or entropy measure? A deeper answer emerges from the causal structure of relativistic spacetime

itself.



The starting point is a result due to Hawking, King, and McCarthy (1976), which suggests that in

suitably well-behaved relativistic spacetimes the chronological relation I⁺(p) — the set of events

reachable from p by future-directed timelike curves — determines the conformal structure of the

spacetime metric. Once the chronological ordering is known, the topology and light-cone structure

can be reconstructed uniquely up to an overall conformal factor. Malament (1977) subsequently

strengthened this result by indicating that the causal ordering relation alone suffices to determine

the conformal metric structure under mild conditions. The philosophical significance is direct:

temporal precedence in relativistic spacetime is not a coordinate artifact but is already encoded in

the causal structure itself. CTGP therefore does not introduce σ as an external time parameter

imposed upon GR. Rather, σ is understood as a physically selected refinement of the causal ordering

already implicit in globally hyperbolic spacetime. Most scalars — Ricci scalar, Weyl invariants,

Kretschmann scalar — cannot serve this role because they do not increase monotonically along every

future-directed causal curve and do not define Cauchy foliations; they fail the most basic

requirement of a temporal ordering parameter.



From the causal ordering, a continuous global time function can be constructed via Geroch’s

volume-time method. Let J⁻(p) and J⁺(p) denote the causal past and future of an event p, and let μ

be an invariant measure on spacetime. Quantities such as t⁻(p) = μ(J⁻(p)) increase strictly along

every future-directed causal curve in any distinguishing spacetime and, in globally hyperbolic

spacetimes, define a continuous time function (Geroch 1970), yielding a continuous causal ordering

parameter. This establishes that relativistic spacetime already contains the ordering CTGP needs,

independently of any interpretive choice.



However, a continuous causal ordering is not yet sufficient for the dynamics, whose initial-value

formulation is posed on smooth spacelike hypersurfaces. This refinement is provided by the

Bernal–Sánchez theorems. In any globally hyperbolic spacetime (M, g), there exists a smooth temporal

function t whose gradient is everywhere timelike, and whose level sets Σ_t = const are smooth

spacelike Cauchy hypersurfaces, with M ≅ ℝ × Σ globally (Bernal and Sánchez 2003, 2005). The

existence of time functions of this kind is therefore not an additional physical postulate but a

consequence of the causal geometry of globally hyperbolic spacetimes. The logical structure is:

causal ordering exists (HKM, Malament) → a continuous time function exists (Geroch) → a smooth

Cauchy temporal function exists (Bernal–Sánchez) → CTGP selects, within the class of time functions,

the one fixed by cosmological time (§6.3), which is smooth wherever τ is differentiable (§6.1).

Where it is not, the two results divide the labor: the level sets of τ fix which events are

co-present, and a smooth Cauchy temporal function of the kind Bernal and Sánchez guarantee supplies

hypersurfaces on which the dynamics can be computed (§8).



In the pre-geometric regime, Σ_σ denotes a generation stage within the causal ordering induced by σ.

Only in the emergent geometric regime does Σ_σ admit representation as a smooth spacelike

hypersurface.



Two further lines of motivation indicate that the cosmological-time foliation is not an arbitrary

representative of this class. First, in FLRW cosmologies the level sets of cosmological time

coincide with the rest frame of the matter flow, along which entropy production supplies a natural

thermodynamic clock. This is a suggestive coincidence in the symmetric case, not a derivation of σ

from entropy production. Second, in a discrete quantum-gravity setting, σ admits a possible

realization within causal-set approaches, where growth dynamics suggest a natural analogue of

spacetime generation (Rideout and Sorkin 2000): one possible interpretation is that σ corresponds,

in an appropriate continuum approximation, to an averaged measure of generated causal structure.

CTGP does not presently provide a rigorous derivation of this correspondence and therefore treats it

as a motivating analogy rather than a proven result. Importantly, causal-set approaches represent

one possible discrete realization of CTGP’s more general continuous generative-flow ontology; CTGP’s

continuum structure is the generation flow ∇_μσ, and discrete models provide compatible but

non-foundational instantiations. These two independent lines of motivation suggest possible deeper

foundations for σ, but neither presently constitutes a derivation of the CTGP formalism.



6.3 The Generation Parameter as Cosmological Time

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The causal-structure results of HKM, Malament, Geroch, and Bernal–Sánchez jointly establish three

facts: that relativistic spacetime possesses an objective causal ordering not reducible to

coordinate choice; that this ordering can be represented by a continuous global time function; and

that in globally hyperbolic spacetimes it can be smoothed into a temporal function whose level sets

are spacelike Cauchy hypersurfaces. Geometry alone determines the existence of admissible temporal

orderings, though not yet their physical interpretation. CTGP resolves that remaining freedom

through cosmological time, which is fixed by the causal and metric structure alone. In FLRW its

level sets are orthogonal to the comoving matter congruence; beyond FLRW the alignment is

approximate (see *Alignment with matter* below). The matter frame is where the present is realized,

not what defines it. These reconstruction results are additionally strengthened by the pre-geometric

ontology of §10.3: since causal structure determines most geometric information up to conformal

factors, CTGP’s commitment to fundamental causal ordering naturally supports the claim that geometry

is emergent from causality rather than prior to it. The HKM and Malament theorems are not merely

mathematical scaffolding for CTGP; under the pre-geometric reading, they become expressions of the

ontological priority of causal ordering over metric structure. The reconstruction direction — from

causal order to geometry, never the reverse — is precisely the direction CTGP’s Causal

Reconstruction Principle requires.
