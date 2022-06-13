---
layout: post
title: "Pytorch and TensorFlow"
date: 2022-02-14
---

## Simple tutorials



## Classical demos



## GPU allocation

[link](https://stackoverflow.com/questions/34199233/how-to-prevent-tensorflow-from-allocating-the-totality-of-a-gpu-memory)



## Reproducibility

Here are some references I read when I need to fix the reproducibility in PyTorch. 

To summarize:

1. Random seed

2. GPU floating-point discrepancy

3. Nondeterministic algorithms (This one is usually associated with the GPU and the ML framework and correpsonding operators)

4. Hyperparameter inconsistency and changes in data (manual factor)


#### References

1. https://pytorch.org/docs/stable/notes/randomness.html

2. https://pytorch.org/docs/stable/data.html#data-loading-randomness

3. https://stackoverflow.com/questions/61718947/when-does-dataloader-shuffle-happen-for-pytorch

4. https://docs.nvidia.com/cuda/cublas/index.html#cublasApi_reproducibility
