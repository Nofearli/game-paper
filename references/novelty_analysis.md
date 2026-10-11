# Novelty Analysis Workflow (`novelty_analysis`)

Use in **Mode B/C** when the user proposes a new research idea, and as item 1
of `reviewer_checklist.md`. Never accept a claimed novelty at face value —
compare against the library first.

## Step 1 — Locate the neighborhood
From the idea, extract: problem class (pursuit-evasion / reach-avoid /
target-defense / perimeter-defense / capture-the-flag / reconnaissance /
lifeline / active defense), player multiplicity (1v1, Nv1, 1vN, NvN),
information structure (perfect / partial / asymmetric / limited sensing),
dynamics (simple motion / double integrator / unicycle / USV / UAV / spacecraft),
environment (free space / obstacles / regions), solution approach (geometric /
HJI / PMP / learning).
Search `papers/index.md` + `references/literature_index.md` for the 5–10
closest papers. Read their archives' Sections 3–5 (problem, contributions,
mathematical results).

## Step 2 — Delta table
| Dimension | Closest work (PXXX) | Proposed idea | Delta |
|---|---|---|---|
| problem/players | | | |
| information structure | | | |
| dynamics/environment | | | |
| main result type | | | |
| proof technique | | | |
| experiments | | | |

## Step 3 — Classify the contribution
Pick the strongest applicable class (higher = stronger):
1. new problem or new information structure
2. new mathematical model (dynamics/environment class)
3. new analytic barrier / winning region (closed form where prior was numerical)
4. new theorem + proof (state what is proven that was not)
5. new optimal strategy (state optimality class: saddle-point / Nash / ε-)
6. new control/learning algorithm with guarantees
7. new experimental validation or application platform
8. nontrivial extension of existing theory to new conditions (must list which
   proof steps break and how they are repaired)
9. parameter/setting change only — **not a contribution**

Distinguish **theoretical** vs **engineering** vs **experimental** contribution.
An honest report may conclude "the delta is mostly class 8/9" — say so.

## Step 4 — Feasibility of the proof chain
For the claimed result, list which existing tools (from
`game_theory_foundations.md` / `theorem_proof_patterns.md`) apply directly,
which need modification, and which proof steps of the closest paper break
under the new conditions (e.g., Apollonius construction needs equal-speed
line-of-sight geometry; HJI scales badly beyond 2 players; barrier
construction assumes no obstacles). State what a referee would attack first.

## Step 5 — Output report
```
# Novelty Analysis — <idea one-liner> (<date>)
Closest works: PXXX, PXXX, PXXX
Delta summary: <2-3 sentences>
Contribution class: <1-9>, theoretical/engineering/experimental
Evidence chain: 已有理论 → 当前局限 → 拟解决问题 → 理论突破 → 实验验证 → 论文贡献
Referee's first attack: <what to strengthen before writing>
Verdict: novel enough for T1 / suitable for T2 / needs repositioning
```
Rules: mark every statement about prior work with its PXXX and page; if the
library lacks coverage of a relevant line of work, write "library gap" — do
not guess that nothing exists outside the library.
