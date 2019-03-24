---
layout:     post                    # 使用的布局（不需要改）
title:      CVX Problems             # 标题 
subtitle:   Basis Pursuit to LP  #副标题
date:       2019-03-24              # 时间
author:     羽聪                      # 作者
header-img: img/convex1.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - convex optimization
    - campus
---

### Basis Pursuit to LP

Consider  the following compressive sensing problem via $\ell_1$-minimization 
$$
\begin{equation}
		\begin{aligned}
		        \mathop {\rm{minimize}}_{{x}\in\mathbb{R}^d}\quad & \|{x}\|_1  \\
		         \rm{subject~to} \quad & {Ax} = {z}.
		\end{aligned}
		\end{equation}
$$
The term $ {\left\| x \right\|}_{1} $ can written in element wise form:

$$ {\left\| x \right\|}_{1} = \sum_{i = 1}^{n} \left| {x}_{i} \right| $$

Then setting $ \left| {x}_{i} \right| \leq {t}_{i} $ one could write:

$$
\begin{align*}
\arg \min_{x,t} \: & \: \boldsymbol{1}^{T} t \\
\text{subject to} \: & \: A x = b \\
& \: \left| {x}_{i} \right| \leq {t}_{i} \; \forall i
\end{align*}
$$

Since $ \left| {x}_{i} \right| \leq {t}_{i} \iff {x}_{i} \leq {t}_{i}, \, {x}_{i} \geq -{t}_{i} $ then:

$$
\begin{align*}
\arg \min_{x,t} \: & \: \boldsymbol{1}^{T} t \\
\text{subject to} \: & \: A x = b \\
& \: {x}_{i} \leq {t}_{i} \; \forall i \\
& \: {x}_{i} \geq -{t}_{i} \; \forall i
\end{align*}
$$

Which can be farther refined:

$$
\begin{align*}
\arg \min_{x,t} \: & \: \boldsymbol{1}^{T} t \\
\text{subject to} \: & \: A x = b \\
& \: I x - I t \preceq \boldsymbol{0} \\
& \: -I x - I t \preceq \boldsymbol{0}
\end{align*}
$$

Which is a Linear Programming problem.
