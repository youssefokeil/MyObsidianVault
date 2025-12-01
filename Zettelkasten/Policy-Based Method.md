Created on: 05-10-2025 10:40, note by Youssef Okeil
Status: #idea
Tags: #AI/reinforcement-learning 
# Policy-Based Method

## Policy
The policy $\pi$ is the brain of our agent and is the function that tells us what action to take given the state we're in. It's a mapping from perceived states of the environment to actions to be taken when in those states.

## Policy-Based Method
by teaching the agent to learn which action to take, given the current state. We learn a policy function directly.

- **Deterministic** the function will define a mapping from each state to the best corresponding action, a policy at a given state will always return the same action.
$$a =\pi(s)$$
- **stochastic** probability distribution over set of actions, given the current state.
$$\pi(a|s) = P[A|s]$$


-----------------
# References
[[Reinforcement Learning Hugging Face]]