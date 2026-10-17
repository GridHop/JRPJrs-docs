# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 22 of 40 (1,812 words)



    (i) Locations. Collapse centres form a Poisson process with intensity λ dVol_g in the region T >

    t_0, as in Definition 13.20, where t_0 > τ is fixed by condition (ii). If the universe

    recollapses at a finite cosmological time T_max, the region is t_0 < T < T_max − τ, so that

    every collapse region lies in the spacetime.



    (ii) Smearing law. Each smearing h_x is built from T and g alone and is supported in the slab |T

    − T(x)| ≤ τ: h_x(p) = c χ((T(p) − T(x))/τ) ψ₀(d_x(p)²/ℓ²), where d_x(p) is the proper distance,

    within the level set of p, from the comoving worldline through x, χ and ψ₀ are fixed smooth

    functions with ψ₀ supported in [0, 1), and c is a constant. The radius ℓ and the earliest time

    t_0 of item (i) are chosen so that, for every centre with T(x) > t_0, the slab stays away from

    the big bang and the support lies within a normal neighbourhood of the worldline in every level

    set it meets, that is, inside the injectivity radius of those level sets, which is infinite for

    flat and open FLRW slices and equals π times the curvature radius for closed ones. There d_x² is

    smooth, so h_x is a smooth test function of compact support; the distance itself can fail to be

    smooth at cut points, which this choice excludes.



    (iii) Ordering rule. Collapses are applied in order of increasing T(x); ties have probability

    zero.



    (iv) Update. Each collapse is the Gaussian collapse of φ(h_x) with width σ (Proposition 13.12).



The parameters are λ, τ, ℓ, σ, c, and t_0.



Proposition 13.28 (Properties of the candidate extension).



    (a) Completeness. Every finite configuration of centres, admissible or not, receives a

    normalized joint law of outcomes. The candidate therefore defines an unconditional collapse

    dynamics on the full Poisson configuration space of any domain of finite four-volume.



    (b) Agreement with the causal-order dynamics. The ordering rule agrees with causal precedence

    for every pair of collapses whose centres differ in cosmological time by more than 2τ. In the

    flat local model of Lemma 13.26(b), the law coincides with that of Theorem 13.21 on every

    admissible configuration, and the candidate extends it to the remaining configurations.



    (c) No signaling for the covered operations. In any finite configuration, let Y be a set of

    collapses, and let j be an operation, inserted at any position in the sequence, whose Kraus

    operators commute with every W(g), g in the span of the h_y with y ∈ Y, the other operations

    being the law’s collapses or Weyl-diagonal operations. Then the unconditioned joint law of the

    outcomes in Y does not depend on whether j is performed. This holds in particular when j is

    localized in a region causally separated from every O_y.



    (d) Forward generation in the free-field representation. The collapse at x is a function of

    φ(h_x), which equals the symplectic product of Eh_x with the Cauchy data of the field on the

    level set T = T(x). It can therefore be applied when the generative present reaches T(x), and

    the centres in each successive slab of cosmological time are drawn from that slab alone. The

    process is generated forward along cosmological time from the present field state and the

    realized events, with no future input. This is forward generation of the mathematical

    description; it is not a fully local dynamical implementation, because the support of h_x

    extends to T(x) + τ.



    (e) Preferred-frame structure. Each collapse changes the expected renormalized stress–energy

    tensor by T^cl[Eh_x]/(4σ²) (Proposition 13.16(d)), which is invariant under the rotations about

    the comoving worldline through x. In the flat local model with rotation-invariant smearings, the

    mean four-momentum injected per unit four-volume is λ ΔP(h), a fixed timelike vector at rest in

    the cosmic frame. This is a property of field expectation values and a theoretical prediction of

    the free-field model, not by itself a measurable signature (see the discussion of measurable

    signatures below). The order that the rule assigns to law collapses among themselves, by

    contrast, affects only the joint law of their outcomes: their unread channels commute, so

    reordering law collapses among themselves, without changing their positions relative to other

    operations, leaves every unconditioned statistic of those other operations unchanged. For two

    collapses with E(h_i, h_j) ≠ 0 whose centres differ in cosmological time by at most 2τ, the

    joint law of the outcomes depends on which centre is earlier in cosmological time (Proposition

    13.23). When such centres are spacelike-separated, different inertial frames would order them

    differently, so the ordering rule produces cosmic-frame-dependent correlations among collapse

    outcomes.



    (f) Infinite histories when past regions are finite. Suppose that every past region D_t = { p :

    t_0 < T(p) ≤ t } has finite four-volume, as in spatially closed FLRW spacetimes; every level set

    of T has four-volume zero. Then almost surely only finitely many centres lie in each D_t and no

    two share a value of T, so the centres form a sequence x_1, x_2, … ordered by T, which is finite

    if the region of centres has finite four-volume and infinite otherwise. There is a unique

    probability measure on the corresponding histories of marked centres, finite or infinite, whose

    marginal on the centres and outcomes in each D_t is the law of part (a) for the domain D_t. This

    projective consistency holds for the nested past regions D_t. It does not hold for an arbitrary

    subdomain D of finite four-volume: collapses outside D that precede some of those in D change

    the state before them, so the marginal of the global law on D differs in general from the law of

    part (a) for D, which applies only the collapses in D. If these regions have infinite four-

    volume, as in spatially infinite FLRW spacetimes, every slab of cosmological time contains

    infinitely many centres almost surely, so its collapses cannot be applied one after another in

    order of T, and the existence of a global process is open.



Proof. (a) A finite sequence of normalized instruments composes to a normalized instrument. (b)

Lemma 13.26 and Theorem 13.21(a). (c) Theorem 13.17 with Corollary 13.18; the conditions of the

theorem do not depend on how the order of the operations was chosen. (d) For a free field on a

globally hyperbolic spacetime, φ(h) = ∫_Σ ((Eh) ∇_nφ − φ ∇_n(Eh)) dΣ for every Cauchy surface Σ, up

to a sign fixed by the convention for E (Wald 1994), and the level sets of T are Cauchy surfaces by

assumption. The statement about the centres is Theorem 13.21(e). (e) Proposition 13.16(c) and (d),

the rotational symmetry of h_x, and Campbell’s formula give the energy–momentum. The unread channels

commute because each multiplies every Weyl operator by a number, so their duals commute on the Weyl

operators and, being normal, on the von Neumann algebra those operators generate, which contains

every observable of the field. The order dependence of the joint outcome law is Proposition 13.23.

(f) Since Vol_g(D_t) is finite, the Poisson count in D_t is finite almost surely, and since level

sets have four-volume zero, ties in T have probability zero. Given the past, the next centre is the

first Poisson point above the current value of T, by the complete independence of the Poisson

process, or there is no further centre, an outcome of probability exp(−λ v(t′)) at the current value

t′, where v(t′) is the four-volume of the part of the region of centres with T > t′; this

probability is positive when v(t′) is finite. Including that terminal state, both the kernel for the

next centre and the Born-rule kernel for the next outcome are measurable on standard Borel spaces,

and the Ionescu-Tulcea theorem gives a unique measure on histories with these kernels. Its marginal

on D_t is the law of part (a) for D_t, because every collapse in D_t precedes every collapse outside

it, and the later collapses, with their outcomes summed over, are trace-preserving. For an arbitrary

subdomain this argument fails at its first step, since collapses outside the subdomain can precede

collapses inside it. A Poisson process of infinite intensity measure on a slab has infinitely many

points there almost surely. □



In the numerical checks (Appendix C.1, items C3(g) and C3(h)), ordering by the times of the centres

is a linear extension of the causal order in all 300 admissible configurations of item C3(c), as

Lemma 13.26(b) requires for causal diamonds. In a Sorkin-type configuration whose two intermediate

law collapses overlap, so that it is not admissible, applying the collapses in order of time leaves

the target’s binned law unchanged, to within 1.6 × 10⁻¹⁵, when a kick, a Gaussian collapse, or an

unsharp Lüders instrument, which is not Weyl-diagonal, is applied in a region causally separated

from the target. If an unsharp Lüders instrument replaces the first intermediate collapse, the kick

shifts the target law by 8.1 × 10⁻⁴. In the tested configuration, the cosmological-time ordering

rule produces no signaling for the specified interventions. The Lüders control shows that this

conclusion cannot be extended to arbitrary intervening instruments. In item C3(e), the unread

channels of two overlapping collapses give the same final state in either order, to 6.8 × 10⁻¹⁵,

although the joint laws of their outcomes differ.



Four limits of Proposition 13.28 should be stated. First, part (d) establishes computability from

present Cauchy data, not physical causal locality. A smeared free-field observable can always be

rewritten through the causal propagator as an observable on a single Cauchy surface, but the

collapse of φ(h_x) concerns the field smeared over a region that extends to cosmological time T(x) +

τ, so its physical localization is extended in time, and a fully local dynamical implementation of

the centre-time rule, for instance through a coupled field, has not been given; Propositions 13.29

and 13.31 below examine two alternatives. Second, part (c) covers the stated class of operations. It

does not show that arbitrary physically implementable interventions can be inserted without

detectable effects of the ordering rule: an intervention whose region interferes, within 2τ in

cosmological time, with a law collapse is ordered relative to it by the rule, and the joint

statistics can then depend on that order, as in Proposition 13.23. In the realization of Proposition

13.31, where the law’s collapses and the interventions are all realized by gapless pointers, no rule

orders them, and this limit does not arise. Third, the correlation structure of part (e) is a

statement about the collapse outcomes, which CTGP treats as primitive occurrences. It shows that the

event statistics depend on the cosmic frame; it does not by itself show measurable Lorentz

violation. By part (e), no unconditioned statistic of other operations reveals the order of law

collapses among themselves, so whether these correlations induce operationally detectable signatures

requires an explicit account of how collapse outcomes are recorded in accessible observables. The
