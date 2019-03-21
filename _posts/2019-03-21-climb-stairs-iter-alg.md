---
layout:     post                    # 使用的布局（不需要改）
title:      Climbing Stairs Problem Algorithm              # 标题 
subtitle:   recusive method  #副标题
date:       2019-03-21              # 时间
author:     羽聪                      # 作者
header-img: img/stairs.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - algorithms
    - campus
---

### Climbing Stairs Problem

There are n stairs and suppose you are at the 0 stair. You can climb at most 3 stairs (i.e., 1 or 2 or 3 stairs) at each step, the problem is to compute the number of possible solutions to reach the nth stair.

#### Recursive Method

```python
def climbStairs_Recursive(n):
    '''Recurisve function to compute the number of solutions'''
    first3 = {1:1, 2:2, 3:4}
    if n in first3.keys():
        return first3[n]
    else:
        return climbStairs_Recursive(n-1) + \
               climbStairs_Recursive(n-2) + \
               climbStairs_Recursive(n-3)
```

#### non-Recursive Method

```python
def climbStairs_NonRecursive(n):
    '''Non-recurisve function to compute the number of solutions'''
    a = 1
    b = 2
    c = 4
    for i in range(n-3):
        c, b, a = a+b+c, c, b
    return c
```

