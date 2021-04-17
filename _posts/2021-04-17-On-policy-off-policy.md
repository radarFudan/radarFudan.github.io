---
layout: post
title: "What is on-policy and what is off-policy"
date: 2021-04-17
---

A reinforcement learning system consists of agent, policy, reward signal and value function. 

## Definition

*On-policy:*

1. training samples are collected according to the target policy. 

For example, **SARSA**(staet-action-reward-state-action) is an on-policy learner. 

*Off-policy:*

1. The off-policy approach does not require full trajectories and can reuse any past episodes (experience replay) for much better sample efficiency.

2. The sample collection follows a behavior policy different from the **target policy**, bringing better exploration.

3. It is independent of agent's actions.

For example, **Q-learning** is off-policy learner.

## Explanation and comparison

From reference 2: *The distinction disappears if the current policy is a greedy policy. However, such an agent would not be good since it never explores.*

The difference is this: <br>
In on-policy learning, the $Q(s, a)$ function is learned from actions that we took using our current policy $\pi(a | s)$. <br>
In off-policy learning, the $Q(s, a)$ function is learned from taking different actions (for example, random actions). We even don't need a policy at all.

## Reference:

1. https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html

2. https://stats.stackexchange.com/questions/184657/what-is-the-difference-between-off-policy-and-on-policy-learning

3. https://stackoverflow.com/questions/6848828/what-is-the-difference-between-q-learning-and-sarsa/41420616#41420616

4. https://towardsdatascience.com/on-policy-v-s-off-policy-learning-75089916bc2f

5. https://analyticsindiamag.com/reinforcement-learning-policy/

