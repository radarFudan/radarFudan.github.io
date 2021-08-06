---
layout: post
title: "paper reading: GAN"
date: 2021-03-17
---

## Paper 2

[Generative Adversarial Networks](https://arxiv.org/abs/1406.2661)

It is a minimax two-player game: <br>
G: A generative model, capture the data distirbution <br>
D: A discriminative model, estimates the probability that a sample came from the data distribution rather than G. <br>
G's target is to maximize the probability for D to make a mistake.

Compare two kinds of models: <br>

1. GSN(Generative stochastic network)
2. Adversarial nets framework does not require a Markov chain for sampling

## Main contents of GAN

$D(x)$ represents the probability that $x$ came from the data rather than $p_g$.

$$\min_G \max_D V(D, G) = \mathbb{E}_{x \sim p_{data}(x)} [\log D(x)] + \mathbb{E}_{z \sim p_z(z)}[\log(1 - D(G(z)))].$$

The cost to fully train the inner loop(discriminator D) is too high, so we choose to go $k$ $D-$step and $1$ $G-$step.

Reference:

1. [Deep generative stochastic networks trainable by backprop](https://arxiv.org/abs/1306.1091)

2. https://lilianweng.github.io/lil-log/2017/08/20/from-GAN-to-WGAN.html
