---
sidebar_position: 3
---

# 1.3 Proprioception: URDF and Body Schema

For a robot to control itself, it must have an internal model of its own body. In ROS 2, this is defined using **URDF (Unified Robot Description Format)**. This is the "Body Schema" of our Physical AI.

## The Anatomy of URDF
URDF is an XML format that describes:
- **Links**: The rigid parts of the robot (arms, wheels, chassis).
- **Joints**: How the links are connected and move (revolute, prismatic, fixed).
- **Visuals**: How it looks (meshes, materials).
- **Collisions**: The physical boundaries for physics engines.

## The TF2 Library: Spatial Awareness
**TF2** (Transform Library) is the system that keeps track of the relationship between all these body parts in 3D space over time.
- If the robot raises its arm, TF2 calculates where the hand is relative to the base.
- This represents the robot's **Proprioception** (sense of self-movement).

## Example: Defining a Humanoid Arm
*(Code snippet showing a simple URDF joint definition)*
```xml
<joint name="shoulder_joint" type="revolute">
  <parent link="torso"/>
  <child link="upper_arm"/>
  <origin xyz="0 0.2 0.5"/>
  <axis xyz="0 1 0"/>
</joint>
```
