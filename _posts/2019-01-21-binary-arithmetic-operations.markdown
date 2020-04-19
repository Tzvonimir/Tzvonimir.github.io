---
layout: post
title: "Binary arithmetic operations"
date: 2019-01-06 22:57:53 +0100
categories: Number systems
---

After grasping basic [binary]({% post_url 2018-12-30-basic-binary %}) knowledge we can learn and understand binary arithmetic operations.

**Addition**

First, we have to understand how addition works in binary. There are only four rules we have to respect when doing binary addition.

| First binary number | Second binary number | Sum | Carry |
|---------------------|----------------------|-----|-------|
| 0                   | 0                    | 0   | 0     |
| 0                   | 1                    | 1   | 0     |
| 1                   | 0                    | 1   | 0     |
| 1                   | 1                    | 0   | 1     |
|---------------------|----------------------|-----|-------|

In case we need to add `1` and `1` as shown in the fourth rule in the table above we can see that product of those two binary numbers is `0` but we carry `1` to the next step of the addition process.

To better understand addition, let’s do an example.

{% highlight ruby %}
26 => 00011010
12 => 00001100

38 => 00100110
{% endhighlight %}

| First binary number | Second binary number | Sum | Carry |
|---------------------|----------------------|-----|-------|
| 0                   | 0                    | 0   | 0     |
| 1                   | 0                    | 1   | 0     |
| 0                   | 1                    | 1   | 0     |
| 1                   | 1                    | 0   | 1     |
| 1                   | 0                    | 0   | 1     |
| 0                   | 0                    | 1   | 0     |
| 0                   | 0                    | 0   | 0     |
| 0                   | 0                    | 0   | 0     |
|---------------------|----------------------|-----|-------|

**Subtraction**

After learning how addition works in binary, we understand that subtraction is the same as an addition because the computer does subtraction through addition.

{% highlight ruby %}
C = A – B

C = A + (-B)
{% endhighlight %}

First, we need to calculate the complement of our second number `B` and add `1`. So let’s take `30 - 15` as an example.

{% highlight ruby %}
C = 30 - 15

A => 30 = 00011110
B => 15 = 00001111

(-B) => 11110000 + 1 = 11110001

C => 00011110 + 11110001 = 00001111
{% endhighlight %}

Now when we have a two’s complement of our number `B` we can proceed to addition.

| First binary number | Second binary number | Sum | Carry |
|---------------------|----------------------|-----|-------|
| 0                   | 1                    | 1   | 0     |
| 1                   | 0                    | 1   | 0     |
| 1                   | 0                    | 1   | 0     |
| 1                   | 0                    | 1   | 0     |
| 1                   | 1                    | 0   | 1     |
| 0                   | 1                    | 0   | 1     |
| 0                   | 1                    | 0   | 1     |
| 0                   | 1                    | 0   | 1     |
|---------------------|----------------------|-----|-------|

**Multiplication**

Multiplication in binary is identical to multiplication in decimal. There are only four rules we have to respect when doing the first part of multiplication.

| First binary number | Second binary number | Multiplication |
|---------------------|----------------------|----------------|
| 0                   | 0                    | 0              |
| 0                   | 1                    | 0              |
| 1                   | 0                    | 0              |
| 1                   | 1                    | 1              |
|---------------------|----------------------|----------------|

To better understand multiplication, let’s do an example.

{% highlight ruby %}
26 => 00011010
12 => 00001100

26 * 12 = 312
00011010 * 00001100 = 100111000
{% endhighlight %}

| Operation       | Binary    | Decimal | Decimal Multi. |
|-----------------|-----------|---------|----------------|
| Multiplicand    | 11010     | 26      | 26             |
|-----------------|-----------|---------|----------------|
| Multiplier      | 01100     | 12      | 12             |
|-----------------|-----------|---------|----------------|
|                 |           |         |                |
|-----------------|-----------|---------|----------------|
| Partial product | 00000     |         | 12             |
|-----------------|-----------|---------|----------------|
| Partial product | 000000    | 0       | 40             |
|-----------------|-----------|---------|----------------|
| Partial product | 1101000   | 104     | 60             |
|-----------------|-----------|---------|----------------|
| Partial product | 11010000  | 208     | 200            |
|-----------------|-----------|---------|----------------|
| Partial product | 000000000 | 0       |                |
|-----------------|-----------|---------|----------------|
| +               |           |         |                |
|-----------------|-----------|---------|----------------|
| Final product   | 100111000 | 312     | 312            |
|-----------------|-----------|---------|----------------|

**Division**

Division in binary is identical to long division in the decimal system. Long division is the standard algorithm used for pen-and-paper division of multi-digit numbers expressed in decimal notation.

To better understand division, let’s do an example and divided 39 with 3.

While doing binary division there are some rules for subtracting files in long division:

Subtracting **0** from **0** we get **0**

Subtracting **1** from **0** equals **1**

Subtracting **1** from **1** equals **0**

But while subtracting **0** from **1** we have to take **1** from the first number to the right and then we have to subtract **10** from **1** and that equals to **1**

But if we want to, we could use two’s complement for subtraction.

{% highlight ruby %}
dividend 39 => 00100111
divisor   3 => 00000011

quotation
_________
divisor ) dividend
reminder


00001101
_________
00000011 ) 00100111
-   11
--------
011
-    11
--------
0011
-      11
--------
0

{% endhighlight %}

| Operation          | Binary   | Binary   | Decimal |
|--------------------|----------|----------|---------|
| Quotation          |          | 00001101 | 13      |
|--------------------|----------|----------|---------|
| Divisor / Dividend | 00000011 | 00100111 | 3 / 39  |
|--------------------|----------|----------|---------|
| -                  |          | 00011    | 3       |
|--------------------|----------|----------|---------|
| Subtraction result |          | 000011   | 3       |
|--------------------|----------|----------|---------|
| -                  |          | 000011   | 3       |
|--------------------|----------|----------|---------|
| Subtraction result |          | 00000011 | 3       |
|--------------------|----------|----------|---------|
| -                  |          | 00000011 | 3       |
|--------------------|----------|----------|---------|
| Rest               |          | 00000000 | 0       |
|--------------------|----------|----------|---------|
