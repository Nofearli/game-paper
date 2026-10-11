# Conclusion skeleton (IEEE Trans)

5-7 sentences, three movements. Forbidden: copying the Abstract; new claims;
unproven generalizations.

## 1. What was studied (1 sentence)
"This article studied <exact problem class> <with key features: information
structure / environment / dynamics>."

## 2. What was established (2-3 sentences)
- Theory: which regions/strategies were characterized (name Theorems), under
  which assumptions.
- Algorithm + validation: headline number (success rate / capture time /
  runtime) from the experiments.

## 3. Scope and future work (2-3 sentences)
- One scope limitation stated honestly (e.g., planar kinematics, perfect
  sensing).
- 2-3 future extensions that directly address the limitations — tied to the
  library's open issues (see archives' Section 7), not vague new topics.

## Example
```
This article studied multiplayer reach-avoid games with limited sensing in
cluttered environments. We constructed the analytic barrier $\mathcal{B}$
(Theorem 1), proved saddle-point equilibrium of the proposed feedback
strategies (Theorem 2), and developed a distributed assignment algorithm with
guaranteed convergence (Theorem 3). Monte-Carlo simulations over 500 runs
show a 96.2\% capture success rate, and hardware experiments on two UAVs
validate the strategy under sensing delays. The analysis assumes unit-speed
simple motion; extensions to second-order dynamics and probabilistic target
motion are natural next steps.
```
