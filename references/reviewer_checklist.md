# Reviewer Checklist — Internal IEEE Trans Review System

Use in **Mode F** (审稿检查) and at the end of **Mode G** (全文协同).
For each item: verdict PASS / CONCERN / FAIL + page/section reference + fix
suggestion. Report format at the bottom. Severity: Critical (blocks
submission), Major (weakens the paper), Minor (polish).

## A. Theory
1. **Novelty vs closest prior work** — list the 1-2 closest papers from the
   library (PXXX), state precisely what is new: new problem/information
   structure, new barrier/winning-region characterization, new proof, new
   strategy, or mere parameter change? A paper whose only delta is a
   different simulation cannot pass.
2. **Model self-consistency** — dynamics, information structure, payoff and
   termination conditions mutually consistent? Control sets nonempty and
   compact where needed? Units consistent?
3. **Assumptions explicit & reasonable** — every assumption numbered (A1…),
   used where claimed, never silently strengthened mid-proof. Flag any
   assumption that is only stated and never used (or vice versa).
4. **Proof completeness** — every theorem has a proof (or a clear pointer);
   no logical jumps; necessary vs sufficient conditions not mixed; boundary
   cases handled; inverse/optimality arguments state the class of admissible
   strategies. A "proof" that only shows simulations is a Critical failure.
5. **Strategy–theory consistency** — the implemented/illustrated strategy is
   exactly the proven one; constants in the algorithm match constants in the
   theorem; feedback vs open-loop class stated once and respected.
6. **Claims within scope** — conclusions never exceed what is proven/shown;
   scope limits (sensing, obstacles, dimension) stated in the introduction
   are respected in the results and conclusion.

## B. Simulation / Experiments
7. **Validates the core contribution** — every main theorem has at least one
   experiment explicitly designed to verify it (boundary plot, trajectory on
   the barrier, win-region overlap), not just generic success rates.
8. **Fair baselines** — baselines from the library chosen because they solve
   the same problem class; same information, same dynamics, same discretization.
   Flag any strawman comparison.
9. **Statistical sufficiency** — number of runs, variance/std reported,
   seeds stated; single-run screenshots never used as aggregate claims.
10. **Parameters real & traceable** — parameter table values match the text;
    nothing "borrowed" without citation.

## C. Presentation
11. **Figures–equations consistency** — symbols in figures match symbols in
    the text; figure captions self-contained; barriers/regions drawn with
    geometrically correct proportions (verify constants, not aesthetics).
12. **References real & relevant** — every \cite resolves in the library
    (run `scripts/citation_checker.py draft.tex`); no citation exists only in
    the bibliography; bibliography format follows IEEEtran.
13. **Language & notation** — IEEE Transactions register (present tense for
    general truths, past for what the authors did); vectors bold upright,
    scalars italic, \|·\|_2; symbols defined at first use
    (run `scripts/notation_checker.py paper.tex`).
14. **Abstract/Intro/Conclusion alignment** — same contributions claimed in
    all three; numbers identical; conclusion adds no new claims.

## Report template

```
# Internal Review Report — <draft title> (<date>)
Verdict: accept-after-minor / major-revision / reject-resubmit

## Critical
- [C1] <issue> — <location (section/eq/page)> — <why> — <fix>
## Major
- [M1] ...
## Minor
- [m1] ...
## Missing comparisons (from library)
- closest works not discussed/cited: PXXX, PXXX
## Notation & citation tool output
- notation_checker: N issues; citation_checker: N unresolved
```
