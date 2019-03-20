---
layout:     post                    # 使用的布局（不需要改）
title:      Linear regression with one variable(notes)              # 标题 
subtitle:   Andrew Ng, Stanford  #副标题
date:       2019-03-20              # 时间
author:     羽聪                      # 作者
header-img: img/ML.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - machine learning
    - campus
---

### Linear Regression with One Variable

---

![image](http://cheeseburg.tk/otherResources/ML_pics/1553073401650.png)

- Regression Problem
  - predict real-valued output

- Classification Problem
  - discrete-valued output

- Denote (x, y) to be one training example
- Denote ($x^{(i)}, y^{(i)}$) to be the ith training example

![image](http://cheeseburg.tk/otherResources/ML_pics/1553073887657.png)

#### How do we represent h?

linear regression with one variable = univariate linear regression

Hypothesis: $h_{\theta}(x) = \theta_{0}+\theta_{1}x$

#### Cost Function

How to choose $\theta_{0}$ and $\theta_{1}$?

​	Choose $\theta_{0}$ and $\theta_{1}$, s.t. $h_{\theta}(x)$ is close to y for our training examples$(x, y)$

Our goal $\rightarrow \mathop {minimize }\limits_{\theta_{0}\theta_{1}}\frac{1}{2m} \sum_{i=1}^{m}(h_{\theta}(x^{(i)})-y^{(i)})^{2}$, m is # of training examples

Denote $J(\theta_{0}, \theta_{1})=\frac{1}{2m} \sum_{i=1}^{m}(h_{\theta}(x^{(i)})-y^{(i)})^{2}$ $\rightarrow$ cost function

$\textit{Squred Error Function}$ = $\mathop{minimize}\limits_{\theta_{0},\theta_{1}} J(\theta_{0},\theta_{1})$ 

