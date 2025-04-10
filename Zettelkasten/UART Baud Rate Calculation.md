Created on: 03-06-2024 22:47
Status: #idea
Tags: #ARM #embedded-systems 
# UART Baud Rate Calculation

$$BRD =IBRD+FBRD$$
$$BRD = \frac{UARTSysClk}{ClkDiv.BaudRate}$$
$$DIVINT=INT(BRD)$$
$$DIVFRAC=INT(FBRD*64+0.5)$$



-----------------
# References
[[Introduction To Embedded Systems]]