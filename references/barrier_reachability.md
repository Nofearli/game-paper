# Barrier and Reachability — Special-Topic Reference

Deep dive into the barrier constructions and reachability machinery in the library. Every claim cites its archive ID; page/equation numbers propagate from the archives' Section 5. `[proven]` = the archive records a verification argument; `[asserted]` = the archive records that the step is stated without proof (archive Section 7).

---

## 0. The two families of barrier claims in the library

- **Value-zero barriers**: $\mathcal{B} = \{V = 0\}$ for a value $V$ that is constructed geometrically and *then* certified as the (classical or viscosity) solution of an HJI equation. Papers: P022, P031, P041 (implicitly), P050, P080, P082, P096, P048, P019 (value-based winning regions).
- **Direct geometric barriers**: the surface is written down as the locus where a dominance region is tangent to the target (or where the team's joint dominance boundary touches the target), and winning regions are its super/sub-level sets. Papers: P073, P091, P094, P099, P100, P102, P112, P035, P036, P098, P087, P011, P012. Verification ranges from full HJI proof (rare) to semipermeability assertion (common).

The organizing trichotomy used by the direct-geometric school (for a candidate initial evader position $x_E^0$ with team dominance boundary $\mathscr{B}$): on the barrier iff $\mathscr{B}$ touches $\mathcal{T}$ but avoids $\Omega_{\mathrm{goal}}$; pursuer-winning iff $\mathscr{B} \cap (\mathcal{T} \cup \Omega_{\mathrm{goal}}) = \emptyset$; evader-winning iff $\mathscr{B}$ intersects $\Omega_{\mathrm{goal}}$ [P073, Sec. III-B, pp. 3–5].

---

## 1. Bisector-plane mirror construction in 3D [P073]

**Setting.** Four equal-speed players, simple motion, target plane $\mathcal{T} = \{z : K^\top z = b\}$ normalized to $\{z_3 = 0\}$ (eq. (1), eq. (3)) [P073, pp. 2–3]. State space $\mathbb{R}^{12}$; capture = closest-pursuer distance zero.

**Recipe.** Because speeds are equal, each pursuer's evasion space is a half-space and its boundary the perpendicular **bisector plane** $\mathscr{B}^i = \{z : \|z - x_E^0\| = \|z - x_{P_i}^0\|\}$ (eq. (4)) — the ratio-1 degenerate Apollonius sphere. The team ES is $\mathscr{E} = \mathscr{E}^1 \cap \mathscr{E}^2 \cap \mathscr{E}^3$ (eq. (6)). The barrier is then assembled from the *arrangement* of these planes:

1. **One pursuer (Lemma 1, eq. (7), p. 3)**: if $z_{P_i}^0 < 0$ (pursuer below the plane), the barrier is the single **mirror point** — the reflection of the pursuer across $\mathcal{T}$; otherwise $B^i = \emptyset$ and the pursuer guards only the vertical ray $\mathcal{W}_P^i = \{x = x_{P_i}^0, y = y_{P_i}^0, z > |z_{P_i}^0|\}$.
2. **Two active pursuers (Theorem 1, eqs. (9)–(10), p. 4)**: barrier = $\{B^i, B^j\}$ plus a **circular arc** $B_{i,j}^3$ in the vertical plane $\mathcal{P}_{i,j}$ through both pursuers, centered at the equal-arrival point $c_{i,j} \in \mathcal{T}$ on the line of projections, radius $\|x_{P_i}^0 - c_{i,j}\|$; contribution condition: projections differ (eq. (8)).
3. **Three pursuers (Lemmas 2–3, eqs. (11)–(13); Theorems 2–3, eqs. (14)–(16), pp. 4–5)**: collinear projections ⇒ union of two pair barriers (Thm 2); noncollinear ⇒ the **spherical patch** $B = \{z : \|z - c\| = \|x_{P_1}^0 - c\|, (x,y) \in S, z > 0\}$ over the closed triangle $S$ of projections, with $c$ the circumcenter in $\mathcal{T}$ (Thm 3). $n$-pursuer extension by active triple coalitions (Algorithm 1, p. 6; the 6-pursuer example yields four spherical patches over a hexagonal footprint, Fig. 6).

**Verification status.** Game of kind only; no value, no strategies, no HJI. The archive records: the decisive $\mathcal{W}_E$-side interception argument (triangle inequality) "is not written out"; $c_{i,j}$ is ill-defined as printed for pairs (the equidistant locus in $\mathcal{T}$ is a line; uniqueness holds only within $\mathcal{P}_{i,j}$); Theorem 3's "$\mathscr{B}^1 \cap \mathscr{B}^2 \cap \mathscr{B}^3$ has the unique element $c$" conflates the $x_E^0$-dependent triple BES point with the pursuer-determined circumcenter; Algorithm 1's union/intersection formulas are unproven for general $n$ [P073, archive Sec. 7, observations 2–4 and Sec. 5 gaps (a)–(e)]. All `[asserted]`.

**Carry-over rule for 3D work.** The 2D circular-arc barrier of P099 (their ref [18]) lifts to the sphere (15); the guarded footprint grows from a segment (2 pursuers) to the triangle $S$ (3 pursuers); heterogeneous speeds break the bisector construction — use Apollonius spheres instead [P075, P033, P013].

---

## 2. Apollonius-tangency barriers [P022 / P080 / P055]

### 2.1 The ATDDG hyperbola [P022, Thm 3, pp. 564–567] `[proven]`

**Qualitative criterion**: with A–T Apollonius circle (center/radius eqs. (85)–(86) at ratio $\alpha = TP/AP$), the Target escapes **iff the AC intersects the orthogonal bisector (14) of AD**. The barrier is the tangency locus: line $BC \parallel AD$ through the tangency point (eq. (87)), the squared tangency inequality (88) collapses to (90), substituting (85)–(86) gives (91), and expansion yields the conic (82) with coefficients (83). Conic identification: discriminant $-\alpha^2(1-\alpha^2) < 0$ ⇒ hyperbola, center $= (x_0, y_0)$ = AD midpoint, principal-axis angle $\theta = \sigma$ = AD bearing. Escape region $\mathcal{R}_e := \{x : H(x;\alpha) < 0\}$ (eq. (81)); only the Attacker-side branch matters (p. 567). This is the exact game-of-kind companion to the Game-of-Degree solution: strategies (11)–(13) with interception point on the bisector at the real root $x^*$ of the quartic (15)–(16), value $V = \alpha\,\mathrm{AI} \pm \mathrm{TI}$ (eqs. (17), (74)), HJI-verified with no singular surfaces (p. 564, $C^1$ gluing of $V_s, V_g$).

### 2.2 Non-zero attacker capture radius [P080, Thms 1–2, pp. 5–8]

Equal speeds $V_A = V_D = 1$, $V_T = \gamma < 1$, **asymmetric radii** (only A has radius $r > 0$; eqs. (2)–(4)). Game of Degree: two-sided PMP gives state-feedback headings $(\beta^*, \delta^*, \zeta^*)$ (eqs. (11)–(13)), capture point $\mathbf{z}^*$ defined by the two scalar equations (14)–(15), and a $C^1$ value (16) **proved** to satisfy HJI (17) `[proven]` — the $r>0$ extension of the $r=0$ methodology. The Apollonius circle becomes the **Apollonius oval** (Lemma 1, eqs. (9)–(10), imported from the lifeline work). Game of Kind (Thm 2, eqs. (50)–(51)): the barrier is characterized by a **tangency test between the A–T oval and the Attacker's ultimate (limiting) interception curve** $y = f(x) = \pm\sqrt{r^2 - x^2}\,(1 - x_A/x)$, $x \in [-r, 0)$ (eq. (56)) — the locus of points A can just capture when simultaneously intercepted.

### 2.3 Both radii, equal speeds [P082, Automatica 2026] `[proven]`

$R > 0$ (A) and $r > 0$ (D) simultaneously; terminal sets (2)–(4). Game of Degree: two-sided PMP for three initial placements of T relative to the D–A interception hyperbola (Theorems 1–3), constant-heading strategies with radius-dependent intercept point solving (11)–(12), $C^1$ values (16), (46) verified against HJI (17), (44). Game of Kind: the **Attacker's limit interception curve** $\mathcal{A}$ (Definition) plus tangency with the Apollonius oval — the reusable template for any finite-radius barrier.

### 2.4 Speed-varying (second-order) players [P055, Thms 1–3, pp. 1850–1861]

Second-order plants with force saturation. The **average-speed-ratio reduction** freezes $\bar\alpha = \tilde v_D/\tilde v_A$ at its maximum, decomposing the game into (i) a PMP force-allocation problem (bang-bang full acceleration then coast) and (ii) a 1-D search of the terminal value over $\bar\alpha$; the constant-speed Apollonius machinery re-instantiates: eqs. (47)–(49) re-use (14)–(15), and eq. (68) **offsets the barrier by $r_T$**. Verification: terminal value continuously differentiable in the ratio (Lemmas 1–2), Theorems 1–3 argue Nash via the HJI equation `[proven, with the archive noting no numerical HJI is solved]`.

---

## 3. Obstacle-modified barriers [P069 / P106 / P041 / P095]

### 3.1 Isochrone-intersection barriers [P069, Automatica 2016]

Without obstacles isochrones are circles (Thm 1, p. 4); with polygonal obstacles paths break at vertices and **every isochrone piece is a circular arc about a known center** (Thm 2, continuous Dijkstra). The plane is exhaustively partitioned into P-dominates / E-dominates / neither (Thm 6); the third region is obtained by intersecting isochrone bundles. **Every piece of the dominance boundary is a generalized Apollonius curve**: limaçon, Apollonius circle, or vertex-centered circle, indexed by the final-segment start-time offset (Thm 7 + Remark 1), with singular surfaces (type-(p,u,p) lines, hyperbolic dispersal surfaces) organizing the assembly "in the large" `[proven within the wavefront framework]`.

### 3.2 Polygonal-obstacle winning strategies [P106, TAC 2025]

Visual-radius capture (distance $\le r_i$ **and** obstacle-free connecting segment, p. 817) — obstacles shield capture. Three pairs of pursuit winning regions: onsite winning via **expanded Apollonius circles** (Thm 1/Lemma 2); goal-visible close-to-goal via **convex goal-covering polygons (GCPs)** with existence/consistency (Def. 5, Lemma 4) and a constructive GCP-enlargement theorem (Thm 3); nongoal-visible via the **ESP (evader's shortest-path) reachable region** with wavefront/circular-sector decomposition (Defs. 11–14) and an anchored safe distance (Thm 4). Fused into hierarchical receding-horizon allocation with monotone defeat-count guarantee `[asserted winning regions; strategy-level proofs constructive]`.

### 3.3 What obstacles do to dominance: rigor and negative results [P041]

Dominance in the shortest-path metric $d_L$: $D(x_1,x_2) = \{x : d_L(x,x_1) - \alpha d_L(x,x_2) > 0\}$ (Def. 2, p. 4). Boundary = Cartesian ovals + Apollonius circles + vertex-centered circles (Thm 11, quoted from Oyler et al.). **Dominance = reachability with obstacles**: $\mathcal{R}_e = D$ proven by exact arrival times and the path-invariance Lemma 6 (Thm 5, pp. 4–5) `[proven]`. **Negative result** (Example 13, p. 8): for a corner obstacle, no PELIDR non-anticipative strategy exists — two evader controls coincide on an interval while the forced pursuer replies differ, violating non-anticipativity (eq. (3)); the archive flags the necessity step ("pursuer must move to $C_1$ directly") as an unformalized heuristic `[gap]`. **Necessary condition** for any confinement strategy: $\partial_2 d_L(x_{c1},x_{p0})\cdot\partial_2 d_L(x_{c2},x_{p0}) - \partial_2 d_L(x_{c1},x_{e0})\cdot\partial_2 d_L(x_{c2},x_{e0}) \ge 0$ on the boundary (Thm 14, eq. (24), via the boundary-evolution equation (21)–(23)) `[proven]`. **Sufficient condition** for a single corner obstacle: $\|x_{p0}\| < \alpha\|x_{e0}\|$, pursuit law piecewise (toward exit point on the oval / straight away from the vertex), capture bound $t_f \le t_0 + \frac{\|x_{p0}-x_{e0}\| - l}{\alpha - 1}$, four-case rate comparison (Thm 20, pp. 11–12) `[proven, with the printed bound keeping a spurious $-l$ term]`.

### 3.4 Obstacle + partial information [P095]

Line-segment obstacle tangent to the sensing circle forces a zig-zag detour; the defender's guaranteed angular set grows by $\Delta\theta_l + \Delta\theta_r$ (Thm 1); three-phase decomposition (deployment / asymmetric information / engagement, Defs. 1–3, eqs. (1)–(5)). Barrier logic is angular-set arithmetic, not a value function `[asserted]`.

---

## 4. Closed-form value barriers [P031 / P041 / P098]

### 4.1 HJI justification of the geometric solution [P031, Automatica 2023]

Setting: $n$ faster defenders ($a = v_D/v_I \ge 1$), convex $C^2$ target $\mathcal{A} = \{\varphi \le 0\}$, capture radius $r$ (valid for $r = 0$ too, Remark 2.1). Dominance region $\mathcal{D}_I = \bigcap_j \{d_j \ge 0\}$, $d = R_D - aR_I - r$ (eq. (2.5)) — convex (Lemma 2.1, proven by a curvature-sign computation with the decisive inequality $(d_y)^3 R_I\, d^2y/dx^2 \ge (a^2-1)(1 - \cos^2(\alpha - \beta)) \ge 0$, App. C). Geometric strategy: everyone heads to the tangency point $p^*$ = solution of the auxiliary convex program $\min \varphi$ over $\mathcal{D}_I$ (eqs. (2.6)–(2.8)); value $V^g = g(p^*)$; the barrier is $\{V^g = 0\}$ (§4.5). Theorem 2.1: (2.7)–(2.8) solve the HJI equation (2.9a) with boundary conditions (2.9b)–(2.9d) `[proven, with flagged gaps]`. Proof architecture: SDSI verified differentiably via the implicit system for $p^*$ (Lemma 3.3, eq. (3.11)) and the **determinant identity** (3.20) collapsing the value gradient to $[\varphi_{y^*}/d_{y^*}; 0]$ in the frame $F_{\alpha^*}$ (eqs. (3.21a)–(3.21b)); 2DSI via the vertex $p^\star$ with gradient additivity $a\|\partial_{p_1}V\| + a\|\partial_{p_2}V\| = \|\partial_{p_I}V\|$ (Lemma 4.1, eq. (4.2)); MDSI closed by continuity + viscosity (§4.4). **Flagged gaps**: "d is concave" is unjustified and generally false (p. 5 — only quasiconcavity follows); the viscosity sub/supersolution inequalities across switching surfaces are asserted; $\Omega$ notation slip in (4.7); typo in (A.9) [P031, archive Sec. 7, observations 1–7].

### 4.2 Dominance-region barriers as reachability certificates [P041]

Without obstacles the guard wins iff $D_l(x_{p0}, x_{e0}) \cap \mathcal{T} = \emptyset$ — **if and only if**, necessity from Thm 4 (dominance = open-loop reachability), sufficiency from Thm 7 (non-anticipative confinement + uniform capture bound) (§6, eq. (48), p. 13; note the archive's D/$D_l$ notation-slip warning). With obstacles, sufficiency only (Example 13 shows necessity fails). The barrier is thus *the boundary of the Cartesian oval* — a closed-form value barrier without ever writing a PDE (no HJI connection; archive observation 8).

### 4.3 Generalized (projection) barrier [P098]

For arbitrary compact convex target $\Omega$: $B(\mathbf{x};\Omega,\gamma) := \|\mathrm{Proj}_\Omega(C(\mathbf{x})) - C(\mathbf{x})\| - R(\mathbf{x})$ (eq. (19), Prop. 3) — the distance from the Apollonius center to the *metric projection onto the target* replaces the distance to the circle; winning sets $\mathcal{R}_c = \{B > 0\}$, $\mathcal{R}_a = \{B \le 0\}$ (eqs. (20)–(21)); semipermeability asserted (Remark 2). Reduces to "(11) in [7]" for a circular target. Games of degree: continuous value with capture/attack strategies from the projection point `[asserted semipermeability; classical C¹ claims on regular regions]`.

### 4.4 Closed-form verification of convex-target guarding [P050, TAC 2024]

The superset of all the above: candidate value $V(\theta) = \inf\{d_{\mathcal{T}}(x) : x \in \mathcal{F}(\theta)\}$ with $\mathcal{F}(\theta) = \{x : f_i(x,\theta) \le 0\}$ the offset-Apollonius dominant region (eqs. (9)–(11)). Theorem 2 proves $V$ is **the viscosity solution of the HJI equation (5) on all of $\Theta$** and classical exactly where LICQ holds `[proven]` — via Slater ⇒ strong duality ⇒ KKT (17), generalized Danskin (Lemma 1, eqs. (24)–(26)), Clarke subdifferential $\partial V = \mathrm{conv}\{\nabla_\theta L\}$ (eq. (27)), and the decisive term-by-term cancellation showing $F(\xi) = 0$ for every convex combination of active-multiplier gradients. Winning regions $\mathcal{W}_A = \Theta^{=0}$, $\mathcal{W}_D = \Theta^{>0}$ (eq. (32)); equilibrium strategies (33) chase the optimal capture point iff the defender's constraint is *strongly active* for some optimal multiplier; the state-space partition by active coalition $\mathcal{W}_{D_\mathcal{I}}$ (eq. (34)) is the built-in allocation logic. This subsumes the special-case verifications [8]–[14] and hardens P031 (archive's own positioning, p. 6357).

---

## 5. Multi-lifeline barriers [P094 / P102 / P112 / P093]

**Lifeline setup.** Strip $0 < y_E < d$ between parallel lifelines $L_1$ ($y=0$), $L_2$ ($y=d$); evader wins by crossing either uncaptured; pursuers win by capture (radius $l > 0$) within the strip.

### 5.1 Two pursuers, one evader, two lifelines [P094, Thms 4.1, 5.1, 5.2]

Reachable region $R = R_1 \cap R_2$ bounded by two Cartesian ovals $C_i: \|x_G - x_E\| = \frac{1}{a}(\|x_G - x_i\| - l)$ (Lemma 3.1, eq. (7) — proof outsourced to the P031 justification `[asserted]`; degenerates to hyperbolas at $a = 1$, Fig. 2b). Capture strategy on the oval: $\varepsilon = \arcsin(\frac{r_2}{ar_2 + l}\sin\varsigma)$ with the inner-oval root of the quadratic (Lemma 3.2, eqs. (8)–(14)) `[proven by synthetic geometry]`; robustness to evader turns cited to Dutkevich–Petrosyan `[asserted]`. **Barrier $B_1$** (Thm 4.1, eqs. (17)–(18)): parametric curve $x_e(\tau) = \tau - nm$, $y_e(\tau) = m\sqrt{1 - n^2}$ with $m = \frac{1}{a}(\|x_{T^*} - x_1\| - l)$, $n = \frac{\tau - x_1}{a\|x_{T^*} - x_1\|}$, derived in 6 steps from the terminal-separation payoff: FOC $dJ_P/d\tau = 0$ (eq. (21)) + on-barrier identity $J_P(\tau^*) = 0$ (eq. (22)); admissible tangency set $U$ excludes the pursuer's projection disc on $L_1$. Mirror barrier $B_2$ for $L_2$ (eq. (27)); vertical-escape boundaries $B_3, B_4$ (eq. (30)). Three-player barrier (Thm 5.1, eq. (33)): eight curves $B_1$–$B_8$ = pairwise merge — **sufficiency of the merge is not proven** (joint-pursuit and sequential-timing effects unanalyzed; regions 7–8 patched by the reachable-set test $R \cap \Omega_{\mathrm{goal}} \ne \emptyset$ instead) `[gap]`. Region-wise strategies (31)–(32) aim at the nearest oval–lifeline intersection; the **resultant-force strategy** (Thm 5.2, eqs. (34)–(38)): pursuers repel with inverse-square forces $F_i = 1/\|x_i - x_E\|^2$, the infinite lifelines attract with $F_{k_1} = 2/y_E$, $F_{k_2} = 2/(d - y_E)$ (correct line integrals, eqs. (37)–(38)); heuristic, no optimality claim — Remark 5.1 concedes "the classical Isaacs method cannot be applied" to multiple terminal manifolds.

### 5.2 Limited-lifetime lifeline [P102, Lemmas 3–7, Thms 1–3]

l-Apollonius evasion region $\mathcal{R}_e = \{\|z - x_E\| < \alpha(\|z - x_P\| - l)\}$ with explicit polar boundary (Lemma 3, eqs. (19)–(24)); potential $F(z) = \|z - x_P\| - \|z - x_E\|/\alpha - l$ (eq. (25)) as the analytic backbone; strict convexity via the monotone function $G(\beta)$ (Lemma 1, eqs. (12)–(18), sign factorization (17) decisive) consumed by Lemma 4 (unique closest point $H$ of $\mathcal{A}^l$ to the goal). **Pursuit law**: aim at $H$; then $\dot y_H \ge 0$ with equality iff the evader runs at $H$ (Lemma 5, eqs. (36)–(40)) — capture with a guaranteed lifeline distance `[proven by differentiation + Cauchy–Schwarz]`. **Barrier without lifetime** (Lemma 7, eqs. (44)–(52)): parametric curve $x = x^* - \alpha^2 ab$, $y = \alpha a\sqrt{1 - \alpha^2 b^2}$ from the FOC (48) + on-barrier identity (49); information-structure independence via uniqueness (eq. (52)). **Barrier with lifetime** (Thm 1, eqs. (58)–(59)): four pieces — middle tangency arc, two circles of radius $\alpha v T_l$ about the tangency points $B, M$, and the horizontal line $y = \alpha v T_l$; the lifetime *shrinks* the evader-winning region (Remark 2). Games of degree: five OTP regions $\mathcal{R}_1$–$\mathcal{R}_5$ (Thms 2–3, eqs. (62)–(83)) with boundary curves $\Gamma_1$–$\Gamma_3$; dispersal surface identified in $\mathcal{R}_2$ with no tie-breaking rule `[gaps: no formal saddle verification; "closer to L" selection argued by monotonicity only]`. Multiplayer: bipartite matching on winnable pairs (Sec. 7, heuristic).

### 5.3 Three-player lifeline via Isaacs RPEs [P112, Thms 1–2]

Two-player sub-game barrier $\mathscr{B}_1$ from Isaacs' main equation + **RPE integration from the whole BUP** (Thm 1, eq. (6), p. 5, eq. (17), p. 6) — the library's one full Isaacs-retrograde barrier construction `[asserted: the RPE integration is presented, but the indeterminate terminal component $\min\{d_1,d_2\} = l$ blocks the classic single-BUP construction for the joint game, p. 4]`. Three-player barrier = **bond** of $\mathscr{B}_1$ and $\mathscr{B}_2$: the evader's barrier trajectory is the piecewise curve (20) switching at the intersection $(\tilde x, \tilde y)$ of the sub-game curves; capture zone of the joint game = union of sub-game capture zones "because the pursuers play individually" (Thm 2, eqs. (18)–(20), p. 6) `[asserted]`. Region-wise explicit-policy layer (regions A–D) operationalizes the escape zone.

### 5.4 One superior pursuer, multiple evaders, two lifelines [P093, Thms 4.1–4.2, 5.1]

Per-lifeline barrier curves without delay (eq. (13)) and with dispatch delay $\Delta t = \sum t_j$ (eq. (19), Cor. 4.1 eq. (26)); the $\Delta$-PDR shrinks monotonically with accumulated delay and can vanish (Fig. 5). Workhorse parallel-pursuit lemma: $\varphi = \arcsin(\frac{1}{a_i}\sin\varphi_i)$ captures on/within the Apollonius circle (Lemma 3.1, eq. (6), sine theorem); capture angle $\Theta = \arccos(1 - 2/a_i^2)$ (Lemma 3.3, eq. (11)); escape criterion $\min\{J_1, h - J_2\} \le 0$ (Cor. 5.2).

---

## 6. Capture-radius-offset barriers [P091 / P096]

### 6.1 Heterogeneous speed ratios and radii [P091, TCYB 2025]

Workhorse identity: interception-tie condition $\frac{1}{\alpha_{ji}}\|S'_j - x^0_{A_j}\| = \|S'_j - x^0_{D_i}\| - \rho_i$ (p. 4) — every barrier below is its consequence. **Theorem 1** (one faster defender, slower attacker): three-curve barrier — two Apollonius-offset endpoint arcs $B_1, B_3$ ($\|x^0_{D_i} - E\| = \|x - E\|/\alpha_{ji} + \rho_i$ on $[0, c_1]$, $[c_2, m]$) plus the implicit middle curve $B_2$ (eq. (11)) obtained by squaring the tangency condition (12) at the FOC point $s_j^*$ (eq. (10)); reduces to Wu et al.'s hyperbolic segments at $\rho_i = 0$ (Remark 6) `[geometric optimality; no Isaacs/HJI verification — archive observation 6]`. **Theorem 2** (two heterogeneous defenders): five curves; cooperative middle segment $B_3$ anchored at the heterogeneous rendezvous point $S_k$ solving the equal-*effective*-capture-time condition $\frac{\|x^0_{D_p} - S_k\| - \rho_p}{v^*_{D_p}} = \frac{\|x^0_{D_q} - S_k\| - \rho_q}{v^*_{D_q}}$ (eq. (13)); the radii difference $\rho_p - \beta_{pq}\rho_q$ shifts the rendezvous toward the weaker defender. **Theorem 3** (faster attacker): Cartesian oval with two arcs; **defensive advantage angle** $\gamma_i = 2\theta_{ji}$ from the zero-discriminant condition; $\rho_i = 0$ recovers $\gamma_i = 2\arcsin(v_D^*/v_A^*)$ (Remark 8). **Theorem 4**: optimal target point by cone-grazing with $\epsilon$-clearance formulas. **Theorem 5**: coalition coverage — adjacent intersecting angles $\delta^{pq}_j$, absolute advantage angle $\Phi_j = \sum_i \gamma_i + \sum \delta^{pq-}_j$; interception guaranteed iff the attacker's cone onto T (eq. (19)) lies inside $[\Phi^I_j, \Phi^S_j]$ — proof is an informal ray-pigeonhole `[gap]`, and the printed interval endpoints are unordered. **Theorem 6** (equal speeds): two hyperbola branches anchored at the target endpoints; the middle segments degenerate (Remark 12) `[endpoint-reduction used implicitly]`. **Theorem 7**: existence/uniqueness of the offensive optimal target point via the monotonicity function $H(\epsilon)$ with $H_2'(\epsilon) > 0$ on $[0,1]$; FOC is a quartic (21) solvable by Ferrari (Remark 14) `[proven, most technical proof of the paper]`.

### 6.2 Orthogonal-line barrier + CBF layer [P096, Thm 1]

Equal-speed defender-pair vs. attacker: orthogonal-line barrier $\mathcal{B}(\mathbf{p}_k)$ (eqs. (18), (23)) partitioning $\mathbb{R}^6$ into $\mathcal{R}_D, \mathcal{R}_A$ (eq. (8)); closed-form interception points $\mathbf{I}^*_{k1}$ (1v1, eq. (21)) and $\mathbf{I}^*_{k2}$ (2v1 cooperative, eqs. (25)–(26)) with unit-speed saddle strategies (eqs. (22), (27)); **both value functions HJI-verified** (eqs. (37)–(41), (42)–(47), Thm 1) `[proven]`. Underactuated ASV kinematics with sideslip converted to a fully-actuated point-mass game on the off-center guidance point $\mathbf{p}^D_i = \mathbf{p}_i + \iota_i\varrho_i$ via the invertible mapping (eq. (5)); CBF-QP stack enforces inter-vehicle collision avoidance on top of the game layer.

---

## 7. Reachability via HJI / level sets [P039 / P040] and alternatives

- **Two-phase CTF by constrained HJI** [P039, CDC 2011]: attacker's flag-return set $R_A$, flag-capture set $F_A$, winning set $W_A$ computed from the constrained HJI PDE (eqs. (3)–(5), p. 1454); defender sets by complement; game rules encoded as *the opponent's winning conditions* (defender excluded from $\mathcal{F} \cup \mathcal{R} \cup \mathcal{D}^C$); sequential composition $\tilde R_A = \mathcal{G}_F \cap R_A$ (eq. (5)). Numerical (grid-based), not closed form.
- **Foundational numerical machinery** [P040, TCST 2015]: Elliott–Kalton formulation (2)–(6); time-dilation augmentation to a constrained terminal-cost minimax (7)–(11); upper value = constrained viscosity solution with Evans–Souganidis representation (12)–(15); Isaacs condition (16) gives value existence. This is the library's reference implementation of level-set reach–avoid; the winning region is $\{V \ge 0\}$-type, feedbacks synthesized from the level-set gradient.
- **Exact alternatives**: isochrone/MRR reachability for damped dynamics [P061, Lemma 2, Thm 1]; shortest-path reachability for obstacle domains [P041, Thm 5]; time-to-go risk metrics [P077, Props. 1–2]; forward enclosure (PEF/ERP) replacing backward reachability for homicidal-chauffeur pursuers — coalition reduction to two pursuers by support-constraint counting (Thm 1) [P105, Defs. 1–3, pp. 2–5].

---

## 8. Verified vs asserted barriers — scorecard

| Paper | Barrier object | Verification |
|---|---|---|
| P022 | Hyperbola (82)–(83); value (17)/(74) | `[proven]` HJI (67), $C^1$ gluing, no singular surfaces; root-selection gap |
| P031 | $\{V^g = 0\}$, tangency point $p^*$ | `[proven]` Thm 2.1 (SDSI/2DSI classical + MDSI viscosity); gaps: "d concave", abbreviated viscosity step |
| P041 | Oval boundary $D_l$; confinement | `[proven]` Thms 4–5, 7, 14, 20; no HJI (archive obs. 8) |
| P044 | 2P1EDG value regions; ATDDG barrier (47) | `[proven]` Thm 2 (classical $C^1$, regular region only); kind attributed to [111] |
| P048 | Stacked capture-point value | `[proven]` Thm 2 (SOSC ⇒ Isaacs classical) |
| P050 | $V = \inf d_{\mathcal{T}}$ over $\mathcal{F}(\theta)$ | `[proven]` Thm 2 (viscosity global, classical iff LICQ); minor $\lambda = 0$ gap |
| P019 | $J_1$; dispersal $\Gamma$; switch envelopes | `[proven]` Thm 1 (unique viscosity, incl. $m$-branch Lemma 7); focal surfaces open |
| P080 | Barrier (50)–(51) via oval ∩ ultimate-interception-curve tangency | `[proven]` degree (17); kind by tangency test `[asserted]` |
| P082 | Limit-interception curve + oval tangency | `[proven]` degree (17), (44); kind template `[asserted]` |
| P096 | Orthogonal-line barrier (18), (23) | `[proven]` HJI (37)–(47) |
| P073 | Mirror points / arcs / spherical patch (7)–(16) | `[asserted]` — no value, no strategies, no HJI |
| P091 | Offset-Apollonius curves (Thms 1–7) | `[asserted]` — geometric optimality only |
| P094 | $B_1$–$B_8$ parametric curves | `[asserted]` — Lemma 3.1 outsourced; merge unproven |
| P102 | $\mathcal{B}^\infty$ (44)–(52), $\mathcal{B}$ (58)–(59) | `[proven]` lemmas (invariance, convexity); saddle property `[asserted]` |
| P112 | $\mathscr{B}_1$, bond $\mathscr{B}$ | `[asserted]` — RPE construction presented; BUP indeterminacy noted |
| P098 | Projection barrier (19) | `[asserted]` semipermeability (Remark 2) |
| P099/P100 | AR-method barriers | `[asserted]` — "utilizing the semipermeability of barrier" (p. 1038) |
| P106 | Expanded-AC / GCP / ESP regions | `[asserted]` constructive |
| P035/P036 | $B = \max\{R_E^2 - R_i^2\}$; football barrier | `[proven]` degree values (HJI); kind pieces analytic |
| P011/P012 | $\mathscr{B}^{\text{inner}}$ (17); piecewise polar barriers | `[proven]` degree via HJI on decoupled payoff (P011 Thm 1); kind geometric |

---

## 9. The standard verification workflow (candidate → semipermeability → HJI/viscosity)

1. **Construct the candidate.** Geometric tangency (P022 step 3: AC tangent to bisector; P102 (48)–(49); P091 (12)), or optimization FOC (P094 (21); P102 (48)), or program value (P050 (9); P031 (2.6)).
2. **Check semipermeability.** Either implicitly via the value (each side's optimality prevents crossing), or explicitly: P099's AR method (asserted); P098 Remark 2 (asserted); P041 Thm 7 (proven: moving region stays inside the initial one).
3. **Verify against HJI.**
   - *Classical route*: show $V \in C^1$ (envelope argument $dV/dx^* = 0$: P022 (64)–(65); P044 steps 1–3 incl. the $F_1 - F_2 \ne 0$ sign argument; P031 determinant identity (3.20)), then evaluate $\nabla V \cdot f$ at equilibrium fields and cancel term-by-term (P022 (67) = $-\alpha/2 - \alpha/2 + \alpha$; P044 (40) = $1 + \partial V/\partial x\cdot f = 0$; P096 (37)–(47)).
   - *Nonsmooth route*: continuity (Berge/Gauvin–Dubeau), Clarke subdifferential via Danskin (P050 Lemma 1), then $F(\xi) = 0$ for all $\xi \in \partial V$ (P050 Thm 2 step 5), or the $m$-branch convex-hull inequality on kinks (P019 Lemma 1 + Lemma 7), closing with Crandall–Lions uniqueness (P019 Thm 1 step iv).
   - *Sensitivity route*: parametric NLP + SOSC ⇒ classical Isaacs (P048 Thm 2); LICQ ⇔ $C^1$ (P050 Thm 1(3), via Wachsmuth).
4. **Handle the singular set.** Dispersal surfaces: verify exit-transversality **and** the viscosity condition (P019 Remark 3; counterexample $\Upsilon_2$ where the naive max-value fails, Fig. 3); or exclude them from the regular region (P044). Switch envelopes via the ODE (35)–(36) (P019 Thms 2–4). Focal surfaces: open everywhere they arise (P019).
5. **Glue the pieces.** Continuity + gradient matching at region boundaries (P022 p. 564: $V_s = V_g$ and shared gradient (66)/(60)–(61) ⇒ $C^1$, no singular surfaces); piecewise classical + continuous ⇒ viscosity *if verified* (P031 §4.4 — flagged as asserted).

**Worked end-to-end exemplars to imitate**: P022 (Theorems 1–3 with the full equation inventory (1)–(92)); P031 (Theorem 2.1 with Appendices A–C); P050 (Theorems 1–2, 7 steps); P044 Theorem 2 (the most explicit cross-boundary $C^1$ computation in the library).

**Anti-patterns to avoid** (documented failures/gaps): squaring without a sign filter (P022; P091 (21)); merging sub-game barriers without a joint-sufficiency proof (P094 Thm 5.1; P073 Algorithm 1); "unique point in $\mathcal{T}$" claims that hold only in a restricted plane (P073 $c_{i,j}$); informal coverage/pigeonhole arguments for coalition cones (P091 Thm 5); straight-line optimality asserted from "Mayer cost + simple motion" without derivation (P102 Lemma 2; P094 p. 3; P033 "intuitive claim, not proved").
