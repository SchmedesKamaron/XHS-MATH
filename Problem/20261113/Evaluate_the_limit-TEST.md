

### 题目1
Evaluate the limit:

$$
\lim_{n\to\infty} \left( \frac{\left(1+\dfrac1n\right)^{n+\frac12}}{e} \right)^n
$$

***

### 解
这是幂指型极限，采用取对数。记

$$
L=\lim_{n\to\infty} \left( \frac{\left(1+\dfrac1n\right)^{n+\frac12}}{e} \right)^n
$$

两边取自然对数：

$$
\ln L
=\lim_{n\to\infty} n\left[ \left(n+\frac12\right)\ln\left(1+\frac1n\right)-1 \right]
$$

令 $t=\dfrac1n$，则当 $n\to\infty$ 时 $t\to 0^+$ ，代入：

$$
\ln L
=\lim_{t\to 0^+} \frac{1}{t}\left[ \left(\frac1t+\frac12\right)\ln(1+t)-1 \right]
=\lim_{t\to 0^+}\frac{(2+t)\ln(1+t)-2t}{2t^2}
$$

使用泰勒展开，$t\to 0$ ：

$$
\ln(1+t)=t-\frac{t^2}{2}+\frac{t^3}{3}+o(t^3)
$$

代入分子：

$$
\begin{aligned}
(2+t)\ln(1+t)-2t
&=(2+t)\left(t-\frac{t^2}{2}+\frac{t^3}{3}+o(t^3)\right)-2t \\
&=2\left(t-\frac{t^2}{2}+\frac{t^3}{3}\right)+t\left(t-\frac{t^2}{2}\right)-2t+o(t^3) \\
&=2t - t^2 + \frac{2}{3}t^3 + t^2 -\frac12 t^3 -2t +o(t^3) \\
&=\left(\frac23-\frac12\right)t^3 + o(t^3) \\
&=\frac16 t^3 + o(t^3)
\end{aligned}
$$

于是

$$
\ln L
=\lim_{t\to 0^+}\frac{\dfrac16 t^3 + o(t^3)}{2t^2}
=\lim_{t\to 0^+}\frac{t}{12}=0
$$

所以

$$
\ln L = 0 \implies L = e^{0}=1
$$

结论：

$$
\boldsymbol{\lim_{n\to\infty} \left( \frac{\left(1+\dfrac1n\right)^{n+\frac12}}{e} \right)^n = 1}
$$

***

### 题目2
Evaluate the limit:

$$
\lim_{x\to 0}\frac{\tan(\sin x)-\sin(\tan x)}{x^7}
$$
