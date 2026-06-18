# Day 3: Embeddings & Vector Search

## 1. Detailed Theory

To search for meaning instead of exact keywords, we need **Embeddings** and **Vectors**.

### Core Concepts

- **Vectors:** A mathematical array of numbers (e.g., `[0.12, -0.44, 0.89, ...]`). In machine learning, vectors represent the features or meaning of data.
- **Embeddings:** The process of converting raw data (text, images, audio) into vectors. Models like `text-embedding-ada-002` take a string of text and turn it into an array of thousands of floating-point numbers.
- **Similarity Search:** Once text is converted to a vector, we can mathematically measure how close one vector is to another. If two vectors are close in the multi-dimensional space, their original texts share semantic meaning.
  - *Cosine Similarity* is the most common mathematical method used to calculate the angle between two vectors.

### The Flow
```text
Text -> Embedding Model -> Vector (Numbers) -> Math (Cosine Similarity) -> Nearest Vectors (Results)
```

## 2. Recommended YouTube Tutorials

- [Word Embeddings, Bias in ML, Why You Don't Like Math, & Why AI Needs You (Rachel Thomas)](https://www.youtube.com/watch?v=25nC0n9ERq4)
- [Vector Embeddings Explained (IBM Technology)](https://www.youtube.com/watch?v=O1wEZK_m27c) - Great visual explanation.
- [What are Vector Embeddings? | Explained by Pinecone](https://www.youtube.com/watch?v=l8_fU6sD1oY)

## 3. Real-Time Project GitHub Links

- [Chroma](https://github.com/chroma-core/chroma) - The AI-native open-source embedding database. Look at their introductory examples.
- [HuggingFace sentence-transformers](https://github.com/UKPLab/sentence-transformers) - The leading library for computing dense vector representations.
