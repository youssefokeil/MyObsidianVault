Created on: 03-06-2024 20:55
Status: #idea
Tags: #ARM #embedded-systems 
# Systick Timers (ARM)
> a simple 24-bit down counter that can be used to create time delays and periodic interrupts.
- The timer is initialized with a value and counts down from that value, till it reaches 0
- Microcontroller is of frequency 80MHz, meaning it counts down one bit every 12.5ns
## Registers for Systick

![[systick.png]]
### Systick Control Register {NVIC_ST_CTRL_R}
- __ENABLE (bit 0):__ Set (1) to enable counter. 
- __INTEN (bit 1):__ Set (1) to enable interrupt. Whenever the timer reaches zero from reload value, systick timer requests interrupt signal. 
__NB:__ if INTEN is cleared, we have to check for count flag.
- __CLK_SRC (bit 2):__ Indicates clock source. Clear (0) from external clock. Set (1) from processor clock. 
__NB:__ set to 1, because external clock source is not implemented on TM4C family.
- __COUNT (bit 16):__ status register. Is set to 1, when counter counts to 0. Could be configured to trigger an interrupt.
### Systick Reload Register {NVIC_ST_RELOAD_R}
- __24-bit max:__ from 0x0000.0001 to 0x00FF.FFFF . 
__NB:___ set to value of N-1, if you want to count N processor clock cycles.

### Systick Current Register {NVIC_ST_CURRENT_R}
- Current value of systick counter. 

[[Steps to initialize Systick Timer]]




-----------------
# References
[[Introduction To Embedded Systems]]