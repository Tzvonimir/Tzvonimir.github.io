---
layout: post
title: "Basic octal conversions"
date: 2020-04-13 13:57:53 +0100
categories: Number systems
---
We have learned about [binary]({% post_url 2018-12-30-basic-binary %}), [octal]({% post_url 2020-04-12-basic-octal %}), and [hexadecimal]({% post_url 2019-01-20-basic-hexadecimal %}) now we can continue to basic conversion from octal to other number system.

**Octal**

We will start with octal number system, also known as number system with base 8.

**Octal to Binary**

Converting number system with base **8** to number system with base **2**.

So lets convert octal number **24** to binary.

{% highlight ruby %}

20 (Base 10) => 010100 (Base 2) => 24 (Base 8)

{% endhighlight %}

While converting **octal** to **binary**, we have to split each number into a separate group. Then we can calculate each group as we would with while converting [decimal]({% post_url 2020-04-13-basic-decimal-coversions %}) to binary numbers.

{% highlight ruby %}

24 (Base 8) = 2 | 4

{% endhighlight %}

**First Group**

<div class="table-wrapper" markdown="block">

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 2/2    | 1         | 0        |
|--------|-----------|----------|
| 1/2    | 0         | 1        |
|--------|-----------|----------|

</div>

If we read **Reminder** from bottom up, we can see `10` as a binary representation of number 2, because we are talking about **octal** we know that octal numbers are created from groups of three bits, we will add zero to the end. So we end up with `010`.

**Second group**

<div class="table-wrapper" markdown="block">

| Divide | Quotation | Reminder |
|--------|-----------|----------|
| 4/2    | 2         | 0        |
|--------|-----------|----------|
| 2/2    | 1         | 0        |
|--------|-----------|----------|
| 1/2    | 0         | 1        |
|--------|-----------|----------|

</div>

If we read **Reminder** from bottom up, we can see `100` as a binary representation of number 4.

Then we just concatenate two binary numbers starting from the first group to get the result `010100`.

**Octal to Decimal**

Converting number system with base **8** to number system with base **10**

Conversion from octal to decimal is like [binary-decimal]({% post_url 2020-04-13-basic-binary-coversions %}) conversion. Main difference is that here we will not add numbers as an exponent of 2, but of 8.

So lets convert octal number **24** to decimal.

{% highlight ruby %}

  24
  => 4*8^0 + 2*8^1
   = 4 + 16
   = 20

{% endhighlight %}

**Octal to Hexadecimal**

Converting number system with base **8** to number system with base **16**

So lets convert octal number **24** to hexadecimal.

{% highlight ruby %}

20 (Base 10) => 24(base 8) => 14 (Base 16)

{% endhighlight %}

Main thing we need to know while converting octal to hexadecimal is that we have to do multiple steps. The first step is to convert the number to binary (check section **Octal to Binary**) and then convert [binary to hexadecimal]({% post_url 2020-04-13-basic-binary-coversions %})

After converting number to binary, we can proceed to hexadecimal conversion.

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
