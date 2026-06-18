# Day 2: The Transformer Architecture

## 1. Detailed Theory

The **Transformer** is the foundational architecture behind modern LLMs (like GPT, Claude, and Llama). Before transformers, models processed text sequentially (RNNs, LSTMs), making it hard to remember long contexts and slow to train. The Transformer solved this.

### Core Components

1. **Self-Attention Mechanism:**
   - The heart of the transformer. It allows the model to look at *other words* in the input sequence to better understand a specific word's context. 
   - Example: "The bank of the river" vs "The bank on the corner." Self-attention links "bank" with "river" or "corner" to figure out the meaning.
   
2. **Multi-Head Attention:**
   - Instead of computing attention once, transformers compute it multiple times in parallel ("heads"). One head might focus on grammar, another on semantic meaning, another on the relationship between nouns and verbs.

3. **Feed-Forward Neural Networks:**
   - After attention is calculated, the data passes through a standard neural network layer to process and transform the representations.

4. **Positional Encoding:**
   - Since transformers process all words simultaneously (not sequentially), positional encoding adds information about the *order* of the words.

### Goal: Why GPT Works
GPT (Generative Pre-trained Transformer) is a decoder-only transformer. It excels because self-attention allows it to hold massive contextual relationships simultaneously, and pre-training on the internet gives it a vast statistical understanding of human language.

## 2. Recommended YouTube Tutorials

- [Illustrated Guide to Transformers Neural Network: A step by step explanation (The AI Hacker)](https://www.youtube.com/watch?v=4Bdc55j80l8) - Visual breakdown of the architecture.
- [Attention Is All You Need (Paper Explanation by Yannic Kilcher)](https://www.youtube.com/watch?v=iDulhoQ2pro) - Deep dive into the original paper that started it all.
- [3Blue1Brown: Attention in neural networks, visually explained](https://www.youtube.com/watch?v=eMlx5fFNoYc) - Masterclass in visualizing the math.

## 3. Real-Time Project GitHub Links

- [nanoGPT](https://github.com/karpathy/nanoGPT) - The simplest, fastest repository for training/finetuning medium-sized GPTs.
- [minGPT](https://github.com/karpathy/minGPT) - A minimal PyTorch re-implementation of the GPT training loop.
