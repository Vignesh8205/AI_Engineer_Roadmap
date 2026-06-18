# Senior-Level Topics (Beyond 30 Days)

## 1. Advanced Architecture

### Graph RAG
Standard RAG struggles with global questions like "Summarize the entire theme of this dataset." Graph RAG extracts entities and relationships into a Knowledge Graph (like Neo4j) before vectorizing them. This allows the AI to traverse relationships, vastly improving complex reasoning over large datasets.

### Agentic RAG
Instead of a straight pipeline (Retrieve -> Answer), Agentic RAG gives the agent tools like `search_docs` and `read_webpage`. The agent decides *if* it needs to retrieve data, evaluates the retrieved data, and if the data is bad, loops back to search again with a different query.

### Local AI Infrastructure
Running OpenAI APIs is easy, but expensive and bad for data privacy.
Senior engineers know how to run open-weight models (like Llama 3, Mistral) on local GPUs or company servers.
- **Tools:** `vLLM` (High-throughput serving), `Ollama` (Easy local execution).

## 2. Recommended YouTube Tutorials

- [GraphRAG Explained (Microsoft Research)](https://www.youtube.com/watch?v=vIfkY2Z9U2Q)
- [Agentic RAG with LlamaIndex](https://www.youtube.com/watch?v=wd7TZ4e1mTA)

## 3. Real-Time Project GitHub Links

- [Microsoft GraphRAG](https://github.com/microsoft/graphrag) - Microsoft's official implementation of Graph RAG.
- [vLLM](https://github.com/vllm-project/vllm) - A high-throughput and memory-efficient LLM serving engine.
- [Ollama](https://github.com/ollama/ollama) - Get up and running with large language models locally.
