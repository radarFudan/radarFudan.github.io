---
layout: post
title: "paper reading: What is diffusion model?"
date: 2022-10-29
categories:
---

## Paper 

[Denoising Diffusion Probabilitistic Models](https://proceedings.neurips.cc/paper/2020/hash/4c5bcfec8584af0d967f1ab10179ca4b-Abstract.html)

[Denoising Diffusion Implicit Models](https://openreview.net/forum?id=St1giarCHLP)

[High-Resolution Image Synthesis with Latent Diffusion Models](https://openaccess.thecvf.com/content/CVPR2022/papers/Rombach_High-Resolution_Image_Synthesis_With_Latent_Diffusion_Models_CVPR_2022_paper.pdf)

## What is the problem / phenemenon?

Diffusion probabilistic models are used to generate high quality images. 

Based on the forward process that adding random noise to an image, the model is trying to "learn" the reverse process that reconstruct the image based on the random noise and the reverse noise adding operation.

The distribution $q(x_{t-1}|x_t)$ in reverse process is still Gaussian when the noise in forward process is small. 


## Why is it important / Why do we study it?





## Contribution of this paper / Main result of this paper?

1. 

2.

## Pros and Cons of this paper



## Reference / Further to read

1. Weng, Lilian. (Jul 2021). What are diffusion models? Lil’Log. https://lilianweng.github.io/posts/2021-07-11-diffusion-models/.

2. https://arxiv.org/abs/1503.03585

3. https://arxiv.org/abs/1907.05600

4. https://yang-song.net/blog/2021/score/

5. 