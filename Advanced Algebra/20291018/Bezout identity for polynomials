# 求多项式 $u(x),v(x)$，使得 $u(x)f(x)+v(x)g(x)=(f(x),g(x))$

## 1）$f(x)=x^4+2x^3-x^2-4x-2,\ g(x)=x^4+x^3-x^2-2x-2$
**解：**
对多项式使用辗转相除法：
$$
\begin{align*}
f(x)&=1\cdot g(x)+(x^3-2x) \quad &r_1(x)=x^3-2x\\
g(x)&=(x+1)r_1(x)+(x^2-2) \quad &r_2(x)=x^2-2\\
r_1(x)&=x\cdot r_2(x)+0
\end{align*}
$$
最后的非零余式为 $r_2(x)=x^2-2$，所以最大公因式：
$$(f(x),g(x))=x^2-2$$

回代：
$$
\begin{align*}
x^2-2 &= g(x)-(x+1)r_1(x) \\
&= g(x)-(x+1)\big[f(x)-g(x)\big] \\
&= -(x+1)f(x)+(x+2)g(x)
\end{align*}
$$

得到：
$$\boldsymbol{u(x)=-x-1,\quad v(x)=x+2}$$

---

## 2）$f(x)=4x^4-2x^3-16x^2+5x+9,\ g(x)=2x^3-x^2-5x+4$
**解：**
辗转相除：
$$
\begin{align*}
f(x)&=2x\cdot g(x)+(-6x^2-3x+9) \quad &r_1(x)=-6x^2-3x+9\\
g(x)&=\left(-\frac13x+\frac13\right)r_1(x)+(-x+1) \quad &r_2(x)=-x+1\\
r_1(x)&=(6x+9)r_2(x)+0
\end{align*}
$$
首一最大公因式：
$$(f(x),g(x))=x-1$$

回代：
$$
\begin{align*}
-x+1 &= g(x)-\left(-\frac13x+\frac13\right)r_1(x)\\
&=g(x)-\left(-\frac13x+\frac13\right)\big[f(x)-2x\,g(x)\big]\\
-x+1&=\frac{x-1}{3}f(x)+\frac{-2x^2+2x+3}{3}g(x)
\end{align*}
$$
两边同乘 $-1$
$$x-1=\frac{1-x}{3}f(x)+\frac{2x^2-2x-3}{3}g(x)$$

得到：
$$\boldsymbol{u(x)=\frac{1-x}{3},\quad v(x)=\frac{2x^2-2x-3}{3}}$$

---

## 3）$f(x)=x^4-x^3-4x^2+4x+1,\ g(x)=x^2-x-1$
**解：**
辗转相除：
$$
\begin{align*}
f(x)&=(x^2-3)g(x)+(x-2) \quad &r_1(x)=x-2\\
g(x)&=(x+1)r_1(x)+1 \quad &r_2(x)=1\\
r_1(x)&=(x-2)\cdot r_2(x)+0
\end{align*}
$$
最大公因式：
$$(f(x),g(x))=1$$

回代：
$$
\begin{align*}
1 &= g(x)-(x+1)r_1(x) \\
&= g(x)-(x+1)\big[f(x)-(x^2-3)g(x)\big] \\
&= -(x+1)f(x)+\big[1+(x+1)(x^2-3)\big]g(x) \\
&= -(x+1)f(x)+(x^3+x^2-3x-2)g(x)
\end{align*}
$$

得到：
$$\boldsymbol{u(x)=-x-1,\quad v(x)=x^3+x^2-3x-2}$$

---

### 答案汇总
1. $u(x)=-x-1,\ v(x)=x+2,\quad (f,g)=x^2-2$
2. $\displaystyle u(x)=\frac{1-x}{3},\ v(x)=\frac{2x^2-2x-3}{3},\quad (f,g)=x-1$
3. $u(x)=-x-1,\ v(x)=x^3+x^2-3x-2,\quad (f,g)=1$

> 注：满足 $u(x)f+v(x)g=(f,g)$ 的多项式 $u(x),v(x)$ 不唯一。
