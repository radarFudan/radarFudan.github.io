---
layout: post
title: "paper reading SGD&SDE"
date: 2021-03-15
---

#### Paper 1
[On the Validity of Modeling SGD with SDEs](https://arxiv.org/abs/2102.12470)

Linear Scaling Rule: When the minibatch size is multiplied by kappa, multiply the LR by kappa. 

SVAG: x_{k+1} = x_k - eta / l L'^l_{gamma_k} (x_k).
SVAG provides an order-1 weak approximation to the corresponding SDE. 

Group Norm:

C-Closedness: Three metrics differ by a multiplicative constant controlled by C. 

PreResNet32: 

Model gradient descent as Levy process:

Relevant paper:

Claim: In (Cheng et al., 2020) that differences in the third-and-higher moments in SGD noise don't affect the test accuracy significantly, though the differences in the second moments do.

(Smith 2020) defined the noise dominated regime and curvature dominated regime. They showed experimentally that in noise dominated regime, the training properties, including the optimal LR are controlled by noise. 

