---
layout: post
title: "Half adder"
date: 2019-02-04 22:57:53 +0100
categories: Logic gates
---

Half adder is a digital circuit, used for [adding]({% post_url 2019-01-21-binary-arithmetic-operations %}) single-bit numbers, it **DOES NOT** take carry from the previous sum.


![half-adder]({{ site.url }}/img/half_adder.jpg){:class="img-responsive"}

<div class="table-wrapper" markdown="block">

| A | B | S | C |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 |
|---|---|---|---|

</div>

We make half adder digital circuit of an XOR and AND [logic gate]({% post_url 2019-02-03-basic-logic-gates %}).

![half-adder-logic]({{ site.url }}/img/half_adder_logic.jpg){:class="img-responsive"}