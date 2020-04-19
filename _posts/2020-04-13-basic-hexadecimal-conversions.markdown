---
layout: post
title: "Basic hexadecimal conversions"
date: 2020-04-13 13:57:53 +0100
categories: Number systems
---
We have learned about [binary]({% post_url 2018-12-30-basic-binary %}), [octal]({% post_url 2020-04-12-basic-octal %}), and [hexadecimal]({% post_url 2019-01-20-basic-hexadecimal %}) now we can continue to basic conversion from hexadecimal to other number system.

**Hexadecimal**

We will start with hexadecimal number system, also known as number system with base 16.

**Hexadecimal to Binary**

Converting number system with base **16** to number system with base **2**.

So lets convert hexadecimal number **14** to binary.

{% highlight ruby %}

20 (Base 10) => 010100 (Base 2) => 14 (Base 16)

{% endhighlight %}

While converting **hexadecimal** to **binary**, we have to split each number into a separate group. Then we can calculate each group as we would with while converting [decimal]({% post_url 2020-04-13-basic-decimal-coversions %}) to binary numbers.

{% highlight ruby %}

14 (Base 16) = 1 | 4

{% endhighlight %}

**First Group**

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 1/2    | 0         | 1        |
|--------|-----------|----------|

If we read **Reminder** from bottom up, we can see `1` as a binary representation of number 1, because we are talking about **hexadecimal** we know that hexadecimal numbers are created from groups of four bits, we will add multiple zeros to the end. So we end up with `0001`.

**Second group**

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 4/2    | 2         | 0        |
|--------|-----------|----------|
| 2/2    | 1         | 0        |
|--------|-----------|----------|
| 1/2    | 0         | 1        |
|--------|-----------|----------|

If we read **Reminder** from bottom up, we can see `100` as a binary representation of number 4, again we are using a hexadecimal number system so we have to add one more zero to the end. So we end up with `0100`.

Then we just concatenate two binary numbers starting from the first group to get the result `00010100`.

**Hexadecimal to Decimal**

Converting number system with base **16** to number system with base **10**

Conversion from hexadecimal to decimal is like [binary-decimal]({% post_url 2020-04-13-basic-binary-coversions %}) conversion. Main difference is that here we will not add numbers as an exponent of 2, but of 16.

So lets convert octal number **14** to decimal.

{% highlight ruby %}

  14
  => 4*16^0 + 1*16^1
   = 4 + 16
   = 20

{% endhighlight %}

**Hexadecimal to Octal**

Converting number system with base **16** to number system with base **8**

So lets convert hexadecimal number **14** to octal.

{% highlight ruby %}

20 (Base 10) => 24(base 8) => 14 (Base 16)

{% endhighlight %}

Main thing we need to know while converting hexadecimal to octal is that we have to do multiple steps. The first step is to hexadecimal number to binary (check section **Hexadecimal to Binary**) and then convert [binary to octal]({% post_url 2020-04-13-basic-octal-coversions %})

After converting number to binary, we can proceed to octal conversion.

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