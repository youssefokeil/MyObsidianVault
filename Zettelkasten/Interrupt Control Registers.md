Created on: 05-06-2024 01:26
Status: #idea
Tags: #ARM  #embedded-systems 
# Interrupt Control Registers
> used to enable interrupt on peripheral level
### NVIC_ENn_R
> Where n is from 0 to 4, corresponding to 5 Interrupt Enable Registers. Should be set in correct bit position, to enable interrupt for specific peripheral. 

to calculate correct bit:
1. choose correct register n
	$$n=int(IRQ/32)$$
2. choose correct bit in the register
	$$b=IRQ\% 32$$
### NVIC_PRIn_R
> n is from 0 to 34, corresponding to 35 priority level register groups. Each register groups has 4 peripherals where the top 3 bits are the only one used and the rest is reserved.

__Group 0 as an example:__
![[Screenshot 2024-06-05 014815.png]]
to calculate correct bit:
1. pick correct register group:$$n=int(IRQ/4)$$
2. pick correct segment: $$s=IRQ\%4$$

-----------------
# References
[[Introduction To Embedded Systems]]