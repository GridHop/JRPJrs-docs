# Cosmic-Time Generative Presentism (CTGP) — Explained

Part 20 of 25 (1,798 words)

swept out, not the intermediate foliation: ρ[Σ_2] = U(Σ_2, Σ_1) ρ[Σ_1] is foliation-path-

independent. No superluminal signaling is introduced. CTGP requires only collapse densities built

from local commuting field polynomials or smeared number/energy densities with spacelike-separated

supports commuting in the AQFT sense; this admissible class satisfies the conditions above, making

hypersurface-path independence a conditional theorem rather than an assumed property. □



Theorem 17.17 (Continuum Limit of Local CP Evolution). Let ℒ^{(n)} be a sequence of Lindblad

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

|R_{μνρσ}| ≪ M_{Pl}^2, σ exists as a time function whose level sets are Cauchy surfaces, given by

cosmological time as in §§6.1–6.3, and it is a smooth temporal scalar field wherever the maximizing

congruence is single-valued. Near Planck curvature, the smooth representation may break down; CTGP

then treats σ as the continuum image of an underlying growth ordering variable, with causal-set

counting as the preferred candidate discrete realization. CTGP is therefore fundamental at the

ordering level, not necessarily at the smooth-manifold level: the smooth σ-field is emergent in the

classical regime, and singular classical regions mark breakdown of the continuum representation

rather than breakdown of temporal ordering itself. This avoids a false dichotomy between “σ is

fundamental as a smooth field everywhere” and “CTGP fails wherever classical GR fails.” □



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

boundary; it is finite, tends to zero on approach to S, and its level sets are Cauchy surfaces.

Consequently σ = F(τ_S), with F strictly increasing, is an admissible generation parameter through

S. In an exact FLRW universe with a single bounce, taking S to be the surface of zero mean curvature

at the bounce makes τ_S cosmic time measured from the bounce.



Proof sketch. Restrict to the open region I⁺(S), itself globally hyperbolic. Every past-inextendible

causal curve in it approaches S, and J⁻(p) ∩ J⁺(S) is compact for each p, so the supremum defining

τ_S(p) is finite and τ_S → 0 along curves approaching S: the cosmological time of I⁺(S) is regular.

Theorem 17.4 then applies to that region, and the same argument with time reversed applies to I⁻(S).

□



----------------------------------------------------------------------------------------------------

References

----------------------------------------------------------------------------------------------------



Andersson, L., Galloway, G. J., & Howard, R. (1998). The cosmological time function. Classical and

    Quantum Gravity, 15, 309–322.



Arkani-Hamed, N., Cheng, H.-C., Luty, M. A., & Mukohyama, S. (2004). Ghost condensation and a

    consistent infrared modification of gravity. Journal of High Energy Physics, 2004(05), 074.



Arnowitt, R., Deser, S., & Misner, C. W. (1962). The dynamics of general relativity. In L. Witten

    (Ed.), Gravitation: An Introduction to Current Research (pp. 227–265). Wiley. (arXiv:gr-

    qc/0405109)



Babichev, E., & Ramazanov, S. (2017). Caustic free completion of pressureless perfect fluid and

    k-essence. Journal of High Energy Physics, 2017(08), 040.



Bassi, A., Lochan, K., Satin, S., Singh, T. P., & Ulbricht, H. (2013). Models of wave-function

    collapse, underlying theories, and experimental tests. Reviews of Modern Physics, 85, 471–527.



Bell, J. S. (1987). Speakable and Unspeakable in Quantum Mechanics. Cambridge University Press.



Bernal, A. N., & Sánchez, M. (2003). On smooth Cauchy hypersurfaces and Geroch’s splitting theorem.

    Communications in Mathematical Physics, 243(3), 461–470.



Bernal, A. N., & Sánchez, M. (2005). Smoothness of time functions and the metric splitting of

    globally hyperbolic spacetimes. Communications in Mathematical Physics, 257(1), 43–50.



Bigelow, J. (1996). Presentism and properties. Philosophical Perspectives, 10, 35–52.



Bohm, D. (1952). A suggested interpretation of the quantum theory in terms of 'hidden' variables.

    Physical Review, 85, 166–179; 180–193.



Bombelli, L., Lee, J., Meyer, D., & Sorkin, R. D. (1987). Space-time as a causal set. Physical

    Review Letters, 59(5), 521–524.



Broad, C. D. (1923). Scientific Thought. Routledge.



Brown, H. R. (2005). Physical Relativity: Space-Time Structure from a Dynamical Perspective. Oxford

    University Press.



Callender, C. (2017). What Makes Time Special? Oxford University Press.



Carroll, S. M. (2004). Spacetime and Geometry: An Introduction to General Relativity. Addison-

    Wesley.



Carroll, S. M. (2010). From Eternity to Here: The Quest for the Ultimate Theory of Time. Dutton.



Chalmers, D. J. (1996). The Conscious Mind. Oxford University Press.



Chamseddine, A. H., & Mukhanov, V. (2013). Mimetic dark matter. Journal of High Energy Physics,

    2013(11), 135.



Chiribella, G., D’Ariano, G. M., Perinotti, P., & Valiron, B. (2013). Quantum computations without

    definite causal structure. Physical Review A, 88, 022318.



Colladay, D., & Kostelecký, V. A. (1998). Lorentz-violating extension of the standard model.

    Physical Review D, 58, 116002.



Craig, W. L. (2001). Time and the Metaphysics of Relativity. Kluwer Academic Publishers.



Dehaene, S. (2014). Consciousness and the Brain. Viking.



Deng, N. (2013). The block universe: A metaphysical analysis. In R. Ciuni et al. (Eds.), New Papers

    on the Present. Philosophia Verlag.



Dieks, D. (Ed.). (2006). The Ontology of Spacetime. Elsevier.



Doob, J. L. (1957). Conditional Brownian motion and the boundary limits of harmonic functions.

    Bulletin de la Société Mathématique de France, 85, 431–458.



Dowker, F. (2005). Causal sets and the deep structure of spacetime. In 100 Years of Relativity.

    World Scientific.



Earman, J. (2006). Two challenges to the requirement of substantive general covariance. Synthese,

    148, 443–468.



Einstein, A. (1915). Die Feldgleichungen der Gravitation. Sitzungsberichte der Preussischen Akademie

    der Wissenschaften.



Ellis, G. F. R. (2014). The evolving block universe and the meshing together of times. Annals of the

    New York Academy of Sciences, 1326, 26–41.



Ellis, G. F. R., & Rothman, T. (2010). Time and spacetime: The crystallizing block universe.

    International Journal of Theoretical Physics, 49, 988–1003.



Ellis, G. F. R., Maartens, R., & MacCallum, M. A. H. (2012). Relativistic Cosmology. Cambridge

    University Press.



Erickcek, A. L., Carroll, S. M., & Kamionkowski, M. (2008). Superhorizon perturbations and the

    cosmic microwave background. Physical Review D, 78, 083012.



Everett, H. (1957). 'Relative state' formulation of quantum mechanics. Reviews of Modern Physics,

    29, 454–462.



Friston, K. (2010). The free-energy principle: A unified brain theory? Nature Reviews Neuroscience,

    11, 127–138.



Garriga, J., & Mukhanov, V. F. (1999). Perturbations in k-inflation. Physics Letters B, 458,

    219–225.



Geroch, R. (1970). Domain of dependence. Journal of Mathematical Physics, 11(2), 437–449.



Ghirardi, G. C., Rimini, A., & Weber, T. (1986). Unified dynamics for microscopic and macroscopic

    systems. Physical Review D, 34(2), 470–491.



Gödel, K. (1949). An example of a new type of cosmological solutions of Einstein’s field equations.

    Reviews of Modern Physics, 21, 447–450.



Gottesman, D., & Preskill, J. (2004). Comment on “The black hole final state.” Journal of High

    Energy Physics, 2004(03), 026.



Hartle, J. B., & Hawking, S. W. (1983). Wave function of the universe. Physical Review D, 28(12),

    2960–2975.



Hawking, S. W., & Ellis, G. F. R. (1973). The Large Scale Structure of Space-Time. Cambridge

    University Press.



Hawking, S. W., King, A. R., & McCarthy, P. J. (1976). A new topology for curved space-time which

    incorporates the causal, differential, and conformal structures. Journal of Mathematical

    Physics, 17(2), 174–181.



Hoftuft, J., Eriksen, H. K., Banday, A. J., Górski, K. M., Hansen, F. K., & Lilje, P. B. (2009).

    Increasing evidence for hemispherical power asymmetry in the five-year WMAP data. The

    Astrophysical Journal, 699, 985–989.



Hořava, P. (2009). Quantum gravity at a Lifshitz point. Physical Review D, 79, 084008.



Horowitz, G. T., & Maldacena, J. (2004). The black hole final state. Journal of High Energy Physics,

    2004(02), 008.



Ismael, J. (2016). How Physics Makes Us Free. Oxford University Press.


