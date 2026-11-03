Some proposals push in this direction. Hartle and Hawking's no-boundary proposal, for instance, tries to make the universe's initial quantum state a matter of law rather than input. Even so, what it aims to yield is probabilities for different possible courses of cosmic events, not one detailed course of events, and it isn't established.

More generally, even a theory with a single solution would still need observation to confirm it describes our world rather than just a consistent mathematical one, because a uniqueness proof says nothing about which model reality matches. And bare math doesn't even say what its symbols stand for. It takes rules linking them to observables to turn equations into a physical theory at all.

There's also the "per given time" aspect of the question. In all of these equations, t is just a parameter. Nothing in x(t) = x₀ + v₀t marks any particular value of t as now. That's true even in Newtonian physics with absolute time: absolute time gives you a single ordering of instants, but the equations don't say which instant is present. Einstein reportedly told Carnap that this bothered him, that physics has no place for the Now. So the math can't, on its own, even sort events into past, present, and future. That sorting has to come from outside the equations. Whether only the present exists is a question the equations stay silent on either way.

So the second description is the accurate one, for past, present, and future alike, as long as "math alone" means the laws without empirical input. The laws reveal constraints on possible existence, sometimes drastic ones. But no current established theory's laws supply the conditions and parameters needed to single out our universe's actual course of events. On their own, they leave many possibilities open at every time, including the present.

Supply complete data at one time, and a deterministic theory with well-behaved equations can narrow things to one in both directions, subject to Laplace's demon's limitations. Even then, the specifics at the time you supplied data for come from the data, not the math. Uniqueness can fail toward the future or the past, chaos limits prediction and retrodiction alike, and a unique mathematical solution still has to be checked against reality. In indeterministic theories, even complete data leaves a spread of possibilities.

In short, the laws constrain what can be the case at any time, past, present, or future, often severely, but they don't by themselves determine which events were, are, or will be the case.

Is "numerical identity" via "'measure of time' plus 'persistence conditions'"?

Yes, as long as "measure of time" means what it should mean, which is time's order and its magnitude, and not the act of reading a clock. Numerical identity across times comes from the order of time plus the persistence conditions of whatever kind of thing you're talking about. Magnitude comes in only when those conditions say something about duration. Clock readings and records are how we find out about identity, not what makes it the case. Each piece of that needs unpacking, so here's the longer version.

Numerical identity means being one and the same thing, as opposed to qualitative identity, which means being exactly alike. Two freshly minted coins can be qualitatively identical and still be two coins. At a single moment numerical identity is trivial, since everything is identical to itself and time doesn't come into it. The interesting question is identity across times: what makes the thing here now the same thing as the one here last year. That's the question of persistence, and that's where time comes in.

By "the measure of time" I mean two things that are easy to run together. The first is order: which stage comes before which. The second is magnitude: how much time separates them. Aristotle had both in his definition, time as "the number of motion with respect to before and after," while Leibniz's leaner version, time as "the order of successive things," keeps only the first. You can see they're different because you can change one without the other. Take any labeling of moments by τ and relabel it with σ = F(τ), where F is any function with F′ > 0. Every before and after stays exactly where it was, so the order is untouched, but every duration has been distorted. Order alone never tells you how long anything took. Precision is a third thing again. "The 21st century" and "2/4/2010" differ in how finely they locate something, but both already rely on magnitude, since a century and a day are units of duration. And the measure of time isn't the same as measuring time. Measuring is something a clock does, and it presupposes an order and a magnitude for it to measure. Weighing a rock tells you its mass, but the rock had that mass before anyone weighed it.

It's also fair to ask what makes an order temporal at all, since points along a ruler are ordered too. Being able to tell one event from another isn't enough, because two distinct events can happen at the same time. What makes an order temporal is succession: its members aren't co-present, each comes after the one before, and on the view that only the present exists, the earlier stage no longer exists once the later one does. Time also isn't the same as the state of things at a time, which is why it makes sense to ask "at what time did that state occur?" The same kind of state can occur at two different times, and a periodic clock shows the same reading at different times, so the time can't simply be the state.

Now, cosmological time. In relativity every clock measures its own proper time, the time elapsed along its own path through spacetime, its worldline. For a path γ, that's

L(γ) = (1/c) ∫ √(−g_μν dx^μ dx^ν)

where g_μν is the metric (sign convention −,+,+,+). Two clocks that start together and later meet again can disagree about how much time went by. That's the twin effect, and when the twins compare readings side by side, nobody in any frame disputes what the clocks say. Proper time is local, though. Cosmological time is built from it but is global. At any event p it's defined as

τ(p) = sup { L(γ) : γ a past-directed causal curve from p }

which in words is the longest proper time that could have elapsed along any causal path reaching p from its past; if the past has a beginning, that's the longest time since the beginning. Andersson, Galloway and Howard worked this out in 1998. When τ is finite everywhere and goes to zero along every causal curve traced back as far as it goes, they call it regular. Regularity is what makes it well behaved. It forces the spacetime to be globally hyperbolic, which among other things rules out closed timelike curves, so "earlier" and "later" can never loop back on themselves. And the surfaces of constant τ slice spacetime into whole-universe "nows": every worldline that continues past one crosses it exactly once, and every causal path traced back from a later event runs through it, so nothing off the slice can influence what comes after it. (Technically they're future Cauchy surfaces, not always full Cauchy surfaces, because a worldline that ends early, say at a black hole's singularity, never reaches the later slices.) So cosmological time isn't a second kind of time competing with proper time. It is proper time, taken at its maximum.

That definition does depend on the past being finite in the right way. If the past goes on forever in proper time, so that causal curves reaching p can have unboundedly long proper times, then

τ(p) = +∞

and if the universe is uniform on large scales, that's true at every point, so τ has no finite value anywhere. The flat, empty spacetime of special relativity is the textbook case. That isn't a flaw in the idea, just a fact about which spacetimes have a cosmological time. Whether ours does is open. The standard cosmological model, which the CMB supports, gives a finite, regular τ. It does so only by extrapolating back to a(t) → 0, beyond the epochs observations test, and some live proposals for the earliest history, such as a bounce or a long or endless phase before the hot Big Bang, would make τ infinite. So nothing below assumes our universe's past is finite. Here's the condition once, for everything that follows: what I say about τ in general holds in any spacetime where τ is regular, and what I say about τ in our universe holds on the standard model. Whether time has an end doesn't matter, since τ only looks backward. And nothing in the account of identity below depends on time having a beginning or an end. Order and magnitude, and particular times and intervals, make sense either way. What a regular τ provides is one common standard for them, set by the geometry itself. In a hypothetical universe with an endless past, you'd have to measure from some physically distinguished slice instead, such as the moment of a bounce, taking the longest proper time from that slice rather than from a beginning. That standard would be only as good as the slice is distinguished. For our universe this fallback is close at hand. The standard model assigns only minutes to everything before the earliest epoch we test directly, the formation of the first light nuclei. So the figures below, such as the 13.8 billion years, are, to within those minutes, the longest proper time since that epoch, whatever came before it.

In an idealized expanding universe with the FLRW metric

ds² = −c² dt² + a(t)² dΣ²

that begins in a Big Bang, with a(t) → 0 as t → 0, the cosmological time is just t, the proper time of observers who ride along with the expansion, the comoving observers. That's what cosmologists mean by the age of the universe, about 13.8 billion years. (Without such a beginning the same metric can give τ = ∞, as de Sitter expansion, a(t) ∝ e^(Ht), does when its t runs back without limit.) In our actual, lumpier universe, τ's slices still exist; only their match with comoving clocks is approximate.

A clock that moves relative to the comoving observers accumulates less time. In FLRW, a clock with peculiar velocity v, measured by the local comoving observers, ticks at

dτ = dt √(1 − v²/c²)

and in a weak gravitational field you get approximately

dτ ≈ dt (1 + Φ/c² − v²/2c²)

