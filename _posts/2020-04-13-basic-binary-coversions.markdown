---
layout: post
title: "Basic binary conversions"
date: 2020-04-13 13:57:53 +0100
categories: Number systems
---
We have learned about [binary]({% post_url 2018-12-30-basic-binary %}), [octal]({% post_url 2020-04-12-basic-octal %}), and [hexadecimal]({% post_url 2019-01-20-basic-hexadecimal %}) now we can continue to basic conversion from binary to other number system.

**Binary**

We will start with binary number system, also known as number system with base 2.

**Binary to Decimal**

Converting number system with base **2** to number system with base **10**.

So lets convert number **20** form binary to decimal.

{% highlight ruby %}

20 (base 10) => 010100 (base 2)

{% endhighlight %}

Main thing we need to know while converting binary to decimal is that we need to understand is that each bit represent power of two. So if we look binary number `1111` from **LSB** to **MSB**. LSB is **2^0**, next bit to the right is **2^1**, next one is **2^2** and MSB is **2^3**

So with that let's convert number `010100` to the decimal.

{% highlight ruby %}

010100
=> 0*2^0 + 0*2^1 + 1*2^2 + 0*2^3 + 1*2^4 + 0*2^5
= 0 + 0 + 4 + 0 + 16 + 0
= 20

{% endhighlight %}

<div class="table-wrapper" markdown="block">

| Binary | Value | Decimal |
|-------|--------|---------|
| 0     | 1      | 0       |
| 0     | 2      | 0       |
| 1     | 4      | 4       |
| 0     | 8      | 0       |
| 1     | 16     | 16      |
| 0     | 32     | 0       |
| Total |        | 20      |
|-------|--------|---------|

</div>

**Binary to Octal**

Converting number system with base **2** to number system with base **8**

So lets convert number **20** from binary to octal.

{% highlight ruby %}

20 (Base 10) => 24 (Base 8) => 010100 (Base 2)

{% endhighlight %}

Main thing we need to know while converting binary to octal is that we need to devide binary number in **groups of three**. So every three bits represent one octal number.

{% highlight ruby %}

010100 => 010 | 100

{% endhighlight %}

After deviding number into groups of three we can procide to converting each group into octal number. Process is the same as for decimal number, but each group is calculated separetly.

{% highlight ruby %}

010100 = 010 | 100

010
=> 0*2^0 + 1*2^1 + 0*2^2
= 0 + 2 + 0
= 2

100
=> 0*2^0 + 1*2^1 + 1*2^2
= 0 + 0 + 4
= 4

010100 (base 2) = 24 (base 8)

{% endhighlight %}

**First group**

<div class="table-wrapper" markdown="block">

| binary | value | decimal |
|-------|--------|---------|
| 0     | 1      | 0       |
| 1     | 2      | 2       |
| 0     | 4      | 0       |
| total |        | 2       |
|-------|--------|---------|

</div>

**Second group**

<div class="table-wrapper" markdown="block">

| binary | value | decimal |
|-------|--------|---------|
| 0     | 1      | 0       |
| 0     | 2      | 0       |
| 1     | 4      | 4       |
| total |        | 4       |
|-------|--------|---------|

</div>

Then we just concat total starting from first group `24`

**Binary to Hexadecimal**

Converting number system with base **2** to number system with base **16**

So lets convert number **20** from binary to hexadecimal.

{% highlight ruby %}

20 (Base 10) => 14 (Base 16) => 010100 (Base 2)

{% endhighlight %}

Main thing we need to know while converting binary to hexadecima is that we need to devide binary number in **groups of four**. So every four bits represent one hexadecimal number.

{% highlight ruby %}

010100 => 0001 | 0100

{% endhighlight %}

After deviding number into groups of four we can procide to converting each group into hexadecimal number. Process is the same as for decimal number, but each group is calculated separetly.

{% highlight ruby %}

010100 => 0001 | 0100

0001
=> 1*2^0 + 0*2^1 + 0*2^2 + 0*2^3
= 1 + 0 + 0 + 0
= 1

0100
=> 0*2^0 + 0*2^1 + 1*2^2 + 0*2^3
= 0 + 0 + 4 + 0
= 4

00010100 (base 2) = 14 (base 16)

{% endhighlight %}

**First group**

<div class="table-wrapper" markdown="block">

| binary | value | decimal |
|-------|--------|---------|
| 1     | 1      | 1       |
| 0     | 2      | 0       |
| 0     | 4      | 0       |
| 0     | 4      | 0       |
| total |        | 1       |
|-------|--------|---------|

</div>

**Second group**

<div class="table-wrapper" markdown="block">

| binary | value | decimal |
|-------|--------|---------|
| 0     | 1      | 0       |
| 0     | 2      | 0       |
| 1     | 4      | 4       |
| 0     | 8      | 0       |
| total |        | 4       |
|-------|--------|---------|

</div>

Then we just concat total starting from first group `14`