# Theorem / Lemma / Proof skeleton (LaTeX)

Preamble packages: \usepackage{amsmath,amssymb,amsthm}
\newtheorem{theorem}{Theorem} \newtheorem{lemma}{Lemma}
\newtheorem{proposition}{Proposition} \newtheorem{corollary}{Corollary}
\newtheorem{remark}{Remark} \newtheorem{definition}{Definition}
\renewcommand{\proofname}{\it Proof}

## Ordering convention in T1 game papers
Definitions → Lemmas (auxiliary geometry/inequalities) → Theorem (main
result) → Corollaries (special cases) → Remarks (interpretation & scope).

```latex
\begin{definition}[Capture time]\label{def:capture}
$\ldots$
\end{definition}

\begin{lemma}[Dominance boundary]\label{lem:boundary}
\emph{(All hypotheses restated here explicitly, citing assumptions A1--A3.)}
Let $\alpha = v_E/v_P \le 1$ and $\mathbf{x}_P(0), \mathbf{x}_E(0)$ satisfy
$\ldots$. Then the boundary of the dominance region $\mathcal{R}_P$ is the
Apollonius circle $\mathcal{C}_{PE}$ with center $c$ and radius $r$ given by
\begin{equation}\label{eq:apollonius}
c = \frac{\mathbf{x}_P - \alpha^2 \mathbf{x}_E}{1-\alpha^2}, \qquad
r = \frac{\alpha \|\mathbf{x}_P - \mathbf{x}_E\|_2}{1-\alpha^2}.
\end{equation}
\end{lemma}

\begin{proof}
Step 1 (candidate boundary): from the equal-time condition
$\|\mathbf{x}-\mathbf{x}_P\|_2/v_P = \|\mathbf{x}-\mathbf{x}_E\|_2/v_E$ and (4),
$\ldots$
Step 2 (algebraic characterization): squaring both sides and rearranging
yields $\|\mathbf{x}-c\|_2^2 = r^2$ with (5), $\ldots$
Step 3 (converse): if $\mathbf{x} \notin \mathcal{C}_{PE}$, then by (6) the
opposite dominance holds, hence $\ldots$
\end{proof}

\begin{theorem}[Main result]\label{thm:main}
$\ldots$
\end{theorem}
\begin{proof}
The proof relies on Lemma \ref{lem:boundary} and proceeds in three phases:
$\ldots$ (cite every intermediate inequality by its equation number)
\end{proof}

\begin{remark}
Theorem \ref{thm:main} extends the planar result of [PXXX] to $\ldots$; it
requires A1 and fails when $\alpha > 1$, in which case $\ldots$
\end{remark}
```

## Rigor rules
1. Every hypothesis used must appear in the statement; no "clearly/obviously".
2. Necessary vs sufficient directions labeled explicitly.
3. Each proof step's justification = named tool or numbered equation.
4. Boundary/degenerate cases addressed (e.g., $\alpha = 1$, collinear initial
   states, $r_c = 0$).
5. Simulations illustrate but never replace proofs.
6. Long proofs → main text + Appendix; state "The proof is given in the
   Appendix" and keep the decomposition there.
