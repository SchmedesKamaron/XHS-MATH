### 证明
设 $\{x_n\}$ 为任意数列，要证极限

$$
\lim_{n\to\infty}\big(2+\sin x_n\big)^{\frac{1}{n}}
$$

存在。

对任意实数 $t$，正弦函数满足

$$
-1 \le \sin t \le 1
$$

因此对任意 $n$ ：

$$
-1 \le \sin x_n \le 1
$$

$$
1 \le 2+\sin x_n \le 3
$$

各项同时取 $\dfrac1n$ 次方（  $n>0$  ，  $t\mapsto t^{1/n}$   在  $t>0$  单调递增，不等号方向不变）：

$$
1^{\frac1n} \le \big(2+\sin x_n\big)^{\frac1n} \le 3^{\frac1n}
$$

利用结论： $\forall a>0,\ \displaystyle\lim_{n\to\infty} a^{\frac1n}=1$  ，于是

$$
\lim_{n\to\infty} 1^{\frac1n}=1,\quad \lim_{n\to\infty} 3^{\frac1n}=1
$$


由**数列夹逼准则（迫敛定理）**：

$$
\lim_{n\to\infty}\big(2+\sin x_n\big)^{\frac1n}=1
$$


故此极限存在，极限值为 $1$。
