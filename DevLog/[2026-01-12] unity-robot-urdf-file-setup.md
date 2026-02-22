# Importing OpenArm URDF to Unity for VR Teleoperation
Date : 2026-01-12
Category : 'unity', 'robotics', 'urdf'

## 1. Goal
Develop a VR teleoperation interface to control the OpenArm robot using MetaQuest3
The Primary goal of this session was to import the robot's URDF model into the Unity scene

## 2. Environment
* Hardware: MacBook Air M3, Meta Quest 3
* OS: macOS
* Unity Version: Unity 6.3 LTS (6000.3.1f1)
* Target Platform: Android (for Quest Standalone)

## 3. key setup Steps
* Asset Preparation : Downloaded OpenArm description files (URDF, meshes and etc)
* Importing : used URDF Importer package to load the robot model into the scene

## 4. Troubleshooting
When I tried to import robot, there were many errors because of different file names and directory with URDF.
I had to match all the files and find all the sources from the Internet :(
Still, when I build and run the file, I cannot see the robot in the scene

### Issue 1 : URDF Import Errors (Broken Mesh References)
* Problem: The importer threw multiple of errors regarding "missing mesh files" due to dircetory structure mismatches in the raw URDF file
* Solution: Manually mapped the .stl and .dae mesh file paths to match the Unity project structure

### Issue 2 : Invisible Robot in Build (Current Blocker)
* Problem: The robot is visible in the Unity Editor but invisible in the standalone VR build (Quest3)
* Debug Attempt: Tried scaling the robot up by 100x to check if it was too small
* Observation:(photo)
* Hypothesis: 
  * Seems like Camera & Robot Coordinate Mismatch
  * Despite pre-configuring the positions in the Editor, the VR Headset tracking likely overrode the camera position to the runtime tracking origin(unintended location)
* Next Action : Reset Scale to 1 and adjust the spawn position of the robot


# 5. Next Step
Upload robot in VR scene after building and running
