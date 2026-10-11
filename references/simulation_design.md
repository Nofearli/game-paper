# Simulation Design Patterns in the Library

Cross-paper synthesis of Section 6 (Simulation and Experiments) of the 117-paper archive. Every claim cites the per-paper archive (PXXX, with printed page when the archive records it). Nothing here is invented: values the archives mark UNREPORTED are reported as UNREPORTED. Use this file to (a) pick a validation design that reviewers of this literature already accept, and (b) avoid the failure modes the library itself documents.

---

## 1. The theory-claim → experiment-design mapping

The library validates eight recurring claim types. For each: who does it, how, and what counts as good evidence.

### V1. Barrier / winning-region verification (outcome matches predicted region membership)

The dominant pattern in the geometric thread: simulate closed-loop play from states placed inside each predicted region and check that the winner is the one the barrier predicts.

- P011 (pp. 19–22, Figs. 15–19): four hand-placed cases — attacker in ADR vs. DDR, three barrier regimes — each validated by one rollout; success additionally checked by trajectory-length inequalities (bypassing path length 3.9179 < v_A·t_A = 4; Fig. 18 shows the entry-angle threshold θ1 separating winning from losing penetrations). Evidence = region-membership-consistent outcome plus a quantitative path-length margin.
- P012 (Figs. 10–11, p. 206–207): 5v5 with α = 0.5; the DDR attacker is captured in Ω_P while the ADR attacker reaches 𝒯, in both the Δt ≤ 0 and Δt > 0 regimes. Qualitative, no metrics.
- P050 (Fig. 4, p. 6363): three scenarios from one shared initial state — optimal/optimal (S1), nonoptimal attacker (S2), nonoptimal defenders using pure pursuit (S3). Capture in S1/S2; the state enters 𝒲_A at t = 2.73 in S3. This "same IC, deviate one side" design is the cleanest saddle-point demonstration in the library.
- P025 (Fig. 6, pp. 6–7): three setups — both optimal, only defender optimal, only intruder optimal — validating the Nash sandwich p(Ω*,Γ) ≤ p(Ω*,Γ*) ≤ p(Ω,Γ*) via flat / non-increasing / non-decreasing payoff curves.
- P053 (Table II, pp. 12–13): the same Nash-sandwich design with capture times as payoff: 3.553 ≤ 3.628 ≤ +∞ (pure-pursuit pursuer never captures). Good evidence because the middle number is the theory's own prediction and the two deviations are punished in opposite directions.
- P058 (Sims 1–4 + 4b, pp. 9–10): on/off-boundary outcomes plus a computed evader-winning-region map (Fig. 6(e) vs. 6(f)) showing the region expanding when capture radius r shrinks 3 → 1 — a parameter-sweep variant of region verification.
- P033 (Table I, p. 2095): five 3-D interception points; the z-ordering I*(1P) < I(2P individual) < I*(2P) < I(3P individual) < I*(3P) is offered as evidence of the saddle point and of dominance-region compression with team size.
- P021 (Fig. 7–8, p. 12): self-validation of value geometry — nested convex sublevel sets S_0 ⊂ S_1.55 ⊂ S_2.5, KKT tangency at y_m, and value drift 1.55 → 1.67 / 2.28 → 2.61 under non-equilibrium attacker play.
- P019 (Figs. 6–12): equilibrium trajectories constructed around switch envelopes; three-segment structure (approach → singular arc → transversal exit) plus monotonicity of J1, J2. Sign checks of f, f_λ, f̄_λ plotted rather than tabulated.
- Counterexample of the pattern: P073 has NO simulation at all — the "complete, closed-form barrier" is supported by construction and schematic figures only (Sec. 6: "no Monte Carlo, no trajectory rollouts"). The archive flags this as the paper's largest evidentiary gap; do not imitate.

Good evidence = (i) at least one run per side of every barrier branch, (ii) initial states explicitly stated, (iii) outcome certified by a printed quantity (capture time, path length, payoff), not by eyeballing, (iv) boundary cases addressed or explicitly excluded (P064, P067 exclude evader-on-barrier starts due to control accuracy — an honest exclusion worth copying in hardware papers).

### V2. Typical on/off-boundary trajectories and feedback-robustness runs

- P058 Sim 2: evader plays a non-optimal curve to the flag, then re-optimizes; capture still guaranteed, and only one of the two matched pursuers ends up contributing — demonstrates the state-feedback (not open-loop) nature of the strategy.
- P026 (Figs. 8–13, pp. 372–374): six case studies pairing (a) trajectories with the barrier overlaid and (b) attacker–target/attacker–defender separation vs. time with the capture radius dashed; includes an explicit boundary loss (Fig. 12: "the policy failed on a boundary game due to a suboptimal pursuit path") and a near-head-on loss (Fig. 13). Reporting failures with mechanism explanations is a library norm worth copying.
- P092 (Scenarios A/B/C, Table I): one scenario per winning-region branch (B1 no observation / B2 limited / B3 maximum), each with full state tables at phase-switch instants; the archive's independent re-simulation of Table II reproduced t2 = 6.2862 and t_obs = 7.4276 exactly — the gold standard of reproducibility from printed numbers.

### V3. Parameter sweeps with theoretical transition points

- P008 (Figs. 8–12, pp. 1451–1452): the model for regime diagrams — competitive-ratio frontiers of five algorithms plotted in (v, M) and (v, ρ) planes against the Theorem-5 impossibility curve (constant v = 1) and the Lemma-4 stationary boundary; piecewise-constant SNP curves change slope exactly at analytically predicted M- and ρ-thresholds (e.g., Dec-CaC beats Dec-SNP for ρ > 0.76 at r = 0.02 but only ρ > 0.38 at r = 0.1). All curves are analytic bounds — "experiments" are numerical visualization of theorems.
- P058 4b: winning-region area vs. capture radius (r = 3 vs. r = 1).
- P027 (Sec. 5.1.2, Fig. 4–5, p. 10): 500 Monte-Carlo runs, 100 per noise level σ_θ ∈ {0.1, …, 0.5}; the subjective-game trajectory gap ‖y_E1* − y_E2*‖ grows monotonically with σ_θ and capture percentage decays from ≈100% to ≈80% — noise-level → performance map used as an engineering design tool ("allowing the measurement device with σ_θ = 0.2 is a reasonable choice", p. 10).
- P028 (Fig. 6, pp. 18612–18613): three noise levels (σ = 0.01/0.03/0.05 × nominal) each with one rollout; the strategy escalates OIS → EC → PS as uncertainty grows. Honest flip side recorded by the archive: at moderate/high noise the evader still wins — the method buys interception distance and minimal resources, not victory.
- P029 (Fig. 5, pp. 16564–16565): belief-convergence vs. Bayesian sample count M ∈ [2, 20], 50 runs per M; win fraction ≈ 0.70 → ≈ 0.95 (read from figure; exact numbers not printed).
- P062: single run exercising the α ≥ α_c branch (α = 1.6 ≥ α_c ≈ 1.365); the harder α < α_c branch is never demonstrated — a coverage gap the archive flags.
- P114 (Figs. 3–5, 9): dense outcome maps over parameter grids (turn radii r_p, r_e; accelerations a_p, a_e; initial distance/heading; alert distance ε1; retargeting parameters Δt̄, pt) — ecology-style heat maps of capture probability with design prescriptions extracted.

### V4. Baseline comparison

Conventions the library accepts: identical initial conditions across methods; explicit baseline provenance; printed tables, not just curves.

- P014 (Table II, p. 8472): the library's best multi-baseline study — Ours vs. PE [MADDPG pursuit] vs. SNH [StringNet Herding] vs. DGT [GAMBIT coordination], each against three attacker policies (PF, MADDPG, human-operated), 20 independent runs per cell, identical initial configurations, metrics MTD/MGT/SR. SR = 0 for PE (objective mismatch: it captures instead of herding) — the archive credits the authors for partially acknowledging that the MTD/MGT gaps partly reflect objective mismatch.
- P089 (Tables II–III, pp. 1002): wall-clock strategy-computation time vs. reproduced 1v1 benchmarks [27], [33] and a 12D-6A assignment baseline [47]: 0.318–0.327 s for 8v6→12v6 vs. 0.375 s for [47]. Caveat recorded by the archive: cross-hardware (2.60 GHz/8 GB vs. 3.60 GHz/32 GB) and cross-implementation comparison.
- P026 (Table 2, p. 374): win-coverage decomposition against the classical point-capture guidance law — the baseline wins 100% inside R_c but 0% outside; the learned policy adds 97.29%/86.95% (train/test) wins in R_e. Decomposing wins by barrier region is more informative than a single aggregate rate.
- P072 (Tables 7–8, Figs. 19–22): APF-evader (9 scenarios) and APF-pursuit baselines (3 trajectories + 50 tests), plus MA-PPO/MA-POCA-no-CL training curves; final co-evolution result a 5:4 pursuer-evader split presented as balance evidence.
- P078 (Tables 2–3, p. 8): three matrix-game variants (learned M-1 vs. non-learning M-2/M-3) over ≈10^3 episodes each at two evader speeds; the archive notes M-1's advantage is survival/delay (≈9.6% inconclusive games) not raw target-reaching — read outcome decompositions, not headline percentages.
- P046 (Fig. 8): comparison against a safety-agnostic game baseline [41] whose trajectories enter unsafe zones while the proposed ones do not — single-scenario, visual only.
- P107 (Fig. 9, p. 13): four sweeps (distance/quantity/velocity/yaw-ratio), seven sub-experiments each, 200 runs per cell = 11,200 simulations vs. a DWA baseline; success-rate bars + average-time lines. The archive flags the baseline as a non-game-theoretic local planner.
- P003 (Fig. 2 vs. Fig. 4): cautionary tale — hybrid 94% vs. classical 24% capture, but the hybrid pursuer runs at 10 m/s vs. the classical 4 m/s with a stale 2.5 m/s speed assumption (speed panel printed in their own figure). No equal-speed comparison exists.
- Negative examples: P085 (no baselines, no metrics, iteration counts only), P050/P025/P056 (deviation-only self-comparisons), P013 (no baseline; the CBF layer's benefit "is not isolated by an ablation").

### V5. Ablation

Rare and thin in this library. P079 (Figs. 9–10, p. 10) is the model: remove the GAN (HPN-ImpLSTM) and the ImpLSTM (HPN-GAN) separately; boxplots of task-completion rate from 100 training sessions per method across 3 tasks, plus reward curves from 4 sessions. P072 ablates curriculum (MA-POCA with/without CL) and imitation (PPO vs. PPO+BC+GAIL, Fig. 14–16). Everywhere else ablation-type claims rest on narrative (P003: no ω-sensitivity, no curriculum-off ablation; P097: no vanilla-QMIX or reward ablation). If your paper claims component synergy, run the P079 pattern.

### V6. Computational cost

- Strategy computation: P089 Table II (0.011–0.063 s for 1v1–2v1; 0.318–0.327 s for 8v6–12v6); P091 (nine barriers ≈ 0.294 s; sixteen barriers ≈ 0.412 s, dominated by sampling barrier points); P014 (three barriers, 300 points each, ≈ 0.0986 s total); P078 Fig. 9 (per-stage LP time vs. N up to 60: 2×4 matrix flat ≈ 0.03–0.07 s, N×(N+1) grows to ≈ 0.23 s); P015 Fig. 9 (log-scale time vs. N_A with an N_A^5 trend line for LGR-Removal; MIS omitted beyond N_A = 25 because searches did not complete).
- Value-function precomputation: P040 (p. 1021): ≈ 1 h per 4-D set at 45 points/dimension, as little as 4 min at 25 points/dimension, on a 2.66 GHz Core i7 with 8 GB RAM, Level-Set Toolbox.
- Inference-time benchmarking: P072 (Fig. 23): 500 Monte-Carlo tests × 1000 consecutive ONNX inferences; pursuit ≈ 0.10–0.13 s CPU per action, escape ≈ 0.14–0.23 s — a repeatable protocol for real-time claims.
- Training cost: P079 Table V (per-iteration time, total training hours, GPU memory for five methods); P026 (5 h total on GTX 1050 Ti, p. 371).
- P089 Table III reports average/min/max assignment time (0.932/0.295/1.780 s) — but the archive caught the text's "21%" max reduction contradicting the printed 2.1%: always recompute percentages from your own tables.

### V7. Robustness to noise / partial information / disturbance

- P084 (Fig. 5, p. 5995): 0%, 20%, 40% noise on target-position sensing; encirclement still achieved, convergence time grows with noise.
- P027: σ_θ sweep (above) plus AGV tracking-error quantification (Table 6, p. 13: average ≈ 0.02 m, max ≈ 0.05 m vs. the linear double-integrator model).
- P028: noise-level escalation (V3) plus hardware Scenario 4 repeating Scenario 2's geometry at 5× noise.
- P046 (Fig. 9): safeguarding-gain study c_j = 2.5 vs. 5.5 with zoom inset — larger gain pushes trajectories farther from obstacle boundaries at higher control effort; Fig. 10 shows the failure case where the capture condition fails (demonstrating non-vacuity).
- P046 (Fig. 8) and P096 (Figs. 6–8): constraint-satisfaction evidence — input signals plotted against their printed bounds (saturating early, then inside dashed limits), and minimum distances to static/dynamic obstacles and neighbors kept above CBF thresholds.
- What is essentially never done: robustness to sensor latency, communication dropout, or adversarial belief manipulation (P029's attacker could masquerade at another level — unexamined; P077 lists noisy position information as future work; P008 models no delays/noise at all).

### V8. Monte-Carlo / success-rate reporting

Counts actually used in the library: 100 runs (P013 Fig. 7: 70% capture at N = 10, ≈75% at N = 16; P029 Tables II–III; P003 100 episodes per controller; P027 100 per noise level), 200 (P059 prompt-robustness and cross-LLM tables; P107 per sweep cell), 3000 random initial configurations (P060, classified 1969 DDR + 1131 ADR), 1000 per initial-distance (P015 Fig. 8: 40 defenders vs. 39 intruders, 10,000 runs per distance on the axis 0–0.3), ≈10^5 (P077 Table I: 0.00% captured at N = 1, 26.88% at N = 2, 41.66% at N = 4, remainder inconclusive), 10,000 test configurations (P026: 88.54% coverage), 11,200 total (P107), "about 10^3 episodes" (P078), 1000 rounds per team size (P059, Np = Ne ∈ {5, …, 50}). Seeds and variance across training runs: reported only by P051 (3 repetitions, mean ± error bars) and partially P079/P072; everywhere else a single run or unreported seeds is the norm — an explicit weakness to outdo.

---

## 2. Consolidated parameter-convention table

Sourced from the archives' Section 6 tables. "n.r." = not recorded (UNREPORTED in the archive). Use these as sanity ranges; cite the specific paper when adopting a value.

| Quantity | Values observed (paper) |
|---|---|
| Simulation time step | 0.001 (P090, CRDE) · 0.01 s (P013, P078 Δt, P050 sampling 0.01 s) · 0.04 s (P033) · 0.1 s (P026 Δt, P014 control period, P046 data t_k = 0.1k) · 0.15 s (P027, P029) · 32 ms (P084 Webots) · 0.5 s (P084 Aliengo) · n.r. (P011, P012, P019, P025, P033 integrator, P050, P053, P056, P058, P062, P085, P091, P092, P096, P107) |
| Normalized player speeds | v = 1 defender-normalized (P008); v_P = v_E = 1, ℓ = 0.1, ϵ = 0.001 (P077); v = 1 evader-normalized, u = 1.2–1.3 pursuers (P033); unit hemisphere, ν = 0.8 intruder (P025) |
| Simulated speeds (SI) | UAV 30 m/s vs. 22 m/s pursuers (P013); USV 10/6 m/s Unity (P072); ASV ≤ 1 m/s (P096); USV field 0.8–1.1 m/s (P060); AGV 0.15–0.25 m/s (P027, P028 0.25/0.2 m/s); quadrotor sim 0.2–0.6 m/s (P064, P067); AAV ≤ 5 m/s flown 0.3–0.5 m/s (P059); TurtleBot < 0.15 m/s (P079); pursuit 6 vs. evader 3 (P097, sim units); isochron u_pm/v_em = 5/2.5, 8/2.2, 6/variable (P053) |
| Speed ratios α (attacker/evader over defender/pursuer) | 0.5 (P012, P011 Case 1) · 0.6–0.8 (P011 Cases 3–4; P092 A/B/C) · 0.6 (P056) · 2/3, 5/6 (P021) · 0.55 target/attacker (P026) · 0.7 (P003 curriculum) · 1.1–1.5 pursuer/evader (P058 Sims; P089 V_d1 = 1.6, V_a = 1) · 1.2–1.3 (P033) · 3 (P064, P067) · heterogeneous 0.52–1.0 (P091 Case 1) · pursuer-faster premise γ_k < 1 (P028) |
| Capture radii (normalized) | 0.01 (P008 Fig. 8; P078 ℓ = ε = 0.01) · 0.05–0.13 (P008 Figs. 9–12) · 0.1 (P077) · 0.5 grid unit (P040) · 0.2 (P026) |
| Capture radii (SI) | 0.25 m (P028 hardware) · 0.3–0.4 m (P084 E-puck d_c = 0.2, d_a = 0.25; Crazyflie d_c = 0.4, d_a = 0.8) · 0.3 m escorts (P014) · 0.5 m (P062) · 0.6–0.7 m (P058 hardware) · 0.15 m (P079) · 2 m (P013 r_c = 2 m; P107 r = 1 m) · 4 m (P096 μ = 4) · 6 m (P060 field) · 10 m (P060 sim ρ_D = 10) · 0.8 interception distance (P029) |
| Sensing radii | 1 m and 2 m (P067 Cases 1–2; P064 r1 = 2, r2 = 1) · 5 m (P062 r_s) · 3 m (P084 Aliengo) · 0.4 m detection (P084 E-puck) · 1 m detection Crazyflie (P084) · 35 m radar, 50 m comms (P003) · 2 m comms E-puck (P084) · 0.25–0.35 m (P079) · 9.5/5/8/7.5 visibility (P090) |
| Monte-Carlo counts | 100 per condition (P003, P013, P027, P029) · 200 (P059, P107) · ~10^3 (P078) · 1000 per team size (P059) · 1000 per cell (P015) · 3000 (P060) · 10^4 (P026 test grid) · 11,200 (P107) · ~10^5 (P077) · 20 repeats (P084 Fig. 9) · 3 (P051) · none/single (P025, P050, P056, P062, P033, P073, P085, P091, P092, P096) |
| Arena / domain sizes | unit square/hemisphere (P078 grid, P025 hemisphere r = 1) · [0,10]^2 eval (P078) · 5×5 m (P084 E-puck) · 24×24 m (P084 Aliengo) · 10×10 m (P014 sim) · 6×8 m (P014 hardware) · 12×5 m (P064, P067) · 40×40 sim units (P059) · radius 10/50 (P003) · [−5,5] rect domain (P040) · [0,40]×[0,25] (P089 Case 1) · [0,70]×[0,30] inferred (P089 Case 2) · 40×30 (P091) · ±400 m (P072) · 50–500 m radius around target (P060 MC) · 50×50 m and ≈200×180 m (P040 field) · 4.0×2.5×0.5 m (P079 Gazebo) · unbounded domains (P001, P011, P012, P053) |
| Control update / replanning | H = 20 horizon, T = 0.15 (P027, P029) · 50 Hz GCS, 100 Hz mocap (P059) · 10 Hz commands (P060) · 50 Hz server (P014) · < 100 ms decision latency (P079) · Δt = 0.04 s control update (P033) |

---

## 3. Metrics dictionary (definitions as actually used)

- **Capture/success rate** — fraction of randomized trials ending in capture. Variants: capture rate over 100 random ICs (P013); percent captured / target-reached / inconclusive (P077 — the inconclusive column is a deliberate third outcome: at N = 1, 2.53% of runs neither capture nor reach); win:lose counts out of 100 MC runs (P029); CER = captured-evader rate after deleting unreasonable pairs and physical conflicts (P059); defense success rate and outcome decomposition pursuer-win/evader-win/timeout (P003); penetration success rate (P107); task-completion rate (P079).
- **Capture time / interception time** — wall-clock or step count to capture. Used as payoff in the Nash-sandwich check (P053 Table II); median + IQR boxplots (P003, P079); per-role capture step counts (P097: 17 vs. 50 steps evader-side, 51 vs. 49 pursuer-side); capture instants t1, t2 and total (P090: t_g = 0.224 < t_n = 0.259 < t_s = 0.303 as the quantitative headline).
- **Miss / margin distances** — P060's DDR/ADR metrics: d_A𝒯(t_f) (attacker-to-target distance at termination) and min_i{d_DiA(t_f) − ρ_Di} (defender-to-attacker margin beyond capture radius), averaged over 3000 MC runs and shown as log-scale histograms of per-run pairwise differences (Figs. 11–12); P062's dual-axis min pursuer–evader distance and evader–target distance vs. time; P026's minimum attacker–defender distance mapped over the initial-condition plane (Figs. 14–15); P114's minimum distance Δd_min surfaces.
- **Payoff gap / value consistency** — V(θ(t)) trajectories under equilibrium vs. deviated play (P050 Fig. 5: flat / increasing / decreasing to 0); game value W* and its drift under non-equilibrium play (P021: 1.55 → 1.67); certified score bounds Q_LG vs. Q_MM − Q_LG gap ≈ 15 against Q_LG ≈ 20 ± 7 at detection distance 0.1 (P015 Fig. 8) — bounds compared, not simulated scores.
- **Competitive ratio** — captures by an online algorithm over the offline optimum (P005, P006, P008, P009); plotted as frontier curves vs. parameters with impossibility boundaries.
- **Runtime / computation time** — per-strategy computation (P089), per-barrier-batch (P091, P014), per-LP-solve (P078), per-iteration and total-training (P079 Table V), per-inference over 500×1000 ONNX runs (P072), assignment time min/avg/max (P089 Table III), time-to-generate-matching excluding API latency (P059 — TC excludes API call latency, so deployment latency is understated; the archive flags this).
- **Tracking error (hardware)** — average and maximum planned-vs-actual trajectory error per agent (P027 Table 6: ae ≈ 0.018–0.027 m, me ≈ 0.043–0.067 m).
- **Prediction metrics** — ADE/FDE in meters over ETH/UCY with 3.2 s observation (P079 Table III).
- **Allocation quality** — cost rate C_r = (C − C_base)/C_base with KM as baseline (P084 Fig. 9); total interception cost and captured count (P033: 20.08 vs. 22.809 open-loop, 7 vs. 6 evaders closed-loop); assignment time (P089); UR/PCR/PUR rates (P059: unreasonable-pair rate and physical-conflict rate driven to 0.00 by the analytic revision layer).
- **Training curves** — cumulative/episode reward, episode length, loss decomposition, entropy, with ±1σ shading over 20 runs (P079 Fig. 6) or single-run variance bands (P072 Figs. 12–16).

---

## 4. Pitfalls observed in the library (do not reproduce)

1. **Kinematic confounds in headline comparisons.** P003's 94% vs. 24% runs a 2.5× faster hybrid pursuer against a classical controller with a stale speed assumption; no equal-speed control. P014's PE baseline optimizes a different objective (capture vs. herding) — SR = 0 partly by construction. P107 compares only against DWA, "a collision-avoidance planner, not a game-theoretic penetrator". P060's baselines (PN guidance, direct rush, capture-radius-blind laws) are known-weak; the archive notes no comparison against the capture-radius-aware works the paper itself criticizes.
2. **Cross-hardware / cross-implementation timing claims.** P089 Tables II–III compare its 2.60 GHz/8 GB runs against references' 3.60 GHz/32 GB runs; direction favorable but not controlled. Also the printed "21%" vs. actual 2.1% discrepancy (P089 obs. 6).
3. **Single-run claims for equilibrium/barrier papers.** P025 (one initial condition, no integration details), P056 (illustrative trajectories only), P050 (one 3-D scenario; solver and target data UNREPORTED), P062 (single 3-vs-1 toy), P033 (single scenario per claim, no runtime despite complexity claims), P091 (no closed-loop trajectories at all — static winning-region plots), P019, P073 (nothing). Reviewers of T1 venues increasingly expect at least a Monte-Carlo over initial conditions, as P077's 10^5-run Table I and P060's 3000-run study provide.
4. **Unreported seeds, platforms, and solver settings.** P085 (platform, ε, t_f, excitation amplitudes all UNREPORTED), P097 (all RL hyperparameters symbolic only), P029 (platform/solver UNREPORTED), P012 (everything but α), P050/P053/P058/P062/P085/P091/P092 (integrator/step UNREPORTED), P027 (case-1 software UNREPORTED), P064/P067 (trial counts, control rates UNREPORTED). P078's stopping-condition typo ("or" for "and") is a reproducibility hazard the archive singles out.
5. **Figure-only statistics without numeric tables or dispersion.** P084's entire quantitative comparison is Fig. 9 ("no numerical table printed — UNREPORTED exact C_r values") despite 20 repeats and a stochastic algorithm; P107 reports no confidence intervals; P029's Fig. 5 numbers are readable only approximately; P003's headline numbers come from one training run each with no seeds.
6. **Metric definition mismatches between text and tables.** P078's rows not summing to 100% (the ≈9.6% inconclusive mass is the real finding); P079's internal inconsistencies (success-rate typo 0.0889 vs. figure 0.8889; IQR stated differently on two pages; text/table value swaps); P089's 21% vs. 2.1%; P026's "1e+3" test cases vs. the 10,000 implied by 2370/10,000; P003's two different IQR statements (pp. 6 vs. 7). Always regenerate every statistic from the tables.
7. **Weak or unproven adversarial models.** P013's "optimal invasion and evasion strategy" is a heuristic QCQP-CBF evader, so the 70–75% capture rates are conditional on that parametrization; P026's attacker is a best response to one fixed defender script; P029 assumes the attacker's level is fixed within a game and that both sides know each other's cost functions; P079's evader side never jointly optimized (P089 obs. 11); P015 compares certified bounds rather than closed-loop play against a non-equilibrium intruder.
8. **Reward-hacking and overtraining artifacts reported honestly** (copy the transparency, avoid the cause): P026's game-prolongation anomaly at (6.0, 0.0) and shrinking coverage with longer training; P029's belief non-convergence in ≈1 of 5 runs; P078's Δt/ℓ-ratio sensitivity ("ℓ/(v_e Δt) is the true dimensionless training parameter").
9. **Proportion-of-effort mismatches.** P011 Case 2's printed initial state sits (barely) inside its own detection set, contradicting the paper's Theorem 1 prediction — a reminder to numerically re-verify each hand-placed case; P092's Scenario-B heading erratum (131.4096° printed where 126.87° generates the tabulated trajectory — found by the archive's re-simulation) shows why state tables must be regenerable.
10. **Barrier-boundary quantifier slips.** P040's honest disclosure that the zero sublevel set "sometimes slightly underapproximated the stop capture set" near F_D ∩ F, with the ±ϵ level-set fix — adopt this prescription in any level-set winning-region paper.
