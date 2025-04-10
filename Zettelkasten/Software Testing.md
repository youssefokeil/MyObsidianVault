Created on: 10-04-2025 18:09
Status: #idea
Tags: #software
# Software Testing
>Executing a program with a finite set of cases and verifying if  they deliver the expected results.

### Types of testing:
1. Unit Testing
	testing small code units like a class
2. Integration tests
	Testing larger units like a set of classes
3. Performance tests
	Checking system performance under specific loads
4. Usability tests
	Evaluating the usability of the system's user interface.

### Purposes of testing:
1. __Verification purposes__
	- system conforms to its specifications. Are we building the product right, according to the specification we received?
	- Ex: testing if a method is returning the correct result.
2. __Validation purposes__
	- Are we building the right product, that meets the customer or market needs?
	- Ex: making a meeting with customer to show him the product.

### Bug, Defect and Failure:
- bug and defect have the same meaning
- failure only occurs when the defective code is executed
- defective code doesn't conform to its specifications (will be handled in verification), if that code is executed a failure occurs.
```
if (condition)
    area = pi * radius * radius * radius; 
```

- in the above code area is specified in a wrong way, this is a defective code
- if condition is true, a failure occurs
-----------------
# References
[[Software Engineering:  A Modern Approach]]