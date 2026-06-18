# Days 13 & 14: Build Complete RAG & Evaluation

## 1. Detailed Theory

Time to put it all together. Building a complete RAG system requires orchestrating the data ingestion pipeline and the generation pipeline.

### The Full Architecture

```text
[PDF/Doc] -> Chunk -> Embed -> Qdrant (Vector DB)
                                    ^
                                    |
[User Query] -> Embed -> Retrieve --+
                                    |
                                    v
                         [Context + Query] -> LLM -> [Answer]
```

### RAG Evaluation (RAGAS)
Once built, how do you know if it's good? You evaluate it on:
- **Context Precision:** Did you retrieve the right chunks?
- **Context Recall:** Did you retrieve *all* the necessary information?
- **Faithfulness:** Is the LLM's answer based *only* on the context?
- **Answer Relevancy:** Did the LLM actually answer the user's question?

## 2. Recommended YouTube Tutorials

- [Build a RAG system from scratch (LangChain)](https://www.youtube.com/watch?v=wd7TZ4e1mTA)
- [Evaluating RAG Applications with RAGAS (AI Engineer)](https://www.youtube.com/watch?v=1Z3H-A8aBts)

## 3. Real-Time Project GitHub Links

- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) - A full-stack application that turns any document into a conversational AI. Excellent reference architecture.
- [Dify](https://github.com/langgenius/dify) - An open-source LLM app development platform with great RAG flows.
