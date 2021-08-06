---
layout: post
title: "paper reading: Extended dynamic mode decomposition with dictionary learning"
date: 2021-03-22
---

## Paper 5

[EDMD](https://aip.scitation.org/doi/10.1063/1.4993854)

I learned about this paper from a group seminar, I'll try to write down the main ideas to better understand the paper.

## Dynamic Mode Decomposition

It is a numerical procedure for extracting dynamical features from flow data:

$$V_1^N = \{v_1, v_2, \dots, v_N\},$$

$$v_{i+1} = Av_i,$$

$$V_2^N = AV_1^{N-1} + re_{N-1}^T,$$

Regardless of the approach, the output of DMD is the eigenvalues and eigenvectors of
$A$, which are referred to as the DMD eigenvalues and DMD modes respectively.

## Extended Dynamic Mode Decomposition

Extended DMD is a modification of Exact DMD that strengthens the connection between DMD and the Koopman operator. As the name implies, Extended DMD is an extension of DMD that uses a richer set of observable functions to produce more accurate approximations of the Koopman operator. It also demonstrated the DMD and related methods produce approximations of the Koopman eigenfunctions in addition to the more commonly used eigenvalues and modes.

## Dictionary Learning

Given a set of inoput data, $X = (x(1), x(2), \dots, x(N)) \in \mathbb{R}^{d \times N}$, we wish to find a sparse represeantation of it in the form of $X = DK$, where $D \in \mathbb{R}^{d \times M}$ is a size-$M$ set of dictionary vectors and $K \in \mathbb{R}^{M \times N}$ is a sparse representation.

## Main results

EDMD-DL: EDMD with dictionary learning.

## Reference:

1. https://en.wikipedia.org/wiki/Dynamic_mode_decomposition
