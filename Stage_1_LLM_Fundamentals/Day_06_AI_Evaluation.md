# Day 6: AI Evaluation & Hallucinations

## 1. Detailed Theory

You can't improve what you can't measure. LLMs are non-deterministic, meaning traditional unit tests ("assert output == expected") often fail. 

### Core Concepts

- **Hallucinations:** When an LLM confidently generates false or fabricated information. This happens because they are predicting the next token, not looking up facts.
- **Grounding:** Tying the LLM's responses to actual, verified data (like documents retrieved in RAG) to reduce hallucinations.
- **Evaluation Metrics (LLM-as-a-Judge):** Because output varies, we use other LLMs to evaluate the output based on rubrics:
  - *Faithfulness:* Is the answer derived *only* from the provided context?
  - *Answer Relevance:* Does the answer actually address the user's question?
  - *Context Precision:* Was the retrieved context actually useful?

## 2. Recommended YouTube Tutorials

- [Evaluating Large Language Models (Standford CS224N)](https://www.youtube.com/watch?v=9_1eB07P4xM)
- [Ragas: Automated Evaluation of RAG Pipelines](https://www.youtube.com/watch?v=1Z3H-A8aBts)
- [Why LLMs Hallucinate, and How to Stop Them](https://www.youtube.com/watch?v=eYkK2A5Tkhg)

## 3. Real-Time Project GitHub Links

- [Ragas (RAG Assessment)](https://github.com/explodinggradients/ragas) - Framework for evaluating RAG pipelines.
- [DeepEval](https://github.com/confident-ai/deepeval) - The open-source evaluation framework for LLMs.
