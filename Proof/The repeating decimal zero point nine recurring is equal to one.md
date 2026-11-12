# A Rigorous Proof: $0.\overline{9}=1$
## Preliminaries and Definitions
Let $\mathbb R$ denote the set of real numbers constructed as equivalence classes of Cauchy sequences of rational numbers, equipped with the usual Euclidean metric 

$d(x,y)=|x-y|$
.

An infinite decimal expansion $0.a_1a_2a_3\cdots$ is defined as the limit of its sequence of finite truncations:

$$
0.a_1a_2a_3\cdots:=\lim_{n\to\infty}\sum_{k=1}^n \frac{a_k}{10^k},\quad a_k\in\{0,1,\dots,9\}.
$$

The repeating decimal $0.\overline{9}$ is by definition

$$
0.\overline{9}:=\lim_{n\to\infty} s_n,\qquad s_n=\sum_{k=1}^n \frac{9}{10^k}.
$$

The sequence $\{s_n\}_{n\in\mathbb N}$ is a sequence of rational numbers. We first verify that $\{s_n\}$ is a Cauchy sequence, hence converges in $\mathbb R$ by the completeness axiom of real numbers.

Take arbitrary $\varepsilon>0$. Choose $N\in\mathbb N$ such that $10^{-N}<\varepsilon$. For all integers $m>n>N$:

$$
|s_m-s_n|=\left|\sum_{k=n+1}^m \frac{9}{10^k}\right|
=9\cdot \frac{10^{-(n+1)}-10^{-(m+1)}}{1-1/10}
=10^{-n}-10^{-m}<10^{-n}<\varepsilon.
$$

Thus $\{s_n\}$ is Cauchy, so $\lim\limits_{n\to\infty}s_n$ exists in $\mathbb R$.

## Proof 1: Evaluation via Infinite Series
We have

$$
0.\overline{9}=\sum_{k=1}^{\infty}\frac{9}{10^k}.
$$

This is a geometric series of the form $\sum_{k=1}^{\infty} ar^{k-1}$ with

$$
a=\frac{9}{10},\qquad r=\frac{1}{10},\qquad |r|=\frac1{10}<1.
$$

A standard result in calculus: if $|r|<1$, then

$$
\sum_{k=1}^{\infty} ar^{k-1}=\frac{a}{1-r}.
$$

Rewrite:

$$
\sum_{k=1}^{\infty}\frac{9}{10^k}
=\sum_{k=1}^{\infty}\frac{9}{10}\cdot\left(\frac{1}{10}\right)^{k-1}.
$$

Substitute $a=\frac{9}{10}, r=\frac1{10}$:

$$
\sum_{k=1}^{\infty}\frac{9}{10}\cdot\left(\frac{1}{10}\right)^{k-1}
=\frac{\frac{9}{10}}{1-\frac{1}{10}}
=\frac{\frac{9}{10}}{\frac{9}{10}}
=1.
$$

Therefore

$$
0.\overline{9}=1.
$$

## Proof 2: Direct Limit of Partial Sums
We solve the finite partial sum explicitly:

$$
s_n=\sum_{k=1}^n\frac{9}{10^k}
=\frac{9}{10}\cdot \frac{1-\left(\frac1{10}\right)^n}{1-\frac1{10}}
=1-\frac{1}{10^n}.
$$

By definition:

$$
0.\overline{9}=\lim_{n\to\infty}\left(1-\frac{1}{10^n}\right).
$$

We prove $\lim\limits_{n\to\infty}\dfrac{1}{10^n}=0$ by the $\varepsilon$–$N$ definition of limit.

Given any $\varepsilon>0$, pick $N\in\mathbb N$ satisfying $10^{-N}<\varepsilon$. For all $n>N$:

$$
\left|\frac{1}{10^n}-0\right|=\frac{1}{10^n}<\frac{1}{10^N}<\varepsilon.
$$

Hence $\displaystyle\lim_{n\to\infty}\frac{1}{10^n}=0$. By linearity of limits:

$$
\lim_{n\to\infty}\left(1-\frac{1}{10^n}\right)
=\lim_{n\to\infty}1-\lim_{n\to\infty}\frac{1}{10^n}
=1-0=1.
$$

We conclude

$$
0.\overline{9}=1.
$$

## Proof 3: Order Argument (Dedekind Cut / Density Form)
Suppose, for contradiction, that $0.\overline{9}<1$. By the density of $\mathbb Q$ in $\mathbb R$, there exists some rational number $q$ such that
$$
0.\overline{9}<q<1.
$$
Write $q$ in decimal form $q=0.q_1q_2q_3\cdots$. Since $q<1$, its decimal expansion is bounded above by $0.999\cdots$. If $q>0.\overline{9}$, then there exists an index $m$ such that for all $k<m$, $q_k=9$ and $q_m>9$, which is impossible because every decimal digit satisfies $0\le q_k\le 9$. Therefore no such $q$ exists.

For real numbers, if $a\le b$ and there is no real strictly between $a$ and $b$, then $a=b$. Since $0.\overline{9}\le 1$ and there is no real $y$ with $0.\overline{9}<y<1$, we obtain

$$
0.\overline{9}=1.
$$

## Heuristic Algebraic Argument (Not Foundationally Rigorous)
The popular $10x-x=9$ argument is intuitive but assumes without justification that we may multiply and subtract infinite decimal expansions termwise, which is not an axiom; it is a consequence of limit properties we proved above.
Let $x=0.\overline{9}$. If we formally manipulate:

$$
x=0.999\cdots,\qquad 10x=9.999\cdots,
$$

$$
10x-x=9 \implies 9x=9 \implies x=1.
$$

This is a useful illustration, but it depends on the prior convergence and linearity results established above.

## Remark
Within the standard real number system, $0.\overline{9}$ and $1$ are two distinct decimal representations of the same real number. Uniqueness of decimal expansions fails precisely for numbers that are finite dyadic/decimal rationals; they admit one terminating expansion and one expansion ending in an infinite string of nines. This is a feature of the decimal representation, not a contradiction in the real numbers.
