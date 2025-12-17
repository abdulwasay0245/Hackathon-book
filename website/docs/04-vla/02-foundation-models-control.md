---
sidebar_position: 2
---

# 4.2 Vision-Language-Action (VLA) Models

A VLA model takes an observation (Image + Instruction) and outputs a direct robot action (Delta Position / Gripper State).

## RT-1 (Robotics Transformer 1)
Google's RT-1 treats robot actions as "tokens," just like words in a sentence.
- Input: Image + "Pick up the coke can."
- Output: Token stream representing arm movement.

## RT-2 & Octo
Newer models like RT-2 and Octo generalize across different robot embodiments (e.g., using a policy trained on a Franka arm to control a UR5 arm).

## The Open-X Embodiment Dataset
The "ImageNet" of robotics. A massive dataset of diverse robot interactions used to train generalist robot policies. We will explore how to fine-tune a small VLA model on this data.
