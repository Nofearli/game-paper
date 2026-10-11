# Theorem–Proof Patterns — Library Catalog

Recurring proof patterns actually used in the 100 per-paper archives (`papers/PXXX.md`). Each entry: when it applies, a LaTeX template skeleton, and 2–3 exemplar instances with what was proven. Page/eq references propagate from the archives. The final section lists the library's most common proof gaps (with frequencies) for the checker.

---

## Pattern 1. Apollonius tangency / algebraic characterization (equal-time identity → quadratic → root discipline)

**When.** Deriving the boundary of a dominance region or barrier in closed form from a time-balance condition with a capture radius or an offset.

**Template.**
```latex
% Time balance (the defining identity):
t_E(x) = ||x - x_E||/v_E,   t_P(x) = (||x - x_P|| - r)/v_P,
% On the boundary t_E = t_P  =>  ||x - x_E|| = alpha(||x - x_P|| - r).   (oval)
% Law of cosines in triangle (P, E, x) with inclusion angle theta:
(1-alpha^2)rho^2 - 2(alpha^2 d^{PE}_e cos theta - alpha r) rho + alpha^2(r^2 - d^2) = 0,
% discriminant Delta(theta) >= 0 selects the visible angular sector; roots:
rho^{pm}(theta) = ( ... +/- sqrt(...) ) / (1 - alpha^2),
% the "+" root is the outer (spurious) branch; keep the "-" (inner) branch.
```
**Exemplars.**
- P022, Thm 3 (pp. 564–567): AC-tangent-to-bisector condition (88) → collapsed identity (90) → conic (82)–(83); conic identification by discriminant $-\alpha^2(1-\alpha^2) < 0$. Proven the ATDDG barrier hyperbola.
- P094, Lemma 3.2 (p. 4): sine rule (9) + time balance (10) → quadratic (13), two roots (14); the "+" root violates (10) (outer oval) — the root discipline is stated. Proven the oval capture law $\varepsilon = \arcsin(\tfrac{r_2}{ar_2+l}\sin\varsigma)$.
- P091, Thm 3 (pp. 6–7): law of cosines → quadratic (17); zero-discriminant condition gives the half-angle $\theta_{ji}$, hence the advantage angle $\gamma_i = 2\theta_{ji}$; $\rho_i = 0$ recovers $\gamma_i = 2\arcsin\mu_{ji}$ (Remark 8).
- P102, Lemma 3 (p. 7): polar quadratic (22) → unique admissible root (23) = the l-Apollonius circle; degenerates to Isaacs' AC at $l = 0$.

---

## Pattern 2. Equal-time / equal-distance identity, then complete the square

**When.** Deriving Apollonius-type loci, tangent-cone angles, and isochrone circles.

**Template.**
```latex
% From the equal-time identity with ratio alpha:
||x - x_P|| = alpha ||x - x_E||   (r = 0)
% Squared and completed:
(1-alpha^2)||x||^2 + 2(alpha^2 x_E - x_P)^T x + (||x_P||^2 - alpha^2||x_E||^2) = 0
% => center/radius in closed form.
```
**Exemplars.**
- P013, Lemma 1 (p. 4, eq. (6)): right triangle on the Apollonius sphere, $\|O - T\| = r/\lambda$ via eqs. (4)–(5) ⇒ $\sin\theta = \lambda$, position-independent tangent-cone angle.
- P052, pp. 1300–1301 (eqs. (4)–(6)): isochrone intersection of a 3D pursuer and a planar evader completes to a circle with altitude-dependent center/radius.
- P066, eq. (2) (p. 2): disc form $c_i, r_i$ of the Apollonius disc, used later inside area-gradient computations.

---

## Pattern 3. HJI verification via the envelope argument $dV/dx^\ast = 0$

**When.** A candidate value is expressed through an implicitly defined aimpoint (interception point, tangency point, optimal target point); differentiability of $V$ and the HJI identity must be proven without closed-form gradients of the aimpoint.

**Template.**
```latex
% V(x) = Phi(x, z*(x)) with z* defined by the stationarity g(x, z*) = 0.
dV/dx = Phi_x + Phi_z z*_x;   differentiate g: g_x + g_z z*_x = 0.
% Decisive step: show Phi_z = mu * g_z^T (parallelism), hence dV/dx = Phi_x - mu g_x,
% which vanishes exactly because z* solves the (squared) design equation.
% Then evaluate the HJI residual at the equilibrium field and cancel term-by-term.
```
**Exemplars.**
- P022, Theorems 1–2 (eqs. (64)–(65), (78)–(79)): $dV/dx^*$ equals the design-equation residual (55)/(79) evaluated at the quartic root, hence 0; HJI residual (67) collapses to $-\tfrac{\alpha}{2} - \tfrac{\alpha}{2} + \alpha = 0$. Proven the $C^1$ Value $\alpha\,\mathrm{AI} \pm \mathrm{TI}$ solves HJI with no singular surfaces.
- P044, Thm 2 (pp. 1057–1058): in the simultaneous-capture region the $\partial V/\partial\phi^*$ term vanishes via $\partial t_{f_i}/\partial\phi^* = F_i t_{f_i}$ and $t_{f_1} = t_{f_2}$; the residual $\partial V/\partial x \cdot f = -1$ follows from the per-pursuer identity (39); $C^1$ across the $\mathcal{R}_1/\mathcal{R}_s$ boundary verified by evaluating both sides at $\phi^* = \lambda_1$ (eqs. (30)–(31)).
- P031, Steps II–III (eqs. (3.13)–(3.21)): chain rule through the implicit tangency point $p^*$; the determinant identity (3.20) collapses $[\partial_{p_D}V^g]_{F_{\alpha^*}} = [\varphi_{y^*}/d_{y^*};\,0]$ and $[\partial_{p_I}V^g]_{F_{\beta^*}} = -a[\varphi_{y^*}/d_{y^*};\,0]$, exactly the structure Lemma 3.2 (eq. (3.9)) demands.
- P050, Thm 2 step (5) (p. 6362): the same cancellation executed in the Clarke subdifferential — $F(\xi) = 0$ for every convex combination of active-multiplier gradients (stronger than the viscosity inequalities (7)–(8), which hold with equality).

---

## Pattern 4. PMP necessary conditions + TPBVP reduction to a scalar design equation

**When.** Simple motion with Mayer cost: derive candidate saddle strategies and the aimpoint.

**Template.**
```latex
% Hamiltonian (separable => Isaacs condition holds):
H = sum_k lambda_k f_k(x, u_k);   ME1: min_u max_v H = 0.
% Stationarity: u_k^* = +- lambda_k / ||lambda_k||  (sign by minimization side).
% Costate dynamics: dot lambda = -H_x = 0  =>  constant costates  =>  straight-line play.
% TPBVP: augment Phi with multipliers nu for the terminal manifold;
%        transversality lambda(t_f) = dPhi_a/dx;  eliminate nu;  H(t_f) = 0 fixes t_f.
% Reduce to ONE scalar unknown (aimpoint coordinate), square => quartic; select root.
```
**Exemplars.**
- P022, Theorem 1 (pp. 556–561): eqs. (18)–(32) transversality chain; design equation (55) → quartic (15)–(16). Gap: root selection after squaring (≥ 2 real roots exist, p. 564; sign filter not stated).
- P044, Sec. V ATDDG (pp. 1062–1064): eqs. (52)–(60), (75)–(90); quartic (49) **with** explicit root and sign selection rules ($x_T \lessgtr 0$).
- P052, Lemma 1 (p. 1301): control is an LP over a ball ⇒ bang-parallel; constant costates.
- P061 (eqs. (7)–(11)): damped dynamics give exponential costates; max-acceleration constant-heading optimality.
- P055, §IV-A (pp. 1857–1858): force-allocation PMP (bang-bang, full acceleration then coast) + 1-D search over the frozen ratio $\bar\alpha$.
- P108, Thm 1 (eqs. (19)–(22), (29)): adjoint antisymmetry halves the 12-state/12-adjoint system to 6+6 with 4 scalar unknowns.

---

## Pattern 5. Viscosity-solution verification and uniqueness via comparison

**When.** The candidate value is nonsmooth (kinks, switching surfaces) or differentiability cannot be established.

**Template.**
```latex
% (i) V continuous (Berge/Gauvin-Dubeau or explicit continuity argument).
% (ii) Off the kink set: classical C^1 verification (Pattern 3).
% (iii) On the kink set with m branches u = min_i u_i (distinct gradients):
%       F(x_0, sum_i lambda_i grad u_i(x_0)) >= 0  for all lambda in the simplex.
%       Proof: no test function attains a local min of u - phi (else pairwise
%       min-branches force ||grad u_i - grad u_j||^2 <= 0); KKT at the lifted
%       minimum gives grad phi = sum lambda_i grad u_i; converse by test phi = sum lambda_i u_i.
% (iv) Uniqueness: comparison principle (Crandall-Lions).
```
**Exemplars.**
- P019, Lemma 1 (eq. (2), p. 560) — the $m$-branch lemma generalizing Melikyan's $m = 2$; Lemma 7 (eqs. (23)–(26)) executes (iii) geometrically on the dispersal set $\Gamma$; Theorem 1 (p. 565) closes with Crandall–Lions [27, Th. 3.1]. Proven: $J_1$ is the unique viscosity solution of $\tilde H(\nabla J_1) = 0$.
- P031, §4.4 (p. 7): MDSI closure — continuity of $V^g$ across SDSI/2DSI switches + "piecewise classical ⇒ viscosity" (archive flags the sub/supersolution inequalities as asserted, not verified).
- P050, Thm 2 (pp. 6361–6362): Fréchet ⊂ Clarke (Frankowska, Lemma 2) lets one verify both viscosity inequalities from a single statement about all of $\partial V$.
- P040, (12)–(15): upper value = constrained viscosity solution by Evans–Souganidis-type representation (attributed).

---

## Pattern 6. Dominance-region construction by contradiction ("if $x$ were reachable, then…")

**When.** Proving a point belongs to (or is excluded from) a dominance/reachable region under adversarial quantifiers $\exists u_e\,\forall u_p$.

**Template.**
```latex
% Lemma (path invariance): if x in D(x_1, x_2) and r*_x is a shortest path x_2 -> x,
% then r*_x([a,b)) subset D.  Proof: for s < b,
%   d_L(x, x_1) <= d_L(r*_x(s), x_1) + d_L(r*_x(s), x)   (triangle ineq.)
%              < d_L(r*_x(s), x_1) + alpha d_L(r*_x(s), x)  (x in D, strict)
%              <= alpha d_L(x, x_2)   (shortest-path additivity)  -- contradiction.
% Theorem: R_e = D by two inclusions with exact arrival times t_p, t_e.
```
**Exemplars.**
- P041, Lemma 6 + Theorem 5 (pp. 4–5): exactly the chain above with the decisive inequality $d_L(x,x_{p0}) < \alpha d_L(x, x_{e0})$; the $D^c \subseteq \mathcal{R}_e^c$ direction uses first-exit times and the "retrace the trajectory" capture argument. Proven dominance = reachability with obstacles ($l = 0$).
- P041, Example 13 (p. 8): non-existence by contradiction against the non-anticipativity axiom (eq. (3)) — two indistinguishable evader prefixes force distinguishable pursuer replies. `[necessity step asserted]`
- P091, Thm 1/Thm 6 endpoint step: if $\|x^0_{D_i} - E\| > \|x^0_{A_j} - E\|/\alpha_{ji} + \rho_i$ the attackable region cuts the target line in infinitely many points (attacker wins); if $<$, in none; equality is the barrier arc `[endpoint argument; interior-reduction asserted]`.

---

## Pattern 7. Set inclusion / invariance by rate comparison (Nagumo-type without Nagumo)

**When.** Proving a moving safe region never shrinks past a fixed one, or that a scalar margin is monotone.

**Template.**
```latex
% Define the margin phi(x, t) = d_L(x, x_p(t)) - alpha d_L(x, x_e(t)) (or a clock gap).
% Boundary evolution: phi(C(s,t), t) = 0  =>  grad phi . dC/dt = -phi_t   (chain rule).
% Show phi_t <= 0 on the boundary under the candidate strategy  (Lemma, case analysis).
% Conclude the moving set stays inside the fixed one:
%   support-hyperplane/QP argument: min over the moving set of <nabla phi(x_d,0), x - x_d>
%   has KKT solution x_H(t) with nabla-parallelism; Rockafellar Thm 18.8 closes the
%   intersection over all boundary points.
```
**Exemplars.**
- P041, Theorem 7(b) (pp. 6–7): QP (14), KKT (16)–(18), $\partial_t\phi(x_H(t),t) \le 0$ via the angular comparison Lemma 8 ($|d\psi/d\chi| \le 1$ on the oval, decisive factorization $f_2 = -\tfrac{r_1}{\alpha^2}[(\alpha^2-1)(r_1-l)^2 + \alpha^2(\sigma^2-l^2)] < 0$); closed by Rockafellar Thm 18.8. Proven confinement of the moving dominance region + capture bound $t_f \le t_0 + \frac{\|x_{p0}-x_{e0}\|-l}{\alpha-1}$.
- P102, Lemma 5 (pp. 9–10): differentiate $F(x_H) = 0$; Cauchy–Schwarz gives $\dot y_H \ge 0$ with equality iff the evader heads at $H$ — the lifeline never approaches.
- P077, Corollary (p. 701): both clocks $\varphi_s, \varphi_T$ decrease at unit rate, so $\varphi_s > \varphi_T$ is preserved — transport invariance in one line; the same paper's Prop. 6 lacks the formal Nagumo condition (documented gap, p. 702).
- P060, Lemma 3 + Thm 1 (p. 4): closed-loop confinement to the Cartesian oval; two defenders by set intersection.
- P046, Lemma 1 (eqs. (6)–(9)): CBF forward invariance of $\mathrm{Int}(C_j)$ requiring only boundedness of the nominal strategy.

---

## Pattern 8. KKT / duality for multi-player programs (strong duality → Danskin → Clarke)

**When.** The value is the optimal value of a convex program parameterized by the game state; gradients/subdifferentials and equilibrium strategies must be extracted.

**Template.**
```latex
% V(theta) = min_x d_T(x) s.t. f_i(x, theta) <= 0 (strictly convex, coercive; Slater holds).
% Lagrangian L; dual q(lambda, theta); strong duality: V = max_{lambda >= 0} q.
% KKT: nabla_x L = 0, sum lambda_i f_i = 0, lambda >= 0; saddle property of L.
% Generalized Danskin: partial V = conv{ nabla_theta L(x*, lambda) : lambda in Lambda(theta) };
%   C^1  <=>  LICQ (multiplier unique).  Rademacher: LICQ fails only on a measure-zero set.
% Equilibrium controls: u_i^* = (pointwise Hamiltonian minimizer) evaluated at
%   grad V / a Clarke element; only strongly-active defenders contribute.
```
**Exemplars.**
- P050 (Prop. 1, Prop. 2 uniqueness by contradiction via strict convexity, Lemma 1 = generalized Danskin [Clarke 1975], Thm 1 (eqs. (27)–(28)), Thm 2, strategies (33), coalition partition (34)). Proven: viscosity solution on all of $\Theta$; classical iff LICQ.
- P021 (Automatica 2025): two-phase CTF value = quasi-convex program (19) with inner convex program (18); Danskin-based state-gradient machinery (eqs. (30), (31), (36), (37)) certifies equilibrium via the Isaacs condition; defender-redundancy $|E| \le 2$ from KKT with linear independence in $\mathbb{R}^2$ (Thm 15).
- P018 (Thms 3–4): cooperative two-guarder defense via value functions $h_i$ + Danskin's theorem under a "uniform minimizer" structural assumption.
- P048 (Thm 2): Fiacco-type — at SOSC minimizers of the stacked capture-point program, $V \in C^1$ and satisfies Isaacs classically.
- P103: KKT–Isaacs equivalence (HJI equals a convex program) for the ES certificates.
- P107 (eqs. (16)–(20)): KKT argument on the minimum-distance problem proving the penetration condition for non-convex targets.

---

## Pattern 9. Matching / assignment optimality (bounds closure, degeneration, approximation)

**When.** Many-vs-many games reduced to pairwise/subgame values plus a combinatorial layer.

**Template.**
```latex
% Lower bound (intruder/evader side): construct a family G of disjoint local regions;
%   guaranteed score Q = max_G sum_{k in G} max{q^k, 0} (max-weight independent set /
%   matching on the conflict graph), realizable against ANY defender strategy.
% Upper bound (defender side): policy realizing the same quantity.
% Close the two:  V = Q  (saddle point in the team objective).
% Degeneration: any coalition acts through at most K members (support-constraint /
%   circumcenter counting)  =>  polynomial-sized subgame family + bipartite matching.
```
**Exemplars.**
- P015 (eqs. (6)–(7) vs. (10), pp. 3–6): intruder bound $Q_{LG} = \max_G \sum_{k\in G}\max\{q^k,0\}$ in $O(N_D^4)$ (max-weight independent set on a circular-arc graph); defender LGR policy closes it into a saddle point. Proven team-vs-team exactness for a class of configurations.
- P100 (Thms 1–4, Lemma 3): inductive coalition barriers; "every multiplayer barrier segment depends on at most two pursuers"; task assignment = small 0-1 ILP.
- P103 (Secs. 3–4): ES certificates $\bar E(s,j) = \{f_{ij} \ge 0, i \in s\}$; degeneration "at most three pursuers necessary in 3D" collapses coalition space to $O(N_p^3)$; matching on top.
- P037: $V(\mathbf{x}) = \max_\iota y_{s_\iota}(\mathbf{x})$ over assignments; hybrid guidance+assignment without PDEs.
- P089: MBMC (maximum bipartite matching with conflict graph) + sequential matching approximation.
- P045 (Thms 1–2): hedonic coalitions — Nash-stable partition exists under single-peaked-at-one preferences; convergence in $\le |A|(|A|+1)/2$ iterations (minor counting gap flagged, p. 1538).
- P105 (Thm 1): ERP winning needs at most two pursuers per evader — support-constraint counting à la Calafiore–Campi.

---

## Pattern 10. Supporting-hyperplane / convexity arguments

**When.** Uniqueness of tangency/aim points; containment of moving regions; well-posedness of auxiliary programs.

**Template.**
```latex
% Strict convexity of the region (curvature-sign computation in a canonical frame):
%   place x-axis along the fold; show sign(d^2 y/dx^2) = sign(d_y) via
%   (d_y)^3 R_I d^2y/dx^2 >= (a^2-1)(1-cos^2(alpha-beta)) >= 0.
% Uniqueness of tangency: F(z) = 0, F_x(z) = 0 has a unique solution by
%   reduction to a monotone function G(beta) (sign factorization of G').
% Containment: supporting hyperplane at each boundary point + intersection argument.
```
**Exemplars.**
- P031, Lemma 2.1 (App. C): convexity of the oval dominance region via the decisive inequality above.
- P102, Lemma 1 (eqs. (12)–(18)) + Lemma 4 (eqs. (28)–(35)): monotone $G(\beta)$ ⇒ unique tangency point $H$ ⇒ well-defined $\dot x_H$; used again for information-structure independence (eq. (52)).
- P050, Prop. 1–2: strict convexity/coercivity of $f_i$ (decisive bound via triangle + Cauchy–Schwarz); uniqueness of the capture point by the two-saddle-points contradiction with the strict-convexity strict inequality $(*)$.
- P091, Thm 7: monotone ratio function $F(\epsilon)$ with $H_2'(\epsilon) = 3r_4(1-\epsilon)(r_3(1+\epsilon) + 2r_4\epsilon) > 0$ ⇒ unique offensive target point.
- P041, Lemma 8 (eqs. (7)–(10)): angular comparison $|d\psi/d\chi| \le 1$ on first-type ovals via the factorization of $f_1 \pm f_2$.

---

## Pattern 11. Monotonicity / rate arguments for capture-time guarantees

**When.** Certifying finite-time capture or quantitative bounds without a value function.

**Template.**
```latex
% Lyapunov-style: pick E = kA + ||x_e - x_p||^2 (area + distance); show dE/dt <= -c < 0
%   against all admissible evader inputs => capture in finite time.
% Or rate comparison: d/dt ||x_p - x_e|| <= f(chi), f monotone, integrate f(pi) = 1 - alpha
%   => t_f <= (||x_p0 - x_e0|| - l)/(alpha - 1).
```
**Exemplars.**
- P113, Thm 3: energy $E = kA + \|x_e - x_p\|^2$ decreases at linear rate $c(\beta)$ under the Voronoi area-descent law; finite-time decentralized capture.
- P041, Thm 7(a): $\tfrac{d}{dt}\|x_p - x_e\| \le f(\chi) = -\alpha\sqrt{1 - \tfrac{1}{\alpha^2}\sin^2\chi} - \cos\chi$ with $f' \ge 0$, $f(\pi) = 1 - \alpha$; integration gives the explicit uniform bound.
- P023, Thm 1: Lyapunov containment of the time-varying AC; capture bound $t \le t_0 + 2(1+\nu^{-1})R_C\ln(R_C/\delta)$; Lemma 1 gives strict distance decrease.
- P097 (Thm 3): finite-time capture certificate via monotone decrease of the current shortest capture time (CSCT).
- P106: hierarchical receding-horizon allocation with a monotone defeat-count guarantee.

---

## Pattern 12. Decomposition / bond of sub-game barriers

**When.** Multi-pursuer games where each sub-game has an explicit barrier; the team barrier is assembled from parts.

**Template.**
```latex
% Sub-games (P_i, E) each yield a barrier B_i (Pattern 1 or RPE integration).
% Classification: which pursuers are "active" (contribute) — closed-form predicates
%   on the initial configuration (Lemma chain).
% Team barrier = union of contributor barriers (or the "bond": evader's barrier
%   trajectory switches at intersection points of sub-game curves).
% Winning subspaces: W_P = union, W_E = intersection (complement).
```
**Exemplars.**
- P073 (Lemmas 1–3 classify contributors; Thms 1–3 give arc/patch pieces; Algorithm 1 unions coalitions) — merge formulas unproven for general $n$ (gap (e)).
- P112 (Thm 2): the bond of $\mathscr{B}_1,\mathscr{B}_2$ with switching at $(\tilde x, \tilde y)$; joint capture zone = union "because the pursuers play individually" `[asserted]`.
- P094 (Thm 5.1): eight-curve merge `[sufficiency gap; regions 7–8 patched by reachable-set test]`.
- P099 (Thm 1): necessary and sufficient condition for the barrier to depend on only one defender ($x^0_{D2} \in \mathcal{W}^1_D \cup \mathcal{B}^1$).
- P100 (Thm 3 + Lemma 3): inductive construction along an $x$-rank index set; every segment depends on ≤ 2 pursuers.

---

## Pattern 13. Singular-surface certification (exit-transversality + viscosity condition)

**When.** A candidate value is built from branches glued on a dispersal/switch surface; must decide whether the glue is the true value.

**Template.**
```latex
% Branches J_i, gradients q_i. On the surface Upsilon = {J_1 = J_2}:
% (1) necessary conditions: f_lambda(0) = (q_2 - q_1)^T F*(q_1) <= 0,
%                           f_lambda(1) = (q_2 - q_1)^T F*(q_2) >= 0.     (28)
% (2) counterexample check: is max_lambda f(lambda, X) > 0 somewhere on Upsilon?
%     If yes, max_i J_i is NOT the value (defender strictly improves both branches).
% (3) On the certified part: m-branch convex-hull viscosity check (Pattern 5)
%     + exit-transversality H(F*(d_j), d_i) > 0  =>  dispersal surface.
% (4) Switch envelopes: singular-arc ODE  dot X = F*(p), dot p = a(X,p)(p - q(X)),
%     a from (p-q)^T F*(p) = 0 differentiated in time.
```
**Exemplars.**
- P019, Sec. V (Lemmas 8, eq. (29); Theorems 2–4): the naive $\bar V = \max\{J_1, J_2\}$ fails on the numerically exhibited set $\Upsilon_2$ (Fig. 3: $f_\lambda(0,X) > 0$ for $\alpha_i \in [0.01, 0.9]$); and (28) is necessary but **not** sufficient (Fig. 4 point with $\max f = 0.0054 > 0$ at $\lambda_m = 0.15$). Focal surfaces left open.
- P044 (p. 1056, p. 1059): 2P1EDG dispersal surface $D$ excluded from the regular region; "pursuers pay an infinitesimally small price for guessing incorrectly"; perpetual dilemma noted.
- P038 (eq. (34)): Phase-II dispersal $\{y_A = y_D\}$ with $C^1$-except-there value.
- P037: dispersal surfaces $y_{s_\iota} = y_{s_{\iota'}}$ between assignments, outside which $V$ is $C^1$ and HJI-satisfying.
- P076: five-surface taxonomy (EDS, ESCS, PES, PDS, PSCS) with the no-barrier single-outcome finding ($V_a^{\max} \lessgtr V_r^{\max}/b$).

---

## Pattern 14. Numeric counterexample hygiene

**When.** Disproving a candidate (a value formula, a strategy, an algorithm's guarantee), or bounding a claim's validity domain.

**Rules distilled from the library.**
(i) Exhibit the counterexample *as a set with positive measure or a concrete instance with printed coordinates*, not as a remark: P019's $\Upsilon_2$ with swept parameters $\alpha_2 \in [0.01,0.9]$, $\alpha_1 \in \{0.3, 0.5, 0.8\}$ (Fig. 3) and the single plotted point violating sufficiency (Fig. 4); P041's Example 13 with $x_{p0} = (4,5)$, $x_{e0} = (2,-1)$, $\alpha = 1.5$ and the 5° corner; P001's Fig. 3 (§4.1, pp. 111–112) showing the Radius algorithm's failure mode on narrow cones.
(ii) Separate necessity from sufficiency numerically (P019 Fig. 4: (28) holds yet $\max f > 0$).
(iii) Check the printed algebra against rendered pages and record errata: P031's (A.9) typo $k_{x_I}$ vs $k_{y_I}$ and the $\Omega$ sign slip in (4.7); P094's Hamiltonian $\sin/\cos$ swap (p. 3); P044's repeated $\dot\lambda_{y_{P1}}$ (p. 1055); P073's ill-defined $c_{i,j}$ and mislabeled typeset items; P036's eq. (1) state typo verified at 400 dpi.
(iv) Stress the degenerate parameters ($\alpha = 1$, $\rho = 0$, collinear/cocircular configurations): P091 Thm 6 (equal speeds), P094 Fig. 2b (a = 1 hyperbolas), P102 ($l = 0$ degeneration to Isaacs' AC).

---

## The library's most common proof gaps (checker's list, by frequency)

1. **Straight-line/max-speed optimality asserted, not derived** — "follows from simple motion and Mayer cost" with no PMP or verification argument. Instances: P102 Lemma 2 ("entire proof" one sentence, p. 7 — the most consequential informal step, since the OTP construction and Lemma 7 build on it); P094 (p. 3); P033 (Assumption-1 discussion, p. 2087: "an intuitive claim, not proved"); P091 (max-speed play assumed citing precedent, p. 3); P062/P096 (standard assumption). *Frequency: high (≥ 6 archives).*
2. **No HJI/Isaacs verification at all — optimality argued geometrically** (dominance + FOC + monotonicity, strategies open-loop straight lines). Instances: P091 (archive observation 6: "no formal Isaacs/HJI verification... anywhere"); P094 (no value-function theory; barrier property asserted, p. 5); P073 (no strategies constructed); P112 (RPE construction presented but the classic BUP route blocked by the indeterminate terminal component); P099/P100 (semipermeability invoked, not proven); P106. *Frequency: high (≈ 8 archives in the geometric-barrier school).*
3. **Key lemma outsourced to a citation.** P094 Lemma 3.1 → "a proof provided by [35]" (= P031); P102 Lemma 3 sufficiency (triangle-inequality argument "not written out"); P102 Lemma 3.2-analog tangency chaining → Dutkevich–Petrosyan; P044 Theorem 1 (HJI verification theorem cited to Hespanha); P041 Example 13's necessity step (heuristic). *Frequency: medium (≈ 5).*
4. **Root/branch selection after squaring left implicit.** P022 (quartic (15): ≥ 2 real roots; no sign filter; "the coordinate x is a real solution"); P091 (quartic (21) with "polynomial constant" phrasing); contrast the good practice of P044 (explicit rules for (49)). *Frequency: medium (≈ 3).*
5. **Merge/decomposition sufficiency unproven.** P094 Thm 5.1 (pairwise merge; joint/sequential effects unanalyzed); P073 Algorithm 1 (coalition unions unproven for general $n$); P112 (bond asserted); P044's 5v3 assignment (exhaustive over 2-2-1 teams only, global optimality beyond enumeration unproven). *Frequency: medium (≈ 4).*
6. **Viscosity step abbreviated at switching surfaces.** P031 §4.4 (piecewise classical + continuous ⇒ viscosity asserted); P044 (dispersal surface excluded; no weak-solution treatment); P050 Thm 1(ii) ($\lambda = 0$ ray where the Lagrangian is not strictly convex — benign but unaddressed in print). *Frequency: medium (≈ 3).*
7. **Informal coverage/rate arguments.** P091 Thm 5 (ray-pigeonhole, unordered interval in (19)); P077 Prop. 6 (no Nagumo condition, informal Hausdorff sentence); P062 (speed-ratio threshold argument with boundedness claims). *Frequency: low–medium (≈ 3).*
8. **Payoff/value conventions incomplete.** P094 (payoff undefined upon capture; termination criteria leave measure-zero gaps); P086 (cost $J = r_{A_f} - 1$ presupposes team capture); P019 (game-of-kind barrier never written; practitioners threshold the value themselves). *Frequency: low (≈ 3).*
9. **Tie-breaking at dispersal points geometric rather than variational.** P022 Cor. 1 ($\kappa = \arg\min_i \Delta_i$ justified via the dual problem, not the payoff); P102 Thm 2 ("closer to L" by monotonicity); P044 (teams "guess"); P050 (undefined controls for non-strongly-active defenders). *Frequency: medium (≈ 4).*
10. **Focal surfaces / global assembly open.** P019 (focal surfaces "left as future work"; local theorems only; global gluing of $\mathcal{D}_0$ open); P076 (termination of singular construction by numerical observation). *Frequency: low (≈ 2, but structural).*
