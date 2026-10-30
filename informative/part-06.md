How the account remains consistent with relevant relativistic constraints and operational no-signaling.
Why changing the effective description or quantum reference frame does not change which underlying history actually occurred.
These are substantive mathematical and physical requirements, not automatic consequences of single-outcome realism.
A definite history also need not mean that every pair of events is temporally ordered. In relativity, spacelike-separated events need not have an invariant before-and-after ordering. A history can be definite without possessing one universal total ordering of all events.
5. What remains unresolved
Experiments support operational ICO in engineered quantum systems, but they do not establish that fundamentally indefinite spacetime causal order occurs naturally.
Nor do they establish that a definite underlying history is impossible.
Some interpretations and models permit definite underlying events or causal structures; others treat indefinite order as more fundamental. Determining which description, if any, reflects the ultimate ontology requires additional theoretical assumptions and potentially new empirical tests.
In particular, demonstrating that a fixed-spacetime implementation reproduces quantum-switch statistics is not equivalent to constructing a complete, relativistically consistent, single-outcome theory of all quantum phenomena.
6. Bell’s theorem and Frauchiger–Renner
Bell’s theorem rules out Bell-local explanations of certain quantum correlations under specified assumptions; it does not rule out every definite underlying event history. Nonlocal realist theories remain possible, although their compatibility with relativistic requirements raises additional challenges.
Bell nonlocality must also be distinguished from operational signaling. In entangled systems, the joint correlations can violate Bell inequalities while the unconditioned local Born-rule statistics remain independent of the distant measurement setting. These are compatible facts: no-signaling does not eliminate the nonlocal correlations established by Bell experiments.
Furthermore, Bell’s theorem does not, by itself, establish that every definite underlying history requires an invariant temporal ordering of spacelike-separated events or a Galilean spacetime structure. Certain realist models employ preferred foliations, but their necessity depends on additional theoretical assumptions.
For example, Gisin (2011) established a no-go result for a class of deterministic nonlocal hidden-variable models required to reproduce quantum correlations independently of relativistic time ordering. By contrast, Tumulka (2006) constructed a Lorentz-invariant stochastic flash model for noninteracting distinguishable particles.
This illustrates why the assumptions governing determinism, nonlocal dependence, and relativistic covariance matter. Neither result establishes that every definite-history theory requires a preferred frame, nor that every stochastic single-outcome theory automatically satisfies all relativistic requirements.
Frauchiger–Renner addresses a different consistency problem involving quantum measurements and agents’ predictions. Its argument concerns the compatibility of particular assumptions about universal quantum reasoning, single outcomes, and consistency between agents’ conclusions.
Although extended Wigner’s-friend scenarios have connections to Bell-type arguments, these connections do not make Frauchiger–Renner a general impossibility theorem against definite histories compatible with operational indefinite causal order.
The central question remains whether a theory can derive a single realized history while reproducing the interference and causal-nonseparability statistics of effective quantum operations. Neither Bell’s theorem nor Frauchiger–Renner, by itself, settles that question.
The crucial distinction is between definite underlying physical events and effective quantum operations whose statistics cannot be represented by a classical mixture of fixed orders.
Bottom line
Yes, in principle, in suitable theoretical settings. A definite underlying event history need not require every effective quantum operation to possess a single classical order.
Operational indefinite causal order rules out particular classical mixtures of effective operation orders, not every possible definite underlying history.
Nonrelativistic single-outcome theories provide mechanisms for definite trajectories or events to coexist with quantum interference. Results concerning finer-grained causal structures further support the distinction between underlying physical events and effective operation order.
However, these results do not establish a complete relativistically satisfactory single-outcome theory reproducing all relevant indefinite-causal-order phenomena. Constructing such a theory remains an open challenge.


When experiments demonstrate operational indefinite causal order (ICO), still never observed occurring naturally, is there objectively no fact about which operation came first, or can a definite underlying order exist that no observation can reveal?

The answer depends on what we mean by “order.” There’s the order in which two quantum operations act on a system, the order of the physical interactions inside the apparatus, and the possibility of some deeper ordering that isn’t captured by the usual quantum description. Those aren’t necessarily the same thing.
The experimental evidence for indefinite causal order (ICO) is real, but it doesn’t settle every one of those questions. What experiments support is that certain quantum processes cannot be represented as ordinary mixtures of processes in which A definitely precedes B or B definitely precedes A. That’s stronger than saying we don’t happen to know the order. It isn’t, by itself, a proof that reality contains no deeper fact about which interaction occurred first.
So the experiments rule out an ordinary classical mixture of definite operation orders, not every possible deeper account in which events have a definite history.
The standard example is the quantum switch. Imagine two quantum operations, A and B, acting on a target system initially in state |ψ⟩. A control qubit determines which operation comes first. If the control is |0⟩, A acts first and B second, giving BA|ψ⟩. If the control is |1⟩, B acts first and A second, giving AB|ψ⟩. The notation is right-to-left because the rightmost operator acts first.
If the control is prepared in a superposition, (|0⟩ + |1⟩)/√2, the combined output is
(|0⟩ ⊗ BA|ψ⟩ + |1⟩ ⊗ AB|ψ⟩)/√2.
The important thing is that this is a coherent superposition, not merely a situation where the experimenter doesn’t know which setting was chosen.
Now measure the control in the basis
|±⟩ = (|0⟩ ± |1⟩)/√2.
The probabilities are
P(±) = ½[1 ± Re⟨BAψ|ABψ⟩].
That inner product measures the interference between the two possible orderings.
For a particularly simple example, choose A = X and B = Z, the Pauli matrices. They anticommute:
XZ = −ZX.
Consequently,
⟨BAψ|ABψ⟩ = −1,
and therefore
P(−) = 1, P(+) = 0.
The minus outcome occurs with certainty. If A and B commute instead, the plus outcome occurs with certainty.
This is not something an ordinary classical random choice between the two orders reproduces. If the control is an incoherent mixture of |0⟩ and |1⟩, measuring it in the |±⟩ basis gives
P(+) = P(−) = ½.
If both branches instead perform the same operation sequence coherently, the control remains |+⟩, giving P(−) = 0.
Notice the qualification, though. These calculations distinguish particular coherent and incoherent implementations. They do not, by themselves, rule out every conceivable definite-order quantum circuit. The stronger result comes from the theory of quantum supermaps and quantum circuits: under specified restrictions, including a single use of each unknown operation, the quantum switch can accomplish discrimination tasks that circuits with a fixed order or a classical mixture of orders cannot accomplish with the same resources. Chiribella’s 2012 work on perfect discrimination and the 2013 paper by Chiribella, D’Ariano, Perinotti and Valiron establish results of this kind.
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
