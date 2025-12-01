Created on: 25-09-2025 13:35, note by Youssef Okeil
Status: #idea
Tags: #verification #siemens #SysVerilog
# Constraint Random Verification
>  generates random test cases with specific constraints to ensure that the design meets design requirements

### Types of Constraints?
- timing constraints
- data ranges
- interface protocols
## Examples:
we use SystemVerilog's `randomize()` function. We define constraints on the random values we define. Here the constraints are:
1. A and B are in the range 0-15
2. output C should be 0-31
3. adder should operate correctly for all possible combinations of A and B
4. adder should operate correctly for both signed and unsigned inputs.

```verilog
class Adder;

  // Define the inputs and output
  rand bit [3:0] A, B;
  rand bit [4:0] C;

  // Define the constraints
  constraint c_adder { 	A inside {[0:15]};
  						B inside {[0:15]};
  						C == A + B;
					}

  function void display();
    $display("A=0x%0h B=0x%0h C=0x%0h", A, B, C);
  endfunction
endclass

module tb;

  initial begin
	Adder m_adder = new();

	// Generate A and B randomly with the constraint that A and B cannot be the same
	m_adder.randomize() with { A != B };

	m_adder.display();
  endfunction

endmodule
```
## Pros:
- covers a wide range of scenarios, identifying design bugs that aren't detected by other verification techniques
- **Scalability*:**  can generate millions of testcases easily to cover more complex designs. It can verify designs of different complexities.

## Limitations:
- **Complexity:** as design becomes more complex, it becomes difficult to define constraints that capture design requirements. 
- **Debugging:** with randomized test cases, it can be more difficult to isolate and debug failing tests. It's  challenging to debug root cause.
- **Coverage:** it can not always guarantee that all scenarios have been covered. In some cases, additional test cases may need to be added to ensure full coverage.
- **Performance:** for performance-critical designs, direct tests are more appropriate.
* **Scalability:** for very large designs, random tests are very computationally expensive and a lot of memory.





-----------------
# References
https://www.chipverify.com/verification/constraint-random-verification