# Days 19 & 20: Multi-Step & Multi-Agent Systems

## 1. Detailed Theory

Single agents struggle with extremely complex tasks. If the context window gets too full, or the task requires too many tools, the agent gets confused and loops endlessly. 

### Multi-Agent Systems
Instead of one massive agent, we build small, highly specialized agents and let them talk to each other.

### Example Flow: Software Development Agency

1. **The Planner Agent:**
   - Takes the user request ("Build a To-Do App").
   - Breaks it down into tasks.
   - Passes tasks to the Coder Agent.
2. **The Coder Agent:**
   - Has one tool: `write_file(path, content)`.
   - Writes the code.
   - Passes execution to the Reviewer Agent.
3. **The Reviewer Agent:**
   - Has tools: `run_linter()`, `run_tests()`.
   - If tests fail, it sends the errors back to the Coder Agent to fix.
   - If tests pass, it informs the Planner Agent that the task is done.

This separation of concerns vastly improves reliability.

## 2. Recommended YouTube Tutorials

- [Getting Started with CrewAI (CodeRabbit)](https://www.youtube.com/watch?v=sPzc6hMg7So)
- [AutoGen Tutorial (Microsoft)](https://www.youtube.com/watch?v=VjPtDquO0XQ)

## 3. Real-Time Project GitHub Links

- [Microsoft AutoGen](https://github.com/microsoft/autogen) - The original powerhouse framework for multi-agent conversation.
- [ChatDev](https://github.com/OpenBMB/ChatDev) - Creates a customized software factory where multiple agents (CEO, CTO, Programmer, Tester) collaborate.
