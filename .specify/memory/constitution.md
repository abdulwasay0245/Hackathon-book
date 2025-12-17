# Physical AI & Humanoid Robotics through AI Agents Constitution

## Core Principles

### I. Book-First Documentation
Every artifact, code change, and experiment must directly contribute to the "Physical AI & Humanoid Robotics through AI Agents" book. The code is the practical companion to the text. If it's not in the book (or supporting it), it's out of scope.

### II. AI-Agent-Driven Curriculum
The content is designed to be consumed and taught by AI agents to humans. Structure, clarity, and explicit context are paramount. Avoid implicit knowledge. Documentation should be machine-readable and structurally sound (Markdown/MDX).

### III. Physical Realism & Digital Twin First
Always prioritize simulation (Digital Twin) before physical deployment. Usage of Gazebo (ROS 2) and Unity for high-fidelity simulation is mandatory for verification. The "Sim-to-Real" gap must be explicitly addressed in all designs.

### IV. Modular & Scalable Architecture
Follow the neurological and functional hierarchy of humanoid robotics:
- **Nervous System**: ROS 2 middleware.
- **Brain**: AI/VLA Learning (NVIDIA Isaac/models).
- **Body**: Physical kinematics and URDF/SDF descriptions.

### V. Reproducibility
All examples and projects must be reproducible from a fresh environment. Use containers (Docker) or rigorous dependency management where applicable.

## Governance

- **Constitution Supersedes**: This document allows us to reject changes that do not fit the "Book-First" or "Digital Twin" approach.
- **Amendments**: Changes to this constitution require a dedicated `prompt-history` record explaining the shift in pedagogical or technical approach.

**Version**: 1.0.0 | **Ratified**: 2025-12-17 | **Last Amended**: 2025-12-17
