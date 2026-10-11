# Introduction — IEEE Trans skeleton (instantiation guide)

Use with `references/introduction_patterns.md` (patterns extracted from the
library) and `references/related_work_taxonomy.md` (how to group citations).
Every [PXXX] must exist in `papers/` — verify with `scripts/citation_checker.py`.

## Para 1 — Context and application (2-4 sentences)
- Domain + why adversarial interaction arises + why game theory is the right
  language. Name the game class in the first or second sentence.

## Para 2 — Related work, line A: analytic/geometric (grouped, 3-8 citations)
- One sentence per work: <Authors> [PXXX] studied <setting> and derived
  <result>. Order: foundational → closest variants. Group by problem class,
  NOT by year.
- Transition sentence acknowledging the line's shared assumption.

## Para 3 — Related work, line B: computational/learning (3-6 citations)
- HJI/numerical line: scalability limits [PXXX].
- Learning line: what works, what guarantees are missing [PXXX].

## Para 4 — Research gap (1-3 sentences, the only place it is stated)
- "However, ..." supported by the specific sentences above. Quantify the gap
  (dimension, information structure, environment feature).

## Para 5 — Contributions ("In this paper, we ...")
- 1 sentence problem statement + numbered contributions:
  (i) theory → maps to Theorem 1-2; (ii) algorithm → Algorithm 1;
  (iii) validation → simulation/physics. Each number = one deliverable.

## Para 6 — Paper organization (1-2 sentences, optional in some journals)

## Style checkpoints
- Tense: present for general truths, past/present perfect for what authors did.
- No "obviously/trivially"; no citation-dump lists; every cited work gets its
  contribution stated.
- The gap sentence must be entailed by Para 2-3.
