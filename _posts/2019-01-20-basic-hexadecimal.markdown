---
layout: post
title:  "Basic hexadecimal"
date:   2019-01-20 09:57:53 +0100
categories: Hexadecimal
---
[Binary language]({% post_url 2018-12-30-basic-binary %}) is used to process and manipulate data in computers, but binary language has some flows. First and most important is readability. 

Hexadecimal uses digits that resembles our basic base-10 counting system (decimal). The second reason is higher information density, with only two digits we can represent numbers to a maximum value of 255, to do the same in binary we need 8 digits.

{% highlight ruby %}
e7 => 1110 0111 = 231
{% endhighlight %}

We as humans use hexadecimal language to represent machine language with more ease. So one would ask why don't we use the decimal system, the main reason why is a collaboration between binary and hexadecimal, every hexadecimal number can be represented as four binary numbers.

| Hexadecimal | Binary         | Decimal value |
|-------------|----------------|---------------|
| 0           | 0000           | 0             |
| 1           | 0001           | 1             |
| 2           | 0010           | 2             |
| 3           | 0011           | 3             |
| 4           | 0100           | 4             |
| 5           | 0101           | 5             |
| 6           | 0110           | 6             |
| 7           | 0111           | 7             |
| 8           | 1000           | 8             |
| 9           | 1001           | 9             |
| A           | 1010           | 10            |
| B           | 1011           | 11            |
| C           | 1100           | 12            |
| D           | 1101           | 13            |
| E           | 1110           | 14            |
| F           | 1111           | 15            |

To better comprehend the reasons behind the above statement we need to know that our basic decimal system has a base of 10. Suppose to hexadecimal which has a base of 16. So with that in mind, we know that the best ways to compress binary data should have a base that is a multiple of 2.

To better imagine how to convert hexadecimal to decimal we will take number 231 as an example:

| Hexadecimal | Value  | Decimal value    |
|-------------|--------|------------------|
| e           | 14     | 224              |
| 7           | 7      | 7                |
| Total       |        | 231              |
 
Mathematical representation of above is calculated as:

{% highlight ruby %}
e7 => 14 * 16 ^ 1 + 7 * 16 ^ 0 = 231
{% endhighlight %}

