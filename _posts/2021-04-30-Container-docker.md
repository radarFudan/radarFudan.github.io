---
layout: post
title: "Commands for docker"
date: 2021-04-30
---

## First time Commands

`nvidia-smi`

`docker images`

`docker container ls`

`docker run -it --gpus all --name shida_research_0 gcr.io/kaggle-gpu-images/python /bin/bash`

`docker cp ~/GitHub/pytorch-classification-master  shida_research_0:/`

## Continue the work

`docker container start shida_research_0`

`docker container attach shida_research_0`

## Reference

1. 