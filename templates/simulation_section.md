# Simulation / Experimental Results section skeleton

Use with `references/simulation_design.md` (theory→experiment mapping from
the library) and `references/visualization_guidelines.md` (figure styles).
`scripts/simulation_plotting.py` provides the IEEE rcParams.

## A. Setup (one paragraph + parameter table)
- Toolchain (Python/MATLAB), integrator + step size, termination.
- Table: parameter | symbol | value | unit (values AS chosen; do not claim
  they come from another paper unless they do).
- Monte-Carlo: number of runs, random seeds, initial-condition sampling rule.

## B. Scenario / validation matrix (one sub-subsection per experiment)
Each experiment = one row of the matrix:
| Experiment | Verifies | Setting | Metric | Figure |
- Theorem boundary verification: plot analytic boundary vs simulated capture
  set; report overlap/%.
- Typical trajectories: on/inside/outside the barrier — one case each.
- Parameter sensitivity: sweep the key ratio (e.g., $v_E/v_P \in [0.5,1]$),
  show metric vs parameter with theoretical transition points marked.
- Baseline comparison: same info, same dynamics; name the baseline papers.
- Ablation: remove one module at a time; quantify each module's contribution.
- Computational cost: wall-clock vs dimension/#players.

## C. Results and discussion (per figure)
- Report metric = value ± std over runs; state significance honestly.
- Tie every observation back to theory: "the plateau in Fig. 5 occurs exactly
  at $\alpha = 0.7$ predicted by Theorem 2".

## D. Physical experiments (if any)
Hardware platform, sensors, localization, communication, latency, trial count;
differences from simulation (unmodeled friction/delay) and how the method
coped.

## Honesty rules
- Distinguish: proven in theory / observed numerically / empirical statistic.
- No cherry-picked runs; report failures (evader escapes) and explain.
- UNREPORTED parameters in source papers must not be silently filled.
