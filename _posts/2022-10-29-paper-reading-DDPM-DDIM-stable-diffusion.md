---
layout: post
title: "paper reading: What is diffusion model?"
date: 2022-10-29
categories:
mathjax: true
---

## Paper List

[Deep Unsupervised Learning using Nonequilibrium Thermodynamics](https://arxiv.org/pdf/1503.03585.pdf)

[Generative Modeling by Estimating Gradients of the Data Distribution](https://arxiv.org/pdf/1907.05600.pdf)

[Denoising Diffusion Probabilitistic Models](https://proceedings.neurips.cc/paper/2020/hash/4c5bcfec8584af0d967f1ab10179ca4b-Abstract.html)

[Denoising Diffusion Implicit Models](https://openreview.net/forum?id=St1giarCHLP)

[Pseudo Numerical Methods for Diffusion Models on Manifolds](https://arxiv.org/pdf/2202.09778.pdf)

[Fast Sampling of Diffusion Models with Exponential Integrator](https://arxiv.org/pdf/2204.13902.pdf)

[High-Resolution Image Synthesis with Latent Diffusion Models](https://openaccess.thecvf.com/content/CVPR2022/papers/Rombach_High-Resolution_Image_Synthesis_With_Latent_Diffusion_Models_CVPR_2022_paper.pdf)

[DPM-Solver: A Fast ODE Solver for Diffusion Probabilistic Model Sampling in Around 10 Steps](https://arxiv.org/pdf/2206.00927.pdf)

## What is the problem / phenemenon?

Diffusion probabilistic models are used to generate high quality images. 

Based on the forward process that adding random noise to an image, the model is trying to "learn" the reverse process that reconstruct the image based on the random noise and the reverse noise adding operation.

The distribution $q(x_{t-1}\vert x_t)$ in reverse process is still Gaussian when the noise in forward process is small. (DDPM)

## What is the difference between the loss function in Dickstein and Ho? 



## What are the improvements of different samplers?

DDPM -> DDIM -> PNDM -> DEIS -> DPM: 

## What is the meaning of stable in stable diffusion?



## Reference / Further to read

1. Weng, Lilian. (Jul 2021). What are diffusion models? Lil’Log. https://lilianweng.github.io/posts/2021-07-11-diffusion-models/.

2. https://yang-song.net/blog/2021/score/

3. https://github.com/acids-ircam/diffusion_models

4. 