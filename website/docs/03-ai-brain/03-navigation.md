---
sidebar_position: 3
---

# 3.3 Getting There: Navigation and Path Planning

Navigation is the art of moving from Point A to Point B safely and efficiently. In ROS 2, this is handled by the **Nav2** stack.

## The Navigation Stack (Nav2)
Nav2 is a modular system that handles:
1. **Global Planning**: Finding the best route on the map (Dijkstra/A*). "The strategic plan."
2. **Local Planning (Controller)**: Following the path while avoiding dynamic obstacles (DWA/TEB). "The tactical steering."
3. **Recovery Behaviors**: What to do if stuck (spin, back up).

## SLAM (Simultaneous Localization and Mapping)
To navigate, you need a map. But to build a map, you need to know where you are.
**SLAM** solves this chicken-and-egg problem.
- We will use **SLAM Toolbox** to build a map of our simulation world.

## AMCL (Adaptive Monte Carlo Localization)
Once a map exists, AMCL uses a particle filter to track the robot's position within it. "I see a wall on my left, so I must be in the hallway."
