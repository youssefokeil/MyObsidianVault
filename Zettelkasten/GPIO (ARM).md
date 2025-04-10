Created on: 03-06-2024 17:48
Status: #idea
Tags: #embedded-systems  #ARM 
# GPIO
> Or General-Purpose Input/Output. 

- Is set of pins that are connected in parallel, so that it can receive multiple signals at once. 
- They're accessed through Advanced Peripheral Bus(APB)
- For initializing GPIO, check [[Steps to Initialize GPIO]]
- For using GPIO in interrupts, check [[GPIO Pins Control Registers]]
--------

### GPIO Run Mode {SYSCTL_RCGCGPIO_R}
Only one register containing 20 bits, 4 bits for each GPIO port from A to F (5 ports). Short for System control Run Clock Getting Control GPIO register.
- __Clear (0){default}:__ clock is disabled on the respective port, to save power & accessing registers produces bus fault.
- __Set (1):__ respective module is provided clock & access to registers is enabled. 
### GPIO Peripheral Ready {SYSCTL_PRGPIO_R}
status register indicating whether GPIO is ready to be accessed.
- __Equals (0):__ means it's not ready
- __Equals (1):__ ready to be accessed.
To be used you usually make while loop to wait for PRGPIO to be set.

![[PRGPIO_RCGCGPIO.png]]

------
___To unlock pins, you have to unlock the port first. Setting Lock register ton the specific value and setting the specific pins you want the data written to be committed to.___
### GPIO Lock {GPIO_PORTx_LOCK_R} (optional)
Locked pins is a stability feature in ARM. To use pins like PF0 & PD7, you have to unlock them.
32 bits, 
- __Unlocked:__ by a specific value= 0x4C4F434B
- __Any other value:__ keeps pins locked.
### GPIO Commit register {GPIO_PORTx_CR_R}
used for allowing changes for specified pins. If pin is locked, writes are ignored. 
8 bits for 8 pins; each pin has 1 bit corresponding to the
- __Set (1):__ allow changes to specific pin.
- __Clear (0):__ data being written, isn't comitted.


-------
### GPIO Direction (GPIO_PORTx_DIR_R)
8 bits for 8 pins; each pin has 1 bit corresponding to:
- __Set (1):__ sets the direction of pin to output
- __Clear (0){default after reset}:__ sets the direction of pin to input

### GPIO Data {GPIO_PORTx_DATA_R}
8 bits for 8 pins; each pin has 1 bits corresponding to the
- data input from pin
- set by software to be output on pin. 
All data bits are cleared by default after a reset.
---------

___If pins are needed as digital, you have to enable DEN and disable analog function.___
### GPIO Digital EN {GPIO_PORTx_DEN_R}
used for enabling digital input/output.
8 bits for 8 pins; each pin has 1 bit corresponding to the
- __Set (1):__ sets the pin to digital input/output
- __Clear (0){default after reset}:__ not used as digital enable (analog).
All data bits are cleared by default after a reset. 
### GPIO Analog mode {GPIO_PORTx_AMSEL_R}
Analog mode select, used for enabling isolation circuits for analog side.
8 bits for 8 pins; each pin has 1 bit corresponding to the
- __Set (1):__ analog function is enabled
- __Clear (0){default}:__ analog function is disabled.

---------
___If function needed as GPIO clear alternate function and PCTL___
### GPIO Alternate function {GPIO_PORTx_AFSEL_R}
used for enabling alternate function.
8 bits for 8 pins; each pin has 1 bit corresponding to the
- __Set (1):__ enables alternate function, must be used in conjunction with PCTL to pick which alternate function to use.
- __Clear (0):__ used as GPIO
### GPIO PCTL {GPIO_PORTx_PCTL_R}
to pick which analog function to use: [[UART]], I2C, SSI, ....
each pin has 4 bits corresponding to the
- __Clear (0):__ regular Input/Output.
- __Set to specific value:__ have to look in data sheet table to set the right value for each pin.
------
### GPIO Pull-up resistors {GPIO_PORTx_PUR_R} (optional)
used for enabling pull-up resistors. usually used for switches.
32 bits for 8 pins; each pin has 4 bits corresponding to the
- __Set (1):__ sets a (weak) pull-up resistor on specific pin.
- __Clear (0){default after reset}:__ not using pull-up resistors.

![[GPIO.png]]
-----------------

# References
[[Introduction To Embedded Systems]]