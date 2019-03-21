---
layout:     post                    # 使用的布局（不需要改）
title:      multiple integer problem(1) --- integer             # 标题 
subtitle:   from Huawei  #副标题
date:       2019-03-21              # 时间
author:     羽聪                      # 作者
header-img: img/equation.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - algorithm
    - python
---

### Equation Transformation

---

输入一个正整数X，在下面的等式左边的数字之间添加+号或者-号，使得等式成立。

Given a positive integer X, add '+' or '-' to satisfy the following equation.

`1 2 3 4 5 6 7 8 9 = X`
For example：

- 1. `12-34+5-67+89 = 5` 
  2. `1+23+4-5+6-7-8-9 = 5`

Please write codes to calculate the total # of solutions.

​	input: integer, eg. 5

​	output: the # of solutions, eg. 21



Sample Code:

```python
class counter(object):
	"""docstring for counter"""
	def __init__(self, i):
		super(counter, self).__init__()
		self.cnt = i
	def add(self):
		self.cnt += 1

def combine(l, i, j, res=0):
	while i <= j:
		res = res*10 + l[i]
		i += 1
	return res


def cnt(l, n, s, c):
	if n > 0:
		for k in range(n, -1, -1):
			if k != 0:
				cnt(l, k-1, s-combine(l, k, n), c)
				cnt(l, k-1, s+combine(l, k, n), c)
			elif k == 0 and s == combine(l, 0, n):
				c.add()
				return c.cnt
	elif n == 0:
		if s == l[0]:
			c.add()
	return c.cnt


if __name__ == '__main__':
	c = counter(0)
	l = [i for i in range(1,10)]
	print(cnt(l, 8, 5, c))

```

