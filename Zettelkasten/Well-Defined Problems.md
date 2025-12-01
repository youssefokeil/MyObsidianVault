Created on: 03-11-2025 16:10, note by Youssef Okeil
Status: #idea
Tags: #AI
# Well-Defined Problems
A problem can be *formally defined* by 5 components, consider an example of going to Alexandria from Cairo:
1. An **initial state** that agent starts from. 
	1. Ex: $In(Cairo)$ 
2. A description of the possible **actions** available to the agent, given a particular state $s$. $Actions(s)$ returns the set of actions that can be executed in $s$. 
	1. Ex: $Actions(Cairo) = \{Go(Daaery), Go(Train), Go(zeraay)\}$
3. **Transition model**, which is a description of what each action does. Specified by function $Result(s,a)$, which returns the state that results from doing action $a$ in state $s$.
	1. Ex: $Result(In(Cairo), Go(Daaery)) = In(Zayed)$, $In(Zayed)$ is called a **successor** which refers to any state reachable from a given state ($In(Cairo)$) by a single action $(Go(daaery))$.
4. **Goal test**, which tests whether we reached the goal state or not. Sometimes there are a set of goal states, and the test checks whether the given state is one of them. Other times the goal state is more abstract property.
	1. Ex: In our example the set is --> $\{In(Alexandria)\}$
5. **Path cost** function, which assigns a numeric cost to each path. The problem-solving agent chooses a cost function that reflects its own performance measure. We assume that cost of a path can be described as the sum of cost of individual actions along the path (**step cost**). 
	1. The step cost of taking action $a$ in state $s$ to reach state $s'$ is $c(s,a,s')$

A **solution**, is a series of actions that leads from initial state to goal state. 
An **optimal solution**, is one that has the lowest path cost among all solutions.

-----------
### Abstraction
We remove detail from a representation (called **abstraction**) like: 
1. Abstracting the state representation, the state of the world includes so many things:
	- traveling companions
	- radio program
	- scenery out of the window
	- proximity of law enforcement officers
	- distance to next rest stop
	- weather
	- condition of the road
2. abstracting actions, themselves. We represent driving as only changing location of vehicle and occupants & we abstract:
	- fuel consumption
	- pollution 
3. We remove actions altogether like:
	- turning on the radio
	- slowing down for law enforcement officers
-----------------
#### The appropriate level of abstraction:
Abstract states and actions encompass large detailed world states and detailed action sequences. 

The abstract state may be: going from Cairo to Zayed, then moving to Sahrawy and reaching Alexandria.

A detailed state, may include: switching the radio on till we reach Zayed, then playing Dalida till we reach Alexandria.

*Valid* abstraction is when were we can expand any abstract solution into a solution in the detailed world.

The abstraction is *useful*, if carrying out any of the "detailed" actions is easier than the original problem actions.

-----------------
# References
[[AI: A Modern Approach]]