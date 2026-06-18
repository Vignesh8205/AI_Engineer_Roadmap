# Day 16: Tool Calling

## 1. Detailed Theory

Agents interact with the world via **Tools**. This is the practical application of the Function Calling we learned in Stage 1.

### How to Build a Tool
A tool consists of:
1. **The Code:** A standard Python or JavaScript function (e.g., `def get_weather(city): ...`).
2. **The Description:** A prompt that tells the LLM exactly *what* this tool does and *when* to use it.
3. **The Schema:** A JSON schema detailing the exact arguments the tool requires.

### Best Practices for Tools
- **Deterministic:** The tool should ideally return predictable, structured data.
- **Error Handling:** If a tool fails, it should return a clear error message *to the LLM*, so the LLM can try fixing the inputs and running it again.
- **Granularity:** Tools should do one thing well (e.g., `search_database` and `delete_record` should be separate tools).

## 2. Recommended YouTube Tutorials

- [Building Custom Tools for LangChain/Agents (Data Independent)](https://www.youtube.com/watch?v=vIfkY2Z9U2Q)
- [Tool Calling with Anthropic Claude](https://www.youtube.com/watch?v=eMlx5fFNoYc)

## 3. Real-Time Project GitHub Links

- [Vercel AI SDK Tools](https://github.com/vercel/ai) - Look at how tools are defined in the Vercel AI SDK for React applications.
- [LangChain Tools Repository](https://github.com/langchain-ai/langchain/tree/master/libs/langchain/langchain/tools) - Browse hundreds of community-built tools.
