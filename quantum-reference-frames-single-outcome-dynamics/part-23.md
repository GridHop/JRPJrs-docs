# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 23 of 40 (1,586 words)

candidate preferred-frame effects identified so far are the energy–momentum injection of part (e)

and the order effects for interfering interventions described under the second limit; neither has

yet been shown to be measurable, as explained below. Fourth, no-signaling and Lorentz invariance are

different properties. Four notions must be kept apart: a Lorentz-invariant law, which refers to no

frame; a covariant formulation with additional background structure, here the cosmological time,

which is covariant under all isometries but not Lorentz-invariant on scales where that structure

matters; preferred-frame effects, which are physical consequences of such structure that single out

the background frame, such as the energy–momentum injection of part (e), and which amount to

measurable Lorentz violation only once an operational prediction for them is given; and superluminal

signaling, which is excluded for the operations of part (c). The candidate contains preferred-frame

structure and satisfies operational no-signaling for the class of interventions covered by

Proposition 13.28(c). Whether a complete physical implementation remains non-signaling under

arbitrary admissible interventions is open, and so is the quantitative question whether its

preferred-frame effects are experimentally viable.



Predicted preferred-frame effects and measurable signatures. The energy–momentum statement of

Proposition 13.28(e) is a theoretical prediction of the free-field model about expectation values:

per unit four-volume, the collapses inject on average the four-momentum λΔP(h), which is at rest in

the cosmic frame. In a laboratory moving with velocity β, in units of c, relative to that frame,

this four-vector has energy component γλΔP⁰ and momentum component −γλΔP⁰ β, so the injected

momentum is a fraction |β| of the injected energy and points against the laboratory’s motion. If the

cosmic frame is identified with the rest frame of the cosmic microwave background, relative to which

the Solar System moves at about 370 km/s (Planck Collaboration 2020), then |β| ≈ 1.2 × 10⁻³. This is

a predicted preferred-frame effect. It is not a demonstrated measurable Lorentz-violation signature,

for four reasons. First, the prediction concerns a free scalar field, whereas an apparatus is made

of matter, for which no collapse law has been given (L2, D7). Second, an operational prediction

needs an account of how the apparatus couples to the field, so that the injected energy–momentum

appears in a recorded quantity: a heating rate of a sample, a stress–energy response, or a

directional effect, such as a mean momentum transfer aligned with the velocity of the cosmic frame,

which an Earth-fixed apparatus would see modulated with the sidereal day. Third, the size of any

such effect depends on λ, σ, τ, ℓ, and c, which are not fixed. Fourth, any predicted signal must be

compared with the experimental bounds on collapse-induced heating (Bassi et al. 2013) and on

preferred-frame effects (Kostelecký & Russell 2011). Until these are supplied, the energy–momentum

injection is a stated prediction of the candidate, not an established observable consequence, and

the same holds for the other effects named in the third limit.



Timing and physical realization. The first limit raises the question whether the collapses can be

timed or realized differently. Three implementations can be compared. Centre-time ordering, rule

(iii) of Candidate extension 13.27, applies each collapse when the generative present reaches the

centre of its region. Completion-time ordering applies it only when the whole region lies in the

generated past. A physical realization replaces each postulated instrument by the reading of a probe

coupled locally to the field and derives the instrument from the coupled dynamics. Propositions

13.29 and 13.31 state what holds for the second and the third.



Proposition 13.29 (Completion-time ordering). In Candidate extension 13.27, replace rule (iii) by

the rule that the collapse at x is applied when the generative present reaches T(x) + τ, the largest

value of T on its support, collapses being applied in order of increasing T(x) + τ.



    (a) Same law. Because every smearing has the same half-width τ, the completion-time order of

    every configuration is its centre-time order. The two rules therefore define the same joint law

    of centres and outcomes on every domain of finite four-volume, and the same measure on infinite

    histories in the setting of Proposition 13.28(f).



    (b) Surviving properties. Parts (a), (b), (c), (e), and (f) of Proposition 13.28 hold for the

    completion-time rule, with the same proofs.



    (c) Forward generation from the generated past. When the collapse at x is applied, its support

    lies in the region T ≤ T(x) + τ, which has already been generated, and φ(h_x) is a function of

    the Cauchy data of the field on the level set T = T(x) + τ within the compact set in which that

    level set meets the causal future of O_x.



    (d) Varying half-widths. If the half-width varied from centre to centre, the two rules would

    order some configurations differently. Lemma 13.26(b), which concerns translates of a single

    region, would then apply to neither rule, and part (b) of Proposition 13.28 would need a

    separate proof for whichever rule was used.



Proof. (a) T(x) + τ < T(x′) + τ exactly when T(x) < T(x′), so the two rules apply the same

instruments in the same order. (b) This follows from (a). (c) Every point of O_x has T ≤ T(x) + τ.

Let Σ be the level set T = T(x) + τ. Since T increases strictly along future-directed causal curves,

a point of Σ in the causal past of O_x lies in O_x. The solution Eh_x vanishes outside the union of

the causal past and the causal future of O_x, so on Σ it vanishes outside the intersection of Σ with

the causal future of O_x, which is compact because Σ is a Cauchy surface and O_x is compact. The

formula for φ(h_x) in the proof of Proposition 13.28(d) then involves only the Cauchy data in that

set. (d) With half-widths τ_x that depend on the centre, the order of the values T(x) + τ_x differs

in general from the order of the values T(x). □



Completion-time ordering thus changes when, in the generative succession, each collapse is applied,

and it changes no probability. It removes the feature that a collapse is applied before part of its

region has been generated. It does not supply a mechanism: the collapse is still an instantaneous

update of the state on one level set by a function of field data in a region whose size is set by ℓ

and τ, and its outcome refers to a field configuration that by then lies in the generated past.



Gapless pointers. Section 13.6 derives a two-outcome instrument from a gapless two-level detector.

The Gaussian collapse is obtained in the same way from a pointer with a continuous reading, in the

manner of von Neumann’s measurement model (see Wiseman & Milburn 2010). Write the causal propagator

as E(f, h) = E_ret(f, h) − E_ret(h, f), where E_ret(f, h) = ±∫ f (G_ret h) dVol_g, G_ret is the

retarded fundamental solution of the field equation, and the sign is fixed by the convention for E.

Then E_ret(f, h) = 0 unless the support of f meets the causal future of the support of h. For a

finite configuration of centres x_1, …, x_n with smearings h_k = h_{x_k} and regions O_k, set Γ_kl =

E_ret(h_k, h_l). Thus E(h_k, h_l) = Γ_kl − Γ_lk, and Γ_kl = 0 unless O_k meets the causal future of

O_l; the diagonal entries Γ_kk are in general nonzero. Attach to centre k a pointer, one canonical

degree of freedom with [q_k, p_k] = i and no Hamiltonian of its own, coupled to the field through

the interaction density p_k h_k(x) φ(x), and let its reading be a value of q_k obtained after its

coupling has ended. Proposition 13.31 gives the Born-rule statistics of the readings; whether the

readings are definite events is a separate question, taken up after its proof. Let η_k(q) =

(2πσ_k²)^{−1/4} exp(−q²/(4σ_k²)). The pointer is pre-chirped if it is prepared in the state

exp(iΓ_kk p_k²/2) η_k, a Gaussian state whose position and momentum are correlated so as to cancel

the pointer’s back-reaction on its own reading.



The following lemma supplies the geometric input for infinite configurations of centres.



Lemma 13.30 (Finitely many causal antecedents). Let (M, g) be an FLRW spacetime with a big-bang

singularity, M = (0, T_max) × S with T_max ≤ ∞ and g = dT² − a(T)² γ, where a is smooth and positive

and (S, γ) is a complete Riemannian three-manifold of constant curvature, so that T is the

cosmological time. Write π(p) ∈ S for the comoving position of a point p. Fix τ > 0, ℓ > 0, and t_0

> τ, and let the region of centres be the set of points x with t_0 < T(x) < T_max − τ, the upper

bound being absent if T_max = ∞. For such x, let R_x be the set of points p with |T(p) − T(x)| ≤ τ

and a(T(p)) d_γ(π(p), π(x)) ≤ ℓ, which lies in M and contains the support of the smearing h_x of

Candidate extension 13.27(ii).



    (a) For every compact set K ⊂ M, the centres x whose sets R_x meet the causal past J⁻(K) lie in

    a compact subset of M, which has finite four-volume.



    (b) Let the centres form a Poisson process with intensity λ dVol_g on the region of centres.

    Almost surely every compact set contains only finitely many centres, and then, for every finite

    set S of centres, the set S⁻ of centres whose regions meet the causal past of the union of the

    regions O_k, k ∈ S, is finite.
