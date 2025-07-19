Created on: 15-04-2024 07:23
Status: #idea
Tags: #AI #AI/fastai #AI/deeplearning 
# 1cycle Training
 is a learning rate scheduling technique developed by Leslie N. Smith, following up on his previous paper [[Cyclical Learning Rates]].

The idea simply around 1cycle training is a schedule that takes two steps. One where the learning rate increases **(warm-up)** and one where it decreases back to a minimum **(cool-down)**. 

There's an extra phase that is optional if you want to increase your accuracy but hurt the speed of learning called the annihilation phase. Represented as a tail in the graph.

![[1__7CeyMZaolYgmfgbl85dqg.webp]]

## Pros:
- Higher learning rates mean faster training. Something we'd like to call **super-convergence.**
- Higher learning rates lets the model generalize better instead of being stuck in a sharp local minima. The model tries to find smoother minima.
- Exploring the learning terrain. By increasing the learning rate, the model is more likely to skip saddle points and find other regions and minima. 

check fastai's [[one_cycle_training]] & Leslie's follow-up [[Disciplined  Approach to Hyperparameters]]

-----------------
# References
[[Deep Learning For Coders]]