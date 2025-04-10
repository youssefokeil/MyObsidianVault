
Created on: 04-06-2024 15:31
Status: #idea
Tags: #ARM #embedded-systems 
# Steps to Setup UART
1. Enable UART clock using SYSCTL_RCGCUART_R
2. Enable GPIO clock using SYSCTL_RCGCGPIO_R
3. Disable UART by clearing UARTEN (bit 0) in UARTx_CTL_R
4. Write parameters; FIFO enable, word length, number of stop bits, parity type and enable to UARTx_LRCH_R
5. Write values for baud rate in UARTx_IBRD_R & UARTx_FBRD_R, using [[UART Baud Rate Calculation]] as guidance
6. Enable UART by setting UARTEN (bit 0) in UARTx_CTL_R & RXE, TXE (depending on the application)
7. Set GPIO as digital: 
	1. set GPIO_PORTx_DEN_R (on used pins)
	2. disable analog mode (on used pins) GPIO_PORTx_AMSEL_R
8. Set GPIO to analog Function
	1. Set(=1) GPIO_PORTx_AFSEL_R on the appropriate pin
	2. Set GPIO_PORTx_PCTL_R to appropriate value to configure UART, (UART=0x1) on used pins
### UART registers:

![[UART_registers.png]]


-----------------
# References
[[Introduction To Embedded Systems]]