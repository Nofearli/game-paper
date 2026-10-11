# Archive template -- copy this file to PXXX.md and fill it for a new paper.

# PXXX: <Full Paper Title>

## 1. Bibliographic Info
- ID: PXXX / source file: `<filename>.pdf` / total pages: N
- Title / Authors (full list) / Year / Venue (exact name) / DOI (if printed)
- Tier: T1 | T2 | T3 (T1=IEEE Trans/Automatica/L-CSS, T2=top conf/strong journal, T3=other)
- BibTeX (ONLY from printed metadata; unknown field -> `note = {to verify}`):
  ```bibtex
  @article{<key>, author={...}, title={...}, journal={...}, volume={...}, year={...}}
  ```
- Topics: <5-10 keywords>

## 2. Research Background
<3-5 sentences: domain, application, practical need.>

## 3. Research Problem and Gap
<Problem studied; what prior work lacks. Mark [authors' claim] vs [verified from cited text].>

## 4. Core Contributions
1. **Theory**: ...
2. **Modeling**: ...
3. **Algorithm**: ...
4. **Experiment**: ...

## 5. Key Mathematical Results
<For EVERY theorem/lemma/proposition/corollary:>
- **Theorem N (p. X, eq. (N))**: precise statement ($LaTeX$); ALL assumptions; proof approach
  in 3-8 steps with tools named; decisive intermediate inequality/equation WITH eq. number;
  local/global, analytic/numerical; physical meaning; extensibility notes.
<Model: dynamics, information structure, cost, termination/winning conditions (eq. numbers).>
<No formal theorems -> say so and extract main analytic results.>
<Unclear step -> "proof gap: ..." with page/eq.>

## 6. Simulation and Experiments
| Parameter | Value | Unit | Source (page) |
|---|---|---|---|
| ... | ... | ... | ... |
<Any value not printed in the paper = UNREPORTED. Never guess.>
<Each figure/table: what it shows + which claim it validates. Baselines & fairness. Metrics.>

## 7. Limitations and Open Issues
<Author-stated + critical observations, with page/eq citations.>

## 8. Citation Value
<Paragraph role in a future IEEE Trans Introduction + ready-to-adapt 1-2 sentence
English citation sentence describing the contribution faithfully.>
