# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 25 of 40 (1,580 words)

to a phase. Tracing out the pointers integrates over the momenta with the density Π_k |η̂_k(p_k)|²,

where η̂_k is the momentum-space wave function of η_k; the pre-chirp does not change this density.

Each factor is the kick density γ of Proposition 13.15(b) with σ = σ_k, so the unread channel is the

composition of the unread Gaussian collapses, which commute (proof of Proposition 13.28(e)).

Proposition 13.16 gives the energy–momentum. (d) A Gaussian collapse of φ(h_k) with width σ_k is the

instrument obtained from an unchirped pointer by the instantaneous coupling V_k = exp(−i p_k φ(h_k))

followed by reading q_k: its Kraus operator for the reading y is ⟨y|V_k|η_k⟩ = η_k(y − φ(h_k)), the

operator K_y of Proposition 13.12. For collapses applied in the order 1, …, n, the first Weyl

relation gives V_n ⋯ V_1 = exp(−(i/2) Σ_{k>l} E(h_k, h_l) p_k p_l) exp(−i Σ_k p_k φ(h_k)). In a

linear extension of the causal order of an admissible configuration, if l precedes k then O_l does

not meet the causal future of O_k, so Γ_lk = 0 and Γ_kl = E(h_k, h_l). Hence Σ_{k,l} Γ_kl p_k p_l =

Σ_k Γ_kk p_k² + Σ_{k>l} E(h_k, h_l) p_k p_l, and the diagonal part of the phase in U cancels the

pre-chirp. U applied to the pre-chirped pointers therefore gives the same joint state of the field

and the pointers as V_n ⋯ V_1 applied to the unchirped ones, and the readings and conditional field

states agree; Theorem 13.21 identifies the law of the sequential collapses as Q_ξ. For the non-

admissible case, item C4(d) of Appendix C.1 gives an example. (e) By (a), the readings in S are

functions of q_k and φ(h_k) for k ∈ S and of the p_l with Γ_kl ≠ 0 for some k ∈ S, that is, of

pointers in S and in S⁻. In the product state, the joint law of these commuting operators is fixed

by the data listed. A classical source f adds E_ret(h_k, f) to the k-th reading, as a pointer with a

definite momentum would, and this vanishes unless the support of f meets the causal past of O_k.

Reading other pointers measures operators that commute with the readings in S, and summing over

their outcomes leaves the law of S unchanged. (f) By Lemma 13.30(b), almost surely S⁻ is finite for

every finite set S of centres. Given the configuration, the law of the readings in S is the same for

every finite configuration containing S ∪ S⁻, by (e), because the further pointers have regions that

do not meet the causal past of the regions in S. For S ⊆ S′, S⁻ ⊆ S′⁻, so the marginal on S of the

law for S′ is the law for S. There are countably many centres, so the Kolmogorov extension theorem

gives a unique law on the readings with these marginals. It depends measurably on the configuration,

because the characteristic functions of part (b) depend continuously on the centres in a quasi-free

state. (g) By (a), the coupled evolution may be computed slab by slab along T, and within a slab the

source involves only the pointers whose regions meet that slab. Each pointer is read after its

coupling has ended, so by (a) the readings and conditional states are those of the complete

evolution. For finitely many centres, the field together with finitely many pointers has a density

operator conditioned on the realized readings, and the next increment, namely evolution through the

next slab, preparation of the pointers whose regions begin there, and reading of those whose regions

end there, depends only on it. For the Poisson centres of Candidate extension 13.27, the centres

whose regions begin in a new slab are those with T(x) − τ in it, and they can be drawn from that

region alone (Theorem 13.21(e)). On a spatially closed FLRW spacetime, the centres with T(x) − τ

below a given value lie in a set of finite four-volume, because the level sets are compact, so there

are finitely many of them almost surely. □



Because the pointers have no Hamiltonian, their coupling densities at spacelike-separated points

commute, as for the gapless detectors of §13.6, and part (e) holds without any rule for ordering

overlapping couplings. Pointers with internal dynamics would require a separate analysis (compare de

Ramón, Papageorgiou & Martín-Martínez 2021). In the numerical checks (Appendix C.1, item C4), the

sums that give the phase of the time-ordered coupling agree exactly along two foliations of relative

rapidity 0.6 and approach Γ as the grid is refined, with largest deviations 2.8 × 10⁻² and 9.0 ×

10⁻³ at 32 and 64 nodes per axis. Explicit pointer computations reproduce the characteristic

function of part (b) to 7.3 × 10⁻¹⁴ and the unread channel of part (c) to 1.7 × 10⁻¹⁴. For a pair of

regions in which one meets the causal future of the other but not conversely, the pointer law equals

that of sequential collapse in causal order to 1.8 × 10⁻¹³. For the overlapping pair of item C3(e),

the pointer law differs from the law of collapses in centre-time order: the variances of the two

readings are larger by 0.0011 and 0.0537.



Statistics and definite outcomes. Proposition 13.31 derives the statistics of the readings from

local coupling densities. It does not derive that the readings have definite values. The coupled

evolution U is unitary and selects no outcome: it produces an entangled state of the field and the

pointers in which every reading allowed by the Born-rule density is represented. A spontaneous-

collapse reading of the construction therefore needs, in addition, a primitive single-outcome

postulate for the pointers.



    (R) Reading postulate. When the coupling of a pointer ends, a reading event occurs. Its value y

    has the Born-rule probability density of q_k in the present state of the field and the pointers,

    conditioned on the readings already made, and the event replaces that state by the normalized

    conditional state, given y, of the field and the other pointers, together with the record y.



The state after a reading can be stated exactly. Write the present state as a density operator ρ on

L²(ℝ) ⊗ H_r = L²(ℝ, H_r), where L²(ℝ) carries the pointer being read in its position representation

and H_r is the space of the field and the other present pointers. Then ρ = Σ_i w_i |Φ_i⟩⟨Φ_i| with

weights w_i ≥ 0 summing to 1 and unit vectors Φ_i ∈ L²(ℝ, H_r), and for almost every y the operator

ρ(y) = Σ_i w_i |Φ_i(y)⟩⟨Φ_i(y)| on H_r is positive and trace-class, with trace p(y), the Born-rule

density of the reading, since Σ_i w_i ∫ ‖Φ_i(y)‖² dy = 1. For every such y with p(y) > 0, the post-

reading state is the normalized density operator ρ(y)/p(y) on H_r together with the record y. The

pointer that has been read does not enter this state as a quantum system: it takes no further part

in the dynamics, and its idealized position eigenvector, which is not normalizable, is not needed.

The present physical state after a reading is therefore well defined, as generability requires, for

every reading outside a set of probability zero.



Three achievements should be kept apart.



    (i) Deriving the Gaussian measurement statistics, the effective field instruments, and their

    causal properties from local coupling densities: established in the stated free-field model

    (Proposition 13.31(a)–(e)).



    (ii) Constructing a consistent probability law for the pointer records, including infinitely

    many centres: established under the stated assumptions (Lemma 13.30, Proposition 13.31(f)), as a

    law of records rather than a global present state; it does not establish infinite-volume

    generability.



    (iii) Deriving objectively definite, spontaneous pointer outcomes without a further postulate:

    not established. The local unitary coupling does not select a single outcome, and the

    construction relies on postulate (R) instead.



Postulate (R) is of the same kind as the event law of the finite model (Definition 4.1) and as the

collapse law of Candidate extension 13.27: in each, the occurrence of a definite event, with

probabilities fixed by the law, is primitive. What the pointer variant changes is where the

postulate acts. Candidate extension 13.27 postulates an instrument on the field; the pointer variant

postulates readings of pointers and derives the instrument on the field. It thus relocates the

collapse postulate from the field to the pointers; it does not remove it. For CTGP the postulate has

three consequences. First, a reading event is a Tier 1 event (Definition 5.1): its occurrence,

labelled by y, is primitive, and the truth profile past-tenses it. The pointer takes no further part

in the dynamics and serves afterwards as the record of y, and the present physical state after the

reading is the normalized conditional state of the field and the other pointers together with that

record. Second, causal inheritance (C-g) and physical instantiation (C-f) require the pointers to

belong to the present physical state: during its coupling a pointer is part of that state, and the

law of its reading depends only on that state, so the variant is generable for finite configurations

(Proposition 13.31(g)). Third, physical adequacy requires an account, not given here, of what the

pointers are, why one exists at each Poisson centre without an experimenter, what prepares it in the

pre-chirped state, and what physical system carries its record. Without such an account, the pointer

variant is a measurement construction read as a spontaneous law, and it shifts the collapse problem

from the field to the pointers rather than solving it.
