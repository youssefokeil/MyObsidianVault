Created on: 04-11-2025 15:39
Status: #idea 
Tags: #algorithms #AI 
# Bi-Directional Search
Run two simultaneous searches, one forward from initial state and one backward from goal.

**The  motivation:** That $\Large{b^{\frac{d}{2}} +b^{\frac{d}{2}}}$ is much less than $\Large{b^{d}}$ . The area of two small circles is less than the area of a big one.

![[Pasted image 20251104160331.png]]

---
## Used for:
In many cases bidirectional search is faster, because it dramatically reduces the time and space required for exploration.
- when both initial and goal states are unique and completely defined
> **NB:** if there are several explicitly listed goal states, for example two goal states, then we can make a *dummy goal state* where its immediate predecessors are all the actual goal states.
- branching factor is the same in both directions

---
## Implementation:
Two searches are executed using [[Breadth-First Search]] usually, from the goal state and initial state. We stop when we reach an intersection, where the two paths meet.

---
## Complexity:
**Time Complexity:** $\Large{O(b^{d/2})}$
**Space Complexity:** $\Large{O(b^{d/2})}$

$\large{b : \text{branching factor}, d : \text{shortest solution length}}$

-----------------
# References
[[AI: A Modern Approach]]