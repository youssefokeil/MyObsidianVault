Created on: 03-11-2025 23:34, note by Youssef Okeil
Status: #idea
Tags: #AI #algorithms 
# Depth-Limited Search (DLS)
on of the problems of [[Depth-First Search]] is that it can look for very deep paths to reach the goal. 

DFS are looking too deep by restricting the depth of any path to a certain limit.
![[Pasted image 20251103234749.png]]
To conduct a depth-limited search:
1. Form a one-element queue consisting of a zero-length path that contains only the root node
2. *Do Until* --> queue terminates at the goal node or depth limit is reached
	1. Create new paths by extending the first path to all neighbors of the terminal node.
	2. Reject all new paths with loops.
	3. Add the new paths if any, to the *front* of the queue.
3. If the goal state is reached announce success and return the path, if not announce failure
![[Pasted image 20251104000008.png]]
## Pros:
- [[Depth-First Search]] can look very deep paths to reach goal, while goal can be be reached by a few steps only. Depth-Limited prevents DFS from looking very deep.
## Cons:
- adds an additional source of [[incompletneness]], as $l < d_g$, for depth limit is $l$ and $d_g$ is the shallowest goal.
- [[non-optimal]] when we choose $l > d_g$

> NB: depth-first search is a special case of depth-limited search when $l=\infty$

## Complexity:
**Time Complexity:** 
$\Large{O(b^L)}$
**Space Complexity:**
$\Large{O(b.L)}$
b: branching factor, L: depth limit

-----------------
# References
[[AI: A Modern Approach]]