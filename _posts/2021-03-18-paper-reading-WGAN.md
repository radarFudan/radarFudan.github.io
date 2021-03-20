---
layout: post
title: "paper reading: WGAN"
date: 2021-03-18
---

## Paper 3
[Wasserstein GAN](https://arxiv.org/abs/1701.07875)

## Earth-Mover distance or Wasserstein-1

$$W(\mathbb{P}_r, \mathbb{P}_g) = \inf_{\gamma \in \Pi(\mathbb{P}_r, \mathbb{P}_g)} \mathbb{E}_{(x, y) \sim \gamma} [\|x - y\|],$$

## Integral Probability Metrics(IPMs)

$$d_{\mathcal{F}} (\mathbb{P}_r, \mathbb{P}_{\theta}) = \sup_{f \in \mathcal{F}} \mathbb{E}_{x \sim \mathbb{P}_r} [f(x)] - \mathbb{E}_{x \sim \mathbb{P}_{\theta}} [f(x)]$$

as an integral probabilic metric associated with the function class $\mathcal{F}$. 

When every $f \in \mathcal{F}$ we have $-f \in \mathcal{F}$, combined with symmetricity and triangular inequality, we have $d_{\mathcal{F}}$ is a pseudometric over Prob($\mathcal{X}$).

**Relevant paper**

DCGAN(Deep convolutional GAN):

EBGAN(Energy-based GAN): 

Kantorovich-Rubinstein duality: Proof of the statement in paper can be found in a [note](https://courses.cs.washington.edu/courses/cse599i/20au/resources/L12_duality.pdf). 