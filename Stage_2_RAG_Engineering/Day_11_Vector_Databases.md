# Day 11: Vector Databases

## 1. Detailed Theory

A **Vector Database** is specialized infrastructure designed to store and query millions of high-dimensional vectors at lightning speed.

### Core Mechanisms
Standard databases use B-Trees for exact matching. Vector DBs use **ANN (Approximate Nearest Neighbor)** algorithms like **HNSW (Hierarchical Navigable Small World)** to find the closest vectors in milliseconds without comparing against every single row.

### Top Options
- **pgvector:** A PostgreSQL extension. Best if you already use Postgres and want to keep your relational data and vectors together.
- **Qdrant:** Written in Rust. Extremely fast, highly scalable open-source engine.
- **Pinecone:** Fully managed, closed-source SaaS. Easiest to get started with.
- **Milvus / Weaviate:** Great for massive enterprise scale.

## 2. Recommended YouTube Tutorials

- [Vector Databases Explained (Fireship)](https://www.youtube.com/watch?v=klTvEwg3oJ4)
- [pgvector in 100 seconds](https://www.youtube.com/watch?v=FDBnjLLroKw)
- [How HNSW works (Vector Search Algorithm)](https://www.youtube.com/watch?v=QvKMwLjwKjz)

## 3. Real-Time Project GitHub Links

- [pgvector](https://github.com/pgvector/pgvector) - Open-source vector similarity search for Postgres.
- [Qdrant](https://github.com/qdrant/qdrant) - Rust-based high-performance vector search engine.
