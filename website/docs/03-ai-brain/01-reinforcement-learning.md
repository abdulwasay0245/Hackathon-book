---
sidebar_position: 1
---

# 3.1 How Robots Learn: Reinforcement Learning (RL)

Traditional robotics relies on hard-coded rules ("If current_time < 5s, move_leg_x"). **Reinforcement Learning (RL)** allows robots to *discover* optimal policies by trial and error.

## The Loop: State, Action, Reward
1. **Agent**: The Robot.
2. **Environment**: The Simulation (Isaac Gym).
3. **State (Observation)**: "I am leaning 5 degrees left."
4. **Action**: "Fire right thruster."
5. **Reward**: +1 if upright, -1 if fallen.

## Isaac Gym & GPU Physics
Training a humanoid to walk takes billions of steps. A real robot would break. A CPU simulator would take years.
**NVIDIA Isaac Gym** runs the physics simulation *directly on the GPU*. This allows us to train thousands of robots in parallel, reducing years of training time to minutes.

## PPO (Proximal Policy Optimization)
We will use **PPO**, the standard algorithm for continuous control. It strikes a balance between ease of tuning and sample efficiency.
