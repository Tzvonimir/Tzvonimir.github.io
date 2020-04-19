---
layout: post
title: "Basic binary"
date: 2019-01-06 22:57:53 +0100
categories: Number systems
---
If we think about language, as Croats use the Croatian language, computers use binary language to process and manipulate data.

The most basic thing any language has to have is an alphabet. Usually, the letters make the alphabet, but in binary `1` and `0` make the whole alphabet we will use.

Binary is a number system with base 2, as a decimal is the number system with base 10

So if we want to input a letter on the computer, we need to use a binary representation of that letter.

{% highlight ruby %}
A => 01000001, a => 01100001
B => 01000010, b => 01100010
B => 01000011, b => 01100011
{% endhighlight %}

As we can represent letters of the alphabet with binary code, we can do the same with numbers.

{% highlight ruby %}
1 => 00000001
2 => 00000010
3 => 00000011
{% endhighlight %}

To better imagine how computer process numbers we will take number 13 as an example:

| Binary | Value | Decimal |
|-------|--------|---------|
| 1     | 1      | 1       |
| 0     | 2      | 0       |
| 1     | 4      | 4       |
| 1     | 8      | 8       |
| 0     | 16     | 0       |
| 0     | 32     | 0       |
| 0     | 64     | 0       |
| 0     | 128    | 0       |
| Total |        | 13      |
|-------|--------|---------|

We calculate a mathematical representation of above as:

{% highlight ruby %}
00001101
=> 0*2^7
+ 0*2^6
+ 0*2^5
+ 0*2^4
+ 1*2^3
+ 1*2^2
+ 0*2^1
+ 1*2^0
= 13
{% endhighlight %}