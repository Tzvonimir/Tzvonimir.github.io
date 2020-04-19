---
layout: post
title:  "Basic logic gates"
date:   2019-01-06 22:57:53 +0100
categories: Logic gates
---

A logic gate is an elementary building block of a digital circuit. Most logic gates have two inputs and only one output. At every moment input or output is one of the two [binary]({% post_url 2018-12-30-basic-binary %}) conditions, `1` or a `0`, represented by different voltage levels `+5 V` represents `1` and `0 V` represents `0`.

There are seven basic logic gates:
* AND
* OR
* NOT
* XOR
* NAND
* NOR
* XNOR

**AND**

![and-gate]({{ site.url }}/img/and.jpg){:class="img-responsive"}

| A | B | AB |
|---|---|----|
| 0 | 0 | 0  |
| 0 | 1 | 0  |
| 1 | 0 | 0  |
| 1 | 1 | 1  |
|---|---|----|

**OR**

![or-gate]({{ site.url }}/img/or.jpg){:class="img-responsive"}

| A | B | A+B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 1   |
|---|---|-----|

**NOT**

![not-gate]({{ site.url }}/img/not.jpg){:class="img-responsive"}

| A | A'  |
|---|-----|
| 0 | 1   |
| 1 | 0   |
|---|-----|

**XOR**

![xor-gate]({{ site.url }}/img/xor.jpg){:class="img-responsive"}

| A | B | A⊕B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

**NAND**

![nand-gate]({{ site.url }}/img/nand.jpg){:class="img-responsive"}

| A | B | AB' |
|---|---|-----|
| 0 | 0 | 1   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

**NOR**

![nor-gate]({{ site.url }}/img/nor.jpg){:class="img-responsive"}

| A | B | A+B' |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 0    |
|---|---|------|

**XNOR**

![xnor-gate]({{ site.url }}/img/xnor.jpg){:class="img-responsive"}

| A | B | A⊕B' |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 1    |
|---|---|------|