---
layout: post
title: "paper reading GAN"
date: 2021-03-17
---

Paper 2
[Generative Adversarial Networks](https://arxiv.org/abs/1406.2661)

It is a minimax two-player game:

G: A generative model, capture the data distirbution

D: A discriminative model, estimates the probability that a sample came from the data distribution rather than G.

G's target is to maximize the probability for D to make a mistake. 

Compare two kinds of models: 

1. GSN(Generative stochastic network)

2. Adversarial nets framework does not require a Markov chain for sampling

Main contents of GAN

$$ E = m\cdot c^2 \label{eq:mc2}$$
$$E = M \cdot c^2$$
$E = M \cdot c^2$
\[E = M \cdot c^2\]

Reference:
1. [Deep generative stochastic networks trainable by backprop](https://arxiv.org/abs/1306.1091)
2. 