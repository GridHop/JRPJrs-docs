where g_μν is the metric (sign convention −,+,+,+). That's local: it orders and measures events along one worldline and says nothing about anything off it. Andersson, Galloway and Howard (1998) built a global time out of it. At any event p,

τ(p) = sup { L(λ) : λ a past-directed causal curve from p }

which is the longest proper time that could have elapsed along any causal path reaching p from its past. When τ is finite everywhere and goes to zero along every causal curve traced back as far as it goes, they call it regular, and they proved several things about it. It's a time function, meaning it strictly increases along every future-directed causal curve:

p causally before q ⟹ τ(p) < τ(q)

Its level sets, the surfaces τ = constant, are future Cauchy surfaces: every worldline that continues past one crosses it exactly once, and every causal path traced back from a later event runs through it. (They're future Cauchy surfaces rather than full ones: a worldline that ends early, say at a black hole's singularity, never reaches the later slices.) And it's fixed by the geometry alone: once you adopt this definition, no coordinates or observers enter, and its values are settled. You could relabel the slices with any strictly increasing σ = F(τ), which changes the numbers but not which events share a slice. So a τ-slice is a cut of the loaf chosen by the loaf's own shape, spatially whole and temporally an instant. In that sense it really is an instant of the universe as a whole.

A common objection is that spacetime has no intrinsic time at all, that time and space only appear once a coordinate system is chosen, and that the metric itself presupposes one. That runs together the metric and its components. The metric is a tensor field g: at each event it takes two directions and returns a number, with no coordinates involved, and g_μν dx^μ dx^ν is just that object written out in one particular chart. Change charts and the components change,

g′_μν = (∂x^α/∂x′^μ)(∂x^β/∂x′^ν) g_αβ

in exactly the way that leaves the interval unchanged. A flat sheet of paper shows the same thing. In Cartesian coordinates ds² = dx² + dy², and in polar coordinates ds² = dr² + r² dθ². The components are different, but the distance between any two marked points comes out the same either way. You need some chart to compute a number, the way you need some ruler, but which one you pick doesn't change the answer. Nature doesn't need a chart at all: a clock carried along a worldline measures its proper time without consulting any coordinates, which is why the twins' age difference is a plain fact.

Nor is the metric neutral between time and space. At every event it sorts directions into three classes: timelike if g(v, v) < 0, null if g(v, v) = 0, and spacelike if g(v, v) > 0. That's the light cone, and no change of coordinates or orientation ever moves a direction from one class to another. It isn't a measurement bias either. The signature is what makes the field equations hyperbolic, which is what lets anything propagate. The wave equation

−(1/c²) ∂²ψ/∂t² + ∇²ψ = 0

carries signals at speed c. Flip the sign to make time just another direction,

(1/c²) ∂²ψ/∂t² + ∇²ψ = 0

and you get a four-dimensional Laplace equation, which is elliptic: it doesn't describe finite-speed wave propagation at all, and, as Hadamard showed, trying to evolve it from one slice to the next is ill-posed, since arbitrarily small changes in the data produce arbitrarily large changes in the solution. Whether empty space is fully isotropic in four dimensions or has Lorentz symmetry is also an empirical question, because the two make different predictions. Full isotropy would put time and space directions on an equal footing, with no light cone and so no speed limit built into the geometry. What we observe, in every test of special relativity from Michelson–Morley onward, is a universal speed limit and time dilation: rotations and boosts mix directions within each class, never across the cone. It's true that empty, flat spacetime singles out no particular timelike direction, so it has no preferred frame. Separately, its cosmological time is infinite, because causal paths of arbitrarily long proper time reach every event. But even there, time and space are not interchangeable. And the geometry doesn't need any predefined reference. Hawking, King and McCarthy (1976) and Malament (1977) showed that, under mild causality conditions, which events can send signals to which, a purely physical relation, fixes the spacetime geometry up to a local scale factor, and clocks supply the scale.

Einstein's hole argument points the same way. Its lesson, on the standard reading from Einstein's own resolution through Earman and Norton's revival of it in 1987, is that bare manifold points have no physical identity apart from the metric and the matter. What's physical is whatever diffeomorphisms, smooth reshufflings of the points, leave unchanged. Diffeomorphisms never change the signature or the light cones, and cosmological time is exactly that kind of invariant, built from the metric alone. If φ is any diffeomorphism and φ*g the reshuffled metric, then

τ_{φ*g} = τ_g ∘ φ

so the reshuffling just carries τ along with the events, and every relation such as "these two events have the same τ" survives untouched. If you'd rather call the metric content than geometry, as many relationalists do by treating it as the gravitational field, nothing here changes. Our universe has that content, and the distinction between time and space is a feature of it, not of our measurements. What has no time or space at all is a bare manifold with the metric stripped away, and that isn't a vacuum; it just isn't spacetime.

In an idealized expanding universe with the FLRW metric

ds² = −c² dt² + a(t)² dΣ²

beginning in a Big Bang (a(t) → 0 as t → 0), τ is just the cosmic time t, the proper time of observers who ride along with the expansion. That's what "the age of the universe" means, about 13.8 billion years. The cosmic microwave background is the strongest evidence that our universe is close to this picture. It has the same temperature in every direction to about one part in 100,000 once our own motion is removed, and it cools with the expansion as

T(z) = T₀ (1 + z)

with T₀ ≈ 2.725 K, a relation that has been checked out past redshift 1. So comoving observers anywhere who measure the same background temperature are at the same cosmic time, to good approximation, without anyone ever synchronizing anything. The dipole in that radiation, about 3.36 mK, is our own motion at roughly 370 km/s relative to the comoving frame, the frame whose clocks keep cosmological time to good approximation.

Now, gapless. Andersson, Galloway and Howard showed that a regular τ is continuous (in fact locally Lipschitz). A continuous function on a connected spacetime takes all the values in between any two it takes, so the values of τ fill an unbroken interval. Since τ is positive everywhere and goes to zero toward the past without ever reaching it, that interval is

0 < τ < T

where T is infinite if the universe expands forever, as the standard model says ours does. So no cosmic time is skipped: between any two slices there's a slice for every value in between. The same holds along every worldline. If a future-directed worldline λ runs from τ = a to τ = b, then τ along it is continuous and strictly increasing, so for every c between a and b there's exactly one point on λ where τ = c. No worldline jumps over a slice.

Notice also what the open bottom end means. There's no first slice. The beginning is a boundary of the loaf, not an instant in it, so cosmic time starts without a first moment, the way the numbers greater than zero have no smallest member.

Two things can look like gaps but aren't. The first is the shape of the slices. In a lumpy universe τ stops being smooth where the longest-time paths from the past stop being unique, so the slices can pick up creases. Near a black hole, a slice can run up against the singularity, which isn't a place in spacetime but marks where spacetime stops, so the slice is left incomplete there, and a worldline that ends at the singularity simply stops crossing later slices; that's something ending, not time skipping. More generally, regularity alone doesn't guarantee that every slice is smooth or even connected. None of that is a gap in time: gaplessness is about τ's values, which still fill an unbroken interval, and about each worldline, which still passes through every value between any two it reaches. The second is an endless past. If causal paths reaching an event could have unboundedly long proper times, as in some models where the past goes on forever, τ would be infinite there rather than gappy, and you'd count instead from some physically distinguished slice, such as a bounce.

The real open question is the smallest scales. Continuity is a feature of spacetime as general relativity describes it, and nobody knows whether that description holds down to the Planck time,

t_P = √(ħG/c⁵) ≈ 5.39 × 10⁻⁴⁴ s.

Some approaches to quantum gravity, causal sets for instance, make spacetime fundamentally discrete. It's worth separating two senses of "gapless" here. If it means continuous, that's what's open at the Planck scale. If it means that each instant follows the one immediately before it with nothing in between, that could still hold in a discrete world, as long as that world has whole-universe instants at all; there'd just be a smallest step. Some discrete approaches, causal sets among them, don't come with global instants, only a discrete web of before-and-after relations, and there the question would have to be restated.

Now, co-occurrence. Read the time-function property backward: two different events with the same τ can't be causally related, so they're spacelike-separated. A τ-slice therefore holds exactly one moment of every worldline that reaches that cosmic time, and none of those moments can affect any other. That includes galaxies beyond our horizons, ones we've never exchanged a signal with and, beyond our event horizon at roughly 16 billion light-years, never will.

