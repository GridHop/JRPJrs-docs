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
To get an idea of the scale, imagine a 1 kg mass in a hypothetical superposition of configurations placing it 1 cm and 2 cm from a clock.
Using
G ≈ 6.67 × 10⁻¹¹ m³ kg⁻¹ s⁻²,
we get
|ΔΦ| ≈ (6.67 × 10⁻¹¹)(100 − 50)
≈ 3.34 × 10⁻⁹ m²/s².
Dividing by
c² ≈ 9 × 10¹⁶ m²/s²
gives
|Δτ|/τ ≈ 3.7 × 10⁻²⁶.
Over one second, the proper-time difference is therefore approximately
|Δτ| ≈ 3.7 × 10⁻²⁶ s.
That’s an extraordinarily small difference.
If two operations are arranged so that their relative order depends on this gravitationally induced timing difference, the relevant timing must be controlled on a correspondingly demanding scale in this example.
Of course, this isn’t a realistic experimental proposal. Maintaining a kilogram-scale object in the required spatial quantum superposition would be an enormous challenge, and the gravitational interaction, coherence, and clock dynamics would all have to be treated consistently.
The calculation illustrates the difficulty of producing a gravitationally controlled change of operation order. It does not establish that nature cannot produce such effects or that every gravitational quantum-switch proposal requires exactly this timing precision.
Environmental decoherence is one major obstacle.
Joos and other researchers have studied how scattering by environmental particles and radiation can suppress coherence between spatially separated states. In simplified models, the off-diagonal coherence can decay approximately as
ρ(x, x′; t) ≈ ρ(x, x′; 0)e^(−Λ(x − x′)²t),
where Λ is a decoherence coefficient appropriate to the model and environment.
Writing Δx = |x − x′|, the corresponding characteristic time is
τ_dec ≈ 1/(ΛΔx²).
To put numbers on it, Joos and Zeh estimated Λ for objects scattering the cosmic microwave background, which fills even the emptiest intergalactic space. For a dust grain about 10 micrometres across (a = 10⁻³ cm) they get roughly
Λ ≈ 10⁶ cm⁻² s⁻¹,
so for a separation equal to its size, Δx = 10⁻³ cm,
τ_dec ≈ 1/[10⁶ × (10⁻³)²] s = 1 s.
Λ isn't a universal constant, though. It depends on the object's size and on the radiation, and for this kind of long-wavelength scattering it falls off steeply as the object shrinks. For a large molecule about 10 nanometres across (a = 10⁻⁶ cm), the estimate is Λ ≈ 10⁻¹² cm⁻² s⁻¹, so with Δx = 10⁻⁶ cm,
τ_dec ≈ 1/[10⁻¹² × (10⁻⁶)²] s = 10²⁴ s,
far longer than the age of the universe, about 4 × 10¹⁷ s. But a molecule like that is far too light to shift any clock's timing appreciably. The contrast illustrates the difficulty. Larger objects can produce more substantial gravitational effects, but they also tend to become entangled with their environments more readily. Smaller systems may preserve spatial coherence much longer, but their gravitational effects are correspondingly weaker. These particular estimates don’t establish a universal limit, and they don’t rule out more sophisticated gravitational quantum experiments or naturally occurring coherent processes. These are order-of-magnitude estimates, valid when Δx is much smaller than the radiation's wavelength (about a millimetre for the microwave background), which holds in both cases.
There’s also research showing that decoherence isn’t confined to ordinary laboratory environments. Danielson, Satishchandran and Wald investigated decoherence associated with Killing horizons, including effects relevant to black holes and certain other spacetime settings.
These results show that maintaining quantum coherence in gravitational settings can be difficult for reasons extending beyond familiar laboratory noise.
But none of this proves that spontaneous indefinite causal order cannot occur in nature.
It would be a mistake to argue that because the laboratory arrangements are delicate, the universe must never produce anything analogous. Nature is not limited to the apparatuses we know how to construct. At the same time, one cannot infer natural ICO simply because quantum gravity might permit it.
As far as established observations go, we have laboratory evidence for operational indefinite causal order, but no confirmed observation of its spontaneous occurrence in nature, whether since the Solar System formed or earlier.
The deeper possibility involves quantum superpositions of spacetime geometry.
Suppose the gravitational field can occupy a coherent superposition of configurations represented schematically by
|Ψ⟩ = α|g₁⟩ + β|g₂⟩.
If the two geometries produce different causal relationships between relevant interventions, the combined process might not admit a single definite causal order of those interventions.
The proposal sometimes called a gravitational quantum switch investigates this possibility. Zych, Costa, Pikovski and Brukner studied a gravitational approach to testing temporal order, and Castro-Ruiz and colleagues examined quantum clocks and the temporal localization of events in the presence of gravitating quantum systems.
The idea is that the gravitational field itself could participate in coherently controlling which operation precedes another.
Unlike an ordinary photonic switch built in a fixed classical spacetime, such a proposal raises the possibility that the relevant causal structure is associated with quantum geometry rather than merely the paths of a target system through a fixed apparatus.
But the gravitational quantum switch remains a proposal, not an experimentally established demonstration of fundamentally indefinite spacetime causal order.
Even a successful future experiment would need careful interpretation. One would have to establish what class of definite-order descriptions its results actually exclude.
And the mathematical expression
α|g₁⟩ + β|g₂⟩
is only schematic. In a full quantum-gravity theory, identifying physical geometries, defining observables, and comparing events across different geometrical configurations are themselves nontrivial problems.
This brings us back to the question about time itself.
One possibility is that indefinite operational causal order reflects something genuinely fundamental. Perhaps there is no deeper fact specifying which of two operations came first, because the physical theory simply does not contain such a fact.
If that turned out to be correct at the level of fundamental spacetime structure, it would challenge the idea that every physical event belongs to one universally definite causal ordering.
But it wouldn’t necessarily mean that time doesn’t exist, that ordinary causality is an illusion, or that every event in the universe lacks a definite temporal relationship. A theory could have indefinite order in some circumstances while retaining well-defined causal relations in others.
Another possibility is that operationally indefinite order emerges from a deeper physical description with definite ordering. That ordering might be expressed through finer-grained spacetime events, additional physical variables, or some structure not directly represented by the operational process.
Such a theory would have to reproduce the observed interference and causal-correlation statistics. It couldn’t simply replace the quantum switch with an ordinary random choice between A-before-B and B-before-A.
A third possibility is that our question about which operation “really happened first” isn’t well defined independently of the physical description being used. In that case, the problem may not be that a fact is hidden, but that we’re trying to assign a single ordering relation to objects that don’t possess one in the relevant theory.
There is also an important distinction between temporal order and causal order. Special relativity already tells us that the chronological order of spacelike-separated events can depend on the reference frame, while their causal relationship remains constrained by the light-cone structure. Quantum indefinite causal order is not simply another name for relativity of simultaneity.
And none of these results, by themselves, settles the philosophical debate between presentism and eternalism. A definite causal structure does not establish that only the present exists, just as an indefinite operational causal structure does not establish that past, present and future all exist equally.
One could also consider a generative view of time in which physical reality has one realized history, produced through successive stages, while certain quantum operations lack a definite ordering at the operational level. That is a possible interpretive program, not an experimentally established conclusion. It would need to specify the underlying dynamics and show that they reproduce the relevant quantum predictions.
This is close to the distinction between the physical state of a system and the truth of propositions about its history.
