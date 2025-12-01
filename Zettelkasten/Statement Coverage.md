Created on: 07-10-2025 12:46, note by Youssef Okeil
Status: #idea
Tags: #verification
# Statement Coverage
> type of code coverage that measures percentage of code **statements** executed during simulation.

### What is a statement?
> a single unit of code that performs an action or operation. It's the smallest standalone element of a program that can be executed.

```verilog
x = 5                    # One statement
name = "Alice"           # One statement
total = price + tax      # One statement

```

### Example:
```python
def check_number(num):
    result = "Processing"     # Statement 1
    
    if num > 0:               # Statement 2
        result = "Positive"   # Statement 3
    else:
        result = "Non-positive"  # Statement 4
    
    return result             # Statement 5
```
using this test-bench 
```python
def test_positive(): check_number(5)
```
will cover statements 1,2,3,5 meaning 80% statement coverage.

-----------------
# References
https://www.chipverify.com/verification/statement-coverage