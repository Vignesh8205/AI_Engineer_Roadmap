# Day 18: Agent Planning & Frameworks

## 1. Detailed Theory

If an agent has tools, how does it know *when* and *in what order* to use them? That requires a planning framework.

### Popular Planning Frameworks

1. **ReAct (Reason + Act):**
   - The original agent framework.
   - Loop:
     1. **Thought:** "I need to find the weather in Paris, then calculate the temperature in Fahrenheit."
     2. **Action:** Call `get_weather("Paris")`.
     3. **Observation:** "It is 20 degrees Celsius."
     4. **Thought:** "I need to multiply 20 by 1.8 and add 32."
     5. **Action:** Call `calculator("20 * 1.8 + 32")`.
     6. **Observation:** "68".
     7. **Final Answer:** "It is 68 degrees Fahrenheit."

2. **Reflection:**
   - The agent writes a draft response.
   - Another prompt (or a different agent) critiques the draft.
   - The agent revises its answer based on the critique.

3. **Task Decomposition:**
   - Given a massive goal ("Write a snake game in Python"), the agent first generates a checklist.
   - It then iterates through the checklist, completing one item at a time.

## 2. Recommended YouTube Tutorials

- [ReAct Prompting Explained (Prompt Engineering)](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- [LangGraph: Multi-Actor Workflows (LangChain)](https://www.youtube.com/watch?v=pd_7vG0Y2O4)

## 3. Real-Time Project GitHub Links

- [LangGraph](https://github.com/langchain-ai/langgraph) - The industry standard framework for building stateful, multi-actor applications with LLMs.
- [CrewAI](https://github.com/joaomdmoura/crewAI) - Framework for orchestrating role-playing, autonomous AI agents.
