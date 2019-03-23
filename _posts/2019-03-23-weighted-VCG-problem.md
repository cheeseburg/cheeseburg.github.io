---
layout:     post                    # 使用的布局（不需要改）
title:      Weighted VCG Problem             # 标题 
subtitle:   Yucong Zhang, SIST  #副标题
date:       2019-03-21              # 时间
author:     羽聪                      # 作者
header-img: img/chessboard.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - Game Theory
    - Campus
---

### Weighted VCG Problem

A mechanism (f, p1, ... , pn) is called a weighted VCG mechanism if

- $f(v_{1},v_{2},...,v_{n})\in arg\mathop\max_{a\in A}(c_{a}+\sum_{i}w_{i}v_{i}(a))$, where $c_{a},w_{1},...w_{n}\in R^{+}$
- for some functions $h_{1},...,h_{n}$, where $h_{i}$ : $V_{-i} \to R$, we have that for all $v_{1}\in V_{1}, ..., v_{n}\in V_{n}$:

$$
p_{i}(v_{1},...,v_{n})=h_{i}(v_{-i})-\frac{c_{a}}{w_{i}}-\sum_{j\ne i}(\frac{w_{j}}{w_{i}})v_{j}(a)
$$

#### Proof
---
Denote $a=f(v_{i},v_{-i})$ and $a'=f(v_{i}',v_{-i})$.
By reporting $v_{i}$, 
$$
\begin{align}
    u_{i}&=v_{i}(a)-p_{i}(v_{i},v_{-i})\\
    &=v_{i}(a)+\sum_{j\ne i}(\frac{w_{j}}{w_{i}})v_{j}(a)+\frac{c_{a}}{w_{i}}-h(v_{-i})
\end{align}
$$
And by reporting $v_{i}'$,
$$
\begin{align}
    u_{i}'&=v_{i}(a')-p_{i}(v_{i}',v_{-i})\\
    &=v_{i}(a')+\sum_{j\ne i}(\frac{w_{j}}{w_{i}})v_{j}(a)+\frac{c_{a'}}{w_{i}}-h(v_{-i})
\end{align}
$$
Then $(2)\times w_{i}-(4)\times w_{i}$, we have
$$
u_{i}\times w_{i}-u_{i}'\times w_{i} = c_{a} + \sum w_{i}v_{i}(a)-c_{a'}+\sum w_{i}v_{i}(a')
$$
And since $a\in argmin_{a \in A}[c_{a}+\sum w_{i}v_{i}(a)]$, the above equation will always greater than zero.\\
Hence, weighted VCG is IC.