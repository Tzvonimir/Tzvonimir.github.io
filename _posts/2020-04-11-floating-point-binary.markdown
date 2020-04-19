---
layout: post
title: "Floating point binary"
date: 2020-04-11 22:57:53 +0100
categories: Number systems
---
Same as in decimal number systems, binary can have floating-point numbers.

Let’s imagine we have 8 bits and we dedicate 4 bits for whole numbers and 4 bits for fractions, then we would represent a decimal number **7.5** as a **0111.1000**.

To understand why is that the case we need to return to the [basic binary]({% post_url 2018-12-30-basic-binary %}) and try to remember who did we represent whole numbers in binary.

Let’s take number 7 and represent him in binary.

| Binary | Value | Decimal |
|--------|-------|---------|
| 1      | 1     | 1       |
| 1      | 2     | 2       |
| 1      | 4     | 4       |
| 0      | 8     | 0       |
| Total  |       | 7       |
|--------|-------|---------|

We calculate a mathematical representation of above as:

{% highlight ruby %}
0111
=>
1*2^0
+ 1*2^1
+ 1*2^3
+ 0*2^4
= 7
{% endhighlight %}

So we can see that we represent each number as the power of two.

We apply the same principle for floating numbers in binary, just as we have to think of numbers are on the right side of the floating-point as a negative power of two. If we want to express 0.5 as a binary number we understand that 0.5 is the same as 1/2. And then we can proceed to conversion 2 to the power of negative -1.

| Binary | Value | Decimal |
|--------|-------|---------|
| 1      | 1/2   | 0.5     |
| 0      | 1/4   | 0       |
| 0      | 1/8   | 0       |
| 0      | 1/16  | 0       |
| Total  |       | 0.5     |
|--------|-------|---------|


We calculate mathematical representation of above as:

{% highlight ruby %}
.1000
=>
1*2^-1
+ 0*2^-2
+ 0*2^-3
+ 0*2^-4
= 0.5
{% endhighlight %}

**Popular representations of floating-point numbers**

With **32** bits we can represent single point precision, and with **64** bits we can represent double point precision. (we will use IEEE standard)

  **Single point precision**

  Single precision floating point representation uses a word of 32 bit.

  We dedicate:

  * 1 bit for **Sign - S**,
  * 8 bit for the **Exponent - E**,
  * 24 bits for the **Fraction or Mantissa - M**

  Let’s take 7.5 from the beginning and represent him as a **single point precision**

  | Sign     | 0                       |
  |----------|-------------------------|
  | Exponent | 10000001                |
  |----------|-------------------------|
  | Matissa  | 11110000000000000000000 |
  |----------|-------------------------|

  We need to remember how to represent scientific numbers because we will use the same principle of number representation while converting floating-point binary numbers.

  When we convert 7.5 to the binary we get:

{% highlight ruby %}

7.5 => 0111.1000

{% endhighlight %}

Now we have to move floating point until we get a single high bit, to do that we need to move floating point two spaces to the right.

{% highlight ruby %}

1.111000

{% endhighlight %}

Because we moved the floating-point two spaces to the right, we know that our exponent is 2.

{% highlight ruby %}

1.11100 x 2^2

{% endhighlight %}

So now we have to convert exponent to the binary. To do it, we need to understand that we have to use the **excess**. It means that the number we will represent is some **excess** value greater than the original number. In our case (Single Point Precision) we use number **127**.

We will represent number 2^2 as a binary value of exponent **2**. Which in binary is **10**, and we can prove that:

{% highlight ruby %}

10 => 0*2^0 + 1*2^1 = 2

{% endhighlight %}

Now we need to add **excess-127** to the number two.

{% highlight ruby %}

127 + 2 = 129

{% endhighlight %}

So let’s covert number 129 to the binary representation.

| Binary | Value | Decimal |
|--------|-------|---------|
| 1      | 1     | 1       |
| 0      | 2     | 0       |
| 0      | 4     | 0       |
| 0      | 8     | 0       |
| 0      | 16    | 0       |
| 0      | 32    | 0       |
| 0      | 64    | 0       |
| 1      | 128   | 128     |
| Total  |       | 129     |
|--------|-------|---------|

Now we can conclude that the **sign** bit will be **0** because we know that number 7.5 is a positive number, and we have found our exponent as an **excess-127** of total numbers we moved the floating-point to get single high bit **10000001**.

We know that our mantissa should be 23 bits as IEEE defined that (e can use a bit of logic to come to the answer why **23** bits. If we have 32 bits and we used 1 bit as a sign bit, it leaves us with 31 bits, now we need to reduce that number by 8 for a total number of bits in our exponent. 31 - 8 is equal to the **23**).

We know that our mantissa is **1.11100** but that number is only **6** bits long, and we are some 17 bits. To compensate for those 17 bits we will add **17 zeros(0)** to the end of our floating-point representation and we will end up with the following mantissa **11110000000000000000000**.

Our **single point precision** representation of floating-point number will look like this:

`11000000111110000000000000000000`

**Double point precision**

Double-precision floating-point representation uses a word of 64 bit.

We dedicate:
* 1 bit for **Sign - S**,
  * 11 bit for the **Exponent - E**,
  * 53 bits for the **Fraction or Mantissa - M**

  **Double point precision** is pretty much similar to the **Single point precision** main difference is that it uses 64 bits to store information about floating-point numbers. The main thing we need to remember here is that our exponent is no longer **8** but **11** bits long, so we will have to use **excess-1023**, so the number we will represent in exponent field is number 1023 greater than the original number.