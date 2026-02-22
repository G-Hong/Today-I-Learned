## 📄 TIL: Unity Teleoperation App Development

### **Overview**

Today, I focused on implementing the control system for a robot arm using Unity and a joystick. I configured the control schemes and addressed physical stability issues within the simulation.

### **Key Achievements & Fixes**

* **Control Scheme B Implementation:** Successfully mapped the primary movement controls to Scheme B.
* **Physics Stabilization:** * Addressed the "shaking/unstable" behavior of the robot arm.
* Applied the `immovable` setting to `Bodylink0` to ensure a stable base for the kinematic chain.
* Stabilized the arm’s erratic movements (overcoming gravity) by preparing the integration with the controller.


* **Left Arm Integration:** Started the setup for the dual-arm configuration by connecting the left arm to the existing system.

### **Current Issues & Challenges (To-Be-Solved)**

* **Joint Dislocation (Joint Stretching):** Even after stabilization, joints are physically separating/dislocating during movement. This requires a fix in joint drive limits or Rigidbody settings.
* **Gripper Control Failure:** The custom script for the gripper (tightening/releasing via joystick) is currently unresponsive.
* **VR Boundary Interference:** Investigating whether the Quest/VR boundary settings are causing clipping or offset issues during seated development

[[Video]](https://github.com/G-Hong/Today-I-Learned/blob/main/DevLog/assets/%5B2026-02-22%5D%20MR%20environment.mp4?raw=true)
