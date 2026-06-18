# Day 8: RAG Overview

## 1. Detailed Theory

**RAG (Retrieval-Augmented Generation)** is the industry standard for making LLMs answer questions about private data without fine-tuning.

### The Problem
LLMs are trained on past data. They don't know your private company documents, and their training cutoff means they don't know recent events.

### The Solution: RAG Flow
Instead of asking the LLM to pull knowledge from its weights, we provide the knowledge in the prompt.

```text
Document -> Chunking -> Embedding -> Vector DB -> Retrieval -> LLM Generation
```

1. **Ingestion Phase:**
   - Parse PDFs, docs, or web pages.
   - **Chunk** them into smaller pieces.
   - Run those pieces through an **Embedding Model** to get vectors.
   - Store vectors + text in a **Vector Database**.
2. **Retrieval Phase:**
   - User asks: "What is our company's refund policy?"
   - Embed the question.
   - Search the Vector DB for the nearest chunks.
   - Pass the retrieved chunks + the user's question to the LLM.
   - "Based on the following context, answer the question..."

## 2. Recommended YouTube Tutorials

- [What is Retrieval-Augmented Generation (RAG)? (IBM Technology)](https://www.youtube.com/watch?v=T-D1OfcDW1M)
- [Building RAG from Scratch (Andrej Karpathy conceptual style tutorial)](https://www.youtube.com/watch?v=wd7TZ4e1mTA)
- [RAG Architecture Explained (ByteByteGo)](https://www.youtube.com/watch?v=LpNgSJA1yT4)

## 3. Real-Time Project GitHub Links

- [LlamaIndex](https://github.com/run-llama/llama_index) - The standard data framework for LLM applications.
- [PrivateGPT](https://github.com/zylon-ai/private-gpt) - A popular project showing how to run RAG entirely locally without leaking data.
