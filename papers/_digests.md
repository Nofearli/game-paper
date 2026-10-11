### P001 — Capture Pursuit Games on Unbounded Domains
[BIBLIO]
- **ID / source file**: P001 / `D:\System\zhuomian\game-paper\10.4171-lem-55-1-5.pdf`
- **Total pages**: 23 PDF pages; printed pagination pp. 103–125 (journal t. 55, 2009).
- **Title**: Capture Pursuit Games on Unbounded Domains (printed in capitals on p. 103).
- **Authors**: S. Alexander, R. Bishop (Department of Mathematics, University of Illinois, Urbana, IL 61801, USA; e-mail sba@math.uiuc.edu, bishop@math.uiuc.edu) and R. Ghrist (Departments of Mathematics and Electrical/Systems Engineering, University of Pennsylvania, Philadelphia, PA 19104, USA; e-mail ghrist@math.upenn.edu). Initials only as printed; full first names are not given in the paper.
- **Year**: 2009. Header (exact, p. 103): *L'Enseignement Mathématique (2) 55 (2009), 103–125*; running footer "L'Enseignement Mathématique, t. 55 (2009)". Received ("Reçu le") 3 January 2008; "Achevé de composer le 5 juin 2009". Funding footnote: DARPA SToMP # HR0011-07-1-0002 and NSF MSPA-MCS # 0528086.
- **DOI**: not printed anywhere in the PDF. The filename is the DOI slug of the EMS-hosted version, i.e. 10.4171/lem/55-1-5; treat a
[CONTRIBUTIONS]
1. **Theory — a dimension- and pursuit-count-independent feasibility criterion.** The *Boundedness Condition* (Def. 1, eq. (1), p. 108): the intersection $\big(\bigcap_{j=1}^N \mathbf{H}_j\big) \cap \mathcal{D}$ is bounded, where $\mathbf{H}_j$ is the closed half-space containing $E$ whose boundary hyperplane passes through $P_j$ orthogonal to $EP_j$. Four equivalent spherical formulations (Theorem 9) and necessity for *any* winning strategy (Proposition 10).
2. **Theory — correction of the prior art.** Identification (Figure 3, §4.1, pp. 111–112) of the exact failure mode of the Radius algorithm of [33, 17] on cones with angle $< \pi/2$: the required next position $P^{t+1}_j$ can lie outside $\mathcal{D}$; the "discard pursuers whose sightline leaves $\mathcal{R}$" preprocessing can destr
[RESULTS-LIST]
- **Definition 1 (Boundedness Condition, p. 108, eq. (1))**: with $\mathbf{H}_j$ the closed half-space containing $E$ bounded by the hyperplane through $P_j$ orthogonal to $EP_j$,
- **Definition 2 (spherical convexity, p. 109)**: $\mathcal{A} \subset S^{n-1}$ is convex iff the cone over it, $C(\mathcal{A}) = \{v \in \mathbf{E}^n : v = \lambda x,\ x \in \mathcal{A},\ \lambda \in [0,\infty)\}$, is a convex subset of $\mathbf{E}^n$. Remark 3: great $k$-spheres (hence antipodal pairs) are convex.
- **Definition 4 (normals set, p. 109)**: $\mathcal{N} \subset S^{n-1}$ = all outer unit normals to support hyperplanes meeting $\mathcal{D}$ but not its interior. Warning preserved from [38]: $\mathcal{N}$ itself need not be convex, though $\overline{\mathcal{N}}$ is.
- **Definition 5 (duality, p. 109)**: the dual $\mathcal{A}^0$ of convex $\mathcal{A} \subset S^{n-1}$ is the set of unit vectors ma
[CITATION]
**Role**: the mathematical-foundations citation for pursuit/capture feasibility on *unbounded* domains. It contributes (i) the recession-set/visibility-sphere formalism that unifies boundary normals, escape directions, and pursuer sightlines; (ii) the sharp (necessary *and* sufficient) Boundedness Condition for equal-speed discrete capture on arbitrary unbounded convex domains (Thms. 9 + 17); (iii) the canonical counterexample showing that naive radius/lifeline-style pursuit fails near non-polyh

### P002 — A Three-Dimensional Pursuit-Evasion Game Based on Fuzzy Actor-Critic Learning Algorithm
[BIBLIO]
- **ID**: P002 | **Source file**: `D:\System\zhuomian\game-paper\2503.08013v1.pdf` | **Total pages**: 10
- **Title**: A Three-Dimensional Pursuit-Evasion Game Based on Fuzzy Actor-Critic Learning Algorithm
- **Authors**: Penglin Hu (single author), Northwestern Polytechnical University, Xi'an, Shaanxi 710129, China (penglinhu@mail.nwpu.edu.cn)
- **Year**: 2025 (arXiv stamp: "arXiv:2503.08013v1 [eess.SY] 11 Mar 2025", printed on p. 1 margin)
- **Venue**: arXiv preprint, class eess.SY; unpublished — no journal/conference name printed anywhere in the PDF; the single-column LNCS-style formatting suggests a conference manuscript. Indexer guess: arXiv. **No DOI printed.**
- **Tier**: T2 (preprint of quality work). Caveat: the theoretical depth is modest — no formal theorem/proof environments, no optimality or convergence analysis; the geometric contribution is an elementary 3D Apollonius-sphere restatement and the learning machinery is the standard FACL of Schwartz's group. Value lies in the explicit 3D formulas and the FACL + artificial-potential-field (APF) reward recipe; borderline for 
[CONTRIBUTIONS]
1. **Geometry (theory, elementary)**: extension of the 2D Apollonius circle to a "generalized AC" in 3D space — an Apollonius sphere with explicit center and radius (eq. (3), p. 5) — and classification of dominant regions by speed ratio $a = v_E/v_P$ ($a<1$: ball around evader is evader-dominant; $a=1$: perpendicular bisector plane; $a>1$: pursuer side), illustrated in Fig. 2 (p. 4).
2. **Strategy geometry (theory, heuristic)**: sine-rule analysis on the pursuer–evader–AC-point triangle giving each agent an "optimal motion space": a pursuit cone of half-angle $\alpha_2^* = \sin^{-1}(v_E/v_P)$ about the line of sight (eqs. (4)–(6), p. 5, Fig. 3).
3. **Algorithm (modeling)**: a Fuzzy Actor-Critic Learning (FACL) scheme — first-order Takagi-Sugeno (TS) fuzzy actor + TS fuzzy critic — with the
[RESULTS-LIST]
- **Dynamics (discrete-time, eq. (1), p. 2)**:
- **Information structure**: agents know each other's location but not the opponent's strategy (p. 2). No velocity observation is used in the control law (only distances and angle differences, eqs. (15)–(16)).
- **Termination/winning (p. 2)**: PEG ends at $t_f$ when $d_{PE}(t_f) \le d_s$ (capture distance $d_s$), or when time exceeds a designated threshold (evader wins by surviving).
- **Proof gap (kinematics convention)**: with $\theta \in [-\pi/4,\pi/4]$ and $v_z = v\cos\theta > 0$ as printed, vertical velocity is strictly positive — agents can never descend or hold altitude, and motion is confined within $\pm 45°$ of the $+z$ axis. If $\theta$ were the elevation from the $x$-$y$ plane, eq. (1) should read $v\cos\theta\cos\alpha$, $v\cos\theta\sin\alpha$, $v\sin\theta$. The simulations corroborate the as-printed behavior: all captures occu
[CITATION]
**Paragraph role**: useful as a 3D-PEG engineering reference at the intersection of geometric dominance reasoning and fuzzy reinforcement learning — citable for (i) the explicit 3D Apollonius-sphere center/radius formulas (eq. (3)) and the tangent-cone heading bound $\alpha_2^* = \sin^{-1}(v_E/v_P)$ (eq. (6)) as a compact statement of 3D dominant-region geometry, and (ii) as an example of APF-shaped reward design (eqs. (17)–(20)) that bakes obstacle avoidance into FACL pursuit learning in clutte

### P003 — Adaptive Interception in Dynamic Domains: Exploration of Hybrid Reinforcement Learning in Pursuit-Evasion Task
[BIBLIO]
- **ID**: P003
- **Source file**: `D:\System\zhuomian\game-paper\Akinmolayan 等 - 2026 - Adaptive Interception in Dynamic Domains Exploration of Hybrid Reinforcement Learning in Pursuit-Ev.pdf` (filename truncated; full title from page 1)
- **Total pages**: 9 PDF pages; printed running pagination 2–10 (printed page = PDF page + 1; every page footer verified)
- **Title**: Adaptive Interception in Dynamic Domains: Exploration of Hybrid Reinforcement Learning in Pursuit-Evasion Tasks
- **Authors**: Matthew Akinmolayan (1), Darsana Josyula (1), David Casbeer (2) — (1) Department of Computer Science, Bowie State University; (2) Aerospace Systems Directorate, Air Force Research Laboratory (AFRL)
- **Year**: 2026
- **Venue (EXACT, from running header p. 1 and copyright block)**: "AAAI Spring Symposium Series (SSS 2026)" (running header) + "Copyright © 2026, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved." (copyright footnote, p. 1). **The indexer guess "AAAI-26" is thereby resolved as the AAAI Spring Symposium Series 2026, NOT the AAAI-26 main 
[CONTRIBUTIONS]
1. **Modeling**: A range-limited circular perimeter-defense environment (single-agent: radius 10, 3 tripwire sensors at 120°; multi-agent: radius 50 m, 2 stations, 4 pursuers with 35 m radar/360° FOV/50 m comms/battery model, 3 RL-trained evader flock) with explicit win/lose/timeout conditions (Sec. 5.6 below; pp. 2–5).
2. **Algorithm (single-agent)**: Hybrid PPO interception — the control input is a convex blend $u_{hybrid} = \omega \hat u_{classic} + (1-\omega)\hat u_{RL}$ (eq. (5), p. 2) with the classical component computed from a relative-kinematics intercept solver (eqs. (1)–(4)), $\omega$ annealed from 1 toward 0 during training; three-phase speed-ratio curriculum (0.7× → 0.9× → 1.1× evader/pursuer speed; p. 2); a shaping reward that includes a classical-bridge term $+0.2\cos(\theta
[RESULTS-LIST]
- **Meaning**: produces a constant-bearing / lead-pursuit path, which the authors contrast with pure pursuit's tail chase; "performs well under straight-line motion assumptions but can fail if the evader is faster or changes direction frequently. In such cases, the computed $t$ may be negative or undefined, indicating infeasibility" (p. 2).
- **Analytic gap (this archive's verification, not the authors')**: eq. (2) is a 2-scalar vector equation in ONE unknown $t$ and in general has no exact solution unless $\vec p_p - \vec p_e \parallel (\vec v_e - \vec v_p)$. Eq. (3) is the least-squares projection of the relative-separation vector onto the relative-velocity direction, i.e., the time of closest approach of the straight-line relative motion, NOT a guaranteed collision time; after heading to $\vec I$, a miss distance generally remains and would need a second correction. The paper never st
[CITATION]
**Paragraph role**: best cited as (a) an example of hybrid classical-guidance + PPO architectures for interception, i.e., "learning to modulate a geometric prior" rather than learning from scratch; (b) a template for alternating adversarial self-play in PE defense with role-encoded adversarial flocks (leader/decoy structures) against station-guarding pursuer teams; (c) a baseline/positioning reference for the claim that pure classical interception fails under speed mismatch and stale target-spee

### P005 — Competitive Perimeter Defense on a Line
[BIBLIO]
- **ID**: P005
- **Source file**: `D:\System\zhuomian\game-paper\Bajaj 等 - 2021 - Competitive Perimeter Defense on a Line.pdf`
- **Total pages**: 6 (proceeding pages 3196–3201)
- **Title**: Competitive Perimeter Defense on a Line
- **Authors**: Shivam Bajaj (Dept. of Electrical and Computer Engineering, Michigan State University; bajajshi@msu.edu), Eric Torng (Dept. of Computer Science and Engineering, Michigan State University), Shaunak D. Bopardikar (Dept. of Electrical and Computer Engineering, Michigan State University)
- **Year**: 2021
- **Venue (EXACT, from header/copyright)**: "2021 American Control Conference (ACC), New Orleans, USA, May 25-28, 2021"; copyright line "978-1-6654-4197-1/$31.00 ©2021 AACC"; footer of p. 1 also prints "2021 American Control Conference (ACC) | 978-1-6654-4197-1/21/$31.00 ©2021 | 10.23919/ACC50511.2021.9483308". Indexer guess (ACC) is **correct**.
- **DOI (printed)**: 10.23919/ACC50511.2021.9483308
- **Funding (printed)**: NSF Award ECCS-2030556
- **Tier**: T2 (top control conference: ACC). No disagreement — the venue is confirmed by the printed he
[CONTRIBUTIONS]
1. **Fundamental limits (impossibility), theory** (Section III): a most-difficult regime $v > \frac{1-\rho}{2\rho}$ in which no algorithm — online *or* offline — is $c$-competitive for any constant $c$ and cannot even capture all intruders (Theorem III.1); a slightly easier regime $v \ge \frac{1-\rho}{1+\rho}$ in which $c(\mathcal{E}) \ge 2$ for every algorithm (Theorem III.2).
2. **Negative result for a natural algorithm, theory**: FCFS is not $c$-competitive for any constant $c$ whenever $\frac{2}{v+1} + \rho > \frac{1-\rho}{v} + \epsilon$ (Lemma 2) — a natural greedy is ruled out even in regimes where other algorithms are competitive.
3. **Three online algorithms with proven ratios, modeling/algorithm** (Section IV): Sweeping (1-competitive for $v \le \frac{1-\rho}{3+\rho}$, Theorem IV.
[RESULTS-LIST]
- **Lemma 1 (Extreme speed algorithms, p. 2)**: Given an arbitrary algorithm $A$ and a non-adaptive input instance $\mathcal{I}$, there exists an extreme-speed algorithm $A': \bar{E}\times\mathcal{F} \to \{-1, 0, 1\}$ (unit speed or stationary) that captures at least as many intruders in $\mathcal{I}$ as $A$. *Assumptions*: non-adaptive inputs (arrival times independent of defender motion). *Proof approach (outline)*: define the **capture profile** of $A$'s execution as the set of pairs $(x_i, k_i)$, $1 \le i \le n$, where $k_i$ is the time of the $i$-th capture and $x_i$ its location; construct $A'$ that reproduces the same profile by moving to the next capture point $x_i$ as fast as possible and, if necessary, **waiting** at $x_i$ until time $k_i$. *Consequence*: all subsequent fundamental limits and algorithm analyses may restrict to extreme-speed (bang-bang) strategies; global statem
[CITATION]
This is the foundational conference paper of the line-environment worst-case perimeter-defense thread (followed by the randomized variant "Randomized Competitive Perimeter Defense on a Line" and the conical-environment extensions already present in this library). Its role in a related-work section is (a) as the citation that **imports competitive analysis into perimeter defense** — providing impossibility thresholds ($v > \frac{1-\rho}{2\rho}$: nothing possible; $v \ge \frac{1-\rho}{1+\rho}$: $c

### P006 — Competitive Perimeter Defense of Conical Environments
[BIBLIO]
- **ID**: P006
- **Source file**: `D:\System\zhuomian\game-paper\Bajaj 等 - 2022 - Competitive Perimeter Defense of Conical Environments.pdf`
- **Total pages**: 8 (proceeding pages 6586–6593)
- **Title**: Competitive Perimeter Defense of Conical Environments
- **Authors**: Shivam Bajaj (Dept. of Electrical and Computer Engineering, Michigan State University; bajajshi@msu.edu), Eric Torng (Dept. of Computer Science and Engineering, Michigan State University), Shaunak D. Bopardikar (Dept. of Electrical and Computer Engineering, Michigan State University), Alexander Von Moll, Isaac Weintraub, Eloy Garcia, David W. Casbeer (Control Science Center, Air Force Research Laboratory)
- **Year**: 2022
- **Venue (EXACT, from header/copyright)**: "2022 IEEE 61st Conference on Decision and Control (CDC), December 6-9, 2022, Cancún, Mexico"; copyright line "978-1-6654-6761-2/22/$31.00 ©2022 IEEE"; p. 1 sidebar also prints "DOI: 10.1109/CDC51059.2022.9993007". Indexer guess (CDC) is **correct**.
- **DOI (printed)**: 10.1109/CDC51059.2022.9993007
- **Funding (printed)**: AFOSR Summer Faculty Fellowshi
[CONTRIBUTIONS]
1. **Theory (impossibility)**: Theorem III.3 (p. 2) — a necessary condition on $(\theta,\rho,r,v)$ under which **no** $c$-competitive online algorithm exists for any finite $c$; in fact no algorithm, online or offline, can capture all intruders.
2. **Theory (lower bound)**: Theorem III.4 (p. 3) — a necessary condition under which $c(\mathcal{P}) \ge 2$ for every algorithm: no online algorithm can capture both intruders of five crafted two-intruder instances $\{\mathcal{I}_1,\dots,\mathcal{I}_5\}$ while an offline algorithm captures both.
3. **Algorithm (open-loop, optimal)**: Angular Sweep (Section IV-A) — the vehicle sweeps a circular arc at radius $x_S$; provably **1-competitive** (captures every intruder, matching the offline optimum) iff $x_S$ lies in a non-empty interval guaranteed by
[RESULTS-LIST]
**Lemma III.1 (static capture-all placement; p. 2).** *For a problem instance $\mathcal{P}(\theta,\rho,r,v)$ with $\theta < \frac{\pi}{4}$, all intruders can be captured if $r \ge \rho\tan(\theta)$ by positioning the vehicle at $\left(\frac{\rho}{\cos(\theta)}, 0\right)$.*
**Lemma III.2 (endpoint crossing time; p. 2).** *The minimum time required by the vehicle to move from a location such that the capture circle contains one end of the perimeter, $(\rho, \theta)$, to a location such that the capture circle contains the opposite end, $(\rho, -\theta)$, is $2(\rho\sin(\theta) - r)$ if $\theta < \frac{\pi}{2}$ and $2(\rho - r)$, otherwise.*
**Theorem III.3 (necessary condition for finite $c(\mathcal{P})$; p. 2).** *For any problem instance $\mathcal{P}(\theta, r, \rho, v)$ with parameters satisfying*
**Theorem III.4 (necessary condition for $c(\mathcal{P}) \ge 2$; p. 3).** *For any problem
[CITATION]
This paper is the **second pillar of the worst-case (competitive-analysis) perimeter-defense thread** archived in this library (after the line-environment P005 = ref [20], before the multivehicle conical extension, Bajaj et al. 2024), and it is the canonical citation for **worst-case guarantees in 2-D sector/conical guard zones with a finite capture radius**. Its role in a related-work section is (a) as the citation establishing that the conical geometry — the natural model for a sensor/weapon c

### P007 — Perimeter Defense Using a Turret with Finite Range and Startup Time
[BIBLIO]
- **ID**: P007
- **Source file**: `Bajaj 等 - 2023 - Perimeter Defense Using a Turret with Finite Range and Startup Time.pdf`
- **Total pages**: 6 (printed pp. 3350–3355 of the ACC 2023 proceedings; PDF page k = printed page 3349+k)
- **Title**: Perimeter Defense Using a Turret with Finite Range and Startup Time
- **Authors** (byline order, p. 3350): Shivam Bajaj (Dept. of Electrical and Computer Engineering, Michigan State University), Shaunak D. Bopardikar (Dept. of Electrical and Computer Engineering, Michigan State University), Alexander Von Moll (Control Science Center, Air Force Research Laboratory), Eric Torng (Dept. of Computer Science and Engineering, Michigan State University), David W. Casbeer (Control Science Center, Air Force Research Laboratory)
- **Year**: 2023
- **Venue**: The first-page header prints verbatim: "IEEE Control Systems Letters paper presented at 2023 American Control Conference (ACC), San Diego, CA, USA. May 31 - June 2, 2023". So the indexer guess (IEEE Control Systems Letters, L-CSS) is **correct**; the printed pagination 3350–3355 is the ACC 2023 proce
[CONTRIBUTIONS]
1. **Modeling**: First perimeter-defense formulation with a fixed-base turret characterized by (heading angle, bounded slew rate ω, range r ∈ [ρ, 1], startup time ∆ > 0), including a lock-on/spool-up capture semantics and a collocated-intruder rule n∆ (Sec. II-A, pp. 3351–3352); offline (P1) and online (P2) problem statements with a competitive-ratio definition adapted to partial capture counts (Sec. II-B, pp. 3352–3353).
2. **Complexity/equivalence (theory)**: Theorem 3.1 — P1 is equivalent to a Travelling Repairperson Problem with Time Windows (TRP-TW) on a line segment (p. 3352); Proposition 3.2 — a 2-approximation algorithm exists for P1 for all parameter regimes, by adapting [28] (p. 3352).
3. **Polynomial-time optimal offline control (theory + algorithm)**: for the regime r = ρ, ∆ > 
[RESULTS-LIST]
- **Turret dynamics**: γ̇_t = u, u a measurable signal in [−ω, +ω] (simple kinematics, bounded slew in either direction) (p. 3351). Heading γ_t ∈ [−θ, θ]. Range r ∈ [ρ, 1] is "the radial distance until which the turret can neutralize an intruder" (p. 3351).
- **Startup/spool-up semantics**: to capture intruder j the turret must lock on (γ_t = θ_j and decides to capture) and then hold γ_t fixed for ∆ time units; "if the turret locks on to the jth intruder at time t, then the jth intruder is captured and removed from E(θ) at time t + ∆" (pp. 3351–3352). Consequently there is "no benefit for the turret to spool up ... if z_j(t) > r + ∆v"; the turret may wait at θ_j until z_j(t) = r + ∆v so that capture occurs exactly as the intruder crosses radius r (p. 3351; cf. Fig. 1, p. 3351). Alternative convention stated to be equivalent with trivial modification: startup time coincides with capturing
[CITATION]
**Role in a paper's narrative**: use as (a) *related work* for turret-defense and perimeter-defense with actuation constraints (startup/spool-up time, finite range, slew-rate limit) — it is the fixed-base-defender counterpart of the mobile-defender competitive line [24], [25] and the P008 journal extension; (b) *gap support* when arguing that differential-game/HJI approaches do not scale to many online-released intruders and that worst-case (competitive) analysis is the right lens for coordinate

### P008 — Multivehicle Perimeter Defense in Conical Environments
[BIBLIO]
- **ID**: P008
- **Source file**: `Bajaj 等 - 2024 - Multivehicle Perimeter Defense in Conical Environments.pdf`
- **Total pages**: 18 (journal pp. 1439–1456); PDF page k corresponds to journal page 1438+k
- **Title**: Multivehicle Perimeter Defense in Conical Environments
- **Authors**: Shivam Bajaj (Member, IEEE; was with Dept. of Electrical and Computer Engineering, Michigan State University, East Lansing, MI 48824 USA; now with Dept. of Electrical and Computer Engineering, Purdue University, West Lafayette, IN 47907 USA; bajaj41@purdue.edu; corresponding author), Shaunak D. Bopardikar (Senior Member, IEEE; Dept. of Electrical and Computer Engineering, Michigan State University, East Lansing, MI 48824 USA), Eric Torng (Dept. of Computer Science and Engineering, Michigan State University), Alexander Von Moll (Senior Member, IEEE; Control Science Center, Air Force Research Laboratory, Dayton, OH 45433 USA), David W. Casbeer (Control Science Center, Air Force Research Laboratory, Dayton, OH 45433 USA) — affiliations as printed in the first-page footnote (p. 1439)
- **Year**: 2024
- **
[CONTRIBUTIONS]
1. **Problem formulation (modeling)**: Perimeter defense with M > 1 identical finite-capture-radius vehicles in a conical environment under arbitrary (non-stochastic, non-anticipative) intruder releases, characterized by five parameters θ, v, ρ, r, M (p. 1440, 1441). The intruder set is fully adversarial; only the "at least one offline-capturable intruder" restriction is imposed (p. 1441).
2. **Necessary condition (theory)**: A fundamental limit — Theorem 5 (p. 1442) — giving a sharp condition on (θ, ρ, v, r, M) beyond which *no* online algorithm has a finite competitive ratio, via an explicit stream-plus-burst adversarial construction; plus Lemma 3 (optimal equal partition and vehicle placement) and Lemma 4 (stationary-capture radius threshold r ≥ ρ sin(θ/M)), the latter an improved lower
[RESULTS-LIST]
- **Dynamics.** Vehicles: first-order integrators, unit speed (footnote 2: unit speed normalizes the scale; "speed of the intruders" and "speed ratio" v are used interchangeably). Footnote 1 states the work "can be extended to other models, such as double integrator" — left to future work. Intruders: released on y = 1, then radial inward motion at fixed speed v.
- **Information structure.** Online A sees only the revealed prefix I(t) (release times, counts, and locations after they occur); O is noncausal. The competitive analysis is interpreted as a game between the online player and an adversary who knows A and constructs the worst input [34] (p. 1441).
- **Capture / breach / winning conditions.** Capture: intruder within or on the capture circle (radius r, centered at a vehicle) at any instant; captured intruders are removed from E(θ). Breach: intruder reaches ∂R(ρ, θ) uncaptured (p. 1
[CITATION]
**Role**: This is the canonical reference for *worst-case (competitive) multi-vehicle perimeter defense in conical environments*. Use it as (a) **related work / gap support** when arguing that game-theoretic reach-avoid and stochastic dynamic-routing approaches assume a priori intruder information or average-case inputs, while arbitrary adversarial release sequences require online-algorithm analysis; (b) **method comparison** as the multi-vehicle extension of the single-vehicle conical-environme

### P009 — Randomized Competitive Perimeter Defense on a Line
[BIBLIO]
- **ID**: P009
- **Source file**: `Bajaj 等 - 2024 - Randomized Competitive Perimeter Defense on a Line.pdf`
- **Total pages**: 6 (journal pp. 1000–1005); PDF page k corresponds to journal page 999+k
- **Title**: Randomized Competitive Perimeter Defense on a Line
- **Authors**: Shivam Bajaj (Member, IEEE; Dept. of Electrical and Computer Engineering, Purdue University, Lafayette, IN 47905 USA, bajaj41@purdue.edu), Eric Torng (Dept. of Computer Science and Engineering, Michigan State University, East Lansing, MI 48824 USA), Shaunak D. Bopardikar (Senior Member, IEEE; Dept. of Electrical and Computer Engineering, Michigan State University, East Lansing, MI 48824 USA) — affiliations as printed in the footnote on p. 1 (p. 1000)
- **Year**: 2024
- **Venue**: IEEE Control Systems Letters, Vol. 8, 2024, pp. 1000–1005. Indexer guess (L-CSS) is **correct** — the running header on every even page prints "IEEE CONTROL SYSTEMS LETTERS, VOL. 8, 2024". Manuscript received 8 March 2024; revised 26 April 2024; accepted 16 May 2024; date of publication 30 May 2024; date of current version 17 June 2024
[CONTRIBUTIONS]
1. **Fundamental lower bound, 2-competitive regime (theory)**: For any instance with v > (1−ρ)/ρ, every randomized online algorithm has c(P) ≥ 2 against an oblivious adversary (Theorem 1, p. 3). Hence in this regime randomization cannot help at all — the randomized frontier coincides with the deterministic one.
2. **Fundamental lower bound, 4/3-competitive regime (theory)**: For v ≥ (1−ρ)/(1+ρ) and Δ < ε (ε defined in the theorem statement), every randomized online algorithm has c(P) ≥ 4/3 ≈ 1.33 (Theorem 2, p. 3). This is the first randomized lower bound for the problem and shows the deterministic 2 bound of [15, Th. III.2] cannot be the whole story near that speed boundary.
3. **Algorithm Stay and a universal 2-competitive guarantee (algorithm + theory)**: A memoryless open-loop algorith
[RESULTS-LIST]
- **Dynamics.** Intruders: constant-speed, straight-line, first-order motion, ẏ = v · sign-inward, from endpoint ±1 toward the nearest perimeter point ±ρ; speed v > 0 fixed per instance. Vehicle: single integrator with unit speed, control = heading on [−1, 1]: u: I(t) × P(ρ,v,N,Δ) → [−1,1] (deterministic) and u_rand: I(t) × P(ρ,v,N,Δ) × Ω → [−1,1] (randomized), where Ω is the (non-empty) sample space of the randomization (p. 2). Crossing the full segment takes exactly 2 time units (used repeatedly, e.g., p. 4–5).
- **Information structure.** Online algorithms see only the input prefix I(t); the offline optimum O sees the entire sequence I in advance; the adversary is oblivious (Definition 1, p. 2) — it fixes I before the algorithm's random outcomes are drawn.
- **Capture / breach / winning conditions.** Capture = coincidence of vehicle and intruder positions; breach = intruder reaches ∂R
[CITATION]
**Paragraph role**: P009 is the canonical reference for *randomization in worst-case perimeter defense*: it imports Yao's minimax principle and oblivious-adversary competitive analysis into the perimeter-defense/reach-avoid literature, proves the first algorithm-independent lower bounds (2 and 4/3) for randomized online defense on a line, and supplies three tight randomized algorithms (Stay, Rand-Stay, Sleep-Switch) whose ratios beat the deterministic frontier of the same authors' ACC 2021 paper

### P010 — Interpopulation and Intrapopulation Linear Quadratic Differential Games
[BIBLIO]
- **ID**: P010
- **Source file**: `D:\System\zhuomian\game-paper\Barreiro-Gomez - 2025 - Interpopulation and Intrapopulation Linear Quadratic Differential Games.pdf` (PDF 1.7, created 2025-03-20, modified 2025-03-21; author-accepted manuscript carrying the notice "This article has been accepted for publication in IEEE Transactions on Control of Network Systems. This is the author's version which has not been fully edited...")
- **Total pages**: 13 (pp. 1–12 content + p. 13 author biography; references end on p. 12)
- **Title**: Interpopulation and Intrapopulation Linear Quadratic Differential Games
- **Author**: Julian Barreiro-Gomez (Senior Member, IEEE), KU Center for Autonomous Robotic Systems (KUCARS), Department of Computer and Information Engineering, Khalifa University, Abu Dhabi 129188, UAE (e-mail: julian.barreirogomez@ku.ac.ae). Single-author paper.
- **Year**: 2025
- **Venue** (EXACT from running header/copyright): "IEEE TRANSACTIONS ON CONTROL OF NETWORK SYSTEMS, VOL. 00, NO. 0, 2025" — early-access stage; volume/issue/page numbers not yet assigned at the time of this PDF
[CONTRIBUTIONS]
1. **Modeling (two-level game)**: A multipopulation model in which every agent $i\in\mathcal{I}^p$ obeys an SDE (eq. (5), p. 4) whose drift contains both agent-level terms and the population aggregates $\bar{x}^p_t,\bar{u}^p_t$, and every population obeys an ODE (eq. (1), p. 3) whose right-hand side aggregates the intra-population behavior $f^p$ (eq. (2a)) and the graph-coupled interpopulation control $g^p$ (eq. (2b)). Heterogeneity is allowed *across* populations; homogeneity is required *within* each population (p. 2: heterogeneous populations can be split into homogeneous subclusters).
2. **Solution-concept framework (theory)**: Definitions of interpopulation/intrapopulation best response and Nash equilibria (Definitions 1–6, pp. 3–5), plus HJB backward PDE systems for the three game pr
[RESULTS-LIST]

[CITATION]
**Paragraph role**: P010 is the reference for *two-level (intra + inter) multipopulation LQ differential games over directed graphs solved by ansatz-reduced coupled backward ODEs*. In a pursuit-evasion/attack-defense paper it plays the role of (i) related-work anchor for "team-of-teams" or multi-population adversarial formulations — e.g., when defenders form homogeneous clusters (sensors, interceptors) and clusters themselves play a game; (ii) methodological precedent for reducing high-dimension

### P011 — Reach-Avoid Games with a Time Limit and Detection Range: A Geometric Approach
[BIBLIO]
- **ID**: P011
- **Source file**: `D:\System\zhuomian\game-paper\Chen 等 - 2022 - Reach‐Avoid Games with a Time Limit and Detection Range A Geometric Approach.pdf`
- **Total pages**: 24 (pp. 1–23 content incl. references ending on p. 24; article is paginated 1–24 internally)
- **Title**: Reach-Avoid Games with a Time Limit and Detection Range: A Geometric Approach
- **Authors**: Xi Chen, Jianqiao Yu (corresponding, jianqiao@bit.edu.cn), Kang Niu, Di Yang, Jiaxun Li — Department of Aerospace Engineering, Beijing Institute of Technology, Beijing 100081, China
- **Year**: 2022. Manuscript history printed on p. 1: Received 18 August 2022; Revised 1 October 2022; Accepted 8 October 2022; Published 26 October 2022. Academic Editor: Hiroki Sayama. © 2022 Xi Chen et al., CC-BY open access.
- **Venue (EXACT from header/copyright)**: **Complexity** (Hindawi, published/hosted by Wiley), "Volume 2022, Article ID 9954014, 24 pages". The indexer guess (Nonlinear Dynamics / Commun. Nonlinear Sci.) is **refuted** by the first-page masthead ("Hindawi Complexity") and the Wiley download watermark on ev
[CONTRIBUTIONS]
1. **Theory (attacker detected initially)**: Theorem 1 (p. 6) — under detection, equilibrium play is straight-line at full speed (via HJI on the decoupled simple-motion payoff (9)–(14)), and the attacker can never leave the detection range once detected (Apollonius-circle monotone-separation argument); hence the game reduces to Yan et al.'s time-limit-only game [36] and the barrier is $\mathscr{B}^{\text{inner}}$ (Theorem 2, eq. (17)), plus the degeneracy condition $\mathscr{B} = \mathscr{B}^T$ of Theorem 3 (eq. (18)–(19)). The authors stress this "cannot leave" result is reusable in other games with time limit + detection range.
2. **Theory (equilibrium terminal-state reduction)**: Theorem 4 (pp. 8–9) — for a penetrating trajectory the neutral outcome $\mathscr{S}_{N,1}$ (capture on the t
[RESULTS-LIST]
- **Geometry**: $\Omega = \mathbb{R}^2$ split by the target line $\mathcal{T} = \{(x,y): y = 0\}$ into play region $\Omega_P = \{y>0\}$ and target region $\Omega_T = \{y<0\}$. Coordinate origin on $\mathcal{T}$ below $D$, so $x_D(0) = (0, y_{D,0})$.
- **Dynamics (eq. (1), p. 4)**: simple motion, $\dot{x} = (v_A\cos\varphi_A,\ v_A\sin\varphi_A,\ v_D\cos\varphi_D,\ v_D\sin\varphi_D)^T = f(x)$, with constant max speeds $v_A, v_D$, $\alpha = v_A/v_D < 1$ (defender faster), headings $\varphi_A, \varphi_D \in [-\pi, \pi)$ chosen simultaneously and instantaneously.
- **Time limit**: only the attacker is energy-limited (defender is deployed near the friendly target area): max operating time $t_A$, maximum range $R_A = v_A t_A$. (Typographic note: the quantity is printed as $t_A$ in Table 1 and eq. (15) but as $\bar{t}_A$ in eqs. (3), (7), (8), (63), (66), (68) and on p. 22 — same quantity.)
- **
[CITATION]
This is the reference for **barrier analysis of reach-avoid games under asymmetric, range-limited detection plus an attacker time limit** — i.e., the "blind until detected defender / fuel- or range-limited attacker" model class on a half-plane with a straight target line. Its reusable assets are: (a) the two-threshold classification $(\tfrac{1-\alpha^2}{\alpha}y_{D,0}, \tfrac{\sqrt{1-\alpha^2}}{\alpha}y_{D,0}, \sqrt{\tfrac{1+\alpha^2}{\alpha^2}R_A^2 - 2R_Ay_{D,0}})$ governing bypass vs. penetrat

### P012 — A geometric approach to reach-avoid games with time limits
[BIBLIO]
- **ID**: P012
- **Source file**: `D:\System\zhuomian\game-paper\Chen 等 - 2023 - A geometric approach to reach‐avoid games with time limits.pdf`
- **Total pages**: 18 PDF pages = printed journal pages 192–209 (PDF p.1 = p.192, ..., PDF p.18 = p.209; page citations below use printed pagination)
- **Title**: A geometric approach to reach-avoid games with time limits
- **Authors**: Xi Chen, Jianqiao Yu (corresponding, jianqiao@bit.edu.cn), Di Yang, Kang Niu — School of Aerospace Engineering, Beijing Institute of Technology, Beijing 100081, P. R. China. ORCID: Xi Chen 0000-0002-8355-8952; Kang Niu 0000-0001-7688-9043.
- **Year**: 2023 (Received 8 April 2022; Revised 18 September 2022; Accepted 3 October 2022; © 2022 The Authors, open access CC BY-NC-ND)
- **Venue (EXACT, from printed header/copyright)**: *IET Control Theory & Applications*, published by John Wiley & Sons Ltd on behalf of The Institution of Engineering and Technology; Vol. 17, pp. 192–209 (issue 2 per the publisher download watermark "17518652, 2023, 2"). **DOI (printed)**: 10.1049/cth2.12374.
- **Indexer-guess resolution
[CONTRIBUTIONS]
1. **Modeling**: first formulation of a planar reach-avoid game with time limits on **both** players (p. 193–195), classified by the pair $(\Delta t=\bar t_A-\bar t_D,\; m=\hat r_D/l^0)$ into two stages and three circle-relation subgames (inclusion / intersection / separation of $\Omega_A,\Omega_D$).
2. **Concepts/tools** (theory): the *reaching region* (RR, from Yan et al. [31]) $\Omega_{ARR}=\Omega_A\cap\Omega_{AD}$ with the AD-based Apollonius circle (Properties 1–2, Remarks 1–2, p. 196–197), and the *optimal target point* (OTP) — the feasible point of smallest y-coordinate in $\Omega_{ARR}$ whose location relative to $\mathcal T$ decides the game; on the barrier the OTP lies exactly on $\mathcal T$ (neutral/equilibrium outcome).
3. **Analytic barriers** (theory): closed-form polar-coor
[RESULTS-LIST]

[CITATION]
**Role in the literature**: the definitive closed-form treatment of *time-limited* planar reach-avoid games of kind. It converts a terminal-surface complication that defeats the HJI machinery into pure geometry: reachable-area pairings $(\Omega_A,\Omega_D)$ → Apollonius-based reaching regions → three candidate optimal target points → piecewise polar barriers, with the $\Delta t>0$ case supplying genuinely new phenomena (the additional connecting arc $\mathcal B^{ADD}_\alpha$, the discontinuous b

### P013 — Cooperative Capture Strategy for a Group of Slower UAVs to Intercept One Faster Intruder in 3-D Space
[BIBLIO]
- **ID**: P013. **Source file**: `D:\System\zhuomian\game-paper\Chen和Xia - 2025 - Cooperative Capture Strategy for a Group of Slower UAVs to Intercept One Faster Intruder in 3-D Spac.pdf`. **Total pages**: 13 (IEEE early-access author version).
- **Title**: Cooperative Capture Strategy for a Group of Slower UAVs to Intercept One Faster Intruder in 3-D Space.
- **Authors**: Lin Chen (School of Automation, Beijing Institute of Technology, Beijing 100081, China; e-mail bulinchen@buaa.edu.cn); Yuanqing Xia (Fellow, IEEE; Zhongyuan University of Technology, Zhengzhou 450007, Henan, China, and School of Automation, Beijing Institute of Technology; corresponding author, xia_yuanqing@bit.edu.cn).
- **Year**: 2025 (manuscript received 3 July 2024; revised 7 October 2024 and 3 January 2025; accepted 15 February 2025).
- **Venue**: IEEE Transactions on Aerospace and Electronic Systems (running header "IEEE TRANSACTIONS ON AEROSPACE AND ELECTRONIC SYSTEMS"; ISSN 0018-9251 printed; citation line prints "DOI 10.1109/TAES.2025.3545780"; header volume/issue fields are early-access placeholders "VOL.
[CONTRIBUTIONS]
1. **Geometry (theory)**: Extension of the 2-D Apollonius circle to the 3-D **Apollonius sphere** (Definition 2, eq. (2)–(5)) and a chain of geometric results: position-independent tangent cone angle (Lemma 1, eq. (6)); tangent-point locus centered on the UAV (Lemma 2, eq. (8)–(12)); closed-form implicit **and** parametric equations of the central projection of the sphere from the intruder onto the goal-plane, which is an **ellipse** defining the UAV's projected dominant area (Theorem 1, eq. (13)–(16)).
2. **Modeling (game → swarm)**: Reformulation of the N-vs-1 faster-intruder reach-avoid game into a swarm control problem: lower-altitude UAVs (z_i < z_T, capable of covering) cover the guarded area with their joint projected dominant ellipses via weighted Voronoi partitions (eq. (25)–(33))
[RESULTS-LIST]
**Definition 2 (Apollonius sphere; p. 3, eq. (2)–(5)).** For UAV P at (x_P, y_P, z_P) and intruder T, λ = V_P/V_T < 1: any simultaneous-interception point Γ satisfies ∥Γ − P∥/∥Γ − T∥ = V_P·Δt/(V_T·Δt) = λ (eq. (2)). Squaring gives
**Lemma 1 (p. 4, eq. (6)).** *Statement*: the angle θ between the line T→O (intruder to sphere center) and any tangent line from T to the Apollonius sphere satisfies sin θ = λ, hence θ depends only on the speed ratio, not on the players' positions. *Assumptions*: λ < 1, Definition 2 geometry. *Proof approach* (4 steps): (i) let F be a tangent point, ∥O − F∥ = r, OF ⊥ TF; (ii) compute ∥O − T∥ = ∥T − (P − λ²T)/(1 − λ²)∥ = ∥P − T∥/|1 − λ²| = r/λ (using eq. (4)–(5)); (iii) right triangle OTF gives sin θ = ∥O − F∥/∥O − T∥ = r/(r/λ); (iv) conclude position-independence. *Decisive equation*: sin θ = λ (eq. (6)). Local/analytic. Physical meaning: the UAV's **dominant a
[CITATION]
This is the flagship "geometry + swarm-control" reference for the speed-disadvantaged 3-D goal-defense problem: it converts a multiplayer reach-avoid game with a faster intruder into centroidal-Voronoi coverage over intruder-referenced footprints, with the 3-D Apollonius-sphere → tangent-cone → central-projection-ellipse chain (Lemma 1–2, Theorem 1) as its load-bearing geometric contribution and a CBF-QCQP filter (eq. (46)–(49)) as its safety layer. In a paper's related-work section it plays the

### P014 — Collaborative Constrained Target-Reaching Control in a Multiplayer Reach-Avoid Game
[BIBLIO]
- **ID**: P014
- **Source file**: `D:\System\zhuomian\game-paper\Collaborative_Constrained_Target-Reaching_Control_in_a_Multiplayer_Reach-Avoid_Game.pdf`
- **Total pages**: 8 (journal pages 8467–8474)
- **Title**: Collaborative Constrained Target-Reaching Control in a Multiplayer Reach-Avoid Game
- **Authors**: Haiyan Zhao, Rongxin Cui (Member, IEEE), Weisheng Yan — School of Marine Science and Technology, Northwestern Polytechnical University, Xi'an 710072, China
- **Year**: 2024 (manuscript received 26 Apr 2024; accepted 11 Aug 2024; published 19 Aug 2024; issue date October 2024)
- **Venue (EXACT, from running header)**: IEEE Robotics and Automation Letters, Vol. 9, No. 10, October 2024, pp. 8467–8474. Associate Editor: Junyan Hu; Editor: Hanna Kurniawati. (Indexer guess "RAL" is CORRECT.)
- **DOI**: 10.1109/LRA.2024.3445816 (printed on p. 1; supplementary downloadable material hosted at the same DOI)
- **Tier**: T1 (RAL is on the T1 list). No disagreement.
- **Funding**: NSFC U22A2066 and U21B2047; Shaanxi Innovative Talent Pandeng Program 2017KJXX-38.
- **BibTeX** (from printed 
[CONTRIBUTIONS]
Stated at [p. 8468, end of Sec. I] and verified against the technical sections:
1. **Modeling**: Formulation of the attacker-relocation (CTR) problem as a multiplayer RA game and its rigorous decomposition into two types of one-on-one subgames — the path defense game (PDG, herder vs. attacker on the inter-escort path Lh) and the path blockade game (PBG, escort vs. attacker on the channel walls Ler/Lel), with a Game of Kind on the extended target set T̊(L) [Sec. III, p. 8469].
2. **Theory (barriers / Game of Kind)**: Complete partition of the game state space into capture and escape regions via analytic barrier expressions for three TL geometries — straight inter-escort line (2), straight channel wall (3), and curved channel wall (4) — with a nesting result (7) yielding the convex-hull safe
[RESULTS-LIST]
- **Dynamics (p. 8468, eq. (1))**: ẋa = ua, ẋn = un (single integrators), x(·) ∈ Ωfr ⊂ R², Ω = Ωfr ∪ Ωobs; ‖ua‖ ≤ va, ‖un‖ ≤ vn, speed ratio αn = va/vn < 1 (every defender faster than the attacker). Capture: ∃n: ‖xn − xa‖ ≤ ℓn; typically ϵ > ℓn; T is known only to defenders; both players avoid Ωobs. Terminal time tf = instant A is captured or enters T. **Information structure**: no absolute positions — only relative distance and LOS angle per pair (onboard camera/UWB-style sensing), consistent with the barriers being written in (ρ, β) polar coordinates.
- **Guide geometry (p. 8468–8469)**: A* path from x_a⁰ to xt, Dubins-smoothed with turning radius rw into ηS⁰ (mixed straight/arc); offsets ±ϵ give ηS^r, ηS^l bounding the virtual channel Ωch with tangent endpoints xtr, xtl. Defense path set L = Lh ∪ Lel ∪ Ler, where Lh is the shortest path between the two escorts and Ler/Lel are the esco
[CITATION]
**Role in the literature**: This is the bridge paper between analytic multiplayer reach-avoid barriers (Isaacs-style barriers, Apollonius circles, explicit-policy decomposition à la Yan et al. [30] and Shishika et al. [29]) and adversarial herding/relocation: it converts the fixed target line required by convex-domain RA decompositions into a *moving* target line realized by a virtual defense channel around a Dubins guide path, thereby extending analytic barrier methods to non-convex domains, an

### P015 — Cooperative Team Strategies for Multi-player Perimeter-Defense Games
[BIBLIO]
- **ID**: P015
- **Source file**: `D:\System\zhuomian\game-paper\D. Shishika 等 - 2020 - Cooperative Team Strategies for Multi-Player Perimeter-Defense Games.pdf`
- **Total pages**: 10 (Secs. I–VIII + References on pp. 1–8; Appendix A–C on pp. 9–10)
- **Title**: Cooperative Team Strategies for Multi-player Perimeter-Defense Games
- **Authors**: Daigo Shishika*, James Paulos and Vijay Kumar — GRASP Laboratory, University of Pennsylvania ({shishika, jpaulos, kumar}@seas.upenn.edu) [footnote, p. 1]
- **Year**: 2019 per the arXiv stamp (v2, 25 Dec 2019); the file name carries "2020" (disagreement noted; no year is printed in the PDF body other than reference years)
- **Venue (EXACT info printed in the PDF)**: arXiv preprint only — side-margin stamp "arXiv:1912.04342v2 [eess.SY] 25 Dec 2019". **No journal note, no DOI, no copyright footer is printed anywhere in the PDF.** The work is known to have been subsequently published in an IEEE Transactions journal, but that fact is NOT stated in this document → published venue `to verify` (per instructions, only PDF-printed information is recorded
[CONTRIBUTIONS]
Stated at [p. 1, end of Sec. I] and verified against the technical sections:
1. **Theory (decomposition)**: A novel *local-game decomposition* of the perimeter into N_D² local game regions (LGRs) generated by ordered defender pairs (D_R^k, D_L^k) [Sec. IV-A, p. 3], turning the global team game into a family of n_D-vs-n_A local games whose combinatorics live on a circular-arc graph.
2. **Theory (intruder side / lower bound)**: The guaranteed intruder score Q_LG = max_G Σ_{k∈G} max{q^k, 0} (eq. (6)) computable in O(N_D^4) as a maximum-weight independent set on a circular arc graph [Sec. IV-C, p. 4], with an intruder team strategy (Theorem 1, eq. (7)) realizing it against ANY defender strategy.
3. **Algorithm (defender side)**: A polynomial-time *LGR defense policy* (Algorithms 1–4, pp. 5–6) 
[RESULTS-LIST]
- **1v1 game** [Sec. III-A, p. 2]: game space splits into intruder-winning R_A(s_D) and defender-winning R_D(s_D), separated by the **barrier** [16] — for perimeter defense a closed curve through the defender position.
- **Property 1 (p. 2)**: the barrier consists of left and right barriers; from x_A ∈ R_D the intruder cannot penetrate the left (resp. right) barrier so long as the defender moves ccw (resp. cw) [15], [16]. Consequence: from R_D the defender keeps the intruder in R_D forever (global, analytic result inherited from [16]).
- **2v1 game** [Sec. III-B, p. 2]: naive independent combination R_I(i, j) = R_A(i) ∩ R_A(j) (eq. (3)); the true intruder-winning region R_C(i, j) (subscript C = cooperative) is *strictly smaller*; its boundary combines the left barrier of D_i, a circle centered at the defenders' midpoint, and the right barrier of D_j (Fig. 2). **Paired-defense region**: R
[CITATION]
**Paragraph role**: this is the landmark "team-vs-team exactness" paper for perimeter-defense reach-avoid games: it converts the assignment-based defense paradigm (pairwise outcomes [14], NP-hard cooperative augmentation [15]) into a polynomial-time, provably optimal team strategy for a class of configurations, by decomposing the perimeter into local games induced by defender pairs and proving a matching pair of intruder/defender bounds (eqs. (6)–(7) vs. (10)) that closes into a saddle-point equ

### P017 — Game-Theory-Assisted Reinforcement Learning for Border Defense: Early Termination based on Analytical Solution
[BIBLIO]
- **ID**: P017
- **Source file**: `D:\System\zhuomian\game-paper\Das 等 - Game-Theory-Assisted Reinforcement Learning for Border Defense Early Termination based on Analytica.pdf` (mission filename was truncated at "based on An.pdf"; true title from p. 1). Sibling file `Das 等 - 2026 - Game-Theory-Assisted...pdf` is a different-build duplicate archived as P016 (preprint variant); this P017 file is the IEEE Xplore published build (Xplore watermark dated Aug 20, 2026).
- **Total pages**: 7 (printed pages 785–791)
- **Title**: Game-Theory-Assisted Reinforcement Learning for Border Defense: Early Termination based on Analytical Solutions
- **Authors**: Goutam Das (School of Aeronautics and Astronautics, Purdue University); Michael Dorothy (Army Research Directorate, DEVCOM Army Research Laboratory, APG, MD); Kyle Volle (Munitions Directorate, Air Force Research Laboratory, Eglin AFB, FL); Daigo Shishika (Department of Mechanical Engineering, George Mason University)
- **Year**: 2026
- **Venue (EXACT, from page-1 footer/copyright)**: "2026 American Control Conference (ACC), May 27-29, 2026. 
[CONTRIBUTIONS]
Stated at [p. 785, end of Sec. I] ("Our contributions are threefold") and verified against the technical sections:
1. **Modeling**: A two-phase border-defense formulation with heterogeneous, per-defender sensing/capture radii and bilateral initial-position uncertainty, transitioning from partial to perfect information at the random sensing time t_s (eqs. (1)–(11), Definitions 1–2, pp. 785–787) — the pre-detection phase is a stochastic optimization (14) coupling sensing probability and pursuit configuration quality (Remark 1).
2. **Theory**: Closed-form Nash equilibrium payoff of the post-detection pursuit phase via Apollonius Circle geometry — Lemma 1 (dominance region), Theorem 1 for one defender (eq. (16)), and Proposition 1 for multiple defenders as the minimum y-coordinate over the int
[RESULTS-LIST]
- **Dynamics, eq. (1)**: ẋ_k = v_k u_k, k ∈ {D_1, …, D_{n_d}, A}, single integrators, u_k ∈ U ≜ {u ∈ R² | ‖u‖ ≤ 1}; state x(t) = [x_D1⊤, …, x_Dnd⊤, x_A⊤]⊤ ∈ R^{2(n_d+1)}. Necessary condition for capture: ν_i = v_Di/v_A > 1 ∀i.
- **Initial condition, eqs. (2)–(3)**: x_A(0) ∼ Uniform(Ω_A); {x_Di(0)} ∼ Uniform(Ω_D), separate predefined regions — this is the source of the partial-information Phase I.
- **Sensing time, eq. (4)**: t_s = inf{t ≥ 0 | ∃i ∈ I : ‖x_A − x_Di‖ ≤ ρ_s^(i)}. Assumption (p. 786): after sensing, full state "trivially" becomes available to all agents for t ≥ t_s (broadcast upon detection).
- **Policies, eqs. (5)–(7)**: Phase-I defender policy γ_Di : O_i → U where O_i contains only defender positions (defender positions are shared over communication; only the attacker is unobserved); Phase-II policy γ_Di : R^{2(n_d+1)} → U. Attacker: γ_A = u_direct = [0, −1]⊤ if t < t_s; γ*
[CITATION]
**Paragraph role**: this is the canonical recent example of *hybrid analytic-game/RL architectures* for adversarial search-and-pursuit under partial observability: the Apollonius-circle Nash value of the post-detection subgame is computed in closed form (or via a tiny convex program) and substituted as the terminal reward at the sensing instant, so MARL (MAPPO) spends all its samples on the genuinely hard, solution-free part — the stochastic search — while provably-optimal continuation is guaran

### P018 — A Geometric Tool for Two-Phase Multiplayer Reach-Avoid Games: Ellipses
[BIBLIO]
- **ID**: P018
- **Source file**: `D:\System\zhuomian\game-paper\Deng 等 - 2024 - A Geometric Tool for Two-Phase Multiplayer Reach-Avoid Games Ellipses.pdf`
- **Total pages**: 6 (printed proceedings pages 46–51; PDF flagged as password-protected by the reader but opens normally — extracted with pymupdf)
- **Title**: A Geometric Tool for Two-Phase Multiplayer Reach-Avoid Games: Ellipses
- **Authors**: Ruiliang Deng, Yang Sun, Zongying Shi, Yisheng Zhong (Department of Automation, Tsinghua University, Beijing 100084, China; emails `{drl20, suny19}@mails.tsinghua.edu.cn`, `{szy, zys-dau}@mail.tsinghua.edu.cn`)
- **Year**: 2024
- **Venue (EXACT from header/copyright)**: "2024 European Control Conference (ECC), June 25-28, 2024. Stockholm, Sweden"; copyright line "978-3-9071-4410-7 ©2024 EUCA". Indexer guess (ECC) is **correct**.
- **DOI**: not printed on the PDF.
- **Funding (printed)**: Science and Technology Innovation 2030 — Key Project of "New Generation Artificial Intelligence", Grant 2020AAA0108200.
- **Tier**: T2 (top control conference). Agree — ECC (EUCA flagship) is a leading co
[CONTRIBUTIONS]
1. **Theory — point-safe-region game of kind (Thms. 1–2)**: the thief wins **iff** the target region intersects an open ellipse with foci at the thief's initial position and the safe point, and major axis $v_T \times$(fastest guarder's arrival time at the safe point). Theorem 1 holds for arbitrary guarder speeds but zero capture radii; Theorem 2 for nonzero capture radii but guarders no slower than the thief — a complementary pair. A logarithmic-spiral "bypassing path" construction handles slower guarders (p. 3).
2. **Theory — cooperative two-guarder defense (Thms. 3–4)**: when neither guarder alone can defend, a minimax characterization via the value functions $h_i$ (eq. (7)) plus Danskin's theorem; under a structural "uniform minimizer" assumption, the game of kind again reduces to a sin
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 1)**: first-order simple motion in $\mathbb{R}^2$,
- **State/information**: state $X = [\mathbf{x}_T^\top, \mathbf{x}_{D_1}^\top, \dots, \mathbf{x}_{D_{N_D}}^\top]^\top \in \mathbb{R}^{2(N_D+1)}$, initial state $X_0$. "It is assumed that the state is fully observable to all players. Each player can make decisions based on all the available state information up to the current moment. However, they do not have access to the current control of their opponents" (p. 2) — i.e., nonanticipative (delayed-opponent-input) information structure.
- **Capture**: thief captured by $D_i$ iff $\|\mathbf{x}_T - \mathbf{x}_{D_i}\|_2 \le r_{D_i}$ (p. 2).
- **Winning condition (unnumbered display, p. 2)**: the thief wins iff $\exists t_f \in \mathbb{R}$: $\mathbf{x}_T(t_f) \in \mathcal{S}$; $\exists t_c \in [0,t_f]$, $\mathbf{x}_T(t_c) \in \mathcal{G}$; $\forall t\in[0,t_f]$, $\min
[CITATION]
**Paragraph role**: P018 is the first paper in this collection to treat **two-phase (capture-the-flag-type) multiplayer** reach-avoid games with a purely geometric method, and the origin of the *ellipse* as the two-phase analogue of the Apollonius circle: the thief's two-leg objective (enter $\mathcal{G}$, then reach $\mathcal{S}$) has iso-cost sets that are ellipses with foci at the thief's initial position and the safe point, with major axis $v_T \times$ the guarders' one-leg deadline. It is a

### P019 — Reach-Avoid Games With Two Cooperative Attackers: Value Function and Singular Surfaces
[BIBLIO]
- **ID**: P019
- **Source file**: `D:\System\zhuomian\game-paper\Deng 等 - 2024 - Reach-Avoid Games With Two Cooperative Attackers Value Function and Singular Surfaces (2).pdf` (16 PDF pages = printed pp. 558–573; PDF not actually encrypted — opens normally, `needs_pass = 0`)
- **Title**: Reach-Avoid Games With Two Cooperative Attackers: Value Function and Singular Surfaces
- **Authors**: Ruiliang Deng, Zongying Shi (Member, IEEE), Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, China (corresponding author: Z. Shi)
- **Year**: 2024 (Vol. 60, No. 1, February 2024; date of publication 23 October 2023; manuscript received 27 Mar 2023, revised 8 Aug 2023, accepted 15 Oct 2023; refereeing handled by T. Lee)
- **Venue (EXACT from header/copyright)**: IEEE Transactions on Aerospace and Electronic Systems (header: "IEEE TRANSACTIONS ON AEROSPACE AND ELECTRONIC SYSTEMS, VOL. 60, NO. 1, FEBRUARY 2024"; copyright 0018-9251 © 2023 IEEE). Indexer guess (TAES) is **correct**.
- **DOI (printed)**: 10.1109/TAES.2023.3326780. Supplementary downloadable material available
[CONTRIBUTIONS]
Stated by the authors (p. 559) and verified against the body:
1. **Theory (Lemma 1, Sec. II, p. 560)**: A necessary and sufficient viscosity condition on a singular surface for a function with $m>2$ differentiable branches, $u=\min_{i\in I}u_i$: $F(x_0,\sum_i\lambda_i\nabla u_i(x_0))\ge 0$ for all convex weights $\lambda_i\ge0$, $\sum\lambda_i=1$ (eq. (2)); generalizes Melikyan's $m=2$ result [21]. Companion Lemma 2 handles the mixed max–min representation (3) (condition holds automatically).
2. **Theory (Theorem 1, Sec. IV, p. 565)**: Full-state-space value function $J_1(X)$ for the constrained scenario (defender must capture $A_1$ first), constructed by geometric Apollonius-circle reasoning and proved to be the *unique viscosity solution* of the HJI equation — including the viscosity con
[RESULTS-LIST]
- **Dynamics (eq. (4), p. 561)**: $\dot X=F$, $F=[u_D^\top,\ \alpha_1 u_{A_1}^\top,\ \alpha_2 u_{A_2}^\top]^\top$, state $X=[x_D^\top,x_{A_1}^\top,x_{A_2}^\top]^\top\in\mathbb{R}^6$, controls $u_D,u_{A_i}\in\mathbb{S}^1$; defender speed normalized to 1, $A_i$ speed $\alpha_i<1$. Simple motion; point capture ($A_i$ captured iff $\|x_D-x_{A_i}\|_2=0$); $T_i$ = capture time of $A_i$; game ends at $t_e=\max_i T_i$.
- **Target / winning**: $\Omega=\{y\le 0\}$; attack team wins iff $x_{A_i}(T_i)\in\Omega$ for $i=1$ or $2$.
- **Cost (game of degree, eq. (5))**: $J(X(0);F(t))=\min_i y_{A_i}(T_i)$; attackers minimize, defender maximizes; $J\le0\iff$ attack team wins, so the game of kind is solved by the degree value.
- **Two-phase reduction (eqs. (6)–(8))**: after the first capture at $t_f=\min_i T_i$ the game reduces to one-defender–one-attacker; equivalent terminal payoff $J=\min\{y_{A_{i1}}(t_
[CITATION]
**Role in the literature**: the rigorous backbone for one-defender–two-attacker reach-avoid games with cooperative attackers, and a methodological exemplar of the modern viscosity-solution treatment of singular surfaces in simple-motion differential games. Three distinct citation payloads: (a) the $m$-branch viscosity Lemma 1 as a reusable certification tool for kinks of value functions; (b) Theorem 1 as the *only* fully proved value function in this game class — the canonical counterexample to 

### P021 — Multi-defender capture-the-flag game with convex target regions
[BIBLIO]
- ID: P021 / source file: `Deng 等 - 2025 - Multi-defender capture-the-flag game with convex target regions.pdf` / total pages: 13
- Title: *Multi-defender capture-the-flag game with convex target regions*
- Authors: Ruiliang Deng, Zongying Shi (corresponding author), Yisheng Zhong — Department of Automation, Tsinghua University, Beijing, 100084, China
- Year: 2025. Venue (EXACT, from header/copyright): **Automatica**, Volume 179 (2025), Article No. 112423 (ISSN 0005-1098, Elsevier Ltd). Article history: received 29 February 2024; revised 8 March 2025; accepted 16 May 2025; available online 13 June 2025. Associate Editor Dena Firoozi; Editor Florian Dörfler. Funding: STI 2030 Key Project "New Generation Artificial Intelligence" Grant 2020AAA0108200; NSFC Grant U24B20173. Not presented at any conference. A Generative-AI statement (gpt4.0 used for readability/language) is printed on p. 12.
- DOI (printed on p. 1): 10.1016/j.automatica.2025.112423
- Tier: **T1** (Automatica). Indexer guess "Automatica" is correct.
- BibTeX (only from printed metadata):
  ```bibtex
  @article{Deng2025mult
[CONTRIBUTIONS]
1. **Modeling**: first formulation and complete solution of the multi-defender CTF game with general convex flag and return regions in $\mathbb{R}^2$ (Sections 3, 5); two-phase recursion with terminal payoff $J_{\mathcal{F}}$ (6) chaining $V^{(2)}$ into phase 1.
2. **Theory**: (a) the phase-2 value equals the optimum $g^*_{\mathcal{R}}(X)$ of a *convex* problem over the attackers' Apollonius dominance region (Theorem 1); (b) the CTF value equals the optimum $W^*(X)$ of a *quasi-convex* problem (19) (Theorems 11, 12, 14), with a unique minimum whenever $W^*(X) > V^{(2)}(X)$; (c) a defender-redundancy result: some subset of at most two defenders suffices to guarantee the game value (Theorem 15), useful for assigning defenders to multiple attackers.
3. **Algorithm**: an iterative two-step con
[RESULTS-LIST]
**Definition 6 (Type-II Effective Set, II-ES):** $E$ with $W(y, X_E) = W(y, X)$ and strict inequality for every non-empty proper subset; $|E| \le 2$ because KKT (24) with linear independence in $\mathbb{R}^2$ would otherwise hold on a proper subset, contradicting minimality (convex sufficiency).
**Lemma 7.** If $\{i\}$ is a II-ES for $(y,X) \in \mathcal{W}$, then $z_{i,m}$ is the unique maximizer of $\max_{z_i \in C_i} V^{(2)}(y, z_i)$. Proof: by (25), any $z \neq z_{i,m}$ in $C_i$ satisfies $\xi_i(d(z, x_m) - r_{Di}) > d(x_m, y)$, i.e., $x_m \in \mathcal{A}(y,z)$ (attacker can pass beyond $x_m$), so $V^{(2)}(y,z) < g_{\mathcal{R}}(x_m) = W(y, X_i)$.
**Theorem 8.** If $E = \{i,j\}$ is a II-ES for $(y,X) \in \mathcal{W}$, then $(z_{i,m}, z_{j,m})$ is the unique maximizer of $\max_{z_E \in C_i \times C_j} V^{(2)}(y, z_E)$. Proof (woven into the preceding text, no separate QED): $x_m \in \p
[CITATION]
**Role.** This is the terminal point of the optimization-based CTF line (Garcia et al. 2018 → Pachter et al. 2020 → Zhou et al. 2021 → here) and the first complete solution of a multi-defender CTF game with general convex target regions; its two reusable assets are (i) the reduction "two-phase game value = quasi-convex program (19) with inner convex program (18)", including the Danskin-based state-gradient machinery ((30), (31), (36), (37)) that certifies equilibrium via the Isaacs condition, an

### P022 — Design and Analysis of State-Feedback Optimal Strategies for the Differential Game of Active Defense
[BIBLIO]
- **ID**: P022
- **Source file**: `D:\System\zhuomian\game-paper\Design_and_Analysis_of_State-Feedback_Optimal_Strategies_for_the_Differential_Game_of_Active_Defense.pdf`
- **Total pages**: 16 (journal pages 553–568)
- **Title**: Design and Analysis of State-Feedback Optimal Strategies for the Differential Game of Active Defense
- **Authors**: Eloy Garcia (Senior Member, IEEE), David W. Casbeer (Senior Member, IEEE), Meir Pachter (Fellow, IEEE). Garcia and Casbeer: Control Science Center of Excellence, Air Force Research Laboratory, Wright-Patterson AFB, Dayton, OH. Pachter: Dept. of Electrical Engineering, Air Force Institute of Technology, Wright-Patterson AFB.
- **Year**: 2019 (issue date: January 28, 2019; online publication April 18, 2018; manuscript received July 26, 2017, accepted March 13, 2018; Recommended by Associate Editor D. Hristu-Varsakelis). Notice: "U.S. Government work not protected by U.S. copyright."
- **Venue (exact, from running header)**: IEEE Transactions on Automatic Control, Vol. 64, No. 2, February 2019, pp. 553–568. Indexer guess (IEEE TAC) is **correct**.
[CONTRIBUTIONS]
1. **Theory — complete regular solution of the ATDDG Game of Degree in the 6-D Cartesian state space** (Theorem 1 for DT ≤ AT, Theorem 2 for DT > AT, x ∈ R_e): closed-form state-feedback saddle-point headings for all three agents, determined by a single scalar — the optimal interception point I* = (x*, y*) on the orthogonal bisector of AD, whose abscissa x* is the (real) root of an explicit quartic equation (15) parameterized by the speed ratio α.
2. **Theory — closed-form Value function** (17)/(74) (piecewise V_s/V_g, continuous and C1 over the escape region), proved to be the classical (C1) solution of the stationary HJI equation everywhere in the T/D winning region (67); explicit gradient (66). No singular surfaces.
3. **Theory — degenerate-case Target heading** (Corollary 1 + Definitio
[RESULTS-LIST]
- **Dynamics (p. 554, eq. (1))**: Isaacs' "simple motion" in the Euclidean plane, six-dimensional state x = (x_T, y_T, x_A, y_A, x_D, y_D) ∈ R^6, game set = entire R^6:
- **Termination set (p. 554–555, eq. (2))**: C = C1 ∪ C2, C1 = {x : (x_A−x_D)² + (y_A−y_D)² = 0} (D intercepts A; T escapes), C2 = {x : (x_A−x_T)² + (y_A−y_T)² = 0} (A captures T). Point capture. Conceptually a two-target differential game [24]–[26].
- **Order of preference (Definition 1, p. 555)**: Type P: m_t ≻_P n_t ≻_P Υ and Υ ≻_E n_t ≻_E m_t — nontermination Υ is worst for A (it cannot win by running: D follows A while T increases the A–T separation) and best for the T/D team; the game terminates only on penetrating contact. This rules out nonterminating play and justifies no discriminatory/stroboscopic strategies.
- **Game of Degree terminal manifold (p. 555, eq. (3))**: x_A = x_D, y_A = y_D — a 4-D hyperplane in R^
[CITATION]
This is the canonical, complete closed-form solution of the three-player active target defense differential game and a flagship example of a differential game with a six-dimensional state solved in the classical sense — saddle-point state-feedback strategies, an explicit C1 Value (α·AI ± TI), HJI verification, and an exact Apollonius/hyperbola barrier. Role in a paper's argument: (i) as the foundational ATDDG reference when formulating target-defense games with an adversarial Attacker (as oppose

### P023 — One Apollonius Circle is Enough for Many Pursuit-Evasion Games
[BIBLIO]
- **ID**: P023
- **Source file**: `D:\System\zhuomian\game-paper\Dorothy 等 - 2022 - One Apollonius Circle is Enough for Many Pursuit-Evasion Games.pdf`
- **Total pages**: 8 (preprint pagination: article pp. 1–6, references pp. 6–7, Appendix A pp. 7–8). This copy is the arXiv v1 preprint; it carries handwritten margin annotations on p. 1 and highlight annotations on pp. 2–3.
- **Title**: One Apollonius Circle is Enough for Many Pursuit-Evasion Games
- **Authors**: Michael Dorothy (Computational and Information Sciences Directorate, Army Research Laboratory, APG, MD); Dipankar Maity (Dept. of Electrical and Computer Engineering, University of North Carolina, Charlotte, NC); Daigo Shishika (Dept. of Mechanical Engineering, George Mason University, Fairfax, VA); Alexander Von Moll (Control Science Center, Air Force Research Laboratory, WPAFB, OH). Printed footnote (p. 1): authors listed alphabetically; first two authors contributed equally (co-first authors); corresponding author M. Dorothy; supported by ARL DCIST CRA W911NF-17-2-0181.
- **Year**: printed footer "Preprint submitted to Au
[CONTRIBUTIONS]
1. **Theory (main)**: Theorem 1 (p. 3) — a Lyapunov-based pursuit law $\mathbf{v}_P=\hat{\mathbf{z}}_P$ with $\mathbf{z}_P=(R_C-R_A(t))\hat{\mathbf{r}}(t)+\nu\,\mathbf{y}(t)$ that (i) confines the time-varying AC strictly inside a fixed disc $\mathcal{C}$ = initial AC inflated by $\delta$, for all $t>t_0$, against any admissible evader, and (ii) guarantees finite-time capture with explicit bound $t_{\text{capture}}\le t_0+2(1+\nu^{-1})R_C\ln(R_C/\delta)$.
2. **Theory (refinements)**: Corollary 1 — capture occurs strictly closer to the initial AC than the $\delta$-inflation suggests; Lemma 1 — the pursuer–evader distance is strictly decreasing below its initial value at all times ($\|{\bf r}(t)\|<\|{\bf r}(t_0)\|$); Corollary 2 — hence a pursuer with a circular sensor of range $\rho\ge\|{\b
[RESULTS-LIST]
- **Dynamics**: $\dot{\bf x}_E={\bf v}_E$, $\dot{\bf x}_P={\bf v}_P$, ${\bf x}_E,{\bf x}_P\in\mathbb{R}^2$ (simple motion, single integrator, fixed Cartesian frame); bounds $\|{\bf v}_E\|\le\nu$, $\|{\bf v}_P\|\le1$, $\nu<1$. Start at $t_0$. **Termination**: point capture, ${\bf x}_P={\bf x}_E$ (p. 3).
- **Apollonius disc** (eq. (1), p. 3): $\mathcal{A}(t)\triangleq\{{\bf x}:\|{\bf x}-{\bf x}_A(t)\|\le R_A(t)\}$, where ${\bf x}_A(t)=\alpha{\bf x}_E(t)-\beta{\bf x}_P(t)$, $R_A(t)=\gamma\|{\bf r}(t)\|$, ${\bf r}(t)={\bf x}_E(t)-{\bf x}_P(t)$, and $\beta=\nu^2(1-\nu^2)^{-1}=\nu\gamma=\nu^2\alpha$; so (implicitly) $\alpha=(1-\nu^2)^{-1}$, $\gamma=\nu(1-\nu^2)^{-1}$, $\beta=\nu^2(1-\nu^2)^{-1}$, and $\alpha\ge\gamma\ge\beta>0$ for $\nu\in[0,1)$. These are exactly the standard AC formulas: center $({\bf x}_E-\nu^2{\bf x}_P)/(1-\nu^2)$, radius $\nu\|{\bf x}_E-{\bf x}_P\|/(1-\nu^2)$. (Minor pres
[CITATION]
**Paragraph role**: This is the definitive "geometric satisficing" paper of the Apollonius-circle line: it converts the AC from a barrier-construction tool into a *containment* guarantee via a Lyapunov argument, and thereby dissolves the dispersal/switching-surface pathologies (chattering, perpetuated dilemma, non-Nash mixed strategies) that the Hamilton–Jacobi treatment of target-guarding games must patch case by case. In the P-collection it is the canonical citation for (a) the precise stateme

### P025 — Perimeter-defense Game between Aerial Defender and Ground Intruder
[BIBLIO]
- **ID**: P025 | **Source file**: `D:\System\zhuomian\game-paper\E. S. Lee 等 - 2020 - Perimeter-defense Game between Aerial Defender and Ground Intruder.pdf` | **Total pages**: 7
- **Title**: Perimeter-defense Game between Aerial Defender and Ground Intruder
- **Authors**: Elijah S. Lee, Daigo Shishika and Vijay Kumar — GRASP Lab, University of Pennsylvania, Philadelphia, PA 19104 USA, {elslee, shishika, kumar}@seas.upenn.edu (p. 1 footnote). Funding: "ARL grant DCIST CRA W911NF-17-2-0181" (p. 1).
- **Year**: 2020 | **Venue**: the ONLY venue information printed in the PDF is the arXiv stamp on the p. 1 margin: "arXiv:2012.14980v1 [cs.RO] 29 Dec 2020". No conference name, no journal, no DOI, no copyright notice appears anywhere in the PDF (all "IEEE" strings occur inside reference entries). The paper is typeset in the IEEE two-column conference template, which suggests a conference submission, but the venue is UNPRINTED. **No DOI printed.**
- **Tier**: T2 (per skill default for this class of preprint). Note disagreement: this is an unreviewed arXiv preprint (cs.RO) whose several lemma
[CONTRIBUTIONS]
1. **Modeling (theory)**: a one-defender-one-intruder perimeter-defense game in 3D — defender on a unit hemisphere, intruder on the base plane — with a 3-state relative model $z = [\psi, \phi, r]$ (azimuth difference, defender elevation, intruder radius) and first-order dynamics (eq. (3), p. 2); Game-of-Kind termination conditions (p. 2).
2. **Payoff and optimal breaching point (theory)**: a Game-of-Degree payoff equal to the difference of target times $p = \tau_D - \tau_A$ (eq. (4)), parameterized by the breaching angle $\theta$ (eq. (12)); a first-order optimality condition yielding the optimal approach angle $\beta^*$ (Theorem 1, eq. (13)) and, combined with a purely geometric relation (eqs. (18)–(25)), a unique optimal breaching point (Definition 1, Remark 3, pp. 3–4).
3. **Barrier / w
[RESULTS-LIST]
- **3D geometry**: unit hemisphere on ground plane R; perimeter = equator (base circle). Positions in spherical coordinates: $\mathbf{z}_D = [\psi_D, \phi_D, 1]$ (defender on the sphere, unit radius), $\mathbf{z}_A = [\psi_A, 0, r]$ (intruder on the plane, elevation 0, radius $r \ge 1$). Relative state $\mathbf{z} \triangleq [\psi, \phi, r]$ with $\psi \triangleq \psi_A - \psi_D$ and $\phi \triangleq \phi_D$; by azimuthal symmetry one normalizes $\mathbf{z}_D = [0, \phi_D, 1]$, $\mathbf{z}_A = [\psi, 0, r]$ (p. 3). Note the intruder state has only 2 DOF $(\psi_A, r)$; the full relative state is 3D $(\psi, \phi, r)$.
- **Dynamics**: both agents first-order (speed-bounded point mass). Defender velocity parameterized by the altitudinal component $\omega_D \triangleq \dot\phi_D \in [-1, 1]$; with unit speed (eq. (1)): $\|\dot{\mathbf{x}}_D\| = \sqrt{\dot\phi_D^2 + \dot\psi_D^2\cos^2\phi_D}$,
[CITATION]
**Paragraph role**: this is the canonical "first 3D step" of the Shishika–Kumar perimeter-defense line — the reference to cite for **surface-constrained defenders in 3D perimeter defense** (defender on a hemisphere vs. intruder on the ground plane), for the **optimal breaching point / breaching-angle formulation** (payoff = geodesic-time minus straight-line-time difference, eqs. (4), (7)–(12)), and for the **barrier-as-zero-level-set construction with Nash-optimal "run to the breach point" strat

### P026 — Defender-Aware Attacking Guidance Policy for the Target–Attacker–Defender Differential Game
[BIBLIO]
- **ID**: P026 | **Source file**: `D:\System\zhuomian\game-paper\English和Wilhelm - 2021 - Defender-Aware Attacking Guidance Policy for the Target–Attacker–Defender Differential Game.pdf` | **Total pages**: 11 (printed pp. 366–376; the Read tool falsely flags the file as password-protected — it opens fine, `needs_pass = 0`).
- **Title**: Defender-Aware Attacking Guidance Policy for the Target–Attacker–Defender Differential Game
- **Authors**: Jacob T. English (Graduate Research Assistant, Computer Science) and Jay P. Wilhelm (Assistant Professor, Mechanical Engineering), Russ College of Engineering and Technology, Ohio University, Athens, Ohio 45701 (p. 366 footnotes).
- **Year**: 2021 | **Venue (EXACT, from running header + copyright block, p. 366)**: *Journal of Aerospace Information Systems* (JAIS), Vol. 18, No. 6, June 2021, pp. 366–376. Copyright © 2021 by the American Institute of Aeronautics and Astronautics, Inc.; eISSN 2327-3097. Timeline printed: received 6 July 2020, revision 20 January 2021, accepted 22 January 2021, published online 26 February 2021. Associate Editor: E. 
[CONTRIBUTIONS]
1. **Modeling (MDP formulation)**: the TAD engagement framed as an MDP whose 9-dimensional state includes the defender's full pose (Eqs. (19)–(20)), with a one-dimensional continuous action $\Delta\chi$ (Eq. (21)), explicit-Euler simple-motion transitions (Eq. (22)), turn-rate bounds (Eqs. (23)–(24)), and terminal sets $\Gamma_{Win}, \Gamma_{Loss}$ (Eqs. (25)–(26)) (Sec. III, pp. 369–370).
2. **Reward design (algorithm enabler)**: a composite shaped reward (Eqs. (27)–(29)) — terminal win bonus + attacker–target Gaussian attraction − defender-proximity Gaussian penalty − heading-alignment penalty $\kappa\delta$ − constant drain $\iota$ — that makes defender avoidance learnable without a binary-only signal (Sec. III, p. 370, following the Gaussian-shaping practice of [45]).
3. **Algorithm (t
[RESULTS-LIST]
- **Kinematics (p. 366, Eq. (1))**: planar simple motion, velocities normalized by $V_A$: $\dot x_T = \alpha\cos\phi$, $x_T(0)=x_{T0}$; $\dot y_T = \alpha\sin\phi$, $y_T(0)=y_{T0}$; $\dot x_A = \cos\chi$, $x_A(0)=x_{A0}$; $\dot y_A = \sin\chi$; $\dot x_D = \cos\psi$, $x_D(0)=x_{D0}$; $\dot y_D = \sin\psi$. Here $\phi,\chi,\psi$ are target/attacker/defender headings and $\alpha = V_T/V_A < 1$; $V_A = V_D$ (equal-speed assumption, p. 366). The paper asserts 2-D sufficiency "as altitude changes in aerial engagements would be relatively small [28]" (p. 367).
- **State/action/transition (p. 369, Eqs. (19)–(22))**: $s = (x_T, y_T, \phi,\; x_A, y_A, \chi,\; x_D, y_D, \psi) \in S$, $S = \{s \mid s\in\mathbb{R}^9,\ 0 \le \phi,\chi,\psi < 2\pi\}$; action $a = \Delta\chi$ (single real value, the attacker's heading increment); transition by explicit Euler with step $\Delta t$ (Eq. (22)): $x_T' = x_T
[CITATION]
Role in the literature: this is the bridge paper between the analytical TAD canon ([6,8,13,14] — barrier, Apollonius aimpoints, cooperative defense) and learning-based attack guidance; it is the earliest-known-to-this-archive demonstration that a reward-shaped TD3 attacker, observing the defender's full state and punished for defender proximity, can convert the defender's turn-rate constraint into additional capture wins on both sides of the classical escape/capture barrier (26% → 88% overall in

### P027 — Cooperative Path Planning for Multiplayer Reach-Avoid Games under Imperfect Observation Information
[BIBLIO]
- **ID**: P027
- **Source file**: `D:\System\zhuomian\game-paper\Fang 等 - 2024 - Cooperative Path Planning for Multiplayer Reach‐Avoid Games under Imperfect Observation Information.pdf`
- **Total pages**: 14 (printed as "2300794 (1 of 14)" … "(14 of 14)")
- **Title**: Cooperative Path Planning for Multiplayer Reach-Avoid Games under Imperfect Observation Information (title as printed on p. 1; the PDF filename truncates the final word "Information")
- **Authors**: Hongwei Fang, Yue Chen, Peng Yi (corresponding author, yipeng@tongji.edu.cn). Affiliations (p. 1): Department of Control Science and Engineering, Tongji University, Shanghai 201804, China; P. Yi additionally: National Key Laboratory of Autonomous Intelligent Unmanned Systems (Shanghai), Shanghai Research Institute for Intelligent Autonomous Systems, and Frontiers Science Center for Intelligent Autonomous Systems (MoE).
- **Year**: 2024. Received 20 Nov 2023; revised 27 Mar 2024; published online 25 Jul 2024 (p. 13). Open access under CC BY, "© 2024 The Author(s). Advanced Intelligent Systems published by Wiley-VCH GmbH" (eve
[CONTRIBUTIONS]
1. **Modeling — asymmetric-information multiplayer RAG with a bait role** (Sections 2–3, pp. 2–6): a 3D reach-avoid game with a TP coalition (target + pursuers) vs. one evader; the TP coalition has imperfect observation of the evader while the evader has perfect observation; each coalition solves its own subjective game (G1 perfect-information for the evader, G2 imperfect-information for the TP coalition).
2. **Imperfect-observation mechanism — virtual evader with chance constraints** (Section 3.2, pp. 5–6): the TP coalition runs a Kalman filter on the evader, forms a *virtual evader* whose state is the filtered mean plus a Gaussian perturbation with the posterior covariance, and predicts its trajectory via a chance-constrained optimization problem whose feasible set is *inflated* relative
[RESULTS-LIST]
- **Players and coalitions (p. 2, Table 1 p. 3)**: V = {T, E, P_i}, i = 1,…,M−2 (M players total); TP coalition {T, P_1,…,P_{M−2}} vs. evader coalition {E}; same-coalition communication is allowed. States x_j^k = [x_j^k, y_j^k, z_j^k, v_{x,j}^k, v_{y,j}^k, v_{z,j}^k]^T ∈ X_j ⊂ ℝ^{2n}, positions y_j^k = [x_j^k, y_j^k, z_j^k]^T ∈ Y_j ⊂ ℝ^n, actions u_j^k = [a_{x,j}^k, a_{y,j}^k, a_{z,j}^k]^T ∈ U_j ⊂ ℝ^n (accelerations).
- **Dynamics (p. 4, eq. (4))**: discrete double integrator, x_j^{k+1} = A x_j^k + B u_j^k, y_j^k = C x_j^k, ∀j ∈ V, with A = [[I_n, T_s I_n],[0, I_n]] ∈ ℝ^{2n×2n}, B = [[(T_s²/2) I_n],[T_s I_n]] ∈ ℝ^{2n×n}, C = [I_n, 0] ∈ ℝ^{n×2n}.
- **Winning/termination conditions (p. 2)**: "the TP coalition wins the game if a pursuer is close enough to the evader (within the capture distance r_p), and … the evader wins if the evader is close enough to the target (within the attack distan
[CITATION]
**Paragraph role.** P027 is the reference implementation of *asymmetric-information cooperative pursuit as receding-horizon game solving*: it shows how a disadvantaged coalition converts a Kalman-filter belief into a virtual opponent with an inflated (chance-constrained) decision set, and how IBR + distributed ADMM turns that subjective game into real-time, collision-free coalition trajectories validated from simulation down to motion-capture hardware. In the game-paper knowledge base it plays f

### P028 — Multiple Pursuers Versus One Evader Reach-Avoid Differential Games With Asymmetric Observations
[BIBLIO]
- **ID**: P028
- **Source file**: `D:\System\zhuomian\game-paper\Fang 等 - 2025 - Multiple Pursuers Versus One Evader Reach-Avoid Differential Games With Asymmetric Observations.pdf`
- **Total pages**: 12 (journal pages 18605–18616, Vol. 22, 2025)
- **Title**: Multiple Pursuers Versus One Evader Reach-Avoid Differential Games With Asymmetric Observations
- **Authors**: Hongwei Fang (College of Electronic and Information Engineering, Dept. of Control Science and Engineering, Tongji University, Shanghai; e-mail hongweif@tongji.edu.cn), Peng Yi (Member, IEEE; corresponding author; Tongji University, also State Key Laboratory of Autonomous Intelligent Unmanned Systems / Shanghai Research Institute for Intelligent Autonomous Systems, and Frontiers Science Center for Intelligent Autonomous Systems, MoE), Di Deng (Shanghai Research Institute for Intelligent Autonomous Systems; Tongji University), Bing He (Dept. of Electronic Engineering, PLA Rocket Force University of Engineering, Xi'an).
- **Year**: 2025. Received 18 Oct 2024; revised 6 Mar 2025 and 6 May 2025; accepted 20 Jun 2025; Date of
[CONTRIBUTIONS]
1. **Theory — RESR with 3σ guarantees**: a robust estimation of the safe region (RESR) built from pursuer-side uncertainties in γ and d, with closed-form boundary/closure (Theorem 1) and boundedness/strict-convexity properties (Lemma 1), supported by the sensitivity analysis (11)–(14) of the Cartesian-oval boundary radius w.r.t. the game parameters.
2. **Theory — 1v1 winning condition and optimal interception**: an estimated interception point (EIP) defined as the closest point of the RESR to Ωgoal, a feedback "optimal interception strategy" (OIS) with an uncertainty-compensation term (Theorem 2, eq. (33)) guaranteeing ẏI ≥ 0 (the EIP never sinks toward the goal), plus a proximity strategy (PS, eq. (39)) for the case where the RESR already intersects the goal region, which shrinks the RESR
[RESULTS-LIST]
- **Dynamics (p. 18606, eq. (1))**: decoupled simple motion in R², ẋPk = vPk uPk, xPk(0) = x⁰Pk (k = 1,…,Np); ẋE = vI uE, xE(0) = x⁰E. **Printed typo**: the evader speed appears as v_I; it is vE (used everywhere else, e.g., "vE ∈ R+ denote the speeds of Pk and E"). Controls uPk, uE ∈ U = {u ∈ R² : ‖u‖2 = 1} (unit-norm heading); speeds constant with vPk > vE, so 0 < γk = vE/vPk < 1.
- **Capture / termination (p. 18606)**: E is captured iff ‖xPk − xE‖ < φPk for some k (∃k ∈ {1,…,Np}); E wins iff yE(t) < φE (goal region reached through the demarcation line y = φE that accounts for E's capture radius φE); "If the evader reaches Ωgoal, the evader wins, otherwise the pursers win" [sic — typo for "pursuers"].
- **Assumption 1 (Initial Deployment, p. 18606)**: ‖xPk(0) − xE(0)‖ > φPk ∀k and yE(0) > φE.
- **Assumption 2 (Constant Speed, p. 18606)**: no player changes speed during the game (so v̄E 
[CITATION]
**Paragraph role**: this is the archival reference for *pursuit under asymmetric observations* in RA games — i.e., the point in the literature where Apollonius/Cartesian-oval safe-region geometry is made robust to measurement noise and then exploited for *minimal-resource coalition formation*. It complements perfect-information geometric solutions ([1], [13], [17], [20]), uncertainty-aware reachable-set work ([18], [32], [33]), and experimental pursuit testbeds ([27]), and it is one of the few R

### P029 — Adaptive Decision-Making in Attack-Defense Games With Bayesian Inference of Rationality Level
[BIBLIO]
- **ID**: P029
- **Source file**: `Fang和Yi - 2024 - Adaptive Decision-Making in Attack-Defense Games With Bayesian Inference of Rationality Level.pdf`
- **Total pages**: 10 PDF pages = printed pp. 16558–16567 (PDF page k = printed page 16557+k)
- **Title**: Adaptive Decision-Making in Attack-Defense Games With Bayesian Inference of Rationality Level
- **Authors** (byline, p. 16558): Hongwei Fang (Dept. of Control Science and Engineering, Tongji University, Shanghai 201804, China) and Peng Yi (corresponding author; same department, and also with the National Key Laboratory of Autonomous Intelligent Unmanned Systems, Shanghai Research Institute for Intelligent Autonomous Systems, and Frontiers Science Center for Intelligent Autonomous Systems, MOE, Tongji University). Bios (p. 16567): Fang — B.E. Wuhan Polytechnic Univ. of Information Technology 2017, M.S. Sichuan Univ. 2020, Ph.D. student at Tongji; Yi — Ph.D. AMSS Beijing 2016, Professor at Tongji, postdoc Toronto 2016–17 and Washington Univ. St. Louis 2017–19.
- **Year**: 2024. Manuscript received 5 October 2023; revised 23 February
[CONTRIBUTIONS]
Stated by the authors (p. 16559) and verified against the body:
1. **Modeling**: a nonequilibrium AD game with level-k rationality formulated in receding-horizon fashion (Secs. II–III): double-integrator dynamics (1), role-specific quadratic costs (2)–(3), receding-horizon program (4), and the recursive level-k best-response mechanism (5)–(6) with its best-response nesting (7)–(9) relating convergent infinite-level play to NE. Applicable to "adversarial games involving players with different computation and reasoning abilities" [authors' claim].
2. **Inference algorithm**: a Bayesian inference algorithm (Steps 1–4, eqs. (10)–(12)) that updates the defender's belief θ^t(k) over the attacker's reasoning level by scoring each level-k model's *historical receding-horizon prediction trajectorie
[RESULTS-LIST]
- **Players/sets** (Table I, p. 16560): V = {D, A}; state x^t_j ∈ X_j ⊂ R^{2n} = [positions; velocities] along n axes; position y^t_j ∈ Y_j ⊂ R^n; action u^t_j ∈ U_j ⊂ R^n = acceleration vector; u^t_{−j}, x^t_{−j}, y^t_{−j} the opponent's counterparts; C_j : R^{2n} → R^n "dynamics constraint"; H ∈ R prediction horizon.
- **Dynamics, eq. (1)** (p. 16560): discrete-time second-order (double-integrator) model
- **Defender cost, eq. (2)** (p. 16560): J_D(y^t_D, y^t_A, u^t_D) = ‖y^t_D − y^t_A‖²_{Q_D} (term1: close distance to intercept) + ‖u^t_D‖²_{R_D} (term2: control effort), with Q_D, R_D ∈ R^{n×n} positive definite.
- **Attacker cost, eq. (3)** (p. 16560): J_A(y^t_A, y^t_D, u^t_A) = ‖y^t_A − y_p‖²_{Q¹_A} (term1: approach the protected area position y_p) − ‖y^t_A − y^t_D‖²_{Q²_A} (term2: *maximize* distance to the defender, entering with a minus sign because J_A is minimized) + ‖u^t_A‖²_{R
[CITATION]
**Role in the literature**: this is the bridge paper between behavioral game theory (level-k / cognitive hierarchy, refs. [13], [14], [20], [22]) and physical attack-defense/pursuit-evasion games: it supplies (a) a concrete receding-horizon (MPC-style) nonequilibrium AD game model with double-integrator players, (b) the observation that one-step trajectory-difference level inference (the autonomous-driving standard [23]–[26]) is non-identifying in free-motion games, and (c) a working alternative

### P031 — Justification of the geometric solution of a target defense game with faster defenders and a convex target are
[BIBLIO]
- **ID**: P031. **Source file**: `D:\System\zhuomian\game-paper\Fu和Liu - 2023 - Justification of the geometric solution of a target defense game with faster defenders and a convex (2).pdf` (duplicate copy without "(2)" also exists; identical size 1,182,235 bytes). **Total pages**: 10 (PDF page i = printed page i; page numbers cited below are the printed ones).
- **Title**: Justification of the geometric solution of a target defense game with faster defenders and a convex target area using the HJI equation.
- **Authors**: Han Fu (corresponding author, flora.fu@mail.utoronto.ca), Hugh H.-T. Liu — University of Toronto Institute for Aerospace Studies, 4925 Dufferin Street, North York, M3H 5T6, Ontario, Canada.
- **Year/Venue**: Automatica, 149 (2023) 110811 (Brief paper). Article history printed: received 26 Sep 2021, revised 22 Sep 2022, accepted 18 Nov 2022, available online 3 Jan 2023. Associate Editor Andrey V. Savkin, Editor Ian R. Petersen. Footnote: "The material in this paper was not presented at any conference."
- **DOI (printed)**: 10.1016/j.automatica.2022.110811. ISSN printe
[CONTRIBUTIONS]
1. **Theory (main)**: Theorem 2.1 — the geometric control law (2.7) and geometric value (2.8) solve the MDSI HJI equation (2.9a) with boundary conditions (2.9b)–(2.9d), under A1–A5, i.e., under strictly more general conditions (convex target of arbitrary shape, r > 0, arbitrary n) than all prior justifications [authors' claim].
2. **Modeling/proof technique**: a derivative-free-form approach — the tangency point p* is handled as an *implicitly defined* function of player positions via system (3.11) (Stationarity + boundary equation), differentiated implicitly (3.13), with all expressions organized in local orthonormal-style frames F_{α*}, F_{β*} aligned with the defender-to-p* and invader-to-p* directions (3.4)–(3.6); a determinant identity (3.20)/(B.5) collapses the value-gradient to the 
[RESULTS-LIST]
- **Target** (A1, eq. (2.1), p. 2): A = {[x,y]ᵀ | φ(x,y) ≤ 0}, φ: R² → R twice continuously differentiable, A convex.
- **Dynamics** (A2, eq. (2.2), p. 2): single integrators with fixed speed magnitudes — ẋ_j = v_{xj}, ẏ_j = v_{yj}, √(v_{xj}²+v_{yj}²) = v_D (j = 1,…,n); same for the invader with speed v_I. Controls are the velocity vectors; information structure is perfect state feedback (the strategies (2.7) are functions of all player positions).
- **Speed ratio** (A3, eq. (2.3)): v_D ≥ v_I, "or a > 1", a = v_D/v_I. (Printed as stated; note the ≥/> inconsistency — Appendix C uses a ≥ 1. See §7.)
- **Capture** (p. 2): ∃j ∈ {1,…,n} s.t. ‖p_I − p_j‖ ≤ r; A4: r > 0. **Remark 2.1** (p. 2): the proof has no requirement on r, hence remains valid for r = 0.
- **Value / termination** (eq. (2.4), p. 2): with [x_I^c, y_I^c]ᵀ the invader's location upon capture,
- **Dominance region** (eq. (2.5), 
[CITATION]
This is the *rigorization* paper for the geometric/barrier solution of target-defense games: it is the natural citation whenever one uses dominance regions (Apollonius circles or Cartesian ovals with non-zero capture radius), "head-to-the-tangency-point" feedback laws, or piecewise value functions for multi-defender target guarding, and needs to claim HJI/viscosity legitimacy rather than intuition. Cite it (a) as the general-case justification covering arbitrary convex targets, non-zero capture 

### P033 — Optimal Strategies and Cooperative Teaming for 3-D Multiplayer Reach-Avoid Games
[BIBLIO]
- ID: P033 / source file: `Gao 等 - 2024 - Optimal Strategies and Cooperative Teaming for 3-D Multiplayer Reach-Avoid Games.pdf` / total pages: 15 (PDF pages 1–15 = printed pp. 2085–2099)
- Title: Optimal Strategies and Cooperative Teaming for 3-D Multiplayer Reach-Avoid Games
- Authors: Peng Gao (Tongji University, Shanghai), Xiuxian Li (Senior Member, IEEE; Tongji University, corresponding author), Jinwen Hu (Northwestern Polytechnical University, Xi'an)
- Year: 2024
- Venue (exact, from running header and copyright line): IEEE Transactions on Cognitive and Developmental Systems, Vol. 16, No. 6, December 2024, pp. 2085–2099. Indexer guess "IEEE Transactions on Cognitive and Developmental Systems" is CORRECT (header of every page; copyright 2379-8920 © 2024 IEEE).
- DOI (printed on p. 1): 10.1109/TCDS.2024.3406889
- Manuscript history (printed, p. 2085): received 5 Feb 2024; revised 4 Apr 2024 and 22 Apr 2024; accepted 24 May 2024; published 3 June 2024; current version 10 Dec 2024. Funding: National Science and Technology Major Project 2022ZD0119702; NSFC Grant U23B2059; Shanghai Mu
[CONTRIBUTIONS]
1. **Theory**: 3-D Apollonius-sphere dominance regions via a barrier function B(s) (eq. (8)); exact value functions and target points for 1P1E (Theorem 1), 2P1E (Theorem 2), 3P1E (Theorem 3) heterogeneous-speed reach-avoid subgames against a plane goal; degeneration analysis showing a pursuit team never needs more than 3 pursuers in 3-D (Remark 4).
2. **Modeling**: decomposition of the MPME game over a plane goal into MPSE subgames with termination set T = T_p ∪ T_e (eqs. (4)–(5)) and terminal payoff Φ = z_E(t_f) (eq. (6)); closed-loop (state-feedback) information structure, contrasted with the open-loop Stackelberg setting of [14] (Remark 3); MPME objective as total capture time W (eq. (34)).
3. **Algorithm**: transformation of MPME task assignment into weighted bipartite matching with ed
[RESULTS-LIST]
- **Dynamics (eq. (1))**: single integrators, ẋ_Pi = u_xi, ẏ_Pi = u_yi, ż_Pi = u_zi; likewise for E_j with controls v_j; controls are 3-D headings (yaw α, β and pitch ψ, γ). Speed constraints (eq. (2)): √(u_xi²+u_yi²+u_zi²) = u_i, √(v_xj²+v_yj²+v_zj²) = v_j. Full state x = (x_{E1}ᵀ,…,x_{EM}ᵀ,x_{P1}ᵀ,…,x_{PN}ᵀ)ᵀ ∈ R^{3M+3N}.
- **Assumption 1 (eq. (3))**: all speeds constant; pursuers keep moving until game end; speed ratio p_ij := u_i/v_j > 1 for EVERY pair (P_i, E_j). Headings may change instantaneously. The authors argue (p. 2087) that maximum-speed motion is optimal even with acceleration dynamics, and that the initial acceleration phase has negligible effect on the terminal interception position — an intuitive claim, not proved.
- **Termination (eqs. (4)–(5))**: T := T_p ∪ T_e with T_p = {x : z_E ≠ 0, ‖x_Pi − x_E‖ = 0 for ∃ i} (capture; point capture) and T_e = {x : z_E = 0, ‖x_Pi − x
[CITATION]
Role in a paper's introduction: this is the natural citation for (a) the 3-D, heterogeneous-speed extension of Apollonius-sphere dominance analysis from one-to-one to many-to-one (2P1E, 3P1E) subgames against a plane goal, with explicit closed-form value functions and target points; (b) the argument that MPME reach-avoid games should be decomposed into value-annotated subgames and re-composed by weighted bipartite matching with online state-feedback rematching, as an alternative to maximum-cardi

### P034 — The Capture-the-Flag Differential Game
[BIBLIO]
- **ID**: P034 / **source file**: `Garcia 等 - 2018 - The Capture-the-Flag Differential Game.pdf` / **total pages**: 6 (printed folios 4167–4172).
- **Title**: The Capture-the-Flag Differential Game.
- **Authors**: Eloy Garcia; David W. Casbeer; Meir Pachter. Affiliations (printed, p. 4167): Garcia and Casbeer — Control Science Center of Excellence, Air Force Research Laboratory, Wright-Patterson AFB, OH 45433 (eloygarcia.2@us.af.mil; david.casbeer@us.af.mil); Pachter — Department of Electrical Engineering, Air Force Institute of Technology, Wright-Patterson AFB, OH 45433 (meir.pachter@afit.edu). Funding (printed footnote): AFOSR LRIR No. 18RQ-COR036.
- **Year**: 2018.
- **Venue (exact, from running header, p. 4167)**: 2018 IEEE Conference on Decision and Control (CDC), Miami Beach, FL, USA, Dec. 17–19, 2018. The indexer guess "IEEE Conference on Decision and Control (CDC)" is **CORRECT**. Copyright line: "U.S. Government work not protected by U.S. copyright". **No DOI printed anywhere** in the document. Page folios 4167–4172 (CDC 2018 proceedings numbering).
- **Tier**: T2 (top contr
[CONTRIBUTIONS]
1. **Theory (Phase I, point capture)**: closed-form state-feedback saddle-point strategies for the Game of Degree in $\mathcal{R}_{D_1}$ (Theorems 1–2): both players aim at the point of the orthogonal bisector of $\overline{AD}$ closest to $F$; Value $V(\mathbf{x}) = \frac{1}{4}(x_A^2+y_A^2-x_D^2-y_D^2)^2/((x_A-x_D)^2+(y_A-y_D)^2)$ (eq. (17)); proof that $V$ is $C^1$ and satisfies the HJI equation (only fully worked proof in the paper).
2. **Theory (Phase II, point capture)**: closed-form feedback strategies and Value for the Game of Degree in $\mathcal{R}_{D_2}$ (Theorems 3–4): the aimpoint is the intersection of the orthogonal bisector of $\overline{AD}$ with the game-set $y$-boundary favored by A; piecewise-defined Value (eq. (25)) that is continuous everywhere and $C^1$ except on the d
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion at unit speed, $\dot{x}_A = \cos\theta_A,\ \dot{y}_A = \sin\theta_A,\ \dot{x}_D = \cos\theta_D,\ \dot{y}_D = \sin\theta_D$, with initial condition $(x_{A_0}, y_{A_0}, x_{D_0}, y_{D_0})$; controls $\theta_A, \theta_D \in [-\pi, \pi]$; state $\mathbf{x} = (x_A, y_A, x_D, y_D) \in \mathbb{R}^4$; $\dot{\mathbf{x}} = f(\mathbf{x}, \mathbf{u}_A, \mathbf{u}_D)$. Full state feedback; **no assumption on the opponent's controller** (p. 4167, 4171).
- **Game set and objects**: $\Omega \subset \mathbb{R}^2$ compact convex; $F$ at $\mathbf{x}_F = (0,0)$ (WLOG); $S = \{(x,y): x \ge x_s\}$ (p. 4168). One Attacker, one Defender; flag radius $r_F \ge 0$, Defender capture radius $r_D \ge 0$.
- **Phase I termination (eqs. (2)–(4))**: $\mathcal{T}_1 = \mathcal{T}_{A_1} \cup \mathcal{T}_{D_1}$, $\mathcal{T}_{A_1} = \{\mathbf{x} \mid \sqrt{x_A^2+y_A^2} = r_F\}$ (A captu
[CITATION]
This is the analytic companion to Huang et al.'s numerical TCST 2015 capture-the-flag differential game and a representative of the AFRL/AFIT school's "closed-form Isaacs solution + HJI verification" template (alongside [8] active defense and [20] target guarding). Cite it (a) as the canonical two-phase CTF differential game with Mayer terminal payoffs and state-feedback saddle-point solutions built on orthogonal-bisector geometry; (b) for the Phase II dispersal-surface example ($\{y_A = y_D\}$)

### P035 — Optimal Strategies for a Class of Multi-Player Reach-Avoid Differential Games in 3D Space
[BIBLIO]
- **ID**: P035
- **Source file**: `D:\System\zhuomian\game-paper\Garcia 等 - 2020 - Optimal Strategies for a Class of Multi-Player Reach-Avoid Differential Games in 3D Space.pdf` (filename in collection truncated to "...in 3.pdf"; true title on p. 1)
- **Total pages**: 8 (printed pp. 4257–4264)
- **Title**: Optimal Strategies for a Class of Multi-Player Reach-Avoid Differential Games in 3D Space
- **Authors**: Eloy Garcia (Senior Member, IEEE), David W. Casbeer (Senior Member, IEEE), Meir Pachter (Fellow, IEEE)
- **Affiliations**: Control Science Center of Excellence, Air Force Research Laboratory, Wright-Patterson AFB, OH (Garcia, Casbeer); Department of Electrical Engineering, Air Force Institute of Technology, Wright-Patterson AFB, OH (Pachter)
- **Year**: 2020 (manuscript received Nov. 27, 2019; accepted Apr. 27, 2020; published May 11, 2020)
- **Venue (EXACT, from running header)**: IEEE Robotics and Automation Letters, vol. 5, no. 3, July 2020, pp. 4257–4264. Indexer guess (RAL) confirmed correct. Associate Editor I. Sa, Editor J. Roberts. "U.S. Government work not protected by 
[CONTRIBUTIONS]
1. **(Theory, Game of Kind)** Explicit Barrier function for the 2P1E target-guarding game in $\mathbb{R}^9$: $B(\mathbf{x}) = \max\{B_1(\mathbf{x}), B_2(\mathbf{x})\}$, $B_i = R_E^2 - R_i^2$ (eq. (21)), partitioning $\mathbb{R}^9$ into pursuer-team winning region $\mathcal{R}_p$ and evader winning region $\mathcal{R}_e$ (eq. (5)).
2. **(Theory, Game of Degree, 1v1 building block)** Theorem 2: closed-form $C^1$ Value $V = \frac{1}{4}(R_E^2-R_1^2)^2/\Gamma^2$ (eq. (13)) with verified HJI solution and straight-line saddle-point strategies (eqs. (14)–(15)) toward the foot of the perpendicular from the origin to the Apollonius bisector plane.
3. **(Theory, Game of Degree, 2v1 simultaneous capture)** Theorem 3: closed-form $C^1$ Value (eq. (22)) whose optimal aimpoint is the point of the *bisect
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 4258)**: single integrators in $\mathbb{R}^3$, $\dot{x}_E = u_x, \dot{y}_E = u_y, \dot{z}_E = u_z$; $\dot{x}_1 = v_x, \dot{y}_1 = v_y, \dot{z}_1 = v_z$; $\dot{x}_2 = w_x, \dot{y}_2 = w_y, \dot{z}_2 = w_z$. Complete state $\mathbf{x} := (\mathbf{x}_E, \mathbf{x}_1, \mathbf{x}_2) \in \mathbb{R}^9$; control set $\mathcal{U} := \{u \in \mathbb{R}^3 \mid \|u\|_2 = 1\}$ with controls $\mathbf{u}$ (E), $\mathbf{v}$ (P1), $\mathbf{w}$ (P2); speeds normalized equal ("Without loss of generality, the speeds have been normalized", p. 4258).
- **Information structure**: full-state feedback; "the players do not know the control implemented by the opponent. Each player only implements the state-feedback optimal strategies" (p. 4264). Non-anticipative (open-loop min–max values are written over feedback strategy classes; eqs. (8), (10)).
- **Termination (eqs. (2)–(4), p. 4258)**
[CITATION]
**Paragraph role.** This is the 3D, equal-speed, two-defender cornerstone of the AFRL "verifiable differential games" line: it is the paper that (i) lifts Garcia–Casbeer–Pachter's 2D target-guarding/active-defense results [19], [22] to $\mathbb{R}^9$ with a complete Game-of-Kind + verified Game-of-Degree solution, (ii) supplies the exact 2P1E barrier $\max\{R_E^2-R_1^2, R_E^2-R_2^2\}$ and the simultaneous-capture Value (22) used later for teaming and task allocation, and (iii) provides the canon

### P036 — The Barrier Surface in the Cooperative Football Differential Game
[BIBLIO]
- ID: P036 / source file: `Garcia 等 - 2020 - The Barrier Surface in the Cooperative Football Differential Game.pdf` / total pages: 5. The PDF text layer was flagged as password-protected by the reader; text was extracted with PyMuPDF and every key equation was visually verified against 200–400 dpi page renders (large math delimiters extract as `\x00`/`\x01` glyphs in the raw text layer).
- Title: *The Barrier Surface in the Cooperative Football Differential Game*. Authors: Eloy Garcia, David W. Casbeer, and Meir Pachter. Year: 2020.
- Venue (EXACT info printed in the PDF): the **only** venue statement is the arXiv margin stamp on p. 1: **"arXiv:2006.03682v1 [math.OC] 5 Jun 2020"**. No conference name, journal, DOI, copyright notice, funding footnote, or received date is printed anywhere in the PDF. The layout is a two-column IEEE-conference-style manuscript (IEEEtran-like), consistent with a submission/preprint, but no venue is printed — treat as arXiv preprint; whether it was later published is `to verify`. No DOI printed.
- Tier: **T2** (as assigned in `manifest.json`). Disagreemen
[CONTRIBUTIONS]
1. **Theory (game of kind)**: complete solution of the game of kind of the cooperative 2P1E football differential game — an explicit Barrier surface $B(\mathbf x)=0$ in $\mathbb R^6$, piecewise defined over segments indexed by the evader's abscissa $x_E$: three segments for equal-speed players (**Theorem 1**, eqs. (7)–(8)) and five segments for faster pursuers with possibly different speeds (**Theorem 2**, eqs. (15)–(17)).
2. **Modeling**: a clean problem statement of the football pursuit-evasion DG (dynamics (2), terminal set (4), non-anticipative perfect-information feedback setting), including the "active pursuer" concept and single vs. simultaneous capture.
3. **Geometric characterization**: closed-form **cross-sections** of the 6-D Barrier surface obtained by fixing the pursuer positi
[RESULTS-LIST]
- **Players and state (eq. (1), p. 1)**: agents $E, P_1, P_2$ with max speeds $v_E, v_1, v_2$; states $\mathbf x_E=(x_E,y_E)$, $\mathbf x_1=(x_1,y_1)$, $\mathbf x_2=(x_2,y_2)$; complete state $\mathbf x := (x_E,y_E,x_1,y_1,x_1,y_1)\in\mathbb R^6$. **Printed typo in eq. (1)** (verified at 400 dpi): the last pair is printed as $(x_1,y_1)$ but must be $(x_2,y_2)$ — eqs. (2)–(3) confirm ($\mathbf x_0 := (x_{E0},y_{E0},x_{10},y_{10},x_{20},y_{20})$).
- **Football setup**: one ball-carrying evader, **no passing**; two pursuers form a team. Game played on $\Omega=\{x,y \mid x\in[0,\bar x],\, y\ge 0\}$; goal line $G=\{(x,y)\in\Omega \mid y=0\}$ (p. 2).
- **Dynamics (eq. (2))**: simple motion, $\dot x_E=v_E\cos\phi$, $\dot y_E=v_E\sin\phi$, $\dot x_1=v_1\cos\psi_1$, $\dot y_1=v_1\sin\psi_1$, $\dot x_2=v_2\cos\psi_2$, $\dot y_2=v_2\sin\psi_2$, with initial conditions and controls $\phi,\psi_1,\psi
[CITATION]
This preprint is the game-of-kind companion to Garcia–Casbeer–Von Moll–Pachter's ACC 2019 blocking-game paper [22]: it completes the football differential game by delivering the explicit Barrier surface that [22] lacked, and it upgrades Yan–Shi–Zhong's analytical-barrier construction [25] from implicit "base curves" to closed-form piecewise-quadratic expressions whose 2-D cross-sections are recognizable conics (circles and hyperbolas), now valid for **heterogeneous** pursuer speeds. In the knowl

### P037 — Multiple Pursuer Multiple Evader Differential Games
[BIBLIO]
- ID: P037 / source file: `Garcia 等 - 2021 - Multiple Pursuer Multiple Evader Differential Games.pdf` / total pages: 6 (journal pp. 2345–2350). PDF text layer was flagged as protected by the reader; extracted with PyMuPDF and all key equations visually verified against 200–500 dpi page renders.
- Title: *Multiple Pursuer Multiple Evader Differential Games*. Authors: Eloy Garcia (Senior Member, IEEE), David W. Casbeer (Senior Member, IEEE), Alexander Von Moll, Meir Pachter. Year: 2021.
- Venue (exact, from running header): **IEEE Transactions on Automatic Control, Vol. 66, No. 5, May 2021, pp. 2345–2350**. Indexer guess (IEEE TAC) is **correct**. DOI printed on p. 2345: **10.1109/TAC.2020.3003840**. Manuscript received Nov. 18, 2019; revised Feb. 21, 2020; accepted June 15, 2020; date of publication June 22, 2020; current version April 26, 2021. Recommended by Associate Editor R. P. Malhamé. Supported in part by AFOSR LRIR 18RQCOR036. "U.S. Government work not protected by U.S. copyright." Affiliations: Garcia, Casbeer, Von Moll — Control Science Center of Excellence, AFRL, Wright-Pat
[CONTRIBUTIONS]
1. **Theory**: Closed-form Value and state-feedback saddle-point strategies for the $N$-vs-$M$ BDDG: $V(\mathbf x)=\max_{\iota} y_{s_\iota}(\mathbf x)$ over feasible assignments $\mathcal A_\iota$, proved (in [35]) to be continuously differentiable except at dispersal surfaces $y_{s_\iota}=y_{s_{\iota'}}$ and to satisfy the HJI equation — the game's hybrid (continuous guidance + discrete assignment) solution is obtained without numerically solving any PDE in $\mathbb R^{2(N+M)}$.
2. **Modeling**: The BDDG formulated as a zero-sum, perfect-information, Mayer-type team game with binary assignment variables $\mu_{ij}$, frozen dynamics after each individual capture time (regularization, p. 2346), and a terminal payoff $\sum_j y_{E_j}(t_f)$ that measures cumulative penetration of the border.
3.
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion for all $2(N{+}M)$ players,
- **State**: $\mathbf x:=(x_{P_i},y_{P_i},x_{E_j},y_{E_j})\in\mathbb R^{2(N+M)}$ (p. 2346, pursuers listed first; note Section III reorders evaders first — minor inconsistency).
- **Termination**: binary assignment $\mu_{ij}=1$ iff $P_i$ is assigned to $E_j$; for every assigned pair the game ends when either $y_{E_j}=0$ (evader reaches the border) or capture ($x_{P_i}=x_{E_j}, y_{P_i}=y_{E_j}$). Terminal set (eq. (2)): $\mathcal T:=\{\mathbf x \mid \forall j\in\{1..M\}\ \exists i\in\{1..N\},\ \mu_{ij}=1,\ x_{P_i}=x_{E_j},\ y_{P_i}=y_{E_j}\}$. $t_f$ = instant the **last** evader is captured; individual terminal times $t_{f_{ij}}$ with $\dot x_{P_i}=\dot y_{P_i}=\dot x_{E_j}=\dot y_{E_j}=0$ for $t\ge t_{f_{ij}}$ (freezing regularization so the game continues until all evaders are captured). Point capture (zero radius).
- *
[CITATION]
This is the flagship "complete closed-form solution" reference for team-vs-team pursuit-evasion with a discrete assignment layer: it is the natural citation whenever an introduction needs to (i) motivate differential-game codesign of weapon-target assignment and guidance, (ii) contrast closed-form Apollonius-based saddle-point solutions against numerical HJI/HJB approximations ([27], [28]) or game-of-kind-only barrier analyses ([33]), or (iii) anchor the border-defense/reach-avoid line of Garcia

### P038 — The Capture-the-Flag Differential Game: Attack, Transition and Retreat
[BIBLIO]
- **ID**: P038
- **Source file**: `D:\System\zhuomian\game-paper\Garcia和Casbeer - 2025 - The Capture-the-Flag Differential Game Attack, Transition and Retreat.pdf` (17 PDF pages; printed journal pages 271–287; PDF p.1 = j.p. 271, ..., PDF p.17 = j.p. 287). Page references below use the printed journal page numbers.
- **Title**: The Capture-the-Flag Differential Game: Attack, Transition and Retreat
- **Authors**: Eloy Garcia (Senior Member, IEEE), David W. Casbeer (Senior Member, IEEE); affiliation line: "Control Theory Fundamentals of Multi-Agent Systems" (AFRL-class lab byline; no institution printed).
- **Year**: 2025. Printed chronology: Received 29 April 2025; revised 18 July 2025; accepted 10 August 2025; Date of publication 14 August 2025; date of current version 8 September 2025. Recommended by Guest Editor S. Martinez. License: CC BY 4.0.
- **Venue (resolved from header, exact)**: *IEEE Open Journal of Control Systems* (IEEE CSS), Volume 4, 2025, pp. 271–287. The indexer guess "IEEE/CAA JAS or IEEE Open Journal" is resolved: it is the IEEE Open Journal of Control Systems (OJ-
[CONTRIBUTIONS]
1. **Theory (Game of Degree, Phase I)**: closed-form state-feedback saddle-point strategies (16), optimal interception point (17), and $C^1$ Value function (18) for the Attack phase in $\mathcal{R}_{D1}$, with a rigorous verification proof (continuity, continuous differentiability, HJI satisfaction), including the constrained/boundary solution when the unconstrained aimpoint leaves $\Omega$ (eqs. (25)–(32), p. 276).
2. **Theory (Game of Degree, Phase II)**: closed-form feedback strategies (33) and piecewise Value (34) for the Retreat phase in $\mathcal{R}_{D2}$, continuous everywhere and $C^1$ except on a dispersal surface $\mathcal{D} = \{\mathbf{x} \mid y_A = y_D\}$, with HJI verification (pp. 277–279).
3. **Modeling novelty (Transition Phase, Section IV)**: formulation of D's inter-phas
[RESULTS-LIST]
- **Statement**: For $x \in \mathcal{R}_{D1}$, headings of A and D are constant under optimal play; optimal trajectories are straight lines.
- **Assumptions**: dynamics (1); $x \in \mathcal{R}_{D1}$ so termination is by (4).
- **Proof approach** (4 steps): (i) Isaacs' Main Equation 1, $\min_{\theta_A}\max_{\theta_D} H = 0$; (ii) stationarity $\partial H/\partial\theta = 0$ gives $\cos\theta_A^* = -\lambda_{x_A}/\sqrt{\lambda_{x_A}^2+\lambda_{y_A}^2}$, $\sin\theta_A^* = -\lambda_{y_A}/\sqrt{\lambda_{x_A}^2+\lambda_{y_A}^2}$ (9) and $\cos\theta_D^* = \lambda_{x_D}/\sqrt{\lambda_{x_D}^2+\lambda_{y_D}^2}$, $\sin\theta_D^* = \lambda_{y_D}/\sqrt{\lambda_{x_D}^2+\lambda_{y_D}^2}$ (10); (iii) costate dynamics $\dot{\lambda} = -\partial H/\partial x$ give $\dot{\lambda}_{x_A} = \dot{\lambda}_{y_A} = \dot{\lambda}_{x_D} = \dot{\lambda}_{y_D} = 0$ (H has no state dependence); (iv) constant costates
[CITATION]
This is the definitive closed-form treatment of the two-player capture-the-flag differential game and the natural journal-citation anchor for the "attack–transition–retreat" phase structure: it contributes (i) OBS-foot aimpoint Values with full HJI verification for both phases, (ii) the inter-phase transition concept — D concedes a lost Phase I and optimizes its Phase II entry state, with the transition optimum shown to continue straight into the Phase II aimpoint (hyperbola condition (57)) — an

### P039 — A Differential Game Approach to Planning in Adversarial Scenarios: A Case Study on Capture-the-Flag
[BIBLIO]
- **ID**: P039
- **Source file**: `D:\System\zhuomian\game-paper\Huang 等 - 2011 - A differential game approach to planning in adversarial scenarios A case study on capture-the-flag.pdf` (6 PDF pages = printed conference pages 1451–1456; PDF p.1 = p.1451, ..., PDF p.6 = p.1456). Page references below use the printed page numbers. NOTE: the Read tool flags this PDF as password-protected; text was extracted with PyMuPDF and every formula/figure was visually verified against 200-dpi page renders.
- **Title**: A Differential Game Approach to Planning in Adversarial Scenarios: A Case Study on Capture-the-Flag (full title confirmed from p. 1451 header; the truncated filename "…on c" resolves to "…on capture-the-flag").
- **Authors**: Haomiao Huang (Dept. of Aeronautics and Astronautics, Stanford University, haomiao@stanford.edu); Jerry Ding, Wei Zhang, and Claire J. Tomlin (Dept. of Electrical Engineering and Computer Sciences, UC Berkeley). Footnote: "These authors contributed equally to this work" (marked on Huang, Ding, Zhang).
- **Year**: 2011 (conference held May 9–13, 2011).
- **Venue
[CONTRIBUTIONS]
1. **Modeling**: first formulation of two-player CTF as a two-phase zero-sum differential game with simple motion, equal speed caps, capture radius, and rule-based state constraints (defender excluded from $\mathcal{F}\cup\mathcal{R}\cup\mathcal{D}^C$), with game rules encoded *as winning conditions for the opponent* rather than as hard state constraints (Sec. II p. 1452; Sec. III-B p. 1453).
2. **Theory (set characterization)**: characterization of the attacker's flag-return set $R_A$, flag-capture set $F_A$, and overall winning set $W_A$ as reach-avoid sets computed from a constrained HJI PDE (eqs. (3)–(5), p. 1454), including the sequential-composition device $\tilde{R}_A = \mathcal{G}_F\cap R_A$ that stitches the two phases; defender sets by complement ($F_D=\hat{\mathcal{D}}\setminus 
[RESULTS-LIST]
- **State**: joint configuration $x=(x^a,x^d)\in\mathbb{R}^4$; permissible set $\hat{\mathcal{D}}=\mathcal{D}\times\mathcal{D}\setminus(\mathcal{F}\cup\mathcal{R})\subset\mathbb{R}^4$. (Notational caveat: as literally printed the set-difference scope is ambiguous; the intended meaning, from "the defender is constrained to remain outside of the flag and return regions, while the attacker can move freely through either" (p. 1452), is $\hat{\mathcal{D}}=\{(x^a,x^d)\in\mathcal{D}\times\mathcal{D}: x^d\notin\mathcal{F}\cup\mathcal{R}\}$.)
- **Dynamics**: $\dot{x}^a=u$, $\dot{x}^d=d$ with $\|u\|_2\le V_{a,\max}$, $\|d\|_2\le V_{d,\max}$, and $V_{a,\max}=V_{d,\max}$ "for fairness" (p. 1452) — i.e., unit-speed simple motion after normalization. No obstacles in the base formulation; obstacles/geometry enter only through the constraint-encoding sets (Sec. 5.3).
- **Capture region** (unnumbered, p.
[CITATION]
This is the **founding paper of the differential-game treatment of capture-the-flag**: it fixed the now-standard two-phase decomposition (flag capture → flag return), the constraint-encoding trick (a player's rule violation is the opponent's winning condition, reusable for obstacles), and the sequential-composition device $\tilde{R}_A=\mathcal{G}_F\cap R_A$ (eq. (5)) by which HJI reach-avoid sets handle games with staged objectives — a device that later reappears, in closed form, as the "transit

### P040 — Automation-Assisted Capture-the-Flag: A Differential Game Approach
[BIBLIO]
- **ID**: P040
- **Source file**: `D:\System\zhuomian\game-paper\Huang 等 - 2015 - Automation-Assisted Capture-the-Flag A Differential Game Approach.pdf` (15 PDF pages; printed journal pages 1014–1028; PDF p.1 = j.p. 1014, ..., PDF p.15 = j.p. 1028). Page references below use the printed journal page numbers (PDF page = printed − 1013).
- **Title**: Automation-Assisted Capture-the-Flag: A Differential Game Approach
- **Authors**: Haomiao Huang (Kuna Systems Corporation, Millbrae, CA), Jerry Ding (United Technologies Research Center, East Hartford, CT; work done at UC Berkeley), Wei Zhang (Dept. of Electrical and Computer Engineering, Ohio State University, Columbus, OH), Claire J. Tomlin (Dept. of Electrical Engineering and Computer Sciences, UC Berkeley). Acknowledgment (p. 1027): "H. Huang, J. Ding, and W. Zhang contributed equally to this work."
- **Year**: 2015. Printed chronology (p. 1014): Manuscript received April 17, 2014; accepted September 20, 2014; Date of publication October 14, 2014; date of current version April 14, 2015. Manuscript received in final form September 23, 2
[CONTRIBUTIONS]
1. **Theory (game-of-kind formulation of reach–avoid, Section IV)**: formal Elliott–Kalton nonanticipating-strategy formulation of the finite-horizon reach–avoid game (2)–(6); equivalent constrained terminal-cost minimax (7)–(11) via the time-dilation augmentation trick; characterization of the upper value as the constrained viscosity solution of the HJI equation (12)–(13), with $J^{\bar{}}_T(x^0) = \phi(x^0,-T)$ (15) "by slight modifications of the proof techniques in [20]" (Evans–Souganidis representation formulas); Isaacs condition (16) guarantees existence of value.
2. **Modeling (two-stage CTF composition, Section V)**: encoding of all CTF rule violations into reach–avoid target/undesired sets ($G_A$, $G_D$ fold "attacker leaves $\Omega$" and "defender enters $F\cup R\cup\Omega^C$" in
[RESULTS-LIST]
- **Result (12)–(15) (representation of the upper value; the closest thing to a theorem in the paper, stated with attribution)**: let $\phi : \mathbb{R}^n \times [-T,0] \to \mathbb{R}$ be the *viscosity solution* [26] of the constrained terminal-value HJI equation
- **Assumptions**: bounded Lipschitz $\phi_T,\phi_K$; compact input sets; nonanticipating strategies; the result is claimed "by the results detailed in [17] and [25]" and "by slight modifications of the proof techniques in [20]" — i.e., proof approach (as attributed, 4 steps): (i) dynamic programming: the terminal-cost game over $[0,T]$ satisfies the semigroup property; (ii) the constrained problem is handled by projecting the value above the obstacle $-\phi_K$ (13) (the constraint $\phi_K(\tilde x(t)) > 0$ becomes a reflected/obstacle-type boundary condition); (iii) Evans–Souganidis-style representation formulas for viscosity 
[CITATION]
Role in a future Introduction/Related Work: this is the **foundational numerical-HJI reference for capture-the-flag and multistage reach–avoid games** — the paper to cite (i) when motivating differential-game (worst-case-guarantee) treatment of multiobjective adversarial planning against assumption-laden MPC/geometric methods, (ii) when introducing the reach–avoid HJI/level-set machinery and its winning-region/feedback-strategy outputs, and (iii) whenever human-in-the-loop or automation-assisted

### P041 — Dominance regions of pursuit-evasion games in non-anticipative information patterns
[BIBLIO]
- **ID**: P041 / source file: `Huang 等 - 2025 - Dominance regions of pursuit-evasion games in non-anticipative information patterns.pdf` / total pages: **14** (pp. 1–12 main text + 2 pages of references and author biographies).
- **Title**: Dominance regions of pursuit-evasion games in non-anticipative information patterns.
- **Authors**: Weiwen Huang (School of Mathematics and Statistics, Beijing Institute of Technology; National Key Lab of Autonomous Intelligent Unmanned Systems), Li Liang (College of Information Science and Technology, Beijing University of Chemical Technology), Ningsheng Xu (School of Automation, BIT), Fang Deng (corresponding author, School of Automation, BIT; National Key Lab of Autonomous Intelligent Unmanned Systems).
- **Year / Venue**: 2025, **Automatica**, Volume 176, Article 112258 (header exactly: "Automatica 176 (2025) 112258"; Elsevier; ISSN 0005-1098 printed in the copyright line). DOI printed on p. 1: `10.1016/j.automatica.2025.112258`. Article history printed: Received 3 November 2023; revised 1 August 2024; accepted 8 February 2025; Associate Edito
[CONTRIBUTIONS]
1. **Theory (definition + rigorous reachability proof)**: the evader's dominance region is defined by the shortest path distance $d_L$, and it is rigorously proved for the first time (per the authors) that the initial dominance region equals the evader's reachable region in the open-loop sense — Theorem 4 (no obstacles) and Theorem 5 (obstacles, $l=0$), with supporting Lemma 6.
2. **Theory (non-anticipative confinement, obstacle-free)**: existence of a PELIDR non-anticipative strategy without obstacles (Theorem 7), with an explicit uniform capture-time bound and a monotone containment of the moving dominance region inside the initial one; built on an angular comparison Lemma 8 on first-type Cartesian ovals. Remark 9 extends part (b) to convex domains.
3. **Theory (obstacles, negative + nec
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 3)**: $\dot{x}_p(t) = \alpha u_p(t)$, $\dot{x}_e(t) = u_e(t)$, $x_p(t_0)=x_{p0}$, $x_e(t_0)=x_{e0}$; controls take values in $\partial B_2(0,1)$; admissible control sets $\mathcal{U}^p_{t_0}(x_{p0}), \mathcal{U}^e_{t_0}(x_{e_0}) \subseteq \mathcal{U}_{t_0} \triangleq \{u : [t_0,+\infty) \to \partial B_2(0,1) : u \text{ piecewise continuous}\}$, restricted so that players never enter $\mathbb{R}^2\setminus X$. Trajectories are continuous, piecewise smooth; sudden direction changes allowed.
- **Termination (p. 3)**: terminal set $\mathcal{T} = \{(x_p,x_e) : \|x_p - x_e\| \le l\}$; terminal time $t_f(t_0,x_0,u_p,u_e) = \inf\{t : x(t;t_0,x_0,u_p,u_e) \in \mathcal{T}\}$ (eq. (2)); $\inf\emptyset = +\infty$ ($t_f=+\infty$ means no capture).
- **Information structure (Definition 1, p. 4, eq. (3))**: a pursuer strategy is a map $\delta : \mathcal{U}^e_{t_0}(x_{e_0}) \to
[CITATION]
This paper is the foundational reference for **dominance-region-based geometric methods under a non-anticipative (Elliott–Kalton) information pattern in obstacle environments**. It occupies a unique niche: it (i) rigorously justifies the long-assumed identity between the evader's shortest-path dominance region and its open-loop reachable region (Theorems 4–5), (ii) proves that the classical "aim at the exit point" strategy is a valid non-anticipative PELIDR strategy without obstacles with the Ap

### P044 — An Introduction to Pursuit-evasion Differential Games
[BIBLIO]
- **ID**: P044. **Source file**: `D:\System\zhuomian\game-paper\Isaac E. 等 - 2020 - An Introduction to Pursuit-evasion Differential Games.pdf`. **Total pages**: 18 (PDF), printed pp. 1049–1066. (Note: the PDF is flagged as password-protected by the reader tool but opens normally; text extracted with PyMuPDF and all formulas verified against 200-dpi page renders.)
- **Title**: An Introduction to Pursuit-evasion Differential Games.
- **Authors**: Isaac E. Weintraub (Aerospace Systems Directorate, Air Force Research Laboratory, Wright-Patterson AFB, OH 45433); Meir Pachter (Dept. of Electrical Engineering, Air Force Institute of Technology, Wright-Patterson AFB, OH); Eloy Garcia (Control Science Center of Excellence, Air Force Research Laboratory, Wright-Patterson AFB, OH).
- **Year**: 2020. **Venue (as printed in footer, p. 1049)**: "2020 American Control Conference, Denver, CO, USA, July 1-3, 2020", copyright line "978-1-5386-8266-1/$31.00 ©2020 AACC". Indexer guess "American Control Conference (ACC)" is **correct** (also confirmed by PDF metadata subject field "2020 American Control 
[CONTRIBUTIONS]
1. **Taxonomy of PE differential games by player count** (1v1, Nv1, 1vM, NvM) with ~90 classified references and one-line problem statements per entry (pp. 1050–1053); canonical descriptions of the Homicidal Chauffeur (Isaacs [3]; definitive solution Merz [20], introducing "switch envelope" and "focal line" singular lines) and the Two Cars game (Meier [22]; Getz–Pachter [23], [24]; Greenfeld [25]; Lewin–Breakwell [26]; Bera et al. [27]).
2. **Pedagogical statement of the HJI verification theorem** (Theorem 1, cited to Hespanha [88]) and an explicit demonstration of the "verify-the-Value" workflow as opposed to synthesis (p. 1054).
3. **Complete solution + full verification proof of the Two-Pursuer-One-Evader Differential Game (2P1EDG, "two cutters and fugitive ship")**: state-feedback sadd
[RESULTS-LIST]
**Theorem 1 (p. 1054, eq. (3); cited to [88] — Hespanha's book).** Assume there exists a C¹ function `V(t, x(t))` satisfying the HJI PDE
**Proposition 1 (p. 1056, eq. (21)) — state-feedback solution of the 2P1EDG (4)–(6) with `beta_1 > 1`, `beta_2 > 1`.**
**Theorem 2 (p. 1057) — verification.** For the 2P1EDG (4)–(6) with the solution of Proposition 1 and Value (22): the Value function is continuous and continuously differentiable over `R` and satisfies the HJI equation for any `x ∈ R`. Proof (pp. 1057–1058), the paper's centerpiece:
**Theorem 3 (p. 1062) — Game of Degree in the escape region, via "two-sided" PMP.** Parameter `0 <= alpha < 1`; reduced state `(x_A, x_T, y_T)`, `x_A > 0`, `y_T >= 0`. In the part of the state space where T can escape, the optimal state-feedback headings are
[CITATION]
**Paragraph role.** This is the field's modern "front-door" citation: a peer-reviewed (ACC 2020) tutorial by three of the most prolific AFRL/AFIT PE-game researchers that (i) canonizes the taxonomy 1v1 / Nv1 / 1vM / NvM used in much of the subsequent multi-player PE literature, (ii) condenses the Isaacs→Bellman→Breakwell→Pontryagin lineage and the Homicidal Chauffeur/Two Cars classics into two paragraphs, and (iii) provides fully worked, verified templates of the two standard solution toolchains

### P045 — Anonymous Hedonic Game for Task Allocation in a Large-Scale Multiple Agent System
[BIBLIO]
- **ID / source file / total pages**: P045 / `D:\System\zhuomian\game-paper\Jang 等 - 2018 - Anonymous Hedonic Game for Task Allocation in a Large-Scale Multiple Agent System.pdf` / 15 PDF pages = printed pp. 1534–1548 (printed page = PDF page + 1533). Note: the Read tool flags this PDF as password-protected; text and 200-dpi page images were extracted with PyMuPDF (file itself opens without a password, `needs_pass=0`).
- **Title**: Anonymous Hedonic Game for Task Allocation in a Large-Scale Multiple Agent System
- **Authors**: Inmo Jang, Hyo-Sang Shin, Antonios Tsourdos (Centre for Autonomous and Cyber-Physical Systems, Cranfield University, Bedford, U.K.; corresponding author: Hyo-Sang Shin)
- **Year / Venue**: 2018, **IEEE Transactions on Robotics**, vol. 34, no. 6, pp. 1534–1548, December 2018 (issue header printed on every page; indexer guess T-RO is **correct**). Manuscript received Dec. 12, 2017; revised Apr. 6, 2018; accepted May 22, 2018; published online Aug. 20, 2018. Associate Editor N. Agmon; Editor T. Murphey. ISSN 1552-3098. **DOI (printed)**: 10.1109/TRO.2018.2858292. 
[CONTRIBUTIONS]
1. **Theory (convergence)**: Identification of *single-peaked-at-one* (SPAO) preferences (Definition 4, p. 1537) — i.e., social inhibition — as the condition under which a Nash stable partition always exists (Theorem 1) and is reachable in at most $|A|(|A|+1)/2$ iterations (Theorem 2), improving the iteration count of [44] from $O(n_a^2 n_t)$ to $O(n_a^2)$ (under a fully connected network; $O(d_G n_a^2)$ time steps under a strongly connected network of diameter $d_G$).
2. **Algorithm (decentralization/asynchrony)**: Algorithm 1 (per-agent greedy decision loop) + Algorithm 2 (`D-Mutex`), a distributed mutex subroutine that selects a unique "valid partition" via lexicographic tie-breaking on (iteration count $r_i$, random time stamp $s_i$), making Theorems 1–2 hold under any strongly connect
[RESULTS-LIST]
- **Decisive quantity**: eq. (4) (the slack $\Delta_\Pi(i)$), and the "slack ≥ 1 after deviation" mechanism.
- **Local/global**: local reasoning per coalition; the bound is a worst-case *analytic* count.
- **Physical meaning**: one arrival disturbs at most the coalition it joins; social inhibition makes the disturbance "daisy-chain" die out because each re-arranged agent gains one unit of tolerance.
- **Extensibility**: this lemma is the engine of Theorems 1–2 *and* of the adaptability claim (Sec. IV-C): any environmental change reduces to a sequence of "new agent joins".
- **proof gap (minor, p. 1538)**: the counting step "at most $|\tilde{A}|$ iterations" is asserted from the immunity remark ("an agent who deviates to a coalition and expels one of the existing agents in that coalition will not deviate again even if another agent joins the coalition in a next iteration"). The immunity c
[CITATION]
**Paragraph role**: P045 is the foundational reference for *hedonic-game-based decentralized task allocation* in multi-robot systems: it imports Darmann's anonymous hedonic games with social inhibition into swarm robotics, converts a global ST-MR assignment problem into a Nash-stability-seeking coalition game, and delivers the full package (existence, polynomial convergence, computable and fixed approximation bounds, asynchronous decentralized implementation) that top-down and bottom-up swarm me

### P046 — Safety-Aware Pursuit-Evasion Game Based on Control Barrier Function and Reinforcement Learning
[BIBLIO]
- **ID**: P046
- **Source file**: `D:\System\zhuomian\game-paper\Jia 等 - 2025 - Safety-Aware Pursuit-Evasion Game Based on Control Barrier Function and Reinforcement Learning.pdf`
- **Total pages**: 11 (printed pp. 5440–5450)
- **Title**: Safety-Aware Pursuit-Evasion Game Based on Control Barrier Function and Reinforcement Learning
- **Authors**: Yupeng Jia, Xiran Cui, Yi Dong (Member, IEEE), Xiaoming Hu (Senior Member, IEEE). Jia, Cui, Dong: College of Electronic and Information Engineering, Shanghai Research Institute for Intelligent Autonomous Systems, Tongji University, Shanghai, China (corresponding author: Yi Dong). Hu: Optimization and Systems Theory, Royal Institute of Technology (KTH), Stockholm, Sweden.
- **Year/Venue**: 2025. Printed header: "IEEE Transactions on Systems, Man, and Cybernetics: Systems, Vol. 55, No. 8, August 2025" — indexer guess confirmed; this is the **Systems** member of the SMC family (ISSN 2168-2216 printed in the copyright line). Received 16 Jan 2025, accepted 26 Feb 2025, published 10 Jun 2025; Associate Editor L. Liu.
- **DOI** (printed): 10.1109/T
[CONTRIBUTIONS]
1. **Theory (safety layer)**: A safeguarding control u_j^s(x_j) = −c_j B^T∇B_j(x_j) (6) built on a reciprocal-form CBF B_j = b_j² (7) satisfying (8), with a feasibility condition (9) (a relaxation of the third condition of [34, Assumption 1], Cohen & Belta); Lemma 1 proves forward invariance of Int(C_j) whenever the nominal strategy u_j^n(x) is bounded — no QP, no model of A needed, B only.
2. **Theory (bounded game strategies + capture)**: A new nonquadratic game cost (13) with tanh^{-1}-integral effort terms (Abu-Khalaf–Lewis-type saturating cost) whose saddle-point solution (14)–(16) is *bounded by construction* (|u_j^{n*}| < λ_j), making it seamlessly compatible with Lemma 1; Theorem 1 gives a sufficient condition (29) under which the closed loop (4) remains asymptotically stable despi
[RESULTS-LIST]
- **Dynamics**: (1), (2), identical (A, B); A unknown to both players, B known (B enters (6), (16), (22), (25) — see §7). Error dynamics (4).
- **Information structure**: nominal strategies are functions of the relative state x only, u_j^n(x); safeguarding controls are functions of each player's own absolute state x_j; so each player needs its own position and the relative position — decentralized in the safety channel, centralized-in-x in the game channel.
- **Cost (13, p. 5442)**: V(x) = ∫_0^∞ [x^T(τ)Qx(τ) + J(u_p, u_e)] dτ, with
- **Game value and HJI**: V*(x) = min_{u_p} max_{u_e} V(x) (14); Hamiltonian H(x, ∇V, u_p, u_e) = x^TQx + J + ∇V^T(Ax + Bu_p − Bu_e) (15); HJI: H(x, ∇V*, u_p^{n*}, u_e^{n*}) = 0 with V*(0) = 0 (17).
- **Saddle-point strategies (16, p. 5443)**: u_j^{n*}(x) = −λ_j tanh( (1/(2λ_j)) R_j^{-1} B^T∇V*(x) ), j ∈ {p, e} — obtained from ∂H/∂u_j = 0. Note both players' o
[CITATION]
This paper is the reference point for the *architecture* "CBF safeguarding layer + off-policy ADP game solver" for two-player PE with state constraints under unknown drift: cite it (i) as evidence that safety layers and learning-based game strategies can be composed so that invariance holds throughout learning (Lemma 1 needs only boundedness of the game strategy, which tanh-based costs supply), (ii) for the nonquadratic tanh^{-1} game cost (13) that yields inherently bounded saddle-point strateg

### P047 — Reach-Avoid Differential Games via Finite-Time Heading Tracking
[BIBLIO]
- **ID**: P047
- **Source file**: `D:\System\zhuomian\game-paper\Lai 等 - 2021 - Reach-Avoid Differential Games via Finite-Time Heading Tracking.pdf`
- **Total pages**: 7 (printed pp. 1656–1662)
- **Title**: Reach-Avoid Differential Games via Finite-Time Heading Tracking
- **Authors**: Haowen Lai, Rui Yan, Weixian Zhang, Zongying Shi, Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, China (emails printed: {lhw19,yr15,wx-zhang17}@mails.tsinghua.edu.cn; {szy,zys-dau}@mail.tsinghua.edu.cn). Funding printed: "supported by the Guoqiang Research Institute of Tsinghua University."
- **Year/Venue**: 2021. Printed on p. 1656: "2021 60th IEEE Conference on Decision and Control (CDC), December 13-15, 2021. Austin, Texas" — indexer guess (CDC) **confirmed**; this is the 60th CDC.
- **DOI** (printed in footer): 10.1109/CDC45484.2021.9683266; ISBN printed: 978-1-6654-3659-5/21/$31.00 ©2021 IEEE.
- **Tier**: T2 (top-tier control conference). No disagreement.
- **BibTeX** (from printed metadata only):
```bibtex
@inproceedings{Lai2021reachavoid,
  author    = {Lai, Haowen
[CONTRIBUTIONS]
1. **Modeling/approach (theory)**: A decomposition method for reach-avoid games with a car-model defender: (i) heading-reference design by pretending the defender has simple motion and applying the ES-based feedback strategy (4)–(5) inherited from [13]; (ii) a finite-time controller that forces the car defender's heading onto the reference. Lemma 1 gives the heading reference in closed form (6).
2. **Theory (tracking-time analysis)**: A "gradient-based method" that yields (a) the exact gradient of the heading reference w.r.t. the relative position (Lemma 2, eq. (12)), (b) the pointwise worst-case bound |θ̇_D^r(x_{D,A})| ≤ φ(x_{D,A}) over all attacker/defender controls (Lemma 3, eq. (13)), (c) a global uniform bound ϑ = α(v_A+v_D)/(r(α−1)) (Theorem 1, eq. (14)), and (d) a finite tracking ti
[RESULTS-LIST]
- **Defender (car model) (1, p. 1656)**: ẋ_D = v_D cos θ_D, ẏ_D = v_D sin θ_D, θ̇_D = u_D, with initial conditions x_D(0) = x_{D0}, θ_D(0) = θ_{D0}; v_D > 0 constant, u_D ∈ R, |u_D| ≤ u_MD. This is a Dubins-type vehicle (constant speed, bounded angular rate).
- **Attacker (simple motion) (2, p. 1657)**: ẋ_A = v_A cos θ_A, ẏ_A = v_A sin θ_A, x_A(0) = x_{A0}; control u_A = (cos θ_A, sin θ_A)^⊤, θ_A ∈ [0, 2π) (the printed text has a typo "θ ∈ [0,2π)").
- **Winning/termination**: attacker wins iff it reaches Ω_goal from Ω_play with ‖x_A − x_D‖₂ > r throughout; defender wins iff capture ‖x_A − x_D‖₂ ≤ r occurs in Ω_play (p. 1657). No value function, HJI equation, or barrier is computed for the *car* game — the paper's analytic machinery is entirely about reference generation and tracking.
- **Information structure**: the defender's strategy is full-state feedback requiring (x_D, θ_D, x_A); th
[CITATION]
**Paragraph role**: This is the bridge paper between the analytic simple-motion reach-avoid literature (Yan et al.'s ES-based/barrier strategies [9], [13], which the skill's library holds as P-series entries) and physically deployable nonholonomic defenders. Its reusable assets are: (i) the closed-form heading reference (6) obtained by differentiating the ES/Apollonius pursuit law, with the geometric picture of equal-heading rays in relative-position space; (ii) the gradient-based worst-case der

### P048 — Guarding a Target Area from a Heterogeneous Group of Cooperative Attackers
[BIBLIO]
- **ID**: P048
- **Source file**: `D:\System\zhuomian\game-paper\Lee 等 - 2024 - Guarding a Target Area from a Heterogeneous Group of Cooperative Attackers.pdf`
- **Total pages**: 6 (printed pp. 233–238)
- **Title**: Guarding a Target Area from a Heterogeneous Group of Cooperative Attackers
- **Authors**: Yoonjae Lee and Efstathios Bakolas — Department of Aerospace Engineering and Engineering Mechanics, The University of Texas at Austin, Austin, Texas 78712-1221, USA (yol033@utexas.edu; bakolas@austin.utexas.edu); Goutam Das and Daigo Shishika — College of Engineering and Computing, George Mason University, Fairfax, VA 22033, USA (gdas@gmu.edu; dshishik@gmu.edu).
- **Year/Venue**: 2024. Printed on p. 233: "2024 American Control Conference (ACC), July 8-12, 2024. Toronto, Canada" — indexer guess (ACC / ICUAS) **resolved: ACC** (not ICUAS), confirmed from the running header and the copyright line.
- **Copyright line (printed)**: "979-8-3503-8265-5/$31.00 ©2024 AACC" (ACC 2024 proceedings ISBN 979-8-3503-8265-5). **No DOI printed** anywhere in the PDF.
- **Tier**: T2 (top-tier control co
[CONTRIBUTIONS]
1. **Modeling**: A one-defender-vs-$m$-attacker target-guarding game in $\mathbb{R}^n$ with a general convex target (1), simple-motion kinematics (2), heterogeneous speed ratios $\nu_i \in (0,1)$ and heterogeneous importance weights $\theta_i > 0$, $\sum_i \theta_i = 1$ entering a **team** (cooperative) performance index (3) minimized by the attacker team and maximized by the defender; sequential capture with exogenous capture order (index = capture order).
2. **Theory (main result, Theorem 2)**: At any state $x \in \mathcal{X}$ (19) for which a local minimizer of the stacked capture-point problem (P) satisfies the Second-Order Sufficient Condition (SOSC), the global optimal value $V$ of (P) is $C^1$ and satisfies the Isaacs equation (21) **in the classical sense** — hence it *is* the Valu
[RESULTS-LIST]
- **Target set (1, p. 234)**: $\mathcal{T} = \{x \in \mathbb{R}^n : h(x) \le 0\}$, where $h: \mathbb{R}^n \to \mathbb{R}$ is twice continuously differentiable and convex; its value indicates the level of proximity to $\mathcal{T}$; example $h(x) = \|x\|^2 - r^2$, $r \ge 0$. (For the disk of radius 2 in Section V: $h(x) = \|x\|_2^2 - 4$; note $h$ is *smaller* = *closer* to $\mathcal{T}$, $h = 0$ on $\partial\mathcal{T}$, and cost minimization by A means getting close.)
- **Kinematics (2a)–(2b, p. 234)**: $\dot{x}_{A_i} = \nu_i u_i$, $x_{A_i}(t_0) = x^0_{A_i}$, $i \in [m]$; $\dot{x}_D = v$, $x_D(t_0) = x^0_D$; controls $u_i, v \in \mathcal{U} = \{\xi \in \mathbb{R}^n : \|\xi\| \le 1\}$; speed ratios $\nu_i \in (0,1)$; "D moves with unitary speed and is faster than all attackers."
- **Information structure (p. 234)**: feedback (perfect state) information pattern; both teams measure the glob
[CITATION]
**Role in a paper**: cite P048 as the reference for **one-defender-vs-many target guarding against a heterogeneous, cooperative attacker team with importance weights**, and as a methodological exemplar of *certifying geometric reach-avoid strategies via parametric nonlinear-programming sensitivity* (Fiacco-type SOSC ⇒ classical Isaacs-equation verification) rather than HJI/viscosity computation. It sits between the noncooperative 1-vs-many line ([25], [26]) and the two-cooperative-attacker singu

### P049 — Two-Player Reconnaissance Game with Half-Planar Target and Retreat Regions
[BIBLIO]
- **ID**: P049
- **Source file**: `D:\System\zhuomian\game-paper\Lee和Bakolas - 2023 - Two-Player Reconnaissance Game with Half-Planar Target and Retreat Regions.pdf` — 6 PDF pages; printed page numbers 3344–3349 (offset: printed = PDF page + 3343). Note: the Read tool reports this PDF as "password-protected", but PyMuPDF opens it unencrypted (`is_encrypted = False`); full per-page text extraction + 200/300-dpi page renders were used, and every equation below was verified against the rendered images.
- **Title** (p. 1): Two-Player Reconnaissance Game with Half-Planar Target and Retreat Regions
- **Authors**: Yoonjae Lee (PhD student) and Efstathios Bakolas (Associate Professor), Department of Aerospace Engineering and Engineering Mechanics, The University of Texas at Austin, Austin, Texas 78712-1221, USA (p. 1 footnote; emails yol033@utexas.edu, bakolas@austin.utexas.edu).
- **Year**: 2023.
- **Venue (EXACT from p. 1 header)**: "**IEEE Control Systems Letters paper presented at 2023 American Control Conference (ACC)**, San Diego, CA, USA. May 31 - June 2, 2023"; copyright line "979-8-
[CONTRIBUTIONS]
1. **Theory**: (a) *Theorem 1* (p. 3, eqs. (14)–(19)): closed-form Value $V_{II}$ and feedback equilibrium of the Phase-II retreat game via a max-over-half-plane of the $\Delta$ function (adopted from [5], [10], [11]); (b) *Theorem 2* (p. 5, eqs. (53)–(56)): closed-form Value $V_I$ and state-feedback equilibrium strategies of the Phase-I approach game, **verified against the HJI equation** (eqs. (57)–(59)) — a step "absent in [20]" (p. 1).
2. **Modeling**: Formulation of the reconnaissance game with disjoint half-planar $\mathcal T$ and $\mathcal R$ (eqs. (1)–(12)); decomposition into Phase I (approach, payoff $J_I=l-y_I^s$, eq. (23)) and Phase II (retreat, terminal-separation payoff $J_{II}$, eq. (13)) based on the Intruder's myopic goal, with the coupling encoded in a parameterized termi
[RESULTS-LIST]
- **Dynamics** (eqs. (1)–(5)): simple motion; $\dot x_I=\cos\phi,\ \dot y_I=\sin\phi$, $\phi\in[-\pi,\pi]$; $\dot x_D=\alpha\cos\psi,\ \dot y_D=\alpha\sin\psi$, $\psi\in[-\pi,\pi]$; $\alpha>1$ is the speed ratio (Defender faster). Game state $x=[x_I,y_I,x_D,y_D]^\top\in\mathbb R^4$, $f\in C^1$. Initial conditions: $[x_I^0,y_I^0]\in\mathbb R^2\setminus(\mathcal T\cup\mathcal R)$, $[x_D^0,y_D^0]\in\mathbb R^2\setminus\mathcal R$.
- **Regions**: $\mathcal T=\{y\ge l\}$ (6), $\mathcal R=\{y\le0\}$ (7), disjoint closed half-planes.
- **Termination / winning** (eqs. (8)–(9)): Intruder wins on $\mathcal T_r=\{y_I\le0\}$; Defender wins on $\mathcal T_c=\{x\in\mathbb R^4\setminus\mathcal T_r:\|x_I-x_D\|^2=0\}$ (zero capture radius); capture on $\partial\mathcal R$ = Intruder win (p. 2).
- **Payoff** (eq. (10)): $J=\min_{t\in[0,t_f]}\mathrm{dist}([x_I(t),y_I(t)]^\top,\mathcal T)$ with $t_f=\inf\{t
[CITATION]
Role in a future paper: this is the **canonical modern reference for the reconnaissance game as a decomposed two-phase reach-observe-return differential game with geometric (half-planar) barriers** — the natural citation when a paper needs (i) the penetrate–observe–return problem statement with disjoint target/retreat half-planes, (ii) the "retreat point = projection of the Apollonius center" device, or (iii) an example of closed-form Value + HJI verification for a multi-stage target-guarding ga

### P050 — Solutions for Multiple-Defender Single-Attacker Convex Target Guarding Games: Verification via Parametric Opti
[BIBLIO]
- **ID**: P050
- **Source file**: `D:\System\zhuomian\game-paper\Lee和Bakolas - 2024 - Solutions for Multiple-Defender Single-Attacker Convex Target Guarding Games Verification via Param.pdf`
- **Total pages**: 8 (printed pp. 6357–6364)
- **Title**: Solutions for Multiple-Defender Single-Attacker Convex Target Guarding Games: Verification via Parametric Optimization
- **Authors**: Yoonjae Lee (Graduate Student Member, IEEE) and Efstathios Bakolas (Senior Member, IEEE), Department of Aerospace Engineering and Engineering Mechanics, The University of Texas at Austin, Austin, TX 78712 USA (corresponding author: Efstathios Bakolas).
- **Year/Venue**: 2024. Printed header: "IEEE TRANSACTIONS ON AUTOMATIC CONTROL, VOL. 69, NO. 9, SEPTEMBER 2024" — indexer guess (IEEE Transactions on Automatic Control) **confirmed**. Manuscript received 23 January 2024; revised 16 March 2024; accepted 17 March 2024; date of publication 20 March 2024; date of current version 29 August 2024. Recommended by Associate Editor G. Hu.
- **DOI** (printed): 10.1109/TAC.2024.3379948
- **Tier**: T1 (IEEE Transactions o
[CONTRIBUTIONS]
1. **Theory (verification)**: A complete verification of Isaacs' geometric method for the MDSA game: the candidate value $V$ (9) is proved to be the **viscosity solution** of the HJI equation (5) (Theorem 2), and its classical solution property holds exactly where LICQ holds (Theorems 1–2). This subsumes all the special-case verifications [8]–[14] and is the first to handle value nondifferentiability via Clarke subdifferentials.
2. **Theory (sensitivity apparatus)**: Association of $V$ with the optimal value function of a parametric convex program (P) and derivation of its continuity (Theorem 1(1)), local Lipschitzness and Clarke subdifferential (Theorem 1(2), eq. (27)), and $C^1$ differentiability characterized exactly by LICQ (Theorem 1(3), eq. (28)) — using duality, Slater's condition, 
[RESULTS-LIST]
- **Dynamics (1a)–(1b), p. 6358**: $\dot x_A = u_A$, $x_A(0) = x_{A,0}$; $\dot x_{D_i} = \nu_i u_{D_i}$, $x_{D_i}(0) = x_{D_i,0}$, $i \in [m]$; $u_r \in \mathcal U = \{u \in \mathbb R^n: \|u\|\le 1\}$; $\nu_i > 1$ for all $i$ (defenders strictly faster; $A$ slowest). Simple motion, no inertia.
- **Information structure**: perfect state feedback; $\theta \in \mathbb R^l$, $l = n(m+1)$; strategies $\gamma_r \in \Gamma$ (piecewise-continuous feedback $\mathbb R^l \to \mathcal U$). No explicit nonanticipativity delay structure is imposed.
- **Cost and termination (2)–(3), p. 6358**: $J = G(\theta(t_f)) = d_{\mathcal T}(x_A(t_f))$, where $d_{\mathcal T}(x) \triangleq \min_{y \in \mathcal T}\|x-y\|^2$ (squared distance; $\nabla d_{\mathcal T}(x) = 2(x - \Pi_{\mathcal T}(x))$). $t_f$ = first entry into $C_b \cup C_c$. Payoff is zero exactly on breach and equals the squared capture distance on c
[CITATION]
This paper is the canonical T1 reference for *rigorous verification of Isaacs' geometric method in multi-defender target guarding with convex targets*: it supersedes the special-case analyses of [8]–[13] and hardens the semi-formal treatment of Fu & Liu (P: Automatica 2023) with the missing uniqueness, gradient/subdifferential, and viscosity-solution proofs, and it is the natural "general MDSA result" to cite when motivating geometric-plus-HJI hybrid methodologies, parametric-optimization sensit

### P051 — Learning Strategy Representation for Imitation Learning in Multi-Agent Games
[BIBLIO]
- **ID**: P051
- **Source file**: `D:\System\zhuomian\game-paper\Lei 等 - 2025 - Learning Strategy Representation for Imitation Learning in Multi-Agent Games.pdf`
- **Total pages**: 9 (proceedings pagination 18163–18171; pp. 1–7 body incl. conclusion, p. 8 acknowledgments + references, p. 9 references continued)
- **Title**: Learning Strategy Representation for Imitation Learning in Multi-Agent Games
- **Authors**: Shiqi Lei¹* (Institute of Automation, Chinese Academy of Sciences, CASIA), Kanghoon Lee²* (KAIST), Linjing Li¹·³ (CASIA and Beijing Wenge Technology Co., Ltd.), Jinkyoo Park²† (KAIST; corresponding author). * = equal contribution, † = corresponding author (title-page footnotes, p. 1).
- **Year**: 2025 (copyright © 2025 AAAI; PDF created 2025-04-07)
- **Venue** (EXACT from running header/footer of every page): "The Thirty-Ninth AAAI Conference on Artificial Intelligence (AAAI-25)"; copyright line "Copyright © 2025, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved." (p. 1). This is the **main conference track** (numbered proceedin
[CONTRIBUTIONS]
1. **Modeling (representation learning)**: the P-VRNN — a Variational Recurrent Neural Network (Chung et al. 2015) whose conditioning variable is *partially trainable*: the strategy representation **l** of each trajectory is a free, per-trajectory trainable variable (randomly initialized), held constant along the trajectory and jointly optimized with the four networks φ_pri, φ_enc, φ_dec, φ_rec to minimize the negative variational lower bound (Eqs. (1)–(9), p. 3–4). No encoder produces **l**; the representation *is* the learned per-trajectory latent code, and player IDs are never used.
2. **Theory (indicators, partially formal)**: (a) the **Randomness Indicator** RI(τ) = Σₜ H(p_θ(a_t|z_≤t,a_<t,o_≤t,l)) — cumulative one-step action-distribution entropy, from the identity that the expected r
[RESULTS-LIST]
- **Model**: Markov game (Littman 1994) = POMDP adapted to n agents: state space S; agent i has action space Aⁱ and observation space Oⁱ (a 'null' action fills Aⁱ when i does not act). Per step t: (1) i observes o_t^i ∈ Oⁱ and samples a_t^i ~ πⁱ(oⁱ,·), πⁱ: Oⁱ × Aⁱ → [0,1]; (2) receives reward r_t^i: S × Aⁱ → ℝ; (3) state transitions by T: S × A¹ × ⋯ × Aⁿ → S (p. 2). No dynamics equations are given for the three test games — the environments are black-box simulators.
- **Return**: trajectory τ = ((o₀ⁱ,a₀ⁱ),…,(o_Tⁱ,a_Tⁱ)); r̂ⁱ(τ) = Σ_{t=0}^{T} r_tⁱ; expected payoff rⁱ(π₋ᵢ,πⁱ) = 𝔼_{τ∼(π₋ᵢ,πⁱ)}[r̂ⁱ(τ)]. *Argument order convention: first slot = opponents, second slot = focal player* (p. 2). Termination: trajectories run to the games' natural end (length T); no artificial truncation or winning-condition equation is given.
- **Best responses and exploitability** (p. 2): BR(π₋ᵢ) = argmax_{π′ⁱ} r
[CITATION]
**Paragraph role**: this is the *learning-based, data-curation* pole of the pursuit-evasion/reach-avoid literature — the counterpoint to analytic solution concepts. In a differential-game paper it serves three roles: (i) in the Introduction/Related Work as evidence that when opponent models or demonstrator identities are unavailable, latent strategy representations plus exploitability-flavored indicators (EL is a sampled, population-based surrogate of exploitability, cf. the E(π) definition on p

### P052 — Pursuit-evasion differential games of players with different speeds in spaces of different dimensions
[BIBLIO]
- **ID**: P052. **Source file**: `D:\System\zhuomian\game-paper\Li 等 - 2022 - Pursuit-evasion differential games of players with different speeds in spaces of different dimension.pdf` (filename truncated; true title from p. 1). **Total pages**: 6 (PDF pp. 1–6 = printed proceedings pp. 1299–1304).
- **Title**: Pursuit-evasion differential games of players with different speeds in spaces of different dimensions.
- **Authors**: Shuai Li, Chen Wang (corresponding author), Guangming Xie — State Key Laboratory of Turbulence and Complex Systems, Intelligent Biomimetic Design Lab, College of Engineering, Peking University, Beijing 100871, China; C. Wang additionally with the National Engineering Research Center of Software Engineering, Peking University; G. Xie additionally with Southern Marine Science and Engineering Guangdong Laboratory (Guangzhou), Guangzhou 511458, China (footnote, p. 1299).
- **Year**: 2022. **Venue** (exact, from header/copyright): "2022 American Control Conference (ACC), Atlanta, USA, June 8-10, 2022"; copyright line "978-1-6654-5196-3/$31.00 ©2022 AACC"; printed proc
[CONTRIBUTIONS]
1. **Geometry (modeling)**: Extension of the Apollonius circle to the 3D-pursuer/2D-evader setting — the intersection of the two players' isochrones is a circle in the evader's plane with closed-form center (eq. (5)) and radius (eq. (6)) depending on the pursuer's altitude $z_P$; Remark 1 interprets it as the intersection of a 3D "Apollonius sphere" with the evader's plane (pp. 1300–1301).
2. **Theory, PE game (Problem 1)**: Lemma 1 (max-speed, constant, straight-line optimal play via PMP) + closed-form capture point $q^\ast$ (farthest circle point for E), value $t_E(\boldsymbol{x})$ (eq. (9)) and feedback strategies (eq. (10)); Theorem 1 asserts Nash-optimality of these feedback strategies (pp. 1301–1302).
3. **Theory, TAD game (Problem 2)**: (a) *game of kind* — exact partition of the st
[RESULTS-LIST]
**Lemma 1 (p. 1301, unnumbered).** *Statement*: for differential game (1)(2)(3)(8) with $\boldsymbol{x}\in\mathcal{R}_0$, the optimal strategies of P and E are constant, at maximum speed, with straight-line trajectories. *Assumptions*: dynamics (1), speed bounds (2), cost (8) $J = \int_0^{t_f} dt$ (pure running cost, $h \equiv 1$, no terminal cost), capture time $t_f$ defined by the terminal manifold $x_P = x_E,\ y_P = y_E,\ z_P = 0$ (pursuer must reach the evader *in the plane*). *Proof approach*: Pontryagin's maximum principle — Hamiltonian $H = 1 + \lambda_x u_x + \lambda_y u_y + \lambda_z u_z + \mu_x v_x + \mu_y v_y$; since $\dot{\boldsymbol{\lambda}} = \partial H/\partial \boldsymbol{x} = \boldsymbol{0}$ (integrator dynamics), all costates are constant; P's $\boldsymbol{u}^\ast = \arg\min_{\boldsymbol{u}} H$ s.t. $\|\boldsymbol{u}\| \le u$ is a linear program over a convex ball, so 
[CITATION]
This is a short but clean conference paper whose lasting role in the knowledge base is as the *canonical reference for dimension-heterogeneous pursuit-evasion geometry*: it shows exactly how the Apollonius circle deforms when the pursuer's altitude $z_P$ enters the isochron intersection (eqs. (4)–(6)), gives the closed-form feedback laws (9), (10), (12)–(14) for both the time-optimal-capture (PE) and target-defense (TAD) degrees of play, and supplies the compact quadratic barrier $B(\boldsymbol{

### P053 — An Isochron-Based Solution to Pursuit-Evasion Games of Two Heterogeneous Players
[BIBLIO]
- **ID**: P053. **Source file**: `D:\System\zhuomian\game-paper\Li 等 - 2024 - An Isochron-Based Solution to Pursuit-Evasion Games of Two Heterogeneous Players.pdf`. **Total pages**: 16 (printed pp. 1–16; Read tool reports the file as password-protected, but pymupdf opens it with `needs_pass = 0`; text extracted page-by-page and key formulas verified against 200–400 dpi renders).
- **Title** (as printed): An isochron-based solution to pursuit-evasion games of two heterogeneous players.
- **Authors**: Shuai Li (Member, IEEE), Chen Wang (Senior Member, IEEE, corresponding author), Guangming Xie (Member, IEEE) — all Peking University (State Key Laboratory of Turbulence and Complex Systems / College of Engineering; C. Wang also National Engineering Research Center of Software Engineering). Funding: NSFC Grants U23B2037, U22A2062, 12272008.
- **Year**: 2024. **Venue** (EXACT, from footer/copyright line on every page): "This article has been accepted for publication in **IEEE Transactions on Automatic Control**. This is the author's version which has not been fully edited... Citation inform
[CONTRIBUTIONS]
1. **Method (modeling/analysis)**: an isochron-based framework for heterogeneous kinematics. Both players' optimal isochrones are circles (Lemma 2); the moving-center, growing-radius extended pursuer isochrones and the static-center evader isochrones generate an intersection curve whose external/internal tangency (ET-IT) events structure the whole game. Three independent factors are isolated: motion capabilities (u_pm/µ vs v_em), capture capability (ϵ via the superiority function F(τ), eq. (21)), and initial states (through τ̃, the first internal-tangency time).
2. **Taxonomy (theory)**: a complete division of the game into **16 cases** (Table I, p. 7; labels A-1…A-8, B-1…B-6, C-1, C-2) by superiority class × position of τ̃ relative to the roots τ1, τ2 of F(τ) × geometric features of the i
[RESULTS-LIST]
**Definition 1**: the isochron of time τ ∈ (0, ∞) of player i is the set of points i can reach at τ under the different (optimal-direction) strategies; the cluster over τ is the player's isochrones. Remark 1: τ is a predicted horizon, distinct from real time t.
**Lemma 2 statement**: under optimal strategies, E's isochron of time τ is the circle I_e(τ) = {(x,y): Γ_e = 0} with Γ_e(x,y,τ) = (x−x_ce)² + (y−y_ce)² − R_e(τ)² (eq. (6)–(7)), center c_e = (xe, ye)ᵀ (10), radius R_e = v_em τ (11); P's isochron is I_p(τ) with Γ_p(x,y,τ) = (x−x_cp)² + (y−y_cp)² − R_p(τ)² (eq. (8)–(9)), center c_p(τ) = (x_p − (v_px/µ)(e^{−µτ}−1), y_p − (v_py/µ)(e^{−µτ}−1))ᵀ (12), radius R_p(τ) = (u_pm/µ)(τ + (e^{−µτ}−1)/µ) (13).
- **Definition 3 (p. 5)**: E's dominant region D = {(x,y): Π(x,y) > 0}; justified by checking Π(x_e, y_e) = (x_p−xe)² + (y_p−ye)² − ϵ² > 0 pre-capture, so e ∈ D. If D is star-shaped at e (e 
[CITATION]
**Paragraph role**: this is the definitive reference for (i) isochrone-based geometric solution methods extended beyond simple (single-integrator) kinematics to a second-order damped pursuer, (ii) the complete game-of-kind taxonomy (16 cases) for the damped-double-integrator vs single-integrator PE game — the modern, thorough treatment of Isaacs' isotropic rocket configuration, and (iii) optimality-based explanations of prey evasion behaviors (swerve/sideway, circling, tail-chase) and of the cou

### P054 — Distributed Task Allocation with Minimum Makespan for Heterogeneous Multiplayer Pursuit-Evasion Games
[BIBLIO]
- **ID**: P054
- **Source file**: `D:\System\zhuomian\game-paper\Li 等 - 2024 - Distributed Task Allocation With Minimum Makespan for Heterogeneous Multiplayer Pursuit-Evasion Game.pdf`
- **Total pages**: 16 (pp. 1–16, early-access pagination; refs and author bios end on p. 16)
- **Title**: Distributed Task Allocation with Minimum Makespan for Heterogeneous Multiplayer Pursuit-Evasion Games
- **Authors**: Shuai Li (Member, IEEE), Chen Wang (Senior Member, IEEE, corresponding), Jinan Sun (Member, IEEE), Shikun Zhang (Member, IEEE), Guangming Xie (Member, IEEE, corresponding) — all Peking University (College of Engineering / National Engineering Research Center of Software Engineering), Beijing, China. Funding: NSFC Grants U23B2037, U22A2062, 12272008. "The material in this paper was not presented at any conference."
- **Year/Venue**: 2024. Printed running head is the IEEE early-access template placeholder "GENERIC COLORIZED JOURNAL, VOL. XX, NO. XX, XXXX 2024"; every page footer states: "This article has been accepted for publication in IEEE Transactions on Automatic Control. This is t
[CONTRIBUTIONS]
1. **Problem/modeling**: First formulation (per authors) of a multiplayer PE game integrating player heterogeneity (different dynamics, speeds, accelerations, capture radii, sensing ranges), fully distributed decision-making with limited sensing/communication, and the minimum-makespan team objective; plus a four-subproblem decomposition (P1 capture condition/strategies, P2 winning region, P3 sensing-range threshold, P4 distributed allocation) forming an overall framework (Section III-A, pp. 4–5).
2. **Theory (P1, Theorem 1)**: A novel isochron-based method for the 1-on-1 game between a simple-motion pursuer and a damped double-integrator evader: capture condition (15), optimal pursuit strategy (17), optimal evasion strategy (18), and value $V_{ij}=\tau^\ast$, validated by substitution into
[RESULTS-LIST]
- **Pursuers (1)**: single integrators, $\dot p_i=v_{pi}$, $\|v_{pi}\|\le v_{mpi}$; **evaders (2)**: damped double integrators with damping factor $\mu>0$ and acceleration input $u_{ej}\in[0,u_{mej}]$ at heading $\theta_{ej}$; the maximum steady-state speed is $u_{mej}/\mu$ (reached by accelerating along a constant direction, p. 3). Heterogeneity: per-player $v_{mpi}$, $\epsilon_i\ge 0$ (capture radius; both point and nonzero capture), $r_i>0$ (sensing), $u_{mej}$.
- **Capture topologies (p. 5)**: $\mathcal G_c=(\mathcal Y,\mathcal Z_c)$, $\mathcal Z_c=\{(P_i,E_j)\,|\,P_i\text{ can capture }E_j\}$; possible targets $\mathcal T_i^c$; feasible targets $\mathcal T_i^{cd}=\mathcal T_i^d\cap\mathcal T_i^c$; conflict graph $\mathcal F_c=(\mathcal Y_{\mathcal P},\mathcal S_c)$, $\mathcal S_c=\{(P_i,P_k)\,|\,\mathcal T_i^c\cap\mathcal T_k^c\ne\emptyset\}$; sensing-restricted conflict subgraph $\
[CITATION]
**Paragraph role**: This paper is the reference point for *bottleneck-objective (makespan) distributed task allocation layered on pairwise heterogeneous pursuit games*. Its most reusable assets are: (a) the isochron-based capture condition (Theorem 1) — an Apollonius-style tangency test between a linearly growing circle (simple-motion pursuer, inflated by the capture radius) and the damped-evader isochrone circle whose center and radius are explicit exponentials in $\mu\tau$ — giving a closed-fo

### P055 — An Analytical Approach for Target Defense Differential Games With Speed-Varying Players
[BIBLIO]
- **ID**: P055
- **Source file**: `D:\System\zhuomian\game-paper\Li 等 - 2026 - An Analytical Approach for Target Defense Differential Games With Speed-Varying Players.pdf` (PDF flagged "password-protected" by the reader but opens normally; text + figures extracted with pymupdf). Duplicate preprint build archived as P004 (VARIANT of P055; cite this record only).
- **Total pages**: 12 PDF pages = journal pp. 1850–1861 (all 12 read: body pp. 1850–1860, references pp. 1860–1861, bios p. 1861).
- **Title**: An Analytical Approach for Target Defense Differential Games With Speed-Varying Players
- **Authors**: Zhan Li (Member, IEEE), Xilun Li (Graduate Student Member, IEEE), Xuebo Yang (Member, IEEE), Xinghu Yu (Member, IEEE), Jianbin Qiu (Fellow, IEEE) — Harbin Institute of Technology (Research Institute of Intelligent Control and Systems; State Key Laboratory of Robotics and Systems); X. Yu with Ningbo Institute of Intelligent Equipment Technology Co. Ltd.
- **Year**: 2026. Received 26 Sep 2025; accepted 24 Dec 2025; date of publication 21 Jan 2026; date of current version 18 Feb 2026. Re
[CONTRIBUTIONS]
1. **Theory (main)**: first (per authors) analytical Nash-equilibrium solution of a TDDG whose players have second-order (speed-dynamic) plants with force saturation, obtained by an *average speed ratio* reduction: the 6-D SOTDDG with four decision variables is decomposed into (i) a force-allocation problem solved by PMP (bang-bang full acceleration, then coast) and (ii) a 1-D extremal search of the terminal value over $\bar\alpha$ — no HJI PDE is solved numerically (Abstract, p. 1850; §IV-A, p. 1857–1858).
2. **Theory (verification)**: a continuously differentiable terminal value function w.r.t. the ratio (Lemmas 1–2, p. 1856), used to argue via the HJI equation that the constructed strategies are the Nash equilibrium (Theorems 1–3; eqs. (35), (36), (44), (67)).
3. **Theory (unification)*
[RESULTS-LIST]
- **Dynamics (1)** (second-order in speed; heading is a *control*, not a state):
- **Constraints (2)**: $v_A\le v_{A\max}$, $|F_A|\le F_{A\max}$, $v_D\le v_{D\max}$, $|F_D|\le F_{D\max}$; controls $\mathbf u_A:=\{\chi,F_A\}$, $\mathbf u_D:=\{\gamma,F_D\}$ (3); state $\mathbf z:=[\mathbf x,\mathbf y,\mathbf v]^\top$ (4); $\mathbf z_0$ (5).
- **Termination (6)**: $\psi(\mathbf z_f):=\sqrt{(x_{A_f}-x_{D_f})^2+(y_{A_f}-y_{D_f})^2}=0$ — capture at coincidence (no capture radius for $D$). Printed typo in the where-line: "$y_{D_f}=x_D(t_f)$" (p. 1852; should be $y_D(t_f)$).
- **Cost (7)–(9)**: Mayer form $J=\varphi(\mathbf z_f)= (x_{A_f}-x_T)^2+(y_{A_f}-y_T)^2$ (squared distance from $A$ to the target *center* at interception; $r_T$ plays no role in the game of degree); $V(\mathbf z_0):=\min_{\mathbf u_A}\max_{\mathbf u_D}J$.
- **Assumptions (p. 1852)**: (i) at maximum speed the force is 0 (coa
[CITATION]
**Paragraph role**: this is the library's reference point for (i) taking TDDG analysis from constant-speed single integrators to speed-varying second-order plants with saturated forces, (ii) the *average-speed-ratio* reduction — freezing the endogenous speed ratio $\bar\alpha=\tilde v_D/\tilde v_A$ at its maximum and reusing the Apollonius-circle machinery ((47)–(49) re-instantiate (14)–(15); (68) offsets the barrier by $r_T$), and (iii) the unified arbitrary-ratio FOTDDG expressions (14)–(16) w

### P056 — A Reconnaissance Penetration Game With Territorial-Constrained Defender
[BIBLIO]
- **ID**: P056
- **Source file**: `D:\System\zhuomian\game-paper\Liang 等 - 2022 - A Reconnaissance Penetration Game With Territorial-Constrained Defender.pdf`
- **Total pages**: 8 (journal pp. 6295–6302)
- **Title**: A Reconnaissance Penetration Game With Territorial-Constrained Defender
- **Authors**: Li Liang (Beijing Univ. of Chemical Technology; liangli@bit.edu.cn), Fang Deng (Senior Member, IEEE; corresponding author), Jianan Wang (Senior Member, IEEE), Maobin Lu (Member, IEEE) — School of Automation, Beijing Institute of Technology; Jie Chen (Fellow, IEEE) — Tongji University / Beijing Institute of Technology
- **Year**: 2022 (received 16 Aug 2021; revised 14 Jan 2022; accepted 7 Jun 2022; published 14 Jun 2022; issue Nov. 2022; Associate Editor S. Grammatico)
- **Venue (EXACT, from page header/copyright)**: IEEE Transactions on Automatic Control, Vol. 67, No. 11, November 2022, pp. 6295–6302. Indexer guess (TAC) is **correct**.
- **DOI (printed)**: 10.1109/TAC.2022.3183034
- **Tier**: T1 (IEEE Trans on Automatic Control) — no disagreement.
- **Funding (printed)**: NSFC 6210304
[CONTRIBUTIONS]
1. **Modeling**: a new reconnaissance-penetration game with a territorial-constrained defender under the multiplayer pursuit-evasion framework, with both target maneuvering evasion and active interception defense (theory/modeling).
2. **Method — explicit policy method**: instead of Isaacs' HJI machinery (hard here because of the three termination sets), the qualitative game (game of kind) is solved by imposing explicit candidate strategies, analyzing pairwise Apollonius-dominance geometry, deriving an "escape angle" for the attacker, and partitioning initial states into three cases by territory size (theory/method).
3. **Games of kind**: analytic winning conditions (Theorems 4.1–4.7) and switching strategies for all three players; the barrier/winning regions are assembled from the conditio
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion for each player, e.g. $\dot{x}_T = V_T\cos\hat\phi,\ \dot{y}_T = V_T\sin\hat\phi$ (initial conditions $x_{T0},y_{T0}$), analogously A with heading $\hat\chi$ and D with heading $\hat\psi$; speeds constant, $V_T < V_A = 1 < V_D$.
- **Territorial constraint (the paper's central modeling object)**: $x_D(t) \in \Omega_D := \{(x,y)\,|\,(x-x_{D0})^2+(y-y_{D0})^2 \le l^2\}$, radius $l$ determined by the communication base-station capability ("obtained in the early reconnaissance"). Note $D$ starts at the center $D_0 = (x_{D0},y_{D0})$.
- **Relative variables**: $\varphi = \hat\phi - \lambda_{AT}$, $\chi = \lambda_{AT} + \theta - \hat\chi$, $\psi = \hat\psi - \theta - \lambda_{AT} + \pi$ (relative headings w.r.t. $\overrightarrow{AT}$, $\overrightarrow{DA}$, $\overrightarrow{AD}$), $\lambda_{AT}$ = inclination of $\overrightarrow{AT}$, $\theta = \angle DAT
[CITATION]
**Paragraph role**: This is the first analytical treatment of a three-player TAD-type game in which the defender is confined to a circular territory, solved by an "explicit policy method" that replaces HJI barrier computation with Apollonius-dominance geometry: an escape-angle theorem for the attacker inside the territory, a case split on territory size (ordinary/small/large), constructive winning conditions and switching strategies for all three players, and a PMP layer (constant costates ⇒ con

### P057 — Reach-avoid differential games technologies for anti-unmanned aerial vehicles
[BIBLIO]
- **ID**: P057 / **source file**: `D:\System\zhuomian\game-paper\Liang 等 - 2025 - Reach-avoid differential games technologies for anti-unmanned aerial vehicles.pdf` / **total pages**: 6 (PDF: cover/pre-proof notice page + article pp. 1–4 + declaration-of-interest page; article content is only 4 pages).
- **Title** (as printed): Reach-avoid differential games technologies for anti-unmanned aerial vehicles.
- **Authors**: Ruining LIANG (a); Rui YAN (a, corresponding author, rui-yan@buaa.edu.cn); Xiwang DONG (a,b,c). Affiliations: (a) School of Artificial Intelligence, Beihang University, Beijing 100191, China; (b) School of Automation Science and Electrical Engineering, Beihang University; (c) Institute of Unmanned System, Beihang University.
- **Year**: 2025 (Received 24 July 2025; Accepted 5 November 2025; © 2025 Published by Elsevier Ltd on behalf of Chinese Society of Aeronautics and Astronautics & Beihang University).
- **Venue (EXACT, from header/copyright)**: *Chinese Journal of Aeronautics*, section **"Views & Comments"**; Journal Pre-proof / Final Accepted Version, article no.
[CONTRIBUTIONS]
1. **(Position/taxonomy)** A compact taxonomy of reach-avoid differential-game technologies organized for the anti-UAV application: games of kind/degree → numerical (HJI) vs. geometric (dominance regions: Voronoi / Apollonius / potential function) solvers; decomposition of multiplayer games into coalition-vs-one-evader subgames with winning-condition-based coalition formation; matching-based task allocation with NP-hardness and the SMA approximation; capture-style taxonomy (laser / collision / net) tied to the capture radius r_i (Secs. 2.1–2.3). This is a curated reading list of 10 anchors, several of which are the authors' own papers.
2. **(Modeling/mapping)** An explicit element-by-element mapping between the reach-avoid formulation (Eq. (1), Ω_goal, P/E, r_i) and AUAV scenario elements 
[RESULTS-LIST]
- **Game space**: R³ split by a closed surface T into Ω_goal = {y ∈ R³ | g(y) ≤ 0}, T = {y ∈ R³ | g(y) = 0}, Ω_play = {y ∈ R³ | g(y) > 0}, with g: R³ → R "a continuous function such that Ωgoal." — **the sentence is truncated in the pre-proof**; the intended regularity/shape condition on Ω_goal is unprinted (p. 2).
- **States**: x_Pi(t) = [x_Pi, y_Pi, z_Pi, ψ_Pi]ᵀ ∈ Rⁿ (n ≥ 3), x_Ej(t) = [x_Ej, y_Ej, z_Ej, ψ_Ej]ᵀ ∈ R^m (m ≥ 3); positions in R³; ψ ∈ R^(n−3) resp. R^(m−3) are "remaining elements (maybe empty)" (pp. 2–3). So the formulation is dimension-generic: 3-D simple motion is the minimal case, and Dubins/attitude states are accommodated.
- **Dynamics (Eq. (1), p. 3)**: ẋ_Pi = f_Pi(x_Pi, u_Pi), x_Pi(0) = x⁰_Pi, Pi ∈ P; ẋ_Ej = f_Ej(x_Ej, u_Ej), x_Ej(0) = x⁰_Ej, Ej ∈ E; f_Pi: Rⁿ×R^kp → Rⁿ and f_Ej: R^m×R^ke → R^m **continuously differentiable**.
- **Controls**: u_Pi ∈ U_p = {u: [0,∞) → S
[CITATION]
**Likely role in a future IEEE Trans introduction**: (a) **application-motivation citation** — the cleanest printed mapping of reach-avoid game elements to anti-UAV defense (infrastructure ↔ Ω_goal, malicious UAVs ↔ evaders, defense UAVs ↔ pursuers with capture radii ↔ capture equipment); (b) **related-work taxonomy anchor** for the decomposition → game-of-kind coalitions → matching-based allocation → SMA line of multiplayer reach-avoid research (its refs. 3, 4, 6 = KB P103, P037); (c) a **gap-s

### P058 — Pursuit Strategies for Capture-the-Flag Games With Half-Plane Flag and Return Region
[BIBLIO]
- **ID**: P058
- **Source file**: `D:\System\zhuomian\game-paper\Liang 等 - 2026 - Pursuit Strategies for Capture-the-Flag Games With Half-Plane Flag and Return Region.pdf` (filename truncated in the task list; full title on p. 1)
- **Total pages**: 13 (pp. 1–11 main text + references, p. 12 references continued, p. 13 references end + author biographies)
- **Title**: Pursuit Strategies for Capture-the-Flag Games With Half-Plane Flag and Return Region
- **Authors**: Ruining Liang, Rui Yan (Senior Member, IEEE; corresponding author), Jiajun Cai, Xiwang Dong (Senior Member, IEEE)
- **Affiliations**: School of Artificial Intelligence, Beihang University (Liang, Yan, Cai); School of Automation Science and Electrical Engineering / School of Artificial Intelligence / Institute of Unmanned System, Beihang University (Dong)
- **Year**: 2026. **Venue (printed)**: running header "IEEE Transactions on Cybernetics"; copyright line "2168-2267 © 2026 IEEE"; footnote "This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of 
[CONTRIBUTIONS]
1. **Modeling** (theory scope): A multiplayer CTF differential game with a half-plane flag Ω_flag, a half-plane return region Ω_return, heterogeneous pursuers with distinct speed ratios α_ij > 1 and nonzero capture radii r_i ≥ 0 — strictly more general than [12], [13], [17], [21], [26], [36], [53] per the authors.
2. **Theory — subgame solution** (Sec. III): A **via-point (flag-aware) potential function** f_ij(x, x_F) (eq. (2)) extending the reach-avoid potentials of [44], [48] to the two-stage CTF setting; the associated **evasion space (ES)** and three classes of interception points (I_F0, I_R, I_R0); strict convexity of the ES (Lemma 1); straight-line optimality (Lemma 2); a pursuit winning strategy and **necessary and sufficient** game-of-kind conditions (Theorems 1–2) for every multip
[RESULTS-LIST]
- **Regions**: Ω_flag = {x ∈ R² | y ≥ y_F} with boundary F = {y = y_F}; Ω_return = {x | y ≤ 0} with boundary R = {y = 0}; play region Ω_play = {x | y < y_F and y > 0} (open strip between the two lines); y_F ∈ R⁺ is the separation between F and R. The flag and return half-planes lie on **opposite sides** of the strip; an evader must cross the strip, touch the flag half-plane, and come back.
- **Dynamics (eq. (1))**: ẋ_Pi = v_Pi u_Pi, ẋ_Ej = v_Ej u_Ej, simple motions (Isaacs mass points, holonomic); controls u ∈ 𝒰 = {u : [0,∞) → S² piecewise smooth}, S² = {u ∈ R² : ‖u‖₂ ≤ 1}; initial positions x⁰_Pi, x⁰_Ej ∈ R².
- **Heterogeneity**: speed ratio α_ij = v_Pi/v_Ej; only faster pursuers α_ij > 1 are considered (justified by [13], [26], [35], [36] precedent and the difficulty of faster evaders [27]). Capture radius r_i ≥ 0; E_j is captured by P_i iff distance ≤ r_i **and** P_i is pursuing that 
[CITATION]
**Paragraph role**: P058 is the analytical, multiplayer, nonzero-capture-radius anchor for two-phase (flag + return) pursuit in this library. It bridges three literatures: (i) Garcia–Casbeer–Pachter's one-to-one CTF line ([12], [13], [26], [53]) — P058 generalizes to heterogeneous teams with capture radii and gives a game-of-kind characterization; (ii) Yan et al.'s potential-function/matching machinery for reach-avoid games ([44], [45], [48], [6]) — P058 lifts it to two-stage objectives via the 

### P059 — TARA-LLM: A Knowledge-Driven Model for Task Assignment of Multiplayer Reach-Avoid Games
[BIBLIO]
- **ID**: P059. **Source file**: `D:\System\zhuomian\game-paper\Liang 等 - 2026 - TARA-LLM A Knowledge-Driven Model for Task Assignment of Multiplayer Reach-Avoid Games.pdf`. **Total pages**: 12.
- **Title**: TARA-LLM: A Knowledge-Driven Model for Task Assignment of Multiplayer Reach-Avoid Games
- **Authors**: Ruining Liang, Rui Yan (Senior Member, IEEE, corresponding author), Bo Liu, Xiaoduo Li (Member, IEEE), Jintao Chen, Xiwang Dong (Senior Member, IEEE)
- **Year**: 2026 (Received 29 March 2026; accepted 5 April 2026; Paper no. TII-26-2765; early access "accepted for inclusion in a future issue")
- **Venue** (EXACT, from page-1 header): *IEEE Transactions on Industrial Informatics* — indexer guess confirmed correct. **DOI (printed)**: 10.1109/TII.2026.3683214. No volume/issue/page yet (PP;99).
- **Tier**: T1 (IEEE Transactions). No disagreement.
- **BibTeX** (from printed metadata only):
```bibtex
@article{Liang2026TARALLM,
  author  = {Liang, Ruining and Yan, Rui and Liu, Bo and Li, Xiaoduo and Chen, Jintao and Dong, Xiwang},
  title   = {{TARA-LLM}: A Knowledge-Driven Model for T
[CONTRIBUTIONS]
1. **Knowledge construction (modeling)**: textual knowledge extracted from analytical M-RA theory — pursuit winning knowledge Kw (Def. 3, from Lemma 2/Def. 2), coalition reduction knowledge Kr (Def. 4, from Lemma 3), constraint knowledge Kc (Def. 5, from BIP (2)) — packaged as LLM prompts (Sec. III, p. 4–5).
2. **Structured prompt engineering / planning module (algorithm)**: a two-chain reasoning process f^plan: (P_bd, P_sr, P¹_rt, P²_rt, P_or) → M0 — chain 1 evaluates one-to-one subgames, chain 2 evaluates two-to-one subgames (separated by Kr), outcomes analyzed by Kw, merged at the end under Kc (Sec. IV-A, p. 5–6, Fig. 5–6).
3. **Revision module (theory + algorithm)**: three analytic corrections Cu, Cr, Cp (Algorithms 2–4) that remove unreasonable pairs, redundant pursuers, and physical 
[RESULTS-LIST]
- **Dynamics (1)** (p. 2–3): simple motion (Isaacs) mass points in the plane: ẋ_Pi = v_Pi u_Pi, ẋ_Ej = v_Ej u_Ej, with u_Pi, u_Ej ∈ U = {u: [0,∞) → S², piecewise smooth}, S² the unit disk; speed ratio α_ij = v_Pi/v_Ej > 1 (all pursuers faster than all evaders).
- **Domain**: Ωgoal = {y | g(y) ≤ 0}, T = {y | g(y) = 0}, Ωplay = {y | g(y) > 0}, with g: R² → R differentiable and Ωgoal nonempty, compact, **convex** (p. 3). Convexity is essential: Lemma 3's reduction is stated for convex goal regions.
- **Capture/termination**: E_j is captured by P_i iff distance ≤ r_i (r_i ≥ 0); a pursuer that captures one evader stays still afterward (p. 3). Evasively, E maximizes the number of evaders reaching Ωgoal; P prevents this. No payoff function is written — the game is a game of kind with a team-level counting objective.
- **Information**: state feedback — both teams act on the current positions of 
[CITATION]
Role in the literature: this is the first bridge between LLM-based decision-making and analytical multiplayer reach-avoid game theory, and a representative instance of the "knowledge-driven LLM + analytic verification" pattern for guaranteed multirobot task assignment; it connects the Yan et al. matching-based M-RA line ([40] Automatica 2022, [41] Automatica 2024, [43] TRO 2020) with the prompt-engineering literature (CoT, CoT-SC, ToT) and provides a rare hardware validation (6-AAV motion-captur

### P060 — Strategy design of reach-avoid game: Geometric modeling and USV implementation
[BIBLIO]
- **ID**: P060 | **Source file**: `D:\System\zhuomian\game-paper\Lin 等 - 2026 - Strategy design of reach-avoid game Geometric modeling and USV implementation.pdf` | **Total pages**: 12
- **Title**: Strategy design of reach-avoid game: Geometric modeling and USV implementation
- **Authors**: Bin Lin, Wei Xie (corresponding), Zhihuan Hu, Zhijian Sun, Zehua Jia, Weidong Zhang (corresponding), Defeng Wu, Xiadong Lyu. Affiliations: School of Automation and Intelligent Sensing, Shanghai Jiao Tong University; State Key Laboratory of Submarine Geoscience (Shanghai); Crossocean of Suzhou Technology Co., LTD; Hainan University; School of Marine Engineering, Jimei University; Fujian Provincial Key Laboratory of Naval Architecture and Ocean Engineering; China Ship Development and Design Center.
- **Year**: 2026 (received 29 Sep 2025; revised 27 Jan 2026; accepted 25 Feb 2026; available online 12 March 2026 — all printed on p. 1)
- **Venue**: **Control Engineering Practice**, Vol. 172 (2026), Article 106882 (running footer "Control Engineering Practice 172 (2026) 106882" on every page; ISSN 0967-
[CONTRIBUTIONS]
1. **Theory (reachability)**: a scalar *time-difference function* $f_{\mathrm{diff},i}(\mathbf p_R) = (d_{D_iR}-\rho_{D_i})/\beta_i - d_{AR}$ (p. 4) as a per-point reachability criterion (Lemma 1), a Lipschitz-type property of the oval's direction map (Lemma 2), and a closed-loop invariance proof that under the proposed oval-based interception strategy (2) the attacker is confined to the Cartesian oval $\mathcal R_i$ (Lemma 3), extended to two defenders by set intersection (Theorem 1). This is exactly the proof layer claimed missing in Garcia (2021)/Shi et al. (2025).
2. **Theory (game values)**: non-inferiority ("no alternative strategy can do better") theorems giving the DDR value $d_{MT}(t_0)-\rho_T$ (Theorem 2) and the ADR value $\Delta_{D_1D_2N}$ (Theorem 3), the latter via a *virtual
[RESULTS-LIST]
- **Statement**: with speed ratio $\beta_i = v^{\max}_{D_i}/v^{\max}_A > 1$ and capture radius $\rho_{D_i}$, the boundary $\mathrm{br}_i$ of $A$'s reachable region $\mathcal R_i$ under $D_i$'s interception is a Cartesian oval centered at $A$ (attributed to Garcia 2021). In polar form about $\mathbf p_A$, with $\delta_A$ the angle between $A$'s heading ray and the LOS angle $\sigma_{D_iA} = \mathrm{atan2}(y_A - y_{D_i}, x_A - x_{D_i})$:
- **Verification (mine)**: the oval condition $d_{D_iC} = \beta_i r_A + \rho_{D_i}$ (attacker flight time to $C$ equals defender time to reach the $\rho_{D_i}$-ball around $C$) plus the law of cosines $d^2_{D_iC} = d^2_{D_iA} + r_A^2 + 2 d_{D_iA} r_A \cos\delta_A$ gives a quadratic in $r_A$ whose positive root is exactly $f_{r_A}$ as printed; the $\delta_{D_i}$ formula is the sine rule in triangle $D_iAC$ ($r_A \sin\delta_{D_i} = r_A^{\mathrm{opp}}$... pre
[CITATION]
This is the collection's cleanest "theory-to-hull" arch: a geometric reach-avoid solution (Cartesian oval + time-difference function + invariance proof + two value theorems) that is actually run on three physical USVs in a lake, with the full NGC integration (guidance-layer strategy → backstepping controller → 3-DOF model) spelled out. In an archive, it plays four roles: (i) as the engineering counterpart of Yan et al. (2019)-style two-defender geometry, showing what changes when capture radii a

### P061 — Reach-avoid games for players with damped double integrator dynamics
[BIBLIO]
- **ID / source file / total pages**: P061 / `D:\System\zhuomian\game-paper\Lyu 等 - 2025 - Reach-avoid games for players with damped double integrator dynamics.pdf` / 20 pages (preprint pagination; printed page numbers 1–20 match PDF pages).
- **Title**: Reach-avoid games for players with damped double integrator dynamics.
- **Authors**: Mengxin Lyu, Ruiliang Deng, Zongying Shi (corresponding author), Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084. Funding printed in footnote: NSFC Grant U24B20173.
- **Year / Venue**: 2025. Header of the local copy: "arXiv:2505.11951v1 [eess.SY] 17 May 2025" and footer "Preprint submitted to Automatica, 20 May 2025". This is the **arXiv v1 preprint submitted to Automatica**, not a typeset published version. Verified online (2026-10-11): arXiv lists v1 (17 May 2025) and v2 (19 Feb 2026), with **no journal-ref, DOI, or acceptance note** — so the indexer guess "Automatica" matches the intended venue but the paper is, as of today, an unpublished/under-review preprint. No DOI printed (arXiv DOI only: 10.48550/arXiv.2505.1195
[CONTRIBUTIONS]
1. **Motion analysis under the optimal strategy** (Sec. 3.1–3.2): via the Maximum Principle, optimal play is maximum acceleration with constant heading (eqs. (7)–(14)); isochrones are circles (15); the **multiple reachable region (MRR)** $\mathcal M_i$ — points reachable at three distinct times, hence by three strategies — is constructed analytically through self-overlapping isochrones (Lemma 2), with boundary curves $\mathcal B_I^i,\mathcal B_II^i$ (26), cusp time $t_u$ (30)–(31), and barrier time $t_{is}$ (25). Circumscribing/inscribing times of the two players' isochrones: at least one, at most three (Theorem 1), computable by a bracketed root-finding scheme (Algorithm 1).
2. **New typology of the attacker's dominance region** (Sec. 3.3): typical ADR (Def. 3) split into $\mathcal R_I$ (
[RESULTS-LIST]
- **Dynamics** (1), p.2 (above). Implicit standing assumption (p.4): $\|\mathbf v_{i0}\| \le u_{im}/\mu$, consistent with the speed saturation $\|v_i(t)\| \le \|v_{i0}\|e^{-\mu t} + \frac{u_{im}}{\mu}(1-e^{-\mu t}) \to u_{im}/\mu$ (p.4).
- **Termination**: point capture, terminal equality constraint (2); value = final attacker–target distance (3)–(4). Defender-winning scenario assumed: target is outside the ADR.
- **Information**: complete state feedback (p.3). Cost is terminal-only; no running cost.
- **Hamiltonian** (7), p.3: $H = \lambda_1 v_{Dx}+\lambda_2 v_{Dy}+\gamma_1 v_{Ax}+\gamma_2 v_{Ay}+\lambda_3(-\mu v_{Dx}+u_D\cos\theta_D)+\lambda_4(-\mu v_{Dy}+u_D\sin\theta_D)+\gamma_3(-\mu v_{Ax}+u_A\cos\theta_A)+\gamma_4(-\mu v_{Ay}+u_A\sin\theta_A)$, with defender co-state $\lambda$, attacker co-state $\gamma$.
- **Co-state solutions** (8)–(11), pp.3–4: $\dot\lambda_1=\dot\lambda_2=0$, $
[CITATION]
This is the first paper to carry reach-avoid geometric game theory from simple motion to damped double integrator dynamics, and its durable contributions are the motion primitives — isochrone reachability disks with Gronwall-certified tightness (Lemma 1), the multiple reachable region with its $\mathcal B_I/\mathcal B_II$ boundary anatomy and barrier time (Theorem 1, Lemma 2, eqs. (25)–(32)), and the three-type attacker's dominance region culminating in $\mathcal R_{III}$, where the attacker mus

### P062 — Cooperative Multiple-Pursuer Single-Evader Reach-Avoid Games with A Convex 3-Dimensional Target Region under P
[BIBLIO]
- **ID**: P062
- **Source file**: `Ma 等 - Cooperative Multiple-Pursuer Single-Evader Reach-Avoid Games with A Convex 3-Dimensional Target Regi.pdf` (filename truncated; full title taken from p. 1)
- **Total pages**: 8 (pp. 1–7 body, p. 8 references)
- **Title**: Cooperative Multiple-Pursuer Single-Evader Reach-Avoid Games with A Convex 3-Dimensional Target Region under Partial Information
- **Authors**: Zihao Ma (Beihang Univ., Institute of Artificial Intelligence), Hao Liu (Senior Member, IEEE; Beihang Univ.; corresponding author), Zhongkui Li (Senior Member, IEEE; Peking Univ.), Frank L. Lewis (Life Fellow, IEEE; UT Arlington Research Institute)
- **Year**: not printed on the paper; PDF compiled 2026-03-16 (TeX output date), consistent with 2026 early access
- **Venue**: running header prints "IEEE Transactions on Automatic Control" on every page; early-access build (no volume/issue/pages/month/DOI printed anywhere). Indexer guess (IEEE TAC) is **correct**.
- **Funding (printed footnote, p. 1)**: NSFC Grants 62273015 and U23B2032
- **Tier**: T1 (IEEE Transactions on Automatic Contr
[CONTRIBUTIONS]
1. **(Modeling)** A many-vs-one reach-avoid game in 3-D with a convex target region and an asymmetric information structure: evader global, pursuit team limited to S with pooled communication; non-anticipative strategy sets (2); the defense strategy is split into an open-loop deployment strategy ΠdP (before detection) and a closed-loop capture strategy ΠcP (after detection), with the feasible capture set Π̄cP required to keep xE(t) ∈ S for all t ∈ [tc, tf] (p. 3).
2. **(Strategy/algorithm — Theorem 1, p. 4, eqs. (6)–(7))** A geometric cooperative capture strategy under partial information with three cases, guaranteeing the partial-information value is bounded below by the complete-information value at the detection instant, V(x) ≥ ‖ϑ*(tc) − χ(tc)‖₂; includes an explicit speed-ratio thresho
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion, ẋPi = vP·uPi, ẋE = vE·uE, controls in U = {u ∈ R³ : ‖u‖₂ = 1 or u = 0} (unit heading or full stop). Homogeneous pursuers; augmented state x = [xP⊤, xE⊤]⊤.
- **Termination**: game ends at tf when ‖xPi − xE‖₂ ≤ rc for some i (capture) or xE reaches Ωtar.
- **Information**: IP(t) = {xPi, vP}ᴺᵖᵢ₌₁ ∪ {xE, uE, vE : xE ∈ S}; IE(t) = {xPi, vP}ᴺᵖᵢ₌₁ ∪ {xE, vE}; non-anticipative admissible strategies (2): ΠP = {uP(·) : uP(t) ∈ UP(IP(t)) ∀t}, likewise ΠE. The evader cannot access rs.
- **Assumption 1 (speed ratio)**: α = vP/vE > 1. **Assumption 2 (initial deployment)**: initial positions randomly generated; x0E ∈ Ωplay \ S (game not trivially over at t = 0).
- **Payoff / value**: J(x, uP, uE) = dist(xE(tf), Ωtar) (evader minimizes); complete-information value Ṽ(x) = sup_{uP∈ΠP} inf_{uE∈ΠE} J; partial-information capture-phase value V(x) = sup_{uP∈Π̄cP} inf_{
[CITATION]
**Role in the literature**: this is a current-generation IEEE TAC paper that pushes barrier/winning-region analysis from complete to partial information, from planar/circular targets to a general convex 3-D target, and from 1-vs-1 to Np-vs-1 — the missing quadrant relative to [8], [9] (partial information, simplified geometry) and [10]–[14] (3-D/convex targets, complete information). It is the canonical reference for three reusable devices: (i) the two-phase deployment/capture decomposition for 

### P064 — Heterogeneous Multiplayer Reach-Avoid Differential Game under Partial Information
[BIBLIO]
- **ID**: P064. **Source file**: `D:\System\zhuomian\game-paper\Ma 等 - Heterogeneous Multiplayer Reach-Avoid Differential Game under Partial Information.pdf`. **Total pages**: 9 (pp. 1–8 body + references + biographies on p. 9).
- **Title**: Heterogeneous Multiplayer Reach-Avoid Differential Game under Partial Information.
- **Authors**: Zihao Ma (Beihang Univ., Inst. of Artificial Intelligence), Hao Liu (Senior Member, IEEE; Beihang Univ. + Zhongguancun Laboratory; corresponding author), Guanghui Wen (Senior Member, IEEE; Southeast Univ., School of Mathematics/Systems Science), Frank L. Lewis (Life Fellow, IEEE; UTA Research Institute).
- **Year**: not printed anywhere in the PDF (accepted-manuscript/early-access layout: no vol., no., pages, DOI, or received/accepted dates). Internal evidence dates it ≥ 2025: refs. [4] (IEEE TAC "to be published, 2025"), [19] (IEEE TAC vol. 70, no. 4, Apr. 2025), [22] (Automatica vol. 176, 2025) are cited. File name carries no year → Year = 2025 or later, **to verify**.
- **Venue**: running header on every page reads "IEEE/ASME TRANSACTIONS ON MECHA
[CONTRIBUTIONS]
1. **(Modeling/information)** A heterogeneous multiplayer reach-avoid differential game with an explicitly asymmetric information structure: pursuers know all evader speeds but only positions of *detected* evaders; evaders know all pursuer positions and speeds but not the sensing radii (p. 2, Sec. II-B). Non-anticipative patterns ([22]) are rejected because pre-detection evader states are inaccessible; a state-feedback partial-information pattern with a centralized coordinator is adopted instead.
2. **(Theory)** Closed-loop capture strategy (eq. (5), Lemma 1, p. 4) with a speed-ratio threshold $\alpha_{ij}\ge\sqrt{2}$ under which the pursuer can head straight to the optimal Apollonius point while provably keeping the evader inside its sensing disk; optimality "under exact velocity conditio
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion, $\dot{x}_{P_i}=v_{P_i}u_{P_i},\ x_{P_i}(0)=x^0_{P_i}$; $\dot{x}_{E_j}=v_{E_j}u_{E_j},\ x_{E_j}(0)=x^0_{E_j}$, $t\ge 0$, with headings $u_{P_i},u_{E_j}\in\mathcal{U}=\{u\in\mathbb{R}^2\,|\,\|u\|_2=1\ \text{or}\ u=0\}$ (players may stop). Geometry: play region $\Omega_{\text{play}}$ and target region $\Omega_{\text{tar}}$ separated by the affine hull of endpoints $\mathfrak{m},\mathfrak{n}$; the target line $\mathcal{T}$ is the segment $\overline{\mathfrak{mn}}$ of length $l$; origin fixed at $\mathfrak{m}$ (Figs. 1, 4, 5, 8: $\mathcal{T}$ horizontal, $\Omega_{\text{tar}}$ above, $\Omega_{\text{play}}$ below). Capture iff $\|x_{P_i}-x_{E_j}\|_2=0$ (point capture). Termination: all evaders captured or having reached $\mathcal{T}$.
- **Information structure (Sec. II-B)**: pursuer $P_i$'s partial information set $I_{P_i}(t)=\{x_{P_i},v_{P_i},r_i\}\cup\
[CITATION]
This paper occupies the intersection of three threads in the skill's literature: analytical-barrier multiplayer reach-avoid games (Yan et al. [8]; Yan et al. Automatica [11]; Chen–Zhou–Tomlin [9]), sensing-limited pursuit ([6], [7], [13]), and geometric target-guarding with one-Apollonius-circle strategies (Dorothy et al. [17]; Fu–Liu [16]; Lee–Bakolas [12], [18]). Its distinctive assets for citing are: (i) the **conservative barrier** construction — a radius-free, ratio-only barrier evaluated a

### P065 — Optimal Evasion from a Sensing-Limited Pursuer
[BIBLIO]
- **ID**: P065. **Source file**: `D:\System\zhuomian\game-paper\Maity 等 - 2024 - Optimal Evasion from a Sensing-Limited Pursuer.pdf`. **Total pages**: 8 (printed pp. 2758–2765; Secs. I–VI pp. 1–5, Secs. VI–VIII + References + Appendix A start p. 6–7, Appendices A–C p. 7–8).
- **Title**: Optimal Evasion from a Sensing-Limited Pursuer.
- **Authors**: Dipankar Maity (Dept. of Electrical and Computer Engineering, and affiliated faculty, North Carolina Battery Complexity, Autonomous Vehicle, and Electrification Research Center (BATT CAVE), University of North Carolina at Charlotte, NC 28223, USA; dmaity@charlotte.edu); Alexander Von Moll (Control Science Center, Air Force Research Laboratory, WPAFB, OH 45433, USA); Daigo Shishika (Dept. of Mechanical Engineering, George Mason University, Fairfax, VA 22030, USA); Michael Dorothy (Army Research Directorate, DEVCOM Army Research Laboratory, APG, MD 20783, USA).
- **Year**: 2024. **Venue (exact from running header/copyright, p. 1)**: "2024 American Control Conference (ACC)", "July 8-12, 2024. Toronto, Canada", footer "979-8-3503-8265-5/$31.00
[CONTRIBUTIONS]
1. **(Modeling)** Extraction of a clean subproblem of the intermittent-sensing PEG: fixed-heading pursuer, evader best response over a fixed window, in a pursuer-fixed frame with a state constraint $S(x)=\|x\|-1\ge 0$ (eqs. (1)–(3), p. 1), plus the two-layer problem stack (fixed-$T$ OCP; Nash game over $T$, p. 1).
2. **(Theory, geometry)** Complete characterization of the fixed-$T$ optimal evasion policy: either a single constant-heading straight line (Lemma 4, eq. (19), p. 3) or a three-phase trajectory — tangent entry, boundary riding, tangential exit (Theorems 1–2, Lemma 6, pp. 4–6), with the riding time given by an elliptic integral (eq. (25), p. 5) and the optimal final distance in closed form $d_f^*=\mu/\cos\theta_{exit}$ (eq. (34), p. 5).
3. **(Theory, reachability)** Necessary and 
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 1)**: inertial frame, $\dot x_P = v_P[1\ 0]^T$ (P moves along $+x$ at constant speed, no control), $\dot x_E = v_E[\cos\psi\ \sin\psi]^T$; $v_E<v_P$, $\psi(t)$ is E's instantaneous heading. Normalization (footnote 1, p. 1): $\bar x_i(t)=\frac{1}{r_{cap}}x_i(\frac{r_{cap}}{v_P}t)$, $\mu=v_E/v_P<1$, capture radius $\to 1$; i.e., WLOG $v_P=1$, $v_E=\mu$, $r_{cap}=1$ (the footnote prints $\dot{\bar x}_P=[-1\ 0]^T$, a sign slip for P's own scaled velocity; the $-1$ drift is correct only in the relative frame).
- **Pursuer-fixed frame (eq. (2), p. 1)**: $x=x_E-x_P=[x\ y]^T$, $\dot x = [\mu\cos\psi-1,\ \mu\sin\psi]^T$, $x(0)=x_0$. E's relative velocity always has non-positive $x$-component.
- **State constraint (eq. (3), p. 1)**: $S(x)=\|x\|-1\ge 0$ for all $t\in[0,T]$ (E must stay on/outside the Proximity Circle of radius 1 centered at the origin of the relative frame
[CITATION]
**Paragraph role**: this is the canonical *building-block* reference for intermittent-sensing pursuit–evasion: whenever a paper models a pursuer that senses only intermittently (event-/self-triggered sensing, costly communication, limited-range passive detection plus scheduled active looks), the inter-observation window reduces to exactly this fixed-horizon, state-constrained evasion problem, and P065 supplies the complete best-response catalog — no-escape zone $\Omega_{capture}$ with exact surv

### P066 — Area-Optimal Control Strategies for Heterogeneous Multi-Agent Pursuit
[BIBLIO]
- **ID**: P066 | **Source file**: `D:\System\zhuomian\game-paper\Mammadov和Ranasinghe - 2026 - Area-Optimal Control Strategies for Heterogeneous Multi-Agent Pursuit.pdf` | **Total pages**: 8 (pp. 17145–17152 of the AAAI-26 proceedings; 7 content pages + 1 references page).
- **Title**: Area-Optimal Control Strategies for Heterogeneous Multi-Agent Pursuit
- **Authors**: Kamal Mammadov and Damith C. Ranasinghe, School of Computer and Mathematical Sciences, the University of Adelaide (emails printed on p. 1: kamal.mammadov@adelaide.edu.au, damith.ranasinghe@adelaide.edu.au).
- **Year**: 2026 (copyright block p. 1: "Copyright © 2026, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved.").
- **Venue**: running header on every page: "The Fortieth AAAI Conference on Artificial Intelligence (AAAI-26)"; PDF subject metadata repeats it. Indexer guess AAAI-26 **resolves exactly**: this is the main AAAI-26 conference proceedings (proceedings page numbers 17145–17152, AAAI copyright), not a workshop. No DOI printed anywhere. PDF keyword metadata lists AAA
[CONTRIBUTIONS]
1. **Modeling (zero-sum game on the area rate)**: formulation of multi-pursuer cooperative capture as the instantaneous min–max game $\min_{\{u_i\}} \max_v \dot A_e(t)$ (eq. (8), p. 3) over the area of the evader's safe-reachable set $S_e(t) = \bigcap_{i=1}^N B_i(t)$ of Apollonius discs (eqs. (3), (11)), with the value $\dot A_e = V_e\|F_e\| - \sum_i V_i\|F_{p_i}\|$ (eq. (10)) — a "direct competition between the weighted magnitudes of the area gradients" (p. 3).
2. **Theory (main contribution)**: analytical derivation of the area gradients $\nabla_{p_i} A_e$ and $\nabla_e A_e$ for the intersection of $N$ Apollonius discs **without any closed-form area formula**, by a coordinate-independent Leibniz integral rule on level-set functions (pp. 4–6): level-set gradients (Proposition 1.3, eqs. (1
[RESULTS-LIST]
- **Dynamics (eq. (1a–b), p. 2)**: $\dot p_i(t) = V_i u_i(t)$, $\|u_i(t)\| \le 1$; $\dot e(t) = V_e v(t)$, $\|v(t)\| \le 1$ — simple kinematic point masses, control = instantaneous heading (unit-norm). Constant maximum speeds $V_i$, $V_e$.
- **Key assumption**: $V_i > V_e$ for all $i \in \{1,\dots,N\}$ ("a critical assumption for capture to be feasible", p. 2). Speed ratio $\alpha_i := V_e/V_i \in (0,1)$.
- **Information structure**: deterministic, full information; the controls below are state-feedback maps of all agent positions (the arcs/centroids require global geometry).
- **Apollonius disc (eq. (2a–b), p. 2)**: $c_i(t) = \frac{V_i^2}{V_i^2 - V_e^2} e(t) + \frac{V_e^2}{V_e^2 - V_i^2} p_i(t)$, $\; r_i(t) = \frac{V_i V_e}{|V_i^2 - V_e^2|} \|e(t) - p_i(t)\|$ — the locus of points the evader reaches no later than pursuer $i$; interior = points reached strictly before. Equivalent forms p
[CITATION]
**Paragraph role**: this is the heterogeneous-speed extension of the area-based cooperative pursuit framework (Shah–Schwager 2019), published as an AAAI-26 main-track paper. In the knowledge base it serves as (i) the canonical reference for the **Apollonius-disc-intersection safe-reachable set** and its active-arc/centroid computation (Lemmas 1.2, Theorem 1.4), (ii) a clean worked example of deriving area gradients of implicitly defined sets via the **Leibniz integral rule / Reynolds transport t

### P067 — Optimal Defense Strategy under Partial Information in One-Versus-One Reach-Avoid Game
[BIBLIO]
- **ID**: P067 / **source file**: `Ma和Liu - 2025 - Optimal Defense Strategy under Partial Information in One-Versus-One Reach-Avoid Game.pdf` / **total pages**: 8.
  - The assigned file is the *review attachment* of an IEEE TCST submission: every page is stamped "Limited circulation. For review only — IEEE TCST Submission no.: 25-0189.1 — Preprint submitted to IEEE Transactions on Control Systems Technology. Received: February 19, 2025"; PDF metadata: "Attachment to Review 42609. Uploaded Fri Apr 4 12:42:15 2025", subject "IEEE TCST Submission ID 25-0189". (A second, later revision of the same paper exists in the corpus as `Ma和Liu - Defense Strategy under Partial Information in One-Versus-One Reach-Avoid Game.pdf`, 8 pp., PDF created 2026-04-21, title without "Optimal"; this archive is based on the assigned 25-0189.1 file.)
- **Title**: Optimal Defense Strategy under Partial Information in One-Versus-One Reach-Avoid Game.
- **Authors**: Zihao Ma (Institute of Artificial Intelligence, Beihang University); Hao Liu (Senior Member, IEEE; Beihang University and Zhongguancun Laboratory); R
[CONTRIBUTIONS]
1. **Theory (complete information)**: closed-form barrier $B(\mathbf{x}_P)=F_1\cup F_2\cup F_3$ (eq. (5)) for a straight target line, and **Theorem 1**: the deployment position minimizing the area of the evasion winning region is the target-line midpoint $\mathbf{x}_{opt}^c=(l/2,0)$, proved analytically via convexity (Hessian, eq. (9)), Lagrange multipliers, the mean value theorem for integrals (eq. (14)) and monotonicity arguments (eqs. (10)–(17)).
2. **Modeling (partial information)**: introduction of two new concepts — the **pursuit sensing winning region** $\mathcal{W}_P^\mathcal{S}=\mathcal{W}_P^\mathcal{B}\cap\mathcal{S}$ and the **fuzzy region** $\mathcal{F}=\mathcal{W}_P^\mathcal{B}-\mathcal{S}$ (Definition 2, p. 5) — and of the partial-information winning regions $\mathcal{W}_P^*$
[RESULTS-LIST]
- **Dynamics (eq. (1))**: Isaacs "simple motion" mass points, $\dot{\mathbf{x}}_P=v_P\mathbf{u}_P$, $\dot{\mathbf{x}}_E=v_E\mathbf{u}_E$, controls $\mathbf{u}_P,\mathbf{u}_E\in\mathcal{U}=\{\mathbf{u}\in\mathbb{R}^2\,|\,\|\mathbf{u}\|_2=1 \text{ or } \mathbf{u}=\mathbf{0}\}$ (instantaneous heading change; stopping allowed).
- **Domain**: $\mathcal{T}$ a segment with $\|\mathbf{m}-\mathbf{n}\|_2=l$; the affine hull splits $\mathbb{R}^2$ into target region $\Omega_{tar}$ and play region $\Omega_{play}$; origin at endpoint $\mathbf{m}$. Printed typo: "the target line belongs to the target region $\Omega_{play}$" (p. 2) — the highlighted $\Omega_{play}$ must be $\Omega_{tar}$; the *extension* of the line belongs to $\Omega_{play}$ (crossing the extension does not win).
- **Information (p. 2, below eq. (2))**: $I_P(t)=\{\mathbf{x}_P,\mathbf{v}_P,\mathbf{v}_E\}\cup\{\mathbf{x}_E\,|\,\mathbf{x}
[CITATION]
**Role**: this is the corpus's most direct treatment of *how a faster defender should choose its guarding position when it cannot see the whole game*: it couples the Yan-et al.-style analytical barrier for a straight target with a finite sensing radius, contributes the fuzzy-region / pursuit-sensing-winning-region vocabulary, and gives a closed-form deployment rule with a phase transition at $R^\alpha=(1+\alpha^{-1})l/2$ (guard the midpoint vs retreat to the barrier-tangency depth $r/(\alpha^{-1

### P069 — Pursuit–evasion games in the presence of obstacles
[BIBLIO]
- **ID**: P069. **Source file**: `D:\System\zhuomian\game-paper\Oyler 等 - 2016 - Pursuit–evasion games in the presence of obstacles.pdf`. **Total pages**: 11 (journal pp. 1–11).
- **Title**: Pursuit–evasion games in the presence of obstacles.
- **Authors**: Dave W. Oyler, Pierre T. Kabamba (deceased September 20, 2014 — noted in footnote 1), Anouck R. Girard. Affiliation: University of Michigan, Department of Aerospace Engineering, United States.
- **Year**: 2016 (issue date; available online 5 December 2015; copyright 2015 Elsevier Ltd.).
- **Venue (EXACT from header)**: Automatica, Volume 65 (2016), pages 1–11. **DOI (printed)**: 10.1016/j.automatica.2015.11.018. Indexer guess "Automatica" is **correct** — confirmed from page header "Automatica 65 (2016) 1–11" and footer "0005-1098/© 2015 Elsevier Ltd".
- **Tier**: **T1** (Automatica confirmed; no disagreement).
- **Other printed metadata**: This research supported in part by United States Air Force grant FA 8650-07-2-3744. Material partially presented at the 53rd IEEE Conference on Decision and Control, December 15–17, 2014, Los A
[CONTRIBUTIONS]
As listed verbatim in Section 1.5 (C1–C8), reorganized by type:
1. **Theory — dominance partition with obstacles (C1)**: Theorem 6: the plane is exhaustively divided into three disjoint regions (P strictly dominates / E strictly dominates / neither dominates), and the third region is obtained by intersecting bundles of isochrones.
2. **Theory — closed-form boundary (C2)**: Theorem 7 + Remark 1: every piece of the dominance boundary is a generalized Apollonius curve (limaçon, Apollonius circle, or vertex-centered circle) parameterized by the final-segment geometry; singular surfaces (type-(p,u,p) lines and hyperbolic dispersal surfaces) organize the assembly of the solution "in the large".
3. **Modeling / analysis (C3)**: comparative study of dominance regions with vs. without obstacles — a
[RESULTS-LIST]
- **Theorem 1 (p. 4)**: Without obstacles, time-optimal paths are straight lines and isochrones are concentric circles centered at the agent's initial location. *Proof approach*: wavefront propagation (Mitchell 1993). *Meaning*: recovers the classical setting.
- **Theorem 2 (p. 4)**: With polygonal obstacles, time-optimal paths are broken lines breaking at obstacle vertices, and isochrones are arcs of concentric circles centered at generating points. *Proof approach*: simulated wavefront propagation (continuous Dijkstra). *Meaning*: the crucial structural fact — even with obstacles, every isochrone piece is a circular arc about a *known* center, so pairwise isochrone intersections are analytically tractable. *Extensibility*: holds for arbitrary polygonal obstacle sets; used verbatim for polygonal (Section 5.1) and asymmetric (Section 5.2) obstacles.
- **Theorem 3 (p. 4)**: The curves sep
[CITATION]
This is the canonical reference for **dominance regions in PE games with obstacles**: it establishes (i) the equal-time (isochrone-intersection) characterization of the dominance boundary, (ii) the obstacle-modified closed-form boundary pieces — Apollonius circle generalized to **limaçons** and vertex-centered circles indexed by final-segment start-time offsets (Theorem 7), and (iii) the singular-surface architecture (type-(p,u,p) lines and hyperbolic dispersal surfaces, Remark 1) that organizes

### P070 — A Region-Based Relay Pursuit Scheme for a Pursuit–Evasion Game With a Single Evader and Multiple Pursuers
[BIBLIO]
- **ID**: P070
- **Source file**: `D:\System\zhuomian\game-paper\Pan和Yuan - 2023 - A Region-Based Relay Pursuit Scheme for a Pursuit–Evasion Game With a Single Evade.pdf` (filename truncated; full title from p. 1. PDF flagged "password-protected" by the reader but opens normally; full text + key pages extracted/rendered with pymupdf, 200 dpi).
- **Total pages**: 12 PDF pages = journal pp. 1958–1969 (all 12 read: body pp. 1958–1968, references pp. 1968–1969, author bios p. 1969).
- **Title**: A Region-Based Relay Pursuit Scheme for a Pursuit–Evasion Game With a Single Evader and Multiple Pursuers
- **Authors**: Tuyu Pan and Yuan Yuan (Senior Member, IEEE; corresponding author), School of Astronautics, Northwestern Polytechnical University, Xi'an 710072, China (e-mails printed: pan_tuyu@163.com; snowkey@aliyun.com).
- **Year**: 2023 (issue date). Manuscript received 14 June 2022; revised 14 September 2022; accepted 19 September 2022; date of publication 3 October 2022; date of current version 16 February 2023. Recommended by Associate Editor M. Perc. Funding: NSFC Grants 62122063 and 6
[CONTRIBUTIONS]
1. **Theory — round pursuit strategy (Definition 5, eqs. (7)–(8); Proposition 1)**: a quickest-descent control law $u_R=\lambda/\|\lambda\|$ with $\lambda=r_1\cos\theta/\|r_1\|+r_2/\|r_2\|$ that minimizes the second derivative of $\|r_2(t)\|$ (evader–static-pursuer distance) at every instant; geometrically, the active pursuer $P_1$ moves *perpendicular* to its line of sight ("round" $E$) until $P_1,E,P_2$ are co-linear ($\theta=0$), then chases head-on so that the **static** $P_2$ makes the capture (Remark 3, p. 1961).
2. **Theory — capture guarantee (Proposition 2, eq. (16))**: a closed-form sufficient condition on the initial geometry, $|\theta_0|<\frac{v_p}{v_e}\big(\frac{c_1+c_2}{c_2}\big)\ln\!\big(\frac{c_1+c_2}{c_1}\big)-\frac{v_p}{v_e}$, under which the round pursuit strategy forces
[RESULTS-LIST]
- **Dynamics (1)**: $\dot x_{p_i}(t)=v_p u_{p_i}(t)$, $\dot x_e(t)=v_e u_e(t)$, all controls in $\mathcal U=\{u\in\mathbb R^2:\|u\|\le1\}$; $v_p,v_e$ are maximum speeds. Pure kinematics (single integrators).
- **Information structure**: pursuers know all positions ($u_P$, $u_R$ depend on $x_e,x_{p_\sigma},x_{p_\tau}$); the evader is assumed to know the *active* pursuer's position (Remark 1, citing [3]) and plays $u_e=u_P(x_e,x_{p_\sigma})$ (Assumption 1). Static pursuers' positions are *not* used by the evader — the key behavioral asymmetry the scheme exploits. No communication/graph constraints, no delays.
- **Capture (Definition 1, eq. (2))**: $\sum_{i=1}^N\|x_{p_i}(t_f)-x_e(t_f)\|=0$. *Inconsistency to flag*: as written this demands **every** pursuer coincide with $E$; but the analysis on p. 1960 terminates when "E is captured by P1 **or** P2, i.e., $\|r_1(t_f)\|=0$ or $\|r_2(t_f)\|=0
[CITATION]
**Paragraph role**: P070 is the reference for *strategy-augmented relay pursuit* — the point in the literature where relay pursuit stops being "closest pursuer chases with pure pursuit" and becomes "active pursuer chooses between direct chase and steering the evader toward a static teammate, with switching regions carved by Voronoi lines, Apollonius circles, and a new Apollonius-like circle." It is the natural citation for (i) Quickest-descent/greedy steering laws as analytically tractable subst

### P071 — Target Defense against Sequentially Arriving Intruders
[BIBLIO]
- **ID**: P071
- **Source file**: `D:\System\zhuomian\game-paper\Pourghorban 等 - 2022 - Target Defense against Sequentially Arriving Intruders.pdf` (PDF flagged "password-protected" by the reader but `needs_pass = 0` in its trailer; full text + key pages extracted/rendered with pymupdf, 200–400 dpi).
- **Total pages**: 8 PDF pages = proceedings pp. 6594–6601 (all 8 read: body pp. 6594–6600, references p. 6601).
- **Title**: Target Defense against Sequentially Arriving Intruders
- **Authors**: Arman Pourghorban (ECE, University of North Carolina at Charlotte, NC 28223; apourgho@uncc.edu), Michael Dorothy (Computational and Information Sciences Directorate, Army Research Laboratory, APG, MD 20783), Daigo Shishika (Mechanical Engineering, George Mason University, Fairfax, VA 22030), Alexander Von Moll (Control Science Center, AFRL, WPAFB, OH 45433), Dipankar Maity (ECE, UNCC; dmaity@uncc.edu). Funding: ARL grant ARL DCIST CRA W911NF-17-2-0181 (p. 6594).
- **Year**: 2022 (conference held December 6–9, 2022).
- **Venue (exact, from header/copyright/footer)**: 2022 IEEE 61st Conference on 
[CONTRIBUTIONS]
1. **Modeling**: formulation of a sensing-limited target-defense game against *sequentially arriving* intruders, where the terminal state of each one-vs-one game (defender on the capture circle or at the target center) is the initial state of the next; intruders are equipped with a limited-range sensor ($\rho_A$) enabling evasive maneuver (p. 6595, contribution (i)).
2. **Theory — engagement surface and capture circle**: equilibrium strategy analysis via two new geometric constructs. The *engagement surface* $\mathcal S_{\text{engage}}$ (Definition 1, eq. (7)) is the set of (engagement time, engagement angle) pairs for which the Apollonius circle is exactly tangent to the target boundary — the favorable configurations to start the full-information phase; the *capture circle* (radius $r_T+2
[RESULTS-LIST]
- **Dynamics (1)**: $\dot x_A=v_A\hat u(\psi_A)$, $\dot x_D=v_D\hat u(\psi_D)$ — first-order (single-integrator) agents directly controlling speed and heading; $\hat u(\theta)=[\cos\theta,\sin\theta]^\top$; $|v_D|\le1$, $|v_A|\le\nu$, $\nu<1$ enforced (trivial outcome otherwise).
- **Information structure**: two phases defined by sensing. *Full information*: $\|x_A(t)\|<r_T+\rho_T$ **and** $\|x_A(t)-x_D(t)\|\le\rho_A$ (both agents see each other). *Partial/asymmetric information*: $\|x_A(t)\|<r_T+\rho_T$ and $\|x_A(t)-x_D(t)\|>\rho_A$ — the defender (through the target-as-sensor TSR) sees the intruder, the intruder does not see the defender. In the partial-information phase the intruder is *prescribed* to move radially toward the target center at maximum speed until first sensing the defender; footnote 1 (p. 6596) admits this is an assumption: deviating only lengthens the time spent insi
[CITATION]
**Paragraph role**: P071 is the reference point for *sequential (one-at-a-time) intruder target defense with cross-game state carry-over under partial information* — the direct extension of the partial-information TAD game [12] from a single intruder to an arrival process, and one of the few perimeter-defense papers where the intruder is strategic (sensing-enabled, evasive) rather than hard-wired straight-line (contrast [14]–[17]). Its durable technical assets are: (i) the **engagement surface**

### P072 — Pursuit-evasion game strategy of USV based on deep reinforcement learning in complex multi-obstacle environmen
[BIBLIO]
- **ID / source file / total pages**: P072 / `Qu 等 - 2023 - Pursuit-evasion game strategy of USV based on deep reinforcement learning in complex multi-obstacle.pdf` / 20 pages.
- **Title**: Pursuit-evasion game strategy of USV based on deep reinforcement learning in complex multi-obstacle environment.
- **Authors**: Xiuqing Qu, Wenhao Gan (co-first authors), Dalei Song (corresponding), Liqin Zhou — College of Engineering / Institute for Advanced Ocean Study, Ocean University of China, Qingdao.
- **Year / Venue**: 2023, **Ocean Engineering**, Vol. 273, Article 114016 (header exactly: "Ocean Engineering 273 (2023) 114016"; indexer guess *Ocean Engineering* — **correct**). DOI printed: 10.1016/j.oceaneng.2023.114016. Received 2 Dec 2022; revised 5 Feb 2023; accepted 15 Feb 2023; online 24 Feb 2023. © 2023 Elsevier Ltd. Funding: Fundamental Research Funds for the Central Universities (201962010); National Key R&D Program of China (2017YFC0305803).
- **Tier**: T2 (as assigned). No disagreement to record: Ocean Engineering is Elsevier's leading applied ocean/marine-engineering journal (Q1 
[CONTRIBUTIONS]
1. **Environment + USV modeling**: a 6-DOF kinematic/dynamic USV model (Fossen-style, Eqs. (1)–(5)) realized in Unity3D's physics engine, plus a multi-obstacle battle-space model with ray-sensor (pursuer "sonar", FOV 120°, 50 m) and grid-sensor (evader "radar", 5 m resolution, 140 m width) perception (Secs. 2.1–2.2).
2. **Game-theoretic MDP/POMDP formulation** with task-specific action spaces (Eq. (11)), separate pursuit/escape state spaces coupled to the capture conditions (Eqs. (12)–(18)), and shaped dense reward functions encoding simultaneous-arrival encirclement (Eqs. (19)–(26)).
3. **Pursuit algorithm**: CTDE training with the MA-POCA actor–critic (counterfactual COMA-style credit assignment with residual self-attention critic, Eqs. (27)–(32)) so that each pursuing USV is rewarded by
[RESULTS-LIST]
- **States (p. 3, Eq. (1))**: η1=[x,y,z]^T, η2=[φ,θ,ψ]^T (roll, pitch, yaw), η=[η1,η2]^T; V=[u,v,w]^T, W=[p,q,r]^T, ν=[V,W]^T — 6 DOF between geodetic frame E0 and hull frame B0 (Table 1).
- **Kinematics (p. 3, Eqs. (2)–(3))**: [η̇1; η̇2] = blkdiag(R_EB1(η2), R_EB2(η2))·[V; W]. R_EB2(η2) = [[1, sinφ tanθ, cosφ tanθ],[0, cosφ, −sinφ],[0, sinφ secθ, cosφ secθ]] (standard z-y-x Euler transform). **Proof gap (typo) in Eq. (2) as printed**: R_EB1(η2) row 1 is printed as [cosψcosθ, cosψsinθsinφ − sinψ**cosθ**, cosψsinθsinφ + sinψ**sinθ**] and row 2 col 3 as sinψ**sinθ**sinφ − cosψsinφ; the standard Fossen rotation requires cosφ/sinφ in those slots (row1: [cψcθ, cψsθsφ − sψcφ, cψsθcφ + sψsφ]; row2 col3: sψsθcφ − cψsφ). The printed matrix is not a valid rotation matrix as typeset; clearly θ/φ subscripts were swapped in production.
- **Dynamics (p. 3, Eq. (4))**: (M_RB + M_A)ν̇_r + (C_RB(ν_r) + C
[CITATION]
**Role in a paper's related-work section**: the canonical citation for *learning-based multi-USV pursuit-evasion in obstacle-rich marine environments with adversarial co-evolution* — i.e., the applied/engineering wing of PE-game research, contrasting with analytic pursuit papers (Apollonius/barrier/reach-avoid). It is also a usable reference for: MA-POCA/CTDE credit assignment in marine agents, PPO+BC+GAIL hybrid escape policies, curriculum + adversarial-evolutionary training against overfitting

### P073 — Construction of the Barrier for Reach-Avoid Differential Games in Three-Dimensional Space with Four Equal-Spee
[BIBLIO]
- **ID**: P073
- **Source file**: `D:\System\zhuomian\game-paper\R. Yan 等 - 2019 - Construction of the Barrier for Reach-Avoid Differential Games in Three-Dimensional Space with Four.pdf` (filename truncated; full title from p. 1. PDF opens normally; full text extracted and all 6 pages rendered to PNG at 200 dpi with pymupdf; every formula below checked against the renders).
- **Total pages**: 6 PDF pages (all read: body and theorems pp. 1–5, Algorithm 1 + conclusion + references p. 6).
- **Title**: Construction of the Barrier for Reach-Avoid Differential Games in Three-Dimensional Space with Four Equal-Speed Players
- **Authors**: Rui Yan, Zongying Shi and Yisheng Zhong — Tsinghua National Laboratory for Information Science and Technology (TNList); Department of Automation, Tsinghua University, Beijing 100084, China (footnote, p. 1; e-mails as printed: yr15@mails.tsinghua.edu.cn and {szy, zys-dau}@mail.tsinghua.edu.cn).
- **Year**: 2019. **Venue (EXACT, as printed in the PDF)**: the only venue marking is the left-margin stamp on p. 1: **arXiv:1904.02810v1 [math.OC] 4 Apr 2019**. No 
[CONTRIBUTIONS]
As stated on p. 1 and verified in the body:
1. **Theory — contribution/contribution classification conditions**: necessary and sufficient conditions determining *which pursuers* contribute to the barrier — Lemma 2 (eq. (8), two pursuers, p. 3) and Lemma 3 (eqs. (11)–(13), three pursuers, p. 4), introducing the notions of **active pursuer** and of barriers dependent on one/two/three pursuers.
2. **Theory — complete closed-form 3D barrier and winning subspaces with all pursuer cooperations**: Lemma 1 + eq. (7) (one pursuer: point/ray geometry), Theorem 1 + eqs. (9)–(10) (two active pursuers: mirror points + circular arc), Theorem 2 + eq. (14) (three collinear-projection pursuers: union of two two-pursuer barriers), Theorem 3 + eqs. (15)–(16) (three noncollinear-projection pursuers: **spheric
[RESULTS-LIST]
- **Game space (eq. (1))**: $\mathcal T=\{z\in\mathbb R^3 \mid K^Tz=b\}$ (target plane, TP), $\Omega_{\mathrm{goal}}=\{z\mid K^Tz<b\}$, $\Omega_{\mathrm{play}}=\{z\mid K^Tz>b\}$, with known $K\in\mathbb R^3$, $K\ne0$, $b\in\mathbb R$.
- **Dynamics (eq. (2))**: $\dot x_{P_i}(t)=p_i(t),\ x_{P_i}(0)=x_{P_i}^0$, $i=1,2,3$; $\dot x_E(t)=e(t),\ x_E(0)=x_E^0$; controls are instantaneous unit headings $p_i, e \in \mathcal U=\{u\in\mathbb R^3 \mid \|u\|_2=1\}$ ("Eculidean norm" [sic]). **Equal unit speed** for all four players; simple motion. Whole state space $\mathbb R^{12}$.
- **Termination / winning conditions**: capture $\iff$ distance from $E$ to the *closest* pursuer $=0$; $E$ wins iff it reaches $\Omega_{\mathrm{goal}}$ before capture; the pursuer team wins iff $E$ is captured in $\Omega_{\mathrm{play}}$ (p. 2). Since reaching $\Omega_{\mathrm{goal}}$ requires crossing $\mathcal T$, the e
[CITATION]
**Paragraph role**: P073 is the reference for the **3D equal-speed multiplayer reach-avoid barrier built from bisector-plane geometry** — the point in the literature where the barrier of a cooperating pursuer team stops being a 2D Apollonius/bisector arc (same authors' P099, IEEE TCYB 2019, their ref [18]) and becomes a **net of spherical patches**: mirror points for one pursuer, a circular arc in the vertical plane for two, a spherical patch over the pursuers' projection triangle for three (The

### P075 — Multiple Pursuers Multiple Evaders Reach-Avoid Games in 3D Space via Analytic Barriers
[BIBLIO]
- ID: P075 / source file: `Ruan 等 - 2026 - Multiple Pursuers Multiple Evaders Reach-Avoid Games in 3D Space via Analytic Barriers.pdf` / total pages: 12 (journal pp. 81–92). Note: the Read tool flags the PDF as password-protected, but pymupdf opens it with `is_encrypted = False`; text + 200-dpi page renders were used for full verification.
- Title: **Multiple Pursuers Multiple Evaders Reach-Avoid Games in 3D Space via Analytic Barriers**
- Authors: Wanying Ruan (School of Electrical and Electronic Engineering, Shijiazhuang Tiedao University, Shijiazhuang 050043, P.R. China); Yongbin Sun (corresponding author; School of Automation Science and Electrical Engineering, State Key Laboratory of Virtual Reality Technology and Systems, Beihang University, Beijing 100083, P.R. China); Lingchen You (Beihang); Siyuan Wang (Beihang). ORCIDs printed: Ruan 0000-0002-1482-257X, Sun 0000-0002-6582-9958, You 0000-0001-6903-3538, Wang 0000-0002-4351-4832.
- Year: 2026 (Received 4 March 2025; Revised 21 July 2025; Accepted 22 July 2025; Published 22 August 2025)
- Venue (EXACT, from header/copyright, r
[CONTRIBUTIONS]
1. **Theory (game of kind):** introduction of the **Apollonius sphere** in 3D; closed-form optimal interception points (OIP) and **analytic barrier expressions for 1-vs-1 (eq. (13)) and 2-vs-1 (Theorem 2, eqs. (15)–(17))**, claimed as "the first successful derivation of the analytical solution in 3D space" (abstract, p. 81).
2. **Theory (game of degree):** optimal feedback headings for pursuers and evaders inside the pursuer winning region W_P (eq. (32)), plus Theorem 1 (straight-line optimal trajectories via PMP, eqs. (9)–(10)). The contributions list additionally claims "the proof that the value function is continuously differentiable and satisfies the HJI partial differential equations is presented" (p. 82) — **not substantiated in the paper body** (see §7).
3. **Algorithm:** the optima
[RESULTS-LIST]
- **Dynamics (eq. (1)), simple motion in R³:** ẋ_Pi = V_Pi u_Pi, ẏ_Pi = V_Pi v_Pi, ż_Pi = V_Pi w_Pi; ẋ_Ej = V_Ej u_Ej, ẏ_Ej = V_Ej v_Ej, ż_Ej = V_Ej w_Ej. Controls are instantaneous headings u_Pi = (u,v,w)_Pi ∈ R³ (similarly u_Ej); players are holonomic; global state x = {x_Pi, x_Ej} ∈ R^{3(N+M)}. Speeds V_Pi > 0, V_Ej > 0, heterogeneous allowed.
- **Assumption 1 (p. 83):** every pursuer faster than every evader: V_Pi > V_Ej; speed ratio γ_ij = V_Ej/V_Pi < 1.
- **Information structure (p. 83):** each player knows only opponents' positions and speeds (not controls); strategies are state-feedback based. Assignment binary α_ij = 1 iff P_i is assigned to E_j; one pursuer per evader; **pursuers firmly commit to their initial assignment without changing**. Point capture: ‖x_Pi − x_Ej‖₂ = 0.
- **Terminal set (eqs. (2)–(4)):** D := D_P ∪ D_E; D_P = {x : x_Pi = x_Ej, ∀j, ∃i, α_ij = 1} (all evader
[CITATION]
**Paragraph role:** use in the Related Work of an IEEE Trans paper on multiplayer reach-avoid / target-defense games, in the sentence cluster on (i) 3D extensions and (ii) analytic-barrier constructions, right after 2D Apollonius-circle results (Garcia et al., Chen–Tomlin) and next to Yan et al.'s 3D evasion-space work. It is the reference to cite for "closed-form 3D barriers up to two-pursuer cooperation via Apollonius spheres, with barrier-measure-driven assignment by bipartite matching." Hone

### P076 — Time-optimal Escape of an Omnidirectional Agent from the Field of View of a Differential Drive Robot
[BIBLIO]
- **ID**: P076. **Source file**: `D:\System\zhuomian\game-paper\Ruiz - 2023 - Time-optimal Escape of an Omnidirectional Agent from the Field of View of a Differential Drive Robot.pdf` (filename complete; title matches p. 1). **Total pages**: 14 (PDF pp. 1–14 = printed journal pp. 292–305).
- **Title**: Time-optimal Escape of an Omnidirectional Agent from the Field of View of a Differential Drive Robot.
- **Authors**: Ubaldo Ruiz (single author) — Centro de Investigación Científica y de Educación Superior de Ensenada (CICESE), Ensenada 22860, Baja California, México (uruiz@cicese.mx); also with Consejo Nacional de Ciencia y Tecnología (CONACYT), Cd. de México 03940, México (footnote, p. 292). Ph.D. from CIMAT (2013), postdoc U. Minnesota 2013–2014 (bio note, p. 305).
- **Year**: 2023. **Venue** (exact, from header/copyright, p. 292): "International Journal of Control, Automation, and Systems 21(1) (2023) 292-305"; ISSN 1598-6446, eISSN 2005-4092; "©ICROS, KIEE and Springer 2023". **DOI** (printed, p. 292): 10.1007/s12555-021-0686-8. **Indexer guess "International Journal of Control" i
[CONTRIBUTIONS]
1. **Game-of-kind criterion (theory)**: escape is decided by the speed ratio alone — if $V_a^{\max}\le V_r^{\max}/b$ the DDR keeps the OA under surveillance forever (rotate in place at max speed); if $V_a^{\max}>V_r^{\max}/b$ the OA escapes from any valid initial configuration; there is no barrier splitting the state space into two outcome regions (pp. 293, 297, 300).
2. **Singular-surface taxonomy (theory)**: five singular surfaces are exhibited — an evader's dispersal surface (EDS), an evader's state constraint surface (ESCS), a pursuer's equivocal surface (PES), a pursuer's dispersal surface (PDS), and a pursuer's state constraint surface (PSCS) (pp. 294, 297–298, 300–302; Figs. 2–3).
3. **Partition of the playing space (theory/modeling)**: four regions I–IV, each with explicit time-opt
[RESULTS-LIST]

[CITATION]
This paper is the knowledge base's reference for the **DDR-vs-OA surveillance-evasion game with a cone field of view**, completing Ruiz's OA/DDR tetralogy ([P3-adjacent T-RO 2013 capture; IJC 2016 role reversal; IJC 2022 circular surveillance; this paper conical FoV]). Its citable assets are: the speed-ratio winner criterion ($V_a^{\max}\lessgtr V_r^{\max}/b$) with the "no barrier — single outcome region" finding; the closed-form primary/ESCS-tributary trajectories (32)/(41) with their implicit 

### P077 — Feedback Strategies for a Reach-Avoid Game With a Single Evader and Multiple Pursuers
[BIBLIO]
- **ID**: P077
- **Source file**: `D:\System\zhuomian\game-paper\Selvakumar和Bakolas - 2021 - Feedback Strategies for a Reach-Avoid Game With a Single Evader and Multiple Pursuers.pdf` (12 PDF pages = journal pp. 696–707; below, "p. X" = printed journal page, i.e., PDF page X−695)
- **Title**: Feedback Strategies for a Reach-Avoid Game With a Single Evader and Multiple Pursuers
- **Authors**: Jhanani Selvakumar; Efstathios Bakolas (Dept. of Aerospace Engineering and Engineering Mechanics, University of Texas at Austin, Austin, TX 78712 USA; corresponding author: bakolas@austin.utexas.edu)
- **Year**: 2021 (issue date February 2021; published online May 17, 2019; manuscript received July 11, 2018, revised February 20, 2019, accepted April 29, 2019; supported by NSF Grant 1562339; recommended by Associate Editor S. E. Shimony)
- **Venue (EXACT, from header/copyright)**: IEEE Transactions on Cybernetics, Vol. 51, No. 2, February 2021, pp. 696–707. Copyright line "2168-2267 © 2019 IEEE". The indexer guess (IEEE Transactions on Cybernetics) is **correct**.
- **DOI (printed on p. 696)**: 10
[CONTRIBUTIONS]
1. **(Theory/metric)** A novel scalar **log-risk metric** β_i = log(φ_T/φ_s) (eq. (9), p. 700) for the two-player target-seeking evasion game, built from the minimum time-to-target φ_T = ‖x_T − x_e‖/v_e and the minimum **intercept** time φ_s of an evader that runs straight for the target (both closed-form via a quadratic equation, eq. (4)).
2. **(Theory/partition)** A partition of the augmented state space X = {z ∈ R⁴ : z = [x_e^T x_i^T]^T} into **safe (S)**, **failing (F)** and **risky (R)** open sets (Prop. 1, p. 699) determined by comparisons of φ_s, φ_c, φ_T; with closed-form circular boundaries of the evader-position projections S_e(x_i), F_e(x_i) (Prop. 2, p. 700) — the reach-avoid analogue of Apollonius-circle partitions, with circles centered at the target and at the pursuer.
3. **
[RESULTS-LIST]
- **Dynamics (eq. (1a)–(1b), p. 697)**: ẋ_i = v_{pi} u_i, x_i(0) = x̄_i; ẋ_e = v_e u_e, x_e(0) = x̄_e; u_i, u_e ∈ U = {u ∈ R² : ‖u‖ ≤ 1}; zero input used only after termination. Positions only (no velocity states).
- **Pursuer model (eq. (2), p. 698)**: relay pursuit — u*_j(x_e, x_j) = r_j/‖r_j‖ if j = i_c, else 0; r_j := x_e − x_j. The active index i_c is the argmin of the relay metric (least capture time over the team).
- **Range dynamics (eq. (3), p. 698)**: d‖r_i‖/dt = r_i^T(v_e u_e − v_{pi} u_i)/‖r_i‖, r_i(0) = x̄_e − x̄_i.
- **Min–max time-to-capture (eq. (4), p. 698)**: with optimal pursuit u_i = r_i/‖r_i‖ and optimal evasion u_e = r_i/‖r_i‖, φ_c(x_e, x_i) is the smallest positive real root of
- **Minimum intercept time**: φ_s(x_e, x_i, x_T) = smallest positive real root of (4) with u_e = (x_T − x_e)/‖x_T − x_e‖ (single quadratic equation, solved via [25]); it is the value of the 
[CITATION]
**Paragraph role.** P077 is a reference point for *analytical, risk-metric-based feedback evasion with terminal constraints* in multi-pursuer reach-avoid settings: it supplies (i) the log-risk metric β = log(φ_T/φ_s) and the safe/failing/risky partition defined purely by comparisons of closed-form capture/intercept/target times (Props. 1–2, eqs. (4)–(9)) — a lightweight, Apollonius-circle-like alternative to HJI-based reachable-set partitions; (ii) the quickest-descent switching feedback (eqs. (

### P078 — Min–Max Q-learning for multi-player pursuit-evasion games
[BIBLIO]
- **ID**: P078
- **Source file**: `D:\System\zhuomian\game-paper\Selvakumar和Bakolas - 2022 - Min–Max Q-learning for multi-player pursuit-evasion games.pdf` (14 pages; all read, key formulas verified against 200–300 dpi renders)
- **Title**: Min–Max Q-learning for multi-player pursuit-evasion games
- **Authors**: Jhanani Selvakumar; Efstathios Bakolas (corresponding author). Affiliation: The Department of Aerospace Engineering and Engineering Mechanics, The University of Texas at Austin, United States.
- **Year**: 2022 (copyright line "© 2021 Elsevier B.V. All rights reserved"; available online 22 December 2021)
- **Venue (EXACT, from printed header)**: *Neurocomputing*, Vol. 475 (2022), pp. 1–14, Elsevier B.V. ISSN 0925-2312. The indexer guess "Elsevier journal, likely Neural Networks or similar" is hereby **resolved exactly to Neurocomputing 475 (2022) 1–14** — the running header on every page and the ScienceDirect footer print "Neurocomputing 475 (2022) 1–14"; the "Communicated by" line reads "Communicated by Zidong Wang" (Neurocomputing uses "Communicated by" editors; Neural Netwo
[CONTRIBUTIONS]
1. **Modeling (game reduction)**: A systematic reduction of the (N+1)-player dynamic non-zero-sum reach-avoid game to a *sequence of two-player static zero-sum matrix games* — pursuer group treated as a single minimizer P that deploys exactly one pursuer per stage — each stage game solved as a primal–dual LP pair (eqs. (6)–(7)); existence of a mixed-strategy saddle point for the finite zero-sum multi-act game is invoked from [4].
2. **Modeling (invariant abstraction)**: A replacement payoff matrix M_k ∈ R^{N_p×N_e}$_{≥0}$ of *constant size 2×4* for any N, built from feature-based discrete actions: pursuer team actions {p1 relay pursuit, p2 all-pursuers-active} and evader actions {e1 pure evasion from nearest pursuer, e2 "collective evasion" toward the largest angular gap (eq. with bisector
[RESULTS-LIST]
- **Continuous dynamics (p. 2, eqs. (1a)–(1b))**: ẋ_i^c(t) = v_{p_i} u_i^c(t), x_i^c(0) = x_i^0; ẋ_e^c(t) = v_e u_e^c(t), x_e^c(0) = x_e^0, for t ∈ [0, T_f], domain D ⊂ R², i ∈ I := {1,…,N}; speeds v_{p_i} > 0, v_e > 0; input set U := {u ∈ R² : ‖u‖ = 1 or u = 0}; the zero input is used only after termination.
- **Discrete model (p. 3, eqs. (2a)–(2b))**: x_i^d(k+1) = x_i^d(k) + (v_{p_i}Δt) u_i^d(k); x_e^d(k+1) = x_e^d(k) + (v_eΔt) u_e^d(k), k ∈ {0,…,K̄}. Inputs are piecewise constant on [kΔt, (k+1)Δt); the game has at most K̄+1 stages and T_f := K̄Δt.
- **Exactness claim (p. 3)**: under the stated hold, x_i^d(k) = x_i^c(kΔt) and x_e^d(k) = x_e^c(kΔt); "the proposed discretization scheme for the continuous-time systems given in (1) is exact." *Verified*: trivially correct, since the input is constant on each interval and the integrator integrates it exactly (no Euler truncation error).
- *
[CITATION]
**Role in a paper's literature**: cite P078 in the reinforcement-learning-for-pursuit-evasion thread and in the matrix-game/abstraction thread: it is the clearest published instance of *minimax Q-learning used not to learn a control policy directly but to learn the entries of a per-stage payoff matrix* inside a zero-sum matrix-game reduction, with a deliberately player-count-invariant feature state (time-to-capture/intercept ratios over time-to-target) that enables cross-team-size transfer (trai

### P079 — Hybrid Predictive Network-Based Multiagent Reconnaissance Game with Limited Perception
[BIBLIO]
- **ID**: P079
- **Source file**: `D:\System\zhuomian\game-paper\Shen 等 - 2025 - Hybrid Predictive Network-Based Multiagent Reconnaissance Game with Limited Perception.pdf`
- **Total pages**: 14 (PDF; early-access article, no printed page numbers; author biographies occupy pp. 13–14)
- **Title**: Hybrid Predictive Network-Based Multiagent Reconnaissance Game with Limited Perception
- **Authors**: Xiangyuan Shen (School of Artificial Intelligence and Automation, Huazhong University of Science and Technology, Wuhan 430074, China); Bin Hu (corresponding author; School of Future Technology, South China University of Technology, Guangzhou 510641, and Guangdong Artificial Intelligence and Digital Economy Laboratory (Guangzhou)); Zhi-Hong Guan (HUST); Dingxue Zhang (School of Petroleum Engineering, Yangtze University, Jingzhou 434023); Tao Li (School of Electrical Engineering and Automation, Hubei Normal University, Huangshi 435002).
- **Year/Venue**: 2025. Every page footer prints: "This article has been accepted for publication in IEEE Transactions on Cognitive and Developmental Systems..
[CONTRIBUTIONS]
1. **Modeling**: A multi-stage (approach–reconnaissance–retreat) reconnaissance game cast as a partially observable Markov game with unequal sensing ranges and discrete action sets, plus a **phase-specific reward system** "grounded in game-theoretic decomposition and cognitive science": total payoff $J = J_{approach}+J_{recon}+J_{retreat}$ (eq. (25), p. 6) over three sub-games $\{G_{approach},G_{recon},G_{retreat}\}$, implemented via Table I and eqs. (26)–(28), with PFC-inspired interpretation of each term (p. 6–7).
2. **Architecture — ImpLSTM** (Sec. IV-A, p. 4): an LSTM variant "inspired by the prefrontal cortex temporal dependency processing mechanisms" in which forget/input gates use an impulse (Gaussian-erf) activation $\phi$ with a surrogate gradient $\phi'(u)=\frac{\alpha}{\sqrt{\pi
[RESULTS-LIST]
- **Dynamics/environment**: no continuous dynamics equations are given. The game is discrete-time with discrete action sets: red agents and blue agent 1 use $\{up, down, left, right, stop\}$; blue agent 2 additionally has diagonal moves (p. 9). Sensing: red agents and blue agent 1 have observation range 5 (Euclidean distance units in simulation), blue agent 2 has range 7 (p. 9); physical values 0.25 m / 0.25 m / 0.35 m with defender capture radius 0.15 m (p. 10).
- **Phases / termination / winning** (p. 3, p. 9): stage 1 approach, stage 2 reconnaissance ("The second stage lasts 10 time steps" in simulation; 3 s / 10 s / 20 s in the physical task), stage 3 retreat. Scouts win (+1) only if at least one scout completes reconnaissance of the target and returns to the safe zone without being captured; tie 0; loss −1; "The score changes only when scouts complete all stages." Capture is an abso
[CITATION]
This paper is the library's representative of the **learning-based, opponent-modeling branch of multi-stage reconnaissance/attack-defense games**: it complements the analytic line (Plante–Levis 1972; Lee–Bakolas 2023; capture-the-flag via HJI/Apollonius) by showing how a three-phase reach–observe–retreat mission with unequal sensing ranges, obstacles, and nonzero dwell time can be handled by an Actor–Critic method whose state is augmented with GAN-predicted defender trajectories, and it is one o

### P080 — Strategy Analysis and Design of Target-Attacker-Defender Game with Non-zero Capture Radius for Attacker Vehicl
[BIBLIO]
- **ID**: P080
- **Source file**: `D:\System\zhuomian\game-paper\Shi 等 - 2024 - Strategy Analysis and Design of Target-Attacker-Defender Game With Non-Zero Capture Radius for Attac.pdf` (filename truncated; full title taken from p. 1)
- **Total pages**: 13 (PDF; early-access author version, printed page numbers 1–13; pp. 12–13 references, p. 13 author biographies)
- **Title**: Strategy Analysis and Design of Target-Attacker-Defender Game with Non-zero Capture Radius for Attacker Vehicle
- **Authors**: Yibo Shi (Dept. of Control Science and Engineering, University of Shanghai for Science and Technology, Shanghai 200093, China; 221240072@st.usst.edu.cn); Chaoli Wang (Member, IEEE; corresponding author; USST; clwang@usst.edu.cn); Zhengtao Ding (Senior Member, IEEE; School of Electrical and Electronic Engineering, University of Manchester, Manchester M13 9PL, U.K.). Funding footnote (p. 1): NSFC 62173232, 62003214.
- **Year/Venue**: 2024. Running header on every page: *IEEE Transactions on Intelligent Vehicles*. Footer on every page: "This article has been accepted for publication in IEE
[CONTRIBUTIONS]
1. **Theory (Game of Degree, Theorem 1, p. 5)**: first optimal state-feedback strategies $(\beta^*,\delta^*,\zeta^*)$ (11)–(13) for the equal-speed TAD game with non-zero Attacker capture radius, together with the capture point $\mathbf z^*(\mathbf x)$ defined by the two scalar equations (14)–(15) and a $C^1$ value function (16) that is **proved** to satisfy the HJI equation (17), hence a state-feedback Nash (saddle-point) equilibrium — extending the $r=0$ HJI methodology of [8],[15] to $r>0$.
2. **Theory (Game of Kind, Theorem 2, p. 7–8)**: an explicit barrier characterization (50)–(51) built from (a) the **Attacker's ultimate (limiting) interception curve** $y=f(x)=\pm\sqrt{r^2-x^2}\,(1-x_A/x)$, $x\in[-r,0)$ (56) — the locus of points A can just capture when it is simultaneously intercep
[RESULTS-LIST]
- **Dynamics (1)**: Isaacs' simple motion, $\dot x_A=\cos\beta,\ \dot y_A=\sin\beta$; $\dot x_D=\cos\delta,\ \dot y_D=\sin\delta$; $\dot x_T=\gamma\cos\zeta,\ \dot y_T=\gamma\sin\zeta$, with initial conditions, $\mathbf x=(\mathbf x_A,\mathbf x_D,\mathbf x_T)\in\mathbb R^6$, controls $\beta,\delta,\zeta\in[-\pi,\pi]$ (Attacker/Defender/Target headings), speeds $V_A=V_D=1$, $V_T=\gamma$, $\gamma=V_T/V_A<1$ (p. 2–3).
- **Termination (2)–(4)**: $\mathcal T=\mathcal T_1\cup\mathcal T_2$; A captures T iff $\|\mathbf x_T-\mathbf x_A\|_2\le r$ (3); T–D wins iff $\|\mathbf x_D-\mathbf x_A\|_2=0$ (4) — **asymmetric radii**: only A has a non-zero capture radius.
- **Information structure** (p. 3): perfect-information differential game; all agents know (1) and the current state $\mathbf x(t)$, use causal (state-feedback) strategies, and do not know the opponents' current decisions — so no discrimin
[CITATION]
This paper is the capture-radius ($r>0$) extension of the equal-speed Garcia–Casbeer–Pachter TAD lineage: it keeps the [8]/[15] two-sided-PMP-plus-HJI machinery but replaces the Apollonius circle by the Apollonius oval (Lemma 1, (9)–(10), from Yan–Shi–Zhong's lifeline work [24]) and replaces the straight-line barrier test of [13]/[18] by a tangency test between the A–T oval and the Attacker's ultimate interception curve $y=\pm\sqrt{r^2-x^2}(1-x_A/x)$ on $x\in[-r,0)$ (56), yielding both a Game-of

### P081 — Determination of barrier surface in Target-Attacker-Defender game with capture radius for superior pursuer
[BIBLIO]
- **ID**: P081. **Source file**: `D:\System\zhuomian\game-paper\Shi 等 - 2025 - Determination of barrier surface in Target-Attacker-Defender game with capture radius for superior p.pdf`. **Total pages**: 9 (pp. 1–8 = article, p. 9 = author biographies). The Read tool flags the PDF as password-protected, but pymupdf reports `needs_pass=0` and opens it normally — same false-positive pattern as other PDFs in this collection; full text extracted and every key formula verified against 200-dpi page renders (pages 2–8).
- **Duplicate / variant**: the literature folder contains a **byte-identical** second copy, `D:\System\zhuomian\game-paper\Yibo Shi 等 - 2025 - Determination of barrier surface in Target-Attacker-Defender game with capture radius for superior p.pdf` (both files MD5 `7a90101845bf90a8351ea3dd48244015`, verified directly and matching `papers/manifest.json`). This copy is recorded as variant **P109 → P081**; `P109.md` is a stub pointing here (note: the P109 stub's phrase "different hashes" is inaccurate for this pair — the hashes are identical). Only P081 carries the full archive;
[CONTRIBUTIONS]
1. **Modeling**: TAD game of kind with non-zero capture radii for **both** $A$ and $D$ and a faster defender ($v_D > v_A > v_T$), terminal sets $\mathcal{L}_1$–$\mathcal{L}_3$ (eqs. (2)–(4)) — extending the zero-radius settings of [2,19] (p. 2, Contribution 1).
2. **Theory — new geometric object**: **Definition 1 + Lemma 3**: the *Attacker's farthest firepower coverage curve* $G(x,y)=0$ (eq. (9)) — the locus of points $C$ where $A$ can still destroy $T$ exactly when $D$ closes to within $R_D$ of $A$; constructed from the $A$-$D$ Apollonius-oval interception curve $B_1$ (eq. (5)) inflated radially by $R_A$ (pp. 3–4).
3. **Algorithm**: **Algorithm 1** (p. 4) — decides whether a given initial state belongs to $A$'s or the $D$–$T$ team's winning region (or the barrier) from the sign of $G(\mat
[RESULTS-LIST]
- **Dynamics (eq. (1))**: planar simple motion $\dot{\mathbf{x}}_A = v_A\mathbf{u}_A$, $\dot{\mathbf{x}}_D = v_D\mathbf{u}_D$, $\dot{\mathbf{x}}_T = v_T\mathbf{u}_T$ with $\mathbf{x}_i=(x_i,y_i)$, unit controls $\mathbf{u}_A=(\cos\delta,\sin\delta)$, $\mathbf{u}_D=(\cos\vartheta,\sin\vartheta)$, $\mathbf{u}_T=(\cos\varphi,\sin\varphi)$; speeds constant with the standing assumption $v_D > v_A > v_T$; $\sigma = v_A/v_D < 1$, $\varrho = v_T/v_A < 1$; capture radii $R_A, R_D > 0$.
- **Termination (eqs. (2)–(4))**: $\mathcal{L}_1$ ($A$ captures $T$, $A$ not yet intercepted: $\|\mathbf{x}_A-\mathbf{x}_T\|_2 \le R_A$ **and** $\|\mathbf{x}_A-\mathbf{x}_D\|_2 > R_D$); $\mathcal{L}_2$ ($D$ intercepts first); $\mathcal{L}_3$ (simultaneous, both equalities — draw). The three-way question "will the state first arrive at $\mathcal{L}_1$, $\mathcal{L}_2$, or $\mathcal{L}_3$" defines the game of kind; $
[CITATION]
This paper is the archive's reference for **barrier-surface determination in the TAD game with non-zero capture radii and a faster defender** — the natural "next step" citation after the zero-radius fast-defender barrier papers [P-references: Garcia IET 2017; Liang Automatica 2019] and the active-defense TAC line [Garcia TAC 2020]. Its reusable assets are (i) the explicit **farthest-firepower-coverage curve** (eq. (9)) — a radial $R_A$-offset of the $A$-$D$ Apollonius oval capturing the fact tha

### P082 — Constructing barrier functions and optimal control for differential games in active defense
[BIBLIO]
- **ID**: P082
- **Source file**: `D:\System\zhuomian\game-paper\Shi 等 - 2026 - Constructing barrier functions and optimal control for differential games in active defense.pdf`
- **Total pages**: 13 (pp. 1–11 body + references pp. 12–13 incl. author biographies)
- **Title**: Constructing barrier functions and optimal control for differential games in active defense
- **Authors**: Yibo Shi (Univ. of Shanghai for Science and Technology, USST), Chaoli Wang (USST, corresponding author, clwang@usst.edu.cn), Shihua Li (Southeast University), Engang Tian (USST)
- **Year**: 2026
- **Venue (EXACT, from header/copyright)**: *Automatica* 188 (2026) 112942. Elsevier. Article history: Received 19 November 2024; revised 3 November 2025; accepted 1 February 2026. Associate Editor Abdelhamid Tayebi, Editor Thomas Parisini. Indexer guess "Automatica" is **correct**.
- **DOI (printed)**: 10.1016/j.automatica.2026.112942; ISSN 0005-1098 printed on copyright line. Funding: NSFC 62173232, 62003214.
- **Tier**: T1 (Automatica). No disagreement.
- **BibTeX** (from printed metadata only):
```bibtex
@article
[CONTRIBUTIONS]
1. **Modeling** (theory): first TAD game formulation — within the Garcia lineage — in which **both** A and D have non-zero capture radii (R > 0, r > 0) under equal speeds V_A = V_D > V_T; terminal sets (2)–(4) with two distinct radii.
2. **Game of Degree** (theory/algorithm): two-sided Pontryagin Maximum Principle solutions for three initial placements of T relative to the D–A interception hyperbola (left / right / on it), giving constant-heading state-feedback strategies (Theorems 1–3) whose intercept point solves the algebraic system (11)–(12) and is radius-dependent (Remark 4); C¹ value functions (16), (46) verified against the HJI equation (17), (44), establishing Nash equilibrium.
3. **Game of Kind** (theory): a new geometric object — the **Attacker's limit interception curve** 𝒜 (Def
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 2)**: Isaacs "simple motion" (holonomic) on the Euclidean plane, states x_T, x_A, x_D ∈ ℝ², full state x = (x_A, x_D, x_T) ∈ ℝ⁶; controls are heading angles ζ (T), β (A), δ (D) ∈ [−π, π]:
- **Termination (eqs. (2)–(4), p. 2–3)**: M = M₁ ∪ M₂, M₁ = {‖x_A − x_T‖₂ ≤ R} (A wins), M₂ = {‖x_A − x_D‖₂ ≤ r} (D–T win); t_f = first entry into M₁ or M₂; a third outcome (simultaneous entry into both) is the tie case realized on the barrier.
- **Information**: perfect-information differential game (p. 3).
- **Cost (eq. (5), p. 3)**: V(x₀) := min_β max_{δ,ζ} ‖x_{Af} − x_{Tf}‖₂ (zero-sum, terminal payoff; solved only for the D–T-victory premise).
- **Dominant-region preliminaries**:
- **Definition 1 (p. 3)**: dominant point/region of an evader (points the evader reaches before capture regardless of the pursuer).
- **Lemma 1 [Yan et al. 2021] (p. 3, eqs. (6)–(7))**: if ‖x_A − x
[CITATION]
This paper is the equal-speed (V_A = V_D > V_T) member of the TAD-with-finite-capture-radii line, complementing Garcia (2021, Automatica) and Liang et al. (2021, TAC), which require a superior attacker; it is the natural extension of Garcia et al. (2018 TAES, 2019 TAC) to R > 0 and r > 0 simultaneously, and its Game-of-Kind machinery (Attacker's limit interception curve + tangency with the Apollonius oval) is the reusable novelty — a template transferable to any pursuit-evasion problem where the

### P083 — A Review of Multi Agent Perimeter Defense Games
[BIBLIO]
- **ID**: P083
- **Source file**: `D:\System\zhuomian\game-paper\Shishika和Kumar - 2020 - A Review of Multi Agent Perimeter Defense Games.pdf`
- **Total pages**: 14 PDF pages (= printed pp. 472–485; body pp. 472–483 incl. Conclusion, References pp. 483–485)
- **Title**: A Review of Multi Agent Perimeter Defense Games
- **Authors**: Daigo Shishika (George Mason University, Fairfax, VA 22030, USA, dshishik@gmu.edu, corresponding author) and Vijay Kumar (University of Pennsylvania, Philadelphia, PA 19104, USA, kumar@seas.upenn.edu)
- **Year**: 2020
- **Venue (EXACT, from header/copyright on p. 472)**: "© Springer Nature Switzerland AG 2020, Q. Zhu et al. (Eds.): GameSec 2020, LNCS 12513, pp. 472–485, 2020. https://doi.org/10.1007/978-3-030-64793-3_26" — i.e., *Decision and Game Theory for Security* (11th International Conference on Decision and Game Theory for Security, GameSec 2020), Lecture Notes in Computer Science, vol. 12513, Springer. PDF metadata subject field confirms: "Decision and Game Theory for Security, doi:10.1007/978-3-030-64793-3_26". **Indexer disagreement resolved**: th
[CONTRIBUTIONS]
1. **Unified two-level solution architecture for multi-agent perimeter defense** (Sect. 3): a recipe — solve small-scale games of kind (1v1, 2v1) for barriers and winning regions, then lift to team-level coordination via combinatorial optimization — presented as the common structure behind the reviewed results.
2. **Comparative taxonomy of three team-level analysis approaches** — MM (maximum matching), MIS (maximum independent set), LGR (local game regions) — with explicit relative-strength/weakness assessment (tightness vs. computational complexity vs. generality of applicability) and the bound chain Q_MIS ≤ Q_MM and the intruder lower bound Q_LG.
3. **Catalog of closed-form agent-level results**: circular barrier ([25], verified [32]), sign-based equilibrium defender strategy, approach-a
[RESULTS-LIST]
- **Item 1 — Problem statement (Sect. 2, p. 474).** Planar dynamics of point particles: N_A intruders (A) and N_D defenders (D), all with *simple dynamics* (first-order integrator; velocity = control). Speed bounds: intruders ν and defenders 1, with constraint **ν ≤ 1** ("the intruders are at most as fast as the defenders"). Assumptions: **(A1)** defenders move along the perimeter of the target region; **(A2)** the target region is convex; **(A3)** each agent has full-state information (positions of all agents); **(A4)** intercept/capture occurs when the intruder–defender distance becomes zero. Outcome categories per intruder: (i) reaches perimeter un-intercepted → scores; (ii) distance to a defender is zero upon reaching the perimeter; (iii) never reaches the perimeter in finite time (defender places itself between target and intruder). Both (ii) and (iii) are defined as *capture*. Team
[CITATION]
- **Likely role in a future IEEE Trans introduction**: the canonical related-work anchor for the *multi-agent perimeter defense / target guarding with perimeter-confined defenders* line. Use it (i) to introduce the perimeter-defense game and its two-level (local differential game + combinatorial teaming) solution paradigm, (ii) to justify the MM/bipartite-assignment and barrier-based pairwise-capturability machinery by citation, (iii) to motivate open problems — faster intruders, capture radius,

### P084 — Multitarget Pursuit-Evasion Based on Distributed and Competitive Mechanisms
[BIBLIO]
- **ID**: P084
- **Source file**: `D:\System\zhuomian\game-paper\Tan 等 - 2024 - Multitarget Pursuit-Evasion Based on Distributed and Competitive Mechanisms.pdf`
- **Total pages**: 12 (pp. 5989–6000; body pp. 5989–5999 incl. references ending p. 5999, author biographies p. 6000)
- **Title**: Multitarget Pursuit-Evasion Based on Distributed and Competitive Mechanisms
- **Authors**: Ning Tan (Senior Member, IEEE, corresponding author, tann5@mail.sysu.edu.cn), Yang Liu, Ruikun Hu, Hui Cheng — all with the School of Computer Science and Engineering and the Key Laboratory of Machine Intelligence and Advanced Computing (Ministry of Education), Sun Yat-sen University, Guangzhou 510275, China
- **Year**: 2024
- **Venue (EXACT, from running header/copyright)**: *IEEE Transactions on Systems, Man, and Cybernetics: Systems*, Vol. 54, No. 10, October 2024, pp. 5989–6000. Copyright line ISSN 2168-2216 © 2024 IEEE. This is the **SMC — Systems** journal (not SMC: Network). Indexer guess "IEEE Transactions on Systems, Man, and Cybernetics" is correct and resolves to **Systems**.
- **DOI (printed)**: 
[CONTRIBUTIONS]
1. **Algorithm (modeling + distributed computation)**: DMK-WTA — a two-phase distributed task-allocation algorithm: (i) a *k-WTA phase* implemented as a three-variable (β, θ, z) per-pair dynamical network (eqs. (7)–(10)) that fuses the classical k-WTA dual-network structure [27] with the dynamic average-consensus estimator of Freeman, Yang & Lynch [25], so each pursuer estimates global winner counts from local neighborhoods; (ii) a *load-reassignment phase* (Algorithm 1, p. 5992, inspired by swarm clustering [28]) that resolves multi-load conflicts and exchanges targets to lower total cost, with a randomized transfer rule (probability ρ) to escape local optima (Remark 1, p. 5992).
2. **Control scheme (modeling)**: the Predator-Pack encirclement Model (PPM) — a Newton-second-law potential-f
[RESULTS-LIST]
- **Robot dynamics (eq. (11), p. 5992)**: Newton's second law at velocity level, v̇_i(t) = F_i(t)/m_i, for i = p_1,…,p_{N_p}, e_1,…,e_{N_e}; F_i resultant virtual force, m_i mass. Positions u_i; single integrator-then-force structure (acceleration-controlled; no nonholonomic constraint in the model — heading/steering appears only in the Aliengo interface (20)–(21)).
- **Information structure (p. 5990)**: evader positions u_{e_j} broadcast to all pursuers; pursuers know nothing about obstacles a priori (obstacles sensed within detection range O); each pursuer communicates only with neighbors ℕ_i^c (within communication range), topology may change during execution; pursuers detect nearby pursuers (set ℕ^d_{p_i}) and obstacles O. Evaders detect pursuers within ℕ^d_{e_j}. So: *local communication, global target-position broadcast, no obstacle map*.
- **Cost**: assignment cost Σᵢ Σⱼ ω_ij d_ij
[CITATION]
**Paragraph role**: a systems-and-algorithms paper in the cooperative-pursuit literature — the reference point for *distributed competitive task allocation* (k-WTA networks) in *multitarget* pursuit, and for potential-field *encirclement* control validated across three locomotion modalities (wheeled E-puck, legged Aliengo, aerial Crazyflie 2.1). It is the natural citation when a paper needs (i) a distributed, communication-light alternative to KM/GA/auction/DQN assignment for pursuit subteam for

### P085 — Value Iteration-Based Cooperative Adaptive Optimal Control for Multi-Player Differential Games With Incomplete
[BIBLIO]
- **ID**: P085
- **Source file**: `D:\System\zhuomian\game-paper\Value_Iteration-Based_Cooperative_Adaptive_Optimal_Control_for_Multi-Player_Differential_Games_With_.pdf` (8 PDF pages = journal pp. 690–697; below, "p. X" = printed journal page = PDF page X−689)
- **Title**: Value Iteration-Based Cooperative Adaptive Optimal Control for Multi-Player Differential Games With Incomplete Information
- **Authors**: Yun Zhang; Lulu Zhang; Yunze Cai (corresponding author) — Department of Automation, Shanghai Jiao Tong University, Shanghai 200240, and Key Laboratory of System Control and Information Processing, Ministry of Education of China, Shanghai 200240, China (zhang_yun@sjtu.edu.cn; zhang_lulu@sjtu.edu.cn; yzcai@sjtu.edu.cn)
- **Year**: 2024 (manuscript received June 27, 2023; revised October 22, 2023; accepted November 12, 2023; Recommended by Associate Editor Lei Ding; supported by the Industry-University-Research Cooperation Fund Project of the Eighth Research Institute of China Aerospace Science and Technology Corporation (USCAST2022-11) and the Aeronautical Science Foundation of Ch
[CONTRIBUTIONS]
1. **(Modeling/theory)** Extension of the finite-horizon value-iteration HJB equation of Bian–Jiang [12] to a **best-response HJB equation** for MPDGs (eq. (10), p. 692): with all other players' policies frozen, player i's problem reduces to a single-controller optimal control problem, so the single-system VI convergence lemma (Lemma 1 of [12]) carries over (Lemma 2).
2. **(Theory)** A **cooperative value-iteration (cVI) scheme** in which players are partitioned into an *adapting* player and *non-adapting* players (concept borrowed from Köpf et al. [21]) and adapt **sequentially** in a pre-ordered loop (policy evaluation (11) → policy improvement (12) → role switching), with a convergence proof to the optimal value functions V*_i (Theorem 1, p. 692–693) — the first continuous-time VI-based
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 691)**: ẋ = f(x) + Σ_{i=1}^N g_i(x) u_i, x ∈ Ω ⊂ R^n a compact set containing the origin, u_i ∈ U_i ⊂ R^m admissible; f : R^n → R^n and g_i : R^n → R^{n×m} locally Lipschitz. (One shared state; players add control channels.)
- **Cost (eq. (2), p. 691)**: J_i(x0; u_i, u_{−i}) = ∫_0^∞ r_i(x, u_i) dt, with r_i(x, u_i) ≜ Q_i(x) + u_i^T R_i u_i; Q_i : Ω → R positive semidefinite, R_i ∈ R^{m×m} positive definite symmetric. r_i does not depend on u_{−i} explicitly; u_{−i} acts on J_i through the trajectory of x (p. 691).
- **Nash equilibrium (eq. (3), p. 691)**: J_i(x0; u*_i, u*_{−i}) ≤ J_i(x0; u_i, u*_{−i}) ∀ i ∈ [1 : N]. **Interactive Nash equilibrium (Definition 1, [22], eqs. (4)–(5), p. 691)**: (3) plus non-degeneracy — for each k there exists u'_k (k ≠ i) with J_i(x0, u*_k, u*_{−k}) ≠ J_i(x0, u'_k, u*_{−k}) (5).
- **Information set (eq. (6), p. 691)**: F_i([t0,t1]
[CITATION]
**Paragraph role**: this paper is the canonical reference in this library for the *learning-based* branch of multi-player differential games: it is the continuous-time, VI-based (admissible-policy-free) ADP answer to the CHJB solve for N-player nonzero-sum games under model/cost/policy privacy, complementing the geometric/analytic pursuit–evasion and reach-avoid results that dominate the collection. Use it (a) as the VI-vs-PI contrast point whenever an archive discusses stabilizing-initial-polic

### P086 — Target Defense Using a Turret and Mobile Defender Team
[BIBLIO]
- **ID**: P086
- **Source file**: `D:\System\zhuomian\game-paper\Von Moll 等 - 2025 - Target Defense Using a Turret and Mobile Defender Team.pdf`
- **Total pages**: 6 (pp. 2921–2926)
- **Title**: Target Defense Using a Turret and Mobile Defender Team
- **Authors**: Alexander Von Moll (Senior Member, IEEE; Control Science Center, AFRL, Wright-Patterson AFB), Dipankar Maity (Senior Member, IEEE; ECE, UNC Charlotte), Meir Pachter (Life Fellow, IEEE; EE, AFIT), Daigo Shishika (Member, IEEE; ME, George Mason University), Michael Dorothy (DEVCOM Army Research Laboratory)
- **Year**: 2025
- **Venue** (exact, from running header/copyright): IEEE Control Systems Letters, Volume 9, 2025, pp. 2921–2926. Indexer guess (L-CSS) is **correct**.
- **DOI** (printed in footnote): 10.1109/LCSYS.2025.3645833
- **Publication history** (printed): Received 11 Sep 2025; revised 17 Nov 2025; accepted 11 Dec 2025; published 18 Dec 2025; current version 31 Dec 2025. Recommended by Senior Editor L. Menini. Funding: AFOSR LRIR Grant 24RQCOR002; DEVCOM ARL DCIST CRA W911NF-17-2-0181. Clearance AFRL-2025-0001003.
-
[CONTRIBUTIONS]
1. **Modeling (theory):** a hybrid-capability defense team — stationary turn-constrained Turret (control = normalized turn rate $u_T \in [-1,1]$) plus holonomic Defender — against a simple-motion Attacker, formulated as a zero-sum terminal-cost differential game with capture sets defined as a union of two geometric predicates (eqs. (1)–(7)).
2. **Dominance-region geometry (theory):** $\mathcal{R}_{A/D}$ = interior of the Apollonius circle (eqs. (13)–(15)); $\mathcal{R}_{A/T}$ = set of points $A$ reaches before $T$ can slew into alignment, bounded by a closed curve with an angular domain $[\underline{\theta}, \bar{\theta}]$ determined by the transcendental equation $\nu\theta/\omega = r_A|\sin(\theta - \theta_A)|$ (Lemmas 3, 5; eqs. (19)–(26)).
3. **Equilibrium characterization (theory):** 
[RESULTS-LIST]
- **Dynamics (eq. (1))**: state $x = (x_D, y_D, x_A, y_A, \theta_T)$;
- **Capture/winning conditions (eq. (3))**: $C_D = \{x \mid r_D = r_A > 1,\ \theta_D = \theta_A\}$ (Defender collides with Attacker at equal bearing); $C_T = \{x \mid \theta_A = 0,\ r_A > 1\}$ (Turret's LOS aligned with $A$ while outside the target disk); $C_{D,T} = C_D \cap C_T$ simultaneous capture. Termination time $t_f = \inf\{t \mid x \in C_D \cup C_T\}$ (eq. (4)). $A$'s alternative win: reach $r_A = 1$ (target circle).
- **Cost (eq. (5))**: $J = r_{A_f} - 1$, $A$ minimizing, D–T team maximizing; note $J$ presupposes team capture (an $A$-win is not represented — see §7).
- **Information structure**: perfect state feedback / open-loop Isaacs equilibrium; Value satisfies Isaacs' condition (eq. (6)) and the Nash-saddle property (eq. (7)) over admissible control sets $U_D, U_A, U_T$.
- **Dominance region (eq. (13))**:
[CITATION]
**Role in the literature.** This letter is the first equilibrium solution of a **mixed-kinematics cooperative defense team** — a stationary turn-constrained Turret fused with a holonomic mobile Defender — against a simple-motion Attacker, and as such it is the natural hub joining three strands in this archive: Apollonius-circle guarding games (Isaacs [4]; Lee–Bakolas [16]; Dorothy et al. [18]), turret/turn-constrained defense (Akilan–Fuchs [7]; Von Moll et al. turret-runner-penetrator [13]; circ

### P087 — Construction of Barrier in a Fishing Game With Point Capture
[BIBLIO]
- **ID**: P087 / **source file**: `D:\System\zhuomian\game-paper\W. Zha 等 - 2017 - Construction of Barrier in a Fishing Game With Point Capture.pdf` / **total pages**: 14 (PDF pages 1–14; published version spans IEEE Xplore pp. 1409–1422, also 14 pages).
- **Title**: Construction of Barrier in a Fishing Game with Point Capture.
- **Authors**: Wenzhong Zha (Student Member, IEEE), Jie Chen (Senior Member, IEEE, corresponding author), Zhihong Peng (Member, IEEE) — School of Automation, Beijing Institute of Technology, and Key Laboratory of Intelligent Control and Decision of Complex Systems, Beijing 100081, China; Dongbing Gu (Senior Member, IEEE) — School of Computer Science and Electronic Engineering, University of Essex, Colchester, UK.
- **Year**: 2017. Printed manuscript dates (p. 1 footnote): received September 6, 2015; revised February 4, 2016; accepted March 21, 2016.
- **Venue**: NOT printed anywhere in this PDF — it is a TeX-generated accepted-manuscript version (MiKTeX/dvipdfmx, 2016) with no running header, no copyright line, no DOI. The indexer's guess "IEEE Transactions on
[CONTRIBUTIONS]
1. **Theory (game of kind)**: analytic construction of the barrier $B_1$ of the fishing game via a *method of explicit policy*: split the game into two sub-games of kind (competition on $\theta$; competition on $\min\{d_1,d_2\}$), solve each, and integrate. Winning regions $\mathscr{D}_p^1$ (eq. (18)) and $\mathscr{D}_e^1$ (eq. (21)), barrier $B_1$ (eq. (19)) with the closed form $\cos\theta = \frac{(1-a^2)(d_1+d_2)^2}{2d_1d_2}-1$; in relative coordinates a fixed-$z$ slice of $B_1$ is the ellipse (43).
2. **Theory (game of degree)**: fusion of kind and degree — feedback-optimal minimum-time strategies and winning-time upper bounds in each of four zones partitioned by $B_1, B_2, B_3$ (eqs. (44)–(65)), including the rendezvous strategy (46)–(49) valid outside $B_3$, the angle-reduction strat
[RESULTS-LIST]
- **Theorem 4.1 (p. 5, eqs. (14)–(15))**: if $r_{12}(t_0)\le a(d_1(t_0)+d_2(t_0))$, equivalently $\theta(t_0)\le\Theta(t_0)$, the pursuers win by adopting (8). *Assumptions*: point capture, $a<1$ (for $a=1$, $\mathscr{D}_p^1$ is all of $\Omega$ minus $\{\theta=\pi\}$), $\min\{d_1^0,d_2^0\}>0$, $0\le\theta_0<\pi$. *Proof approach*: explicit policy + Isaacs-style main equation (no RPE integration). Steps: (i) at $\theta_0<\Theta_0$, (11) gives $\dot\theta(t_0)<0$; (ii) substituting (8)–(9) into (4)–(5): $\dot d_i = -v_e d_i\sin\theta/r_{12}<0$ and $\dot d_1/\dot d_2 = d_1/d_2$, so $b=d_1/d_2$ is invariant ($\dot b=0$); (iii) (13) becomes (16) $\cos\Theta = \frac{(1-a^2)(1+b)^2}{2b}-1$, so $\Theta(t)$ is invariant along equilibrium play and $\theta(t)$ decreases monotonically below the constant $\Theta$; (iv) "based on the concept of Nash equilibrium" the pursuers achieve $\theta(t_f)<\pi$ 
[CITATION]
This is the canonical reference for **barrier construction via explicit policies in a two-pursuer/one-faster-evader "fishing" game with point capture**: it supplies (i) the closed-form barrier $r_{12}=a(d_1+d_2)$ (equivalently the Apollonius ellipse $x^2+(1-a^2)y^2=\frac{(1-a^2)z^2}{a^2}$ in relative coordinates), (ii) the non-escape angle $\Theta=\arccos\!\big(\frac{(1-a^2)(d_1+d_2)^2}{2d_1d_2}-1\big)$ and its maximum $\arccos(1-2a^2)$, and (iii) a four-zone minimum-time strategy synthesis fusi

### P089 — Matching-Based Capture-the-Flag Games for Multiagent Systems
[BIBLIO]
- **ID**: P089
- **Source file**: `D:\System\zhuomian\game-paper\Wang 等 - 2024 - Matching-Based Capture-the-Flag Games for Multiagent Systems.pdf`
- **Total pages**: 13 (printed pp. 993–1005)
- **Title**: Matching-Based Capture-the-Flag Games for Multiagent Systems
- **Authors**: Jiali Wang and Zhao Zhou (equal contribution; Key Laboratory of Smart Manufacturing in Energy Chemical Process, Ministry of Education, East China University of Science and Technology, Shanghai 200237, China), Xin Jin (Research Institute of Intelligent Complex Systems, Fudan University, Shanghai 200433, China), Shuai Mao (Department of Electrical Engineering, Nantong University, Nantong 226019, China), Yang Tang (Senior Member, IEEE; corresponding author, ECUST, Shanghai).
- **Year/Venue**: 2024. Printed header: "IEEE TRANSACTIONS ON COGNITIVE AND DEVELOPMENTAL SYSTEMS, VOL. 16, NO. 3, JUNE 2024", pp. 993–1005 — indexer guess (IEEE Transactions on Cognitive and Developmental Systems) **confirmed**. Manuscript received 18 September 2022; revised 12 July 2023; accepted 13 September 2023; date of publication 13 
[CONTRIBUTIONS]
1. **Modeling**: Extension of one-to-one CTF games [27], [33], [34], [49] to multiplayer CTF differential games with complex interactions and with counting of objects captured by defenders (contribution 1, p. 994).
2. **Theory**: Analytical solution of multiplayer CTF games by reduction to two-defense-one (2D-1A) or one-defense-one (1D-1A) situations; a **two-phase joint optimal strategy** for defenders obtained by constructing a continuous and continuously differentiable value function, proved to satisfy the HJI equation (contribution 2, p. 994; Theorem 1 + Corollary 1).
3. **Algorithm**: A constrained matching formulation — maximum bipartite matching with conflict graph (MBMC) — to maximize the number of captured attackers, solved approximately by a **sequential matching algorithm** buil
[RESULTS-LIST]
- **Dynamics (1), p. 995**: simple motion, 2$(N_a{+}N_d)$ scalar ODEs as above; no capture radius (point capture), no region-boundary dynamics (players are not constrained to stay in $\Omega$ by the equations).
- **Speed ratios (3), p. 996**: $\mu_1 = V_{d1}/V_a$, $\mu_2 = V_{d2}/V_a$, $\mu_3 = V_{d2}/V_{d1}$, with $\mu_1 > 1$, $\mu_2 > 1$; in the Appendix it is assumed WLOG that $D_1$ is the slower defender, so $\mu_3 > 1$.
- **Apollonius circles (4)–(7), p. 996**: between $D_1$ and $A$: $C_1 = \{(x,y)\,|\,(x-x_{C_1})^2 + (y-y_{C_1})^2 = R_{C_1}^2\}$ with $x_{C_1} = \frac{x_a\mu_1^2 - x_{d_1}}{\mu_1^2-1}$, $y_{C_1} = \frac{y_a\mu_1^2 - y_{d_1}}{\mu_1^2-1}$, $R_{C_1} = \frac{\mu_1\sqrt{(x_{d_1}-x_a)^2 + (y_{d_1}-y_a)^2}}{\mu_1^2-1}$ (5); analogously $C_2$ with $(\mu_2, x_{d_2}, y_{d_2})$ (6)–(7). **Dominance (winning) disks (8)**: $\Gamma_1 = \{(x,y) \mid (x-x_{C_1})^2 + (y-y_{C_1})^2 \l
[CITATION]
This paper is the bridge node between the geometric one-to-one capture-the-flag line (Garcia–Casbeer–Pachter CDC 2018 [27]; Pachter–Casbeer–Garcia CCTA 2020 [33]; Huang et al. TCST 2015 [34]) and the matching-based multiplayer reach-avoid line (Chen–Zhou–Tomlin TAC 2017 [38]; Yan et al. Automatica 2022 [30]; Yan–Shi–Zhong TRO 2020 [46]; Garcia et al. TAC 2021 [47]), and it is the first journal treatment of CTF with two whole alliances of players. Its three reusable assets for our knowledge base 

### P090 — Multi-Agent Target-Attacker-Defender Differential Games with Anomalous Defenders under Limited Perception
[BIBLIO]
- **ID**: P090. **Source file**: `D:\System\zhuomian\game-paper\Wang 等 - 2025 - Multi-Agent Target-Attacker-Defender Differential Games With Anomalous Defenders Under Limited Perce.pdf`. **Total pages**: 16 (double-column IEEE accepted-version preprint).
- **Title** (as printed on p. 1): *Multi-Agent Target-Attacker-Defender Differential Games with Anomalous Defenders under Limited Perception*.
- **Authors**: Jiali Wang, Daniel W. C. Ho (Life Fellow, IEEE), Xin Jin, Fangfei Li (Member, IEEE), Yang Tang (Fellow, IEEE).
- **Year**: 2025. **Venue** (EXACT, from the copyright line on every page): "This article has been accepted for publication in **IEEE Transactions on Automatic Control**... Citation information: DOI 10.1109/TAC.2025.3631483". **DOI**: 10.1109/TAC.2025.3631483 (printed). Volume/issue/pages not printed (early-access stage).
- **Tier**: T1 (IEEE Transactions on Automatic Control) — indexer guess confirmed by the printed header; no disagreement.
- **BibTeX** (from printed metadata only; volume/pages not printed, hence the note):
```bibtex
@article{Wang2025TADanomalous,
  au
[CONTRIBUTIONS]
1. **Modeling**: a multi-agent TAD nonzero-sum LQ differential game with n defenders, m attackers (m ≤ n), one active target, single-integrator dynamics in relative coordinates, and a novel two-parameter anomaly model: defender $D^I_l$'s interception drive $\mu_{lj}$ scales its quadratic penalty on defender–attacker distances ($\mu_{lj}>1$ greedy, $0\le\mu_{lj}<1$ fearful, $=1$ normal) — Definition 2 (p. 4).
2. **Information structure**: binary-visibility adjacency matrices $\mathcal{A}(t)$ (16) and $\mathcal{A}^*(t)$ (17) inducing a time-varying directed visibility network; masking matrices $\mathcal{I}_h(t)$ (20) that project Riccati feedback onto each agent's observable subspace; adaptive state-feedback strategy classes (19) (Definition 4).
3. **Theory — inverse game theory**: Theorem 1
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 3)**: every agent is a 2-D single integrator, $\dot x_{D_i}=u_{D_i x},\ \dot y_{D_i}=u_{D_i y}$ (likewise attackers $A_j$ and target $T$). Relative-state vector $Z(t)=\mathrm{col}\{Z_{D_1A_1},\dots,Z_{D_nA_m},Z_{TA_1},\dots,Z_{TA_m}\}\in\mathbb{R}^{2m(n+1)}$ with $\dot Z(t)=\sum_i B_{D_i}u_{D_i}(t)+B_Tu_T(t)+\sum_j B_{A_j}u_{A_j}(t)$ (eq. (2)); $B_{A_j}$ carries the $-1$ block (column $e^j_{n+1}$) so attacker controls subtract. After splitting anomalous/normal defenders (eq. (3)): $\dot Z=B^I_Du^I_D+B^{II}_Du^{II}_D+B_Tu_T+B_Au_A$, with $B_A=-1_{m(n+1)\times m}\otimes I_2$ (p. 4).
- **Visibility (Definition 1, p. 3)**: agent $h$ perceives $\ell$ at time $t$ iff $\|x_h(t)-x_\ell(t)\|_2=\|Z_{hA_j}(t)-Z_{\ell A_j}(t)\|_2\le R_h$; this defines the directed graph $Q(t)=(\mathcal{H},E(t))$. Assumption: capture radii $r_{D_i}<R_{D_i}$, $r_{A_j}<R_{A_j}$.
- **Terminatio
[CITATION]
**Paragraph role**: P090 is the bridge paper between geometric TAD games and networked/partially-observable nonzero-sum LQ games. It contributes (a) a minimal, transferable formalization of "anomalous teammates" via a scalar drive coefficient $\mu$ in the team cost — usable in any Stackelberg/Nash LQ multiplayer setting; (b) an inverse-game-theory construction (Theorems 1–2) that converts arbitrary visibility-feasible feedback laws into Nash equilibria of reverse-engineered quadratic costs, with

### P091 — Optimal Strategies in Multiplayer Reach–Avoid Games With Different Speed Ratios
[BIBLIO]
- **ID**: P091
- **Source file**: `D:\System\zhuomian\game-paper\Wang 等 - 2025 - Optimal Strategies in Multiplayer Reach–Avoid Games With Different Speed Ratios.pdf`
- **Total pages**: 13 (paper body pp. 1–12 incl. references pp. 12–13; author bios p. 13). Early-access PDF: "This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination."
- **Title**: Optimal Strategies in Multiplayer Reach–Avoid Games With Different Speed Ratios
- **Authors**: Jiali Wang; Daniel W. C. Ho (Life Fellow, IEEE); Shuai Mao; Jing Xu (Senior Member, IEEE); Yang Tang (Fellow, IEEE)
- **Year**: 2025 (copyright line "2168-2267 © 2025 IEEE"; received 20 Aug 2025, revised 6 Nov 2025, accepted 10 Nov 2025; Recommended by Associate Editor W. Xia)
- **Venue** (exact, from running header and copyright): IEEE Transactions on Cybernetics. The indexer guess (TCYB) is **correct** — header on every page reads "IEEE TRANSACTIONS ON CYBERNETICS" and the PDF subject metadata is "IEEE Transactions on Cybernetics; PP; 99".
- **DOI** (printed on 
[CONTRIBUTIONS]
1. **Theory (α_{ji} ≤ 1, Scenario 1 & 3).** An advantage-region method that constructs fully analytical barriers for reach–avoid games with defender capture radii: a three-curve barrier for one faster defender vs. one slower attacker (Theorem 1) and a five-curve barrier for two heterogeneous cooperating defenders vs. one attacker (Theorem 2); the equal-speed case collapses to a two-curve hyperbola-branch barrier (Theorem 6). Compared to [30], which only handles faster defenders, all speed ratios are covered.
2. **Theory (α_{ji} > 1, Scenario 2).** For a faster attacker, winning regions are built from per-defender *defensive advantage angles* γ_i obtained from a Cartesian oval of simultaneous arrival (Theorem 3), a case classification of the attacker's optimal target point against one defen
[RESULTS-LIST]
- **Dynamics, eq. (1)**: simple motion, ẋ_{Di} = v_{Di} cos φ_{Di}, ẏ_{Di} = v_{Di} sin φ_{Di} (identically for attackers), heading φ ∈ [−π, π) changeable at any time (no turn-rate limit); controls u_{Di} = {v_{Di}, φ_{Di}}. Both sides play maximum speed v*_{Di}, v*_{Aj} (standard assumption, citing [33], [34]); speed-dependent costs acknowledged as out of scope. State x̃ = (x_{D1},…,x_{DN}, x_{A1},…,x_{AM}) ∈ R^{2(N+M)}; N ≥ M (Remark 1: if N < M the problem becomes attacker prioritization, not barrier construction).
- **Information structure**: perfect, instantaneous knowledge of own and all others' positions/speeds and of Ω; no disturbances; strategies are state feedback (u_{Aj}(·), u_{Di}(·) in eqs. (6), (8)). Assignment: binary χ_{ij}, Σ_{j=1}^M χ_{ij} ≤ 1 (each defender pursues ≤ 1 attacker; cooperative 2-vs-1 pursuit allowed); captured defenders become stationary.
- **Ratios**: at
[CITATION]
This is the bridge paper between the point-capture analytical-barrier school (Yan–Shi–Zhong [2], [19], [30]; Wu et al. [18]) and nonpoint-capture heterogeneous reach–avoid games: it is the natural "related work" anchor for any paper that adds capture radii, mixed faster/slower defenders, or advantage-angle coalition coverage to a barrier-based multiplayer reach–avoid analysis, and its eq. (13) (heterogeneous rendezvous with radii) and Theorem 5's absolute-advantage-angle condition (19) are the t

### P092 — Surveillance of a Faster Fixed-Course Target
[BIBLIO]
- **ID**: P092
- **Source file**: `D:\System\zhuomian\game-paper\Weintraub 等 - 2023 - Surveillance of a Faster Fixed-Course Target.pdf` — 12 pages (journal pp. 4147–4158). Note: the Read tool reports this PDF as "password-protected", but PyMuPDF opens it unencrypted (`needs_pass = 0`); full text + 200-dpi page renders were used.
- **Title**: Surveillance of a Faster Fixed-Course Target
- **Authors**: Isaac E. Weintraub (Senior Member, IEEE; corresponding author), Alexander Von Moll (Senior Member, IEEE), Eloy Garcia (Senior Member, IEEE), David W. Casbeer (Senior Member, IEEE) — all with the Control Science Center, Air Force Research Laboratory, Wright-Patterson AFB, OH 45433 USA; Meir Pachter (Life Fellow, IEEE) — Dept. of Electrical and Computer Engineering, Air Force Institute of Technology, Wright-Patterson AFB, OH USA.
- **Year**: 2023. Manuscript received 22 Sep 2022; revised 1 Dec 2022 and 3 Jan 2023; accepted 10 Jan 2023; date of publication 16 Jan 2023; date of current version 9 Aug 2023. Refereeing handled by A. Ratnoo. AFRL/RQ 22-OPSEC-PR-354 (Distribution Unlimited); supp
[CONTRIBUTIONS]
1. **Theory**: A complete closed-form solution of a two-phase optimal-control problem (approach + observation) for a slower holonomic observer maximizing observation time of a faster fixed-course target; the full state space is partitioned into three regions with distinct optimal strategies (Theorem 1, eqs. (58)–(60)).
2. **Modeling**: A fixed-course-target surveillance model in relative-frame coordinates (eqs. (1)–(5)) where the observation disk of radius $R$ plays the role of a finite capture/sensor range, making the problem the "observation analog" of finite-range pursuit of a superior evader; explicit connection to the Apollonius circle / Cartesian oval machinery of containment games [17].
3. **Geometric tool**: The **Decision Line (DL)** — the locus of points whose Apollonius circle (
[RESULTS-LIST]
- **State** (eq. (1)): $\mathbf{x}(t) = [x_O(t),\, y_O(t),\, y_T(t)]^\intercal \in \mathbb{R}^3$. Cartesian frame with $\hat{y}$-axis aligned with the target's velocity (WLOG); target at $(0, y_T)$, observer at $(x_O, y_O)$.
- **Speeds**: target speed normalized to $1$; observer speed $\alpha = v_O/v_T$, $0 < \alpha < 1$ (observer strictly slower).
- **Control** (p. 4149): $u(t) = \psi_O(t)$, the observer's instantaneous heading — holonomic, constant-speed, unlimited turn rate (kinematic point-mass).
- **Dynamics** (eq. (3)): $\dot{x}_O = \alpha\cos\psi_O$, $\dot{y}_O = \alpha\sin\psi_O$, $\dot{y}_T = 1$.
- **Observation set** (eq. (2)): disk $\mathscr{O} = \{\mathbf{x}(t) \mid x_O^2(t) + (y_O(t)-y_T(t))^2 - R^2 \le 0,\ t\in[t_2,t_f]\}$, $R>0$; realistic readings: visual contact range, sensor range, or communication range (p. 4148).
- **Terminal manifold / termination** (eq. (4)): escape
[CITATION]
This paper is the canonical closed-form reference for the **surveillance/stand-off tracking of a superior (faster) fixed-course target** and for **two-phase optimal-control coupling by backward induction** in the AFRL reach-avoid/perimeter-defense corpus. It occupies a distinctive niche: the "pursuer is slower" regime where capture is impossible but *dwell time* is the currency, connecting the finite capture-radius literature (containment of high-speed evaders, [17], [19]) to the surveillance-ev

### P093 — One superior pursuer and multiple-evader differential games with two lifelines
[BIBLIO]
- ID: P093 / source file: `Xu 等 - 2024 - One superior pursuer and multiple-evader differential games with two lifelines.pdf` / total pages: 15
- Title: One superior pursuer and multiple-evader differential games with two lifelines
- Authors: Ningsheng Xu (BIT), Fang Deng (corresponding author, dengfang@bit.edu.cn, BIT), Weiwen Huang (BIT, School of Mathematics and Statistics), Li Liang (Beijing University of Chemical Technology), Xiang Shi (BIT)
- Year: 2024. Venue (EXACT, from header/copyright): **European Journal of Control**, Volume 80 (2024), Article 101130. © 2024 European Control Association, published by Elsevier Ltd. Recommended by T. Parisini. Received 6 Mar 2024 / revised 8 Jul 2024 / accepted 17 Oct 2024. **DOI (printed on p.1): 10.1016/j.ejcon.2024.101130**. Indexer guess "European Journal of Control" is CORRECT.
- Tier: **T2** — agree. EJC (ECA/Elsevier) is a strong control journal but below the T1 band (IEEE TAC/Automatica); assignment consistent. (Note: the same group's companion one-evader/two-pursuer two-lifeline paper, Xu et al., cited as ref. [Xu, Huang, Liang, & D
[CONTRIBUTIONS]
1. **Theory (barriers)**: closed-form barrier curves for each lifeline **without time delay** (Thm 4.1, eq. (13)) and **with time delay** Δt = Σ t_j accumulated while P dispatches previously pursued evaders (Thm 4.2 eq. (19), Cor. 4.1 eq. (26)); merging B_i^1 and B_i^2 yields per-evader pursuer dominance region (PDR, 𝒲_{P_i}) and evader dominance region (EDR, 𝒲_{E_i} = Ω_play ∖ 𝒲_{P_i}); Δ-PDR shrinks monotonically with Δt and can vanish (Fig. 5).
2. **Modeling (game of kind)**: terminal payoff functions J_2 (28) / J_1 (31) equal to the topmost/bottommost y-coordinate reachable on the evader's updated Apollonius circle; cooperative vs. non-cooperative value functions (29)-(30); lifeline-selection rule min{J_1, h−J_2} (Cor. 5.1) and escape criterion min{J_1, h−J_2} ≤ 0 (Cor. 5.2); necessary
[RESULTS-LIST]
- **Lemma 3.1 (p. 3, eq. (6))** — *Parallel pursuit strategy.* If E_i uses control φ_i, then P using **φ = arcsin((1/a_i) sin φ_i)** (eq. (6)) captures E_i on or within the Apollonius circle 𝓒_i. Proof: sine theorem in ▵PCE_i, sin φ_i / sin φ = |PC|/|E_iC| = a_i (eq. (7)) ⇒ (8). If E_i keeps changing direction, the reachable region shrinks and P, mirroring via (6), still captures inside 𝓒_i (Fig. 3(b)). Global, analytic; the workhorse pursuit policy used throughout all simulations.
- **Lemma 3.2 (p. 3, eq. (9))** — *Capture time along straight lines.* T_i = ‖x_i − x_P‖₂ sin φ / (v_i sin(φ_i + φ)) (from sine law eq. (10)), bounded by ‖x_i−x_P‖₂/(v_i+v_p) ≤ T_i ≤ ‖x_i−x_P‖₂/(v_p−v_i); minimum at the near intersection of line P E_i with 𝓒_i, maximum at the far one.
- **Lemma 3.3 (p. 4, eq. (11))** — *Capture angle.* Θ = arccos(1 − 2/a_i²) = 2 arcsin(1/a_i), from sin∠BPO_i = R_i/‖x_P − x_{O_
[CITATION]
Role: this is the archival reference for **barrier-based dominance analysis and cooperative "sacrifice" strategies in a one-superior-pursuer vs. many-evader two-lifeline (reach-two-goals) differential game** — the multi-evader sequel to the lifeline-game line (Isaacs' lifeline problem, Zha's fishing game, Yan et al.'s limited-lifetime lifeline game, Zhang & Zha's three-player game) and the mirror image of the authors' TAC two-pursuer/one-evader paper. Use it when a paper needs: (i) explicit no-d

### P094 — Optimal Strategies of a Two-lifeline Differential Game
[BIBLIO]
- **ID**: P094
- **Source file**: `D:\System\zhuomian\game-paper\Xu 等 - 2024 - Optimal Strategies of a Two-lifeline Differential Game.pdf` (file opens normally; the Read tool misreports it as password-protected — full text extracted with pymupdf and formulas verified against 200-dpi page renders)
- **Total pages**: 8 (pp. 1–7 body and figures, p. 8 conclusion + references [1]–[36])
- **Title**: Optimal Strategies of a Two-lifeline Differential Game
- **Authors**: Ningsheng Xu, Weiwen Huang, Li Liang, Fang Deng (Senior Member, IEEE; corresponding author: Fang Deng)
- **Affiliations (printed)**: N. Xu & F. Deng — National Key Lab of Autonomous Intelligent Unmanned Systems, Beijing Institute of Technology, Beijing 100081, and BIT Chongqing Innovation Center, Chongqing 401120, China; W. Huang — School of Mathematics and Statistics, BIT; L. Liang — College of Information Science and Technology, Beijing University of Chemical Technology.
- **Year**: 2024 (copyright block "© 2024 IEEE"; IEEE Xplore download stamp Nov 05, 2024)
- **Venue (EXACT, printed in header of every page)**: "This arti
[CONTRIBUTIONS]
1. **(Modeling)** First formulation of a two-lifeline differential game with two pursuers P1, P2 (speed vP) and one evader E (speed vE), capture radius l > 0, speed ratio a = vP/vE > 1, two target sets C (capture) and D (lifeline crossing), terminal payoff J = min{ye(tf1), d − ye(tf2)} (eq. (4)) and value V = max_{u1,u2} min_{uE} J (eq. (5)), under a non-anticipative information structure (p. 2–3).
2. **(Theory — reachable region)** Characterization of the evader's guaranteed reachable region R = R1 ∩ R2 by two Cartesian ovals C1, C2 (Lemma 3.1, eq. (7)), generalizing the Apollonius circle [10], [11] to nonzero capture radius; a = 1 degenerates to hyperbolas (Fig. 2).
3. **(Theory — pursuit)** Closed-loop pursuer capture strategy (8) (heading angle ε as a function of the evader's control a
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion, ẋi = vP cos ϕi, ẏi = vP sin ϕi (i = 1, 2); ẋe = vE cos φ, ẏe = vE sin φ. Controls are headings u1 = (cos ϕ1, sin ϕ1)⊤, u2 = (cos ϕ2, sin ϕ2)⊤, uE = (cos φ, sin φ)⊤ in admissible sets U1, U2, Ue. Speeds fixed, directions piecewise-continuous in time; **a = vP/vE > 1** ("If a < 1, it would not be meaningful ... as the evader can successfully reach the target area when the initial distance between pursuers and evader is greater than l", p. 3). L1 fixed at y = 0, L2 at y = d; ye is the evader's distance from L1.
- **Target sets (eq. (2)–(3))**: C = {x(x1, x2, xE) ∈ R^6 | ‖xE − x1‖2 ≤ l ∨ ‖xE − x2‖2 ≤ l} (capture), D = {x(x1, x2, xE) ∈ R^6 | ye ≤ 0 ∨ ye ≥ d} (lifeline crossed). Capture means distance to at least one pursuer ≤ l.
- **Termination criteria (p. 3, unnumbered)**: (1) if min{ye, d − ye} < 0 and min{‖x1 − xE‖2, ‖x2 − xE‖2} > l, the evader win
[CITATION]
**Paragraph role**: P094 is the first systematic treatment of the *two-lifeline* pursuit-evasion differential game (two pursuers, one evader, strip between two parallel lifelines, nonzero capture radius), sitting at the intersection of the Isaacs lifeline lineage [7], [8], [13], [14], [23], [36] and the geometric reach-avoid/target-defense school [10]–[12], [29]–[32], [35]. Its reusable assets are: (i) the Cartesian-oval reachable region (7) generalizing the Apollonius circle to l-capture; (ii) 

### P095 — Partial information target defense game in the presence of a line segment obstacle
[BIBLIO]
- **ID**: P095
- **Source file**: `D:\System\zhuomian\game-paper\Xu 等 - 2024 - Partial information target defense game in the presence of a line segment obstacle.pdf` (Read tool misreports it as password-protected; full text extracted with pymupdf, and every load-bearing formula verified against 200/300-dpi page renders)
- **Total pages**: 12 (journal pp. 1289–1300; pp. 1–10 body incl. Figs. 1–8, p. 11 back matter + references [1]–[37], p. 12 references cont. + "How to cite" block)
- **Title**: Partial information target defense game in the presence of a line segment obstacle
- **Authors**: Jingwen Xu, Qiyong He, Min Meng, Xiuxian Li (corresponding, xxli@ieee.org), Jiaqi Yan
- **Affiliations (printed, p. 1)**: 1 Dept. of Control Science and Engineering, College of Electronics and Information Engineering, Tongji University, Shanghai, China; 2 Shanghai Research Institute for Intelligent Autonomous Systems, Shanghai, China; 3 Dept. of Computer Science, Tokyo Institute of Technology, Yokohama, Japan
- **Year**: 2024 (Received 7 Nov 2023; Revised 12 Jan 2024; Accepted 14 Feb 2024 — all pr
[CONTRIBUTIONS]
1. **(Modeling)** Extension of the classic target defense game to partial information *with a fixed line segment obstacle*: three-phase decomposition by information possession — deployment (Def. 1, eq. (1)–(2)), asymmetric information (Def. 2, eq. (3)–(4)), engagement (Def. 3, eq. (3)+(5)) — with engagement termination rules (capture / breach / escape back to deployment, p. 4); fairness Assumption 1 restricting $(\rho_T,\rho_I,l_o)$ (p. 3).
2. **(Strategy design)** Redesigned closed-loop strategies for both players in the asymmetric phase: intruder $\mu_I^{\text{asym}}$ = radial invasion with an endpoint-directed detour after sensing an obstacle endpoint (p. 5); defender $\mu_D^{\text{asym}}$ = move to the optimal defense point on the radial direction of the *predicted* endpoint (chosen by
[RESULTS-LIST]
- **Geometry**: target disk radius $r_0$ centered at origin $O$; TSR $=\{r_0<\|x\|\le r_0+\rho_T\}$ (p. 3 — printed with a typo as $\mathcal{S}_{r_0+\rho_I}(0)\setminus\mathcal{S}_{r_0}(0)$, the subscript should be $r_0+\rho_T$; verified on the p. 3 render). Obstacle: segment of length $l_o$, midpoint at $(r_0+\rho_T/2,\theta_o)$ in polar coordinates, tangent to the circle $\|x\|=r_0+\rho_T/2$ (hence perpendicular to the radial ray $\theta_o$). Endpoint polar angles $\theta_o\pm\beta$, with $\beta=\arctan\!\big((l_o/2)/(r_0+\rho_T/2)\big)$ (p. 6).
- **Dynamics**: never written explicitly; implicitly single-integrator (simple motion) with speeds $\nu<1$ (intruder) and 1 (defender) — "assume that the speed of the defender is 1 and the speed of the intruder is $\nu$" (p. 3). All results are kinematic/geometric.
- **Information structure**: target is static, has full information of I inside 
[CITATION]
**Paragraph role**: P095 is the canonical "obstacle + partial information" point in the target-defense lineage Isaacs → [9] Bopardikar et al. (sensing limits, discrete time) → [10] Shishika et al. ICRA 2021 (partial-information target defense, three phases, $P_D=\Theta/\pi$) → this paper, which grafts a fixed tangent line-segment obstacle onto [10]'s framework and shows that the forced zig-zag detour enlarges the defender's guaranteed angular set by $\Delta\theta_l+\Delta\theta_r$ (Theorem 1). I

### P096 — Collision-free Reach-Avoid Differential Game of Multiple Underactuated Autonomous Surface Vehicles via Control
[BIBLIO]
- **ID**: P096
- **Source file**: `D:\System\zhuomian\game-paper\Xu 等 - 2025 - Collision-free Reach-Avoid Differential Game of Multiple Underactuated Autonomous Surface Vehicles v.pdf` — 10 pages (content pp. 1–9, references pp. 9–10, author biographies p. 10). Note: the Read tool reports this PDF as "password-protected", but PyMuPDF opens it unencrypted (`needs_pass = 0`); full text + 200/300-dpi page renders were used to verify every formula.
- **Title** (p. 1): Collision-free Reach-Avoid Differential Game of Multiple Underactuated Autonomous Surface Vehicles via Control Barrier Functions
- **Authors**: Fangyuan Xu (Dalian Maritime University, Dalian, China); Nan Gu (Dalian Maritime University; Swinburne University of Technology, Melbourne, Australia; corresponding author); Zhouhua Peng (Senior Member, IEEE; Dalian Maritime University; corresponding author); Bing Han (Minjiang University; Shanghai Ship and Shipping Research Institute; Dalian Maritime University); Weidong Zhang (Senior Member, IEEE; Shanghai Jiao Tong University; Hainan University). **Byline typo as printed**: "Zhou
[CONTRIBUTIONS]
1. **Theory (Game of Kind/Degree for equal-speed pairs)**: For each defender-pair-vs-attacker game, an equal-speed orthogonal-line barrier $\mathcal B(\mathbf p_k)$ (eqs. (18), (23)) partitions $\mathbb R^6$ into winning regions $\mathcal R_D,\mathcal R_A$ (eq. (8)); a closed-form optimal interception point $\mathbf I^*_{k1}$ (1v1, eq. (21)) and $\mathbf I^*_{k2}$ (2v1 cooperative, eqs. (25)–(26)) with unit-speed saddle-point strategies (eqs. (22), (27)); HJI verification of both value functions (eqs. (37)–(41), (42)–(47), Theorem 1).
2. **Modeling**: Underactuated ASV kinematics with sideslip (eq. (4)) converted to a fully-actuated 2-D point-mass game on an *off-center guidance point* $\mathbf p^D_i=\mathbf p_i+\iota_i\varrho_i$ via the invertible mapping $R_{\iota_i}(\psi_{iw})$ (eq. (5)
[RESULTS-LIST]
- **Underactuated kinematics** (eq. (4), citing Fossen [45]): $\dot x_i = U_i\cos\psi_{iw}$, $\dot y_i = U_i\sin\psi_{iw}$, $\dot\psi_{iw} = r_i + \dot\beta_i$, where $U_i=\sqrt{u_i^2+v_i^2}>0$ is the resultant of surge $u_i$ and sway $v_i$; $\psi_{iw}=\psi_i+\beta_i$ is the actual course; $\beta_i=\arctan(v_i/u_i)$ is the sideslip angle; $r_i$ the body-frame yaw rate. The ASV is underactuated: it controls $(U_i, r_i)$ but its planar velocity direction is the course $\psi_{iw}$, not a freely chosen heading.
- **Guidance-point (auxiliary variable) reduction** (p. 3, eq. (5)): with a constant positive offset $\iota_i>0$ and rotation vector $\varrho_i=[\cos\psi_{iw},\sin\psi_{iw}]^T$, define the shifted point $\mathbf p^D_i=\mathbf p_i+\iota_i\varrho_i$. Then $\dot{\mathbf p}^D_i=[u^x_i,u^y_i]^T=R_{\iota_i}(\psi_{iw})[U_i,\, r_i+\dot\beta_i]^T$ with $R_{\iota_i}(\psi_{iw})=\begin{bmatrix}\c
[CITATION]
**Paragraph role**: a *systems/application-tier* reach-avoid paper that bridges the geometric equal-speed reach-avoid game literature ([38]–[40], Garcia–Casbeer–Pachter; Yan–Shi–Zhong–Bullo) and the marine cooperative-control community (T-IV/TIE/Ocean Engineering USV attack–defense line [21]–[26]), using the standard CBF-QP safety-filter stack ([42]–[44], Ames et al.) and Fossen's guidance-point trick [45] to make simple-motion game strategies executable by underactuated, sideslip-affected ASVs.

### P097 — Apollonius partitions based pursuit-evasion strategies via multi-agent reinforcement learning
[BIBLIO]
- **ID**: P097
- **Source file**: `D:\System\zhuomian\game-paper\Xue 等 - 2025 - Apollonius partitions based pursuit-evasion strategies via multi-agent reinforcement learning.pdf` — 11 pages (content pp. 1–8, appendices A–C pp. 9–10, references + author biographies p. 11). The Read tool did not flag this PDF; text extracted with PyMuPDF (`needs_pass = 0`) and all formulas cross-checked against 200/300-dpi page renders.
- **Title** (p. 1): Apollonius partitions based pursuit-evasion strategies via multi-agent reinforcement learning
- **Authors**: Lei Xue (corresponding author, leixue@seu.edu.cn; School of Automation, Southeast University, Key Laboratory of Measurement and Control of Complex Systems of Engineering, Ministry of Education, Nanjing 210096, China); Qing Wang (Department of Information Technology, Bank of Nanjing, Nanjing 210019, China); Yongbao Wu (Southeast University); Xin Yuan (Southeast University); Jian Liu (Southeast University).
- **Year**: 2025. Received 20 June 2022; revised 28 September 2024; accepted 8 February 2025; available online 19 February 2025. Communicate
[CONTRIBUTIONS]
1. **Theory (geometry)**: Characterization of the evader's optimal fixation aimpoint within the Apollonius-partition dominant region — it lies on a two-circle boundary intersection $B_i\cap B_j$ (eq. (15)) or on the ray extension $B_i\cap L(\mathbf x_e,\mathbf x_{\mathbf O_i})$ (eq. (16)) — with a geometric proof (**Theorem 1**, p. 5, Appendix A).
2. **Theory (game theory)**: Formulation of the multi-pursuer/single-evader PEG as an **ordinal potential game** with potential $\Phi$ (eq. (22)) and proof of NE existence for $N_e=1, N_p\ge 2$ (**Theorem 2**, p. 6, Appendix B, eqs. (22)–(28)); equilibrium reachability via the finite improvement property (FIP) [35].
3. **Theory (guarantee)**: Finite-time capture certificate via monotone decrease of the current shortest capture time (CSCT), $\math
[RESULTS-LIST]
- **Dynamics** (eq. (1), p. 3): $\dot x_i = v_p\cos\theta_i$, $\dot y_i = v_p\sin\theta_i$, $\dot x_e = v_e\cos\theta_e$, $\dot y_e = v_e\sin\theta_e$ — constant-speed simple motion; controls are the instantaneous heading angles $\theta_i,\theta_e$; $\alpha = v_e/v_p <1$ constant.
- **Information structure**: positions and speeds shared globally ("location and speed information are shared, but the respective strategies are private", p. 1); the evader's strategy is **scripted** (fixation, Section 3.2), only pursuers are learned. Neighbor indicator $\delta_i = 1$ iff $i\in\mathbf N_{\mathbf{ep}}$, the set of pursuers whose Apollonius circles contribute to the evader's current dominant region (p. 2).
- **Apollonius partition** (eqs. (6)–(9), pp. 3–4): for each pursuer $i$, the Apollonius circle $\{(x,y):(x-cx_i)^2+(y-cy_i)^2 = r_i^2\}$ (eq. (7)) with
- **Utility / reward** (eq. (17), p. 5):
[CITATION]
**Paragraph role**: P097 is a *hybrid geometry-plus-learning* reference: it imports the classical Apollonius-circle dominant-region partition (Isaacs-lineage tools also used in P-periphery works like Dorothy et al. "One Apollonius circle is enough", and Makkapati–Tsiotras' Apollonius allocation [31]) into a CTDE multi-agent RL pipeline, wraps the pursuit side in an ordinal-potential-game NE-existence argument, and adds a role-freezing mechanism motivated by the active/redundant structure of [31]

### P098 — Optimal Strategies for Guarding a Compact and Convex Target Set: A Differential Game Approach
[BIBLIO]
- **ID**: P098
- **Source file**: `D:\System\zhuomian\game-paper\Y. Lee和E. Bakolas - 2021 - Optimal Strategies for Guarding a Compact and Convex Target Set A Differential Game Approach.pdf`
- **Total pages**: 6 (Secs. I–VI + References [1]–[20] all within pp. 1–6; two-column CDC/IEEE-conference format)
- **Title**: Optimal Strategies for Guarding a Compact and Convex Target Set: A Differential Game Approach
- **Authors**: Yoonjae Lee (PhD student) and Efstathios Bakolas (Associate Professor), Department of Aerospace Engineering and Engineering Mechanics, The University of Texas at Austin, Austin, Texas 78712-1221, USA; e-mails: yol033@utexas.edu; bakolas@austin.utexas.edu (printed footnote, p. 1).
- **Year**: 2021
- **Venue** (EXACTLY what the PDF states): **arXiv preprint only**. The sole venue marker is the vertical margin stamp on p. 1: "arXiv:2104.00717v2 [eess.SY] 16 Sep 2021". No journal name, no conference name, no copyright/DOI/ISSN is printed anywhere. PDF producer metadata: "LaTeX with hyperref / pdfTeX-1.40.21", creation date 2021-09-17 (consistent with the v2 stamp). Exte
[CONTRIBUTIONS]
1. **Theory (game of kind — generalized barrier)**: a barrier function on the joint state space $\mathbb{R}^4$, $B(\mathbf{x}; \Omega, \gamma) := \|\mathbf{Proj}_\Omega(C(\mathbf{x})) - C(\mathbf{x})\| - R(\mathbf{x})$ (eq. (19), Prop. 3), built from the Apollonius circle between the players and the **metric projection onto $\Omega$**; winning sets $\mathcal{R}_c := \{B > 0\}$ (capture), $\mathcal{R}_a := \{B \le 0\}$ (attack) (eqs. (20)–(21)); semipermeability of $\mathcal{B}$ (Remark 2). This is the "generalized Apollonius" barrier: for a circular target it reduces to the expression "(11) in [7]"; for a general $\Omega$ the distance from the Apollonius center to $\Omega$ is replaced by the distance to the projection $\mathbf{Proj}_\Omega(C)$.
2. **Theory (capture game of degree)**: conti
[RESULTS-LIST]
**Definition 1**: $\mathcal{A}(\mathbf{x};\gamma) := \{z \in \mathbb{R}^2 : \|z - C(\mathbf{x};\gamma)\| = R(\mathbf{x};\gamma)\}$ (eq. (14)) — the locus of points both players reach simultaneously under optimal (constant-input) play — with center and radius
[CITATION]
**Paragraph role**: this is the reference that completes the "Isaacs + Apollonius geometry" program for target-defense games with *general* compact convex targets: it lifts the circular-region solution of Garcia–Casbeer–Pachter [7] to arbitrary smooth convex targets through one clean substitution — the distance from the Apollonius center to the circle is replaced by the distance to the metric projection $\mathbf{Proj}_\Omega(C)$ — and shows that the entire solution architecture (barrier → winnin

### P099 — Reach-Avoid Games With Two Defenders and One Attacker: An Analytical Approach
[BIBLIO]
- **ID**: P099; **source file**: `D:\System\zhuomian\game-paper\Yan - 2019 - Reach-Avoid Games With Two Defenders and One Attac.pdf` (truncated filename; full title from p. 1); **total pages**: 12 (printed pp. 1035–1046).
- **Title**: Reach-Avoid Games With Two Defenders and One Attacker: An Analytical Approach.
- **Authors**: Rui Yan (Student Member, IEEE), Zongying Shi (Member, IEEE, corresponding author), Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, China.
- **Year/Venue**: IEEE Transactions on Cybernetics, Vol. 49, No. 3, March 2019, pp. 1035–1046. Indexer guess (TCYB) **confirmed** by running header on every page. Manuscript received June 20, 2017; revised Nov. 7, 2017 and Jan. 7, 2018; accepted Jan. 11, 2018; published online Feb. 2, 2018; Associate Editor: T. Vasilakos. Funded by NSFC Grants 61374034 and 61210012. Copyright 2168-2267 © 2018 IEEE.
- **DOI (printed)**: 10.1109/TCYB.2018.2794769.
- **Tier**: T1 (IEEE Transactions on Cybernetics — IEEE Trans journal). No disagreement.
- **BibTeX** (all fields from printed metadata):
```bibtex
@art
[CONTRIBUTIONS]
1. **Theory (game of kind)**: closed-form barrier $\mathcal{B}^1$ (one defender: two/three parts, Lemmas 1–2) and $\mathcal{B}^2$ (two defenders: three/five parts, Theorem 2) for speed ratio $\alpha = v_A/v_D \le 1$, built via a new **attack region (AR) method** — the AR $R^i_A$ (points the attacker reaches uncaught) computed from Voronoi diagrams ($\alpha = 1$) and Apollonius circles ($\alpha < 1$), with the barrier obtained by "utilizing the semipermeability of barrier" [p. 1038]. Winning regions follow as upper/lower regions of the barrier (Remark 1, Def. 1).
2. **Theory (which defenders matter)**: necessary and sufficient condition for the barrier to depend on only one defender — $x^0_{D2} \in \mathcal{W}^1_D(x^0_{D1},1) \cup \mathcal{B}^1(x^0_{D1},1)$ (Theorem 1); conversely $x^0_{D2}
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 1036)**: simple motion, $\dot{x}_{Di,1} = v_{Di}\cos\phi_{Di}$, $\dot{x}_{Di,2} = v_{Di}\sin\phi_{Di}$ ($i=1,2$); $\dot{x}_{A,1} = v_A\cos\phi_A$, $\dot{x}_{A,2} = v_A\sin\phi_A$. Controls $\phi_{Di}, \phi_A \in [-\pi,\pi)$; no constraints beyond constant speed; instantaneous heading changes. $v_{D1} = v_{D2} = v_D$; $\alpha = v_A/v_D$; **only $\alpha \le 1$ considered**: "Since the attacker always wins from any given initial positions of the players for $\alpha > 1$, we only consider the case $\alpha \le 1$" [p. 1037] — asserted without proof (see §7).
- **Information structure**: full-state — all players know $\Omega$, $\mathcal{T}$, and exact positions/speeds of everyone at all times [p. 1037]; no knowledge of the opponent's current strategy; strategies are saddle-point (zero-sum Nash) under open-loop info, refreshed in practice as piecewise open-loop with sm
[CITATION]
**Role**: this is the canonical analytical benchmark for the smallest genuinely *cooperative* reach-avoid block — two defenders guarding one line segment against one attacker — and the natural companion/corrective to Chen–Zhou–Tomlin's pairwise-outcome maximum-matching framework [11] (whose 1v1 pairs ignore intra-team cooperation). It supplies: (i) closed-form barriers combining Voronoi bisectors, Apollonius circles, and a hyperbola arc in a bounded rectangular domain; (ii) an if-and-only-if con

### P100 — Task Assignment for Multiplayer Reach–Avoid Games in Convex Domains via Analytical Barriers
[BIBLIO]
- **ID**: P100. **Source file**: `D:\System\zhuomian\game-paper\Yan 等 - 2020 - Task Assignment for Multiplayer Reach–Avoid Games .pdf` (filename truncated; full title taken from p. 107). **Total pages**: 18 (journal pp. 107–124).
- **Title**: Task Assignment for Multiplayer Reach–Avoid Games in Convex Domains via Analytical Barriers.
- **Authors**: Rui Yan (Student Member, IEEE), Zongying Shi (Member, IEEE, corresponding author), Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, China.
- **Year/Venue**: IEEE Transactions on Robotics, Vol. 36, No. 1, February 2020, pp. 107–124. Header/copyright printed: "IEEE TRANSACTIONS ON ROBOTICS, VOL. 36, NO. 1, FEBRUARY 2020"; © 2019 IEEE; date of publication September 4, 2019. Manuscript received Jan. 5, 2019; revised Jun. 13, 2019; accepted Aug. 7, 2019. Recommended by Associate Editor J. Shamma and Editor P. Robuffo Giordano. Funded by NSFC Grant 61374034 and China Scholarship Council.
- **DOI (printed)**: 10.1109/TRO.2019.2935345.
- **Tier**: T1 (IEEE Transactions on Robotics — indexer guess confirmed correct by 
[CONTRIBUTIONS]
1. **Theory — one-pursuer barrier (Theorem 1)**: closed-form, three-piece barrier B1 for one pursuer vs. one evader in any convex Ωplay, composed of two circular arcs (centered at the target-line endpoints m, n) and one middle hyperbola-type arc (p. 113–114).
2. **Theory — two-pursuer barrier (Theorem 2)**: five-piece analytical barrier for two pursuers vs. one evader, with the active/inactive pursuer dichotomy (Definition 3) and the unique equal-arrival point pc on T (p. 115–116).
3. **Theory — general-coalition barrier (Theorem 3 + Lemma 3 + Algorithm 1 + Theorem 4)**: analytical barrier for a full-active pursuit coalition of arbitrary size nk, constructed inductively along an x-rank index set; every barrier segment depends on at most two pursuers; any general coalition degenerates to it
[RESULTS-LIST]
- **Dynamics (eq. (1), p. 109)**: decoupled simple motion, ẋPi = vPi·uPi, ẋEj = vEj·uEj, xi(0) = x0i; controls u ∈ U = {u ∈ R² : ‖u‖₂ = 1}. Point-mass players, point capture (positions coincide) inside Ωplay; once an evader enters Ωtar it can no longer be captured (p. 109).
- **Domain (p. 109–110)**: Ω ⊂ R² bounded, convex; target line T ⊂ Ω with endpoints m, n, ‖m − n‖₂ = l; Ωtar compact with T ⊂ Ωtar; Ωplay = Ω \ Ωtar. Coordinates: origin at m, x-axis along T, y-axis toward Ωtar; hence evaders satisfy y0Ej < 0.
- **Assumptions (p. 110)**: Ass. 1 distinct initial positions; Ass. 2 (constrained) pursuers in Ωplay ∪ T, evaders in Ωplay; Ass. 3 (relaxed) pursuers anywhere in Ω; Ass. 4 homogeneous speeds, α = vE/vP ∈ (0,1) (slower evaders).
- **Information structure (p. 110)**: nonanticipative — the pursuit team chooses its input knowing the evaders' current inputs; the evader knows the pur
[CITATION]
**Paragraph role**: this is the reference work for *analytical* (grid-free) barrier and winning-region construction in multiplayer reach–avoid games of kind with simple motion, slower evaders, and straight-line target sets in convex domains, and for the reduction of the resulting cooperative task-assignment problem to a small 0-1 integer program. Its two structural lemmas — (a) every multiplayer barrier segment depends on at most two pursuers, hence cooperative capture never needs more than two 

### P101 — Cooperative strategies for two-evader-one-pursuer reach-avoid differential games
[BIBLIO]
- **ID**: P101 | **Source file**: `D:\System\zhuomian\game-paper\Yan 等 - 2021 - Cooperative strategies for two-evader-one-pursuer reach-avoid differential games.pdf` | **Total pages**: 20 (1 Taylor & Francis cover page + printed pages 1–19; for printed-page citations below, printed page = PDF page − 1 after the cover).
- **Title**: Cooperative strategies for two-evader-one-pursuer reach-avoid differential games
- **Authors**: Rui Yan, Zongying Shi, Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, People's Republic of China (contact: szy@mail.tsinghua.edu.cn). ORCIDs printed: Rui Yan 0000-0002-8685-5055, Zongying Shi 0000-0002-6805-6858.
- **Year**: 2021. Article history printed on p. 1: Received 8 July 2020; Accepted 2 January 2021; Published online 15 January 2021.
- **Venue (resolved exactly from printed metadata)**: **International Journal of Systems Science** (Taylor & Francis). Evidence: cover page banner "International Journal of Systems Science" (journal code `tsys20`), every running header "INTERNATIONAL JOURNAL OF SYSTEMS SCIENCE", and the print
[CONTRIBUTIONS]
1. **Pursuit strategy (theory)**: the evader dominance region compression (EDRC) strategy — Lemma 3.1 proves that if $P$ always runs toward the intersection of the current Apollonius circle $\mathcal{A}_i$ with the ray from $E_i$ along $E_i$'s current heading, the new Apollonius circle is internally tangent to the old one, so $E_i$'s dominance region strictly shrinks until capture (p. 4–5, eqs. (4)–(10)); Theorem 3.2 gives the *unique* closed-form feedback realization (p. 5, eq. (11)).
2. **Time-shifted barrier machinery (theory)**: Definition 4.1 introduces the δ-Apollonius circle $\mathcal{A}_i^\delta$ (locus reachable by $P$ exactly $\delta$ earlier than $E_i$), Lemma 4.2 computes it explicitly in polar coordinates (p. 7, eqs. (18)–(23)); Theorem 4.3 constructs the barrier and the two w
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple motion for all three players, $\dot x_1 = v_{E1}\cos\psi_1,\ \dot y_1 = v_{E1}\sin\psi_1$; $\dot x_2 = v_{E2}\cos\psi_2,\ \dot y_2 = v_{E2}\sin\psi_2$; $\dot x_P = v_P\cos\phi,\ \dot y_P = v_P\sin\phi$, with initial states $(x_{10}, y_{10})$, $(x_{20}, y_{20})$, $(x_{P0}, y_{P0})$ and control constraint $U = \{u \mid u \in [0, 2\pi)\}$ (instantaneous headings). The two evaders choose $(\psi_1, \psi_2)$ *jointly* (team).
- **Winning/termination conditions** (pp. 3–4): capture = zero Euclidean distance (point capture; non-zero radius deferred to Yan, Duan et al. 2019 / Yan, Shi et al. 2019); an evader wins locally by reaching $\Omega_2$ (crossing $L$); game terminates when no evader remains in $\Omega_1$; evader in $\Omega_2$ is immune. Assumption: $P$ faster, $\alpha_i < 1$ for $i = 1, 2$.
- **Information structure** (p. 3): nonanticipative — $P$'s current
[CITATION]
This is the canonical analytic reference for *evader-side cooperation* in reach-avoid differential games with simple motion: it complements the authors' two-pursuer-one-evader series (Yan et al., TCYB 2019; TCYB 2020a; TRO 2020b) by moving the cooperation to the losing side, and it supplies three reusable primitives — the EDRC feedback pursuit law (eq. (11)), the δ-Apollonius circle and time-shifted barrier (eqs. (18)–(26)), and the sacrifice/aiding equilibrium construction with the team-vs-indi

### P102 — Optimal Strategies for the Lifeline Differential Game with Limited Lifetime
[BIBLIO]
- **ID**: P102
- **Source file**: `D:\System\zhuomian\game-paper\Yan 等 - 2021 - Optimal strategies for the lifeline differential game with limited lifetime.pdf` (accepted-author-version PDF, "ARTICLE TEMPLATE" header; the Read tool flags it as password-protected but it opens unencrypted via pymupdf).
- **Total pages**: 25 PDF pages = 1 Taylor & Francis cover page + 24 manuscript pages (printed folios 1–24: body pp. 1–19, references pp. 19–21, figure pages pp. 22–24). The keywords line states "(8119 words)". Page numbers cited below are the printed manuscript folios.
- **Title**: Optimal Strategies for the Lifeline Differential Game with Limited Lifetime
- **Authors**: Rui Yan, Zongying Shi, Yisheng Zhong — Department of Automation, Tsinghua University, Beijing 100084, China (yr15@mails.tsinghua.edu.cn; szy@mail.tsinghua.edu.cn; zys-dau@mail.tsinghua.edu.cn).
- **Year**: 2019 (received 16 May 2019, revised 5 Nov 2019, accepted 24 Nov 2019, accepted author version posted online 6 Dec 2019 — all printed). The file name / indexer assigns 2021 (print-issue dating): **disagreement noted**;
[CONTRIBUTIONS]
1. **(Modeling)** Formulation of the lifeline game with limited lifetime: state $\mathbf x=(\mathbf x_P,\mathbf x_E,t)\in\mathbb R^4\times\mathbb R_{\ge0}$, simple-motion dynamics (1); capture set $\mathcal C$ (2); two target sets from lifeline and lifetime, $\mathcal T_1=\{\mathbf x\,|\,y_E=0\}$, $\mathcal T_2=\{\mathbf x\,|\,t=T_l\}$ (3); player target sets $\mathcal T_P=\mathcal C\cup\mathcal T_2$, $\mathcal T_E=\mathcal T_1$ (4); game space $\mathbb E$ and terminal surface $\mathcal C:=\mathcal T_P\cup\mathcal T_E$ (5); two games of degree with payoffs (6)–(11). The winner is decided by which target set the state hits first (p. 4).
2. **(Theory)** Introduction of the **evasion region** $\mathcal R_e$ and its boundary $\mathcal A^l$, the **l-Apollonius circle** (claimed as new; degenera
[RESULTS-LIST]
- **Lemma 1 (Strictly Decreasing Function) (p. 6, eq. (12)–(16)).** For $k_1\ge0$, $k_2>0$, $k_3\ge0$ with $k_1+k_3>0$, define $G(\beta)=1+\dfrac{k_1\beta^2-k_2(\beta-1)^2}{(\beta-1)^2(k_3\beta^2+k_2)}$ (12) on the interval $\beta<0,\ (\sqrt{k_2}-\sqrt{k_1})\beta<\sqrt{k_2}$ (13). Then $G$ is strictly decreasing there with values in $(0,1)$. *Proof*: $G'(\beta)=2\beta\,\dfrac{G_1(\beta)-k_1k_2}{(\beta-1)^3(k_3\beta^2+k_2)^2}$ (14) with $G_1(\beta)=k_2k_3(\beta-1)^3-k_1k_3\beta^3$ (15). Case $k_3=0$: $G'(\beta)=2\beta\frac{-k_1}{(\beta-1)^3k_2}<0$ (16). Case $k_3>0$: factorization $G_1'(\beta)=3k_3\big(\sqrt{k_2}(\beta-1)+\sqrt{k_1}\beta\big)\big((\sqrt{k_2}-\sqrt{k_1})\beta-\sqrt{k_2}\big)$ (17) is positive on (13), hence $G_1(\beta)<G_1(0)=-k_2k_3<0\Rightarrow G'(\beta)<0$ (18); limits $G\to0$ as $\beta\to0$ and $G\to1$ at the far end of (13). *Decisive step*: the sign factorization (17
[CITATION]
This is the canonical reference for the **lifeline differential game under a hard deadline**: it is the first (by the authors' claim, p. 19) to inject a limited lifetime into Isaacs' lifeline game, and it delivers a complete closed-form solution — l-Apollonius evasion region (Lemma 3), tangency barrier with and without lifetime (Lemma 7, Theorem 1), and region-wise optimal strategies via the OTP construction (Theorems 2–3) — all for a non-zero capture radius, a setting where most analytical reac

### P103 — Matching-based capture strategies for 3D heterogeneous multiplayer reach-avoid differential games
[BIBLIO]
- **ID**: P103
- **Source file**: `D:\System\zhuomian\game-paper\Yan 等 - 2022 - Matching-based capture strategies for 3D heterogeneous multiplayer reach-avoid differential games.pdf`
- **Total pages**: 14 (article: pp. 1–11; references pp. 12–14 incl. author bios)
- **Title**: Matching-based capture strategies for 3D heterogeneous multiplayer reach-avoid differential games
- **Authors**: Rui Yan (Dept. of Automation, Tsinghua University, Beijing 100084, China); Xiaoming Duan (Dept. of Automation, Shanghai Jiao Tong University, Shanghai 200240, China); Zongying Shi (corresponding author, Tsinghua); Yisheng Zhong (Tsinghua); Francesco Bullo (Center of Control, Dynamical Systems and Computation, University of California, Santa Barbara, USA)
- **Year**: 2022 (Received 13 Feb 2020; revised 8 Oct 2021; accepted 21 Jan 2022; online 14 Mar 2022). Associate Editor: Sergio Grammatico; Editor: Ian R. Petersen.
- **Venue (EXACT, from header/copyright)**: *Automatica* **140** (2022) 110207. © 2022 Elsevier Ltd. ISSN 0005-1098. Indexer guess "Automatica" — **correct**.
- **DOI (printed)**: 10.1016
[CONTRIBUTIONS]
1. **(Modeling)** A 3D heterogeneous multiplayer reach-avoid game formulation (Section 2): simple motion (holonomic, instantaneous heading changes, controls on the unit sphere S²), plane-separator goal/play regions, heterogeneous capture sets C_i = {x : ‖x − x_Pi‖₂ ≤ r_i}, state-feedback information structure (deliberately not non-anticipative, since opponents' current inputs are unavailable; under feedback the game "may not necessarily admit a value", citing Cardaliaguet 1996, 1997 and Krasovskii et al. 1987, p. 3), Assumption 2.1 (generic initial deployment) and Assumption 2.2 (α_ij = v_Pi/v_Ej > 1 for all pairs).
2. **(Theory — subgame of kind)** Evasion-space (ES) machinery for a pursuit coalition vs. one evader: the generalized (capture-radius-bearing) Apollonius surface as zero level
[RESULTS-LIST]
- **Dynamics (p. 3, eq. (1))**: ẋ_Pi = v_Pi u_Pi, x_Pi(0) = x0_Pi; ẋ_Ej = v_Ej u_Ej, x_Ej(0) = x0_Ej; controls u_Pi, u_Ej ∈ S² (instantaneous heading, simple motion). Positions in R³; plane T = {z = 0}, Ω_goal = {z ≤ 0}, Ω_play = {z > 0}.
- **Capture set (p. 3)**: C := ∪_{i=1}^{Np} C_i, C_i = {x ∈ R³ : ‖x − x_Pi‖₂ ≤ r_i}; evader Ej is captured when its distance to at least one pursuer equals that pursuer's radius; coalition capture set C_s = ∪_{i∈s} C_i (p. 4).
- **Information structure (p. 3, Section 2.2)**: state feedback — each player chooses u based on the information set {x_Pi, x_Ej} for all players. Non-anticipative structures (Elliott–Kalton; Margellos & Lygeros 2011; Mitchell et al. 2005; Yan et al. 2020) are rejected as too strong (they instantiate Stackelberg play); the authors note the feedback game may not admit a value (Cardaliaguet 1996, 1997; Krasovskii et al. 1987, Sectio
[CITATION]
**Paragraph role**: This is the canonical reference for **analytical 3D heterogeneous multiplayer reach-avoid games with nonzero capture radii**: it supplies (a) the capture-radius-generalized Apollonius/evasion-space certificate Ē(s,j) = {f_ij ≥ 0, i ∈ s} as the win/tie/lose criterion for a pursuer coalition vs. one evader; (b) the "at most three pursuers are necessary in 3D" degeneration theorem that collapses the coalition space to O(Np³); (c) the HJI-equals-convex-program result (KKT–Isaacs 

### P104 — Multiplayer reach-avoid differential games with simple motions: A review
[BIBLIO]
- **ID**: P104 / **source file**: `Yan 等 - 2023 - Multiplayer reach-avoid differential games with simple motions A review.pdf` / **total pages**: 11 (PDF read in full, incl. references; pages rendered to PNG at 200–400 dpi to verify all formulas).
- **Title**: Multiplayer reach-avoid differential games with simple motions: A review.
- **Authors**: Rui Yan (Dept. of Automation, Tsinghua University; also Dept. of Computer Science, University of Oxford), Ruiliang Deng (Tsinghua), Xiaoming Duan (Dept. of Automation, Shanghai Jiao Tong University), Zongying Shi (Tsinghua, corresponding: szy@mail.tsinghua.edu.cn), Yisheng Zhong (Tsinghua; co-corresponding: rui.yan@cs.ox.ac.uk). Author contribution note: RY conceived/wrote the draft; RD wrote Sections 3.2 and 6 (p. 10).
- **Year / Venue (EXACT, from printed header/citation block, p. 1)**: Published 10 January 2023; received 08 November 2022, accepted 21 December 2022. "Frontiers in Control Engineering" (OPEN ACCESS; TYPE Review; SPECIALTY SECTION: Networked Control; Edited by Daigo Shishika, George Mason University; Reviewed by Shaunak Bopa
[CONTRIBUTIONS]
1. **Taxonomy/survey**: a structured, selective review of M-RA differential games with simple motions, organized as game elements (Sec. 2) → two solution methods (Sec. 3) → barrier construction for five representative many-vs-one games (Sec. 4) → task allocation for many-vs-many (Sec. 5) → three cooperative strategy families (Sec. 6) → open problems (Sec. 7).
2. **Unified formulation**: a common model (dynamics (1), Assumptions 1–4, payoff (2), terminal data (3)) under which Voronoi, Apollonius, δ-Apollonius and function-based dominance regions, HJI equations, barriers, ILP assignment and convex-optimization strategies are presented in one notation (n-dimensional regions, speed ratios α_ij = v_Pi/v_Ej, capture radii r_i).
3. **Assessment of methods**: geometric method = exact and cheap whe
[RESULTS-LIST]
- **Def. 1 (Voronoi cell)**: partition V(Ω) = {R¹_p,…,R^Np_p, R¹_e,…,R^Ne_e} with R^p_i = {x ∈ Ω | ‖x − x_Pi‖₂ ≤ min{‖x − x_Pi'‖₂, ‖x − x_Ej'‖₂}, ∀i' ≠ i, 1 ≤ j' ≤ N_e} (and symmetrically R^e_j). If v_Pi = v_Ej and r_i = 0 ∀i, j, the Voronoi cell of P_i (E_j) is its dominance region. Covers equal-speed, point-capture games; simplest dominance tool.
- **Def. 2 (Apollonius circle)**: if v_Pi > v_Ej and r_i = 0, R^a_ij has center (α²_ij x_Ej − x_Pi)/(α²_ij − 1) and radius α_ij‖x_Pi − x_Ej‖₂/(α²_ij − 1), where α_ij = v_Pi/v_Ej. The evader's dominance region against P is ∩_{i=1}^{N_p} R^a_ij. Covers strict speed superiority, point capture; the intersection form underlies point-based pursuit (Sec. 6.2).
- **Def. 3 (Function-based dominance region; attributed to Yan et al. 2022, Automatica)**: f_ij: R² → R, f_ij(x) = ‖x − x_Pi‖₂ − α_ij‖x − x_Ej‖₂ − r_i; if v_Pi ≥ v_Ej and r_i ≥ 0, then {x ∈ Ω |
[CITATION]
Role in a future IEEE Trans Introduction: **primary related-work taxonomy anchor** for multiplayer reach-avoid / target-defense papers. Use it once in the opening related-work paragraph to justify the adopted methodology (barrier/game-of-kind analysis → task allocation → game-of-degree strategies), and again when motivating a gap (faster evaders, partial information, sequential capture, coupled trajectories, realistic dynamics) — its Sec. 7 is a citable menu of open problems. It also legitimizes

### P105 — Multiplayer Homicidal Chauffeur reach-avoid games: A pursuit enclosure function approach
[BIBLIO]
- **ID**: P105 / **source file**: `Yan 等 - 2024 - Multiplayer Homicidal Chauffeur reach-avoid games A pursuit enclosure function approach.pdf` / **total pages**: 13
- **Title**: Multiplayer Homicidal Chauffeur reach-avoid games: A pursuit enclosure function approach
- **Authors**: Rui Yan (School of Artificial Intelligence, Beihang University, corresponding author), Xiaoming Duan (Dept. of Automation, Shanghai Jiao Tong University), Rui Zou, Xin He, Zongying Shi (Dept. of Automation, Tsinghua University), Francesco Bullo (Center of Control, Dynamical Systems and Computation, UC Santa Barbara)
- **Year**: 2024. **Venue (exact, from header)**: Automatica, Vol. 167 (2024), Article 111770. **DOI (printed)**: 10.1016/j.automatica.2024.111770; ISSN 0005-1098. History: received 26 April 2023; revised 22 December 2023; accepted 7 May 2024; available online 10 June 2024; recommended by Associate Editor Gurdal Arslan under the direction of Editor Florian Dörfler; footnote states "The material in this paper was not presented at any conference."
- **Tier**: T1 (Automatica). Indexer guess (Automa
[CONTRIBUTIONS]
1. **Theory (winning concept)**: Pursuit enclosure functions (PEFs) and a new *enclosure region pursuit* (ERP) winning condition: a dynamically updated compact strictly convex region containing the evader must keep positive distance from $\Omega_{\text{goal}}$ at all times. ERP winning and its strategies are computed by **forward analysis** instead of backward reachability/HJI (pp. 2, 4; Definitions 1-3).
2. **Theory (complexity reduction)**: A coalition-reduction theorem: under ERP winning with positive safe distance, at most **two** pursuers of a coalition matter (support-constraint counting à la Calafiore–Campi), so only 1-vs-1 and 2-vs-1 subgames need be solved (Theorem 1, p. 5).
3. **Theory (state generation)**: A **steer-to-ERP** approach: an optimization problem (7) whose optimal va
[RESULTS-LIST]
- **Pursuer $P_i$ (Dubins car), eq. (1), p. 2**: $\dot x_{P_i}=v_{P_i}\cos\theta_{P_i}$, $\dot y_{P_i}=v_{P_i}\sin\theta_{P_i}$, $\dot\theta_{P_i}=v_{P_i}u_{P_i}/\kappa_i$, with $u_{P_i}\in\mathcal U_{\mathcal P}=\{u:[0,\infty)\to\mathcal S_1 \mid u \text{ piecewise smooth}\}$ (so $u_{P_i}\in[-1,1]$ is a normalized turning rate); $v_{P_i}>0$ max speed, $\kappa_i>0$ min turning radius.
- **Evader $E_j$ (simple motion), eq. (2), p. 2**: $\dot x_{E_j}=v_{E_j}u^x_{E_j}$, $\dot y_{E_j}=v_{E_j}u^y_{E_j}$, $u_{E_j}\in\mathcal U_{\mathcal E}=\{u:[0,\infty)\to\mathcal S_2\mid u\text{ piecewise smooth}\}$.
- **Speed ratio** $\alpha_{ij}=v_{P_i}/v_{E_j}>1$ (faster pursuers assumed). **Capture radius** $r_i>0$; capture occurs when the pursuer "is pursuing the former and their Euclidean distance is less than or equal to the pursuer's capture radius" — deliberately a **closed** capture condition, unli
[CITATION]
This paper is the multiplayer capstone of the Yan et al. Homicidal-Chauffeur reach-avoid line (companion one-vs-one TAC paper Yan et al. 2024): it introduces pursuit enclosure functions and the enclosure-region-pursuit (ERP) winning concept that converts backward HJI/terminal-surface analysis into a forward, convex-program-based sufficient condition, proves via support-constraint counting that at most two pursuers ever matter per evader, and lifts 1-vs-1/2-vs-1 subgame outcomes to a receding-hor

### P106 — Pursuit Winning Strategies for Reach-Avoid Games With Polygonal Obstacles
[BIBLIO]
- **ID**: P106. **Source file**: `D:\System\zhuomian\game-paper\Yan 等 - 2025 - Pursuit Winning Strategies for Reach-Avoid Games With Polygonal Obstacles.pdf`. **Total pages**: 16 (journal pp. 814–829; the Read tool flags the PDF as password-protected, but pymupdf reports `needs_pass=0` and opens it normally).
- **Title**: Pursuit Winning Strategies for Reach-Avoid Games With Polygonal Obstacles.
- **Authors**: Rui Yan (Beihang Univ., School of Artificial Intelligence, corresponding author), Shuai Mi, Jintao Chen, Xiangyang Ji (Tsinghua Univ., Dept. of Automation), Xiaoming Duan (Shanghai Jiao Tong Univ., Dept. of Automation).
- **Year**: 2025 — Vol. 70, No. 2, February 2025 (date of publication 6 August 2024; manuscript received 11 March 2024, accepted 27 July 2024; Recommended by Associate Editor Zhongkui Li; © 2024 IEEE).
- **Venue (exact, from running header)**: IEEE Transactions on Automatic Control, pp. 814–829. Indexer guess (TAC) confirmed correct.
- **DOI (printed)**: 10.1109/TAC.2024.3438806.
- **Tier**: T1 (IEEE Transactions on Automatic Control). No disagreement.
- **BibTe
[CONTRIBUTIONS]
1. **Theory (subgame winning regions)**: three pairs of pursuit winning regions + strategies for a coalition $P_c$ vs. one evader $E_j$ in bounded polygonal environments with general polygonal obstacles: *onsite* winning (Theorem 1/Lemma 2, expanded Apollonius circles), *goal-visible close-to-goal* winning (Theorem 2, convex GCPs), *nongoal-visible close-to-goal* winning (Theorem 4, ESP + anchored safe distance).
2. **Modeling tools**: new geometric constructs — convex goal-covering polygons (Definition 5) with existence/consistency (Lemma 4), direction range (Definition 6), first-visible obstacle vertices (Definition 9) and a constructive GCP-enlargement theorem (Theorem 3), ESP reachable region/wavefront/circular-sector decomposition (Definitions 11, 12, 14), and the anchored ESP-based s
[RESULTS-LIST]
- **Dynamics (eq. (1))**: simple (Isaacs) holonomic motion, $\dot x_{Pi}(t) = v_{Pi} u_{Pi}(t)$, $\dot x_{Ej}(t) = v_{Ej} u_{Ej}(t)$, $x_{Pi}, x_{Ej} \in \mathbb{R}^2$, controls $u \in \mathcal{U} = \{u : [0,\infty) \to \mathbb{S}^2 \mid u \text{ piecewise smooth}\}$. Speed ratio $\alpha_{ij} = v_{Pi}/v_{Ej} > 1$ (faster pursuers). Capture radius $r_i \ge 0$; **capture condition**: Euclidean distance $\le r_i$ AND the connecting segment is obstacle-free ("visual radius capture") — obstacles hence also shield capture.
- **Environment**: obstacles $O_i \subset \Omega$ simple polygons with boundaries excluded, disjoint closures; $\Omega_{\text{goal}} = \{x \mid A_i x + b_i \ge 0,\ i \in I_{\text{goal}}\}$ convex, disjoint from obstacles. State-feedback information: each team decides controls from all players' current positions.
- **Winning (Definition 1, p. 817)**: coalition $P_c$ wins agai
[CITATION]
This is the reference point for **reach-avoid games under geometric obstacles via computational geometry**: it is the first TAC-level work to construct obstacle-aware pursuit winning regions (expanded Apollonius + tangent-wedge onsite region; GCP-based goal guarding; ESP-anchored safe distance) and to fuse many-vs-one coalition outcomes into a hierarchical receding-horizon allocation with a monotone defeat-count guarantee. For a new paper it serves as (i) the canonical citation for "winning stra

### P107 — Defense penetration strategy for inferior USV based on reach-avoid game under complex target region
[BIBLIO]
- **ID**: P107. **Source file**: `D:\System\zhuomian\game-paper\Yang 等 - 2025 - Defense penetration strategy for inferior USV based on reach-avoid game under complex target region.pdf`. **Total pages**: 15 PDF pages (printed pp. 15155–15169).
- **Title**: Defense penetration strategy for inferior USV based on reach-avoid game under complex target region.
- **Authors**: Kai Yang, Xiao Liang, Cong Chen, Changdong Yu, Dianyong Liu, Wei Li (corresponding: weiwei99231@dlmu.edu.cn). Affiliations: Naval Architecture and Ocean Engineering College, Dalian Maritime University (Yang, Liang, Chen, Liu); College of Artificial Intelligence, DMU (Yu); College of Environmental Science and Engineering, DMU (Li). Dalian 116026, China.
- **Year**: 2025. **Venue (exact, from running header)**: "Nonlinear Dyn (2025) 113:15155–15169" — i.e., Nonlinear Dynamics, vol. 113, pp. 15155–15169. Indexer guess (Nonlinear Dynamics) is **correct**. **DOI**: 10.1007/s11071-025-10932-8 (printed on p. 1). Received 27 June 2024 / Accepted 23 January 2025 / Published online 3 February 2025. © The Author(s), under exclusi
[CONTRIBUTIONS]
1. **Penetration condition (PC) under complex target region** (theory): a geometric condition (eq. (20)) — the closed joint safe region S̃ (intersection of Apollonius disks of all defenders) intersects the target boundary and the signed set distance is non-increasing under the Nash guidance — proved via a KKT argument on the minimum-distance problem (eqs. (16)–(19)), with the indirect point y_F and penetration point x_I defined separately for **non-convex** (Definitions 1, eq. (10)) and **convex** (Definition 2, eq. (11)) target regions.
2. **Two-stage penetration strategy with two yaw-velocity constraints** (modeling + algorithm): Stage 1 converts the non-penetration-angle case (NPC, θ_E ≠ φ_E) into the penetration-angle case (PAC, θ_E = φ_E) using a bang-bang yaw law (eq. (42)) whose suf
[RESULTS-LIST]
**Definition 1 — Indirect point, non-convex case (eq. (9)–(10), p. 5).** The line i attaining the minimum, i = argmin_i l(∂S̃, g_i(x,y)) with g_i ∩ ∂S̃ ≠ ∅ (eq. (9)); y_F is "the unique point on ∂Ω_goal with minimum distance to ∂S̃", given as the perpendicular-foot construction through the Apollonius center o_{Aj}: x_F = [m_i/(1−λ²)]·[y_E − m̄_i x_E − λ²(y_P − m̄_i x_P) − (1−λ²)n_i]/(m̄_i²+1), y_F = [m̄_i²/(1−λ²)]·[y_E − m̄_i x_E − λ²(y_P − m̄_i x_P) + ((1−λ²)/m̄_i²)n_i]/(m̄_i²+1), where m̄_i, n̄_i are the gradient/intercept of the line orthogonal to g_i through o_{Aj}. *Defects*: λ carries no subscript j; n̄_i is declared but unused; the derivation is not shown; as printed it cannot be cross-checked against the line convention (see (11) below).
**Definition 2 — Boundary intersection, convex case (eq. (11), p. 6).** When the closest point would fall on the *extension* of an edge (convex 
[CITATION]
This is an *application-oriented RA-game paper*: it imports the standard Apollonius-circle reachable-set machinery (Isaacs; Von Moll et al. border defense) into a marine-USV penetration setting and adds two genuinely useful engineering elements — a convex/non-convex polygonal target-region treatment of the closest penetration point (Definitions 1–3), and yaw-rate-feasible, two-stage closed-loop guidance with explicit admit conditions (31)/(39) on the speed ratio λ_j, radius-to-yaw-gain ratio 2r/

### P108 — Satellite Proximate Pursuit-Evasion Game with Different Thrust Configurations
[BIBLIO]
- **ID**: P108. **Source file**: `D:\System\zhuomian\game-paper\Ye 等 - 2020 - Satellite proximate pursuit-evasion game with different thrust configurations.pdf`. **Total pages**: 10 (the Read tool flags the PDF as password-protected, but pymupdf reports `needs_pass=0` and opens it normally — same false-positive pattern as other PDFs in this collection; full text extracted and all key formulas verified against 200-dpi page renders).
- **Title**: Satellite proximate pursuit-evasion game with different thrust configurations.
- **Authors**: Dong Ye (Research Center of Satellite, Harbin Institute of Technology, 150001, Harbin, China; yed@hit.edu.cn), Mingming Shi (Faculty of Sciences and Engineering, University of Groningen, 9747AG, Groningen, the Netherlands; corresponding author, M.Shi@rug.nl), Zhaowei Sun (Research Center of Satellite, HIT; sunzhaowei@hit.edu.cn).
- **Year**: 2020 — received 19 July 2019, revised 15 December 2019, accepted 16 January 2020, available online 23 January 2020; Communicated by Christian Circi; © 2020 Elsevier Masson SAS; ISSN 1270-9638.
- **Venue (exact, fr
[CONTRIBUTIONS]
1. **Modeling**: formulation of a two-player zero-sum capture-time differential game under CW relative dynamics with dissimilar continuous-thrust constraints — cube-constrained pursuer (eq. (5)) vs. ball-constrained evader (eq. (6)), $\rho^P > \rho^E$ — serving "as a starting point for considering more complex and real satellite pursuit-evasion game" (p. 2).
2. **Theory (derivation)**: PMP-based open-loop saddle controls (eqs. (11)–(12)); adjoint antisymmetry observation (18); **Theorem 1** — equivalence of the original 12-state/12-adjoint game to a reduced 6-state/6-adjoint game (eqs. (19)–(22)), halving the state+adjoint count and leaving only 4 scalar unknowns $(\boldsymbol{\lambda}^r_f, \tau_f)$ for the TPBVP (eq. (29)).
3. **Algorithm**: an indirect solver (Algorithm 1) — PSO minimiza
[RESULTS-LIST]
- **Relative orbital dynamics (CW equations, eq. (1))**: in a local rotating frame $Oxyz$ (origin at the chief, $x$ radial, $y$ along-track, $z$ along orbital angular momentum),
- **Virtual-chief reduction (p. 2)**: if both players are close and travel short distances, a virtual chief on a circular reference orbit is placed near both trajectories and the *same* dynamics $\dot x^P = Ax^P + Bu^P$, $\dot x^E = Ax^E + Bu^E$ (eq. (4)) hold for both, with $x^P = [(\mathbf{r}^P)^\top (\mathbf{v}^P)^\top]^\top, x^E \in \mathbb{R}^6$. Both dynamics share one $A$ — the fact that makes the adjoint antisymmetry below possible.
- **Thrust configurations (continuous thrust, not impulsive)**: pursuer $|u^{P,x}| \le \rho^P$, $|u^{P,y}| \le \rho^P$, $|u^{P,z}| \le \rho^P$ (eq. (5), cube $\mathcal{U}^P$); evader $\|u^E\|_2 \le \rho^E$ (eq. (6), ball $\mathcal{U}^E$); assumption $\rho^P > \rho^E$ (p. 2). T
[CITATION]
This paper is the natural **modeling-baseline and cautionary reference for actuator-asymmetric orbital pursuit–evasion games**: it is, to the knowledge recorded here, the first archive entry to mix an $L_\infty$-box (three orthogonal thrusters) pursuer with an $L_2$-ball (single-thruster) evader under CW dynamics, and its reusable assets are (i) the cube-vs-ball PMP control pair (eqs. (11)–(12)) showing exactly where the discontinuity enters (componentwise sign vs. normalized alignment), (ii) th

### P110 — Hierarchical Mean-Field Deep Reinforcement Learning for Large-Scale Multiagent Systems
[BIBLIO]
- **ID**: P110. **Source file**: `D:\System\zhuomian\game-paper\Yu - 2023 - Hierarchical Mean-Field Deep Reinforcement Learning for Large-Scale Multiagent Systems.pdf`. **Total pages**: 9 (proceedings pp. 11744–11752). The Read tool flags the PDF as password-protected, but pymupdf reports `needs_pass=0` / `is_encrypted=False` and opens it normally — same false-positive pattern as other PDFs in this collection; full text extracted and all key formulas verified against 200-dpi page renders.
- **Title** (p. 1): Hierarchical Mean-Field Deep Reinforcement Learning for Large-Scale Multiagent Systems.
- **Authors**: Chao Yu (single author), with dual affiliations: (1) School of Computer Science and Engineering, Sun Yat-sen University, Guangzhou, China; (2) Pengcheng Laboratory, Shenzhen, China; yuchao3@mail.sysu.edu.cn (p. 1, verified against the rendered title page).
- **Year**: 2023 (copyright line: "Copyright © 2023, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved.", p. 1).
- **Venue (exact, from page-1 running header)**: "The Thirty-Seventh
[CONTRIBUTIONS]
1. **Modeling (value factorization)**: individual joint Q-function split into a local part and an individual-MF (IMF) part, $Q^k(s,a) = Q^k_{\mathrm{LOC}}(x_k) + Q^k_{\mathrm{IMF}}(\mu(x), x_k)$, $x_k=(o_k,a_k)$ (eq. (6), p. 2) — with the IMF conditioned on the neighborhood average *including the agent itself* (p. 2–3), in contrast to MFVFD's neighbor-only mean of eq. (5).
2. **Theory (group mean-field collapse, derivation chain eqs. (7)–(11), p. 3)**: the influence-weighted sum of all individual joint Q-functions of a group (eq. (7)) is shown to reduce, under an additive virtual-reward decomposition and a first-order Taylor argument, to $\ Q_{\mathrm{GRP}}(x) = \sum_{k\in N}\lambda_k Q^k_{\mathrm{LOC}}(x_k) + 2\,Q_{\mathrm{GMF}}(\mu(x))$ (eq. (11)) — i.e., one Group MF function $\bar{Q}\e
[RESULTS-LIST]
- **Stochastic game** (p. 2): $\langle \mathcal{S}, \mathcal{A}^1,\dots,\mathcal{A}^N, r^1,\dots,r^N, p,\gamma\rangle$, $\gamma\in[0,1)$; $r^k:\mathcal{S}\times\mathcal{A}^1\times\dots\times\mathcal{A}^N\to\mathbb{R}$; $p:\mathcal{S}\times\mathcal{A}^1\times\dots\times\mathcal{A}^N\to\Omega(\mathcal{S})$; joint policy $\pi\triangleq[\pi^1,\dots,\pi^N]$; value $v^k_\pi(s)=\sum_{t=0}^\infty\gamma^t\mathbb{E}_{\pi,p}[r^k_t\,|\,s_0=s]$; Bellman pair $Q^k_\pi(s,a)=r^k(s,a)+\gamma\mathbb{E}_{s'\sim p}[v^k_\pi(s')]$, $v^k_\pi(s)=\mathbb{E}_{a\sim\pi}[Q^k_\pi(s,a)]$. Local-information input converts this to Partially Observable Stochastic Games (citing Yang and Wang 2020) — the formal scaffold of everything that follows.
- **Pairwise decomposition (eq. (1))**: $Q^k(s,a)=\frac{1}{\mathcal{N}^k}\sum_{j\in\mathcal{N}(k)}Q^k(s,a^k,a^j)$, $\mathcal{N}^k$ = number of neighbors, $\mathcal{N}(k)$ = neig
[CITATION]
This is the reference implementation of *hierarchical/group-structured mean-field MARL*: it is the natural citation when a large-population learning or pursuit problem (e.g., many-pursuer interception, swarm coverage, mass dynamics) requires coordination beyond a single neighbor-averaging layer, and when execution must rely on local observations only. It also anchors the "uniform averaging discards per-neighbor influence" argument (attention-weighted MF) and the El Farol/Bar-game evidence for MF

### P111 — Impulsive Maneuver Strategy Design for Target–Attacker–Defender Game of Spacecrafts via a Curriculum Learning-
[BIBLIO]
- ID: P111. Source file: `D:\System\zhuomian\game-paper\Yuan 等 - 2026 - Impulsive Maneuver Strategy Design for Target–Attacker–Defender Game of Spacecrafts via a Curriculum.pdf` (filename in mission was truncated; full title from p. 1). Total pages: 14 (pp. 11404–11417).
- Title: "Impulsive Maneuver Strategy Design for Target–Attacker–Defender Game of Spacecrafts via a Curriculum Learning-Based Hamilton-Regularized MATD3 Algorithm".
- Authors: Huanhuan Yuan (School of Astronautics, National Key Laboratory of Aerospace Flight Dynamics, Northwestern Polytechnical University, Xi'an, China; corresponding address yuanhh@nwpu.edu.cn), Xiangyu Wang (NWPU), Yuan Yuan (NWPU; corresponding author).
- Year: 2026. Received 11 June 2025; revised 3 April 2026; accepted 11 May 2026; published online 19 May 2026; current version 22 June 2026. Refereeing handled by E. Bakolas.
- Venue (EXACT from header/copyright): IEEE Transactions on Aerospace and Electronic Systems, Vol. 62, 2026, pp. 11404–11417. Indexer guess (IEEE TAES) is CORRECT. DOI printed: 10.1109/TAES.2026.3694782. Copyright 0018-9251 © 2
[CONTRIBUTIONS]
Stated as threefold (p. 11406), with my classification:
1. **Algorithm (theory-flavored)**: HMATD3 — MATD3 with a "Hamiltonian regularization" loss added to each value network's TD loss (eqs. (18)–(27)), claimed to stabilize training and improve exploration/convergence. This is a heuristic loss-shaping contribution; no convergence or optimality proof is given.
2. **Training methodology**: a performance-driven adaptive curriculum that adjusts the maneuver interval Δt online via a staircase map of a sliding-window truncated rate (eqs. (28)–(30)), combined with a dual-component reward architecture (process-oriented + terminal-condition rewards, eqs. (31)–(35)) to fight sparse-reward local optima.
3. **Constraint-handling mechanism**: a sun-elevation-angle adaptation method that rotates the in
[RESULTS-LIST]
- **CW equations (p. 11406, eq. (1))**: in the LVLH frame centered at the nonmaneuverable target,
- **Assumption 1 (p. 11406)**: (1) relative distances ≪ orbit radius so CW applies; (2) attack/defense spacecraft maneuver by instantaneous impulsive velocity changes and attitude adjustment is instantaneous (radar always faces the opponent); (3) both maneuverable spacecraft use the same fixed maneuver interval Δt during the game. (Note: Assumption 1(3) holds within an episode; the curriculum of eq. (30) varies Δt across episodes — see §7.)
- **Discretized state transition (p. 11406, eq. (2))**: with state x_l(t_i) = [r_l^T(t_i), v_l^T(t_i)]^T, l ∈ {A, D}:
- **STM blocks (p. 11407, unnumbered, verified from rendered page)**: with s ≡ sin(nΔt), c ≡ cos(nΔt):
- **Impulse model (p. 11407, eq. (3))**: v_l(t_i⁺) = v_l(t_i⁻) + Δv_l(t_i), l ∈ {A, D}.
- **Coasting phase (p. 11407, eq. (4))**: betwee
[CITATION]
Role in the literature: this is the bridge paper between the classical TAD differential-game corpus (Garcia/Casbeer/von Moll-style TAD, Coon–Panagou multiplayer TAD, Li–Liang–Dang orbital TAD) and the MARL-for-orbital-games line (PRD-MADDPG [18], elliptical-orbit RL [19]); within the game-paper skill it is the primary T1 reference for (i) CW-equation impulsive TAD modeling with STM discretization, (ii) constrained multiagent RL reward/constraint engineering (process+terminal reward decomposition

### P112 — Evasion strategies of a three-player lifeline game
[BIBLIO]
- **ID**: P112. **Source file**: `D:\System\zhuomian\game-paper\Zhang和Zha - 2018 - Evasion strategies of a three-player lifeline game.pdf`. **Total pages**: 11 (article-numbered 112206:1–112206:11).
- **Title**: Evasion strategies of a three-player lifeline game.
- **Authors**: Fan Zhang (School of Automation, Beijing Institute of Technology, Beijing 100081; State Key Laboratory of Intelligent Control and Decision of Complex System, Beijing 100081) and Wenzhong Zha (Information Science Academy, China Electronics Technology Group Corporation, Beijing 100086; corresponding author, zhawenzhong@126.com). Printed footnote: "Zhang F and Zha W Z have the same contribution to this work."
- **Year/Venue**: November 2018, **Science China Information Sciences** ("SCIENCE CHINA Information Sciences" printed on p. 1 header; citation block prints "Sci China Inf Sci, 2018, 61(11): 112206"). The indexer guess (Science China Technological Sciences vs. Information Sciences) resolves to **Science China Information Sciences**, Vol. 61, No. 11, article 112206. **DOI (printed)**: 10.1007/s11432-017-9408-6
[CONTRIBUTIONS]
1. **Theory (barrier of the two-player sub-game)**: closed-form parametric barrier $\mathscr{B}_1$ (and by symmetry $\mathscr{B}_2$) of the $E$ vs. $P_i$ lifeline sub-game in the reduced state space, via Isaacs' main equation, optimal strategies, and RPE integration from the whole BUP (Theorem 1, p. 5, eq. (6); p. 6, eq. (17)).
2. **Theory (barrier of the three-player game)**: the three-player barrier $\mathscr{B}$ is the "bond" of $\mathscr{B}_1$ and $\mathscr{B}_2$ — with pursuers fixed at $(-u,h_1)$, $(u,h_2)$, the evader's barrier trajectory is the piecewise curve (20) switching at the intersection $(\tilde x,\tilde y)$ of the two sub-game curves (Theorem 2, p. 6, eqs. (18)–(20)); capture zone of the joint game = union of sub-game capture zones because "the pursuers play individually."
[RESULTS-LIST]
- **Dynamics** (p. 3, eqs. (3)–(4)), simple motion in the half-plane, headings measured from the downward vertical:
- **Information structure** (p. 4): "the instantaneous positions and velocities of the players are available to their opponents" — perfect full-state information, perfect recall.
- **Termination/winning conditions** (p. 4, Sec. 3): (1) $y_e = 0$ and $\min\{d_1,d_2\}\ge l$ $\Rightarrow$ $E$ wins; (2) $y_e > 0$ and $\min\{d_1,d_2\} < l$ $\Rightarrow$ pursuers win; otherwise the game proceeds. Terminal manifold (Def. 1, eq. (2)): $\mathcal{D} = \{x,t \mid G(x(t),t)=0\}$; for the joint game one component $\min\{d_1,d_2\}=l$ is "indeterminate," which blocks the classic single-BUP RPE construction (p. 4).
- **Reduced state** for sub-game 1 (p. 4): $x_1 = x_{p_1}-x_e$, $y_1 = y_{p_1}$, so (eq. (5)):
- **Roles**: pursuers are homogeneous (same speed, same payoff form); the lifeline
[CITATION]
**Paragraph role**: P112 is the reference point for the *lifeline (reach-a-line) variant of three-player pursuit-evasion*: it is, to this archive's knowledge, among the first to give an explicit analytic barrier for two pursuers vs. one evader with a line target, by combining Isaacs-style barrier construction (Theorem 1) with a decomposition/bond integration (Theorem 2) and an explicit-policy layer (regions A–D) that operationalizes the escape zone. In a reach-avoid/target-defense paper it serve

### P113 — Cooperative pursuit with Voronoi partitions
[BIBLIO]
- **ID**: P113
- **Source file**: `D:\System\zhuomian\game-paper\Zhou 等 - 2016 - Cooperative pursuit with Voronoi partitions.pdf`
- **Total pages**: 9 (journal pages 64–72)
- **Title**: Cooperative pursuit with Voronoi partitions
- **Authors**: Zhengyuan Zhou (Dept. of Electrical Engineering, Stanford University); Wei Zhang (Dept. of ECE, Ohio State University); Jerry Ding (Dept. of EECS, UC Berkeley); Haomiao Huang (Kuna Systems, CA); Dušan M. Stipanović (Control and Decision Group, Coordinated Science Laboratory, University of Illinois, Urbana); Claire J. Tomlin (Dept. of EECS, UC Berkeley)
- **Year**: 2016
- **Venue** (EXACT from header/copyright): *Automatica* 72 (2016) 64–72, article type "Brief paper". Copyright line: "0005-1098/© 2016 Elsevier Ltd. All rights reserved." Indexer guess "Automatica" is **correct**. Footnote: material presented at the 50th IEEE Conference on Decision and Control and European Control Conference (CDC-ECC), December 12–15, 2011, Orlando, FL; recommended by Associate Editor Hideaki Ishii under the direction of Editor Ian R. Petersen. History: received
[CONTRIBUTIONS]
1. **Strategy (modeling/algorithm)**: A cooperative pursuit law defined by the Voronoi partition of Ω generated by all agent positions; each pursuer moves in the direction that most steeply decreases the area A of the evader's Voronoi cell S_e (Eq. (6)); non-neighbors of the evader fall back to pure pursuit (Sec. 3.1). Decentralized: inputs decouple given the shared partition (information = agent positions only).
2. **Geometric characterization (theory)**: Theorem 2 — under the area-gradient strategy each pursuer heads exactly for the midpoint of its line of control B_i (the shared Voronoi edge), giving a closed-form, easily implementable input from local geometry (L_i, l_i, ‖ξ_i‖).
3. **Capture guarantee (theory)**: Theorem 3 — an energy function E = kA + ‖x_e − x_p‖² decreases at a linea
[RESULTS-LIST]
- **Dynamics (Eq. (1))**: ẋ_e = d, x_e(0) = x_e^0; ẋ_p^i = u_i, x_p^i(0) = x_{p}^{i,0}, i = 1,…,N — kinematic single integrators in ℝ².
- **Input constraints (Eq. (2))**: D = {d | ‖d‖ ≤ v_{e,max}}, U_i = {u_i | ‖u_i‖ ≤ v_{i,max}} (Euclidean norm).
- **State constraint (Eq. (3))**: x_e(t), x_p^i(t) ∈ Ω ∀t ≥ 0; inputs satisfying (2)–(3) are *admissible*.
- **Closed loop (Eq. (4))**: ẋ_p^i = μ_i(x_e, x_p^1, …, x_p^N); evader uses an admissible strategy γ; admissible strategy sets U, D.
- **Termination/winning condition**: capture when at least one pursuer is within distance r_c > 0 of the evader (p. 65). Pursuers win if capture occurs in finite time against all admissible evader inputs.
- **WLOG normalization** (Sec. 3 opening): by re-scaling, v_{e,max} = v_{i,max} = 1 for the convex-domain analysis.
- **Voronoi partition** V(Ω) = {S_e, V_1, …, V_N} generated by {x_e, x_p^1, …, x_p^N}:
- **
[CITATION]
This is the journal archetype of the "Voronoi/area-minimization cooperative pursuit" line: it converts a high-dimensional multi-agent differential game into N independent low-dimensional gradient descent problems coupled only through a shared geometric partition, and it is one of the few cooperative pursuit papers with an explicit finite-time capture proof for a *decentralized, implementable* law (energy function E = kA + ‖x_e − x_p‖² decreasing at rate c(β)). Cite it (a) as the canonical refere

### P114 — Nature-inspired dynamic control for pursuit-evasion of robots
[BIBLIO]
- **ID**: P114
- **Source file**: `D:\System\zhuomian\game-paper\Zhou 等 - 2026 - Nature-inspired dynamic control for pursuit-evasion of robots☆.pdf`
- **Total pages**: 9 (journal pages 1–9 of article 112629; p. 1–8 body, p. 9 references + author biographies)
- **Title**: Nature-inspired dynamic control for pursuit-evasion of robots
- **Authors**: Panpan Zhou (Dept. of Mathematics, KTH Royal Institute of Technology, Stockholm); Sirui Li (Division of Transport and Systems Analysis, KTH); Benyun Zhao (Dept. of Mechanical and Automation Engineering, The Chinese University of Hong Kong); Bo Wahlberg (Division of Decision and Control Systems, KTH); Xiaoming Hu (Dept. of Mathematics, KTH; corresponding author, hu@kth.se)
- **Year**: 2026 (issue dated; accepted 26 August 2025, available online 26 September 2025)
- **Venue** (EXACT from header/copyright): *Automatica* 183 (2026) 112629, article type "Brief paper". Copyright line: "© 2025 The Author(s). Published by Elsevier Ltd. ... open access article under the CC BY license (http://creativecommons.org/licenses/by/4.0/)". Indexer guess "Auto
[CONTRIBUTIONS]
1. **Dynamic framework (modeling)**: both players modeled as unicycles (Eq. (1)) with constraints 0 ≤ v ≤ V^max, w ≤ W^max (Eq. (2)) and the predator–prey asymmetry V_p^max > V_e^max, W_p^max < W_e^max (Eq. (3)); angular velocity is additionally bounded by the centripetal limit r·v⁻¹ (turning radius r/v² grows with speed), encoding the empirically observed anti-correlation between speed and agility (Wilson et al. 2013).
2. **Alert-Turn escape/pursuit strategy (algorithm)**: Algorithm 1 partitions the encounter into a long-distance phase (straight flee/chase with finite-time heading alignment, Eqs. (4)–(6)) and a short-distance phase (decelerate-then-accelerate sharp turn with distance-dependent angular velocity, Eqs. (7)–(8)), plus a stop condition at capture radius ε₂.
3. **Two-level anal
[RESULTS-LIST]
- **Dynamics (Eq. (1))**: unicycle models — ẋ_p = v_p cos θ_p, ẏ_p = v_p sin θ_p, θ̇_p = w_p; ẋ_e = v_e cos θ_e, ẏ_e = v_e sin θ_e, θ̇_e = w_e. Position col(x,y) := [x y]^T ∈ ℝ²; control u = col(v, w) ∈ ℝ². Full-state information: each player knows the relative position (bearing ∆θ_pe = atan((y_e−y_p)/(x_e−x_p)) is the orientation of the vector from pursuer to evader); no noise/delay modeled.
- **Constraints (Eq. (2))**: 0 ≤ v_p(t) ≤ V_p^max, 0 ≤ v_e(t) ≤ V_e^max (no reverse motion), w_p(t) ≤ W_p^max, w_e(t) ≤ W_e^max — printed without absolute-value bars on w (the intended bound is |w| ≤ W^max, cf. (4), (6), (8)).
- **Role asymmetry (Eq. (3))**: V_p^max > V_e^max, W_p^max < W_e^max — the predator is faster, the prey more agile.
- **Maneuverability model**: angular velocity commands are bounded by min(r v⁻¹, W^max), where r is the centripetal acceleration and r/v is the inverse turning r
[CITATION]
**Paragraph role**: P114 is the reference example of the *bio-inspired, non-game-theoretic* branch of pursuit–evasion research: it replaces the Isaacs/value-function machinery with a two-phase behavioral control law (Alert-Turn) on unicycles whose angular-rate bound r·v⁻¹ encodes the speed-dependent turning radius — the quantitative core of the "faster but less agile predator vs slower but more agile prey" trade-off. It is most useful to this library as (a) the modernized, nonlinear-dynamics suc

### P115 — A Survey of Decision Making in Adversarial Games
[BIBLIO]
- **ID**: P115 | **Source file**: `D:\System\zhuomian\game-paper\s11432-022-3777-y.pdf` | **Total pages**: 28 (article-numbered 141201:1–141201:28). PDF flagged "password-protected" by the Read tool but opens normally (pymupdf: `needs_pass: 0`); text extracted with pymupdf, ambiguous formulas verified against 200-dpi rendered page images.
- **Title**: A survey of decision making in adversarial games
- **Authors**: Xiuxian LI (1,2), Min MENG (1,2, corresponding author, mengmin@tongji.edu.cn), Yiguang HONG (1,2), Jie CHEN (1,2). Affiliations: (1) College of Electronics and Information Engineering, Tongji University, Shanghai 201804, China; (2) Shanghai Research Institute for Intelligent Autonomous Systems, Shanghai 201210, China.
- **Year**: 2024 (Received 28 Sep 2022 / Revised 21 Jan 2023 / Accepted 21 Mar 2023 / Published online 4 Feb 2024; issue: April 2024)
- **Venue** (EXACT from page-1 header/copyright): "SCIENCE CHINA Information Sciences", April 2024, Vol. 67, Iss. 4, 141201:1–141201:28, © Science China Press 2024 (link.springer.com also printed). Indexer guess "Science China I
[CONTRIBUTIONS]
1. **First systematic overview of adversarial games [authors' claim]** across game models, (approximate) equilibrium concepts, complexity, algorithms, applications, and future directions — orthogonal/complementary to the specialized surveys of Table 1.
2. **Unified model exposition** (Sec. 2): formal definitions of NFG, II-EFG (with infosets, perfect recall, exploitability), zero-sum team games with TME, GSG/SSG, and TP-ZS-DG, each with its canonical solution concepts (Defs. 1–5: ε-NE, ε-CE, ε-CCE, TME, SSE).
3. **Complexity and feature synthesis**: Table 3 maps game models → solution concepts → computational complexity; Table 4 maps models → player numbers, action order, information structure, dynamics; Table 5 gives SSG complexity vs. resource homogeneity and schedule size [from their re
[RESULTS-LIST]
- **NFG (Sec. 2.1)**: tuple (N, A, u), N:=[n]; A=A_1×⋯×A_n; u_i:A_i→R; mixed strategy π_i∈Δ(A_i); expected utility E_{a∼π}[u_i(a)]; social welfare SW(a):=Σ_i u_i(a); constant-sum if Σ_i u_i(a)=c_s, zero-sum if c_s=0. Continuous action sets (closed, convex) → continuous games.
- **II-EFG (Sec. 2.1)**: tuple (N, H, Z, A, P, μ, u, I) with histories H, terminal nodes Z, chance player c, player function P, infoset partition I_i of H_i with identical action sets per infoset; perfect recall formally defined via prefix-order histories; normal-form plan a_i∈Ξ_i=×_{I_{i,j}∈I_i}A(I_{i,j}); behavioral strategy π_i; reach probability p^π(h); expected payoff u_i(π)=Σ_{h∈Z} p^π(h)u_i(h). Best response BR(π_{−i}):=argmax_{π'_i} u_i(π'_i,π_{−i}). **Exploitability** e(π_i):=u_i(π*_i,π*_{−i})−u_i(π_i,BR(π_i)); multiplayer total exploitability/NashConv e(π):=Σ_{i∈[n]}[u_i(BR(π_{−i}),π_{−i})−u_i(π_i,π_{−i})]
[CITATION]
- **Role**: ideal Introduction/Related-Work anchor when a paper needs a single citation covering the whole adversarial-games landscape — from discrete zero-sum/Stackelberg security games to continuous-time zero-sum differential games — and for motivating why game-theoretic equilibrium computation connects to AI (CFR/PSRO/PoG/NAC, GANs). For differential-game papers (pursuit–evasion, reach–avoid, target defense), it serves as the "state of the art in the broader adversarial decision-making" citat
