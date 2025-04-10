Created on: 03-06-2024 01:53
Status: #idea
Tags: #ARM #embedded-systems #assembly 
# Assembler Directives
> We use assembler directives to assist & control the assembly process. They're used to change way code is assembled.

# Initializing Area in memory
## AREA
`AREA sectionname {,attr}{,attr}`
tells assembler to define new section of memory (SRAM or ROM)
#### First Attribute:
- CODE: for machine instructions/const. data (R)
	`AREA myCode, CODE, ReadOnly`
- DATA:  contains data, no instructions 
	`AREA RESET, DATA, READONLY`
- NOINIT:  data section uninitialized or initialized to zero,  `ALIGN=3` aligned to 8-byte boundary 
	`AREA STACK, NOINIT, READWRITE, ALIGN=3`
	`AREA HEAP, NOINIT, READWRITE, ALIGN=3`
#### Second Attribute:
- READONLY: area should not be written to & placed in ROM(for code)
	`AREA myCode, CODE, ReadOnly`
- READWRITE: area may be read or written to placed in SRAM for variables
	`AREA myVarData, DATA, READWRITE`

------

# Other:
## ENTRY
indicates assembler beginning of executable code
## END
indicates assembler end of source file
## EQU
**defines** a constant value or fixed address. Sets aside storage for data item, but associates a constant number with a data or an address label
	`Stack_Size EQU 0x00000200`
	`abc EQU 2`
## ALIGN
ensures the instruction is aligned properly
> `ALIGN {2}` aligns next instructions to 2 bytes (16-bit)
> `ALIGN=2` aligns next instruction to 2^2 bytes (32-bit)

## DCB, DCW, DCD
Initializes operands. Allocates aligned byte (8-bit), half-word (16-bit), word (32-bit) respectfully with an initialized value.
```
A DCB 10;  allocates one byte with value 10
B DCW 22;  allocates half-word with value 22
C DCD 40;  allocates word with value 40
arr DCD 1,2,3,4; another usage is for arrays, and all are word-aligned
```

## SPACE
used for initializing a block of data with zeros
>`data1 SPACE 255` initialized 255bytes  of zeros
>used in conjunction with NOINIT to initialize area in memory
```
                AREA    STACK, NOINIT, READWRITE, ALIGN=3
Stack_Mem       SPACE   Stack_Size
;// from startup code
```


-----------------
# References
[[Introduction To Embedded Systems]]