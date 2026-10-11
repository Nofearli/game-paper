# Introduction Patterns — Paragraph-Level Architecture of T1 Game Papers

Cross-paper synthesis (labeled **[归纳]**) built from the Section 3 (problem/gap framing) and
Section 8 (citation value) records of the per-paper archives in `papers/PXXX.md`. Every pattern
below is traceable to named archives; before reusing any exemplar, open the cited `PXXX.md` and
verify the claim against its recorded pages/equations.

**Anti-plagiarism rule (binding, from `SKILL.md`):** never lift sentences from source papers.
The exemplars below record the *structural move* of each paragraph in paraphrase; when writing a
new Introduction, instantiate the move with fresh prose and real citations only from the archives.
Two absolute red lines apply: do not fabricate works, authors, theorems, or DOIs; and keep the
three registers separate — paper-stated facts (`[authors' claim]` with PXXX), cross-paper
synthesis (`[归纳]`), and new advice (`[建议]`).

---

## 1. The six-paragraph role template

T1 game papers (IEEE Trans and Automatica alike) overwhelmingly open with a single-column
Introduction of five to seven paragraphs performing the following roles. The skeleton mirrors
`templates/templates_overview.md` Section 1; this file supplies the evidence and the variants.

| Para | Role | Share of T1 game papers in this library |
|------|------|------------------------------------------|
| 1 | Context & application motivation | universal |
| 2..k | Related-work lines, grouped by method family or problem class | universal (2–4 paragraphs) |
| k+1 | Gap statement — the pivot | universal; usually 1 short paragraph or final 2–3 sentences of the last related-work paragraph |
| k+2 | "In this paper, we …" + numbered contributions | universal |
| k+3 (optional) | Organization paragraph | common in IEEE Trans; often omitted in Automatica |

### 1.1 Para 1 — Context hook (three opening moves)

**Move A: application-first.** Name a concrete adversarial application, then promote the game
class to the natural model.
- P050: opens from counter-UAS defense of protected airspace, then defines target-guarding games
  as the formal frame.
- P105: opens from multi-robot threats to safety-critical infrastructure (airports, military
  facilities), motivating Dubins-car pursuers guarding a convex region.
- P099: stacks four short application instances — robot-soccer interception, harbor/coastline
  defense, collision avoidance with multiple obstacles, military confrontation — before
  introducing the reach-avoid class.

**Move B: problem-class-first.** Lead with a one-sentence definition of the game class; give
applications second.
- P021: defines capture-the-flag as a two-target reach-avoid differential game, then lists
  motivating domains (UAV path planning, air traffic control, ship escort).
- P037: leads with the team-vs-team border-defense scenario and the commander's joint
  discrete-assignment/continuous-guidance burden.

**Move C: method-critique-first.** Lead with the standard solution machinery and its pain point;
the application arrives inside the gap paragraph.
- P053: opens from the HJI equation being "hard to solve and non-intuitive" for nonlinear
  dynamics, motivating an intuitive geometric replacement for a specific heterogeneous pairing.
- P104 (the review) legitimizes this move: its Section 2 taxonomy is the citable menu that
  justifies both Move A and Move C openings.

**[归纳] Rule:** the hook sentence must contain the player roles (pursuer/evader or
defender/attacker/target), the objective asymmetry, and at most one number; deeper model details
belong in Section II, never in Para 1.

### 1.2 Paras 2–k — Related-work lines

The library's dominant grouping is **by method family**, not chronology:

1. **HJI/computational line** — cite the exact-solution machinery, then its dimension wall.
   Standard evidence sentence: level-set HJI is complete but intractable beyond roughly five
   joint states (P105, P106, P021, P040 all record this limit; P103 quantifies a 12-state subgame
   at order 10^12 grid points).
2. **Geometric/analytic line** — Apollonius circles, Voronoi partitions, dominance regions,
   barriers (P099, P100, P103, P091, P050). One sentence per cited work: contribution + setting
   + citation.
3. **Assignment/matching line** — pairwise outcomes and maximum matching for multiplayer games
   (P100 contrasts its coalition-level barriers with the 1-vs-1 matching of Chen–Zhou–Tomlin;
   P059 recaps the NP-hard constrained matching).
4. **Learning line** — RL/ADP/LLM methods, strong empirically, weak on guarantees (P046, P059;
   P106 records "learning-based approaches: empirically strong, no guarantees").

Variant grouping — **by information structure** when information is the contribution: P064
orders its survey around complete-information analytical games, sensing-limited pursuit, and
geometric guarding with one-Apollonius-circle strategies; P090 orders around classical TAD
geometry, the LQ nonzero-sum tradition, and anomaly/visibility modeling.

**[归纳] Rule (echoed in templates_overview.md):** every related-work sentence = contribution +
setting + bracket. Never a bare list. The archives show T1 authors compress each prior work to
one clause with a named limitation that will be harvested by the gap sentence.

### 1.3 The gap paragraph — construction from the preceding lines

Gap sentences in this library are *always* built from the immediately preceding related-work
sentences: each prior sentence deposits one restriction, and the gap sentence negates the
conjunction. Four recurring gap types (names below are the library's own vocabulary):

**Assumption-gap** (a listed modeling restriction across all prior works):
- P050: prior geometric verifications needed closed-form value gradients, which forced few
  defenders, planar spaces, zero capture radii, circular or half-planar targets, and
  classical-only (C1) verification; the paper removes exactly that list.
- P091: the analytical barrier line assumed point capture and homogeneous/equal speeds; the
  paper covers heterogeneous radii and all three speed-ratio regimes.
- P100: prior multiplayer treatments construct barriers only for 1-vs-1 pairs, so cooperative
  capture is invisible to the matching stage and the resulting matching is suboptimal.

**Setting-gap** (a problem configuration never treated):
- P013: 3-D engagement and pursuers slower than the intruder are "two key issues that have not
  yet been effectively solved"; prior 3-D faster-evader works imposed escape-route or
  initial-configuration constraints.
- P053: the isochron method had not been applied to heterogeneous dynamics; the
  damped-double-integrator-vs-single-integrator game lacks a full solution.
- P021: prior CTF solutions cover only degenerate target shapes (point, strip, half-plane).
- P106: almost all reach-avoid results assume obstacle-free domains; winning regions with
  obstacles were missing, harder still for multiplayer.

**Guarantee-gap** (prior results construct candidates but do not certify them):
- P019: candidate value functions in the one-defender-two-attacker line lack rigorous
  sufficiency proofs; the naive max-of-branch values fails the viscosity condition on a set the
  paper exhibits.
- P037: prior multiplayer reach-avoid work approximates HJI numerically or with semi-open-loop
  strategies, and barrier-only analyses do not provide saddle-point strategies.
- P040: MPC/geometric defenses give no optimality or winning guarantee if the opponent deviates
  from the assumed behavior.

**Scalability/computational-gap** (exact tools cannot reach the required dimension or
decentralization):
- P054: allocation in multiplayer PE is centralized despite limited robot sensing/communication,
  and linear-sum assignment cost cannot express the makespan objective.
- P059: LLM planners hallucinate and lack differential-game knowledge; classical assignment
  algorithms violate the coalition conflict constraint.

**[归纳] Templates for the pivot sentence (paraphrased moves):**
1. Enumeration pivot — "These works either assume A, or restrict to B, or require C; none
   addresses X." (P050, P106 shape)
2. Closest-work pivot — "The most relevant work [ref] considers only … and does not …" (P105,
   P100 shape; name the closest work explicitly, then its two deficits)
3. Priority claim — "To the best of the authors' knowledge, this is the first …" (P059, P100,
   P053, P040 all record this phrase). Use once, only after the enumeration has earned it.
4. Contrast pivot — "In contrast to the above problems, in this paper we present …" (P077).

**Honesty calibration the archives enforce:** when the gap is argumentative rather than
theorem-backed, the strongest T1 papers scope it ("as far as the authors are aware", P053) and
the archive reviewer flags unqualified novelty claims. Never convert a plausible gap into an
impossibility claim.

### 1.4 The contributions paragraph

Universal formula: one sentence stating the studied problem, then "The main contributions of
this paper are summarized as follows." followed by enumerated items. Archive evidence:
- P017 records the verbatim convention "Our contributions are threefold" with exactly three
  items; P103 lists seven numbered items; P053 six; P054 and P106 five each; P050 four.
- **[归纳] Mapping rule:** each numbered contribution maps to exactly one main theorem, one
  algorithm, or one experiment (P050's contribution 1 is its Theorem 2; P103's items map to
  Lemmas 3.1–3.3, Theorems 3.1–4.2, Algorithms 1–2). Contributions naming "first formulation",
  "complete solution", "complexity analysis", and "experiments" in that order is the most common
  sequencing (P054, P103).
- Contribution verbs observed: *formulate / prove / derive / construct / design / show /
  demonstrate*. Avoid "study" inside a contribution item — it names no deliverable.

### 1.5 The organization paragraph

IEEE Trans convention recorded across the archives: "The remainder of this paper is organized as
follows. Section II … Section III … Finally, Section VI concludes the paper." One sentence per
section, no content claims. Frequently omitted in Automatica (P021, P103 record no organization
paragraph in their structures).

---

## 2. Sentence-level stylistic moves

- **Attribution verbs:** "derived", "solved", "constructed", "characterized", "proved … is the
  viscosity solution" (P050-style verification claims), "formulated … as" (P040). Reserve
  "proved" for certified results; use "showed/argued" for geometric reasoning (the archives
  distinguish these).
- **The "However" pivot:** always preceded by at least two affirmative related-work sentences in
  the same paragraph; the archive pattern is affirmative-affirmative-However.
- **Quantifier placement in claims:** "guarantees capture in finite time **against any admissible
  evader strategy**" (P023's containment guarantee, P106's winning definition) — the adversarial
  quantifier must appear inside the claim sentence, not in a following remark. P097 and P105
  record the same discipline for coalition winning conditions.
- **Numbers in the introduction:** T1 papers quote exactly two kinds of numbers — dimension
  limits of competitors (the ~5-state HJI practical limit, P105/P106) and headline guarantees
  ("at most three pursuers are necessary in 3-D", P103; "at most two pursuers suffice", P100,
  P105, P021). These double as the paper's memorable identity.
- **Forward references:** the last contribution item typically previews the validation ("validated
  in simulations on …", P059's Monte-Carlo + hardware sentence), never the conclusion.
- **Transitions between related-work lines:** the library's T1 papers hand off between method
  families with contrast clauses rather than new topics — "When the analytic assumption does not
  hold, …" (the templates' own formula), "In parallel, …" (P021 moving from HJI-CTF to the
  optimization-based line), "Two realism gaps motivate the work: (i) … (ii) …" (P090 converting
  its survey directly into its gap). Each transition names the *condition* under which the next
  family is needed; a related-work section that merely changes subject between paragraphs
  forfeits the gap construction.
- **Self-positioning move:** journal extensions and line-capstone papers state their relation to
  their own predecessors explicitly inside the related-work block, not only in the gap — P022
  records that the paper positions itself as the rigorous journal treatment of a reduced-state
  conference result and enumerates the new results w.r.t. it; P105 names its companion 1-vs-1
  TAC paper as the directly extended work. The pattern: one sentence per own precursor =
  what it did + what was missing, feeding the same gap sentence.

### 2.1 Anti-patterns the archives document

- **Undifferentiated citation strings.** Sentences of the form "[12]–[18] studied pursuit
  games" appear nowhere in the T1 records; the closest any archive shows is a grouped sentence
  that still assigns each cluster a distinct property (P099 groups its alternatives as
  "numerical, conservative for the defenders, or preformed one by one without cooperation" —
  three adjectives that become three gap clauses).
- **Gap stated before its evidence.** No archive records a gap paragraph that precedes all
  related-work paragraphs; P046's gap ("existing PE strategies do not handle safety … and CBF-QP
  methods are inapplicable under unknown dynamics") arrives only after both threads are
  surveyed, and its second half is honestly marked as a plausibility argument rather than a
  proven impossibility.
- **Contribution lists without deliverables.** Items phrased as "we study X" or "we consider Y"
  are the defect the mapping rule exists to prevent; every attested contribution item names a
  theorem, a construction, an algorithm with a guarantee, or an experiment.
- **Numbers without provenance.** The dimension-wall numbers that open so many gap paragraphs
  (the ~5-state HJI practical limit; P103's 10^12 grid-point estimate) are always attributed to
  a citable source or computed in the paper — an unattributed "curse of dimensionality" is
  treated by the archives as a reviewer target.
- **Application padding.** Para 1 in the T1 records runs three to five sentences; extended
  application surveys (sensor types, platform histories) belong in Section II or a dedicated
  motivation subsection, as in P040, which defers testbed detail to its experimental section.

### 2.2 Paragraph-count calibration

The archives show a stable budget: Introduction ≈ 1–1.5 columns (IEEE Trans) or ≈ 1 page
(Automatica). Five-to-seven paragraphs total; the gap paragraph is the shortest (2–4 sentences);
the contribution paragraph is the longest. When a paper needs both a method-family survey and an
information-structure survey (P064's three-thread layout), the Introduction may reach eight
paragraphs, but the excess is spent on related work, never on context — context stays at one
paragraph in every recorded case.

---

## 3. Filled EXAMPLE skeleton — multiplayer reach-avoid game with limited sensing

**This is a worked example for training, not a real paper.** All bracketed citations are real
archives in `papers/`; the prose is freshly written here (no source sentences reused). Scenario:
N pursuers with bounded sensing radii defend a convex target region against evaders in 3-D.

> **[Para 1 — context]** Autonomous vehicles protecting airspace, maritime infrastructure, and
> restricted zones increasingly face intruders whose behavior is adversarial rather than
> stochastic, a setting for which reach-avoid differential games — pursuers must capture evaders
> before they enter a protected set — provide worst-case guarantees [P104], [P115].
>
> **[Para 2 — analytic line]** For complete-information games with simple motion, an extensive
> geometric literature delivers closed-form winning regions: analytical barriers for
> two-defender-one-attacker line defense [P099], coalition barriers and 0-1 task assignment in
> convex domains [P100], matching-based 3-D solutions with heterogeneous capture radii [P103],
> and barrier families covering all speed-ratio regimes with nonzero radii [P091]. Verification
> machinery has matured in parallel: the geometric candidate value for multiple-defender
> target guarding is now certified as the viscosity solution of the associated HJI equation via
> parametric optimization [P050], with earlier justifications covering convex targets [P031].
>
> **[Para 3 — information-limited line]** When players cannot observe the whole state, the
> geometry must be re-derived: partial-information target defense introduces deployment and
> engagement phases with sensing-triggered transitions [P062], [P067], uncertain-observation
> pursuit makes Apollonius-type safe regions robust to measurement noise [P028] and couples
> Kalman-filtered beliefs with coalition formation [P027], and multi-agent games with limited
> perception require visibility-network modeling [P090].
>
> **[Para 4 — gap]** However, the analytical barrier machinery of [P100], [P103], [P091] assumes
> full-state feedback by every player; the sensing-limited treatments of [P062], [P067] either
> restrict to a single defender or a straight target line; and none of the partial-information
> works provides a coalition-level winning characterization for a 3-D convex target, leaving the
> combination of closed-form barriers and finite sensing radii unresolved. [P064] reaches the
> same frontier from the multiplayer side but stops at speed-ratio-threshold capture strategies
> rather than coalition barriers.
>
> **[Para 5 — contributions]** In this paper, we study a multiplayer reach-avoid game in 3-D in
> which each pursuer observes opponents only within a finite sensing radius. The main
> contributions are summarized as follows. (i) We formulate the game with an asymmetric
> information structure and prove a sensing-radius threshold (in the spirit of the conservative
> barrier of [P064] and the sensing threshold of [P054]) under which local information suffices
> for coalition-level decisions. (ii) We construct closed-form coalition winning regions for
> convex 3-D targets, extending the two-pursuer-sufficiency principle established in 2-D [P100],
> [P105] and 3-D [P103]. (iii) We design a receding-horizon assignment with a nondecreasing
> guaranteed-capture count, following the monotone-bound pattern of [P106], and validate the
> framework in Monte-Carlo simulations and hardware experiments.
>
> **[Para 6 — organization]** The remainder of this paper is organized as follows. Section II
> formulates the game. Sections III and IV develop the sensing threshold and the coalition
> barriers. Section V presents the assignment strategy, Section VI the simulations, and
> Section VII concludes the paper.

Paragraph-role audit of the example: Para 2 cites four same-line works each with contribution +
setting; Para 4's gap sentence enumerates exactly the restrictions deposited by Paras 2–3
(assumption-gap: full-state feedback; setting-gap: single defender / straight line; guarantee-gap:
no coalition-level characterization under partial information) — the construction rule of
Section 1.3 in action. Contribution item (ii) is a *new-construction* delta, item (i) a
*new-setting* delta, item (iii) a *new-algorithm* delta, matching the delta taxonomy of
`related_work_taxonomy.md` Section "How to position a new paper".
