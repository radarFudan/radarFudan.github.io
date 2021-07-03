---
layout: post
title: "Commands for docker"
date: 2021-04-30
---

## First time Commands

`nvidia-smi`

`docker images`

`docker container ls`

Running the run command with the -it flags attaches us to an interactive tty in the container. <br>
`docker run -it --gpus all --name shida_research_0 gcr.io/kaggle-gpu-images/python /bin/bash`

`docker ps`

`docker ps -a` <br>
To do that, you can run the `docker rm` command. Just copy the container IDs from above and paste them alongside the command.

`docker cp ~/GitHub/pytorch-classification-master  shida_research_0:/`

## Continue the work

`docker container start shida_research_0`

`docker container attach shida_research_0`

## Reference

1. https://docs.docker.com/get-started/

2. https://docker-curriculum.com/#docker-run
