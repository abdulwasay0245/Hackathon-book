---
sidebar_position: 3
---

# 4.3 Speaking to Robots: Voice Interaction

The final interface for a Humanoid Robot is natural speech.

## Whisper (Speech-to-Text)
We use OpenAI's **Whisper** to function as the robot's "ears." It provides state-of-the-art transcription even in noisy environments (like a room with whirring motors).

## Dialogue Management
Once we have text, we feed it to an LLM (like Llama 3 or GPT-4o) which acts as the high-level planner.
- User: "I'm thirsty."
- LLM Thought: "User is thirsty -> Solution: Fetch drink -> Action: Navigate to kitchen."
- LLM Output: "I will go get you some water."

## Text-to-Speech (TTS)
The robot responds using a TTS engine, completing the loop of natural human interaction.
