---
sidebar_position: 1
---

# 2.1 Simulating Laws of Nature: Gazebo & SDF

Before we risk expensive hardware, we must master the **Digital Twin**. This starts with simulating the fundamental laws of physics: gravity, friction, and collision.

## Gazebo (Ignition)
Gazebo is the standard physics simulator for ROS. It allows us to:
- Simulate robot dynamics (mass, inertia).
- Simulate sensors (cameras, LiDAR, IMU).
- Control environments (weather, lighting).

## SDF (Simulation Description Format)
While URDF describes the robot, **SDF** describes the *world* and the robot's interaction with it. SDF is more detailed than URDF and is the native format for Gazebo.

### Key Simulation Components
1. **Rigid Body Dynamics**: Solving F=ma for complex articulation chains.
2. **Collision Detection**: Determining when two objects touch.
3. **Contact Dynamics**: Friction, restitution (bounciness), and stickiness.

## Building Your First World
We will create a simple "Playground" world with:
- A ground plane (friction verification).
- Obstacles (collision verification).
- Lighting (sensor verification).
