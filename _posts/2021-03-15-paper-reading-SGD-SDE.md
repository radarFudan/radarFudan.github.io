---
layout: post
title: "paper reading SGD&SDE"
date: 2021-03-15
---

## Paper 1
[On the Validity of Modeling SGD with SDEs](https://arxiv.org/abs/2102.12470)

## Background knowledge

**Linear Scaling Rule**: When the minibatch size is multiplied by $\kappa$, multiply the LR by $\kappa$. 

## Main Content

**SVAG**: $x_{k+1} = x_k - \frac{\eta}{l} \nabla \mathcal{L}^l_{\overline{\gamma}_k} (x_k).$<br>
SVAG provides an order-1 weak approximation to the corresponding SDE. (SVAG converges weakly to the SDE) <br>
$$\mathcal{L}_{\overline{\gamma}_k}^l (\cdot) := \frac{1 + \sqrt{2l-1}}{2} \mathcal{L}_{\gamma_{k, 1}}(\cdot) + \frac{1 - \sqrt{2l-1}}{2} \mathcal{L}_{\gamma_{k, 2}}(\cdot).$$ <br>
(But why this form?)

**C-Closedness**: Three metrics differ by a multiplicative constant controlled by $C$. <br>
The three metrics are: squared weight norm $|x|^2$, squared gradient norm $|\nabla \mathcal{L}(x)|^2$, trace of noise covariance $Tr[\Sigma(x)]$.

## A condition for SDE approximation to hold. 

$$\eta \leq \frac{\overline{N}_{\infty}}{\overline{G}_{\infty}}(C^2 - 1).$$

## Model gradient descent as Levy process:

**Relevant paper**:

Claim: In (Cheng et al., 2020) that differences in the third-and-higher moments in SGD noise don't affect the test accuracy significantly, though the differences in the second moments do.

(Smith 2020) defined the **noise dominated regime** and **curvature dominated regime**. They showed experimentally that in noise dominated regime, the training properties, including the optimal LR are controlled by noise. 

PreResNet32: (He Kaiming, 2016)