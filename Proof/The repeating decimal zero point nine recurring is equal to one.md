# A Rigorous Proof of the Identity $0.\overline{9} = 1$

## Notation
The symbol $0.\overline{9}$ is defined as the infinite decimal expansion
\[
0.\overline{9} := \lim_{n\to\infty} \sum_{k=1}^{n} \frac{9}{10^{k}}.
\]
This limit is well-defined within the standard real number system $\mathbb{R}$ equipped with the usual metric topology.

## Proof 1: Infinite Geometric Series
Consider the series representation:
\[
0.\overline{9} = \sum_{k=1}^{\infty} \frac{9}{10^{k}}.
\]
This is an infinite geometric series with first term $a = \dfrac{9}{10}$ and common ratio $r = \dfrac{1}{10}$. Since $|r| < 1$, the series converges, and the sum formula for convergent geometric series applies:
\[
\sum_{k=1}^{\infty} a r^{k-1} = \frac{a}{1-r}.
\]
Rewriting our summation to match the canonical form:
\[
\sum_{k=1}^{\infty} \frac{9}{10^{k}}
= \sum_{k=1}^{\infty} \frac{9}{10}\left(\frac{1}{10}\right)^{k-1}.
\]
Substitute $a = \dfrac{9}{10},\ r = \dfrac{1}{10}$:
\[
\sum_{k=1}^{\infty} \frac{9}{10}\left(\frac{1}{10}\right)^{k-1}
= \frac{\dfrac{9}{10}}{1 - \dfrac{1}{10}}
= \frac{\dfrac{9}{10}}{\dfrac{9}{10}}
= 1.
\]
Hence
\[
0.\overline{9} = 1.
\]

## Proof 2: Limit of Finite Truncations
By definition of infinite decimal expansion:
\[
0.\overline{9} = \lim_{n\to\infty} \left( 1 - \frac{1}{10^{n}} \right).
\]
From the standard limit result $\displaystyle\lim_{n\to\infty} \frac{1}{10^{n}} = 0$, we apply the linearity of limits:
\[
\lim_{n\to\infty} \left( 1 - \frac{1}{10^{n}} \right)
= \lim_{n\to\infty} 1 - \lim_{n\to\infty} \frac{1}{10^{n}}
= 1 - 0 = 1.
\]
Therefore
\[
0.\overline{9} = 1.
\]

## Proof 3: Algebraic Derivation (Auxiliary, Elementary)
Let $x = 0.\overline{9}$. Then
\[
x = 0.999\cdots.
\]
Multiply both sides by $10$:
\[
10x = 9.999\cdots.
\]
Subtract the original equality:
\[
10x - x = 9.999\cdots - 0.999\cdots.
\]
\[
9x = 9 \implies x = 1.
\]
This argument is heuristic and relies on consistency of infinite decimal manipulation; it is not taken as the foundational rigorous proof in real analysis.

## Remark
Within the axiomatic framework of $\mathbb{R}$, $0.\overline{9}$ and $1$ are **two distinct decimal representations of the same real number**. There does not exist any real number $y$ satisfying $0.\overline{9} < y < 1$. The apparent paradox arises from the intuitive but mistaken assumption that every real number possesses a unique decimal expansion.
