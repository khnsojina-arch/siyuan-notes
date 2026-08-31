---
title: 第二章 一维随机变量及其分布
date: 2026-08-31
---

![image](image1.png)

# 第二章 一维随机变量及其分布

# 1️⃣随机变量的概念及分布

## 一、随机变量的定义

　　在样本空间 $\Omega=\{e\}$ 上定义的一个实值单值函数 $X=X(e)\quad(e\in\Omega)$，称为随机变量。

　　随机变量常用大写字母 $X,Y,Z$ 等表示，其取值通常用小写字母 $x,y,z$ 等表示。

## 二、随机变量的分类

　　随机变量有三种：

1. 离散型随机变量；
2. 连续型随机变量；
3. 既非离散型也非连续型随机变量。

## 三、随机变量的分布函数

### 1. 随机变量分布函数的定义

　　设 $X$ 是一个随机变量，对于任意实数 $x$，令

$$
F(x)=P\{X \le x\}\quad(-\infty<x<+\infty)
$$

　　称 $F(x)$ 为随机变量 $X$ 的概率分布函数，简称为分布函数。

### <span data-type="text" style="color: var(--b3-font-color1);">2. 利用分布函数求各种随机事件的概率</span>

　　已知随机变量 $X$ 的分布函数 $F(x)=P\{X \le x\}$，则有：

1. $\boldsymbol{P\{X \le a\} = F(a)}$
2. $\boldsymbol{P\{X > a\} = 1-F(a)}$
3. $\boldsymbol{P\{X < a\} = \lim\limits_{x \to a^-}F(x)=F(a-0)}$
4. $\boldsymbol{P\{X \ge a\} = 1-F(a-0)}$

![image.png](https://siyuan-image-1330022534.cos.ap-shanghai.myqcloud.com/siyuan/20260831103720.png)

5. $\boldsymbol{P\{X = a\} = F(a)-F(a-0)}$
6. $\boldsymbol{P\{a < X \le b\} = F(b)-F(a)}$
7. $\boldsymbol{P\{a \le X < b\} = F(b-0)-F(a-0)}$
8. $\boldsymbol{P\{a < X < b\} = F(b-0)-F(a)}$
9. $\boldsymbol{P\{a \le X \le b\} = F(b)-F(a-0)}$

　　**==9=8+5+5，可以自己验证一下==**

> 注：$F(a-0)$ 代表分布函数在 $a$ 点的**左极限** $\lim\limits_{x\to a^-}F(x)$。  
> 离散型看跳跃，$P\{X=a\}$ 就是 $F(x)$ 在 $a$ 处跳跃高度；  
> 连续型 $F(a-0)=F(a)$，$P\{X=a\}=0$。

### <span data-type="text" style="background-color: var(--b3-font-background9);">如何求分布函数？</span>

　　例题：求随机变量的分布函数[^1]

### 【例1】设随机变量 $X$ 的分布函数为

$$
F(x)=
\begin{cases}
0, & x<0,\\[4pt]
\dfrac12, & 0\le x<1,\\[4pt]
1-\mathrm{e}^{-x}, & x\ge 1.
\end{cases}
$$

　　求 $P\{X=1\}$。

---

　　公式：$\boldsymbol{P\{X=a\}=F(a)-F(a-0)}$

1. $F(1)$：代入 $x\ge1$ 段：

$$
F(1)=1-\mathrm{e}^{-1}
$$

2. $F(1-0)$ 是 $x\to 1^-$ 的左极限，用 $0\le x<1$ 段：

$$
F(1-0)=\frac12
$$

3. ‍

$$
P\{X=1\}=F(1)-F(1-0)=\big(1-\mathrm{e}^{-1}\big)-\frac12=\boldsymbol{\frac12-\mathrm{e}^{-1}}
$$

### <span data-type="text" style="color: var(--b3-font-color1);">3. 分布函数的性质</span>

　　设随机变量 $X$ 的分布函数为 $F(x)=P\{X \le x\}$，则 $F(x)$ 满足：

1. **非负性**：$\boldsymbol{0 \le F(x) \le 1}$；
2. **规范性**：$F(-\infty)=\lim_{x\to-\infty}F(x)=0,\quad F(+\infty)=\lim_{x\to+\infty}F(x)=1$

3. **单调不减性**：对任意 $x_1<x_2$，有 $\boldsymbol{F(x_1)\le F(x_2)}$；
4. **右连续性**：$\boldsymbol{F(x_0)=F(x_0+0)}$。

> 说明：
>
> - ==$F(x_0+0)=\lim\limits_{x\to x_0^+}F(x)$==​==，代表在== ==$x_0$== ==处的右极限；==
> - 以上四条同时成立，是函数成为分布函数的充要条件。

### 【例2】设 $X_1$ 和 $X_2$ 的分布函数分别为 $F_1(x)$ 和 $F_2(x)$，则（）

　　(A) $F_1(x)+F_2(x)$ 必为某一随机变量的分布函数。  
(B) $F_1(x)-F_2(x)$ 必为某一随机变量的分布函数。  
<u>(C) </u><u>$F_1(x)F_2(x)$</u><u> 必为某一随机变量的分布函数。</u>  
(D) $-\dfrac13F_1(x)+\dfrac43F_2(x)$ 必为某一随机变量的分布函数。

　　**选项A** 

$$
\lim_{x\to+\infty}\big[F_1(x)+F_2(x)\big]=1+1=2 \neq 1
$$

　　不满足规范性，不是分布函数。

　　**选项B** 

　　$\lim\limits_{x\to+\infty}\big[F_1(x)-F_2(x)\big]=1-1=0\neq1$；  
还可能出现函数值小于0，不满足条件。

　　**选项C** 

　　令 $F(x)=F_1(x)F_2(x)$

1. $0\le F_1,F_2\le1 \Rightarrow 0\le F(x)\le1$
2. $\lim\limits_{x\to-\infty}F(x)=0\cdot0=0$，$\lim\limits_{x\to+\infty}F(x)=1\cdot1=1$
3. $F_1,F_2$ 单调不减，乘积也单调不减
4. $F_1,F_2$ 右连续，乘积右连续  
   全部满足分布函数四条性质。

> 实际背景：若 $X_1,X_2$ 独立，则 $F_1(x)F_2(x)$ 是 $\max\{X_1,X_2\}$ 的分布函数。

　　**选项D** 

### <span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">混合分布要求：</span>$a_1F_1+a_2F_2$<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">，必须满足 </span>$\boldsymbol{a_1\ge0,\ a_2\ge0,\ a_1+a_2=1}$<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">。</span>本题 $a_1=-\dfrac13<0$，系数为负，不满足，不是分布函数。连续型的也同理。

　　‍

### 【例3】设随机变量 $X$ 的分布函数为 $F(x)$，则下列函数中，仍为分布函数的是（$\boldsymbol A$）。(A)$F(2x-1)$  (B)$F(1-x)$  (C)$F(x^2)$  (D)$1-F(-x)$

#### 选项A：$\boldsymbol{G(x)=F(2x-1)}$

1. 单调性：$t=2x-1$ 关于 $x$ 单调递增，$F(\cdot)$单调不减，复合后 $G(x)$单调不减 ✔
2. 有界：$0\le F(\cdot)\le1 \Rightarrow 0\le G(x)\le1$ ✔
3. 无穷极限

$$
\lim_{x\to-\infty}F(2x-1)\xlongequal{t=2x-1}\lim_{t\to-\infty}F(t)=0
$$

$$
\lim_{x\to+\infty}F(2x-1)\xlongequal{t=2x-1}\lim_{t\to+\infty}F(t)=1
$$

　　✔  
4. 右连续

$$
\lim_{x\to a^+}F(2x-1)=\lim_{t\to(2a-1)^+}F(t)=F(2a-1)=G(a)
$$

　　✔

> 四条全部满足，是分布函数。

#### 选项B：$\boldsymbol{G(x)=F(1-x)}$

　　$t=1-x$ 随 $x$ 增大而减小，$F$单调不减，复合后 $G(x)$​**单调递减**，违反“单调不减”条件。  
❌排除。

#### 选项C：$\boldsymbol{G(x)=F(x^2)}$

$$
\lim_{x\to-\infty}G(x)=\lim_{x\to-\infty}F(x^2)\xlongequal{t=x^2}\lim_{t\to+\infty}F(t)=1 \neq 0
$$

　　$x\to-\infty$极限不等于0，不满足无穷条件。  
❌排除。

#### 选项D：$\boldsymbol{G(x)=1-F(-x)}$

　　考察右连续：

$$
\lim_{x\to a^+}G(x)=\lim_{x\to a^+}\big[1-F(-x)\big]
\xlongequal{t=-x}\lim_{t\to -a^-}\big[1-F(t)\big]=1-F(-a^-)
$$

　　而 $G(a)=1-F(-a)$。  
当原分布 $F(x)$ 存在跳跃间断点（离散型随机变量），$F(-a^-) \neq F(-a)$，右连续被破坏。

> 注意：正态分布例子碰巧成立，但**对任意分布函数不成立**。  
> ❌排除。

　　‍

　　‍

# 2️⃣一维==离散型==随机变量及其概率分布

## 1. 离散型随机变量的定义

　　若随机变量 $X$ 的取值是**有限个或者可列无穷多个**，则称 $X$ 为离散型随机变量。

## 2. 离散型随机变量的分布律

　　设 $X$ 为离散型随机变量，其所有可能取值为 $x_1,x_2,\dots,x_k,\dots$，且 $X$ 取各个值 $x_k$ 的概率为

$$
P\{X=x_k\}=p_k,\quad \text{其中 } p_k \ge 0,\ (k=1,2,\cdots),\ \sum_{k=1}^{\infty} p_k=1,
$$

　　则称 $P\{X=x_k\}=p_k\,(k=1,2,\cdots)$ 为随机变量 $X$ 的概率分布或分布律，也可记为：

|$X$|$x_1$|$x_2$|$x_3$|$\cdots$|$x_k$|$\cdots$|
| --| --| --| --| --| --| --|
|$p$|$p_1$|$p_2$|$p_3$|$\cdots$|$p_k$|$\cdots$|

> 分布律两条充要条件：
>
> 1. 非负：$\boldsymbol{p_k \ge 0}$
> 2. 归一：$\boldsymbol{\sum\limits_{k=1}^{\infty} p_k = 1}$

## 3. 离散型随机变量的分布函数

　　**定义：**

　　若 $X$ 的分布律为 $P\{X=x_k\}=p_k\,(k=1,2,\cdots,n)$，不妨设 $x_1<x_2<\cdots<x_k<\cdots<x_n$，则

$$
F(x)=
\begin{cases}
0, & x<x_1,\\[4pt]
p_1, & x_1\le x<x_2,\\[4pt]
p_1+p_2, & x_2\le x<x_3,\\[4pt]
\vdots & \\[4pt]
1, & x\ge x_n.
\end{cases}
$$

> 要点：
>
> 1. 离散型分布函数是**阶梯函数**，在每个 $x_k$ 处发生跳跃；
> 2. 跳跃高度等于该点概率：$\boldsymbol{P\{X=x_k\}=F(x_k)-F(x_k-0)}$；
> 3. 分布函数右连续。

　　‍

　　‍

# 3️⃣常见的离散型分布

## 1. 二项分布

　　设事件 $A$ 在任意一次试验中出现的概率都是 $p\ (0<p<1)$，$X$ 表示 $n$ 重伯努利试验中事件 $A$ 发生的次数，其所有可能的取值为 $0,1,2,\dots,n$，且相应的概率为：

$$
P\{X=k\}=C_n^k p^k(1-p)^{n-k}\quad (k=0,1,\dots,n),
$$

　　则称 $X$ 服从二项分布，记为 $\boldsymbol{X \sim B(n,p)}$。

　　二项分布的期望：$\boldsymbol{E(X)=np}$，方差：$\boldsymbol{D(X)=np(1-p)}$。

### 【例】设随机变量 $X$ 服从于参数为 $(2,p)$ 的二项分布，随机变量 $Y$ 服从于参数为 $(3,p)$ 的二项分布，若 $P\{X \ge 1\}=\dfrac{5}{9}$，则 $P\{Y \ge 1\}=$________。

　　$X\sim B(2,p)$

$$
P\{X\ge 1\}=1-P\{X=0\}=1-C_2^0 p^0(1-p)^2=1-(1-p)^2
$$

　　由题：

$$
1-(1-p)^2=\frac{5}{9}
$$

$$
(1-p)^2=\frac{4}{9} \Rightarrow 1-p=\frac23 \quad(0<p<1) \Rightarrow p=\frac13
$$

　　$Y\sim B(3,p)$，$p=\dfrac13$

$$
\begin{aligned}
P\{Y\ge 1\}&=1-P\{Y=0\} \\
&=1-C_3^0 p^0(1-p)^3 \\
&=1-\left(\frac23\right)^3 \\
&=1-\frac{8}{27}\\
&=\boldsymbol{\frac{19}{27}}
\end{aligned}
$$

## 2. 0-1分布

　　若随机变量 $X$ 的概率分布为：

$$
P\{X=k\}=p^k(1-p)^{1-k},\ k=0,1\ (0<p<1),
$$

　　则称 $X$ 服从0-1分布。

　　0-1分布 $X$ 的期望：$\boldsymbol{E(X)=p}$，方差：$\boldsymbol{D(X)=p(1-p)}$。

> 说明：0-1分布是二项分布 $B(n,p)$ 当 $n=1$ 的特殊情况。

　　‍

## 3. 泊松分布

　　设随机变量 $X$ 的概率分布为：

$$
P\{X=k\}=\frac{\lambda^k e^{-\lambda}}{k!},\quad (k=0,1,2,\cdots),\ \text{其中参数 } \lambda>0,
$$

　　则称 $X$ 服从参数为 $\lambda$ 的泊松分布，记为 $\boldsymbol{X \sim P(\lambda)}$。

　　泊松分布的期望：$\boldsymbol{E(X)=\lambda}$，方差：$\boldsymbol{D(X)=\lambda}$。

> 泊松近似：当 $n$ 很大，$p$ 很小，$\lambda=np$ 适中时，二项分布 $B(n,p)$ 近似泊松分布 $P(\lambda)$。

### 泊松定理

　　设 $\lambda>0$ 是一个常数，$n$ 是任意正整数，设 $\lambda=np_n$，则对于任一固定的非负整数 $k$，有

$$
\lim_{n\rightarrow+\infty} \mathrm{C}_n^k p_n^k(1-p_n)^{n-k}=\frac{\lambda^k}{k!}\mathrm{e}^{-\lambda},\quad (k=0,1,2,\cdots).
$$

> 意义：当 $n$ 很大，$p$ 很小，**$\lambda=np$**  ****  <span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">适中时，二项分布 </span>$B(n,p)$<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);"> 可以用泊松分布 </span>$P(\lambda)$<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);"> 近似计算。</span>

　　‍

## 4. 几何分布

　　设随机变量 $X$ 的概率分布为：

$$
P\{X=k\}=(1-p)^{k-1}p,\quad (0<p<1),\ k=1,2,\cdots
$$

　　则称 $X$ 服从几何分布。

　　几何分布的期望：$\boldsymbol{E(X)=\dfrac{1}{p}}$，方差：$\boldsymbol{D(X)=\dfrac{1-p}{p^2}}$。

> 含义：独立重复试验，<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">直到第一次成功所需要的试验次数；具有</span>**无记忆性**<span data-type="text" style="background-color: var(--b3-card-error-background); color: var(--b3-card-error-color);">。</span>**注意这个k是从1开始的**

　　‍

## 5. 超几何分布

　　设随机变量 $X$ 的概率分布为：

$$
P\{X=k\}=\frac{\mathrm{C}_M^k \mathrm{C}_{N-M}^{n-k}}{\mathrm{C}_N^n},\quad k=0,1,2,\dots,n,
$$

　　其中 $M,N,n$ 都是正整数，且 $n\le M\le N$，则称 $X$ 服从参数为 $M,N$ 和 $n$ 的超几何分布，记为 $\boldsymbol{X \sim H(n,M,N)}$。

> 含义：不放回抽样；总共有 $N$ 个元素，其中 $M$ 个合格品，抽取 $n$ 个样本，样本中合格品的数量服从该分布。  
> 当 $N$ 很大，$\dfrac{n}{N}$ 很小时，超几何分布近似二项分布 $B\left(n,\dfrac{M}{N}\right)$。

　　‍

　　‍

　　‍

# 4️⃣一维<u>==连续型==</u>随机变量及其概率分布

## 1. 连续型随机变量的定义

　　如果对于随机变量 $X$ 的分布函数 $F(x)$，存在非负可积函数 $f(x)$，使得对于任意实数 $x$，有

$$
F(x)=\int_{-\infty}^{x} f(t)\mathrm{d}t
$$

　　则称 $X$ 为连续型随机变量，函数 $f(x)$ 称为 $X$ 的概率密度函数（简称密度函数）。

> 重要性质：
>
> 1. $f(x)\ge 0$
> 2. $\displaystyle \int_{-\infty}^{+\infty}f(x)\mathrm{d}x=1$
> 3. $P\{a<X\le b\}=\int_{a}^{b}f(x)\mathrm{d}x$
> 4. 连续型随机变量在任意单点处概率：$\boldsymbol{P\{X=x_0\}=0}$
> 5. 若 $f(x)$ 在点 $x$ 处连续，则 $F'(x)=f(x)$

## 【例】已知连续型随机变量 $X$ 的密度函数为

$$
f(x)=\begin{cases}
x, & x\in[0,1),\\
2-x, & x\in[1,2),\\
0, & \text {其他}.
\end{cases}
$$

　　求分布函数 $F(x)$。

　　**解：**

　　由分布函数的定义，

$$
F(x)=\int_{-\infty}^{x}f(t)\,\mathrm {d}t.
$$

1. 当 $x<0$ 时，

$$
F(x)=\int_{-\infty}^{x}0\,\mathrm {d}t=0.
$$

2. 当 $0\le x<1$ 时，

$$
F(x)=\int_{-\infty}^{0}0\,\mathrm {d}t+\int_{0}^{x}t\,\mathrm {d}t=\frac {1}{2}x^2.
$$

3. 当 $1\le x<2$ 时，

$$
\begin{aligned}
F(x)&=\int_{-\infty}^{0}0\,\mathrm {d}t+\int_{0}^{1}t\,\mathrm {d}t+\int_{1}^{x}(2-t)\,\mathrm {d}t\\
&=\frac {1}{2}+\left.\left(2t-\frac {1}{2}t^2\right)\right|_{1}^{x}\\
&=-\frac {1}{2}x^2+2x-1.
\end{aligned}
$$

4. 当 $x\ge 2$ 时，

$$
\begin{aligned}
F(x)&=\int_{-\infty}^{0}0\,\mathrm {d}t+\int_{0}^{1}t\,\mathrm {d}t+\int_{1}^{2}(2-t)\,\mathrm {d}t+\int_{2}^{x}0\,\mathrm {d}t\\
&=\frac {1}{2}+\frac {1}{2}=1.
\end{aligned}
$$

　　综上，

$$
F(x)=\begin{cases}
0, & x<0,\\
\dfrac {1}{2}x^2, & 0\le x<1,\\
-\dfrac {1}{2}x^2+2x-1, & 1\le x<2,\\
1, & x\ge 2.
\end{cases}
$$

## 2. 概率密度的性质

　　（1）非负性：$f(x) \ge 0 \quad (-\infty < x < +\infty)$。

　　（2）规范性：$\displaystyle \int_{-\infty}^{+\infty} f(x)\mathrm{d}x = 1$。

　　（3）对于任意实数 $a$ 和 $b \ (a<b)$，有

$$
P\{a<X \le b\}=P\{a \le X < b\}=P\{a<X<b\}=P\{a \le X \le b\}=\int_{a}^{b} f(x)\mathrm{d}x.
$$

　　==一个点的值不影响整体的面积值。==

　　（4）在 $f(x)$ 的连续点处，有 $F'(x)=f(x)$。

　　‍

　　‍

# 5️⃣常见的连续型分布

## 1. 均匀分布

　　如果随机变量 $X$ 的密度函数为

$$
f(x)=
\begin{cases}
\displaystyle \frac{1}{b-a}, & a\le x \le b,\\[4pt]
0, & \text{其他}.
\end{cases}
$$

　　则称 $X$ 服从 $[a,b]$ 上的均匀分布，记作 $X\sim U(a,b)$。其中 $a,b$ 是分布的参数。

　　$X$ 的分布函数为

$$
F(x)=
\begin{cases}
0, & x<a,\\[4pt]
\displaystyle \frac{x-a}{b-a}, & a\le x < b,\\[4pt]
1, & x\ge b.
\end{cases}
$$

　　均匀分布的期望：$\displaystyle E(X)=\frac{a+b}{2}$，方差：$\displaystyle D(X)=\frac{(b-a)^2}{12}$。

　　‍

## 2. 指数分布

　　如果随机变量 $X$ 的概率密度为

$$
f(x)=
\begin{cases}
\lambda \mathrm{e}^{-\lambda x}, & x>0,\\
0, & x \le 0,
\end{cases}
$$

　　其中 $\lambda>0$ 为参数，则称 $X$ 服从参数为 $\lambda$ 的指数分布，记作 $X\sim E(\lambda)$。

　　$X$ 的分布函数为

$$
F(x)=
\begin{cases}
1-\mathrm{e}^{-\lambda x}, & x>0,\\
0, & x \le 0.
\end{cases}
$$

　　指数分布的期望：$\displaystyle E(X)=\frac{1}{\lambda}$，方差：$\displaystyle D(X)=\frac{1}{\lambda^2}$。

## 【例】设随机变量 $Y$ 服从参数为 $1$ 的指数分布，$a$ 为常数且大于零，则

$$
P\{Y \le a+1 \mid Y> a\} = \_\_\_\_\_.
$$

　　解：  
$Y\sim E(1)$，分布函数

$$
F_Y(y)=
\begin{cases}
1-\mathrm{e}^{-y}, & y>0\\
0, & \text{其他}
\end{cases}
$$

　　由条件概率公式：

$$
\begin{aligned}
P\{Y \le a+1 \mid Y> a\}
&=\frac{P\{a<Y \le a+1\}}{P\{Y> a\}} \\
&=\frac{F(a+1)-F(a)}{1-F(a)} \\
&=\frac{\big[1-\mathrm{e}^{-(a+1)}\big]-\big(1-\mathrm{e}^{-a}\big)}{1-(1-\mathrm{e}^{-a})} \\
&=\frac{ \mathrm{e}^{-a}-\mathrm{e}^{-(a+1)} }{\mathrm{e}^{-a}} \\
&=\frac{\mathrm{e}^{-a}(1-\mathrm{e}^{-1})}{\mathrm{e}^{-a}} \\
&=1-\mathrm{e}^{-1}.
\end{aligned}
$$

> 考点：指数分布**无记忆性**：$P\{X>s+t\mid X>s\}=P\{X>t\}$  
> $P\{Y\le a+1\mid Y>a\}=1-P\{Y>a+1\mid Y>a\}=1-P\{Y>1\}=1-\mathrm{e}^{-1}$

　　‍

## 3. 正态分布

### ① 正态分布的定义

　　<span data-type="text" style="background-color: var(--b3-inline-builtin-error-background-color, var(--b3-card-error-background)); color: var(--b3-inline-builtin-error-color, var(--b3-card-error-color));">如果随机变量 </span>$X$<span data-type="text" style="background-color: var(--b3-inline-builtin-error-background-color, var(--b3-card-error-background)); color: var(--b3-inline-builtin-error-color, var(--b3-card-error-color));"> 的密度函数为（这个密度函数一定要背下来！！）</span>

$$
f(x)=\frac{1}{\sqrt{2\pi}\sigma}\mathrm{e}^{-\frac{(x-\mu)^2}{2\sigma^2}} \quad (-\infty<x<+\infty),
$$

　　其中 $\mu,\sigma$ 为常数，$-\infty<\mu<+\infty$，$\sigma>0$，则称 $X$ 服从参数为 $\mu$ 和 $\sigma^2$ 的正态分布，记作

$$
X\sim N(\mu,\sigma^2).
$$

　　正态分布的期望：$E(X)=\mu$，方差：$D(X)=\sigma^2$。

![image.png](https://siyuan-image-1330022534.cos.ap-shanghai.myqcloud.com/siyuan/20260830161534.png)

### 【例】利用正态分布概率密度的结论计算积分 $\displaystyle \int_{-\infty}^{+\infty} \mathrm{e}^{-x^2+2x}\mathrm{d}x$。

　　解：  
先对指数配方：

$$
-x^2+2x = -(x^2-2x)=-\big[(x-1)^2-1\big] = -(x-1)^2+1
$$

$$
\begin{aligned}
\int_{-\infty}^{+\infty} \mathrm{e}^{-x^2+2x}\mathrm{d}x
&=\int_{-\infty}^{+\infty}\mathrm{e}^{-(x-1)^2+1}\mathrm{d}x \\
&=\mathrm{e}\int_{-\infty}^{+\infty}\mathrm{e}^{-(x-1)^2}\mathrm{d}x
\end{aligned}
$$

　　正态分布密度规范性：

$$
\int_{-\infty}^{+\infty}\frac{1}{\sqrt{2\pi}\sigma}\mathrm{e}^{-\frac{(x-\mu)^2}{2\sigma^2}}\mathrm{d}x=1
\Rightarrow
\int_{-\infty}^{+\infty}\mathrm{e}^{-\frac{(x-\mu)^2}{2\sigma^2}}\mathrm{d}x=\sqrt{2\pi}\,\sigma
$$

　　对比 $\displaystyle \mathrm{e}^{-(x-1)^2}=\mathrm{e}^{-\frac{(x-1)^2}{2\cdot\frac12}}$，得 $2\sigma^2=1 \Rightarrow \sigma=\frac{1}{\sqrt2}$

$$
\int_{-\infty}^{+\infty}\mathrm{e}^{-(x-1)^2}\mathrm{d}x=\sqrt{2\pi}\cdot \frac{1}{\sqrt2}=\sqrt{\pi}
$$

　　代入：

$$
\int_{-\infty}^{+\infty} \mathrm{e}^{-x^2+2x}\mathrm{d}x=\boldsymbol{e\sqrt{\pi}}
$$

### ② 标准正态分布

　　当正态分布中的参数 $\mu=0,\ \sigma=1$ 时，称为标准正态分布，记作 $N(0,1)$。  
密度函数记为 $\varphi(x)$，分布函数记为 $\Phi(x)$。

$$
\varphi(x)=\frac{1}{\sqrt{2\pi}}\mathrm{e}^{-\frac{x^2}{2}} \quad(-\infty<x<+\infty)
$$

### ③ 标准正态的性质

1. $\boldsymbol{\varphi(-x)=\varphi(x)}$ （$\varphi(x)$ 是偶函数，图像关于 $y$ 轴对称）
2. $\boldsymbol{\Phi(0)=\dfrac12}$
3. $\boldsymbol{\Phi(-x)=1-\Phi(x)}$
4. $\boldsymbol{P\{|X|\le a\}=2\Phi(a)-1}$

> 说明：
>
> - $\varphi(x)$：概率密度；$\Phi(x)=\displaystyle\int_{-\infty}^x\varphi(t)\mathrm{d}t$，分布函数。
> - $\Phi(-x)=1-\Phi(x)$ 用来算负的自变量，不用查负的标准正态表。
> - $P\{|X|\le a\}=P\{-a\le X\le a\}=\Phi(a)-\Phi(-a)=\Phi(a)-\big[1-\Phi(a)\big]=2\Phi(a)-1$。

### ④ 上$\boldsymbol{\alpha}$分位点

　　设 $X\sim N(0,1)$，对于给定的 $\alpha(0<\alpha<1)$，若 $u_\alpha$ 满足

$$
\boldsymbol{P\{X>u_\alpha\}=\alpha}
$$

　　则称 $u_\alpha$ 为标准正态分布的**上**​**$\boldsymbol{\alpha}$**​**分位点**。

　　‍

![image.png](https://siyuan-image-1330022534.cos.ap-shanghai.myqcloud.com/siyuan/20260830163133.png)

![image.png](https://siyuan-image-1330022534.cos.ap-shanghai.myqcloud.com/siyuan/20260830163659.png)

　　‍

### ⑤ 标准化

　　若随机变量 $\boldsymbol{X \sim N(\mu,\sigma^2)}$，令

$$
\boldsymbol{Z=\frac{X-\mu}{\sigma} \sim N(0,1)}
$$

　　$Z$ 称为 $X$ 的标准化变量。

> 含义：一般正态做平移、缩放，转化为标准正态 $N(0,1)$，就可以用 $\Phi(x)$ 计算概率。

#### 概率计算公式

$$
P\{X\le x\}=P\left\{\frac{X-\mu}{\sigma}\le \frac{x-\mu}{\sigma}\right\}=\boldsymbol{\Phi\left(\frac{x-\mu}{\sigma}\right)}
$$

　　‍

#### 例题1

　　设随机变量 $X$ 与 $Y$ 均服从正态分布，$X \sim N(\mu,4^2)$，$Y \sim N(\mu,5^2)$。  
记 $p_1 = P\{X \le \mu-4\},\ p_2 = P\{Y \ge \mu+5\}$，则（）  
(A) 对任何实数 $\mu$，都有 $p_1 = p_2$  
(B) 对任何实数 $\mu$，都有 $p_1 < p_2$  
(C) 只对 $\mu$ 的个别值，都有 $p_1 = p_2$  
(D) 对任何实数 $\mu$，都有 $p_1 > p_2$

　　**解：标准化**

$$
\begin{aligned}
p_1&=P\{X\le \mu-4\} \\
&=P\left\{\frac{X-\mu}{4}\le \frac{\mu-4-\mu}{4}\right\}\\
&=P\{Z\le -1\}=\Phi(-1)=1-\Phi(1)
\end{aligned}
$$

$$
\begin{aligned}
p_2&=P\{Y\ge \mu+5\} \\
&=P\left\{\frac{Y-\mu}{5}\ge \frac{\mu+5-\mu}{5}\right\}\\
&=P\{Z\ge 1\}=1-\Phi(1)
\end{aligned}
$$

　　$p_1=p_2$，与 $\mu$ 无关。  
**答案：A**

---

#### 例题2

　　设随机变量 $X \sim N(\mu,\sigma^2),(\sigma>0)$，记 $p=P\{X\le \mu+\sigma^2\}$，则（）  
(A) $p$ 随着 $\mu$ 的增加而增加  
(B) $p$ 随着 $\sigma$ 的增加而增加  
(C) $p$ 随着 $\mu$ 的增加而减少  
(D) $p$ 随着 $\sigma$ 的增加而减少

　　**解：标准化**

$$
\begin{aligned}
p &= P\{X\le \mu+\sigma^2\} \\
&=P\left\{\frac{X-\mu}{\sigma}\le \frac{\mu+\sigma^2-\mu}{\sigma}\right\}\\
&=P\{Z\le \sigma\}=\Phi(\sigma)
\end{aligned}
$$

　　$p=\Phi(\sigma)$，不含 $\mu$，故 $p$ 和 $\mu$ 无关。  
$\Phi'(x)=\varphi(x)>0$，$\Phi(x)$ 单调递增；$\sigma$ 增大，$\Phi(\sigma)$ 增大。  
**答案：B**

---

#### 例题3

　　设 $f_1(x)$ 为标准正态分布的概率密度，$f_2(x)$ 为 $[-1,3]$ 上均匀分布的概率密度，

$$
f(x)=
\begin{cases}
af_1(x),& x \le 0\\
bf_2(x),& x > 0
\end{cases}\quad(a>0,b>0)
$$

　　若 $f(x)$ 为概率密度，则 $a,b$ 应满足（）  
(A) $2a+3b=4$  
(B) $3a+2b=4$  
(C) $a+b=1$  
(D) $a+b=2$

　　**解：概率密度性质** **$\displaystyle\int_{-\infty}^{+\infty}f(x)\mathrm{d}x=1$**

　　$[-1,3]$ 均匀分布：区间长度 $4$，故

$$
f_2(x)=
\begin{cases}
\dfrac14,& -1\le x \le 3\\[4pt]
0,& \text{其他}
\end{cases}
$$

　　标准正态密度：$\displaystyle\int_{-\infty}^{0}f_1(x)\mathrm{d}x=\frac12$。

　　拆分积分：

$$
\begin{aligned}
\int_{-\infty}^{+\infty}f(x)\mathrm{d}x
&= a\int_{-\infty}^{0}f_1(x)\mathrm{d}x
+ b\int_{0}^{+\infty}f_2(x)\mathrm{d}x \\[4pt]
&=a\cdot \frac12 + b\int_{0}^{3}\frac14\mathrm{d}x =1 \\[4pt]
&=\frac a2 + \frac34 b =1
\end{aligned}
$$

　　两边同乘 $4$：$\boldsymbol{2a+3b=4}$。  
**答案：A**

　　‍

# 6️⃣一维随机变量函数的分布

## 一维离散型随机变量函数的分布

　　设 $X$ 是离散型随机变量，其概率分布为

$$
P\{X=x_k\}=p_k,\ k=1,2,\dots
$$

　　随机变量函数 $Y=g(X)$，则

$$
P\{Y=g(x_k)\}=p_k,\ k=1,2,\dots
$$

> 注意：若 $g(x_k)$ 出现相同函数值，**将对应概率相加**，作为 $Y$ 取该值的概率。

### 解题步骤

1. 将 $X$ 的每一个取值 $x_k$ 代入函数，得到 $y_k=g(x_k)$；
2. 把相同 $y$ 值对应的概率合并求和；
3. 去重，整理写出 $Y$ 的分布律。

### 例题

　　$X$ 的分布

|$X$|$-1$|$0$|$1$|
| :-: | :-: | :-: | :-: |
|$P$|$0.2$|$0.3$|$0.5$|

　　令 $Y=X^2$

- $x=-1 \Rightarrow y=1,\ p=0.2$
- $x=0 \Rightarrow y=0,\ p=0.3$
- $x=1 \Rightarrow y=1,\ p=0.5$

　　合并 $y=1$：$P\{Y=1\}=0.2+0.5=0.7$

　　$Y$ 的分布

|$Y$|$0$|$1$|
| :-: | :-: | :-: |
|$P$|$0.3$|$0.7$|

## 2. 一维连续型随机变量函数的分布

　　下面这个视频方法讲得非常非常好，忘记怎么算可以重新看看👇

<div>
<style>
.kg-card-main {width:min(760px,100%);margin:8px 0;font-family:var(--b3-font-family),sans-serif}.kg-bookmark-container {display:flex;min-height:112px;max-height:132px;overflow:hidden;text-decoration:none!important;color:var(--b3-theme-on-background)!important;border:1px solid var(--b3-border-color);border-radius:16px;background:color-mix(in srgb,var(--b3-theme-background) 78%,transparent);box-shadow:0 8px 24px rgba(15,23,42,.09);transition:.18s}.kg-bookmark-container:hover {transform:translateY(-1px);box-shadow:0 12px 30px rgba(15,23,42,.14)}.kg-bookmark-content {min-width:0;flex:1;display:flex;flex-direction:column;justify-content:center;padding:12px 15px}.kg-bookmark-title {font-size:15px;font-weight:700;line-height:1.35;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}.kg-bookmark-description {margin-top:5px;font-size:13px;line-height:1.45;opacity:.68;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}.kg-bookmark-metadata {margin-top:8px;display:flex;align-items:center;gap:6px;font-size:12px;opacity:.62;white-space:nowrap;overflow:hidden}.kg-bookmark-icon {width:16px;height:16px;border-radius:4px}.kg-bookmark-thumbnail {position:relative;flex:0 0 180px;overflow:hidden}.kg-bookmark-thumbnail img {position:absolute;inset:0;width:100%;height:100%;object-fit:cover}@media(max-width:680px){.kg-bookmark-thumbnail {flex-basis:130px}.kg-bookmark-description {-webkit-line-clamp:1}}
</style>
<main class="kg-card-main"><div class="kg-bookmark-card"><a class="kg-bookmark-container" href="https://www.bilibili.com/video/BV1rM4y1G7Uz/?spm_id_from=333.337.search-card.all.click&amp;vd_source=42bec97100a0d831cda9a1c7895b2cb1](https://www.bilibili.com/video/BV1rM4y1G7Uz/?spm_id_from=333.337.search-card.all.click&amp;vd_source=42bec97100a0d831cda9a1c7895b2cb1"><div class="kg-bookmark-content"><div class="kg-bookmark-title">（概率论必看）结合图形解决一维连续性随机变量的分布函数和概率密度_哔哩哔哩_bilibili</div><div class="kg-bookmark-description">-, 视频播放量 82597、弹幕量 292、点赞数 2784、投硬币枚数 2387、收藏人数 2800、转发人数 446, 视频作者 吃尽天下面, 作者简介 工科考研生21数一148，随缘更新一些考研数学视频～，相关视频：（概率论必看）卷积法求解简单二维连续型随机变量函数的概率密度，【概率救命】一期视频拿捏概率，听完就会！，【数学一 已完结】2027李林880题逐题精讲 超细致 By 没咋了、吃尽天下面，伽马函数，你必须得会，【概率救命#2】专治一维随机变量&quot;恐惧症&quot; 考研冲刺上大分，图像法，真正爆杀随机变量函数的分布，【概率论与数理统计】7小时轻松通关，【概率救命#1】用顶级思维带你拿下随机事件和概率 考研冲刺上大分，考研数学K妈深夜课堂变KTV吟唱，精神状态美丽，数一148学长个人复习经验分享</div><div class="kg-bookmark-metadata"><img class="kg-bookmark-icon" src="https://i0.hdslb.com/bfs/static/jinkela/long/images/favicon.ico" alt=""><span>哔哩哔哩</span></div></div><div class="kg-bookmark-thumbnail"><img src="https://i1.hdslb.com/bfs/archive/0cf8a6b9fa77f15eafcecf53c94c4fa6d1f4433b.jpg@1200w_630h" alt=""></div></a></div></main>
</div>

　　随机变量 $X$ 的概率密度为 $f_X(x)$，$Y=g(X)$（$y=g(x)$ 为连续函数），求 $Y$ 的概率分布。

　　**方法：分布函数法**

$$
F_Y(y)=P(Y \le y)=P\{g(X)\le y\}=\int_{g(X)\le y} f_X(x)\mathrm{d}x
$$

　　得到分布函数 $F_Y(y)$ 之后，对 $y$ 求导得到概率密度：

$$
\boldsymbol{f_Y(y)=F_Y'(y)}
$$

![cdb4eb5138cfe91503b23905001f017e](https://siyuan-image-1330022534.cos.ap-shanghai.myqcloud.com/siyuan/cdb4eb5138cfe91503b23905001f017e-20260830201705-k77ctl9.jpg)

　　‍

[^1]: # 例题：求随机变量的分布函数

    ## 一、题目

    假设随机变量 $X$ 的绝对值不大于 $1$，且

    $$
    P\{X=-1\}=\frac18
    $$

    $$
    P\{X=1\}=\frac14
    $$

    在事件 $\{-1<X<1\}$ 出现的条件下，$X$ 在 $(-1,1)$ 内的任一子区间上取值的条件概率与该子区间长度成正比。

    求 $X$ 的分布函数 $F(x)$。

    ---

    # 二、第一步：确定 $X$ 的取值范围

    由题意：

    $$
    |X|\le1
    $$

    因此：

    $$
    -1\le X\le1
    $$

    所以 $X$ 的取值范围为：

    $$
    [-1,1]
    $$

    可以把它分成三个部分：

    $$
    \boxed{
    \{-1\},\quad (-1,1),\quad \{1\}
    }
    $$

    其中：

    - $X=-1$：有一个离散概率 $\frac18$
    - $-1<X<1$：连续取值
    - $X=1$：有一个离散概率 $\frac14$

    因此，这道题本质上是一个：

    > **离散部分 + 连续部分的混合分布**
    >

    ---

    # 三、第二步：求中间连续部分的总概率

    因为 $X$ 一定落在 $[-1,1]$ 内：

    $$
    P(-1\le X\le1)=1
    $$

    将 $[-1,1]$ 分成三个互不相交的部分：

    $$
    \{X=-1\}\cup\{-1<X<1\}\cup\{X=1\}
    $$

    因此：

    $$
    P(X=-1)+P(-1<X<1)+P(X=1)=1
    $$

    代入已知概率：

    $$
    \frac18+P(-1<X<1)+\frac14=1
    $$

    所以：

    $$
    P(-1<X<1)
    =
    1-\frac18-\frac14
    $$

    $$
    \boxed{
    P(-1<X<1)=\frac58
    }
    $$

    这说明：

    > $X$ 有 $\frac58$ 的概率落在中间的连续区间 $(-1,1)$ 内。
    >

    ---

    # 四、第三步：理解“与子区间长度成正比”

    题目说：

    > 在事件 $\{-1<X<1\}$ 出现的条件下，$X$ 在 $(-1,1)$ 内的任一子区间上取值的条件概率与该子区间长度成正比。
    >

    设：

    $$
    -1<a<b<1
    $$

    那么区间 $(a,b)$ 的长度为：

    $$
    b-a
    $$

    题目告诉我们：

    $$
    P(a<X<b\mid -1<X<1)
    \propto b-a
    $$

    也就是说：

    > **在已知** **$X$** **落在** **$(-1,1)$** **内的条件下，**​**$X$** **在这个区间内均匀分布。**
    >

    因为 $(-1,1)$ 的总长度为：

    $$
    1-(-1)=2
    $$

    所以条件概率为：

    $$
    \boxed{
    P(a<X<b\mid -1<X<1)
    =
    \frac{b-a}{2}
    }
    $$

    这实际上就是：

    $$
    X\mid(-1<X<1)\sim U(-1,1)
    $$

    ---

    # 五、第四步：求整体的概率密度

    注意：

    $$
    \frac12
    $$

    只是**条件密度**，不是 $X$ 整体的密度。

    由条件概率公式：

    $$
    P(A\mid B)=\frac{P(A\cap B)}{P(B)}
    $$

    所以：

    $$
    P(A\cap B)=P(A\mid B)P(B)
    $$

    对于 $-1<a<b<1$：

    $$
    P(a<X<b)
    =
    P(a<X<b\mid-1<X<1)
    P(-1<X<1)
    $$

    代入：

    $$
    P(a<X<b)
    =
    \frac{b-a}{2}\cdot\frac58
    $$

    得到：

    $$
    \boxed{
    P(a<X<b)=\frac5{16}(b-a)
    }
    $$

    而连续型随机变量满足：

    $$
    P(a<X<b)=\int_a^b f(x)\,dx
    $$

    因此中间部分的概率密度为：

    $$
    \boxed{
    f(x)=\frac5{16},\qquad -1<x<1
    }
    $$

    ---

    # 六、第五步：求分布函数 $F(x)$

    分布函数的定义：

    $$
    \boxed{
    F(x)=P(X\le x)
    }
    $$

    求分布函数最重要的方法：

    > **按照** **$x$** **所处的位置进行分段讨论。**
    >

    本题的关键分界点是：

    $$
    \boxed{-1,\quad1}
    $$

    因此分成三种情况。

    ---

    ## 情况一：$x<-1$

    因为 $X$ 最小只能取到 $-1$。

    所以：

    $$
    P(X\le x)=0
    $$

    因此：

    $$
    \boxed{
    F(x)=0,\qquad x<-1
    }
    $$

    ---

    ## 情况二：$-1\le x<1$

    此时：

    $$
    F(x)=P(X\le x)
    $$

    需要把左端点的离散概率和连续部分的概率都算进去。

    ### ① 左端点 $X=-1$

    因为 $-1\le x$：

    $$
    P(X=-1)=\frac18
    $$

    ### ② 连续部分 $-1<X\le x$

    连续部分的概率密度为：

    $$
    f(t)=\frac5{16}
    $$

    所以：

    $$
    P(-1<X\le x)
    =
    \int_{-1}^{x}\frac5{16}\,dt
    $$

    计算得：

    $$
    P(-1<X\le x)
    =
    \frac5{16}(x+1)
    $$

    ### ③ 两部分相加

    因此：

    $$
    F(x)
    =
    \frac18+\frac5{16}(x+1)
    $$

    整理：

    $$
    \boxed{
    F(x)=\frac{5x+7}{16},
    \qquad -1\le x<1
    }
    $$

    ---

    ## 情况三：$x\ge1$

    此时 $X$ 的所有可能取值都已经包含在 $X\le x$ 中。

    所以：

    $$
    F(x)=1
    $$

    因此：

    $$
    \boxed{
    F(x)=1,\qquad x\ge1
    }
    $$

    ---

    # 七、最终答案

    综上，$X$ 的分布函数为：

    $$
    \boxed{
    F(x)=
    \begin{cases}
    0, & x<-1,\\[6pt]
    \dfrac18+\dfrac5{16}(x+1), & -1\le x<1,\\[8pt]
    1, & x\ge1.
    \end{cases}
    }
    $$

    也可以写成：

    $$
    \boxed{
    F(x)=
    \begin{cases}
    0, & x<-1,\\[6pt]
    \dfrac{5x+7}{16}, & -1\le x<1,\\[8pt]
    1, & x\ge1.
    \end{cases}
    }
    $$

    ---

    # 八、结果检查

    ## 1. 检查 $x=-1$ 处

    分布函数应该满足：

    $$
    F(-1)=P(X\le-1)
    $$

    而只有 $X=-1$：

    $$
    F(-1)=P(X=-1)=\frac18
    $$

    代入中间表达式：

    $$
    F(-1)=\frac{5(-1)+7}{16}
    =\frac2{16}
    =\frac18
    $$

    正确。

    ---

    ## 2. 检查 $x=1$ 左极限

    当 $x\to1^-$ 时：

    $$
    F(1^-)
    =
    \frac{5(1)+7}{16}
    =
    \frac{12}{16}
    =
    \frac34
    $$

    这表示：

    $$
    P(X<1)=\frac34
    $$

    而：

    $$
    P(X=1)=\frac14
    $$

    因此：

    $$
    F(1)=P(X\le1)
    =
    \frac34+\frac14
    =1
    $$

    正确。

    所以在 $x=1$ 处存在一个大小为：

    $$
    \boxed{\frac14}
    $$

    的跳跃。

    ---

    # 九、这道题最核心的理解

    这道题最容易混淆的是：

    $$
    \boxed{\frac12}
    $$

    和

    $$
    \boxed{\frac5{16}}
    $$

    的区别。

    ### $\frac12$ 是什么？

    它是**条件密度**。

    因为在已经知道：

    $$
    -1<X<1
    $$

    的条件下，$X$ 在长度为 $2$ 的区间 $(-1,1)$ 上均匀分布。

    所以：

    $$
    f_{X\mid -1<X<1}(x)=\frac12
    $$

    ---

    ### $\frac5{16}$ 是什么？

    它是 $X$ **整体在** **$(-1,1)$** **上的概率密度**。

    因为只有：

    $$
    \frac58
    $$

    的概率进入中间连续区域。

    因此：

    $$
    \frac58\times\frac12
    =
    \frac5{16}
    $$

    所以：

    $$
    \boxed{
    \text{整体密度}
    =
    \text{连续部分总概率}
    \times
    \text{条件密度}
    }
    $$

    即：

    $$
    \boxed{
    \frac5{16}
    =
    \frac58\times\frac12
    }
    $$

    ---

    # 十、考研做题模板

    以后遇到这种“求分布函数 + 区间长度成正比”的题，可以直接按照下面的模板做。

    ### Step 1：确定取值范围

    根据题目确定：

    $$
    a\le X\le b
    $$

    ---

    ### Step 2：求连续部分总概率

    如果题目给出了若干离散点概率：

    $$
    P(\text{连续部分})
    =
    1-\sum P(\text{离散点})
    $$

    ---

    ### Step 3：判断连续部分是否均匀

    如果题目说：

    > 区间上的概率与区间长度成正比
    >

    那么直接判断：

    $$
    \boxed{\text{条件均匀分布}}
    $$

    若连续区间长度为 $L$，则条件密度：

    $$
    \boxed{\frac1L}
    $$

    ---

    ### Step 4：求整体密度

    $$
    \boxed{
    \text{整体密度}
    =
    \text{连续部分总概率}
    \times
    \text{条件密度}
    }
    $$

    ---

    ### Step 5：根据 $F(x)=P(X\le x)$ 分段

    通常按照：

    $$
    \boxed{
    \text{取值范围的端点 + 离散点}
    }
    $$

    进行分段。

    ---

    ### Step 6：离散点要单独加进去

    如果某个离散点 $x_0$ 满足：

    $$
    P(X=x_0)>0
    $$

    那么求 $F(x)$ 时一定注意：

    $$
    F(x)=P(X\le x)
    $$

    所以当 $x\ge x_0$ 时，要把：

    $$
    P(X=x_0)
    $$

    加进去。

    ---

    # 十一、一句话记忆

    > **先分清“条件概率”和“整体概率”：先算连续部分占多少，再利用“与长度成正比”得到条件均匀分布，最后把连续部分和离散点一起塞进** **$F(x)=P(X\le x)$**​ **。**
    >

    本题核心链条：

    $$
    \boxed{
    \frac18,\frac14
    \rightarrow
    P(-1<X<1)=\frac58
    \rightarrow
    \text{条件密度}=\frac12
    \rightarrow
    \text{整体密度}=\frac5{16}
    \rightarrow
    F(x)
    }
    $$

    ‍
