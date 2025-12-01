Created on: 03-11-2025 22:38, note by Youssef Okeil
Status: #idea
Tags: #AI
# State-Space Representation Problem
after making the [[Well-Defined Problems|formal definition of the problem]], we make a graph where:
- **nodes** are *states*
- **links** between nodes are *actions*
- **path** is a sequence of states connected by sequence of actions.
- *states* appear only once in the graph (removing loops)

## Problem Solving Using State-Space Representation:
The following must be specified first:
1. **General State Representation**
	how to represent the state? Ex: for the [[Sliding-Block Puzzles]] ![[Sliding-Block Puzzles#Sliding-Block Puzzles]]
	it can be represented like a list \[7,2,4,5, _ , 6, 8, 3, 1] or a list of lists like   \[\[7,2,4], 
	\[5, \_, 6], 
	\[8,3,1]]. 
	Notice that the list of lists is better for human understanding, and will be probably easier to code actions this way, but the list of lists may achieve more optimal performance to use a list. 
2. **Initial State**
	what is the initial state of our problem? in our example it's the list (or list of lists) above
3. **Goal State**
	which state/expression will we compare our states to, to make sure we have reached the goal state. In our example, it will be (if we use a list)
	the goal states are {\[\_,1,2,3,4,5,6,7,8],\[1,2,3,4,5,6,7,8,\_]}
4. **Actions**
	the defining problem rules that a state can apply to reach another state. Inn our example it's the blank space moving *up,down,right,left* if it's in the middle & exclude right if it's in the rightmost edge, up when we're in the upmost edge and so on ...



-----------------
# References
[[AI: A Modern Approach]]