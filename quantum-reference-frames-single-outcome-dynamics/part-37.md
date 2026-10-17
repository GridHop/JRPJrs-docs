# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 37 of 40 (1,723 words)



Phi = lambda z: 0.5 * (1 + erf(z / np.sqrt(2)))          # standard normal CDF

bump = lambda z: np.where(np.abs(z) < 1, np.exp(-1 / np.maximum(1 - z**2, 1e-300)), 0.0)





def ladder(nc):

    return np.diag(np.sqrt(np.arange(1, nc)), 1)





def modes(nc, m):

    """annihilation operators of m modes, each truncated at nc quanta"""

    a1, I = ladder(nc), np.eye(nc)

    out = []

    for k in range(m):

        A = np.array([[1.0]])

        for j in range(m):

            A = np.kron(A, a1 if j == k else I)

        out.append(A)

    return out





def dephase(rho, A, sig):

    """unread Gaussian collapse of A: multiplier exp(-(a - a')^2/(8 sig^2)) in A's eigenbasis"""

    w, V = eigh(A)

    M = np.exp(-(w[:, None] - w[None, :])**2 / (8 * sig**2))

    return V @ ((V.conj().T @ rho @ V) * M) @ V.conj().T





print('C1. Random-kick form of the unread Gaussian collapse channel')

nc, sig = 24, 0.8

a1, a2 = modes(nc, 2)

q = [(a + a.T) / np.sqrt(2) for a in (a1, a2)]

p = [1j * (a.T - a) / np.sqrt(2) for a in (a1, a2)]

A = 0.6 * q[0] - 0.3 * q[1] + 0.2 * p[0] + 0.5 * p[1]

w, V = eigh(A)

d = w[:, None] - w[None, :]

Mex = np.exp(-d**2 / (8 * sig**2))

dy = 0.01

ys = np.arange(w.min() - 8 * sig, w.max() + 8 * sig, dy)

kap = lambda y: (2 * np.pi * sig**2)**-0.25 * np.exp(-(w - y)**2 / (4 * sig**2))

Mk = sum(dy * np.outer(kap(y), kap(y)) for y in ys)

tq, wq = np.polynomial.hermite.hermgauss(80)

st = 1 / (2 * sig)                     # standard deviation of the kick parameter t

Mru = sum(wt * np.exp(-1j * np.sqrt(2) * st * tt * d) for tt, wt in zip(tq, wq))

Mru = Mru / np.sqrt(np.pi)

print('   Kraus integral over y vs exact multiplier:     max dev %.1e' % np.abs(Mk - Mex).max())

print('   Gaussian mixture of kicks vs exact multiplier: max dev %.1e' % np.abs(Mru - Mex).max())



print('C2. Energy-momentum cost')

# (a) one particle, position collapse, anharmonic potential; expected hbar^2/(8 m sig^2)

mass, om, g4, sig = 1.7, 1.3, 0.2, 0.7

for nc in (140, 180):

    a = ladder(nc + 8)

    Q = (a + a.T) / np.sqrt(2 * mass * om)

    P = 1j * np.sqrt(mass * om / 2) * (a.T - a)

    H = P @ P / (2 * mass) + 0.5 * mass * om**2 * Q @ Q + g4 * np.linalg.matrix_power(Q, 4)

    H, Qt = H[:nc, :nc], Q[:nc, :nc]

    e0, U0 = eigh(H)

    rng = np.random.default_rng(31)

    c = rng.normal(size=8) + 1j * rng.normal(size=8)

    psi = np.zeros(nc, complex)

    psi[:8] = c / np.linalg.norm(c)

    dE = []

    for vec in (U0[:, 0], psi):

        rho = np.outer(vec, vec.conj())

        dE.append(np.trace(dephase(rho, Qt, sig) @ H).real - np.trace(rho @ H).real)

    print('   (a) cutoff %d: ground %.12f, random %.12f; 1/(8 m sig^2) = %.12f'

          % (nc, dE[0], dE[1], 1 / (8 * mass * sig**2)))

# (b) two coupled modes, A linear in (q, p), H quadratic: (|a|^2 + b.K.b)/(8 sig^2)

nc, sig = 24, 0.8

Kc = np.array([[1.3, -0.4], [-0.4, 0.9]])

H2 = 0.5 * (p[0] @ p[0] + p[1] @ p[1])

H2 = H2 + 0.5 * sum(Kc[i, j] * q[i] @ q[j] for i in range(2) for j in range(2))

av, bv = np.array([0.6, -0.3]), np.array([0.2, 0.5])

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
