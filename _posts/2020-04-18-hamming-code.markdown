---
layout: post
title: "Hamming code"
date: 2020-04-16 13:57:53 +0100
categories: Codes
---
**Hamming code** is a [error correcting](% post_url 2020-04-14-basic-coding-and-codes %}) code,
Hamming code can detect up to 2 bit errors, or correct 1 bit error.

General rule for generating parity bits when creating error codes is:
`2^n^ >= n + m + 1`
where:
* n = parity bits
* m = bits

So lets say we want to `1001`we would have `3` parity bits.
`2^3 >= 3 + 4 + 1 => 8 >= 8`

So the code would be:
`1001100 `

So the hamming code would look like this.

| 2^0 | 2^1 | 2^2 | 2^3 | 2^4 | 2^5 | 2^6 |
|-----|-----|-----|-----|-----|-----|-----|
| p1  | p2  | d3  | p4  | d5  | d6  | d7  |
|-----|-----|-----|-----|-----|-----|-----|
|  0  |  0  |  1  |  1  |  0  |  0  |  1  |
|-----|-----|-----|-----|-----|-----|-----|

Let’s explain how to find a position where we will put parity bits.
Parity bit will always go to the position equal to the 2 to the
some exponent.

So first parity bit will go to the position 2^0^, second one will be 2^1^,
and the last one is 2^2^. 2^2^ is equal to `4`. `4` >= to the
m(total number of bits) and 2^3^ would be `8` which is greater than
the total number of bits, that means 2^2^ is the last parity bit.

To find out value of parity bits, we need to understand that each sum
of numbers used to define parity bit value must be equal to `1`.

`P1 = d7 + d5 + d3 = 1 + 0 + 1 = 1 so we put 0 in p1`

`P2 = d7 + d6 + d3 = 1 + 0 + 1 = 1 so we put 0 in p2`

`P3 = d7 + d6 + d5 = 1 + 0 + 0 = 0 so we put 1 in p3`

So we can see that for parity bit one we start from MSB and then take 1 bit
into calculation and skip one, repeating that process till the LSB

The growth is linear, as for p2 we will take 2 bits and skip 2.
For a third parity bit we will take 3 and skip 3 bits.

So now that we know how to convert a binary number into hamming code,
we can decode the hamming code back to the binary.

So let's decode `0011001`

First lets first find all the parity bits in the code. We know that our
code is `7` bits long, and that 2^2^ is equal to the `4` and 2^3^ is equal
to the `8` which means  a number of parity bits will be 3 (2^0^, 2^1^, 2^2^) because if it would be 4(2^0^, 2^1^, 2^2^, 2^3^) we would need at
least 8 bits in our code.

| 2^0 | 2^1 | 2^2 | 2^3 | 2^4 | 2^5 | 2^6 |
|-----|-----|-----|-----|-----|-----|-----|
| p1  | p2  | d3  | p4  | d5  | d6  | d7  |
|-----|-----|-----|-----|-----|-----|-----|
|  0  |  0  |  1  |  1  |  0  |  0  |  1  |
|-----|-----|-----|-----|-----|-----|-----|

So for p1 we will check one and skip one, starting from p1 to d7.

`p1 = d3 + d5 + d7 = 1 + 0 + 1 = 1 => p1 = 0`

We get 1 as a result so we know that p1 should be 0

For p2 we will check two and skip two, starting from p2 to d7.

`p2 = d3 + d6 + d7 = 1 + 0 + 1 = 1 => p2 = 0`

For p4 we will check three and skip three, starting from p4 to d7.

`p4 = d5 + d6 + d7 = 0 + 0 + 1 = 0 => p4 = 1`

We can see that all parity bits are equal, so we can conclude that that
code is correct and there is no need for error correction.

We can proceed and remove all the parity bits. And then we are left with
`d3 d5 d6 d7`, which is `1001`. Now we just need to flip bit from `LSB` to
`MSB`, and then we get `1001`.

Let’s look at a hamming code with an error we can correct.

`0011011`

| 2^0 | 2^1 | 2^2 | 2^3 | 2^4 | 2^5 | 2^6 |
|-----|-----|-----|-----|-----|-----|-----|
| p1  | p2  | d3  | p4  | d5  | d6  | d7  |
|-----|-----|-----|-----|-----|-----|-----|
|  0  |  0  |  1  |  1  |  0  |  1  |  1  |
|-----|-----|-----|-----|-----|-----|-----|

So for p1 we will check one and skip one, starting from p1 to d7.

`p1 = d3 + d5 + d7 = 1 + 0 + 1 = 1 => p1 = 0`

We get 1 as a result so we know that p1 should be 0

For p2 we will check two and skip two, starting from p2 to d7.

`p2 = d3 + d6 + d7 = 1 + 1 + 1 = 0 => p2 = 1`

For p4 we will check three and skip three, starting from p4 to d7.

`p4 = d5 + d6 + d7 = 0 + 1 + 1 = 1 => p4 = 0`

We can see that `p2` and `p4` have wrong value. We then add value of the
position of both parity bits that have wrong value, and we get a position
of bit we have to complement.

`2 + 4 = 6`
This means we have to flip bit in position `d6` to correct the code.
`0011001`