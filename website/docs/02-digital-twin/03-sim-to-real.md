---
sidebar_position: 3
---

# 2.3 Crossing the Gap: Sim-to-Real Strategies

The **Reality Gap** is the difference in performance between a policy trained in simulation and its behavior in the real world. Bridging this gap is the "Holy Grail" of Physical AI.

## The Gap's Sources
1. **Visual Gap**: Real cameras have noise, blur, and dynamic lighting.
2. **Physics Gap**: Friction is hard to model; motors have backlash and dead zones.
3. **Latency Gap**: Real world communication is not instantaneous.

## Strategy 1: Domain Randomization
Instead of trying to model the world perfectly, we model *many variations* of the world.
- Randomize friction, mass, and damping.
- Randomize lighting, textures, and camera positions.
- **Goal**: The real world becomes just "another variation" of the training data.

## Strategy 2: System Identification (SysID)
We run experiments on the real robot to measure its actual physical parameters (e.g., exact motor torque curve) and update the simulation to match.

## Strategy 3: Robust Control Policies
Training policies that are explicitly penalized for high-frequency control actions or over-reliance on precise state estimation.
