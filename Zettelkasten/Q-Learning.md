Created on: 24-11-2025 14:14, note by Youssef Okeil
Status: #idea
Tags: #AI/reinforcement-learning 
# Q-Learning
> Q-Learning is an **off-policy value-based method that uses a TD approach to train its action-value function:**
- *Value-Based:* We find the optimal policy indirectly by training a value or action-value that will tell us the value of each state.
- *TD:* updates the *action-value function* after each step not at the end of the episode.
- *Off-Policy:*
	 ![[Pasted image 20251124163524.png|center|700]]

Q-Learning is the algorithm use to train our *Q-Function*. 
- *Q-Function* is an action-value function that takes as input the state and the action at that state and outputs a Q-value.
- *Q-table* has the value of each state-action pair. Given a state and an action, the Q-function will search inside its Q-table to output the value.

![[Pasted image 20251124160054.png| center | 600 ]]

> Q comes from the "Quality" (value) of the action at that state.

> We know that having an optimal Q-function, we will have an optimal policy.

## Pseudocode
```pseudo

Sarsamax (Q-Learning)
## Algorithm 14: Sarsamax (Q-Learning)

**Input:** policy π, positive integer *num_episodes*, small positive fraction α, GLIE {ϵᵢ}

**Output:** value function Q (≈ q* if *num_episodes* is large enough)

**Initialize** Q arbitrarily (e.g., Q(s,a) = 0 for all s ∈ S and a ∈ A(s), and Q(*terminal-state*, ·) = 0)

**for** i ← 1 **to** *num_episodes* **do**
  - ϵ ← ϵᵢ
  - Observe S₀
  - t ← 0
  - **repeat**
    - Choose action Aₜ using policy derived from Q (e.g., ϵ-greedy) *[Step 2]*
    - Take action Aₜ and observe Rₜ₊₁, Sₜ₊₁ *[Step 3]*
    - Q(Sₜ, Aₜ) ← Q(Sₜ, Aₜ) + α(Rₜ₊₁ + γ max_a Q(Sₜ₊₁, a) - Q(Sₜ, Aₜ)) *[Step 4]*
    - t ← t + 1
  - **until** Sₜ *is terminal*

**end**

**return** Q
```





-----------------
# References
[[Reinforcement Learning Hugging Face]]