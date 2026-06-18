# Day 17: Agent Memory

## 1. Detailed Theory

Without memory, an agent is amnesic. Every request is treated as brand new. 

### Types of Memory

1. **Short-Term Memory (Working Memory):**
   - Typically implemented as a sliding window of the conversation history.
   - You append user inputs, agent reasoning, and tool outputs to an array of messages.
   - *Limitation:* Eventually hits the context window limit of the LLM.

2. **Long-Term Memory:**
   - When the short-term memory gets too long, we summarize it or store the interactions in a **Vector Database**.
   - When the user asks a new question, the agent retrieves relevant past interactions via RAG and injects them into the current prompt.
   - Example: Remembering a user's dietary preferences mentioned 3 weeks ago.

## 2. Recommended YouTube Tutorials

- [Adding Memory to AI Agents (LangChain)](https://www.youtube.com/watch?v=O1wEZK_m27c)
- [Mem0 (formerly Embedchain) - Personalized AI Memory](https://www.youtube.com/watch?v=wd7TZ4e1mTA)

## 3. Real-Time Project GitHub Links

- [Mem0](https://github.com/mem0ai/mem0) - The memory layer for personalized AI.
- [Zep](https://github.com/getzep/zep) - A long-term memory store designed specifically for LLM applications.
