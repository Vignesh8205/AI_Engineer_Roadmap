# Day 1: LLM Fundamentals & Basics

## 1. Detailed Theory

An **LLM (Large Language Model)** is an AI model trained on massive amounts of text data to understand and generate human-like text. Under the hood, LLMs don't read words like we do; they read **tokens**.

### Key Concepts

- **Tokens:** The fundamental unit of data processed by the LLM. A token can be a single character, a part of a word, or an entire word (e.g., "Apple" = 1 token, "hamburger" = 3 tokens). Roughly, 1 token ≈ 0.75 English words.
- **Tokenization:** The process of converting raw text into tokens. Different models use different tokenizers (like Byte Pair Encoding or BPE).
- **Context Window:** The maximum number of tokens an LLM can process in a single request (input + output). If you exceed the context window, the model "forgets" earlier parts of the conversation.
- **Temperature:** Controls the randomness of the output. 
  - `0.0`: highly deterministic, predictable (best for coding/data extraction).
  - `0.7+`: creative, varied (best for brainstorming).
- **Top-P (Nucleus Sampling):** Another way to control randomness. A `top_p` of 0.9 means the model only considers the most probable tokens that add up to 90% cumulative probability. 

### The Flow
```text
Input text -> Tokenization -> Tokens -> LLM -> Output Tokens -> De-tokenization -> Text
```

## 2. Recommended YouTube Tutorials

- [Andrej Karpathy: Let's build GPT: from scratch, in code, spelled out.](https://www.youtube.com/watch?v=kCc8FmEb1nY) - The most comprehensive guide to understanding how LLMs work from the former Director of AI at Tesla.
- [What is an LLM? (IBM Technology)](https://www.youtube.com/watch?v=5sLYAQS9sWQ) - A great high-level conceptual overview.
- [Intro to Large Language Models (Andrej Karpathy)](https://www.youtube.com/watch?v=zjkBMFhNj_g) - Excellent 1-hour conceptual breakdown.

## 3. Real-Time Project GitHub Links

- [tiktoken by OpenAI](https://github.com/openai/tiktoken) - See how tokenization actually works in code.
- [llama.cpp](https://github.com/ggerganov/llama.cpp) - Run LLMs locally to see inference parameters (temperature, top-p) in real time.
