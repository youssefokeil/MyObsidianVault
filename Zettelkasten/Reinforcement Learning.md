Created on: 05-10-2025 09:28, note by Youssef Okeil
Status: #idea
Tags: #AI/reinforcement-learning
# Reinforcement Learning
> an agent will learn from the environment by interacting with it through trial and error, receiving awards (negative or positive) as feedback from performing actions.

> **NB:** Reinforcement Learning differs from other machine learning methods in several ways. The data used to train the agent is collected through interactions with the environment by the agent itself (as opposed to, for example, supervised learning where you have a fixed dataset).

This is how animals and humans learn, through interaction. Reinforcement learning is just a computational approach of learning from actions.

## Formal Definition:
> Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback.

![[Pasted image 20251005093148.png]]
1. agent receives state $S_0$ from the environment
2. based on state $S_0$, the agent takes action $A_0$ (move to right, for example)
3. the environment goes to new state $S_1$
4. environment gives some reward $R_1$ to the agent
## The reward hypothesis
the reward hypothesis is a central idea of reinforcement learning, as the goal is to maximize the expected return (expected cumulative reward).

## Markov Decision Process
RL is called a [[Markov Decision Processes (MDP)]], as it only needs the current state to decide what action to take.

## States/observations:
a **state** $s$ is a complete description of the world, while an **observation** $o$ is a partial description of the world.

## Action Space
is the set of all possible actions in an environment.
- $\text{Discrete Space}$: number of possible actions is finite (up, down, right, left)
- $\text{Continuous Space}$: number of possible actions is infinite
## Discounting Rewards
**the cumulative reward is** $$R(\tau)= r_{t+1} + r_{t+2} + r_{t+3}+ ...$$
however, the reward is a lot of times discounted by a gamma $\gamma$ between 0 and 1. In order to maximize long-term reward. The smaller the gamma, the bigger the discount. 

**the discounted reward is** 
$$R(\tau)=r_{t+1}+\gamma r_{t+2} + \gamma^{2}r_{t+3}+...$$


-----------------
# References
[[Reinforcement Learning Hugging Face]]