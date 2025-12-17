---
sidebar_position: 1
---

# 4.1 Understanding the World: Multimodal LLMs

The "Brain" of the future is not just a controller code; it's a **Vision-Language Model (VLM)**. These models connect text (Language) with pixels (Vision).

## CLIP (Contrastive Language-Image Pre-training)
Developed by OpenAI, CLIP learns to associate images with text descriptions.
- It allows a robot to find "a red apple" without ever being explicitly trained on apples, just by understanding the semantic concept of "red apple" from its internet-scale training.

## SigLIP & Modern Encoders
We explore modern encoders like SigLIP (Sigmoid Loss for Language Image Pre-training), which offer better performance for dense visual tasks.

## Zero-Shot Detection
Traditional object detection requires training on specific classes (cat, dog). VLMs allow **Zero-Shot Detection**: You can prompt the robot "Find the screwdriver," and it works, even if "screwdriver" wasn't in its training set.
