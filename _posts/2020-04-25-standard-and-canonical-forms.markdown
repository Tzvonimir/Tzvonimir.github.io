---
layout: post
title: "Standard and canonical forms"
date: 2020-04-25 13:57:53 +0100
categories: Boolean algebra
---
We get four boolean product terms by combining two variables x and y with
with logical AND operator. These Boolean product terms are called **min terms**
or **standard product terms**

`x'y', x'y, xy', xy`

But if we combine two variables x and y with logical OR operator we will get
Boolean sum terms called **max terms** or **standard sum terms**

<div class="table-wrapper" markdown="block">

| x | y | Min terms  | Max terms    |
|---|---|------------|--------------|
| 0 | 0 | m0 = x'y'  | M0 = x + y   |
| 0 | 1 | m1 = x'y   | M1 = x + y'  |
| 1 | 0 | m2 = xy'   | M2 = x' + y  |
| 1 | 1 | m3 = xy    | M3 = x' + y' |
|---|---|------------|--------------|

</div>

From table above we can see that min terms and max terms are complemetary.

And if there ar `n` Boolean variables, then there will be `2^n` min terms and
`2^n` max terms.

All boolean expressions regardles of their form can be converted into either
one of two standard forms **sum of product** and **product of sum**

**Canonical Sum of Product**

Canonical SoP or Canonical sum of product form. In this form, each product term
contains all literals (a single variable that may or may not be be complemented).
So these product terms are nothing but the min terms. So the canonical SoP can be
called **sum of min terms** form.

Canonical SoP expression:

` A'B'CD + AB'CD + ABCD `

**Example**

```

AB'C + A'B' + ABC'D

1. AB'C = AB'C(D+D')
        = AB'CD + AB'CD'
2. A'B' = A'B'(C+C') = A'B'C + A'B'C'
        = A'B'C(D+D') + A'B'C'(D+D')
        = A'B'CD + A'B'CD' + A'B'C'D + A'B'C'D'
3. ABC'D

= AB'CD + AB'CD' + A'B'CD + A'B'CD' + A'B'CD' + A'B'C'D + A'B'C'D' + ABC'D

```

**Canonical Product of Sum**

Canonical PoS or Canonical product of sum form. In this form, each product term
contains all literals (a single variable that may or may not be be complemented).
So these product terms are nothing but the max terms. So the canonical PoS can be
called **product of max terms** form.

Canonical PoS expression:

` (A' + B' + C + D)(A + B' + C + D)(A + B + C + D) `

**Example**

```

(A' + B + C)(B' + C + D')(A + B' + C' + D)

1. A' + B + C = A' + B + C + DD'
              = (A' + B + C + D)(A' + B + C + D')

2. B' + C + D' = B' + C + D' + AA'
               = (B' + C + D' + A)(B' + C + D + A')

3. A + B' + C' + D

= (A' + B + C + D)(A' + B + C + D')(A + B' + C + D')(A' + B' + C + D)(A + B' + C' + D)

```



**Standard Sum Of Product**

Standard SoP or **Standard Sum of Product** form. In this form each product
term doesn't have to contain all literals. So, the product terms can be in
**min terms** bit it doesn't have to. So we can say that standard SoP is
simplified form of of canonical SoP form.

We can get standard SoP by doing:

  * Get the canonical SoP form of output variables
  * Simplify Boolean function

**Example**

```

A'BC + AB'C + ABC' + ABC

1. Use X = X + 1 Boolean postulate

= A'BC + AB'C + ABC' + ABC + ABC + ABC

2. Use Distributive law (first with fourth | second with fifth | third with sixth)

= BC(A' + A) + AC(B' + B) + AB(C' + C)

3. Use Boolean postulate x + x' = 1

= BC1 + AC1 + AB1

4. Use Boolean postulate x1 = x

= BC + AC + AB

```

**Standard Product of Sum**

Standard PoS or **Standard Product of Sum** form. In this form each product
term doesn't have to contain all literals. So, the product terms can be in
**max terms** bit it doesn't have to. So we can say that standard PoS is
simplified form of of canonical PoS form.

We can get standard PoS by doing:

  * Get the canonical PoS form of output variables
  * Simplify Boolean function

```

(A + B + C)(A + B + C')(A + B' + C)(A' + B + C)

1. Use XX = 1 Boolean postulate

= (A + B + C)(A + B + C)(A + B + C')(A + B' + C)(A' + B + C)

2. Use Distributive law (first with fourth | second with fifth | third with sixth)

= (A + B + C'C)(A + B'B + C)(A'A + B + C)

3. Use Boolean postulate xx' = 0

= (A + B + 0)(A + 0 + C)(0 + B + C)

4. Use Boolean postulate x + 0 = x

= (A + B)(A + C)(B + C)

```
