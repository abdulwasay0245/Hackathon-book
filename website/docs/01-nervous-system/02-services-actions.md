---
sidebar_position: 2
---

# 1.2 Reflex vs. Deliberation: Services and Actions

While Topics (streams of data) represent the continuous flow of sensory information (like vision or touch), **Services** and **Actions** represent the robot's ability to ask questions and perform long-term tasks.

## Services: The Request-Reply Reflex
Services are synchronous communication. One node sends a request, and waits for a reply. This is like a "reflex" or a query.
- **Example**: "Is the gripper open?" -> "Yes."
- **Analogy**: Asking a question and waiting for the answer.

### When to use Services?
- Quick calculations (Inverse Kinematics).
- State queries.
- Toggling a boolean state.

## Actions: The Deliberate Task
Actions are asynchronous. They are designed for long-running tasks where you might want feedback during execution or the ability to cancel.
- **Example**: "Navigate to the kitchen." (Takes 2 minutes, provides feedback "I am 50% there", can be cancelled "Stop!").
- **Analogy**: Giving a command to a subordinate and getting periodic reports.

### Structure of an Action
1. **Goal**: The command (Go to X).
2. **Feedback**: Progress updates (Distance remaining: 5m).
3. **Result**: Final outcome (Arrived / Failed).
