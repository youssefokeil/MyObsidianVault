# Introduction
In this section of the mission you are supposed to read the attached paper thoroughly and understand as much as you can of it, to answer the following questions.
You will also discuss the paper further in the interview.

# General Questions
## Why is Autonomous Racing Challenging?
It combines:
- high-speed dynamics
- necessity for reliability
- real-time decision-making

## Infrastructure-less Localization:
Is Localization without the use of GPS (Global Positioning System) or motion capture systems. They usually use, sensors and environmental sounds to get accurate localization.
# Frenet Coordinates
## What are Frenet Coordinates?
Is a coordinate system relative to a reference path. In the example we have, the reference path is the global racing line. They're denoted by $(s,d)$, where $s$ is the progression along racing line & $d$ is the perpendicular distance from the racing line, positive when left of the line & negative when right of the line.

## Advantage of Frenet Coordinates.
1. easier to determine a point's position relative to the race track.
2. describes motion models in relation to a reference racing line. We have the corresponding velocities $v_s$ and $v_d$.
3. much easier to generate evasion waypoints that align with the racing line.
# State Estimation
## What is the role of IMU?
- measures the orientation $q_{x},\, q_{y}, \, q_{z},\, q_w$. 
- the angular velocity $v_{ax}, \, v_{ay}, \, v_{az}$
- The linear acceleration $a_{lx,}, \, a_{ly}, \, a_{lz}$
## The state estimation method:
1. it combines localization and velocity estimation. 
2. It uses the sensor inputs from the IMU, 2D laser scans from the LiDAR and the ERPM gets us the wheel-odometry.
3. The odom filter is an Extended Kalman Filter, that fuses wheel-odometry and IMU data for better velocity estimation.
4. Localization is done either with the:
	1. Cartogropher: Yields very high accuracy localization and pose estiimation if odometry input data is of high-quality.
	2. SynPF: less accurate pose estimation, but more robust against low-quality odometry data.  
5. We then use a motion-capture system to detect the car's actual location. 

![[Pasted image 20250907150018.png|500, center]]
# Perception
- What features are extracted from LiDAR detections?
- Why was an opponent tracking module added?
## LiDAR Scan Data
1. The LiDAR scan data is split into clusters of potential obstacles. 
2. Then we do segmentation to ensure a low false positive rate.
3. We then eliminate the track data, by inflating the track boundaries by a predefined distance.
4. The remaining points are approximated with rectangles on the 2D map space.
5. Then we remove objects smaller than a a specific size threshold.

## Why Opponent Tracking?
For downstream robotic tasks, example:
- when taking corners, it's better to have good opponent estimation to ensure safety and performance. By maintaining a safe distance and smarter maneuvers.
- This is good when trying to follow an opponent, too. As we have to maintain a safe distance because if it slowed down for any reason, we'll be able to do a maneuver to ensure our car's safety by preventing collisions.

# Motion planning and Control
- What is the purpose of the local planner?
-  What are the roles of the lateral and longitudinal controllers?
## Why local planner?
This generates a feasible trajectory for the controller to follow to avoid obstacles. Local Planner is employed only if the perception module detects an opponent, then the local planner brings the car to the $Overtake$ state. This way the planner needs to create a local trajectory to overtake that opponent.

## Why Lateral & Longitudinal Controllers?
**Lateral Controller:** computes the steering angle $\delta$  to enable accurate spatial trajectory and for the car to follow the desired trajectory0. For this we use the Model- and Acceleration-based Pursuit (MAP) controller. 

**Longitudinal Controller:** computes the velocity of the car. When the perception module detects an opponent, and overtaking it is not viable. The state of the car is transitioned to $Trailing$, in such scenario the longitudinal controller adjusts the velocity to have a safe distance with the the opponent and in a good position to seize an overtaking opportunity.