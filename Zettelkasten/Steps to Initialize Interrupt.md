Created on: 05-06-2024 02:04
Status: #idea
Tags: #ARM #embedded-systems 
# Steps to Initialize Interrupt
1. Enable for the specific pin the interrupt. __NB:__ if interrupt is using GPIO, check and set [[GPIO Pins Control Registers]] for appropriate values.
2. Enable interrupt and set priority, using [[Interrupt Control Registers]]
3. Enable global interrupt using one of the below codes

```
EnableInterrupts(); //first implementation
__enable_irq(); //second
__asm{
CPSIE I
}; //third
```
4. Write interrupt handler function,
	in which you have to acknowledge interrupt by setting ICR_R of peripheral to 1 on the appropriate bit. Otherwise, the interrupt appears to be still pending and the handler gets executed again and again and the program hangs.




-----------------
# References
[[Introduction To Embedded Systems]]