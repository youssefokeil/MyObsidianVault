Created on: 03-06-2024 21:39
Status: #idea
Tags: #ARM #embedded-systems 
# Steps to initialize Systick Timer 

1. Turn off systick during initialization, by clearing enable bit in NVIC_ST_CTRL_R
2. Put reload value in NVIC_ST_RELOAD_R. Remember to put N-1 if you want to count N processor cycles
3. Write a value in NVIC_ST_CURRENT_R to clear counter.
4. Enable systick and set CLK_SRC to 1 (because external CLK_SRC is not implemented on LM3S/TM4C family)
5. __If INTEN is not set,__ check NVIC_ST_CURRENT_R using polling method.



-----------------
# References
[[Introduction To Embedded Systems]]