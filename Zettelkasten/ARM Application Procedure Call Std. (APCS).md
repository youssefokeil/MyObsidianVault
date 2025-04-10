Created on: 03-06-2024 14:33
Status: #idea
Tags: #ARM #assembly #embedded-systems 
# ARM APCS
> Standard to be followed on the usage of registers by caller and callee
### Scratch Registers
>Registers that their values may be changed upon returning to caller, preserve their values on stack if needed after subroutine

__R0-R3__: used to pass parameters to callee
__R0-R1__: used to return result to caller
__R12 (IP)__: intra-procedure-call scratch register. The caller isn't expected to send values through that register. Callee overwrites the value in it for internal calculations. Or can be used by linker between routine and sub-routine.
__Extra Parameters__: are passed through stack 
### Preserved Registers
> Hold values of routine's variables. Callee needs to save them by placing them on stack before using them and then returning values from stack again.

__R4-R11__
### Stack Pointer
__R13 (SP)__: 
- In start of function, we allocate space in stack to save registers that will be used and must be preserved, at the end of the function the saved values are popped off and SP returns to its original value.
- We don't need to manually decrease and increase SP value, it's already internalized in PUSH & POP instructions.
### Link Register
__R14 (LR)__: Set by BL on function call and must be preserved if the function calls another function (Nested-Call)


-----------------
# References
[[Introduction To Embedded Systems]]