# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 22 of 25 (1,822 words)

    relativity. Philosophy of Science, 33(4), 341–344.



Rovelli, C. (2004). Quantum Gravity. Cambridge University Press.



Savitt, S. F. (2009). The transient nows. In W. C. Myrvold & J. Christian (Eds.), Quantum Reality,

    Relativistic Causality, and Closing the Epistemic Circle. Springer.



Sider, T. (2001). Four-Dimensionalism: An Ontology of Persistence and Time. Oxford University Press.



Skow, B. (2015). Objective Becoming. Oxford University Press.



Smolin, L. (2013). Time Reborn. Houghton Mifflin Harcourt.



Sorkin, R. D. (2003). Causal sets: Discrete gravity. In Lectures on Quantum Gravity (pp. 305–327).

    Springer.



Stein, H. (1991). On relativity theory and openness of the future. Philosophy of Science, 58(2),

    147–167.



Stoner, E. C., & Wohlfarth, E. P. (1948). A mechanism of magnetic hysteresis in heterogeneous

    alloys. Philosophical Transactions of the Royal Society A, 240(826), 599–642.



Tegmark, M. (1997). On the dimensionality of spacetime. Classical and Quantum Gravity, 14, L69–L75.



Tononi, G. (2008). Consciousness as integrated information: A provisional manifesto. Biological

    Bulletin, 215, 216–242.



Vilasini, V., & Renner, R. (2024). Fundamental limits for realising quantum processes in spacetime.

    Physical Review Letters, 133, 080201.



Wald, R. M. (1984). General Relativity. University of Chicago Press.



Wallace, D. (2012). The Emergent Multiverse. Oxford University Press.



Will, C. M. (2014). The confrontation between general relativity and experiment. Living Reviews in

    Relativity, 17, 4.



Zimmerman, D. W. (2011). Presentism and the space-time manifold. In C. Callender (Ed.), The Oxford

Handbook of Philosophy of Time (pp. 163–244). Oxford University Press.



Zurek, W. H. (2003). Decoherence, einselection, and the quantum origins of the classical. Reviews of

    Modern Physics, 75, 715–775.



Zurek, W. H. (2009). Quantum Darwinism. Nature Physics, 5, 181–188.



----------------------------------------------------------------------------------------------------

Appendix A. ADM Evolution and σ-Reparameterization (Derivations)

----------------------------------------------------------------------------------------------------



This appendix collects standard ADM equations and shows how CTGP's growth parameter σ can be used to

reparameterize evolution. The presentation follows standard canonical GR notation and then adds

CTGP's σ-change of variables.



A.1 ADM Variables and Constraints

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



        g_{μν} → (h_{ij}, N, N^i);  K_{ij} = (1/2N)(∂_t h_{ij} − ∇_i N_j − ∇_j N_i)



Hamiltonian constraint:



        H = R^{(3)} + K² − K_{ij}K^{ij} − 16πG ρ = 0



Momentum constraint:



        H_i = ∇_j (K^j_i − δ^j_i K) − 8πG j_i = 0



A.2 Evolution Equations

~~~~~~~~~~~~~~~~~~~~~~~



        ∂_t h_{ij} = 2N K_{ij} + ∇_i N_j + ∇_j N_i



        ∂_t K_{ij} = −∇_i ∇_j N + N( R^{(3)}_{ij} + K K_{ij} − 2K_{ik}K^k_j ) + (shift and matter terms)



A.3 Cosmological Time and Its Relabelings

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



The discussion in §6.7 establishes that the present hypersurfaces are future Cauchy surfaces whose

induced data satisfy the ADM constraints and fix their successors under the Einstein equations. This

appendix records the explicit form of the generation parameter in cosmological settings.



In FLRW with a big-bang singularity, cosmological time is cosmic time: τ = t. A relabeling σ = F(t)

with F′ > 0 converts time derivatives by ∂_σ = (1/F′) ∂_t; for the canonical choice F = identity, σ

= t.



A.3.1 Well-Definedness, Dimensions, and Reparameterization of σ

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Three properties of the generation parameter are relied upon elsewhere and are stated explicitly

here. The first is well-definedness. Cosmological time is defined as a supremum over all

past-directed causal curves, not by integration along a chosen congruence, so no path-independence

condition is required: τ(p) is well defined whenever it is finite. Its level sets are future Cauchy

surfaces when τ is regular (Theorem 17.4). A rotating cosmology such as Gödel’s dust solution admits

no regular cosmological time, consistent with the global hyperbolicity requirement of §6.1.



The second is dimension. For the canonical choice σ = τ, σ carries dimensions of time; for other

relabelings, its dimensions are those of F. The two are related monotonically, induce the same

foliation, and differ only in normalization and units. Statements that σ “corresponds to”

cosmological proper time are to be read in this sense.



The third is reparameterization. Any strictly increasing F yields an equally admissible parameter,

so σ is fixed only up to monotonic relabeling. This is harmless for every claim the framework makes,

because those claims depend on the level sets of σ and the direction of ∇_μσ, both of which are

relabeling-invariant. The magnitude |∇_μσ| = F′ is conventional and carries no physical content.



For reference, the chain from geometry to foliation is as follows: g_{μν} → causal structure → τ,

the maximal elapsed proper time, defined without choice → Σ_τ, future Cauchy surfaces when τ is

regular → σ = F(τ), a labeling convention. The matter congruence enters only as a consequence: in

cosmology, the maximizing geodesics are the comoving worldlines.



A.4 ADM Equations Parameterized by σ

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Substituting ∂_t = F′ ∂_σ into ADM evolution, with the lapse normalized to cosmic time:



        ∂_σ h_{ij} = (2N/F′) K_{ij} + (1/F′)(∇_i N_j + ∇_j N_i)



        ∂_σ K_{ij} = (1/F′)(standard ADM right-hand side)



A.5 Expansion Scalar and Raychaudhuri Calibration

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Let u^μ be the timelike unit vector field aligned with the matter congruence. The expansion scalar θ

= ∇_μu^μ satisfies θ = d(ln √h)/dτ, measuring the fractional rate of local volume change of the

foliation along the congruence. Its evolution is governed by the Raychaudhuri equation:



        dθ/dτ = -(1/3)θ² - σ_{μν}σ^{μν} + ω_{μν}ω^{μν} - R_{μν}u^μu^ν + ∇_μa^μ



In the irrotational, geodesic cosmological limit (ω_{μν} = 0, a^μ = 0) this reduces to:



        dθ/dτ = -(1/3)θ² - σ_{μν}σ^{μν} - R_{μν}u^μu^ν



CTGP uses this result to interpret geometric growth in terms of foliation expansion rather than as a

derivative dM/dσ of the generated domain treated as a scalar quantity. The expansion scalar θ

provides the GR-native local measure of how the present hypersurface is extending relative to

neighboring hypersurfaces: θ > 0 in expanding cosmologies, θ < 0 in collapsing regimes. Via the

Einstein equations, the R_{μν}u^μu^ν term links the evolution of θ directly to the matter content

through the Ricci curvature, grounding CTGP’s growth picture in standard relativistic dynamics.



----------------------------------------------------------------------------------------------------

Appendix B. Causal Structure Theorems and Their Application to CTGP

----------------------------------------------------------------------------------------------------



B.1 Global Hyperbolicity and Causal Order

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



A spacetime (M, g) is globally hyperbolic if it admits a Cauchy hypersurface — a spacelike surface

intersected exactly once by every inextendible causal curve. This property is widely believed to

hold for our universe on cosmological scales (Hawking and Ellis 1973).



Theorem B.1 (Hawking–King–McCarthy, 1976). In suitably well-behaved relativistic spacetimes, the

chronological relation I⁺(p) — the set of events reachable from p by future-directed timelike curves

— determines the conformal structure of the spacetime metric. The topology and light-cone structure

can be reconstructed uniquely up to an overall conformal factor from knowledge of the chronological

order alone.



Theorem B.2 (Malament, 1977). The causal ordering relation alone suffices to determine the conformal

metric structure of relativistic spacetime under mild conditions. Temporal precedence is not a

coordinate convention but a geometric fact encoded in causal relations.



Theorem B.3 (Geroch, 1970). In a globally hyperbolic spacetime there exists a continuous time

function — a function that strictly increases along every future-directed causal curve. Moreover, M

≅ ℝ × Σ, where each slice is a Cauchy hypersurface. This splitting is not imposed but follows from

the causal structure.



Theorem B.4 (Bernal and Sánchez, 2003, 2005). In any globally hyperbolic spacetime, there exists a

smooth temporal function whose gradient is everywhere timelike and whose level sets are smooth

spacelike Cauchy hypersurfaces. Any Geroch splitting can be refined to a smooth one. Moreover, any

two smooth Cauchy foliations can be smoothly deformed into each other.



B.2 Application to CTGP

~~~~~~~~~~~~~~~~~~~~~~~



These theorems guarantee that the mathematical structure CTGP requires — a global foliation by

present hypersurfaces Σ_σ with σ increasing causally — exists in any globally hyperbolic spacetime.

This is not an additional CTGP postulate but a consequence of GR’s causal structure under physically

reasonable assumptions. Standard interpretations treat the entire product manifold ℝ × Σ as

ontologically complete. CTGP instead interprets the parameter labeling the slices as indexing the

progressive generation of spacetime structure: at stage σ, only the present slice exists; the

hypersurfaces in its past belong to the formal history M(σ), and the future hypersurfaces Σ_{σ′>σ},

while mathematically definable within the full spacetime manifold, are not part of the generated

domain.



The freedom to choose among smooth temporal foliations corresponds to the freedom to pick different

smooth temporal functions. CTGP resolves this ambiguity with cosmological time: among all time

functions, it is singled out by maximal elapsed proper time, and in cosmology it coincides with the

matter rest frame. The logical priority is clear: causal geometry (Theorems B.1–B.4) precedes

cosmological time (Theorem 17.4), which precedes the labeling convention σ = F(τ). σ is not a novel

object introduced by CTGP; it is a distinguished time function that general relativity already

provides.



----------------------------------------------------------------------------------------------------

Appendix C. Vulnerability Assessment

----------------------------------------------------------------------------------------------------



The three principal vulnerabilities of CTGP concern foliation dependence, underdetermination with

respect to eternalism, and the use of a preferred cosmological frame. The responses to each are

developed in the main text (§§6.10, 11.4, 12, 9.3.1); this appendix records the residual assessment.



After these responses, the residual severity of each vulnerability is as follows. The foliation

criticism is answered: the present is geometrically unique wherever cosmological time is regular,

aligned with matter in cosmology, and globally defined through structure formation; the open cases

are past-eternal, cyclic, and emergent cosmologies and non-uniform bounces, with single uniform

bounces covered by §6.10.1. The underdetermination criticism is correct and is accepted in its

precise form: the ontology is observationally equivalent to eternalism for fixed physics, and its

empirical exposure is structural rather than observational (§12). The preferred-frame criticism is

answered in its usual form, since cosmology already employs the same frame and CTGP predicts no

local preferred-frame effects.



The deep philosophical challenge that remains is whether a generative ontology is more than an

interpretive preference. That question cannot be settled by formal argument or by measurement alone;

it belongs to the broader debate over scientific realism, underdetermination, and inference to the

best explanation. CTGP’s contribution is to make the debate concrete: to specify the present

precisely, to show which physical realizations of it are consistent, and to identify the structural

commitment through which the ontology remains exposed to evidence.



----------------------------------------------------------------------------------------------------

Appendix D. CTGP and Conscious Experience

----------------------------------------------------------------------------------------------------



The relationship between CTGP's temporal ontology and the philosophy of mind is among the

framework's most distinctive contributions. This appendix develops the connection systematically.



Structural note on scope. CTGP operates at two analytically distinct levels that should be kept

separate when evaluating the framework’s physics credentials. The core theory — comprising §§1–12,

the σ formalism, ADM evolution, cosmological foliation, and the empirical standing set out in §12 —

is a standalone spacetime ontology that can be evaluated entirely on physics and philosophy-of-

physics merits, independent of the consciousness discussion. Appendix D extends CTGP’s temporal

ontology into the domain of mind and experience. This extension is motivated by the core theory —

the present-edge structure of M(σ) provides a natural locus for qualia — but it is not a

prerequisite for accepting the core framework. Readers primarily interested in the physics case may
