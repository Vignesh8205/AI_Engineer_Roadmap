# Day 10: Embedding Models

## 1. Detailed Theory

Embeddings are the backbone of search quality in RAG. If your embeddings are bad, your retrieval will be bad, resulting in bad LLM answers.

### Model Selection

- **OpenAI (`text-embedding-3-small` / `large`):** High quality, fast, paid API.
- **Cohere / Voyage AI:** Specialized models often outperforming generic ones on specific domains (like code or finance).
- **Open Source (BGE, Nomic, E5):** Run locally for free. You can find the best models on the **MTEB (Massive Text Embedding Benchmark)** leaderboard.

### Why Embeddings Matter for RAG
Embeddings capture semantic similarity. A search for "How to cancel my subscription" will closely match a chunk saying "Termination of monthly payment plan," even though the words are completely different.

## 2. Recommended YouTube Tutorials

- [Choosing the right Embedding Model for RAG (AI Engineering)](https://www.youtube.com/watch?v=MofUjVn6yS8)
- [MTEB Leaderboard Explained](https://www.youtube.com/watch?v=p7HwE12xX78)

## 3. Real-Time Project GitHub Links

- [MTEB Leaderboard (HuggingFace)](https://huggingface.co/spaces/mteb/leaderboard) - Not GitHub, but the source of truth for embedding quality.
- [Nomic-Embed-Text](https://github.com/nomic-ai/nomic) - A fully open-source, highly performant embedding model.
