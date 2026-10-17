# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 01 of 40 (1,575 words)

QUANTUM REFERENCE FRAMES AND SINGLE-OUTCOME DYNAMICS



A Compatibility Framework for Generative Presentism



====================================================================================================



ABSTRACT



Quantum reference frames (QRFs) permit different quantum systems to serve as reference frames,

raising a foundational question for single-outcome theories: how can frame-dependent descriptions

represent one objectively realized history? Cosmic-Time Generative Presentism (CTGP) holds that only

the present exists, that physical reality is generated through successive stages, and that truths

about the determinate past are grounded in primitive past-tensed properties of the present world. We

develop a mathematical compatibility framework connecting these commitments to QRF covariance,

stochastic quantum instruments, and relativistic measurement theory.



We first construct an explicit QRF-covariant, single-outcome quantum model using relational GRW-type

events and a Lucretian truth profile. We establish a frame-independent determinacy criterion,

characterize when different frame descriptions identify the same complete physical state and

realized history, and prove covariance of the generative law and its history probabilities. We

distinguish physical-state identity, historical identity, and observational indistinguishability,

and show that the present quantum state need not determine the complete past. The construction

demonstrates the joint mathematical consistency of these commitments without deriving their

ontological interpretation or establishing physical adequacy.



We then formulate a compatibility program for relativistic quantum field theory, quantum clocks, and

quantum gravity. For specified causally local instruments, we establish conditions for foliation-

independent outcome histories and operational no-signaling. Free-field detector and Gaussian-

collapse constructions identify both sufficient conditions for causal admissibility and obstructions

to extending them to arbitrary local operations and to covariantly located collapses. We calculate

the energy–momentum cost of Gaussian collapse and examine, without adopting it, a cosmological-time-

guided candidate that defines normalized finite-volume dynamics but introduces preferred-frame

structure.



To distinguish formal collapse prescriptions from physical implementations, we compare centre-time

ordering, completion-time ordering, and a local field–pointer coupling. The pointer construction

yields foliation-independent statistics, reproduces ordered-collapse predictions for causally

orderable configurations with suitably prepared pointers, and defines a consistent law of outcome

records even in spatially infinite universes. Interfering collapse regions, however, produce

different joint outcome laws, showing that this local coupling does not in general reproduce a

prescribed collapse ordering. Definite pointer readings require an explicit single-outcome

postulate, and infinite-volume generation of the physical state remains open. We also give clock-

neutral descriptions of late-record instruments for two ideal clocks and exhibit interference

between alternative clock-dependent interaction orders.



These results establish a concrete mathematical compatibility framework, not a completed

relativistic theory or an empirical confirmation of CTGP. They separate frame-dependent descriptions

from the identity of realized events, identify which features of single-outcome dynamics survive

changes of reference frame and foliation, and isolate the additional physical requirements for

relativistic collapse, temporal quantum reference frames, and quantum gravity.



Keywords: presentism; generative presentism; Lucretianism; quantum reference frames; perspective-

neutral framework; objective collapse; GRW; flash ontology; quantum instruments; quantum jump

processes; single-outcome realism; determinacy; truth preservation; non-supervenience; relativistic

quantum field theory; foliation independence; particle detectors; measurement models; Gaussian

collapse; impossible measurements; no-signaling; Poisson point processes; collapse energy; temporal

quantum reference frames; quantum clocks; clock-neutral instruments; quantum gravity; cosmological

time; preferred frames; philosophy of time



READER’S GUIDE



Three layers of claim run through this preprint and should be kept distinct. Layer 1 is established

mathematics adopted without modification: the perspective-neutral framework for quantum reference

frames with a finite symmetry group, quantum instruments (Kraus operators) for stochastic single-

outcome dynamics, and piecewise-deterministic quantum jump processes in continuous time. Layer 2

consists of the definitions proposed here: the complete ontological state, the space of admissible

histories, the determinacy criterion, the cross-frame identification criterion, and the validity

condition for frame-relative laws. Layer 3 is the concrete model of Part III, which shows that the

Layer 2 definitions are jointly satisfiable by an explicit dynamics. Part V adds a further kind of

material, a research program, whose items are labeled by status: proved theorems and propositions,

definitions offered as proposals, and conjectures or targets that remain open.



Three kinds of result should likewise be kept apart. An existence result says that at least one

model in a specified class satisfies a given set of commitments. A general compatibility result

would say that every physically admissible QRF theory can accommodate those commitments. A physical

adequacy result would say that the model reproduces the relevant features of established quantum

physics and relativity. This preprint establishes an existence result. It does not establish the

other two, and §17 states precisely why not.



Interpretation enters at identifiable points, and those points are flagged in the text. The theorems

are mathematical consequences of the definitions. The claims that the perspective-neutral state and

the truth profile represent what exists, and that each orbit of frame descriptions represents one

realized present with one history, are interpretive theses (Ontological Reading 4.3 and Thesis

5.10). They are what CTGP adds to the mathematics, and they are argued for rather than derived. The

spaces of histories and the probability measures over future trajectories used throughout are

mathematical representations of possibilities; they do not assert that past or future stages exist

(§4.5).



Part I (§§1–2) states the problem and the background. Part II (§§3–5) develops the general formalism

for any finite symmetry group. Part III (§§6–10) builds the concrete model in discrete-stage and

continuous-time form and checks CTGP’s further requirements. Part IV (§11) identifies what CTGP adds

beyond QRF covariance. Part V (§§12–16) sets out the compatibility program for relativistic quantum

field theory, temporal quantum reference frames, and quantum gravity. Part VI (§§17–19) states the

scope of the results and the open problems, and maps the results back to the original questions.

Appendix A collects the frame-relative forms used in the model. Appendix B contains the verification

script for the model and the finite theorems, with its output and the information needed to

reproduce it, and Appendix C contains separate scripts for the results of §§13.8–13.11 and §14.5.



Nothing here modifies the CTGP postulates, and nothing here is an empirical result. The aim is to

replace schematic statements about CTGP and quantum theory with definitions precise enough to be

proved or refuted.



====================================================================================================

PART I. The Problem

====================================================================================================



----------------------------------------------------------------------------------------------------

1. Introduction

----------------------------------------------------------------------------------------------------



CTGP claims that the present stage of the universe is all that exists, that it is generated from the

preceding stage by physical law, and that truths about the past are grounded Lucretian-style in the

present world’s primitive past-tensed properties: the present world has the property *having been,

at stage σ′, such that φ* (CTGP – explained, §5.2.1 and Definition 17.20). Because it entails a

unique factual past, CTGP requires single-outcome realism in quantum theory, which excludes the

standard Everettian ontology, and it rejects relational interpretations on which facts are relative

to observers (CTGP – explained, §10.1).



Quantum reference frames put pressure on this combination. In the QRF literature (Giacomini, Castro-

Ruiz & Brukner 2019; Vanrietvelde, Höhn, Giacomini & Castro-Ruiz 2020; de la Hamette & Galley 2020),

there is no external classical reference frame: a physical system is described relative to another

quantum system. A system in a definite position relative to one frame can be in a superposition, and

entangled, relative to another. Three questions then arise for CTGP. Is determinacy frame-relative?

If two frames describe the present differently, what makes them descriptions of one present and one

history? And where do the Lucretian past-tensed properties sit relative to a quantum state that has

many frame-relative descriptions?



A prior analysis of these questions proposed the schematic representation



        Ω_σ = (S_σ, L_σ),   S_{σ′} ∼ K(S_{σ′} | S_σ),   L_{σ′} = L_σ ∪ ΔL_{σ→σ′},



in which S_σ is the present physical state governing successor-state generation, L_σ is the present

world’s Lucretian past-tensed truth profile, K is a stochastic generative law, and ΔL_{σ→σ′}

represents the truths newly acquired about what occurred during the transition. It drew a key

distinction: CTGP’s unique factual history must be grounded in the chosen single-outcome quantum

ontology, and L represents truths about the history actually generated rather than serving as an

independent mechanism that determines which history occurs. It identified four tasks:



    (T1) Which propositions are determinate under the chosen quantum ontology.



    (T2) How corresponding physical facts are identified across quantum reference frames.



    (T3) Whether valid QRF transformations preserve the truth of those corresponding propositions.



    (T4) How Lucretian past-tensed properties relate to the physical quantum state without

    introducing unjustified dynamical assumptions.



It added a fifth requirement: a QRF-compatible single-outcome model must also satisfy CTGP’s

requirements of definite generative ordering and generability (T5). It also posed the question at

the heart of T2: how can one establish that two frame descriptions refer to the same realized

history, rather than simply assuming that they do?



This preprint addresses all five tasks by construction. It specifies a class of QRF-covariant,

single-outcome stochastic quantum dynamics, shows that every member of the class admits a CTGP

interpretation, and proves what that interpretation implies. The strategy has three parts. First,

the underlying present state lives in the perspective-neutral (gauge-invariant) Hilbert space of the

QRF framework, and frame descriptions are obtained from it by unitary reduction maps. Second, the

single-outcome dynamics is a stochastic quantum instrument whose operators are invariant under the

symmetry group, so that each outcome is a frame-independent event; this is a relational version of

the flash ontology of the Ghirardi–Rimini–Weber (GRW) collapse model (Ghirardi, Rimini & Weber 1986;

Bell 1987; Tumulka 2006). Third, the truth profile L is defined as the past-tensing of the realized

states and events, so that it is generated by the dynamics rather than feeding into it, and the

space of admissible profiles is specified exactly.
