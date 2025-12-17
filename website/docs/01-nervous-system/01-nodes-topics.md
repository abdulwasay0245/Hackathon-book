---
sidebar_position: 1
---

# 1.1 The Neuron & Synapse: Nodes and Topics

In the **Robotic Nervous System**, the fundamental unit of computation is the **Node**, and the primary method of communication is the **Topic**. This architecture mirrors the biological nervous system, where neurons (Nodes) process information and transmit signals across synapses (Topics) to other neurons.

## The Node (The Neuron)
A Node is a process that performs computation. Nodes are combined into a graph and communicate with one another using streaming topics, RPC services, and the Parameter Server. Each node in ROS 2 should be responsible for a single, modular purpose (e.g., one node for controlling the wheel motors, one node for performing laser localization, etc.).

### Key Concepts
- **Executables vs Nodes**: An executable can contain multiple nodes (composition).
- **Lifecycle**: Nodes have states (Unconfigured, Inactive, Active, Finalized).

## The Topic (The Synapse)
Topics are named buses over which nodes exchange messages. Topics have anonymous publish/subscribe semantics, which decouples the production of information from its consumption.

### Communication Pattern
- **Publisher**: "My current velocity is X." (Broadcasts to anyone listening)
- **Subscriber**: "I need to know the velocity to adjust the camera." (Listens to the topic)
- **Many-to-Many**: One topic can have multiple publishers and subscribers.

## Hands-On: Your First Reflex
*(This section will guide the reader to create a simple talker/listener in Python/C++)*
