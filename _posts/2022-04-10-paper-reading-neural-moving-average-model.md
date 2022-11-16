---
layout: post
title: "paper reading: The Neural Moving Average Model for Scalable Variational Inference of State Space Models"
date: 2022-04-10
categories:
---

## Paper 11

[The Neural Moving Average Model for Scalable Variational Inference of State Space Models](https://proceedings.mlr.press/v161/ryder21a/ryder21a.pdf)

## What is neural moving average model?

To achieve the locality property we introduce the neural moving average (nMA) model. This is **a generative model for sequence data** in which a learnable convolutional neural network (CNN) processes (1) an underlying sequence of base N(0,1) variables and (2) the sequence of observed data.

By viewing the nMA model as a type of normalising flow, we show later that the mini-batch samples can be used to unbiasedly estimate the log-density of the whole x chain, which is crucial to implement variational inference.

## Why do we need it?

No idea...

## What's the assumptions of the improvement?

Using a nMA as the variational approximation assumes no long-range depend- ence in the posterior for x.

## Contribution of this paper / Main result of this paper?

1. We propose an extension to state space models of time series data based on a novel generative model for latent temporal states: the neural moving average model.

2. This permits a subsequence to be sampled without drawing from the entire distribution, enabling training iterations to use mini-batches of the time series at low computational cost.

3. We illustrate our method on several examples to **achieve accurate parameter estimation in a short time**.

4. They compare their methods with MCMC. 

## Reference

