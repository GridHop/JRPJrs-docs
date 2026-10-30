If O is an ordinary classical variable that selects A-before-B or B-before-A and the experiment is otherwise described by the usual fixed-order processes, then the resulting process belongs to the class that causal-nonseparability tests are designed to exclude. Simply adding ignorance about O won’t reproduce the coherent quantum-switch statistics.
But that doesn’t mean every hidden-order theory is impossible.
A deeper theory might contain additional variables, nonclassical dynamics, or contextual relationships between the hidden description and observed results. Bohmian mechanics is an instructive comparison. In Bohmian mechanics, particles have definite trajectories, even when the wavefunction follows multiple paths and produces interference. The particle’s trajectory is not necessarily something that can be reconstructed from the ordinary quantum measurement statistics.
One could investigate analogous trajectory-based descriptions of quantum-switch implementations, including descriptions in which a particle follows one definite route through the apparatus while the wavefunction has support on multiple routes.
That would not automatically give us a universal hidden definite causal order for arbitrary quantum processes. It would establish something more limited: that a definite particle trajectory can coexist with operational interference between different orderings in a particular implementation.
There is also a distinction between a hidden variable being inaccessible and being causally irrelevant.
Suppose O is a hidden variable and R is some future measurement result. If the theory satisfies
P(R | S, O) = P(R | S),
where S is the complete operationally specified quantum state and experimental context, then knowing O adds no predictive information about R.
But that condition is not automatically required of every possible hidden-variable theory. In a theory reproducing ordinary quantum predictions, hidden variables may influence individual outcomes even though their distribution leaves the observable statistics unchanged. Bohmian particle positions are an example of variables that are dynamically relevant within the theory but do not ordinarily permit predictions beyond quantum mechanics. In a theory like that, the hidden trajectory needn’t be meaningless or causally idle. It can play a genuine role in the underlying dynamics, even when ordinary measurements cannot determine it independently of the theory. Bohmian trajectory calculations can assign paths to particles in experiments such as the double slit, but those paths are theoretical reconstructions, not independently observed histories. If the theory reproduces standard quantum statistics, the agreement of those statistics alone cannot establish which ontology is correct.
In fact, even if a result is certain, such as P(−) = 1 in the ideal anticommuting example, the fact that
P(− | O) = 1
for every O with nonzero probability tells us only that this particular outcome is certain regardless of O. It doesn’t establish that O has no effect on any other measurement.
Likewise, a Bell-like or theory-independent causal test excludes the class of models satisfying its assumptions. Depending on the test, these may include locality, free choice of interventions, particular laboratory isolation conditions, or a definite causal ordering. Violating the relevant inequality means that those assumptions cannot all be maintained together. It doesn’t uniquely identify which assumption must fail.
This is one reason the distinction between device-dependent and device-independent evidence matters.
Most early quantum-switch experiments relied on characterizing the optical devices and trusting a quantum description of their operation. Procopio and colleagues demonstrated a photonic superposition of gate orders in 2015. Later experiments investigated increasingly demanding ways of certifying the effect.
Rubino and colleagues studied correlations involving entangled temporal orders, and more recent work has pursued certification using Bell-like or causal inequalities. Richter and colleagues in Vienna reported the first implementation of a device-independent protocol, published in PRX Quantum in 2026: they violated such an inequality with a photonic quantum switch, while leaving the locality, freedom-of-choice, and detection loopholes open, along with a “closed-laboratory” assumption that each operation acts only once. Qu and colleagues reported a further device-independent certification experiment in a 2025 preprint, using correlations between spacelike-separated photonic systems. They address the locality and freedom-of-choice loopholes but still rely on a fair-sampling assumption, which leaves the detection loophole open.
These are significant developments, but “device-independent” doesn’t mean completely assumption-free. Such tests still depend on physical conditions that must be justified experimentally, and loopholes can remain.
Nor does a violation of a causal inequality automatically mean that fundamental spacetime itself has no definite causal structure. It means the observed correlations are incompatible with the relevant class of causally ordered models under the test’s assumptions.
The next distinction is probably the most important one for the original question.
In an ordinary laboratory quantum switch, the physical apparatus exists in a spacetime with an ordinary causal structure. The photon’s route can be coherently controlled so that it encounters the devices in different orders, but the apparatus itself doesn’t require spacetime to lose its causal ordering.
For example, imagine two possible routes. Along one route the photon encounters A at an earlier time t₁ and B at a later time t₂. Along the other route it encounters B at t₁ and A at t₂.
The target operations are therefore associated with different spacetime regions depending on the route.
We can represent the alternatives schematically as
Route 1: A(t₁) → B(t₂)
Route 2: B(t₁) → A(t₂),
with
t₁ < t₂.
The coherent quantum process doesn’t simply choose one route randomly. Both alternatives contribute to the quantum state, and their relative phase can affect measurement probabilities.
Nevertheless, the individual time-localized interactions can be described within an ordinary spacetime causal structure.
This is closely related to a result by Vilasini and Renner, published in Physical Review Letters in 2024. They showed, under their assumptions about relativistic causality and realizations in classical background spacetime, that indefinite-order processes require systems that are not localized in spacetime in the ordinary way. They also showed that such realizations admit a finer-grained description with a definite, acyclic causal order.
That is a substantial result. It means an operationally indefinite ordering of two effective operations can coexist with a definite causal ordering of the finer-grained spacetime interactions.
The distinction isn’t merely philosophical wordplay. The effective operation A may be associated with different spacetime regions in different branches of the quantum process. Treating A as one operation localized at one fixed spacetime event would then be misleading.
Oreshkov’s 2019 work on time-delocalized quantum subsystems and operations develops precisely this sort of idea. Paunković and Vojinović, in their 2020 paper on causal orders, quantum circuits and spacetime, discuss why it matters when interpreting experimental claims about indefinite causal order.
The important point is that we have to specify what the supposed ordering relation is between.
If we’re talking about effective operations acting on a quantum system, the order can be indefinite in the operational sense.
If we’re talking about finer-grained physical interactions in a fixed spacetime, those interactions may have a definite causal organization.
And if we’re talking about an even deeper ordering of physical reality, neither of those descriptions automatically settles whether such an ordering exists.
So the two possibilities in the question aren’t necessarily mutually exclusive. There can be no definite operational order of A and B while a definite causal ordering exists in a finer-grained description of the apparatus.
There’s another way to formulate the problem that doesn’t depend on photons traveling along different optical routes. It involves quantum clocks.
Suppose two clocks, A and B, have a relative offset
Δ = t_A − t_B.
Let operation U_A occur when clock A reads τ_A, and operation U_B occur when clock B reads τ_B.
Using clock A’s time coordinate, the second operation occurs at
t_A = τ_B + Δ,
whereas the first occurs at
t_A = τ_A.
The order therefore depends on the sign of
τ_A − (τ_B + Δ).
If the relative offset is a definite classical quantity, then for fixed intervention readings the order can be definite.
But suppose the relative clock offset is in a coherent superposition of two distinguishable alternatives, δ₁ and δ₂, chosen so that the operations occur in opposite orders.
Schematically, the initial state might be
(|f_δ₁⟩ + |f_δ₂⟩)/√2 ⊗ |ψ⟩.
After the controlled interactions, it becomes
(|f_δ₁⟩ ⊗ U_AU_B|ψ⟩ + |f_δ₂⟩ ⊗ U_BU_A|ψ⟩)/√2.
Here the labels are chosen so that δ₁ corresponds to U_B acting first and δ₂ to U_A acting first.
Now suppose the two clock-offset alternatives are orthogonal and we measure only the target system, without accessing the clocks’ coherence. In this idealized model, tracing out the clocks removes the interference terms, so the target statistics are exactly those of an incoherent mixture:
P(α) = ∫ dΔ |χ(Δ)|² P_Δ(α).
Here χ(Δ) is the normalized clock-offset wavefunction and P_Δ(α) is the outcome probability for a definite offset Δ. The expression is a weighted average of definite-offset predictions. It doesn’t mean the full quantum state was an incoherent mixture; it means measurements restricted to the target cannot distinguish the two descriptions in this model. Coherent measurements involving the clocks can reveal the interference.
If the two offset states are orthogonal and we measure the clock in the superposition basis
|f_±⟩ = (|f_δ₁⟩ ± |f_δ₂⟩)/√2,
then the corresponding probabilities are
P(±) = ½[1 ± Re⟨U_AU_Bψ|U_BU_Aψ⟩].
Again, the interference term distinguishes a coherent superposition of alternatives from an incoherent mixture.
For example, if the real part of the overlap is 0.854, then
P(+) = ½(1 + 0.854) = 0.927.
That numerical result is just an illustration of the formula, not a universal prediction about quantum clocks.
There are several qualifications here. The clock states have to be defined consistently, the intervention model matters, and one must distinguish a genuine coherent measurement from merely reading out a classical clock value. The formula is an idealized two-branch model, not a general theorem covering every quantum-clock construction.
This is relevant to quantum reference frames because different physical clocks need not supply identical descriptions of when an interaction occurs. Baumann and Lock investigated temporal localization and causality across quantum reference frames in 2026. Their analysis shows that consistent modeling of interventions across multiple clocks can require temporal delocalization, and that certain cases naturally lead to indefinite operational causal order.
That still doesn’t mean different clocks literally create different objective histories. Nor does it prove that there’s one unique fundamental history. Those are further interpretive questions.
It means that assuming every quantum-clock description can be reduced to one ordinary classical timeline may be too restrictive.
Gravity makes the issue even more interesting.
General relativity says that clocks tick at rates influenced by gravitational potential and spacetime geometry. If the source of the gravitational field is itself in a quantum superposition, one can investigate whether the relative timing of operations becomes correlated with different gravitational configurations.
In a weak, approximately static gravitational field, the fractional proper-time difference associated with a gravitational-potential difference is approximately
Δτ/τ ≈ ΔΦ/c².
For a point mass M, the magnitude of the potential difference between distances r₁ and r₂ is
|ΔΦ| = GM|1/r₁ − 1/r₂|.
Therefore,
|Δτ|/τ ≈ (GM/c²)|1/r₁ − 1/r₂|.
