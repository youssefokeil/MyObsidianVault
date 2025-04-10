Created on: 02-06-2024 19:18
Status: #idea
Tags: #embedded-systems #ARM #assembly
# Register Direct (Register to register)
>Address is in register

`MOV R0, R1`

-----------------------------------------------------------------
# Immediate Addressing (literal)
> Using immediate values directly

Instructions using immediate addressing:
`MOV R3, #30`
`ADD R1, R2, #0xFF`
`CMP R0, #0X22`
`LDR R3, =const` is a pseudo-instruction, assembler fetches value then executes
- If const=<16-bit, assembler uses MOV
- If const>16-bit, assembler uses PC-relative addressing mode

-----------------------------------------------------------------
# Register Indirect
### Direct Absolute
`LDR R7, =LABEL`
1. R7=value at LABEL
### Regular Register Indirect
`LDR R7, [R5]`
1. R5 unchanged
2. R7=mem{R5}
### with Register Offset
`LDR R7, [R5,R6]`
1. R5 unchanged
2. R7=mem{R5+R6}
### with Shifted Register Offset
`LDR R7, [R5,R6, LSL #2]`
1. R5 unchanged
2. R7=mem{R5+R6<<2}
### with Immediate Offset
`LDR R7, [R5, #4]`
1. R5 unchanged
2. R7=mem{R5+4}
### with Pre-Indexed Immediate Offset
`LDR R7, [R5, #4]!`
1. R5=R5+4 
2. R7=mem{R5}
### with Post-Indexed Immediate Offset
`LDR R7, [R5], #4`
1. R7=mem{R5}
2. R5=R5+4


-----------------
# PC Relative Addressing
> Addressing mode, where address is calculated with reference to current value of program counter

```
LDR R0, =imm32
LDR R0, [PC, #20]
B LABEL
BL LABEL
```
----------------------------------------------------------------- 

# References
[[Introduction To Embedded Systems]]