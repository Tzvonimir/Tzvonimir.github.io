---
layout: post
title: "Universal logic gates"
date: 2020-04-10 22:57:53 +0100
categories: Logic gates
---

Any logic gate which can create all other logical functions is **Universal logic gate**.

There are three different sets or categories we can use to classify universal logic gates:

* Full Set
* Complete Set
* Minimal Set

<div class="table-wrapper" markdown="block">

| Full set     | Complete set | Minimal Set |
|--------------|--------------|-------------|
| AND, OR, NOT | AND, NOT     | NAND        |
|              | OR, NOT      |             |
|--------------|--------------|-------------|

</div>

All sets can create a different range or Boolean functions, but logical gates in **Minimal set** have a build-in property to create all the boolean functions by themselves.

So let’s try to define all the basic logic gates using only **Universal logical gates** from **Minimal set**

**NAND Universal gate transformations**

**NAND GATE**

![nand-gate]({{ site.url }}/img/universal/NAND.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | AB’ |
|---|---|-----|
| 0 | 0 | 1   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

</div>

**NAND TO AND**

![and-gate]({{ site.url }}/img/universal/NAND->AND.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | AB |
|---|---|----|
| 0 | 0 | 0  |
| 0 | 1 | 0  |
| 1 | 0 | 0  |
| 1 | 1 | 1  |
|---|---|----|

</div>

**NAND TO OR**

![or-gate]({{ site.url }}/img/universal/NAND->OR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A+B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 1   |
|---|---|-----|

</div>

**NAND TO NOT**

![not-gate]({{ site.url }}/img/universal/NAND->NOT.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | A’|
|---|---|
| 0 | 1 |
| 1 | 0 |
|---|---|

</div>

**NAND TO XOR**

![xor-gate]({{ site.url }}/img/universal/NAND->XOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A⊕B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

</div>

**NAND TO NOR**

![nor-gate]({{ site.url }}/img/universal/NAND->NOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A+B’ |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 0    |
|---|---|------|

</div>

**NAND TO XNOR**

![xnor-gate]({{ site.url }}/img/universal/NAND->XNOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A⊕B’ |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 1    |
|---|---|------|

</div>

**NOR Universal gate transformations**

**NOR**

![nor-gate]({{ site.url }}/img/universal/NOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A+B’ |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 0    |
|---|---|------|

</div>

**NOR TO AND** 

![and-gate]({{ site.url }}/img/universal/NOR->AND.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | AB |
|---|---|----|
| 0 | 0 | 0  |
| 0 | 1 | 0  |
| 1 | 0 | 0  |
| 1 | 1 | 1  |
|---|---|----|

</div>

**NOR TO OR** 

![or-gate]({{ site.url }}/img/universal/NOR->OR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A+B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 1   |
|---|---|-----|

</div>

**NOR TO NOT**

![not-gate]({{ site.url }}/img/universal/NOR->NOT.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | A’ |
|---|----|
| 0 | 1  |
| 1 | 0  |
|---|----|

</div>

**NOR TO XOR**

![xor-gate]({{ site.url }}/img/universal/NOR->XOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A⊕B |
|---|---|-----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

</div>

**NOR TO NAND** 

![nand-gate]({{ site.url }}/img/universal/NOR->NAND.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | AB’ |
|---|---|-----|
| 0 | 0 | 1   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 0   |
|---|---|-----|

</div>

**NOR TO XNOR**

![xnor-gate]({{ site.url }}/img/universal/NOR->XNOR.png){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | A⊕B’ |
|---|---|------|
| 0 | 0 | 1    |
| 0 | 1 | 0    |
| 1 | 0 | 0    |
| 1 | 1 | 1    |
|---|---|------|

</div>