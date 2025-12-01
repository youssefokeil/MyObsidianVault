Created on: 04-11-2025 15:25
Status: #idea 
Tags: #algorithms #AI
# Non-Deterministic Search
• Explores the tree in a random order
• Implementation identical to breadth-first, except that the list of paths is randomized before selecting which one to explore.

---
## Used for:
Random search can be better than [[Breadth-First Search]] or [[Depth-First Search]] in certain AI problem-solving scenarios, particularly when:
1. **Large or Infinite Search Space:** When the search space is vast or even infinite, random search can offer a practical alternative to exhaustively exploring every option as in breadth-first or depth-first searches. Random sampling can efficiently cover a large search space
2. **No Prior Knowledge:** In cases where there is no clear understanding of the structure of the search space, or the problem doesn't lend itself well to systematic exploration, random search can potentially stumble upon a solution faster than trying to every option (as in BFS or DFS)
3. **Time Constraints:** If time is limited and it's not feasible to perform an exhaustive search (like BFS), random search can sometimes yield results faster

---
## Implementation:
To conduct a nondeterministic search:
1. Form a one-element queue consisting of a zero-length path that contains only the root node
2. *Do Until* --> queue terminates at the goal node or depth limit is reached
	1. Create new paths by extending the first path to all neighbors of the terminal node.
	2. Reject all new paths with loops.
	3. Add the new paths if any, at *random places* of the queue. 
3. If the goal state is reached announce success and return the path, if not announce failure

---
## Complexity:
**Time Complexity:** 
$\Large{O(b^m)}$
**Space Complexity:**
$\Large{O(b^m)}$
b: branching factor, m: maximum depth for depth-first search


-----------------
# References
[[AI: A Modern Approach]]