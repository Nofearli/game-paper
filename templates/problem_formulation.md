# Problem Formulation — IEEE Trans skeleton

Use with `references/problem_formulation.md` (per-problem-class modeling
archives from the library) and `references/latex_notation.md` (symbol
contract). Order and numbering below follow the dominant T1 convention.

## A. Verbal scenario (1 short paragraph)
Players, arena, regions, sensing, obstacles — in words before any symbol.

## B. Notation and players
$\mathbf{x}_i \in \mathbb{R}^n$ state, $\mathbf{u}_i \in \mathcal{U}_i$ control,
player sets $\mathcal{P}, \mathcal{E}, \mathcal{D}, \mathcal{A}$.

## C. Dynamics
$\dot{\mathbf{x}}_i = f_i(\mathbf{x}_i, \mathbf{u}_i)$, e.g. simple motion
$\dot{\mathbf{x}}_i = \mathbf{u}_i$, $\|\mathbf{u}_i\|_2 \le v_i$; or double
integrator; state assumptions on $f_i$ (Lipschitz, etc.).

## D. Definitions
Definition 1 (capture): $\exists t$ s.t. $\|\mathbf{x}_P - \mathbf{x}_E\|_2 \le r_c$.
Definition 2 (outcome/win region): sets with precise membership.

## E. Assumptions (numbered, each used later by number)
A1 speed ratio; A2 information structure (who measures what, when);
A3 region shape/obstacles; A4 admissible strategy class (feedback
$\phi_i:\mathcal{X}\to\mathcal{U}_i$ vs open-loop).

## F. Payoff / objective
$J = \int_0^{t_f} L\,dt$ or terminal payoff; zero-sum vs nonzero-sum stated.

## G. Problem statement
"Problem 1: characterize the barrier $\mathcal{B}$ / find $\phi_P^*$ such that
...". Ends the section; Main Results section answers it by number.

## Checklist before leaving the section
- [ ] every symbol defined at first use (notation_checker clean)
- [ ] every assumption is used somewhere later
- [ ] termination and winning conditions are mathematically precise
- [ ] information structure stated (what each player knows)
