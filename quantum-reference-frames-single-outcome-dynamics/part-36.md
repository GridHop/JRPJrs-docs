# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 36 of 40 (1,615 words)

Appendix C. Verification of the Collapse and Two-Clock Results

----------------------------------------------------------------------------------------------------



The results of §§13.8–13.11 and §14.5 are checked by two separate scripts, one for each branch of

the program, so that each can be rerun and audited independently of Appendix B. As there, the checks

confirm the analytical results in specific instances and guard against sign and ordering errors.

They do not prove anything about all states, all configurations, or the continuum. Table C.1 lists,

for each check, the quantity computed, the identity tested, the result, and the analytical argument

that establishes the identity.



Item  | Quantity and identity tested                   | Result                   | Proved in

------+------------------------------------------------+--------------------------+---------------

C1    | Unread Gaussian channel: Kraus integral and    | max dev 2.4 × 10⁻¹⁴ and  | Prop. 13.15

      | kick mixture vs exp(−(a − a′)²/(8σ²))          | 7.8 × 10⁻¹⁶              |

C2(a) | Position collapse, anharmonic potential: ΔE =  | 12 digits, both states   | Prop. 13.16(a)

      | ħ²/(8mσ²) in the ground state and in a random  | and cutoffs              |

      | state                                          |                          |

C2(b) | Two coupled modes, A linear: ΔE =              | 12 digits, both states   | Prop. 13.16(b)

      | −[A,[A,H]]/(8σ²) in the vacuum and in a random |                          |

      | state                                          |                          |

C2(c) | Lattice field: double commutator vs Fourier    | relative diff. 5 × 10⁻¹⁶ | Prop. 13.16(c)

      | formula                                        |                          |

C2(d) | ΔP(Λh) = Λ ΔP(h) under a boost; ΔP timelike    | 1.3 × 10⁻¹⁶; timelike    | Prop. 13.16(c)

C3(a) | Poisson counts in a box: mean and variance     | 96.00 and 96.35          | Def. 13.20

      | both equal to λ × area = 96                    |                          |

C3(b) | Probability of admissibility against the cell  | below the bound; 0.599   | Prop. 13.22

      | bound                                          | to 0.015                 |

C3(c) | Outcome covariance across linear extensions,   | max diff. 1.8 × 10⁻¹⁵    | Thm 13.21(a)

      | 300 admissible configurations                  |                          |

C3(d) | Direct Hilbert-space history laws: across      | 4.8 × 10⁻¹⁶; 1.8 × 10⁻¹⁴ | Thm 13.21(a)

      | linear extensions; vs closed-form              |                          |

      | characteristic function                        |                          |

C3(e) | Overlapping pair: variance shift E²/(4σ_1²);   | 10 digits; TV 0.057;     | Props 13.23,

      | distance between the two orders; unread        | states agree to          | 13.28(e)

      | channels in either order give the same state   | 6.8 × 10⁻¹⁵              |

C3(f) | Non-admissible configurations ordered by       | laws differ in 234 of    | Prop. 13.23

      | centre time in two frames                      | 300                      |

C3(g) | Centre-time order is a linear extension of the | 300 of 300               | Lemma 13.26(b)

      | causal order, 300 admissible configurations    |                          |

C3(h) | Time-ordered collapses, non-admissible Sorkin- | at most 1.6 × 10⁻¹⁵;     | Prop. 13.28(c)

      | type configuration: target law with and        | Lüders shift 8.1 × 10⁻⁴  |

      | without a causally separated kick, collapse,   |                          |

      | or Lüders instrument; Lüders negative control  |                          |

C4(a) | Gapless pointers: E = Γ − Γᵀ; phase of the     | exact; 0 between         | Prop. 13.31(a)

      | time-ordered coupling along two foliations,    | foliations; 9.0 × 10⁻³   |

      | and its approach to Γ                          | at 64 nodes per axis     |

C4(b) | Explicit pointers, overlapping pair:           | 7.3 × 10⁻¹⁴; 2.0 × 10⁻¹³ | Prop. 13.31(b)

      | characteristic function vs closed form, with   |                          |

      | and without the pre-chirp                      |                          |

C4(c) | Unread field channel vs two unread Gaussian    | 1.7 × 10⁻¹⁴              | Prop. 13.31(c)

      | collapses                                      |                          |

C4(d) | One-way pair: pointers vs sequential collapse  | 1.8 × 10⁻¹³; variances   | Prop. 13.31(d)

      | in causal order; overlapping pair: pointers    | differ by 0.0011 and     |

      | vs collapses in centre-time order              | 0.0537                   |

C.2   | Record keyed to A: P_phys = P_A = P_B at late  | 12 digits                | Prop. 14.5(c)

      | readings                                       |                          |

C.2   | One interaction per clock: record law =        | 12 digits                | Prop. 14.5(d)

      | mixture of the definite orders                 |                          |

C.2   | Offset-coherent observable: P(+) = (1 +        | 12 digits; 0.5           | Prop. 14.5(e)

      | Re⟨W_1ψ, W_2ψ⟩)/2 in all three descriptions;   |                          |

      | incoherent mixture of offsets                  |                          |



Table C.1. Checks of §§13.8–13.11 (script C.1) and §14.5 (script C.2), with the result each

instantiates.



Two analytical ingredients of the scripts should be stated. First, for a quasi-free state with

vanishing one-point function, the characteristic function of the outcomes of Gaussian collapses

applied in a given order follows from the identity ∫ e^{isy} K_y W(g) K_y dy = exp(−E(g, h)²/(8σ²) −

s²σ²/2) W(g + sh), applied from the last collapse to the first. The outcomes are then jointly

Gaussian with covariance



        C = Σ + diag(σ_m²) + Σ_m e_m e_mᵀ / (4σ_m²),



where Σ is the covariance of the smeared fields in the state, and (e_m)_{m′} = E(h_{m′}, h_m) if

collapse m′ follows collapse m in the order and 0 otherwise. When the order is a linear extension of

an admissible configuration, every nonzero entry of e_m belongs to a collapse in the causal future

of collapse m, so C does not depend on the linear extension; items C3(c) and C3(d) test this formula

against direct computation. Second, for a massless field in 1 + 1 dimensions the causal propagator

is E(t, x) = −(sgn u + sgn v)/4 in light-cone coordinates u = t − x and v = t + x, up to an overall

sign convention. For smearings that are products β(u)β(v) supported in causal diamonds, E(h_i, h_j)

therefore reduces to one-dimensional integrals. It equals zero exactly when the diamonds are

causally separated. Third, for the gapless pointers of Proposition 13.31, the retarded part of the

propagator is E_ret(t, x) = −θ(u)θ(v)/2, so Γ_kl also reduces to products of one-dimensional

integrals, and in a one-mode realization the field vector exp(−i Σ_k p_k φ(h_k))|0⟩ produced from

the vacuum at given pointer momenta is a coherent state. The script uses this to compute the joint

state of the field and the pointers on a grid of pointer momenta. The sums of item C4(a) place the

smearings on Gauss–Legendre nodes and add E over the pairs of nodes ordered by each foliation.



Reproducibility. The software is that of Appendix B: Python 3.13.16, NumPy 2.5.3, and SciPy 1.18.1.

Script C.1 runs in about four minutes, most of it in item C3(h), and script C.2 in about 5 seconds.

Seeds are 31 and 32 for the random states of item C2, 2027 for the configurations of item C3, and 5

for the system states of script C.2. Item C1 uses two oscillator modes with Fock cutoff 24 per mode,

A = 0.6 q_1 − 0.3 q_2 + 0.2 p_1 + 0.5 p_2, σ = 0.8, an outcome grid of step 0.01, and 80-point

Gauss–Hermite quadrature for the kicks. Item C2(a) uses m = 1.7, ω = 1.3, V(Q) = ½mω²Q² + 0.2 Q⁴, σ

= 0.7, and cutoffs of 140 and 180 quanta. Item C2(b) uses the modes of C1 with the coupling matrix

((1.3, −0.4), (−0.4, 0.9)). Item C2(c) uses a periodic lattice of 48 sites with mass 0.6, σ = 0.9,

and a product smearing of half-widths 2.5 in time and 3 sites in space. Item C2(d) uses mass 1, σ =

0.9, and a boost of rapidity 0.5. Item C3 uses causal diamonds of half-size 0.5 with smearings

scaled by 4. The intensities are 6 in C3(a), 1.5 in C3(b) and C3(f), and 0.4 in C3(c), in square

boxes of side 4, 1 to 2.5, 2, and 4, and the three-collapse configurations of C3(d) are drawn

uniformly in a box of side 1.6. Item C3(h) uses diamonds with light-cone centres (u, v) = (0, 0),

(−0.525, 1.2), (−0.225, 1.05), and (−1.05, 2.3) for j, c1, c2, and y, smearings scaled by 8, widths

0.8, 0.9, and 1 for c1, c2, and y, a kick W(3 f_j), a Gaussian collapse of width 0.8, or the unsharp

Lüders instrument of Example 13.10 at j, a two-mode Fock realization in which φ(h_j) and φ(h_y) act

on different modes, with cutoffs of 36 and 44 quanta per mode, and, as the negative control, the

same Lüders instrument at c1. Item C4 uses the overlapping pair of C3(e) and a one-way pair with

centres (t, x) = (0, 0) and (1.2, 0.3), smearings scaled by 4, pointer widths 0.8 and 0.9, 81

momenta per pointer with spacing 0.12, the one-mode realization with cutoff 140, the foliations by t

and by cosh(0.6) t − sinh(0.6) x, and 32 and 64 Gauss–Legendre nodes per light-cone axis. The widths

σ are drawn uniformly from [0.5, 1.2] in C3(c) and fixed at 0.8, 0.9, and 1.0 in C3(d). Items C3(d)

and C3(e) use a one-mode Fock realization of the commutation data with cutoff 140 and outcome bins

with edges −0.7, 0, and 0.7. Items C3(c) and C3(f) use quasi-free states with covariance ½|E| + 0.3.

In script C.2 the clocks are ideal, the grid step is 0.01, and the wave packets in the offset are

smooth bumps of half-width 0.25. Case 3 of script C.2 uses one system state in both offset packets.

Throughout, smooth bumps are exp(−1/(1 − z²)) on (−1, 1).



C.1 Collapse Networks



# Verification of the collapse results of Sections 13.8-13.10 (Appendix C.1).

# C1: random-kick form of the unread Gaussian collapse channel (Proposition 13.15).

# C2: energy-momentum cost of Gaussian collapse (Proposition 13.16).

# C3: Poisson-located Gaussian collapses on a massless field in 1+1 dimensions

#     (Theorem 13.21, Propositions 13.22 and 13.23, Lemma 13.26, Proposition 13.28).

# C4: the same collapses realized by gapless pointers coupled to the field (Proposition 13.31).

import numpy as np

from scipy.linalg import eigh, schur, expm

from scipy.special import erf
