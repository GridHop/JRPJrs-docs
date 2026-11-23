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

where Φ is the gravitational potential, negative inside a well. At present our motion relative to the cosmic background, about 370 km/s, costs our clocks roughly v²/2c² ≈ 7.6 × 10⁻⁷, about 24 seconds a year, and the gravitational wells we sit in add more. More generally, if Sₐ is the surface where τ = a, then for any event q with τ(q) ≥ a,

τ(q) = a + d(Sₐ, q)

where d(Sₐ, q) is the longest proper time along any causal curve from Sₐ to q. So between cosmic times a and b, no clock anywhere can accumulate more than b − a. Measured against cosmological time, local clocks run at or below it and never above. When you compare two local clocks with each other, one can look stretched relative to the other, but against the common time they all sit at or under the same ceiling.

Here's a way to picture it. In a universe with a Big Bang, imagine indestructible clocks started there and carried along every possible path, so there's one at every location and none ever stops. When you look at them, they disagree, because they've moved differently and sat in different gravitational wells. Now pick any event, look at all the clocks that could have gotten there, and take the one showing the most elapsed time. That reading is τ at that event. And that top reading is actually achieved, not just approached: when cosmological time is regular, a theorem guarantees a freely falling path from the initial singularity to every event that realizes the maximum. The clocks that come out on top are the ones that never fought the expansion and just rode along with it: the comoving ones. What makes their time common is that, in a homogeneous universe, all the comoving clocks read the same at the same cosmic moment everywhere, without anyone ever synchronizing them. They agree because they all started at the same beginning and the universe has been the same everywhere on average ever since. Every other clock reads less than that common value. So the "oldest clock" reading isn't any one clock's private time. It's the ceiling all of them share, and every local clock's shortfall is measured against it.

This isn't just a thought experiment, because the universe gives us something very close to that common clock: the cosmic microwave background. It's the light left over from when the universe became transparent, about 380,000 years after the Big Bang, and it fills every location. It lines up with cosmological time in three ways.

First, it's the same in every direction to about one part in 100,000 once you take out the effect of our own motion, and its spectrum is the most perfect blackbody ever measured in nature. COBE's FIRAS instrument found deviations below about 50 parts per million of the peak, with a temperature today of T₀ = 2.72548 ± 0.00057 K. A blackbody that clean means the radiation was once in thermal equilibrium throughout the region we can see, which is the common hot early phase that the comoving clocks share. Uniformity that good is also what makes the idealized FLRW picture a good approximation to our universe, and that picture is where cosmological time coincides with the proper time of comoving clocks.

Second, the temperature works as a clock. As the universe expands, the radiation cools as T ∝ 1/a(t), so at redshift z it should be

T(z) = T₀ (1 + z)

