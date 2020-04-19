---
layout: post
title: "Full adder"
date: 2020-03-01 22:57:53 +0100
categories: Logic gates
---

Unlike the [half adder]({%post_url 2019-02-04-half-adder %}), the full adder can **TAKE** a carry from the previous sum.


![full-adder]({{ site.url }}/img/full_adder.jpg){:class="img-responsive"}

| A | B | C in | S | C out |
|---|---|------|---|-------|
| 0 | 0 | 0    | 0 | 0     |
| 0 | 0 | 1    | 1 | 0     |
| 0 | 1 | 0    | 1 | 0     |
| 0 | 1 | 1    | 0 | 1     |
| 1 | 0 | 0    | 1 | 0     |
| 1 | 0 | 1    | 0 | 1     |
| 1 | 1 | 0    | 0 | 1     |
| 1 | 1 | 1    | 1 | 1     |
|---|---|------|---|-------|

We make a full adder digital circuit of a two XOR, three AND, and two OR [logic gates]({% post_url 2019-02-03-basic-logic-gates %}).

![full-adder-logic]({{ site.url }}/img/full_adder_logic.jpg){:class="img-responsive"}