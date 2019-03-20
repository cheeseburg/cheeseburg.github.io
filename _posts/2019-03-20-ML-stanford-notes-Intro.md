---
layout:     post                    # 使用的布局（不需要改）
title:      Introduction to ML(notes)              # 标题 
subtitle:   Andrew Ng, Stanford  #副标题
date:       2019-03-20              # 时间
author:     羽聪                      # 作者
header-img: img/PublicSpeaking_midterm_post.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - machine learning
    - campus
---

### Supervised learning(ML Stanford Lecture 1.2)

---
#### Example 1

![pic 1](https://github.com/cheeseburg/cheeseburg.github.io/tree/master/img/ML/1553062754689.png)

![pic 2](https://github.com/cheeseburg/cheeseburg.github.io/tree/master/img/ML/1553062819359.png)

"right answers" given

​	Regression: Predict continuous valued output(price)

#### Example 2

![pic 3](https://github.com/cheeseburg/cheeseburg.github.io/tree/master/img/ML/1553063006612.png)

![pic 4](https://github.com/cheeseburg/cheeseburg.github.io/tree/master/img/ML/1553063295981.png)

### Unsupervised Learning

---

#### Cocktail party problem algorithm

```octave
[W,s,v] = svd((repmat(sum(s.*x,1),size(x,1),1).*x)*x')
```
