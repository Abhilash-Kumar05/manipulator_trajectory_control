# 4DOF Robotic Manipulator Trajectory Control (Simulink and simscape)

## Overview

This project implements **trajectory tracking control of a 4-DOF articulated robotic manipulator** using **MATLAB and Simulink**.
The robot follows a desired planar trajectory by computing joint angles through **inverse kinematics**, applying **PID joint control**, and validating the motion using **forward kinematics**.

The simulation demonstrates how a robotic manipulator can track a reference path in task space using joint-space control.

---

## Features

* Desired **task-space trajectory generation**
* **Inverse kinematics** for computing joint angles
* **Forward kinematics** for validating end-effector motion
* **PID controllers** for each revolute joint
* Full simulation implemented in **Simulink / Simscape**
* Comparison between **desired and achieved trajectory**

---

## System Architecture

The control pipeline used in the simulation:

```
Desired Trajectory (xd, yd)
        ↓
Inverse Kinematics
        ↓
Desired Joint Angles (q1, q2, q3, q4)
        ↓
PID Joint Controllers
        ↓
Robot Mechanical Model
        ↓
Forward Kinematics
        ↓
End Effector Position (x, y)
```

The output trajectory is compared with the desired trajectory to evaluate tracking performance.

---

## Tools and Technologies

* **MATLAB**
* **Simulink**
* **Simscape Multibody**
* **PID Control**

---

## Results

The robot successfully tracks the desired trajectory using joint-space PID control.
Forward kinematics confirms that the simulated end-effector follows the commanded path.

---

## Repository Structure

```
project/
│
├── articulated_robot.slx      # Simulink model
├── inverse_kinematics.m       # IK implementation
├── forward_kinematics.m       # FK implementation
├── desired_trajectory.m       # trajectory generator
└── README.md
```

---

## Author

Abhilash Kumar
