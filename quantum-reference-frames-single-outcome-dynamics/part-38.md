# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 38 of 40 (1,613 words)





def realize(E):

    """one-mode realization phi_i = cu_i q + cw_i p of a rank-2 antisymmetric E"""

    T, Z = schur(E, output='real')

    k = next(k for k in range(len(E) - 1) if abs(T[k, k + 1]) > 1e-12)

    b, uu, ww = T[k, k + 1], Z[:, k], Z[:, k + 1]

    if b < 0:

        b, uu, ww = -b, ww, uu

    cu, cw = np.sqrt(b) * uu, np.sqrt(b) * ww

    assert np.abs(np.outer(cu, cw) - np.outer(cw, cu) - E).max() < 1e-12

    return cu, cw





ncut = 140

a = ladder(ncut)

qo, po = (a + a.T) / np.sqrt(2), 1j * (a.T - a) / np.sqrt(2)

edges = [-np.inf, -0.7, 0.0, 0.7, np.inf]





def run_order(order, eigs, mult):

    """apply the maps rho -> V (M o V* rho V) V* in the given order to the vacuum; trace"""

    rho = np.zeros((ncut, ncut), complex)

    rho[0, 0] = 1

    for m in order:

        w_, V_ = eigs[m]

        rho = V_ @ ((V_.conj().T @ rho @ V_) * mult(m, w_)) @ V_.conj().T

    return np.trace(rho)





def bin_mult(bins, sg):

    def mb(m, w_):

        dd, mm = w_[:, None] - w_[None, :], (w_[:, None] + w_[None, :]) / 2

        lo, hi = edges[bins[m]], edges[bins[m] + 1]

        mass_in_bin = Phi((hi - mm) / sg[m]) - Phi((lo - mm) / sg[m])

        return np.exp(-dd**2 / (8 * sg[m]**2)) * mass_in_bin

    return mb





def bin_probability(rho, eig, b, sgy):

    """probability that a Gaussian collapse of width sgy lands in bin b (eig: its observable)"""

    w_, V_ = eig

    dd, mm = w_[:, None] - w_[None, :], (w_[:, None] + w_[None, :]) / 2

    in_bin = Phi((edges[b + 1] - mm) / sgy) - Phi((edges[b] - mm) / sgy)

    M = np.exp(-dd**2 / (8 * sgy**2)) * in_bin

    return np.trace((V_.conj().T @ rho @ V_) * M).real





def binned_law(order, eigs, sg, k):

    law = np.zeros((4,) * k)

    for bins in np.ndindex(*law.shape):

        law[bins] = run_order(order, eigs, bin_mult(bins, sg)).real

    return law





found, cf_dev, ord_dev, norm_dev = 0, 0.0, 0.0, 0.0

while found < 4:

    pts = rng.uniform(0, 1.6, size=(3, 2))

    if topo(relation(pts, dl)) is None:

        continue

    R, E = geometry(pts, dl, scale)

    orders = list({tuple(topo(R, rng)) for _ in range(30)})

    if np.sum(np.abs(E) > 1e-3) < 4 or len(orders) < 2:

        continue

    found += 1

    cu, cw = realize(E)

    eigs = [eigh(cu[i] * qo + cw[i] * po) for i in range(3)]

    Sig = 0.5 * np.outer(cu, cu) + 0.5 * np.outer(cw, cw)

    sg = np.array([0.8, 0.9, 1.0])

    for s in rng.normal(size=(4, 3)):

        def ms(m, w_, s=s):

            dd, mm = w_[:, None] - w_[None, :], (w_[:, None] + w_[None, :]) / 2

            return np.exp(-dd**2 / (8 * sg[m]**2) + 1j * s[m] * mm - s[m]**2 * sg[m]**2 / 2)

        for o in orders:

            closed = np.exp(-0.5 * s @ cov_closed(list(o), E, Sig, sg) @ s)

            cf_dev = max(cf_dev, abs(run_order(o, eigs, ms) - closed))

    laws = [binned_law(o, eigs, sg, 3) for o in orders]

    norm_dev = max(norm_dev, max(abs(l.sum() - 1) for l in laws))

    ord_dev = max(ord_dev, max(np.abs(l - laws[0]).max() for l in laws))

print('   (d) 4 three-collapse configurations, one-mode realization, Fock cutoff %d:' % ncut)

print('       characteristic function, direct vs closed form: max dev %.1e' % cf_dev)

print('       64-cell binned history laws: max difference between linear extensions %.1e,'

      % ord_dev)

print('       normalization error %.1e' % norm_dev)

pts = np.array([[0.3, 0.1], [0.55, 0.25]])               # two overlapping diamonds

R, E = geometry(pts, dl, scale)

cu, cw = realize(E)

eigs = [eigh(cu[i] * qo + cw[i] * po) for i in range(2)]

sg = np.array([0.8, 0.9])

rho = np.zeros((ncut, ncut), complex)

rho[0, 0] = 1

A2 = cu[1] * qo + cw[1] * po

rho1 = dephase(rho, cu[0] * qo + cw[0] * po, sg[0])

var_after = (np.trace(rho1 @ A2 @ A2) - np.trace(rho1 @ A2)**2).real

var_alone = (np.trace(rho @ A2 @ A2) - np.trace(rho @ A2)**2).real

print('   (e) overlapping pair, E(h1, h2) = %.6f:' % E[0, 1])

print('       increase of Var(y2) caused by collapse 1: %.10f; E^2/(4 sigma1^2) = %.10f'

      % (var_after - var_alone, E[0, 1]**2 / (4 * sg[0]**2)))

l12, l21 = binned_law((0, 1), eigs, sg, 2), binned_law((1, 0), eigs, sg, 2)

print('       binned joint laws for the two orders: total-variation distance %.4f'

      % (0.5 * np.abs(l12 - l21).sum()))

A1 = cu[0] * qo + cw[0] * po

r12 = dephase(dephase(rho, A1, sg[0]), A2, sg[1])

r21 = dephase(dephase(rho, A2, sg[1]), A1, sg[0])

print('       unread channels in the two orders: max difference of the final states %.1e'

      % np.abs(r12 - r21).max())

eta, nbad, nchg, maxd = 0.6, 0, 0, 0.0

while nbad < 300:

    pts = rng.uniform(0, 2.0, size=(rng.poisson(6.0), 2))

    if len(pts) < 2 or topo(relation(pts, dl)) is not None:

        continue

    n = len(pts)

    R, E = geometry(pts, dl, scale)

    sg = np.full(n, 0.8)

    Sig = 0.5 * absE(E) + 0.3 * np.eye(n)

    o1 = list(np.argsort(pts[:, 0]))

    o2 = list(np.argsort(np.cosh(eta) * pts[:, 0] - np.sinh(eta) * pts[:, 1]))

    dC = np.abs(cov_closed(o1, E, Sig, sg) - cov_closed(o2, E, Sig, sg)).max()

    nbad, nchg, maxd = nbad + 1, nchg + (dC > 1e-12), max(maxd, dC)

print('   (f) %d non-orderable configurations ordered by centre time in two frames' % nbad)

print('       (relative rapidity 0.6): laws differ in %d, max covariance difference %.3f'

      % (nchg, maxd))

print('   (g) centre-time order is a linear extension of the causal order in %d of the %d'

      % (t_ext, nconf))

print('       orderable configurations of item (c)')





# (h) cosmological-time-ordered collapses on a non-orderable Sorkin-type configuration:

# j (tested operation), c1 and c2 (overlapping law collapses), y (target), applied in order

# of t. Light-cone centres (u, v) give j < c1 < y causally, j and y causally separated.

uvc = np.array([[0.0, 0.0], [-0.525, 1.2], [-0.225, 1.05], [-1.05, 2.3]])

pts = np.column_stack([(uvc[:, 0] + uvc[:, 1]) / 2, (uvc[:, 1] - uvc[:, 0]) / 2])

R, E = geometry(pts, dl, 8.0)

print('   (h) order j, c1, c2, y by t; c1 and c2 overlap; E(h_j, h_c1) = %.4f, E(h_c1, h_y) = %.4f,'

      % (E[0, 1], E[1, 3]))

print('       E(h_c1, h_c2) = %.4f, E(h_j, h_y) = %.1f' % (E[1, 2], abs(E[0, 3])))

gl = lambda x: (1 + np.tanh(2 * x)) / 2

for nc in (36, 44):

    a1, a2 = modes(nc, 2)

    q1, q2 = [(a + a.T) / np.sqrt(2) for a in (a1, a2)]

    p1, p2 = [1j * (a.T - a) / np.sqrt(2) for a in (a1, a2)]

    # two-mode realization of the commutation data with phi_j on mode 1 and phi_y on mode 2

    phis = [q1, E[1, 2] / E[0, 2] * q1 + E[0, 1] * p1 - E[1, 3] * p2,

            E[0, 2] * p1 - E[2, 3] * p2, q2]

    for i in range(4):

        for k in range(4):

            c = (phis[i] @ phis[k] - phis[k] @ phis[i])[:8, :8]

            assert np.abs(c - 1j * E[i, k] * np.eye(8)).max() < 1e-9

    ey = eigh(phis[3])

    w1, V1 = eigh(phis[1])

    w0, V0 = eigh(phis[0])



    def target_law(at_j, luders):

        rho = np.zeros((nc * nc, nc * nc), complex)

        rho[0, 0] = 1

        if at_j == 'kick':

            U = expm(3j * phis[0])

            rho = U @ rho @ U.conj().T

        elif at_j == 'collapse':

            rho = dephase(rho, phis[0], 0.8)

        elif at_j == 'luders':                  # an operation outside the Weyl-diagonal class

            K = [V0 @ np.diag(np.sqrt(gl(w0))) @ V0.conj().T,

                 V0 @ np.diag(np.sqrt(1 - gl(w0))) @ V0.conj().T]

            rho = sum(k @ rho @ k.conj().T for k in K)

        if luders:

            K = [V1 @ np.diag(np.sqrt(gl(w1))) @ V1.conj().T,

                 V1 @ np.diag(np.sqrt(1 - gl(w1))) @ V1.conj().T]

            rho = sum(k @ rho @ k.conj().T for k in K)

        else:

            rho = dephase(rho, phis[1], 0.8)

        rho = dephase(rho, phis[2], 0.9)

        return np.array([bin_probability(rho, ey, b, 1.0) for b in range(4)])



    base = target_law(None, False)

    dk = np.abs(target_law('kick', False) - base).max()

    dc = np.abs(target_law('collapse', False) - base).max()

    lb = target_law(None, True)

    dlk = np.abs(target_law('kick', True) - lb).max()

    print('       cutoff %d: Gaussian c1: change of the target law by a kick at j %.1e,' % (nc, dk))

    dlj = np.abs(target_law('luders', False) - base).max()

    print('       by a collapse at j %.1e; target law sums to %.12f' % (dc, base.sum()))

    print('       unsharp Lueders instrument at j (not Weyl-diagonal): change %.1e' % dlj)

    print('       unsharp Lueders c1 (negative control): change by the kick, largest bin %.7f'

          % dlk)





print('C4. Gapless pointer realization of the collapses (Proposition 13.31)')

# Each collapse is realized by a pointer (q_k, p_k) with no Hamiltonian, coupled through the

# density p_k h_k(x) phi(x). The matrix M below is Gamma_kl = E_ret(h_k, h_l), the retarded

# part of E, with E_ret(t, x) = -theta(u) theta(v)/2, so that E = Gamma - Gamma^T.





def Mret(pts, dl, scale):

    u, v = pts[:, 0] - pts[:, 1], pts[:, 0] + pts[:, 1]

    n = len(pts)

    M = np.zeros((n, n))

    for k in range(n):

        for l in range(n):

            M[k, l] = -scale**2 / 32 * ((1 + Sfun((u[k] - u[l]) / dl))

                                        * (1 + Sfun((v[k] - v[l]) / dl)))

    return M





def ordered_sums(pts, dl, scale, nn, eta):

    """sum of E(x_a - x_b) w_a w_b over node pairs with x_a later than x_b in the time

    cosh(eta) t - sinh(eta) x: the phase of the time-ordered product of the couplings"""

    z, wz = np.polynomial.legendre.leggauss(nn)

    Zu, Zv = np.meshgrid(z, z, indexing='ij')

    w = (scale / 2) * np.outer(beta(z) * wz, beta(z) * wz).ravel()

    nodes = [((t - x) + dl * Zu.ravel(), (t + x) + dl * Zv.ravel()) for t, x in pts]

    T = np.zeros((len(pts), len(pts)))

    for k in range(len(pts)):

        for l in range(len(pts)):

            for c in range(0, len(w), 512):

                du = nodes[k][0][c:c + 512, None] - nodes[l][0][None, :]

                dv = nodes[k][1][c:c + 512, None] - nodes[l][1][None, :]

                later = np.cosh(eta) * (du + dv) - np.sinh(eta) * (dv - du) > 0

                Ev = np.where(later, -(np.sign(du) + np.sign(dv)) / 4, 0.0)

                T[k, l] += w[c:c + 512] @ Ev @ w

    return T
