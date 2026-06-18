# Day 15: Agent Fundamentals

## 1. Detailed Theory

An **[AI Agent](https://github.com/resources/articles/what-are-ai-agents)** is an autonomous software tool that performs tasks, makes decisions, and interacts with its environment intelligently and rationally. AI agents differ from other AI technologies in their ability to act autonomously. Unlike other AI models that require constant human input, intelligent agents can initiate actions, make decisions based on predefined goals, and adapt to new information in real time.

At its core, **[Agentic AI](https://github.com/resources/articles/what-is-agentic-ai)** is a system built around an AI model that enables it to operate more like an active teammate, capable of setting goals, taking action, and working independently. This system uses memory (to retain context), tools (like access to your codebase or terminal), a defined goal, and the autonomy to act.

### Core Components of an Agent

1. **Brain (LLM):** The reasoning engine. It decides *what* to do.
2. **Memory:** Context about past actions (Short term: conversation history. Long term: Vector DB).
3. **Tools (Function Calling):** The API connections that allow the agent to affect the world (e.g., executing Python code, reading a database, searching the web).
4. **Planning:** The ability to break a large goal into smaller, executable steps.

### The Agent Loop
```text
User Request -> Reason (What do I need?) -> Choose Tool -> Execute Tool -> Read Result -> Reason (Am I done?) -> Final Response
```

## 2. Recommended YouTube Tutorials

- [What is an AI Agent? (IBM Technology)](https://www.youtube.com/watch?v=F8NKVhkZZWI)
- [Intro to AI Agents (LangChain)](https://www.youtube.com/watch?v=O1wEZK_m27c)

## 3. Real-Time Project GitHub Links

- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) - One of the first and most famous autonomous agents.
- [BabyAGI](https://github.com/yoheinakajima/babyagi) - A very simple, easy-to-read script demonstrating task planning and execution.
