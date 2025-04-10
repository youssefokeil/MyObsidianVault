Created on: 08-10-2023 19:57
Status: #idea
Tags: #control
## Evaluation Criteria:
 **Damping Response**: 
  It requires that the controlled variable is of one-polarity (doesn't oscillate about the set-point) for any change whether it was a _transient effect_ or _set-point change_. We measure the quality of this response with:
   ![[Screenshot (15).png|300x300]]
	1. Damping time:
		- In transient effects: time from the start of disturbance till the controlled variable falls within 4% of the reference.
		- For set-point change: the time for the controlled variable to go from 10% to 90% of difference between new set-point and the old one. $$t_{D}\text{ :  damping time}$$
	2. Maximum error:
		  In transient effects it's the maximum deviation from the reference. $$e_{max}\text{: maximum error}$$
 **Cyclic Response:** 
	It applied to the case where the controlled variable oscillates about the setpoint for any change. We measure the quality by:
	![[Screenshot (16).png|300x200]]
	1. Settling time: duration from the time the allowable error was exceeded till it falls within it and stabilizes. $$t_{S}:\text{ settling time}$$
	2. Maximum error: $$e_{max}:\text{maximum error}$$
    **Tuning:** 
	nature of response is modified by controlling the parameters of the loop. Sometimes we want less maximum error on the expense of a shorter settling time. For cycling tuning we use a couple of parameters:
	![[Screenshot (17).png|300x200]]
	1. Minimum area $$A=\int |e(t)| dt$$
	2. Quarter-amplitude : each peak is one-fourth of the peak before it$$a_{2}=a_{1}/4 $$

-----------------
# References
[[System Dynamics & Control]]