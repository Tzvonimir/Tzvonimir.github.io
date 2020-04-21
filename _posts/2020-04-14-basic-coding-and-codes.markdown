---
layout: post
title: "Basic encoding and codes"
date: 2020-04-14 13:57:53 +0100
categories: Codes
---

Most digital devices use binary to store data and manipulate data. So to make life a bit easies people created corresponding codes for displaying number and characters.

So lets say we want to (using codes) display decimal number. We have to use combination of at least 4 bits. As we know with for bites we can display **16** different combinations (2^4).

But if we think about for decimal characters we only need **10** combinatios for numbers from **0 to 9**, but if we take only 3 bits we will end up with **8** different combinations which certently isen't enough. One great example of encoding (decimal characters) is **BCD** or **Binary Coded Decimal**. We will talk more about **BCD** in the future articles.

As much as we can encode numbers we can encode characters and special characters, that type of code is known as **character codes** or **alphanumeric codes**. And cetanly the most popular and well known code is **ASCII** code, but there are some other codes like **EBDDIC** code, and **UNICODE**.

Codes can be classified as:
* Weighted code
* Non-Weighted code
* Reflective code
* Sequential code
* Alphanumeric code
* Error detecting and correcting code

**Weighted** codes are those in which each digit is assigned with a specific weight according to its position. Let's take a look at `1001` in **BCD**.

|----------|---|---|---|---|
| Code     | 1 | 0 | 0 | 1 |
|----------|---|---|---|---|
| Position | 4 | 3 | 2 | 1 |
|----------|---|---|---|---|
| Value    | 8 | 4 | 2 | 1 |
|----------|---|---|---|---|

From the example above we can see that each position is assigned specific value.

**Non-Wighted** codes are those that are not positionally weighted. In other words, each digit position within the number is not assigne a fixed value. Example of non-weigted code is **Excess-3** code. Let's take a look at a `0011` in **Excess-3** code.

Example 1.

|----------|---|---|---|---|
| Code     | 0 | 0 | 1 | 1 |
|----------|---|---|---|---|
| Position | 4 | 3 | 2 | 1 |
|----------|---|---|---|---|
| Value    | 0 | 0 | 0 | 0 |
|----------|---|---|---|---|
| Total    |   |   |   | 0 |
|----------|---|---|---|---|


Example 2.

|----------|---|---|---|---|
| Code     | 0 | 1 | 0 | 0 |
|----------|---|---|---|---|
| Position | 4 | 3 | 2 | 1 |
|----------|---|---|---|---|
| Value    | 0 | 1 | 0 | 0 |
|----------|---|---|---|---|
| Total    |   |   |   | 1 |
|----------|---|---|---|---|

Example 3.

|----------|---|---|---|---|
| Code     | 0 | 1 | 1 | 0 |
|----------|---|---|---|---|
| Position | 4 | 3 | 2 | 1 |
|----------|---|---|---|---|
| Value    | 0 | 2 | 1 | 0 |
|----------|---|---|---|---|
| Total    |   |   |   | 3 |
|----------|---|---|---|---|

We can see from examples above that values are not strictly defined by position.

**Reflective** code is also known as **self complemented** code. As the word **reflective** says value should be reflected that each number has its own reflection, or reflected value e.g. `8` is `1`, `5` is `4` and so on... Example of reflective code is **Excess-3** code.

For example `1000` is `5` in decimal, and 1st complement of `5` is `0111` or `4` in Excess-3 which in total corresponds to `9`.

Let’s take one more example, `2` in Excess-3 is `0101`, and 1st complement is `1010` which is `7`, and again the sum of two numbers is `9`.

**Sequential** codes are those codes in which each succeeding number is one binary number greater than its preceding number. Once again we can use **Excess-3** code as an example of sequential codes.

Code `0100` is `1`, code `0101` is `2`, and code `0110` is `3`. We can see that each succeeding decimal number is one binary number greater than its preceding number.

**Alphanumeric** codes are codes used to represent numbers, symbols, alphabetic characters necessary for representing information. Best known example is **ASCII** code.

**Error detecting and correcting** codes are those codes which allow error detection and correction. **Hamming code** is the most common error detecting and correcting code.
