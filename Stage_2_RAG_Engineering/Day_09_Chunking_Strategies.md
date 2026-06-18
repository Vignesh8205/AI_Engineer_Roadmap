# Day 9: Chunking Strategies

## 1. Detailed Theory

You can't embed an entire 500-page PDF as a single vector because:
1. It won't fit in the embedding model's context window.
2. The resulting vector would be too "noisy" and lose specific semantic meaning.
We must split documents into **chunks**.

### Chunking Strategies

- **Fixed-Size Chunking:** Split by a fixed number of characters or tokens (e.g., 500 tokens). Simple, but might cut a sentence in half. Overlap (e.g., 50 tokens) is used to maintain context between chunks.
- **Recursive Character Chunking:** Attempts to split by paragraphs first, then sentences, then words. This keeps semantic units intact better than fixed-size.
- **Semantic Chunking:** Advanced technique that measures the vector similarity between sentences. If the similarity drops, it assumes a new topic has started and creates a chunk boundary.
- **Document-Specific (Markdown/HTML):** Splitting by `# Heading 1`, `## Heading 2`, etc., ensuring each chunk represents a specific section.

## 2. Recommended YouTube Tutorials

- [Advanced RAG: Chunking Strategies (Greg Kamradt)](https://www.youtube.com/watch?v=8OJC21T2SW4) - The absolute best tutorial on chunking.
- [The ultimate guide to Chunking for RAG (Pinecone)](https://www.youtube.com/watch?v=eqOlsT-Wn0c)

## 3. Real-Time Project GitHub Links

- [Unstructured](https://github.com/Unstructured-IO/unstructured) - The best library for parsing and chunking messy file formats (PDFs, Word, PPT).
- [LangChain Text Splitters](https://github.com/langchain-ai/langchain/tree/master/libs/text-splitters) - Review the source code for recursive character splitters.
