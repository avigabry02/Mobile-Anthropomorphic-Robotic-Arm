# Mobile-Anthropomorphic-Robotic-Arm

# Bachelor's Thesis: Mobile Anthropomorphic Robotic Arm

This repository contains the study and simulation work for my Bachelor's Thesis, focused on the design and control of a mobile anthropomorphic robotic arm. The project aimed to integrate an anthropomorphic manipulator onto a mobile platform (like the LIMO robot) to enable autonomous tasks, such as dynamic pick-and-place operations.

---

## Key Methodologies and Analysis

The project involved a deep dive into the theoretical and practical aspects of the 3-Degree-of-Freedom (DOF) robotic arm and the mobile platform.

* **Kinematic and Dynamic Analysis:** The foundational study involved deriving the system's kinematics (Forward and Inverse) and dynamics. The **Newton-Euler approach** was used to calculate the forces, moments, and internal reactions at the joints, providing essential information for motor dimensioning.
* **Mobile Robotics Simulation:** A simulation model was built in Simulink to replicate the behavior of a mobile robot. This model used Lidar-like sensing to **detect and track objects**, allowing the mobile base to orient itself and approach the target (e.g., within $0.24~m$) to bring the object into the arm's workspace.
* **Robotic Arm Simulation and Control:** The core logic was developed in **MATLAB/Simulink**, utilizing the Inverse Kinematics block to translate desired end-effector coordinates into the necessary joint rotations.
* **Response Quality Evaluation:** The system's step response was critically analyzed for transient behavior, quantifying phenomena like **overshoot**, **preshoot**, and **undershoot**. This analysis confirmed that despite minor non-ideal behaviors, the system stabilizes rapidly (e.g., settling time of $\approx 6~ms$), making it adequate for the magnetic retrieval task.

---

## Tools Employed

* **MATLAB / Simulink:** Primary environment for all simulation, modeling, and control development, including the use of Simscape for the physical modeling of the robotic mechanism.
* **Mathematica:** Used for complex symbolic and numerical calculation during the kinematic and dynamic modeling phases.
* **CAD/Prototyping:** The final implementation envisioned using **3D-printed parts**, **DC motors**, and **Arduino/custom electronics** for the control system, with code generated directly from the Simulink model for Hardware-in-the-Loop (HIL) testing.

---

## Intended Audience

This repository is a comprehensive resource for:

* **Robotics Students and Enthusiasts:** Demonstrates a complete workflow for developing a robotic system, from theoretical kinematics/dynamics to full simulation.
* **Control Engineers:** Provides examples of closed-loop control systems in Simulink, focusing on PID tuning principles and the evaluation of system response quality (overshoot, settling time, etc.).
* **Mechanical Engineers:** Offers insight into the modeling and analysis required for articulated mechanical systems and the integration of CAD design with simulation tools.
