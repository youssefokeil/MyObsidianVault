Created on: 05-10-2025 10:53, note by Youssef Okeil
Status: #idea
Tags: #AI/reinforcement-learning 
# Value-Based Methods
> instead of a policy function like the [[Policy-Based Method]], we learn a value function that maps a state to the expected value of being at that state. We define the policy by hand and we learn the value function. If we have an optimal value function, we will have an optimal policy..

## Value
The value of the state is the expected discounted return that the agent can get if it starts at that state, and acts according to our policy.

$$v_{\pi}(s)=E_{\pi}[R_{t+1}+\gamma R_{t+2} +\gamma^{2} R_{t+3}+...|S_{t}=s]$$

![[Pasted image 20251005110504.png]]
As you can notice, every state has a value based on our value function!

Values are **secondary**, while **rewards** are primary. Estimating values are to achieve more reward, there's no point of values if there's no reward.

Value estimation is central in reinforcement learning, as we seek actions that bring states of highest value not highest reward. This is also a much harder problem to determine values than to determine rewards, as rewards are given by the environment, while values are estimated and re-estimated from agent's observations over its lifetime.

## Types of Value-Based Functions:
1. **State-value Function:** the expected return if the agents *starts at a given state* and acts according to the policy forever after.
2. **Action-Value Function:** outputs the expected return if agent *starts at a given state and takes an action at that state.* And then acts according to the policy forever after.

## Methods to Update the Value Function:
1. [[Monte-Carlo Method]], update after the completion of a full episode.
2. [[TD-Learning]] update value function from a step, replacing the unknown $G_t$ the an estimated return called the TD target.

-----------------
# References
[[Reinforcement Learning Hugging Face]]