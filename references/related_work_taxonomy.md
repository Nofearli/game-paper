# Related-Work Taxonomy — Placing Any New Work in the Library's Map of the Field

The library's own taxonomy of differential-game research, organized so a writer can locate any
new paper's cell and assemble the correct citation set. Synthesized (**[归纳]**) from the
Section 1 topics, Section 3 gap framings, and Section 8 citation-value records of
`papers/PXXX.md`; verify each cell's standard assumptions against the named archives before
reusing them in a manuscript. Primary taxonomy anchor to cite in a paper's opening related-work
paragraph: P104 (multiplayer reach-avoid review, whose Sec. 7 is a citable open-problem menu),
supplemented by P044 (PE-games tutorial that canonizes the 1v1/Nv1/1vM/NvM player-count
taxonomy) and P115 (broad adversarial-games survey).

**Anti-plagiarism rule (binding):** paraphrase all one-line contributions below when writing;
never copy prose from the papers or from these archives.

---

## 1. Problem-class taxonomy

### 1.1 Pursuit–evasion (PE) — capture time as the currency
Representative papers and one-line contributions:
- P044: peer-reviewed tutorial; the 1v1/Nv1/1vM/NvM taxonomy, HJI verification theorem, and
  fully worked 2P1E solution templates.
- P053: isochron-based complete solution of the damped-double-integrator pursuer vs.
  single-integrator evader game, with a 16-case game-of-kind taxonomy.
- P069: dominance regions with obstacles; every isochrone piece remains a circular arc about a
  known center, so dominance boundaries are limaçons/Apollonius curves.
- P041: rigorous proof that shortest-path dominance regions equal open-loop reachable regions
  under non-anticipative (Elliott–Kalton) information, with and without obstacles.
- P070: relay pursuit with steering — active pursuer chooses direct chase or herding toward a
  static teammate; capture condition on initial geometry.
- P077: time-metric (log-risk) state partition safe/failing/risky; quickest-descent evasion
  feedback against relay pursuit.
- P066: multi-pursuer cooperative capture as a min–max game on the growth rate of the evader's
  Apollonius-disc-intersection safe set (area gradients without closed-form area).
Standard assumptions of the cell: simple motion or one non-integrator side; point or small
capture radius; perfect or relay-model information; capture time (game of degree) or
capture/no-capture (game of kind) as payoff.

### 1.2 Reach-avoid (RA) — line/region defense with speed-superior defenders
- P099: closed-form 2D1A barriers (Voronoi + Apollonius + hyperbola arcs) in a bounded rectangle;
  necessary-and-sufficient condition for when a second defender matters.
- P100: analytical barriers for pursuit coalitions of arbitrary size in convex domains; at most
  two pursuers ever needed per evader; optimal matching via a 0-1 integer program.
- P103: 3D heterogeneous multiplayer RA with nonzero radii; evasion-space certificates; at most
  three pursuers necessary; NP-hardness + 1/3-approximation for constrained matching.
- P091: barriers for heterogeneous capture radii across all three speed-ratio regimes
  (offset-Apollonius curves, Cartesian-oval advantage angles, coalition coverage condition).
- P106: winning regions with polygonal obstacles (expanded Apollonius, goal-covering polygons,
  ESP-anchored safe distance) fused into a receding-horizon strategy with a monotone defeat count.
- P105: multiplayer Homicidal Chauffeur RA via pursuit enclosure functions; forward analysis
  replaces backward HJI; two-pursuer coalition reduction.
- P019: one defender vs. two cooperative attackers; only fully proved value function in the
  class; m-branch viscosity lemma; singular-surface classification.
- P054, P061: RA under damped double-integrator dynamics (isochrone tangency tests; multiple
  reachable regions).
Standard assumptions: defenders faster (α > 1) in the geometric line; straight/convex target
sets; state feedback; games of kind decided by barriers; degree payoffs = distance on arrival.

### 1.3 Target-attacker-defender (TAD) / active target defense — three-player, adversarial attacker
- P022: complete closed-form ATDDG solution in the 6-D frame; quartic-parameterized saddle-point
  strategies; C1 Value α·AI ± TI; hyperbola barrier; no singular surfaces.
- P055: speed-varying second-order plants with saturated forces; average-speed-ratio reduction;
  PMP force allocation + HJI verification.
- P080: TAD with nonzero attacker capture radius; Apollonius oval replaces the circle; limit
  interception curve barrier test.
- P082: both attacker and defender radii nonzero under equal speeds; two-sided PMP for three
  target placements.
- P090: multi-agent TAD as nonzero-sum LQ game; anomalous (greedy/fearful) defenders modeled by
  cost-coefficient scaling; visibility-network masking; inverse game theory.
Standard assumptions: A and D comparable speeds, T slower; simple motion; point or asymmetric
radii; perfect feedback (P090 excepted); Type-P order of preference to exclude nontermination
(P022).

### 1.4 Target guarding — static target, defender-vs-intruder
- P050: MDSA convex-target guarding; geometric candidate value proven the viscosity HJI solution
  via parametric convex programming and Clarke subdifferentials; coalition-partition allocation.
- P031: HJI justification of the geometric solution for faster defenders and convex targets
  (implicit-function treatment of the tangency point).
- P098: compact convex targets; metric-projection-generalized Apollonius barrier.
- P048: one defender vs. heterogeneous cooperative attackers with importance weights; SOSC-based
  classical Isaacs verification.
- P011: target guarding with attacker time limit and detection range; two-threshold
  bypass/penetrate classification.
Standard assumptions: defender strictly faster; convex (or circular) targets; payoff = distance
to target on capture/breach.

### 1.5 Perimeter defense — cyclic/symmetric perimeters and worst-case intruder streams
- P015: local-game decomposition of multi-player perimeter defense; polynomial-time provably
  optimal team strategy via matching intruder/defender bounds.
- P025: 3-D perimeter defense with surface-constrained defender (hemisphere vs. ground plane);
  optimal breaching point.
- P005/P006/P008/P009: competitive-analysis thread — impossibility thresholds and
  competitive ratios on a line, conical environments, and multivehicle extensions; randomized
  lower bounds via Yao's principle (P009). Information structure: online algorithm vs.
  adversarial release process (worst-case, non-strategic intruders).
- P007, P086: actuator-constrained defense (turret with slew rate and startup time; turret +
  mobile defender hybrid team).
Standard assumptions: fixed perimeter geometry; capture/breach counts as payoff; competitive
ratio as the guarantee; intruders adversarial in timing, not strategic.

### 1.6 Capture-the-flag (CTF) — two-phase reach-observe-return
- P039/P040: founding two-phase formulation and complete numerical HJI solution (constrained
  viscosity solutions; sequential composition of stage winning sets); BEARCAT human-in-the-loop
  validation (P040).
- P034/P038: closed-form two-player CTF (attack/transition/retreat) with orthogonal-bisector
  aimpoints, C1 Values, HJI verification; dispersal surface at the phase boundary.
- P021: multi-defender CTF with general convex flag/return regions; value = quasi-convex program;
  at most two defenders needed.
- P018: ellipse as the two-phase analogue of the Apollonius circle (CTF-type thief–guarders).
- P089: matching-based multiplayer CTF with two alliances; two-phase joint optimal strategy.
- P058: CTF with half-plane flag and return regions, heterogeneous pursuers and nonzero radii;
  flag-aware via-point potentials; necessary-and-sufficient pursuit winning conditions.
Standard assumptions: staged objectives; phase boundary = flag contact; defender exclusion from
flag/return regions encoded as opponent winning conditions (P039's constraint-encoding trick).

### 1.7 Lifeline games — reach-a-line with deadline structure
- P102: lifeline game with limited lifetime; l-Apollonius evasion region; tangency barrier.
- P094: two-lifeline game (strip between two parallel lines), two pursuers; Cartesian-oval
  reachable region; terminal payoff = min distance to both lifelines.
- P093: one superior pursuer vs. multiple evaders with two lifelines; delay-aware barriers
  (dispatch time shrinks dominance regions); cooperative sacrifice values.
- P112: three-player lifeline game; barrier "bond" of two sub-game barriers.
Standard assumptions: parallel goal lines; nonzero capture radius; speed-superior pursuer;
payoff = signed distance to nearest line.

### 1.8 Reconnaissance — penetrate-observe-return
- P049: two-player reconnaissance game with disjoint half-planar target and retreat regions;
  two-phase decomposition with HJI-verified values.
- P056: reconnaissance-penetration with territorial-constrained defender; explicit-policy method
  replacing HJI; escape-angle theorems.
- P095: partial-information target defense with a line-segment obstacle; forced detour enlarges
  the defender's guaranteed angular set.
- P079: learning-based multi-stage reconnaissance (approach–recon–retreat) with unequal sensing;
  phase-specific rewards.
- P092: surveillance of a faster fixed-course target; two-phase approach/observation optimal
  control; Decision Line from Apollonius circles (dwell time as currency).
Standard assumptions: three phases with distinct payoffs; myopic intruder goals (P049);
territorial/visibility constraints on the defender.

### 1.9 Task allocation for adversarial teams (the combinatorial layer)
- P100: 0-1 integer program over ≤2-pursuer coalitions from analytical barriers.
- P103: constrained matching (MBMC), NP-hard + APX-complete, 1/3-approximation.
- P054: minimum-makespan distributed allocation (distributed Hungarian + binary search) with a
  sensing-range design rule.
- P084: distributed k-WTA dynamical network + load reassignment for multitarget pursuit.
- P045: anonymous hedonic games with social inhibition; Nash-stable partitions with polynomial
  convergence for decentralized task allocation.
- P059: LLM-driven assignment with analytic revision restoring feasibility of the matching.
- P033: 3D multiplayer subgames solved in closed form, then weighted bipartite matching with
  online rematching.
Standard assumptions: allocation precedes or accompanies pursuit; subgame outcomes (win/lose or
capture time) as edge weights; conflict constraint "one pursuer, one coalition".

---

## 2. Method taxonomy (cross-cutting the problem classes)

### 2.1 Geometric-analytic (dominance regions, barriers)
Tools: Apollonius circle/sphere/oval, Voronoi diagrams, Cartesian ovals, isochrones, evasion
space, attack-region method, enclosure functions, l-Apollonius circles.
Papers: P099, P100, P103, P091, P098, P013, P069, P053, P102, P094, P105, P092, P067.
Standard assumptions: simple motion (or one integrator side); speed superiority; exact positions.
Output: games of kind (winning regions) + games of degree (aim points, straight-line strategies).
Weakness recorded by the archives: geometric candidates often lack HJI/viscosity certification
unless paired with 2.2 or 2.5 (motivating P031, P050).

### 2.2 HJI-computational (level sets, viscosity solutions)
Papers: P040, P039 (founding CTF numerical line); P019 (viscosity value + singular surfaces);
P085 (value-iteration ADP for multiplayer HJB); P050 (viscosity verification of a geometric
candidate).
Standard assumptions: dimension small (practical limit ≈ 5 joint states, recorded in P105/P106;
P103's 12-state estimate 10^12 grid points); compact domains; boundary data on capture/target
sets. Output: complete winning regions + feedback strategies, offline.

### 2.3 PMP / two-sided Pontryagin (characteristics route)
Papers: P022 (costates constant ⇒ straight-line optimal play; quartic design equation), P037,
P055 (force allocation bang-bang then coast), P056, P052, P108 (orbital CW dynamics, adjoint
antisymmetry).
Standard assumptions: Mayer (terminal) payoff; simple or Newtonian dynamics; Hamiltonian
separable in controls so Isaacs' condition holds. Output: open-loop/feedback extremals + Value
candidates that then need verification.

### 2.4 Game-theoretic assignment & optimization-duality
Papers: P100 (0-1 IP), P103 (MBMC + approximation), P054 (distributed Hungarian + binary
search), P045 (hedonic games), P059 (LLM + revision), P033, P089, P037 (max over matchings of
Apollonius pair sums), P021 (value = quasi-convex program; Danskin gradients), P050 (value =
parametric convex program; KKT–Isaacs bridge).
Standard assumptions: subgame outcomes precomputed; coalition sizes bounded by a degeneration
theorem (≤2 in 2-D: P100, P105, P021; ≤3 in 3-D: P103); conflict graphs encode player reuse.
Output: team-level guarantees (capture counts) with complexity classes.

### 2.5 Learning-based (RL, ADP, LLM)
Papers: P046 (CBF safeguarding layer + off-policy ADP; bounded tanh strategies; safety
throughout learning), P097 (Apollonius partitions + ordinal potential game + MARL), P078
(min–max Q-learning learning payoff-matrix entries of a reduced matrix game), P079 (multi-stage
reconnaissance MARL with opponent-trajectory prediction), P111 (curriculum-regularized MATD3
for impulsive orbital TAD), P059 (LLM with analytic revision), P002/P003 (fuzzy/hybrid RL
engineering references).
Standard assumptions: simulated or data-driven dynamics; rewards encode objectives; guarantees
are empirical unless hybridized with 2.1 (the "LLM proposes, analytic certificate disposes"
pattern of P059; the "geometry seeds RL" pattern of P097).

### 2.6 Worst-case / competitive analysis (perimeter stream)
Papers: P005, P006, P008, P009. Assumptions: non-strategic but arbitrarily timed intruder
releases; online algorithm sees only the revealed prefix; guarantees = competitive ratios with
matching impossibility thresholds. This is the only library cell whose "game" is against an
input-adversary rather than a strategic player — cite it to contrast guarantees, not to merge
models.

---

## 3. Information-structure axis (the third taxonomy dimension)

1. **Perfect state feedback** — the default of the geometric school: P022, P037, P099, P100,
   P103, P091, P050. Strategies are functions of all current positions; opponents' current
   controls unknown (P037, P099 explicitly note this).
2. **Non-anticipative / Elliott–Kalton (Stackelberg-flavored)** — P041 (PELIDR strategies),
   P040 (upper value), P100 (pursuers know evaders' current inputs — flagged in its archive as
   an asymmetry that may overstate capture capability). P103 deliberately *rejects* it for
   feedback, citing value nonexistence under feedback (Cardaliaguet) — a citable tension.
3. **Asymmetric / partial observation** — sensing radii and detection-triggered phases:
   P062 (deployment/capture phase split, value lower-bounded by complete-information value),
   P064 (conservative barrier evaluated from sensed geometry), P067 (fuzzy region =
   barrier-winning minus sensing set), P071 (engagement surface for sensing-limited intruders),
   P095 (obstacle + partial information), P090 (visibility networks + masking matrices),
   P017 (pre/post-detection two-phase with Apollonius terminal reward).
4. **Belief-based / subjective games** — P027 (virtual evader with chance-constrained inflated
   decision set), P029 (Bayesian level-k rationality inference over receding-horizon models).
5. **Adversarial input streams (non-strategic)** — the competitive thread P005–P009.

**[归纳] Rule:** information structure is the cheapest novelty axis — the library shows the
same barrier machinery re-derived under each of the five regimes above, each re-derivation being
a publishable delta (P067, P062, P064, P090).

---

## 4. How to position a new paper — decision procedure

**Step 1 — Fix the cell.** Locate your (problem class, player configuration, information
structure) triple in Sections 1 and 3. Player configurations use P044's taxonomy (1v1, Nv1,
1vM, NvM) plus two-team variants (NvM with coalitions). Record the cell's standard assumptions
from the representative papers.

**Step 2 — Name the 2–3 closest works.** Not the most famous — the closest. The archives show
T1 introductions always name the single closest work explicitly and state its two deficits
(P105 names its companion 1-vs-1 TAC paper; P100 names the square-domain 2D1A paper P099 and
the pairwise-outcome TAC paper; P050 names Fu & Liu's Automatica paper as closest and lists the
four missing proofs).

**Step 3 — Choose and state the delta type.** The library exhibits exactly four delta types:
- **New setting**: new geometry/dynamics/information for an existing solution pattern.
  Examples: P106 (obstacles enter RA winning regions); P013 (3-D + slower pursuers);
  P021 (general convex CTF regions); P091 (all speed ratios + nonzero radii); P053
  (heterogeneous dynamics in isochron geometry); P062/P064 (partial information with 3-D
  convex targets).
- **New guarantee**: same setting, stronger certification — barrier → value, sufficient →
  necessary-and-sufficient, feasibility → saddle-point, asserted → viscosity-proved.
  Examples: P050 (viscosity verification of geometric candidates; subsumes special cases);
  P031 (HJI justification of geometric solutions); P019 (first proved value in the
  1D-2A class; naive max-value counterexample); P037 (exact saddle-point Value vs. numerical
  HJB approximations); P009 (first randomized lower bounds).
- **New construction**: a new geometric/analytic object that unlocks the cell.
  Examples: P023 (Lyapunov containment on a single Apollonius circle); P105 (pursuit enclosure
  functions); P058 (flag-aware via-point potentials); P067 (fuzzy region); P018 (two-phase
  ellipse); P019 (m-branch viscosity lemma; singular-arc ODE).
- **New algorithm**: complexity, approximation, distribution, or implementation for the
  combinatorial layer. Examples: P103 (NP-hardness + 1/3-approximation); P054 (distributed
  min-makespan with finite-time optimality); P100 (0-1 IP with real-time barrier evaluation);
  P059 (LLM + analytic revision); P084 (k-WTA dynamical network).

**Step 4 — Assemble the citation set for the related-work section.** For any cell, include:
1. One survey anchor: P104 (reach-avoid/multiplayer), P044 (PE), or P115 (adversarial games
   broadly) — one sentence, once.
2. The founding/classic works of the problem class: Isaacs lineage via P044; CTF: P039/P040;
   TAD: P022; competitive perimeter: P005; lifeline: P102; hedonic allocation: P045.
3. The 2–4 immediately preceding works of your exact cell (the works your theorems modify),
   cited with contribution + setting + limitation.
4. One contrast citation per alternative method family (numerical HJI: P040; learning: P046 or
   P078; LLM/planning: P059; competitive: P008) to justify the chosen methodology.
5. If you use a tool (Apollonius circle, Voronoi, Danskin/Clarke, CBF, matching), cite its
   canonical library source: Apollonius containment P023; KKT–Isaacs bridge P103/P021;
   parametric-optimization verification P050; effective-set/dimension bound P021/P103;
   ESP/obstacle machinery P106.

**Step 5 — Calibrate the claim.** Mark every positioning statement as [authors' claim] or
[verified] against the cited archive (P050's "no restrictive assumptions" hides the
speed-superiority assumption — the archive flags it; P046's "model-free" abstract claim is
overstated because the input matrix is used). The Introduction may claim the delta; it may not
claim the absence of related work beyond what Step 2's search of this taxonomy supports.
