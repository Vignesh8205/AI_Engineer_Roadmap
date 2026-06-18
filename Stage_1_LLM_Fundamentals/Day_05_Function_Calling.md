# Day 5: Function Calling & Structured Outputs

## 1. Detailed Theory

LLMs generate text, but applications need structured data (like JSON) to trigger code logic. **Function Calling** bridges this gap.

### Core Concepts

- **Structured Outputs (JSON Mode):** Forcing the LLM to reply with valid JSON matching a specific schema, rather than conversational text.
- **Function Calling / Tool Calling:**
  1. You provide the LLM with a list of "tools" (functions) and their JSON schemas (e.g., `get_weather(location)`).
  2. The LLM determines if a tool needs to be called to fulfill the user's request.
  3. Instead of answering the user, the LLM outputs a JSON payload containing the function name and arguments.
  4. Your code executes the function, gets the result, and feeds it back to the LLM.
  5. The LLM then generates the final human-readable response.

This is the foundational step required to build Agents.

## 2. Recommended YouTube Tutorials

- [OpenAI Function Calling Tutorial (TechLead)](https://www.youtube.com/watch?v=0-hEP3yqE_8)
- [How to use OpenAI Function Calling in Python (AssemblyAI)](https://www.youtube.com/watch?v=0rsAFGg07Gg)
- [Structured Outputs with OpenAI API (Fireship)](https://www.youtube.com/watch?v=1bEj1kQZkDU)

## 3. Real-Time Project GitHub Links

- [OpenAI Python SDK - Function Calling Examples](https://github.com/openai/openai-cookbook/tree/main/examples)
- [Instructor](https://github.com/jxnl/instructor) - Structured extraction in Python, powered by OpenAI function calling.
