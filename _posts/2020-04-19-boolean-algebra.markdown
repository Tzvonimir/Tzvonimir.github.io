---
layout: post
title: "Boolean algebra"
date: 2020-04-18 13:57:53 +0100
categories: Boolean algebra
---

**Boolean algebra** is the branch of algebra in which variables are either
**true** or **false**. Usually denoted as `1` or `0`.

Basic operations of boolean algebra are:

  * AND (conjuction) - denoted `x^y` or `xy`
  * OR (disjunction) - denoted `xvy` or `x+y`
  * NOT (negation) - denoted `¬x` or `x'`

**Laws**

**Idempotent law**

`A * A = A`

`A + A = A`

**Associative law**

`(A*B)*C = A*(B*C)`

`(A+B)+C = A+(B+C)`

**Commutative law**

`A * B = B * A`

`A + B = B + A`

**Distributive law**

`A*(B+C) = A*B + A*C`

`A+(B*C) = (A+B) * (A+C)`

**Identity law**

`A * 0 = 0`

`A * 1 = A`

`A + 1 = 1`

`A + 0 = A`

**Complement law**

`A - A' = 0`

`A + A' = 1`

**Involution law**

`(A')' = A`

**DeMorgan's law**

`(A * B)' = A' + B'`

`(A + B)' = A' * B'`