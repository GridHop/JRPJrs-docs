# Quantum Reference Frames and Single-Outcome Dynamics — A Compatibility Framework for Generative Presentism

Part 34 of 40 (1,693 words)



# frame-relative product state becomes entangled in the other frame

def ket(x, y): v = np.zeros(d2); v[ridx(x, y)] = 1; return v

prodA = (ket(1, 0) + ket(2, 0))/np.sqrt(2)

def ent(v):

    sv = np.linalg.svd(v.reshape(N, N), compute_uv=False)**2; sv = sv[sv > 1e-12]

    return -(sv*np.log2(sv)).sum()

print(f"7. entanglement entropy: frame A {ent(prodA):.3f} bits, "

      f"frame B {ent(V_AB @ prodA):.3f} bits")



# an absolute (non-invariant) collapse operator leaves the physical sector

Pabs = np.zeros((D, D))

for t in itertools.product(range(N), repeat=3):

    if t[2] == 0: Pabs[idx(*t), idx(*t)] = 1

v = Pabs @ (JA @ phiA0)

leak = np.linalg.norm(v - Pi @ v)/np.linalg.norm(v)

print(f"8. absolute collapse: ||(1-Pi) P_abs Psi|| / ||P_abs Psi|| = {leak:.3f}")



# ---- 9. continuous-time relational jump process (GRW-type), frames A and B

Lam, T = 1.2, 5.0

JA_ops = {k: red(K, JA) for k, K in kraus(s, lam_=1.0).items() if k != 'none'}

JB_ops = {k: V_AB @ K @ V_AB.T for k, K in JA_ops.items()}      # = frame-B forms

HA, HB = red(H, JA), red(H, JB)

assert np.allclose(sum(K.conj().T @ K for K in JA_ops.values()), np.eye(d2))

def trajectory(psi, Hm, ops, r):

    t, events = 0.0, []

    while True:

        dt = r.exponential(1/Lam)             # hit times: Poisson, rate Lam

        if t + dt > T:

            psi = expm(-1j*Hm*(T-t)) @ psi; break

        t += dt; psi = expm(-1j*Hm*dt) @ psi

        keys = list(ops)

        p = np.array([np.linalg.norm(ops[k] @ psi)**2 for k in keys])

        k = keys[r.choice(len(keys), p=p/p.sum())]

        psi = ops[k] @ psi; psi /= np.linalg.norm(psi)

        events.append((round(t, 12), k))

    return psi, events

same, worst, nev = True, 0.0, 0

for trial in range(200):

    pa, ea = trajectory(phiA0, HA, JA_ops, np.random.default_rng(1000+trial))

    pb, eb = trajectory(V_AB @ phiA0, HB, JB_ops, np.random.default_rng(1000+trial))

    same &= (ea == eb); nev += len(ea)

    worst = max(worst, 1-abs(np.vdot(V_AB @ pa, pb)))

print(f"9. continuous time: 200 trajectories, {nev} events; "

      f"identical event records in A and B: {same}")

print(f"   max(1-|<V psi_A|psi_B>|) at final time = {worst:.1e}")



# ---- 10. generic parameters: do distinct histories reach the same present ray?

fin = [(h, v[1]) for h, v in dA.items()]

G = np.array([v for _, v in fin]); ov = np.abs(G.conj() @ G.T)

np.fill_diagonal(ov, 0); best = ov.max()

ncoinc = int((ov > 1 - 1e-10).sum() // 2)

F2 = best**2; helstrom = 0.5*(1 - np.sqrt(1 - F2))

print(f"10. generic parameters, {len(fin)} three-stage histories: "

      f"exact coincidences = {ncoinc}; largest overlap = {best:.4f}")

print(f"    minimum error probability for telling that pair apart (Helstrom) = {helstrom:.3f}")



# ---- 11. finite-width flashes: every present state is reachable by every history

Phi = rng.normal(size=d2) + 1j*rng.normal(size=d2); Phi /= np.linalg.norm(Phi)

hists = [((0, 1, 1), (1, 2, 4), 'none'), ('none', (0, 2, 0), (0, 1, 3))]

res = []

for h in hists:

    psi = Phi.copy()

    for k in reversed(h):                     # back-propagate: psi_prev ~ W^-1 F_k^-1 psi

        psi = WA.conj().T @ np.linalg.solve(FA[k], psi); psi /= np.linalg.norm(psi)

    psi0, pr = psi.copy(), 1.0

    for k in h:                               # forward run from the reconstructed start

        v = FA[k] @ (WA @ psi); q = np.vdot(v, v).real; pr *= q; psi = v/np.sqrt(q)

    res.append((abs(np.vdot(psi, Phi)), pr, psi0))

print(f"11. two different 3-stage histories, same present ray: "

      f"|<end|Phi>| = {res[0][0]:.12f}, {res[1][0]:.12f}")

print(f"    history probabilities {res[0][1]:.2e}, {res[1][1]:.2e}; "

      f"overlap of the two initial states = {abs(np.vdot(res[0][2], res[1][2])):.3f}")



# ---- 12. a history-dependent (QRF-covariant) law is not a kernel on the present state

# second instrument: same flashes, pair weights q = (1/2, 1/4, 1/4) instead of 1/3 each

def kraus_q(width, q):

    ws = np.array([wfun(r, width) for r in range(N)]); ws = ws/ws.sum()

    out = {'none': np.sqrt(1-lam)*np.eye(D)}

    for (i, j), qq in zip(pairs, q):

        for dd in range(N):

            out[(i, j, dd)] = np.sqrt(lam*qq)*sum(np.sqrt(ws[(r-dd) % N])*P(i, j, r)

                                                  for r in range(N))

    return out

def law(Fa, Fb):                    # instrument for transitions after the first

    return lambda first: Fa if (first != 'none' and first[:2] == (0, 1)) else Fb

def run_law(psi, hist, Fa, Fb, Wm):

    pr = 1.0

    for m, k in enumerate(hist):

        Fm = Fa if m == 0 else law(Fa, Fb)(hist[0])

        v = Fm[k] @ (Wm @ psi); q = np.vdot(v, v).real; pr *= q; psi = v/np.sqrt(q)

    return psi, pr

def next_law(psi, first, Fa, Fb, Wm):

    Fm = law(Fa, Fb)(first)

    return np.array([np.linalg.norm(Fm[k] @ (Wm @ psi))**2 for k in Fa])

# (a) finite width, across initial conditions: invert the two branch products

FA_q = {k: red(K, JA) for k, K in kraus_q(s, (0.5, 0.25, 0.25)).items()}

Phi_c = WA.conj().T @ ket(1, 3)                         # present ray; W Phi_c = |1,3>

br1, br2 = ((0, 1, 2), (1, 2, 0)), ('none', (1, 2, 0))

starts = []

for hb in br1, br2:

    Fsecond = law(FA, FA_q)(hb[0])

    M = Fsecond[hb[1]] @ WA @ FA[hb[0]] @ WA

    psi0 = np.linalg.solve(M, Phi_c); psi0 /= np.linalg.norm(psi0)

    end, pr = run_law(psi0, hb, FA, FA_q, WA); starts.append((abs(np.vdot(end, Phi_c)), pr))

tv_a = 0.5*np.abs(next_law(Phi_c, br1[0], FA, FA_q, WA)

                  - next_law(Phi_c, br2[0], FA, FA_q, WA)).sum()

print(f"12a. finite width: both branches end at the same ray "

      f"(|<end|Phi>| = {starts[0][0]:.12f}, {starts[1][0]:.12f}),")

print(f"     probabilities {starts[0][1]:.2e}, {starts[1][1]:.2e}; "

      f"next-event total variation = {tv_a:.4f} (lambda/6 = {lam/6:.4f})")

# (b) sharp flashes, J = 0, one fixed initial state

Fs1 = {k: red(K, JA) for k, K in kraus(0).items()}

Fs2 = {k: red(K, JA) for k, K in kraus_q(0, (0.5, 0.25, 0.25)).items()}

w1, w2 = ((0, 1, 1), (0, 2, 3)), ((0, 2, 3), (0, 1, 1))

e1, p1 = run_law(phiA0, w1, Fs1, Fs2, Wd); e2, p2 = run_law(phiA0, w2, Fs1, Fs2, Wd)

tv_b = 0.5*np.abs(next_law(e1, w1[0], Fs1, Fs2, Wd) - next_law(e2, w2[0], Fs1, Fs2, Wd)).sum()

print(f"12b. sharp, fixed initial state: same present ray: "

      f"{np.isclose(abs(np.vdot(e1, e2)), 1.0)}; probabilities {p1:.3e}, {p2:.3e};")

print(f"     next-event total variation = {tv_b:.4f}")



# ---- 13. conditioning on a future event = forward Markov law with a Doob h-transform

E, nT = (1, 2, 0), 3

def h(psi, m):                                          # Pr(event E at stage nT | psi at m)

    if m == nT - 1: return np.linalg.norm(FA[E] @ (WA @ psi))**2

    tot = 0.0

    for k in F:

        v = FA[k] @ (WA @ psi); q = np.vdot(v, v).real

        if q > 1e-15: tot += q*h(v/np.sqrt(q), m+1)

    return tot

cond = {hh: v[0] for hh, v in dA.items() if hh[-1] == E}

Z = sum(cond.values()); cond = {hh: p_/Z for hh, p_ in cond.items()}

def doob(hist):

    psi, p_ = phiA0.copy(), 1.0

    for m, k in enumerate(hist):

        v = FA[k] @ (WA @ psi); q = np.vdot(v, v).real; nxt = v/np.sqrt(q)

        hn = (1.0 if k == E else 0.0) if m == nT-1 else h(nxt, m+1)

        p_ *= q*hn/h(psi, m); psi = nxt

    return p_

dmax = max(abs(doob(hh) - pc) for hh, pc in cond.items())

print(f"13. conditioned on {E} at stage {nT}: Doob forward kernel vs conditioned law, "

      f"max diff = {dmax:.1e}")



# ---- 14. realized-history consistency for causally local instruments (brickwork circuit)

rq = np.random.default_rng(2026)

nq = 6

slots = [(1, 0), (1, 2), (1, 4), (2, 1), (2, 3), (3, 0), (3, 2), (3, 4)]   # (layer, first qubit)

def qubits(x): return {slots[x][1], slots[x][1] + 1}

direct = {(x, y) for x in range(len(slots)) for y in range(len(slots))

          if slots[x][0] < slots[y][0] and qubits(x) & qubits(y)}

prec = set(direct)

while True:                                             # transitive closure

    new = {(a, d) for (a, b) in prec for (c, d) in prec if b == c} - prec

    if not new: break

    prec |= new

def rand_instr(r):                                      # random 2-outcome instrument, 2 qubits

    Z_ = r.normal(size=(8, 4)) + 1j*r.normal(size=(8, 4)); Q, _ = np.linalg.qr(Z_)

    return [Q[0:4, :], Q[4:8, :]]

def embed(K, q0, n=nq): return np.kron(np.kron(np.eye(2**q0), K), np.eye(2**(n - q0 - 2)))

instr = {x: rand_instr(rq) for x in range(len(slots))}

psi_c = rq.normal(size=2**nq) + 1j*rq.normal(size=2**nq); psi_c /= np.linalg.norm(psi_c)

def lin_ext(r):

    left, order = set(range(len(slots))), []

    while left:

        ready = [x for x in left if not any((y, x) in prec for y in left)]

        x = ready[r.integers(len(ready))]; order.append(x); left.remove(x)

    return tuple(order)

def joint(order, ins, where=None):

    where = where or {x: slots[x][1] for x in range(len(slots))}

    out = {}

    for outs in itertools.product((0, 1), repeat=len(slots)):

        v = psi_c.copy()

        for x in order: v = embed(ins[x][outs[x]], where[x]) @ v

        out[outs] = v

    return out

def all_ext(left, prefix):

    if not left: yield tuple(prefix); return

    for x in sorted(left):

        if not any((y, x) in prec for y in left):

            yield from all_ext(left - {x}, prefix + [x])

exts = set(all_ext(set(range(len(slots))), []))

ref = joint(next(iter(exts)), instr)

dp, ds = 0.0, 0.0

for e in exts:

    jj = joint(e, instr)

    for o in ref:

        pa, pb = np.vdot(ref[o], ref[o]).real, np.vdot(jj[o], jj[o]).real

        dp = max(dp, abs(pa - pb))

        if pa > 1e-12: ds = max(ds, 1 - abs(np.vdot(ref[o], jj[o]))/np.sqrt(pa*pb))

print(f"14. causally local instruments: all {len(exts)} foliations (linear extensions), "

      f"{len(ref)} outcome histories;")

print(f"    max |p - p'| = {dp:.1e}, max state deviation = {ds:.1e}")

# no-signaling: marginal at slot 3 is unchanged when instruments outside its causal past change

X = 3; past = {y for y in range(len(slots)) if (y, X) in prec} | {X}

def marg(ins):

    jj = joint(next(iter(exts)), ins); m = np.zeros(2)

    for o, v in jj.items(): m[o[X]] += np.vdot(v, v).real

    return m

m0 = marg(instr); worst = 0.0

for y in set(range(len(slots))) - past:

    ins2 = dict(instr); ins2[y] = rand_instr(rq); worst = max(worst, np.abs(marg(ins2) - m0).max())

print(f"    instruments changed outside the predecessor set of slot {X}: "

      f"max change = {worst:.1e}")

# consistency on nested order ideals: law on I computed from instruments in I alone

I_ideal = sorted(past)

devI = 0.0

full = joint(next(iter(exts)), instr)

for oI in itertools.product((0, 1), repeat=len(I_ideal)):

    v = psi_c.copy()

    for x, ax in zip(I_ideal, oI): v = embed(instr[x][ax], slots[x][1]) @ v

    pI = np.vdot(v, v).real

    pm = sum(np.vdot(w, w).real for o, w in full.items()

             if tuple(o[x] for x in I_ideal) == oI)

    devI = max(devI, abs(pI - pm))

print(f"    order ideal {I_ideal}: law from its own instruments vs marginal of full law, "

      f"max diff = {devI:.1e}")

# counterexample: two 'spacelike' slots acting on overlapping qubits

where_bad = {x: slots[x][1] for x in range(len(slots))}; where_bad[1] = 1   # slot 1 on (1,2)

o1 = (0, 1, 2, 3, 4, 5, 6, 7); o2 = (1, 0, 2, 3, 4, 5, 6, 7)

j1, j2 = joint(o1, instr, where_bad), joint(o2, instr, where_bad)

tvb = 0.5*sum(abs(np.vdot(j1[o], j1[o]).real - np.vdot(j2[o], j2[o]).real) for o in j1)

print(f"    non-commuting 'spacelike' pair: total variation between orders = {tvb:.3f}")
