---
layout: post
title: "Basic octal"
date: 2020-04-12 09:57:53 +0100
categories: Number systems
---
Octal number system is a number system with a base 8. Octal number system is used to represent binary data in groups of three.

So lets look at a first 15 numbers in decimal, binary and octal.

<div class="table-wrapper" markdown="block">

| Decimal | Binary | Octal |
|---------|--------|-------|
| 0       | 0000   | 0     |
| 1       | 0001   | 1     |
| 2       | 0010   | 2     |
| 3       | 0011   | 3     |
| 4       | 0100   | 4     |
| 5       | 0101   | 5     |
| 6       | 0110   | 6     |
| 7       | 0111   | 7     |
| 8       | 1000   | 10    |
| 9       | 1001   | 11    |
| 10      | 1010   | 12    |
| 11      | 1011   | 13    |
| 12      | 1100   | 14    |
| 13      | 1101   | 15    |
| 14      | 1110   | 16    |
| 15      | 1111   | 17    |
|---------|--------|-------|

</div>

So we can see that the greatest number in one octal group is 7, because we represent octal number as three binary numbers.

Let’s check out logic in representing decimal number 15 as an octal number.

{% highlight ruby %}
1111
  => 001 | 111
  =>   1 |   7
  => 17 (base 8)
{% endhighlight %}