---
layout:     post                    # 使用的布局（不需要改）
title:      reduce Chebyshev to LP            # 标题 
subtitle:   Convex Optimization(Stephen_Boyd) study note  #副标题
date:       2019-04-24              # 时间
author:     羽聪                      # 作者
header-img: img/convex1.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - convex optimization
    - campus
---

### Chebyshev approximation to LP
\textbf{Chebyshev approximation:}\\
$$\text{minimize}\quad max_{x=1,...,k}|a_{i}^{T}x-b_i|$$.

It can be converted to a LP problem, which is

$$\begin{align*} \text{minimize} &\quad t\\ \text{subject to} &\quad a_{i}^{T}x-t\le b_i, i=1,...k\\&-a_{i}^{T}x-t\le -b_{i}, i= 1,...,k\end{align*}$$
