Created on: 27-02-2025 03:28
Status: #idea
Tags: #AI #machinelearning 
# Concept Learning
>The problem of searching through a predefined space of possible hypotheses for a hypothesis that best fits the data.

It's based on a _inductive learning_, where a learner learns by example. The learner discovers the rules of a concept by seeing examples of that concept.

------
### Aim:
is to find a function that generalizes well on unseen data. Using the Inductive Learning Hypothesis.  Which indicates that we can learn from training data.![[Inductive Learning Hypothesis#Inductive Learning Hypothesis]]

### Representation of hypotheses:
Each hypothesis is defined with two features, each feature has a value and each value has a constraint. There are 3 types of constraints.
- **Single-value constraint:** that value is the only one value is acceptable. Fixed value associated with a feature. For example "age=18"
- **The general constraint:** That any value is acceptable for that feature. Meaning that this feature is not important for the final outcome. Written using the question mark symbol "?". For example "nationality=?".
- **The specific constraint:** Meaning that no value is acceptable for that feature. Represented with a phi symbol or a "0". For example for a job intended for students we can put a feature "work=0", meaning that the applicant doesn't have any other job.



-----------------
# References
[Concept Learning: Key to Better and Faster Decisions!](https://www.analyticsvidhya.com/blog/2023/03/concept-learning-key-to-better-and-faster-decisions/#What_is_Concept_Learning?)
