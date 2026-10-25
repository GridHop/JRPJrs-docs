# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 33 of 35 (1,795 words)

A = av[0] * q[0] + av[1] * q[1] + bv[0] * p[0] + bv[1] * p[1]

rng = np.random.default_rng(32)

psi = np.zeros(nc * nc, complex)

for n1 in range(3):

    for n2 in range(3):

        psi[n1 * nc + n2] = rng.normal() + 1j * rng.normal()

psi /= np.linalg.norm(psi)

vac = np.zeros(nc * nc)

vac[0] = 1

pred = (av @ av + bv @ Kc @ bv) / (8 * sig**2)

res = [np.trace(dephase(np.outer(v, v.conj()), A, sig) @ H2).real - (v.conj() @ H2 @ v).real

       for v in (vac, psi)]

print('   (b) two modes: vacuum %.12f, random %.12f; predicted %.12f' % (*res, pred))

# (c) lattice field in 1+1 dimensions: canonical double commutator vs Fourier formula

Nl, mf, sig = 48, 0.6, 0.9

Lap = 2 * np.eye(Nl) - np.roll(np.eye(Nl), 1, 0) - np.roll(np.eye(Nl), -1, 0)

Kl = mf**2 * np.eye(Nl) + Lap

ev, Ev = eigh(Kl)

Om = np.sqrt(ev)

tn, tw = np.polynomial.legendre.leggauss(200)

T0 = 2.5

ts, tw = T0 * tn, T0 * tw

xs = np.arange(Nl)

hx = bump((xs - 24) / 3.0)

avec, bvec = np.zeros(Nl), np.zeros(Nl)

for t, wt in zip(ts, tw):

    ht = bump(t / T0) * hx

    avec += wt * Ev @ (np.cos(Om * t) * (Ev.T @ ht))

    bvec += wt * Ev @ (np.sin(Om * t) / Om * (Ev.T @ ht))

dE_can = (avec @ avec + bvec @ Kl @ bvec) / (8 * sig**2)

ks = 2 * np.pi * np.arange(Nl) / Nl

wk = np.sqrt(mf**2 + (2 * np.sin(ks / 2))**2)

ht_hat = np.array([np.sum(tw * bump(ts / T0) * np.exp(1j * wk[j] * ts)) for j in range(Nl)])

hx_hat = np.array([np.sum(hx * np.exp(-1j * ks[j] * xs)) for j in range(Nl)])

dE_mode = np.sum(np.abs(ht_hat * hx_hat)**2) / (8 * sig**2 * Nl)

print('   (c) lattice: canonical %.12f, Fourier formula %.12f, relative diff. %.1e'

      % (dE_can, dE_mode, abs(dE_can - dE_mode) / dE_can))

# (d) Delta P^mu transforms as a four-vector (continuum, 1+1 dimensions, mass 1)

mf, sig = 1.0, 0.9





def hfun(t, x):

    return bump(t / 1.2) * bump((x - 0.3 - 0.4 * t) / 1.5) * (1 + 0.4 * x)





def dP(hf, tmax, xmax, n):

    """(1/(4 sig^2)) int dk/(2 pi 2 omega) k^mu |h^(omega_k, k)|^2 by quadrature"""

    tt, xx = np.linspace(-tmax, tmax, n), np.linspace(-xmax, xmax, n)

    TT, XX = np.meshgrid(tt, xx, indexing='ij')

    kg = np.linspace(-80, 80, 8001)

    omk = np.sqrt(mf**2 + kg**2)

    Et, Ex = np.exp(1j * np.outer(omk, tt)), np.exp(-1j * np.outer(kg, xx))

    hh = np.sum((Et @ hf(TT, XX)) * Ex, axis=1) * (tt[1] - tt[0]) * (xx[1] - xx[0])

    wgt = np.abs(hh)**2 / (4 * np.pi * omk) * (kg[1] - kg[0]) / (4 * sig**2)

    return np.array([np.sum(wgt * omk), np.sum(wgt * kg)])





eta = 0.5

L = np.array([[np.cosh(eta), np.sinh(eta)], [np.sinh(eta), np.cosh(eta)]])

Li = np.linalg.inv(L)

P0 = dP(hfun, 1.25, 2.4, 500)

P1 = dP(lambda t, x: hfun(Li[0, 0] * t + Li[0, 1] * x, Li[1, 0] * t + Li[1, 1] * x),

        3.2, 3.6, 900)

print('   (d) Delta P(h) = (%.8f, %.8f), squared invariant mass %.8f'

      % (P0[0], P0[1], P0[0]**2 - P0[1]**2))

print('       boost of rapidity 0.5: |Delta P(Lambda h) - Lambda Delta P(h)| = %.1e'

      % np.abs(P1 - L @ P0).max())



print('C3. Poisson-located Gaussian collapses, massless field in 1+1 dimensions')

# Collapse regions are causal diamonds of half-size dl in light-cone coordinates

# u = t - x, v = t + x, with product smearings beta(u) beta(v).

zn, zw = np.polynomial.legendre.leggauss(200)

Ib = np.sum(zw * bump(zn))

beta = lambda z: bump(z) / Ib                       # normalized bump on [-1, 1]

gn, gw = np.polynomial.legendre.leggauss(64)





def Bcdf(z):

    z = np.clip(z, -1, 1)

    s = -1 + np.outer(z + 1, gn + 1) / 2

    return (z + 1) / 2 * (beta(s) @ gw)





def Sfun(dd):

    """int int beta(z) beta(z') sgn(z - z' + dd); exactly +-1 for disjoint supports"""

    if dd >= 2:

        return 1.0

    if dd <= -2:

        return -1.0

    if dd < 0:

        return -Sfun(-dd)

    return np.sum(zw * beta(zn) * (2 * Bcdf(zn + dd) - 1))





def relation(pts, dl):

    """R[i, j]: region j meets the causal future of region i"""

    u, v = pts[:, 0] - pts[:, 1], pts[:, 0] + pts[:, 1]

    R = (u[None, :] - u[:, None] > -2 * dl) & (v[None, :] - v[:, None] > -2 * dl)

    np.fill_diagonal(R, False)

    return R





def geometry(pts, dl, scale):

    """relation and E_ij = E(h_i, h_j), with E(t, x) = -(sgn u + sgn v)/4"""

    n = len(pts)

    u, v = pts[:, 0] - pts[:, 1], pts[:, 0] + pts[:, 1]

    E = np.zeros((n, n))

    for i in range(n):

        for j in range(i + 1, n):

            val = -scale**2 / 16 * (Sfun((u[i] - u[j]) / dl) + Sfun((v[i] - v[j]) / dl))

            E[i, j], E[j, i] = val, -val

    return relation(pts, dl), E





def topo(R, rng=None):

    """a linear extension of R (random if rng is given); None if R has a cycle"""

    n = len(R)

    indeg = R.sum(0).astype(int)

    order, avail = [], [i for i in range(n) if indeg[i] == 0]

    while avail:

        k = avail.pop(rng.integers(len(avail)) if rng is not None else 0)

        order.append(k)

        for j in np.nonzero(R[k])[0]:

            indeg[j] -= 1

            if indeg[j] == 0:

                avail.append(j)

    return order if len(order) == n else None





def cov_closed(order, E, Sig, sg):

    """outcome covariance along an order: Sigma + diag(sigma^2) + kicks of earlier collapses"""

    C = Sig + np.diag(sg**2)

    for pos, m in enumerate(order):

        e = np.zeros(len(order))

        for m2 in order[pos + 1:]:

            e[m2] = E[m2, m]

        C = C + np.outer(e, e) / (4 * sg[m]**2)

    return C





def absE(E):

    w_, V_ = eigh(1j * E)

    return (V_ @ np.diag(np.abs(w_)) @ V_.conj().T).real





rng = np.random.default_rng(2027)

dl, scale = 0.5, 4.0

cnt = rng.poisson(6.0 * 16.0, size=20000)

print('   (a) counts, area 16, intensity 6: mean %.2f, variance %.2f (expected 96 and 96)'

      % (cnt.mean(), cnt.var()))

lam_b = 1.5

print('   (b) intensity 1.5, 40000 samples per box:  side  P(orderable)  bound of Prop. 13.22')

for side in (1.0, 1.5, 2.0, 2.5):

    ok = 0

    for _ in range(40000):

        pts = rng.uniform(0, side, size=(rng.poisson(lam_b * side * side), 2))

        ok += topo(relation(pts, dl)) is not None

    lv, Ncell = lam_b * dl**2, int(round(side / dl))**2

    print('                                              %.1f   %.5f       %.5f'

          % (side, ok / 40000, (np.exp(-lv) * (1 + lv))**Ncell))

lam_c, side = 0.4, 4.0

nconf, worst, nev, next_, t_ext = 0, 0.0, 0, 0, 0

while nconf < 300:

    pts = rng.uniform(0, side, size=(rng.poisson(lam_c * side * side), 2))

    if len(pts) < 2 or topo(relation(pts, dl)) is None:

        continue

    n = len(pts)

    R, E = geometry(pts, dl, scale)

    sg = rng.uniform(0.5, 1.2, size=n)

    Sig = 0.5 * absE(E) + 0.3 * np.eye(n)

    orders = {tuple(topo(R, rng)) for _ in range(40)}

    Cs = [cov_closed(list(o), E, Sig, sg) for o in orders]

    worst = max(worst, max(np.abs(C - Cs[0]).max() for C in Cs))

    nconf, nev, next_ = nconf + 1, nev + n, next_ + len(orders)

    t_ext += all(pts[i, 0] < pts[k, 0] for i, k in zip(*np.nonzero(R)))

print('   (c) %d orderable configurations, %d collapses, %d linear extensions:'

      % (nconf, nev, next_))

print('       max covariance difference between linear extensions %.1e' % worst)





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
