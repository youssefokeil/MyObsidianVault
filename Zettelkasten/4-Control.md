# Control Theory and Philosophy
## Control Theory:
is a field of control engineering, where it is desired to develop an algorithm to drive the system to a desired state. While minimizing overshoot, delay and steady-state error.
### Significance of Control
- The Wright Brothers succeeded in making the first successful test flights, that can last for long periods of time. To do this they used control to make the flight stay for more than a couple of seconds.
- Control theory has graced us with a lot of modern inventions, like: Cruise Control and Air-Conditioners. It's also used extensively in the field of robotics and mechatronics.
--------

## Open-Loop vs Closed-Loop:
### Closed-Loop
> a system that maintain a relationship between output and reference input, by using the difference between them for control. Also called a feedback control system. $error_{actuating} = input_{reference}-feedback_{signal}$ . The actuating error signal, is fed to the controller to reduce the error, so that, the system is more aligned to the desired value.


> **Note:** feedback signal is usually a function of the output signal, whether it is its derivative, its integral or it's the output signal multiplied by a factor

**Example:**
Air conditioners, have a thermometer (to measure the room temperature) and a desired value. By measuring the difference between room temperature and the desired value the thermostat turns the cooling component on or off till we reach the desired value.

---------------
<br>

### Open-Loop
>The output has no effect on the control action. There is no feedback loop, the reference input is fed to the system  by calibration. If the outside conditions change, we have no guarantee that the system will stay doing the desired thing. 

**Example:**
An air conditioner that is programmed to switch on the cooling component every 30 mins for example and off for another 30 mins. This may be calibrated in specific working conditions to ensure that room temperature says at 24$\celsius$. However, if working conditions change like opening the air conditioner in an extra hot day, we don't have a guarantee that it will reach the desired temperature!

|                              | Open-Loop                                                         | Closed-Loop                                                              |
| ---------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------ |
| response to disturbances | needs recalibration when changes and disturbances happen          | insensitive to external disturbances                                     |
| stability                | stability is easy to cause                                        | system tends to overcorrect errors and can cause oscillations            |
| when to use?             | When inputs are known before hand, and there are no disturbances. | When unpredictable disturbances in system components are present.        |
| cost                     | less expensive                                                    | number of components are more, so it generally needs more cost and power |

![[Pasted image 20250907002906.png| center ]]

### When Do We Need Feedback?
Imagine you made a cruise control in your car, to maintain a specific speed. The open loop way, would be to ensure that the motor should make the amount of rpm needed to maintain that specific speed $s$. But what if the car goes on a hill? In such scenario, we'd need that the motor will do more work. What if the car goes down a hill? We'd want to hit the brakes a bit, as the car would gain a lot of acceleration due to gravity. That's why feedback is essential in such scenario.

------------
# PID Control 
## PID Controller:

>  PID stands for Proportional Integral Derivative controllers. The error between the set-point value and the actual value $e(t)$. We then have correction based on a proportional component $P$, an integral component $I$ and a derivative component $D$.

- **Proportional component** -> immediate correction based on how far the actual value is from the set-point value. $P_{component}=k_p*e(t)$.
- **Integral component** -> cumulative sum of all past errors to address steady-state errors that are persistent. $I_{component}=k_I*\int_{0}^{t}{e(t).dt}$ 
- **Derivative component** -> predicts future errors by seeing how fast is the error changing at this moment, so that, it can address rapid changes. $D_{component}=k_D*\dot{e}(t)$.
## How to tune PID?
Ziegler and Nichols proposed rules for tuning PIDs. Using the block diagram below, we'll find that the components of the PID-controller are $K_p$, $T_i$ & $T_d$.

![[Pasted image 20250907013744.png|center]]
### First Method:
1. We input a unit-step to the plant and see its response.
2. If the unit-step response is a S-shape curve like below, then this method is applicable. Else, use another method.
3. This method gets two constants $T$ and $L$.
4. Draw a tangent at the inflection point.
5. Take the intersection of the tangent line with the time axis and get $L$. $L=t, \text{when } c(t)=0$.
6. Take the intersection of the tangent line with the line $c(t)=K$. $K$ is where the response stabilizes. Then get $T$ by taking that intersection, and subtracting $L$ from it.
7. Use the Ziegler-Nichols Tuning Rule:
	- $K_{P}=1.2\frac{T}{L}$
	- $T_{i}=2L$
	- $T_d=0.5L$

![[Pasted image 20250907014004.png|500, center]]

### Second Method:
1. Set $T_i=\infty$ and $T_d=0$.
2. Increase $K_p$ steadily till you reach a response of oscillation, this value of $k_p$ is called $k_{cr}$ or the critical gain.
3. Use the Ziegler-Nichols Tuning Rule based on Critical Gain:
	- $K_{P}=0.6K_{cr}$
	- $T_{i}=0.5K_{cr}$
	- $T_d=0.125K_{cr}$
	
![[Pasted image 20250907015552.png|500, center]]
## Imagining a Temperature Control System for an Industrial Furnace:
This application of PID controllers need stability and energy efficiency more than fast response time.
**Considerations:**
- Change in temperature is very slow, if a disturbance happens it's better to ignore it at the time as if we acted immediately the change will happen after minutes --> low gain of P controller $k_p$
- Since the change in heat is always very slow, derivatives will probably be responding to noise or inaccuracies in the sensor, so it's better if we limit the derivative too --> low $T_d$.
- Integral Action is important however.
- If a system has reached the set-point value, but then we throw a cold object in the furnace, a huge error will happen. This will let the integral part to compensate for the error by adding so much fuel that it overcompensates the problem as the integral part will stay high for a long time. --> freeze the integral part when we throw cold objects in the furnace.
- We may need to put a deadband to decrease wear on our valve, by decreasing the frequency of activation of a device.
- We can also use a hysteresis comparator to accommodate noise in the furnace.
*Under that scenario, it's better to use a PI controller, with low $k_p$* *and freezing the integral part, when throwing objects in the furnace*.
**Sensors used:**
- Thermocouples, most common for high-temperature furnaces.
- Infrared Temperature Sensors, can measure moving objects easily
- Pressure sensors, to measure gas/air pressure in combustion systems.
**Actuators used:**
- Gas valves, to change air pressure for combustion.
- Electric heating elements, if using electrical heating.

![[Pasted image 20250907024612.png]]
## Limitations of PID Controllers
PID controllers are the best controllers for a person who doesn't know anything about the system. 
1. PID controllers don't work well in the presence of non-linearities. They will cause a lot of instabilities, if introduced to a plant that is not linear.
2. Noise can impact the derivative term significantly, so it can cause large amounts of change in response to noise.
3. Windup is a problem in PID controllers, is a problem when the integration part keeps accumulating and it gets a value larger than the maximum value for a regulation variable.
4. The derivative part can create an Impulse, when a change in set-point happens which can cause a huge change output from the controller.
### Alternatives to PID controllers:
1. Using a PI controller, when we're in an environment of a lot of noise -> to decrease derivative action.
2. Using an open-loop control with the PID controller. The open-loop controller can make the heavy lifting in controlling the variable, but the PID controller will only adjust to disturbances.
-------------
<br><br>
<br>


# References
1. *Modern Control Engineering* by *Katsuhiko Ogata*
2. https://en.wikipedia.org/wiki/Proportional%E2%80%93integral%E2%80%93derivative_controller
3. https://en.wikipedia.org/wiki/Control_theory

























































































































































