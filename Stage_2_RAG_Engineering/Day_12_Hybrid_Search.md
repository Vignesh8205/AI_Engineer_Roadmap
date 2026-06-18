# Day 12: Hybrid Search

## 1. Detailed Theory

Vector search is great for semantics, but terrible at exact keyword matching (e.g., searching for a specific ID like "USER-9942" or a rare name "X Æ A-12"). 

### The Solution: Hybrid Search
Hybrid search combines:
1. **Dense Vector Search:** Good for meaning ("cancel plan").
2. **Sparse Keyword Search (BM25):** Good for exact matches ("Error Code 504").

### Re-ranking (The Secret Weapon)
When you combine two different scoring systems, how do you sort them?
You use a **Re-ranker model** (like Cohere Rerank or BGE-Reranker). 
1. Retrieve top 50 results from Vector Search.
2. Retrieve top 50 results from Keyword Search.
3. Pass all 100 to a Cross-Encoder Re-ranker model.
4. The Re-ranker looks at the actual text and accurately scores the top 5 most relevant results to feed to the LLM.

## 2. Recommended YouTube Tutorials

- [Hybrid Search & Reranking in RAG (Cohere)](https://www.youtube.com/watch?v=P2oB6s2E6kU)
- [Improving RAG with BM25 + Vector Search](https://www.youtube.com/watch?v=8j0BebGjIuw)

## 3. Real-Time Project GitHub Links

- [FlagEmbedding (BGE Re-ranker)](https://github.com/FlagOpen/FlagEmbedding) - Open-source state-of-the-art re-rankers.
- [Elasticsearch Hybrid Search](https://github.com/elastic/elasticsearch) - The industry standard for BM25, now integrating vector search.
