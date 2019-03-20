---
layout:     post                    # 使用的布局（不需要改）
title:      Linear regression with one variable(notes)              # 标题 
subtitle:   Andrew Ng, Stanford  #副标题
date:       2019-03-20              # 时间
author:     羽聪                      # 作者
header-img: img/PublicSpeaking_midterm_post.jpg    #这篇文章标题背景图片
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

![image](http://cheegit seburg.tk/otherResources/ML_pics/1553073887657.png)

#### How do we represent h?

linear regression with one variable = univariate linear regression

$h_{\theta}(x) = \theta_{0}+\theta_{1}x$