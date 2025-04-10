Created on: 08-10-2023 19:18
Status: #idea
Tags: #control 
## Process-Control Diagram
This is the diagram of process-control. It works by comparing the measurement of the _controlled variable_ we want to change and the required set-point, then, manipulating a variable in the process(called the _manipulated variable_) till we reach the required set-point/reference value.
![[1_AlA-Y4zDx4Wh6lsgdn0-gg.jpg|600]]
## Practical Example:
- Process: filling juice bottles to a specific volume.
- Measurement: sensor measuring the juice volume (b).
- Error: difference between the reference point(set point) and the volume measure (b)
	e=r-b
- Controller: manipulates the error to enter the control element.
- [[Control Element]]: actuator in this case a valve controlling the volume flow rate(how much juice poured). 

-----------------
# References
[[System Dynamics & Control]]