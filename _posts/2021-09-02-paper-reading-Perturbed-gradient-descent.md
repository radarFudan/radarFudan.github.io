---
layout: post
title: "paper reading: How to Escape Saddle Points Efficiently"
date: 2021-09-02
---

## Paper 10

[PGD](http://proceedings.mlr.press/v70/jin17a/jin17a.pdf)

## What is Perturbed Gradient Descent?

Before each gradient descent step, if the perturbation condition holds, then perturbed the gradient with some Gaussian noise.

## Why do we need PGD?

On high dimensional space, gradient descent get trapped in saddle point.

## Contribution of this paper:

1. Perturbed gradient descent can finds an approxiamte second-order stationary point in at most $polylog(d)$ iterations. Previous work depends on d linearly, this $polylog(d)$ complexity is almost dimension-free.
2. Under a strict-saddle condition(Hessian's minimum eigenvalue is negative), this convergence result applies for finding local minima.

## Paper Structure

1. Introduction: Our Contribution; Related Work
2. Preliminaries: Notation; Gradient Descent
3. Main Result
4. Example
5. Proof Sketch
6. Conclusion
7. Appendix ABC

## Reference
