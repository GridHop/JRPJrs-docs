# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 24 of 40 (1,804 words)



Proof. (a) Let t_K be the largest value of T on K. The level set Σ = { T = t_0 − τ } is a Cauchy

surface, because t_0 − τ > 0, and in a globally hyperbolic spacetime the intersection of the causal

past of a compact set with the causal future of a Cauchy surface is compact. Hence A = J⁻(K) ∩ { T ≥

t_0 − τ } is compact, and so is its projection π(A) ⊆ S. Suppose that R_x meets J⁻(K) at a point p.

Then T(p) ≥ T(x) − τ > t_0 − τ, so p ∈ A, and T(x) ≤ T(p) + τ ≤ t_K + τ, because T increases along

future-directed causal curves. The value T(p) lies in the compact interval [t_0 − τ, t_K], on which

a has a positive minimum a_*, so the condition a(T(p)) d_γ(π(p), π(x)) ≤ ℓ gives d_γ(π(x), π(A)) ≤

ℓ/a_*. The set N of points of S within γ-distance ℓ/a_* of π(A) is closed and bounded, hence compact

by the Hopf–Rinow theorem. Therefore x lies in the compact set [t_0, t_1] × N, where t_1 is the

smaller of t_K + τ and T_max − τ, and a compact set has finite four-volume. (b) The intensity

measure is finite on compact sets, so the number of centres in a compact set is a Poisson variable

with finite mean and is finite almost surely. Exhausting M by countably many compact sets shows

that, almost surely, every compact set contains finitely many centres. For a finite set S of

centres, the union K of the regions O_k ⊆ R_{x_k}, k ∈ S, is compact, and S⁻ lies in the compact set

of part (a), which then contains finitely many centres. □



The lemma uses the FLRW structure: the product form of M, the positive minimum of the scale factor

on compact time intervals, and the completeness of the spatial sections. It is not claimed for

arbitrary globally hyperbolic spacetimes.



Proposition 13.31 (Collapse by gapless pointers). Let φ be the free field of §13.6 on a globally

hyperbolic spacetime, in a state ω, and consider any finite configuration of centres, admissible or

not, with pointers as just described.



    (a) Foliation-independent coupled evolution. Ordered by any Cauchy time function, the coupled

    evolution from before all couplings to after them is the same unitary,



        U = exp(−(i/2) Σ_{k,l} Γ_kl p_k p_l) exp(−i Σ_k p_k φ(h_k)).



    After the coupling, the pointer positions are



        U† q_k U = q_k + φ(h_k) + Σ_l Γ_kl p_l,



    where, as in U, φ is the field of the uncoupled theory. These operators commute with one

    another. Each q_k commutes with the interaction after the coupling of pointer k has ended. The

    joint law of the readings, and the field state conditional on them, therefore do not depend on

    when or in what order the pointers are read, provided that each is read after its own coupling

    has ended.



    (b) Outcome law. For pre-chirped pointers, the readings y_1, …, y_n have the characteristic

    function χ(s), the expectation of exp(i Σ_k s_k y_k) for s ∈ ℝⁿ, given by



        χ(s) = ω(W(Σ_k s_k h_k)) exp(−½ Σ_k σ_k² s_k² − ½ Σ_l b_l² / (4σ_l²)),



    with b_l = Σ_{k≠l} s_k Γ_kl. In a quasi-free state with vanishing one-point function, the

    readings are jointly Gaussian with covariance Σ + diag(σ_k²) + Σ_l g_l g_lᵀ / (4σ_l²), where Σ

    is the covariance of the smeared fields, (g_l)_k = Γ_kl for k ≠ l, and (g_l)_l = 0. Without the

    pre-chirp, (g_l)_l = Γ_ll, so the readings acquire further terms from each pointer’s back-

    reaction on its own reading.



    (c) Unread channel. With all readings summed over, the field undergoes the composition, in any

    order, of the unread Gaussian collapses of φ(h_1), …, φ(h_n) with widths σ_1, …, σ_n

    (Proposition 13.15), with or without the pre-chirp and for every configuration. The

    energy–momentum and the stress–energy injected are therefore those of Proposition 13.16, added

    over the collapses.



    (d) Agreement with sequential collapse. If the configuration is admissible, then for pre-chirped

    pointers the joint law of the readings, together with the conditional field state, is that of

    the Gaussian collapses of φ(h_k) with widths σ_k (Proposition 13.12) applied in any linear

    extension of the causal order; in particular, in a quasi-free state, the law of the readings is

    the law Q_ξ of Theorem 13.21. If the configuration is not admissible, Γ_kl and Γ_lk can both be

    nonzero, and the law of part (b) then differs in general from the law of the collapses applied

    in order of their centres.



    (e) No signaling without an ordering rule. For a set S of pointers, let S⁻ be the set of

    pointers whose regions meet the causal past of some O_k with k ∈ S. The joint law of the

    readings in S depends only on the values ω(W(g)) for g in the span of the h_k with k ∈ S, and on

    the smearings and states of the pointers in S and in S⁻. It is therefore unchanged by adding,

    removing, re-preparing, or reading any further pointer, or by coupling the field to a classical

    source, which acts as a kick, provided that its region does not meet the causal past of any O_k

    with k ∈ S, in particular when that region is causally separated from all of them. This holds

    for every configuration, admissible or not, including Sorkin’s. Part (e) concerns the modeled

    operations, namely gapless pointers and classical sources. It is not a statement about arbitrary

    interventions, such as operations involving interacting matter, probes with internal dynamics,

    or measurements that such pointers do not realize.



    (f) A law of records for infinite configurations. Let the centres form the Poisson process of

    Candidate extension 13.27, with the smearings of its item (ii) and pre-chirped pointers of width

    σ, on any FLRW spacetime of that class, whether its spatial sections are closed, flat, or open,

    and let ω be quasi-free. Almost surely S⁻ is finite for every finite set S of centres, and there

    is a unique probability law on the readings of all centres whose marginal on every finite set S

    is the law of part (b) for the configuration S ∪ S⁻. Averaged over the Poisson process, it gives

    a law of marked centres. Neither an enumeration of the centres in order of T nor finiteness of

    the past regions is needed. This is a probability law for the readings, which are the outcome

    records. It is not a present quantum state containing infinitely many pointers, and no such

    state is constructed here. The law is compatible with a single-outcome reading, in which each

    record is one definite event, but it does not establish the physical generation of infinitely

    many actual events, one present after another, in an infinite volume; that infinite-volume

    generability is open.



    (g) Forward generation for finite configurations. For a finite configuration, let each pointer

    be prepared when the generative present reaches the smallest value of T on its region and read

    when it reaches the largest, which are T(x) − τ and T(x) + τ for the smearings of Candidate

    extension 13.27. Between successive presents, the field then evolves by its field equation with

    the local source Σ_k p_k h_k, each pointer interacts only within its region, and each reading

    concerns a single pointer whose coupling has ended. The present state at each value of T,

    consisting of the field and the pointers whose couplings have begun, conditioned on the readings

    already made, is a density operator, and the law of the next increment depends only on it. The

    readings and conditional states are those of parts (a)–(d). For the Poisson centres of Candidate

    extension 13.27 on a spatially closed FLRW spacetime, only finitely many pointers begin before

    any given value of T, almost surely, so the construction applies at every present. On spatially

    flat or open FLRW spacetimes, infinitely many pointers begin in every slab of cosmological time,

    and a complete stochastic evolution of a present state containing them is not constructed here;

    for these spacetimes part (f) supplies the law of the records only.



Proof. (a) The coupling commutes with every p_k, so the momenta are conserved, and in their joint

spectral representation the field is driven, for each value of the momenta, by the classical source

j = Σ_k p_k h_k. For a free field driven by a classical source of compact support, the interaction-

picture evolution through the support of the source is W(−j) times the phase exp(−(i/2) E_ret(j,

j)). To see this, order the coupling by a Cauchy time function and split j into pieces j_1, …, j_N

supported in successive thin slabs. The slab unitaries are W(−j_a) up to corrections that vanish as

the slabs are refined, and by the first Weyl relation W(−j_N) ⋯ W(−j_1) = exp(−(i/2) Σ_{a>b} E(j_a,

j_b)) W(−j). For a > b and slabs that do not overlap, the support of j_b does not meet the causal

future of the support of j_a, so E_ret(j_b, j_a) = 0 and E(j_a, j_b) = E_ret(j_a, j_b). The phase

therefore tends to exp(−(i/2) E_ret(j, j)) as the slabs are refined, the terms with a = b vanishing

in the limit, and E_ret(j, j) = Σ_{k,l} Γ_kl p_k p_l does not refer to the time function. Since U is

unitary and the q_k commute, so do the U† q_k U. To compute them, conjugate q_k first by the phase

factor, which adds Σ_l Θ_kl p_l with Θ = (Γ + Γᵀ)/2, and then by exp(−i Σ_l p_l φ(h_l)), which adds

φ(h_k) + ½ Σ_l E(h_k, h_l) p_l, the commutator series terminating because E is a number; and Θ_kl +

½ E(h_k, h_l) = Γ_kl. After the coupling of pointer k has ended, the interaction density no longer

contains p_k, so it commutes with q_k, and measuring q_k then has the same effect as measuring it at

the end. (b) Because exp(−iΓ_kk p_k²/2) q_k exp(iΓ_kk p_k²/2) = q_k − Γ_kk p_k, expectations in the

pre-chirped states equal expectations in the states η_k with q_k replaced by q_k − Γ_kk p_k. The

readings thus become q_k + φ(h_k) + Σ_{l≠k} Γ_kl p_l in the state ω ⊗ η_1 ⊗ ⋯ ⊗ η_n. Then Σ_k s_k

y_k corresponds to φ(Σ_k s_k h_k) + Σ_l (s_l q_l + b_l p_l), a sum of commuting terms, and for the

Gaussian η_l, ⟨exp(i(s q_l + b p_l))⟩ = exp(−½ (s² σ_l² + b²/(4σ_l²))). The covariance is the

quadratic term in s of the logarithm. Without the pre-chirp, the term Γ_kk p_k remains in the k-th

reading. (c) In the momentum representation of the pointers, U acts for each value of the momenta as

a phase times exp(−i Σ_k p_k φ(h_k)), which is the product of the single kicks exp(−i p_k φ(h_k)) up
