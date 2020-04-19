---
layout: post
title: "BCD"
date: 2020-04-13 13:57:53 +0100
categories: Codes
---

**Excess-3** code is [reflective]({% post_url 2020-04-14-basic-coding-and-codes %}) or [self complemented]({% post_url 2020-04-14-basic-coding-and-codes %}), but **Excess-3** code is classified as [sequential]({% post_url 2020-04-14-basic-coding-and-codes %}), and [non weighted]({% post_url 2020-04-14-basic-coding-and-codes %})

**Excess-3** code is used to express decimal numbers. **Excess-3** code is useful for arithmetics because it overcomes shortcomings of **BDC** in adding numbers that are greater than `9`.

| Excess-3 | Decimal | BCD  |
|----------|---------|------|
| 0011     | 0       | 0000 |
| 0100     | 1       | 0001 |
| 0101     | 2       | 0010 |
| 0110     | 3       | 0011 |
| 0111     | 4       | 0100 |
| 1000     | 5       | 0101 |
| 1001     | 6       | 0110 |
| 1010     | 7       | 0111 |
| 1011     | 8       | 1000 |
| 1100     | 9       | 1001 |
|----------|---------|------|

Easy way to covert **decimal** number into **Excess-3** code is to add `3` to it and then convert it into **Binary**

{% highlight ruby %}

20 (base 10) =>

2 + 3 = 5
0 + 3 = 3

5 => 0101
3 => 0011

Excess-3 => 0101 0011

{% endhighlight %}