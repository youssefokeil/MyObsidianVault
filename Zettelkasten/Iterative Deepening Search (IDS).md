Created on: 04-11-2025 00:07, note by Youssef Okeil
Status: #idea
Tags: #AI #algorithms 
# Iterative Deepening Search (IDS)
Execute the [[Depth-Limited Search (DLS)]] iteratively, by varying the depth limit with a very low depth limit and gradually increase the limit until a solution is found.

![[Pasted image 20251104000932.png|center]]

## Code:
```
function ITERATIVE-DEEPENING-SEARCH(problem) returns a solution, or failure
    for depth = 0 to ∞ do
        result ← DEPTH-LIMITED-SEARCH(problem, depth)
        if result ≠ cutoff then return result
```
> NB: [[Depth-Limited Search (DLS)]] returns $\{failure, solution, \text{or } cutoff\}$

## Pros:
- combines the benefits of depth-first and breadth-first search. 
## Cons:
- may seem wasteful, because states are generated multiple times. The bottom nodes are generated once, the next-to-bottom are generated twice and so on... until we reach the root.
$N (IDS) = (d)b + (d − 1)b^2 + · · · + (1)b^d$
## Complexity:
From the above the time-complexity is $O(b^d)$, similar to [[Breadth-First Search]] but with the extra cost of generating the upper levels multiple times

**Time Complexity:** 
$\Large{O(b^d)}$
**Space Complexity:**
$\Large{O(b.d)}$
b: branching factor, d: shortest solution length

> NB: In general, iterative deepening is the preferred uninformed search method when the search space is large and the depth of the solution is not known.
-----------------
# References
[[AI: A Modern Approach]]