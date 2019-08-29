---
layout:     post                    # 使用的布局（不需要改）
title:      CS243 final cheatsheet            # 标题 
subtitle:   algorithm game theory  #副标题
date:       2019-08-29              # 时间
author:     羽聪                      # 作者
header-img: img/algo_sheet.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - game theory
    - campus
---

[TOC]

# CS243 Final Cheatsheet

## Basic concepts

### Nash equilibrim and dominant strategy

1. A dominant strategy is always a Nash equilibrium.
2. ![1557645214150](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645214150.png)
3. ![1557645250120](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645250120.png)



## Auction Design

### Second Price Auction(Vickery Auction)

------

### Truthfulness(IC)

![1557645479723](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645479723.png)

------

### How to verify a mechanism is truthful?

![1557646395423](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557646395423.png)

------

### Vickrey–Clarke–Groves Mechanisms

![1557645617710](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645617710.png)

------

### An example proof of truthfulness

**Prove that VCG mechanism is IC.**

![1557645737269](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645737269.png)

------

### Clarke Pivot Rule

![1557645902943](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645902943.png)

![1557646587433](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557646587433.png)

![1557645944555](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557645944555.png)

------

### Efficiency

![1557646617254](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557646617254.png)

```
1. Is the second price auction efficient? Yes!
2. Is the first price auction efficient? Yes!
3. Is fixed price auction efficient? No!
```

------

### Individual Rationality

```
1. No negative utility.
2. Is the second price auction individually rational? Yes!
3. Is the first price auction individually rational? Yes!
4. Is fixed price auction individually rational? Yes!
```



## Social Choice

### Voting Methods

![1557648486375](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557648486375.png)

------

### Truthful Social Choice Function

![1557649407099](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557649407099.png)

![1557649393414](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557649393414.png)

------

### Unanimity, Dictator, Independence of irrelevant alternatives

![1557648769957](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557648769957.png)

------

### Dictatorship

![1557649067156](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557649067156.png)

------

### Arrow's Theorem

![1557648729089](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557648729089.png)

------

### Gibbard–Satterthwaite Theorem

![1557649012985](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557649012985.png)



## Matching

### Serial dictationship

![1557650370885](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557650370885.png)

------

### Top Trading Cycle Mechanism

```
1. Each agent points to its most preferred house (allow
   self-edge).
2. Trade on cycles, agents and houses leave market.
3. Each remaining agent points to its most preferred, remaining house.
4. Repeat (#1, #2, #3), until no agents left.
```

------

### One-sided Matching

![1557650323972](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557650323972.png)

**Serial dictatorship mechanism is also optimal and truthful**

------

### Stable Matching

![1557649977498](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557649977498.png)

------

### Deferred Acceptance Algorithm, male-proposals

![1557650394926](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557650394926.png)

![1557650501320](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557650501320.png)

------

### Truthful Stable Matching

![1557650567129](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557650567129.png)

------

### Not truthful for colleges

![1557651474846](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557651474846.png)



## Single-Peaked Preference

![1557651971644](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557651971644.png)



## Cake Cutting

### Fairness

![1557652032542](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652032542.png)

------

































### An example

![1557652139429](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652139429.png)

![1557652169317](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652169317.png)



## Cooperative Games

![1557659705091](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557659705091.png)

------

### Core

![1557652313289](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652313289.png)

![1557652578367](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652578367.png)

------

### Is core always nonempty and unique?

![1557652645562](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652645562.png)

![1557652656611](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652656611.png)

------

### Shapley Value

![1557652533668](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652533668.png)

------

### Shapley Value Example

![1557652461733](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652461733.png)

------

### Properties of Shapley Value

![1557652721039](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557652721039.png)



## Cost Sharing

### Core of Cost Sharing Games

![1557660070486](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557660070486.png)



## Profit Maximization

### Virtual Valuation

![1557661647256](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557661647256.png)

------

### Virtual Surplus

![1557661660478](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557661660478.png)

------

### Expected Profit

![1557661715194](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557661715194.png)

- Therefore, to maximize the profit, we just need to maximize the expected virtual surplus (the social welfare under virtual valuation).

------

### Truthfulness of Virtual Surplus Maximization

![1557661846896](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557661846896.png)

------

### Myerson’s Optimal Auction

![1557662048435](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557662048435.png)

![1557662489536](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557662489536.png)



## Sponsored Search Auction

### Basic Model

![1557662616684](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557662616684.png)

![1557662650599](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557662650599.png)

------

### Efficiency in a Static Setting

![1557662702085](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557662702085.png)



## Bayesian-Nash Equilibrium

![1557663149877](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557663149877.png)



## First Price Auction

![1557663732270](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557663732270.png)

![1557663747870](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557663747870.png)

![1557663759650](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557663759650.png)



## The Revenue Equivalence Principle

### *First Price Auction Versus Second Price Auction*

![1557664122599](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557664122599.png)

![1557663861188](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557663861188.png)

![1557664049718](C:\Users\cheeseburg\AppData\Roaming\Typora\typora-user-images\1557664049718.png)

