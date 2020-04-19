---
layout: post
title: "Basic decimal conversions"
date: 2020-04-13 13:57:53 +0100
categories: Number systems
---
We have learned about [binary]({% post_url 2018-12-30-basic-binary %}), [octal]({% post_url 2020-04-12-basic-octal %}), and [hexadecimal]({% post_url 2019-01-20-basic-hexadecimal %}) now we can continue to basic conversion from decimal to other number system.

**Decimal**

We will start with decimal number system, also known as number system with base 10.

**Decimal to Binary**

Converting number system with base **10** to number system with base **2**.

So lets convert number **20** to binary.

{% highlight ruby %}

20 (Base 10) => 010100 (Base 2)

{% endhighlight %}

Main thing we need to know while converting decimal to binary is that we need to divide decimal number with **2** until we get **quotation 0**

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 20/2   | 10        | 0        |
|--------|-----------|----------|
| 10/2   | 5         | 0        |
|--------|-----------|----------|
| 5/2    | 2         | 1        |
|--------|-----------|----------|
| 2/2    | 1         | 0        |
|--------|-----------|----------|
| 1/2    | 0         | 1        |
|--------|-----------|----------|

If we read **Reminder** from bottom up, we can see `10100` as a binary representation of number 20.

**Decimal to Octal**

Converting number system with base **10** to number system with base **8**

So lets convert number **20** to octal.

{% highlight ruby %}

20 (Base 10) => 24 (Base 8)

{% endhighlight %}

Main thing we need to know while converting decimal to octal is that we need to divide a decimal number with **8** until we get **quotation 0**

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 20/8   | 2         | 4        |
|--------|-----------|----------|
| 2/8    | 0         | 2        |
|--------|-----------|----------|

If we read **Reminder** from bottom up, we can see `24` as an octal representation of number 20.

**Decimal to Hexadecimal**

Converting number system with base **10** to number system with base **16**

So lets convert number **20** to hexadecimal.

{% highlight ruby %}

20 (Base 10) => 14 (Base 16)

{% endhighlight %}

Main thing we need to know while converting decimal to octal is that we need to divide a decimal number with **16** until we get **quotation 0*

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 20/16  | 1         | 4        |
|--------|-----------|----------|
| 2/16   | 0         | 1        |
|--------|-----------|----------|

If we read **Reminder** from bottom up, we can see `14` as a hexadecimal representation of number 20.