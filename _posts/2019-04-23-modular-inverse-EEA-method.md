---
layout:     post                    # 使用的布局（不需要改）
title:      RSA（Cryptosystem）            # 标题 
subtitle:   modular inverse&EEA(from wikibooks)  #副标题
date:       2019-04-23              # 时间
author:     羽聪                      # 作者
header-img: img/RSA(1).jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - cryptology
    - campus
---

### Key generation

The keys for the RSA algorithm are generated the following way:

1. Choose two distinct prime numbers p and q.
   - For security purposes, the integers *p* and *q* should be chosen at random, and should be similar in magnitude but differ in length by a few digits to make factoring harder. Prime integers can be efficiently found using a [primality test](https://en.wikipedia.org/wiki/Primality_test).
2. Compute *N* = *pq*.
   - *N* is used as the [modulus](https://en.wikipedia.org/wiki/Modular_arithmetic) for both the public and private keys. Its length, usually expressed in bits, is the [key length](https://en.wikipedia.org/wiki/Key_length).
3. Compute *λ*(*n*) = [lcm](https://en.wikipedia.org/wiki/Least_common_multiple)(*φ*(*p*), *φ*(*q*)) = lcm(*p* − 1, *q* − 1), where *λ* is [Carmichael's totient function](https://en.wikipedia.org/wiki/Carmichael%27s_totient_function). This value is kept private. (i.e.(p-1)(q-1))
4. Choose an integer *e* such that 1 < *e* < *λ*(*n*) and gcd(*e*, *λ*(*n*)) = 1; i.e., *e* and *λ*(*n*) are coprime.
5. Determine *d* as *d* ≡ *e*−1 (mod *λ*(*n*)); i.e., *d* is the modular multiplicative inverse of *e* modulo *λ*(*n*).

The *public key* consists of the modulus *n* and the public (or encryption) exponent *e*. The *private key* consists of the private (or decryption) exponent *d*, which must be kept secret. *p*, *q*, and *λ*(*n*) must also be kept secret because they can be used to calculate *d*.

```python
'''step 4'''
def xgcd(a, b):
    """return (g, x, y) such that a*x + b*y = g = gcd(a, b)"""
    x0, x1, y0, y1 = 0, 1, 1, 0
    while a != 0:
        q, b, a = b // a, a, b % a
        y0, y1 = y1, y0 - q * y1
        x0, x1 = x1, x0 - q * x1
    return b, x0, y0

'''step 5'''
def mulinv(a, b):
    """return x such that (x * a) % b == 1"""
    g, x, _ = xgcd(a, b)
    if g == 1:
        return x % b

if __name__ == '__main__':
    '''step 1'''
    p, q = int(input("Give a large prime p: ")), int(input("Give another large prime q: "))
    
    '''step 2'''
    N = p*q
    
    '''step 3'''
	phi=(p-1)*(q-1) # Euler function
	e= int(input("e: ")) # 1<e<phi
    
    '''the mulinv() function contains step 4 and step 5'''
    d = mulinv(e, phi) # modular inverse of e
	print("e's modular inverse is {}".format(d))
    
    '''(N, e) is public key, (N, d) is private key. 
    	Note that p,q,phi are also private'''
    
    # EEA part below
    # convert d to binary
	d = str(bin(d))[2:]
	cnt = len(d) # number of xs
	res, x = 1, c
	for i in range(1, cnt+1):
		if eval(d[-i]) == 1:
			res = res*x*eval(d[-i])
			x = (x*x)%N

	print(res%N)

```

---

Sample input:

```py
p=6703903964971298549787012499102923063739682910296196688861780721860882015036773488400937149083451713845015929093243025426876941405973284973216824503042159
```
```py
q=6703903964971298549787012499102923063739682910296196688861780721860882015036773488400937149083451713845015929093243025426876941405973284973216824503042857
```
```py
N=44942328371557897693232629769725618340449424473557664318357520289433168951375240783177119330601884005280028469967848339414697442203604155623211857659874698686089746950882175370574729589530164038140743238975004280473649682039449551977807139812363584867575042325912358143379538270713424498384198560948854808263
```
```py
e=96369814566225467924653014805513492896964134518515264524627861474879778069831660663897677046727957192703934803972250616430609259595745097617769926942112134367594307837488500988473653982226257757541106532514633452399397504073793231177982720744337722569856046005247772492366591236471725562440735800298613269
```
```py
c=2891727949404584416984483039628011793418731724707010912459311103904063699345063990602821823945679515706022741850211764083405982592172753137941011321836731232557083320397234166409780292554150125902007953546388941791826672419571635549151361562690084861544977890629208820465212228909954211513216097290151297004
```

Sample output:

```py
6136879889769859843339301577722997182129868587887339753139901763514760694081149936516473057997760974158492171629633020715475369567035610830146744067879776431874619734155216204780204580420829619502974882298285138907824168798040820980303720180842260785479653907965557599613852706558767393952982716800255288174
```

