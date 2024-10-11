---
layout: post
title: "paper reading: What is diffusion model?"
date: 2022-10-29
categories: Research
mathjax: true
---

## Paper List

[Estimation of Non-Normalized Statistical Models by Score Matching](https://www.jmlr.org/papers/volume6/hyvarinen05a/hyvarinen05a.pdf)

[Deep Unsupervised Learning using Nonequilibrium Thermodynamics](https://arxiv.org/pdf/1503.03585.pdf)

[Generative Modeling by Estimating Gradients of the Data Distribution](https://arxiv.org/pdf/1907.05600.pdf)

[Denoising Diffusion Probabilitistic Models](https://proceedings.neurips.cc/paper/2020/hash/4c5bcfec8584af0d967f1ab10179ca4b-Abstract.html)

[Denoising Diffusion Implicit Models](https://openreview.net/forum?id=St1giarCHLP)

[Pseudo Numerical Methods for Diffusion Models on Manifolds](https://arxiv.org/pdf/2202.09778.pdf)

[Fast Sampling of Diffusion Models with Exponential Integrator](https://arxiv.org/pdf/2204.13902.pdf)

[High-Resolution Image Synthesis with Latent Diffusion Models](https://openaccess.thecvf.com/content/CVPR2022/papers/Rombach_High-Resolution_Image_Synthesis_With_Latent_Diffusion_Models_CVPR_2022_paper.pdf)

[DPM-Solver: A Fast ODE Solver for Diffusion Probabilistic Model Sampling in Around 10 Steps](https://arxiv.org/pdf/2206.00927.pdf)

[Diffusion Models: A Comprehensive Survey of Methods and Applications](https://arxiv.org/pdf/2209.00796.pdf)

## What is the problem / phenemenon?

Diffusion probabilistic models are used to generate high quality images. 

Based on the forward process that adding random noise to an image, the model is trying to "learn" the reverse process that reconstruct the image based on the random noise and the reverse noise adding operation.

The distribution $q(x_{t-1} \vert x_t)$ in reverse process is still Gaussian when the noise in forward process is small. (DDPM)

## What is the difference between the loss function in Dickstein and Ho? 

Dickstein - maximize the model log likelihood by maximizing the lower bound negative log likelihood $K$:

$$ L = \int d \mathbf{x}^{(0)} q(\mathbf{x}^{(0)}) \log p(\mathbf{x}^{(0)}) = \int d \mathbf{x}^{(0)} q(\mathbf{x}^{(0)}) \log \left [ \int d\mathbf{x}^{(1 \dots T)} q(\mathbf{x}^{(1 \dots T)} | \mathbf{x}^{(0)}) p(\mathbf{x}^{(T)}) \prod_{t=1}^T \frac{p(\mathbf{x}^{(t-1)} | \mathbf{x}^{(t)})}{q(\mathbf{x}^{(t)} | \mathbf{x}^{(t-1)})}\right ].$$

$$ K = - \sum_{t=2}^T \int d \mathbf{x}^{(0)} d \mathbf{x}^{(t)} q(\mathbf{x}^{(0)},\mathbf{x}^{(t)}) D_{KL} \left ( q(\mathbf{x}^{(t-1)} | \mathbf{x}^{(t)} , \mathbf{x}^{(0)}) | | p(\mathbf{x}^{(t-1)} | \mathbf{x}^{(t)})\right ) + H_q(\mathbf{x}^{(T)}| \mathbf{x}^{(0)}) - H_q(\mathbf{x}^{(1)} | \mathbf{x}^{(0)}) - H_p(\mathbf{x}^{T}).$$

Ho:

$$ K = \mathbb{E}_q \left [ D_{KL} \left ( q(\mathbf{x}_T | \mathbf{x}_0 ) | | p(\mathbf{x}_T) \right ) + \sum_{t > 1} D_{KL}(q(\mathbf{x}_{t-1} | \mathbf{x}_t, \mathbf{x}_0) | | p_\theta(\mathbf{x}_{t-1} | \mathbf{x}_t)) - \log p_\theta(x_0 | x_1) \right ]$$

Only the middle parameterized term is necessary to be minimized

$$ L_{simple} =\mathbb{E}_{t, \mathbf{x}_0, \mathbf{\epsilon}} \left [ \| \mathbf{\epsilon} - \mathbf{\epsilon}_{\theta} (\sqrt{\bar{\alpha}_t} \mathbf{x}_0 + \sqrt{1-\bar{\alpha}_t} \mathbf{\epsilon}, t)\|^2 \right ] .$$


## What are the improvements of different samplers?

$ DDPM -> DDIM $

First, the forward process is considered from another perspective that is non-markovian: 

$$q_\sigma(\mathbf{x}_{1:T} | \mathbf{x}_0) = q_\sigma(\mathbf{x}_T | \mathbf{x}_0) \prod_{t=2}^T q_{\sigma}(\mathbf{x}_{t-1} | \mathbf{x}_t, \mathbf{x}_0)$$

During generation, we only sample a subset of $S$ diffusion steps $\{\tau_1, \dots, \tau_S \}$.

$ -> PNDM $



$ -> DEIS $

$ -> DPM$

## What is the meaning of stable in stable diffusion?

I don't see anything `stable' in the paper, it's not a good name... 
The previous name is latent diffusion. 

## Conditioned generation

Based on score approach, there is a text-guided generation which generate the data conditioned on some text input. 

## Reference / Further to read

1. Weng, Lilian. (Jul 2021). What are diffusion models? Lil’Log. https://lilianweng.github.io/posts/2021-07-11-diffusion-models/.

2. https://yang-song.net/blog/2021/score/

3. https://github.com/acids-ircam/diffusion_models

4. 

