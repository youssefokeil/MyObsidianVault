Author: [[Rich Sutton]], [[Andrew Barto]]
Type: #TextBook 
Fields: #AI/reinforcement-learning 
# Reinforcement-Learning by Sutton & Barto 📚

## Chapter 1
### 1.1 Reinforcement Learning
It is a way of learning what to do to map situations/states to actions in order to maximize a reward signal. 

#### Difference from other machine learning approaches
Reinforcement Learning is different from [[Supervised Learning]] as it doesn't have labeled data by an external supervisor, the point of supervised learning is that the system will extrapolate its knowledge on unseen data. This however is very different from reinforcement learning as it will mean that an external supervisor will label each action the agent might take as desirable or undesirable. This is impractical, inefficient and probably impossible to happen in complex environments. 

Reinforcement Learning is also very different from [[Unsupervised Learning]], in unsupervised learning we find structure in collections of unlabeled data. Reinforcement Learning is more about maximizing a reward signal than finding hidden structure, by every step the agent is trying to do an action that will maximize this signal. 

![[Exploration-Exploitation trade-off#Exploration-Exploitation trade-off]]

### 1.2 Examples of Reinforcement Learning
- A chess player chooses his next move; this decision is based on the desirability of a particular position and move, the expectation of replies from the opponent and countering those replies.
- A cleaning robot chooses between cleaning another room, or getting back to the docking station; the decision is informed by the current battery level, the anticipation of how much time it'll take in the room and how far away it's from the docking station.

**Those examples have two important characteristics:**
1. The outcomes of the actions can't be fully predicted.
2. It involves an interaction between a decision-making agent and an environment. The agent seeks to achieve a goal despite uncertainties about the environment.
3. Important note: there is not always a clear separation between agents and environment. In the cleaning robot example, the robot's battery is a part of the environment of the controlling agent.
4. The agent uses its experience to improve its performance over time. The chess player improves his model about human behavior and decision-making intuition, the robot learns about its environment. This is what we call that the agent has explored the environment in order to exploit it afterwards.

### 1.3 Elements of Reinforcement Learning
1. **Agent** 
2. **Environment**
3. **Policy $\pi$ 
![[Policy-Based Method#Policy]]
4. **reward signal**
![[Reward Signal#Reward Signal]]

5. **value function $v_{\pi}$** 
![[Value-Based Methods#Value]]
 Rewards tell us what's desirable in the immediate, intrinsic sense, while values are what's desirable in a long-term after taking into account the states that are likely to follow. 

6. **(optional) model of the environment**
![[Model of The Environment#Model of The Environment]]

### 1.4 Limitations and Scope
The point of this book is to study reinforcement learning methods structured around estimating value functions. 

We don't work on 
![[Evolutionary Methods#Evolutionary Methods]]

This, however, isn't a very good approach as it doesn't make use of the way that policies are functions from states to actions. It ignores a lot of the useful structure reinforcement learning uses. 

We also study functions that don't appeal to value functions like:
![[Policy Gradient Methods#Policy Gradient Methods]]

> NB: Reinforcement Learning is connected [[Optimization Method]]s but it doesn't ensure optimality, it just means that the agent is trying to maximize a reward signal.

