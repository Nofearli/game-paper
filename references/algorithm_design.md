# Algorithm Design — Archetypes, Pseudocode Norms, Complexity, LaTeX Conventions

Source: per-paper archives `papers/PXXX.md` (Sections 5–6 algorithm and experiment records), synthesized 2026-10-11. Each archetype gives the standard Algorithm-environment skeleton, the mathematical justification for every step (which lemma/theorem), the recorded complexity, and the proof-gap flags to respect. Pseudocode skeletons below are composites faithful to the recorded steps — verify line-level details against the cited archive before quoting as the paper's own. Companion: `templates/algorithm.tex` (comment discipline: every step using a theoretical result carries a `\Comment` naming the equation/lemma; complexity is stated in text after the float).

## 1. Recurring algorithm archetypes

### A. Barrier enumeration + 0–1 integer program (centralized matching)
- **Recorded in**: P100 (Algorithms 1–2 + Theorem 5, eq. (50), pp. 118–121); P103 (Algorithm 1 Sequential Matching inside Algorithm 2, eqs. (28)–(30)); P104 Sec. 5 (eq. (18) generic ILP + Sequential Matching 1/N_c-approximation); P089 (MBMC sequential matching); P083 Items 8–10 (MM / MIS / LGR).
- **Skeleton** (P100-style):
  1. **Input**: initial positions, speeds ($\alpha = v_E/v_P$), radii; target line endpoints $m, n$.
  2. **for each candidate coalition** $k$ (execution coalitions of size 1–2, by Lemma 5 degeneration): compute active pursuers (Algorithm 1: intersect the target line with per-pursuer RD half-planes, eq. (47); $O(n_k^2)$ tests) — *justification*: Lemma 3/Theorem 4 (barrier equivalence to the largest full-active subcoalition).
  3. Build the barrier $\mathcal{B}^{n_k}$ from closed-form pieces $F_{1s}, F_{2s}$ (Theorems 1–3, eqs. (12)–(14)) and winning regions $W_P, W_E$.
  4. Edge $(k, j)$ exists iff $x^0_{E_j} \in W_P^{n_k}$ — *justification*: barrier separability + straight-line optimal play (Lemma 2, PMP constant costates).
  5. Solve the 0–1 IP (eq. (50)): maximize $\mathbf{c}^\top z$ s.t. feasibility ($A_1$), one-evader-once ($A_2$), pursuer-disjointness ($A_3$, enumerated by Algorithm 2).
  6. **Output**: matching $M_1, M_2$; matched pairs play their subgame feedback strategies.
- **Complexity/verification as recorded**: P100 Case 1 — 31 barriers in ≈ 0.984 s (300-point sampling dominates), IP ≈ 0.025 s; Case 2 — 0.023 s / 0.012 s (MATLAB R2016b, Core i7-8550U, 16 GB). P103: MBMC NP-hard (Theorem 4.1, reduction from 3-dimensional matching [proven]), Sequential Matching 1/3-approx (Theorem 4.2), APX-complete (Cor. 2); **no runtime numbers reported** (MATLAB R2017b, i7-8550U, 16 GB). P100 §7 flags: coalition enumeration is still $2^{N_p} - 1$; "NP-problem" is used loosely in the source.
- **Justification chain**: barrier ⇒ edge set (game of kind) ⇒ IP ⇒ exact value q for the pursuit team (Theorem 5 [proven, scoped]).

### B. Distributed k-winner-take-all dynamical network + load reassignment
- **Recorded in**: P084 (DMK-WTA, eqs. (7)–(10) + Algorithm 1, pp. 5991–5992).
- **Skeleton**:
  1. Initialize $\beta_{ij} = \theta_{ij} = z_{ij} = 0$; inputs $d_{ij}$ (distances), neighbor sets $\mathbb{N}_i^c$.
  2. **loop** (Euler discretization): update $\beta$ (winner indicator + consensus diffusion, eq. (7)), $\theta$ (integral consensus action, eq. (8)), $z$ (constraint-violation dual, $\dot{z}_{ij} = -\lambda(N_p\beta_{ij} - k)$, eq. (9)); output $\omega_{ij} = f_\Omega(z_{ij} - d_{ij}/(2a))$ (piecewise-linear saturation, eq. (10)).
  3. Resolution condition: $a \le \frac{1}{2}(d_{(k)j} - d_{(k+1)j})$ — *justification*: k-WTA dual-network structure [27] + dynamic average consensus [25]; **convergence under switching topology inherited by citation only — no proof in the paper** (archive proof gap).
  4. Reassignment (Algorithm 1): multi-load holders keep min-cost load and transfer the rest (randomized transfer with probability ρ to escape local optima, Remark 1); single-load holders swap if cost decreases; empty holders take the nearest evader.
- **Complexity as recorded**: per agent per iteration **6N_e + 15 flops = O(N_e)** (decisive count, p. 5991) vs Hungarian method O(n³). **Not proved**: satisfaction of the ≥k constraint after reassignment; any cost-ratio bound vs the KM optimum (empirical Fig. 9(b) only: DMK-WTA best for > 20 tasks; GA best below).
- **Platforms as recorded**: Webots R2020b E-puck (5×5 m², 32 ms step, k = 4); Gazebo 9/ROS Aliengo (24×24 m²); hardware Crazyflie 2.1 + OptiTrack (16 cameras, 0.1 mm); noise-robustness runs at 0/20/40% sensor noise; benchmark over N_e ∈ {2..40} × k ∈ {3,4,5}, 20 reps, baselines random/GA/KM/DPSO/DQN. **No success-rate statistics or capture-time tables** (archive Sec. 6).

### C. Distributed Hungarian + binary search (bottleneck makespan allocation)
- **Recorded in**: P054 (Algorithm 1 + Theorem 5, pp. 11–12).
- **Skeleton**: (1) each pursuer computes pairwise capture times $T_{ij}$ from the isochron capture condition (Theorem 1, eq. (15)) — *justification*: geometric construction + HJI-equation check (27), **Lemmas 1–2 proofs omitted in the source** (archive §7(1)); (2) form groups as connected components of the sensing-restricted conflict graph; (3) distributed Hungarian method per group (converges in $O(|\mathcal{Y}_i^P|^3)$ communication rounds, Lemma 7/Cor. 4 of [37]); (4) binary search the makespan over $[\underline{T}_i, \bar{T}_i]$, $O(\log\frac{\bar T_i - \underline T_i}{\delta_i})$ iterations; (5) maximum-cardinality matching at the trial makespan.
- **Complexity as recorded (Remark 5, p. 12)**: worst case $O(N^3\log\frac{\bar T - \underline T}{\Delta})$ communication rounds. **Flags**: exactness needs the global minimum gap $\delta_i$ (extra synchronization, message complexity unanalyzed; else additive $\delta_i$-suboptimal); the dynamic/event-triggered variant has **no formal guarantee**; allocation benchmark uses synthetic costs (archive §7(2)–(5)). Platform: simulation only (8-vs-10 scenario); no hardware.

### D. Decentralized hedonic-coalition iteration with mutex
- **Recorded in**: P045 (Algorithm 1 + D-Mutex Algorithm 2, pp. 1539–1540).
- **Skeleton** (per agent, infinite loop): (1) if not satisfied, pick $\arg\max$ over task-coalition pairs ($O(n_t)$ evaluations); (2) if strictly preferred, join, increment iteration counter $r_i$, draw stamp $s_i \sim U[0,1]$; (3) broadcast $\{r_i, s_i, \Pi_i\}$; (4) D-Mutex: adopt the lexicographically largest $(r_k, s_k)$ neighbor message so a unique valid partition eventually dominates under strong connectivity.
- **Justification**: Theorem 1 (existence under SPAO, induction via Lemma 1's slack $\Delta_\Pi(i)$ eq. (4)); Theorem 2 (≤ $|A|(|A|+1)/2$ iterations; the counting step is **informal as printed** — archive proof gap); Theorems 3–4/Props. 1–2 (a posteriori bounds $\alpha \ge J/(J+\lambda)$; 50% under nondecreasing social utility).
- **Complexity as recorded**: $O(d_G n_a^2)$ time steps ($O(n_a^2)$ fully connected) vs $O(n_a^2 n_t)$ centralized; per-iteration communication $O(|\mathbb{N}_i| \cdot n_a)$; unicast cap $n_c = 1$ degrades to $O(n_a^3)$ (Remark 5 trade-off). Experiments: 100-run scalability ($n_a$ up to 320, mean diameters 36–92), C₁ as low as 5×10⁻⁴, 3–4 dummy iterations per normal iteration; brute-force optimum for suboptimality at $n_a = 12$. Platform: unreported (Matlab/Python).

### E. Receding-horizon loops (forward certificates, allocation, belief games)
- **ERP receding-horizon allocation** (P105): per step solve steer-to-ERP problem (7) (an optimization whose value generates the enclosure update); 1-vs-1/2-vs-1 subgame tables (Theorem 1: ≤ 2 pursuers matter) lifted hierarchically; monotone defeat-count guarantee recorded in the archive's contribution list. Justification: enclosure-region pursuit winning (Defs. 1–3) replaces backward HJI.
- **Modified-FMM safe-reachable-set pursuit** (P113 Sec. 4): (1) FMM computes $\psi_i^c(y)$ per pursuer on a grid; (2) modified FMM grows $S_e$ from $x_e$ adding nodes with $\varphi(y) < \psi_i^c(y)$; (3) $A \approx N_s h^2$; (4) gradients by $h$-perturbation of each pursuer; recompute each instant (receding horizon). Guarantee: **capture theorem only in the convex equal-speed case** (Theorem 3); non-convex: no proof (author-stated, p. 69). Baseline note: numerical HJI pursuit restricted to 1v1 "due to complexity"; grid differentiation caused 29%/8.5% action-inversion statistics (P113 p. 69, Fig.-based).
- **IBR + ADMM under partial observation** (P027): per horizon, each coalition solves its subjective game with the virtual (chance-constrained) evader; best-response iteration (25)–(26) capped (Remark 1); distributed ADMM for the linearized collision-constrained problem. **No NE-existence or convergence proofs**; only Lemma 1's scenario-sample feasibility (eqs. (20)–(21)).
- **Level-k receding-horizon Bayesian play** (P029): receding-horizon program (4) per level; belief update (10)–(12) scores each level-k model's historical prediction trajectories; no equilibrium claimed (nonequilibrium design).

### F. CBF-QP safety filters over game strategies
- **Recorded in**: P096 (eqs. (29)–(36), Theorem 1 proof steps 7); P013 (CBF-QCQP filter eqs. (46)–(49)); P046 (analytic safeguarding control, eqs. (6)–(9), no QP).
- **Skeleton (P096-style)**: per ASV per instant — (1) compute the nominal game strategy $\mathbf{u}^{A*}_\varpi$ (eqs. (22)/(27), heading to the interception point $\mathbf{I}^*$ — *justification*: HJI verification of $V = \mathcal{B}^2/(4\Theta^2)$, eqs. (37)–(47), equidistance of $\mathbf{I}^*$ from the players); (2) form CBF constraints $\dot{h} \ge -\gamma h$ for static obstacle ($h_{\varpi s} = \|p - p_s\|^2 - \alpha_1^2$), dynamic obstacle (needs $\dot{p}_d$), and neighbor (needs the neighbor's current input) families (eqs. (29)–(34)) — *justification*: Lemma 1 [44] forward invariance; (3) solve the QP (35): minimize $\|\mathbf{u} - \mathbf{u}^*\|^2$ s.t. CBF inequalities + the body-frame velocity box via $R^{-1}_{\iota}(\psi)$; (4) map to $(U, r)$ by eq. (36).
- **Flags**: QP feasibility (CBF vs velocity box compatibility) **not analyzed**, no fallback (archive §5.3); optimality of the *filtered* signals claimed but not shown — when a constraint activates, the HJI stationarity argument no longer applies (Proof gap 2); the game-theoretic layer is verified only for the reduced point-mass guidance-point game. P046's alternative avoids the QP entirely: reciprocal CBF $B_j = b_j^2$ with $u^s = -c_j B^\top \nabla B_j$ and Lemma 1 giving invariance under any bounded nominal strategy — the tanh-bounded ADP saddle (eq. (16)) supplies the boundedness.

### G. Value-iteration / ADP solvers for nonzero-sum games
- **Recorded in**: P085 (cVI, eqs. (10)–(12), Theorem 1); P046 (off-policy ADP for the two-player game, HJI eq. (17)); P078 (minimax Q-learning, §9 of `optimal_strategies.md`).
- **Skeleton (P085 cVI)**: (1) partition players into an adapting player and non-adapting players; (2) with others' policies frozen, solve player i's single-controller HJB by value iteration (evaluation (11) → improvement (12)); (3) switch roles in a pre-ordered loop until convergence. *Justification*: best-response HJB (eq. (10)) reduces to the single-system VI whose convergence is Lemma 2 (carried from Bian–Jiang); Theorem 1 proves convergence to $V_i^*$ [proven]. Recorded contrast (P085 archive): VI needs no admissible initial policy, unlike policy iteration — the "VI-vs-PI contrast point".
- **Guarantee boundary**: P085's convergence is for the ADP model class (finite approximation architecture unaddressed in the archive record); P078's minimax QL with linear approximation has **no convergence theorem**; P097's FIP argument connects to deep Q-learning only by analogy (archive gap 10).

### H. Indirect TPBVP solvers (PMP two-point boundary-value problems)
- **Recorded in**: P108 (Algorithm 1, pp. 5–6); P053 (MATLAB `vpasolve` for tangency timings); P055 (1-D extremal search instead of full TPBVP); P022 (quartic closed form — the "solved by hand" limit of this archetype).
- **Skeleton (P108 Algorithm 1)**: Input $x^P(0), x^E(0), t_0, \omega, \varepsilon$; (1) PSO minimizes $F^\top K F$ (eq. (38)) for the initial guess $\xi_0$, $\xi = [(\lambda^r_f)^\top, \tau_f] \in \mathbb{R}^4$ — *justification*: Theorem 1 reduction (adjoint antisymmetry eq. (18)); $\lambda^v_f = 0$ enforced by construction (eq. (26)); (2) evaluate $F(\xi) = [\mathbf{r}_f; \tilde H_f]$ by STM propagation (eqs. (26)–(29)); (3) damped Newton $\xi \leftarrow \xi - \alpha J^{-1}F$ with analytic $\tau_f$-blocks (eqs. (32)–(33)) and finite-difference $\lambda^r_f$-blocks (eqs. (34)–(36)) — *justification*: sign-function discontinuity blocks the sensitivity ODE (Remark 1); (4) stop at $\|F\| < \varepsilon$; reconstruct controls (27) and trajectory.
- **Complexity/verification as recorded**: two successes — total ≈ 24.8 s / 24.4 s (PSO-dominated), Newton 7 iterations ≈ 0.10 s, terminal miss 0.18 m / 0.14 m; one **failure case** (> 2 km miss) attributable to the cube-constrained sign function (single-thruster control succeeds on the same initial condition — the paper's conjecture); retry parameters (swarm 500, 800 iterations, $\alpha = 5\times10^{-6}$) also fail (MATLAB, 2.7 GHz, 8 GB). **Converse direction of Theorem 1 (sufficiency) asserted, not proven**; PSO/Newton have no global guarantees (archive §5.6).
- **Speed-varying alternative** (P055): replace the TPBVP by force-allocation PMP + 1-D extremal search over $\bar\alpha$; verification via C¹-in-ratio Lemmas 1–2 + HJI substitution (Theorems 1–3). **Isochron root-finding alternative** (P061 Algorithm 1): bracketed root-finding for circumscribing/inscribing isochrone times (≥1, ≤3 roots, Theorem 1).

### I. Curriculum RL pipelines (constrained multi-agent training)
- **Recorded in**: P111 (HMATD3 + adaptive curriculum, §III); P003 (hybrid PPO + speed-ratio curriculum); P072 (curriculum + adversarial co-evolution).
- **Skeleton (P111-style)**: (1) environment: CW STM discretization (eq. (2)) with impulsive maneuvers at interval Δt; (2) per step: MATD3 actor/critic updates **plus** Hamilton-regularization loss on value networks (eqs. (18)–(27)) — heuristic, no proof; (3) curriculum: update Δt by the staircase map of a sliding-window truncated success rate (eqs. (28)–(30)) — note Δt fixed within an episode (Assumption 1(3)) but varies across episodes; (4) reward: process-oriented + terminal components (eqs. (31)–(35)); (5) constraint handling: sun-elevation vector rotation + impulse correction $\Delta\bar v = \mu_v \Delta v_{adj} + \Delta v$, $\mu_v = 0.2$ (eq. (38)) — **no feasibility check**.
- **Platform as recorded**: 3-D geostationary TAD (35 786 km), single RTX 1060, ≈ 10 h training; baseline = quoted discrete LQ Nash (Section IV-D) whose gain form the archive flags as non-standard (does not match $(R + B^\top P B)^{-1}B^\top P\tilde A$). P003 platform: three-phase speed-ratio curriculum 0.7×→0.9×→1.1×; P072: Unity3D ML-Agents, MA-POCA.
- **Analytic-terminal alternative** (P017): MAPPO in BenchMARL/VMAS, 20 parallel envs, 1.2–1.8M frames, 3 seeds; episodes terminate at sensing with the analytic Nash payoff $J^*$ (Algorithm 1) — saves pursuit simulation (Prop. 2 heuristic $T_p$) and yields +10%/+18.9% reward; hyperparameters (γ, λ_GAE, clip, lr, sizes) **unreported**; 3 seeds, no significance tests.

### J. LLM-driven assignment with analytic corrections
- **Recorded in**: P059 (TARA-LLM, Algorithms 2–4 corrections $C_u, C_r, C_p$; two-chain planning $f^{plan}$).
- **Skeleton**: (1) build prompts from analytic knowledge objects ($K_w$ winning from Lemma 2/Def. 2; $K_r$ coalition reduction from Lemma 3; $K_c$ BIP constraints from (2)); (2) chain 1 evaluates 1v1 subgames, chain 2 evaluates 2v1 subgames (separated by $K_r$); (3) merge under $K_c$ into a candidate matching $M_0$; (4) corrections remove unreasonable pairs ($C_u$), redundant pursuers ($C_r$), physically infeasible assignments ($C_p$) — *justification*: the analytic layer; the LLM is a search prior. Hardware validation recorded: 6-AAV motion-capture platform (archive [CITATION]). Guarantee: inherited from the analytic knowledge; the LLM step itself is **[asserted/H]**.

## 2. Complexity table (per-paper, as recorded in the archives)

| Paper | Algorithm | Recorded complexity / timing | Platform (as recorded) |
|---|---|---|---|
| P015 | LGR defense policy (Algs. 1–4) vs MM/MIS | Intruder bound $O(N_D^4)$ (max-weight IS on circular-arc graph); MM $O(N_A^{2.5})$; MIS super-polynomial (incomplete ≥ N_A = 30); LGR tracks ~$N_A^5$ | MATLAB, Core i7-7820HQ, 16 GB (p. 9) |
| P021 | Iterative two-step convex program (Algorithm 1) | Analytical Step-1 projection (rhombus flags); no timing recorded | not recorded |
| P027 | IBR + distributed ADMM, receding horizon | iterations capped (Remark 1); no timing | simulation → motion-capture validation (per archive) |
| P028 | RESR + OIS feedback | closed-form boundary; no timing recorded | not recorded |
| P033 | Weighted bipartite matching + online rematching | not recorded in archive | simulation (3-D scenarios) |
| P045 | GRAPE + D-Mutex | $O(d_G n_a^2)$ time steps; $O(n_t)$/iteration; 100-run MC, C₁ ≈ 5×10⁻⁴ | unreported (Matlab/Python) |
| P048 | Stacked capture-point program (P) + SOSC check | nonconvex for m ≥ 2; solved per state | not recorded |
| P050 | Per-step QCQP (eq. (36)) | 12-D state, real-time by design ("far out of reach for real-time HJI") | not recorded |
| P053 | Isochron tangency root-finding | Algorithm 1 via MATLAB `vpasolve`; no timing | MATLAB (implied) |
| P054 | Distributed Hungarian + binary search | $O(N^3 \log\frac{\bar T - \underline T}{\Delta})$ rounds (Remark 5) | simulation, 8-vs-10 |
| P059 | LLM planning + analytic corrections | two-chain LLM inference; no timing recorded | 6-AAV motion-capture hardware |
| P060 | Oval invariance strategy + NGC stack | closed loop; no timing recorded | 3 physical USVs, lake trials |
| P061 | Bracketed isochrone root-finding (Algorithm 1) | ≥1, ≤3 roots (Theorem 1) | MATLAB 2023a |
| P066 | Area-gradient pursuit (Leibniz rule) | level-set gradients, no closed-form area; no timing | not recorded |
| P069 | Isochrone-intersection construction (analytic) | no simulations at all | — |
| P072 | MA-POCA CTDE, Unity3D | curriculum + adversarial co-evolution; no timing | Unity3D physics engine |
| P073 | 3D barrier pieces (analytic) | Algorithm 1 for active-pursuer classification | — |
| P078 | Minimax Q-learning + per-stage LPs | per-stage LP: M-1 (2×4) ≈ 0.03–0.07 s flat vs M-2 (N×(N+1)) ≈ 0.23 s at N≈45–60; training 2000 episodes | MATLAB + cvx 1.21, 8 GB, 3.20 GHz |
| P084 | DMK-WTA network + reassignment | 6N_e + 15 flops/agent/iteration = O(N_e); benchmark vs GA/KM/DPSO/DQN over N_e ∈ {2..40} | Webots E-puck; Gazebo Aliengo; Crazyflie 2.1 + OptiTrack hardware |
| P085 | Cooperative value iteration (cVI) | convergence proved (Thm 1); no timing | not recorded |
| P096 | CBF-QP filter + guidance-point mapping | one QP per vehicle per instant; no timing | simulation (marine scenarios) |
| P097 | Apollonius-partition QMIX (Algs. 1–4) | no complexity analysis; 20 000 episodes; convergence ≈ episode 1000 | APES (authors' platform); no hardware |
| P100 | Barrier construction + 0–1 IP | 31 barriers ≈ 0.984 s; IP ≈ 0.025 s (Case 1); 0.023 s / 0.012 s (Case 2) | MATLAB R2016b, i7-8550U, 16 GB |
| P103 | Sequential Matching (1/3-approx) inside MBMC | NP-hard (Thm 4.1), APX-complete; **no runtime numbers** | MATLAB R2017b, i7-8550U, 16 GB |
| P106 | Hierarchical receding-horizon allocation | monotone defeat-count guarantee; no timing | not recorded |
| P108 | PSO + damped-Newton TPBVP | total ≈ 24.4–24.8 s (PSO-dominated); Newton 7 iters ≈ 0.10 s; 1 failed case | MATLAB, 2.7 GHz, 8 GB, Win 10 |
| P111 | HMATD3 + adaptive curriculum | ≈ 10 h training | NVIDIA RTX 1060 |
| P113 | Area-gradient pursuit / modified FMM | FMM grid-based; HJI baseline 1v1 only "due to complexity" | not recorded |
| P017 | MAPPO + GT early termination | 1.2–1.8M frames, 20 envs, 3 seeds; $T_p$ savings heuristic | BenchMARL + VMAS |

Generic scaling facts worth quoting: HJI level-set grids suffer the curse of dimensionality (P103 Remark 3.2: 12-state subgame ≈ $10^{12}$ points at 10 pts/dim; P083 p. 481 look-up-table-per-ratio critique); closed-form barriers + matching is the library's answer (P100/P103); distributed networks trade optimality for O(N_e) per-agent compute (P084) or communication rounds (P054).

## 3. LaTeX environment notes (observed in the library)

- **No archive records `algpseudocode` or `algorithm2e` usage** in any source PDF; the term "algorithmic" appears in P002, P007, P009, P010, P014, P027, P040, P048, P099, P111, P115 but always as prose ("algorithmic core/treatment/…"), **not** as a recorded LaTeX environment of the source. Where the archives describe algorithm floats (e.g., P084 "Algorithm 1 (p. 5992)", P100 "Algorithms 1–2", P103 "Algorithm 1", P045 "Algorithm 1/Algorithm 2 (D-Mutex)", P108 "Algorithm 1", P097 "Algorithms 1–4", P111), they are numbered floats of the `algorithm`-environment family; line-numbered `algorithmic`-style listings are the IEEE Trans default.
- **Practical convention** (from the archives' description practices + the skill template): use `\usepackage{algorithm}` + `\usepackage{algorithmic}` (or `algpseudocode` if the target journal's template ships it — do not mix); caption as "Algorithm N: <verb phrase>"; `\Require/\Ensure` for inputs/outputs; per-step `\Comment{}` naming the lemma/theorem/equation that justifies the step (P100's Algorithm 1 steps are half-plane intersections justified by eq. (47); P017's Algorithm 1 steps are Apollonius centers/radii from eqs. (15a)–(15b) — this comment discipline is the library's norm); state complexity **in text after the float**, not inside it (P084's 6N_e+15 flops and P054's Remark 5 are both textual).
- **Templates**: `templates/algorithm.tex` is the canonical float skeleton (distributed capture assignment with dominance-boundary comments + complexity-note template). Pair with `references/problem_formulation.md` (assumption numbering A1–A4 style of P104) and `references/latex_notation.md` (symbol contract) so that algorithm inputs use the same symbols as the formulation section.
- **Reproducibility norms to emulate/flag** (from archive §6 records): print hyperparameters in a table (P078's table is the good example; P097's all-symbolic Algorithm 4 and P017's unreported MAPPO hyperparameters are the flagged bad cases); report seeds/variance when training (P017: 3 seeds, no tests — flagged); report per-step solver timing when claiming real-time capability (P100's 0.025 s IP; P050's per-step QCQP claim without timing is flagged); state platform + CPU/GPU explicitly (P084/P100/P103/P108 all do).

## 4. Proof-gap ledger for algorithmic claims (do not upgrade these without checking the source)

- P084: k-WTA network convergence under switching topology — by citation only; ≥k constraint after reassignment unproven; printed sign inconsistency in the repulsion forces (archive §5.2, §5.4).
- P054: Lemmas 1–2 unproven; δ_i synchronization unanalyzed; dynamic variant no guarantee (archive §7).
- P045: Lemma 1 iteration-count informality (archive §5.2).
- P097: CSCT monotonicity assumes line-of-sight learned play; area-threshold termination never linked to CSCT; potential-game proof freezes the neighbor set (archive §5.3–5.4, §7).
- P078: no convergence theorem; LP dimension typo after eq. (6); while-condition "or"/"and" typo (archive §5.3, §5.8).
- P108: Theorem 1 converse direction asserted; PSO/Newton no global guarantee; failed-case analysis is a conjecture (archive §5.2, §5.6).
- P111: Hamilton regularization heuristic; impulse correction no feasibility check; LQ baseline gain form non-standard (archive §5.9–5.10).
- P096: QP feasibility unanalyzed; filtered-signal optimality claimed not shown; Γ = 0 degeneracy unhandled (archive §5.2–5.4).
- P095: dynamics never written explicitly; TSR typo $r_0 + \rho_I$ for $r_0 + \rho_T$ (archive §5).
- P107: indirect-point formulas not cross-checkable as printed (archive Def. 1).
- P103: contribution-list HJI-differentiability claim "not substantiated in the paper body" (archive contribution 2).
- P015: equilibrium sandwich holds only for the class of initial configurations treated in the underlying RA-L paper (P083 Item 12).
