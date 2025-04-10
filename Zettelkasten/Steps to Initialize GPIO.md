Created on: 04-06-2024 18:44
Status: #idea
Tags: #ARM #embedded-systems 
# Steps to Initialize GPIO
1. Active clock for corresponding port
	1. set SYSCTL_RCGCCGPIO_R on needed port
	2. wait for the status register SYSCTL_PRGPIO_R to be set 
2. Unlock port and pins needed
	1. Unlock port (optional, depending on port) by setting GPIO_PORTx_LOCK_R=0x4C4F.434B
	2. Enable commit register for needed pins by setting GPIO_PORTx_CR_R in correct positions
 3. If needed as digital, 
	 1. set digital enable on GPIO_PORTx_DEN_R
	 2. disable analog mode on GPIO_PORTx_AMSEL_R
4.  If needed as GPIO
	1. disable analog functionality, by clearing GPIO_PORTx_AFSEL_R on pins
	2. clear PCTL values on GPIO_PORTx_PCTL_R on pins
5. (Optional) Enable Pull up resistors if need to use switches, by setting GPIO_PORTx_PUR_R on corresponding pins



-----------------
# References
[[Introduction To Embedded Systems]]