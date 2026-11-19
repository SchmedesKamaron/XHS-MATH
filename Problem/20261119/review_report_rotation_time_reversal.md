# 审查报告：[《旋转对称性与时间反演对称性》](https://zhuanlan.zhihu.com/p/2106496592765363332?share_code=18qgB79wPcFE0&utm_psn=2106878612406277697)

- **作者**：[钱睿雯](https://www.zhihu.com/people/jiang-lou-yue-27)
- **审查日期**：2026-11-19

## 结论

推导主体正确，但有一处硬错误、一处概念混淆、两处逻辑缺口。结论可信，公式不能原样照抄。

我用数值方法独立验证了关键例子（ $j=3/2$   两粒子态）：$M=0$ 子空间 $J^2$ 的本征值为  $0,2,6,12$ （对应 $J=0,1,2,3$）， $|\Phi\rangle$  在  $J=0$  与  $J=2$  上的投影都是 $1/\sqrt{2}$  ，且  $\hat T|\Phi\rangle=|\Phi\rangle$  。作者的例子和分解完全正确。

---

## 一、硬错误（必须改）

**对易子指标写错。** 原文：

$$
[\hat J_\pm, a^\dagger_{ajm}] = \sqrt{(j\mp m)(j\pm m+1)}\, a^\dagger_{aj,m+1}
$$

根号因子对，末态指标错。正确结果是

$$
[\hat J_+, a^\dagger_{ajm}] = \sqrt{(j-m)(j+m+1)}\, a^\dagger_{aj,m+1},\qquad [\hat J_-, a^\dagger_{ajm}] = \sqrt{(j+m)(j-m+1)}\, a^\dagger_{aj,m-1}
$$

即必须是 $a^\dagger_{aj,m\pm1}$。

反证：若 $[\hat J_-,a^\dagger_m]\propto a^\dagger_{m+1}$，用 Jacobi 恒等式，

$$
[\hat J_z,[\hat J_-,a^\dagger_m]]=[-\hat J_-,a^\dagger_m]+[\hat J_-,m a^\dagger_m]=(m-1)[\hat J_-,a^\dagger_m],
$$

而直接对右边取对易子给出 $(m+1)[\hat J_-,a^\dagger_m]$  。$m+1\neq m-1$  ，矛盾。这个错误会破坏 $[\hat J_z,\hat J_-]=-\hat J_-$  。

---

## 二、概念混淆

**"时间反演的定义要求 $\hat T\hat H\hat T^{-1}=\hat H$" 是错的。** $\hat T$ 的定义是反幺正性加 $\hat T i\hat T^{-1}=-i$；$\hat T\hat H\hat T^{-1}=\hat H$ 是"哈密顿量具有时间反演对称性"这一物理陈述，不是 $\hat T$ 的定义。文章自己在前面写"奇数费米子体系可以不具有时间反演不变性"——若按这句"定义"，两句话直接自相矛盾。

正确说法：若系统 T 不变，则 $\hat T\hat H\hat T^{-1}=\hat H$。

---

## 三、逻辑缺口

**Kramers 简并的证明链被压缩。** $\langle\Psi|\hat T\Psi\rangle=0$ 的代数推导本身正确（   $\langle\hat T\hat T\Psi|\hat T\Psi\rangle=\langle\Psi|\hat T\Psi\rangle=-\langle\Psi|\hat T\Psi\rangle$  ）。但要推出"至少两重简并"还缺两步没明说：

1. $[\hat T,\hat H]=0 \Rightarrow \hat T|\Psi\rangle$   是**同能量**本征态；
2. 正交 $\Rightarrow$ 它与 $|\Psi\rangle$ 线性无关。

另外这个内积为零对 $\hat T^2=-1$ 空间中的**任意**态都成立，与 $H$ 无关，简并性完全来自 $[\hat T,\hat H]=0$。

**"Kramers 伴随态会包含在角动量多重态之中"不严格。** 准确表述：$\hat T$ 把 $(E,J,M)$ 映到 $(E,J,-M)$。只有当 $(E,J)$ 子空间里没有多个同 $J$ 多重态偶然简并时，它才落在"同一个"多重态内；否则落在整个 $(E,J)$ 简并子空间里，可能是不同多重态的线性组合。

**跳步：** 开头写的一般形式

$$
\hat{H}=\sum_{\alpha\beta}t_{\alpha\beta}a_\alpha^\dagger a_\beta + \frac{1}{4}\sum_{\alpha\beta\gamma\delta}\bar{v}_{\alpha\beta\gamma\delta}a_\alpha^\dagger a_\beta^\dagger a_\delta a_\gamma
$$

并不自动满足 $[\hat H,\hat J_i]=0$。需要 $t_{\alpha\beta}$ 正比于 $\delta_{\alpha\beta}$（球对称单粒子项）且 $\bar v$ 是旋转标量；T 不变还要求矩阵元在选定相位约定下为实数。文章直接写 $[\hat H,\hat J_i]=0$，没从 $H$ 的形式推出来。

---

## 四、验证通过的部分

| 项目 | 判定 |
|---|---|
| $\hat T^2=(-1)^A$ 、半整数 $j$ 下 $\hat T^2 a^\dagger \hat T^{-2}=-a^\dagger$ | 正确（实数相位，反幺正性不引入额外共轭） |
| $\hat T\hat J_i\hat T^{-1}=-\hat J_i$ ，$\hat T\hat J_\pm\hat T^{-1}=-\hat J_\mp$ | 正确 |
| $\hat T\hat R(\Omega)\hat T^{-1}=\hat R(\Omega)$ 及 $R_y$ 例子 | 正确 |
| $|\Phi\rangle$ 的 T 不变性、$\hat J_z=0$、$1/\sqrt2$ 的 $J=0$/$J=2$ 分解 | 正确（已数值复核） |
| 自旋 $1/2$ 取 $\hat T=-i\sigma_y\hat K$，$\hat T^2=-1$ | 正确 |
| $\frac12\sum\langle\alpha\beta|V|\gamma\delta\rangle a^\dagger a^\dagger aa=\frac14\sum\bar v\, a^\dagger a^\dagger aa$  的系数 | 正确 |

**小瑕疵：** 用了 $D^j_{m'm}$ 却没声明 D 矩阵指标约定（有的教材用 $D^j_{mm'}$ ，容易混）；$R_y$ 例子的指数写法绕但结果对。

