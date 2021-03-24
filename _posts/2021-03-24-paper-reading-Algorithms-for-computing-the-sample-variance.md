---
layout: post
title: "paper reading: Algorithms for computing the sample variance: analysis and recommendations"
date: 2021-03-24
---

## Paper 6
[computing the sample variance](http://www.cs.yale.edu/publications/techreports/tr222.pdf)

## Intro 

Standard two-pass algorithm: 

$$S = \sum_{i=1}^N (x_i - \overline{x})^2,$$

$$\overline{x} = \frac{1}{N} \sum_{i=1}^N x_i$$

And it is standard to manipulate the definition of S into the form

$$S = \sum_{i=1}^N x_i^2 - \frac{1}{N} (\sum_{i=1}^N x_i)^2.$$

## 