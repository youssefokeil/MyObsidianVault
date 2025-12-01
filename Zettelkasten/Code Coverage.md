Created on: 07-10-2025 10:24, note by Youssef Okeil
Status: #idea
Tags: #verification 
# Code Coverage
> code-coverage is a degree to which code has been executed by a set of test cases. 

## Types of Code Coverage
- **[[Statement Coverage]]**: This measures the percentage of code statements that have been executed during the simulation.
- **Branch coverage**: This measures the percentage of decision points in the code that have been exercised by the testbench.
- **Condition coverage**: This measures the percentage of Boolean conditions in the code that have been tested.
- **Expression coverage**: This measures the percentage of expressions that have been executed.
- **Toggle coverage**: This measures the percentage of signal transitions that have been observed during the simulation.
- **Path coverage**: This measures the percentage of paths through the code that have been executed.
- **Finite State Machine (FSM) coverage**: This measures the percentage of states and transitions in the FSM that have been exercised.
### How to generate code coverage?
A testbench is created that contains RTL design and set of test vectors that exercise the design. Testbench is run through a simulation tool and coverage data is collected. 

### Limitations:
**it's not enough alone:**
- it doesn't ensure that the executed code is correct, it only says that it was executed
- a test can execute code without actually verifying anything. Quality testing means
	- *Assertions* that verify correct behavior
	- *Multiple test cases* covering different scenarios
	- *Edge Cases* 
	- *Meaningful validation* of outputs
- doesn't measure quality of design itself, it only measures the amount of code that was executed and doesn't indicate whether the design is efficient, or scalable.

-----------------
# References
https://www.chipverify.com/verification/code-coverage