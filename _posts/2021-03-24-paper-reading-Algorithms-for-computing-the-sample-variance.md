---
layout: post
title: "paper reading: Algorithms for computing the sample variance: analysis and recommendations"
date: 2021-03-24
---

## Paper 6
[computing the sample variance](http://www.cs.yale.edu/publications/techreports/tr222.pdf)

## Intro 

1. Standard two-pass algorithm: 

$$S = \sum_{i=1}^N (x_i - \overline{x})^2,$$

$$\overline{x} = \frac{1}{N} \sum_{i=1}^N x_i$$

2. And it is standard to manipulate the definition of S into the form(*textbook one-pass algorithm*)

$$S = \sum_{i=1}^N x_i^2 - \frac{1}{N} (\sum_{i=1}^N x_i)^2.$$

However, the second form of $S$ is still disastrous numerically.

3. Welford, West and Hanson:

$$M_{1, j} = M_{1, j-1} + \frac{1}{j} (x_j - M_{1, j-1})$$

$$S_{1, j} = S_{1, j-1} + (j-1) (x_j - M_{1, j-1})(\frac{x_j - M_{1, j-1}}{j})$$

with $M_{1,1} = x_1$ and $S_{1,1} = 0$

4. An *unrelated* method is divide the $n$ elements into two part and speed up the method. 

5. When the shift is the computed mean and the textbook algorithm is then applied to the shifted data, one obtains the corrected two-pass algorithm.

$$S = \sum_{i=1}^N (x_i - \overline{x})^2 - \frac{1}{N} (\sum_{i=1}^N (x_i - \overline{x}))^2.$$

## Condition numbers and error analysis

Unrelated to my current progress, to be continued. 