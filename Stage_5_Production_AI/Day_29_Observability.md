# Day 29: Observability & Tracing

## 1. Detailed Theory

When a standard REST API fails, you look at the stack trace. When an AI Agent fails, it's much harder to debug because the "failure" is often a bad LLM reasoning step, not a code crash.

### AI Observability
You need to track the entire **trace** of an interaction:
1. What was the exact user prompt?
2. What documents did RAG retrieve? (Were they relevant?)
3. What was the exact prompt injected into the LLM?
4. What tools did the LLM decide to call?
5. How long did the LLM take to generate the tokens? (Latency)
6. How much did this request cost?

### Tools for Observability
- **LangSmith:** Built by LangChain. The industry leader for tracing agent runs step-by-step.
- **OpenTelemetry (OTEL):** The open standard for tracing. Many modern AI SDKs (like Vercel AI SDK) emit OTEL traces natively.

## 2. Recommended YouTube Tutorials

- [Debugging LLM Apps with LangSmith](https://www.youtube.com/watch?v=7h-m4B0R5iY)
- [LLM Observability and Tracing Explained](https://www.youtube.com/watch?v=vIfkY2Z9U2Q)

## 3. Real-Time Project GitHub Links

- [LangSmith Cookbook](https://github.com/langchain-ai/langsmith-cookbook) - Examples of how to trace and evaluate agents.
- [Phoenix (by Arize)](https://github.com/Arize-ai/phoenix) - Open-source AI observability and evaluation in your local environment.
