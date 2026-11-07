So when physicists call the quantum switch causally nonseparable, they’re making a precise statement. Within the relevant operational framework, the process cannot be decomposed into a probabilistic mixture of an A-before-B process and a B-before-A process.
That does not mean all conceivable underlying descriptions of the experiment have been ruled out.
This distinction matters when asking whether there’s “objectively no fact” about the order. In the standard operational quantum description, the process has no definite order of the relevant operations in the sense just explained. It’s not an ordinary unknown classical variable selecting one of two process orders. But interpreting that as a statement about every possible underlying physical fact is an additional step.
There is a useful way to see why ordinary ignorance is inadequate. Suppose the two alternatives leave distinguishable records in the environment. Let |e_BA⟩ be the environmental state associated with the A-then-B branch, and |e_AB⟩ the state associated with the B-then-A branch. The joint state becomes
(|0⟩ ⊗ BA|ψ⟩ ⊗ |e_BA⟩ + |1⟩ ⊗ AB|ψ⟩ ⊗ |e_AB⟩)/√2.
The interference probabilities are then
P(±) = ½[1 ± Re(⟨BAψ|ABψ⟩⟨e_BA|e_AB⟩)].
The additional factor,
⟨e_BA|e_AB⟩,
is the overlap between the environmental states associated with the two alternatives.
If those states are identical, their overlap has magnitude one and they carry no distinguishable which-order information. The interference can remain intact.
If the environmental states are orthogonal,
⟨e_BA|e_AB⟩ = 0,
they are perfectly distinguishable. The interference term disappears, leaving
P(+) = P(−) = ½.
That’s decoherence. The environment has become correlated with the alternative orderings, and interference in the reduced system is lost.
Nobody has to look at the environment for this to happen. The effect depends on physical entanglement and distinguishability, not on whether a human observer learns anything.
There is a familiar quantitative relation here from Englert’s 1996 work on interference visibility and which-way information. For two equally weighted alternatives with pure environmental marker states, define the distinguishability as
D = √(1 − |⟨e_BA|e_AB⟩|²).
If V denotes the normalized interference visibility, then in the ideal pure-state case,
V = |⟨e_BA|e_AB⟩|,
and
V² + D² = 1.
More generally, the complementarity relation is
V² + D² ≤ 1.
This is important because it gives a physical meaning to the distinction between interference and accessible which-alternative information. As the alternatives become more distinguishable, the interference visibility decreases.
It also explains why maintaining coherence becomes difficult when many environmental degrees of freedom are involved.
Suppose the environmental state factors into N components and each component acquires a tiny amount of information distinguishing the alternatives. The total overlap is
⟨e_BA|e_AB⟩ = ∏ₖ ⟨eₖ,BA|eₖ,AB⟩.
If each factor is approximately 1 − ε, then
⟨e_BA|e_AB⟩ ≈ (1 − ε)ᴺ ≈ e^(−Nε).
Take ε = 10⁻⁶ and N = 10⁸. Then
e^(−Nε) = e^(−100) ≈ 3.7 × 10⁻⁴⁴.
Each environmental component carries very little distinguishing information, yet the combined effect almost completely suppresses interference.
This is why simply saying “nobody measured the order” isn’t enough. Environmental correlations can matter even when nobody deliberately measures or collects them.
But I would be careful about turning that into the claim that indefinite order requires absolutely no physical trace anywhere. The precise requirement is that distinguishability of the relevant alternatives must not destroy the coherence needed for the particular interference effect. Partial distinguishability can coexist with partial interference. Correlations may also be manipulated or erased under suitable conditions, and the result depends on which degrees of freedom are included and which measurements are performed.
More importantly, the absence of a distinguishable quantum record does not logically establish the absence of every conceivable underlying fact. That’s a philosophical inference, not a consequence of the overlap equation alone.
Consider the possibility that there really is some deeper variable O specifying which operation occurred first.
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
