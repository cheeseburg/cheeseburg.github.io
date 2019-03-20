---
layout:     post                    # 使用的布局（不需要改）
title:      Introduction to ML(notes)              # 标题 
subtitle:   Andrew Ng, Stanford  #副标题
date:       2019-03-10              # 时间
author:     羽聪                      # 作者
header-img: img/PublicSpeaking_midterm_post.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - machine learning
    - campus
---

### Supervised learning(ML Stanford Lecture 1.2)

---
$\textbf{Example 1}$

![pic 1](img\ML\1553062754689.png)

![pic 2](img\ML\1553062819359.png)

"right answers" given

​	Regression: Predict continuous valued output(price)

$\textbf{Example 2}$

![pic 3](img\ML\1553063006612.png)

![pic 4](img\ML\1553063295981.png)

### Unsupervised Learning

---

#### Cocktail party problem algorithm

```octave
[W,s,v] = svd((repmat(sum(s.*x,1),size(x,1),1).*x)*x')
```