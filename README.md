# AI & ML Cheatsheets

> A practical, open reference for understanding Artificial Intelligence, Machine Learning, Deep Learning, AI hardware, LLMs, Generative AI, RAG, AI agents, training, inference, and AI infrastructure.

The goal of this repository is simple:

**Make complex AI concepts understandable, technically accurate, and easy to reference.**

This is designed to work both as a learning path and as a quick-reference library.

---

## Repository Map

### 🧠 AI & ML Foundations

- [AI & ML Glossary](./foundations/ai-ml-glossary.md)
- [Machine Learning Fundamentals](./foundations/machine-learning.md)
- [Deep Learning Fundamentals](./foundations/deep-learning.md)
- [AI Metrics](./foundations/metrics.md)

### 🖥️ AI Hardware

- [CPU vs GPU](./hardware/cpu-vs-gpu.md)
- [GPU Architecture](./hardware/gpu-architecture.md)
- [GPU Memory & Bandwidth](./hardware/gpu-memory.md)
- [AI Accelerators](./hardware/ai-accelerators.md)

### 🤖 LLMs & Transformers

- [Transformer Architecture](./llms/transformers.md)
- [Attention & QKV](./llms/attention.md)
- [LLM Fundamentals](./llms/llm-fundamentals.md)
- [LLM Inference](./llms/inference.md)

### ⚙️ Training & Optimization

- [Training Fundamentals](./training/training.md)
- [Fine-Tuning & PEFT](./training/fine-tuning.md)
- [Quantization](./training/quantization.md)
- [Distributed Training](./training/distributed-training.md)

### ✨ Generative AI

- [Generative AI](./generative-ai/generative-ai.md)
- [Diffusion Models](./generative-ai/diffusion.md)
- [Multimodal AI](./generative-ai/multimodal.md)

### 🔎 RAG & AI Agents

- [RAG](./rag/rag.md)
- [Embeddings & Vector Search](./rag/embeddings.md)
- [AI Agents](./agents/agents.md)
- [Tool Calling & MCP](./agents/tools-and-mcp.md)

### 🚀 Production AI

- [AI Inference & Serving](./production/inference-serving.md)
- [MLOps](./production/mlops.md)
- [AI Infrastructure](./production/infrastructure.md)

---

## The AI Stack

```text
┌───────────────────────────────────────────────┐
│                 APPLICATIONS                  │
│       Agents • RAG • Copilots • APIs         │
├───────────────────────────────────────────────┤
│                    MODELS                    │
│   LLMs • Transformers • Diffusion • VLMs     │
├───────────────────────────────────────────────┤
│                 COMPUTATION                  │
│ Tensors • Attention • Matrix Multiplication  │
├───────────────────────────────────────────────┤
│                 OPTIMIZATION                 │
│ Quantization • Batching • Kernel Optimization│
├───────────────────────────────────────────────┤
│                 ACCELERATORS                 │
│       GPUs • TPUs • NPUs • ASICs             │
├───────────────────────────────────────────────┤
│              MEMORY & NETWORKING             │
│   VRAM • HBM • RAM • PCIe • NVLink • NICs    │
└───────────────────────────────────────────────┘
```

---

## Recommended Learning Order

If you are new to AI:

1. [Machine Learning Fundamentals](./foundations/machine-learning.md)
2. [Deep Learning Fundamentals](./foundations/deep-learning.md)
3. [CPU vs GPU](./hardware/cpu-vs-gpu.md)
4. [GPU Architecture](./hardware/gpu-architecture.md)
5. [Transformer Architecture](./llms/transformers.md)
6. [Attention & QKV](./llms/attention.md)
7. [LLM Fundamentals](./llms/llm-fundamentals.md)
8. [Training Fundamentals](./training/training.md)
9. [LLM Inference](./llms/inference.md)
10. [Quantization](./training/quantization.md)
11. [RAG](./rag/rag.md)
12. [AI Agents](./agents/agents.md)
13. [AI Infrastructure](./production/infrastructure.md)

---

## Core Mental Models

### CPU vs GPU

```text
CPU
→ Few sophisticated execution resources
→ Flexible control flow
→ Low latency
→ General-purpose work

GPU
→ Many parallel execution resources
→ High throughput
→ Excellent for repetitive numerical work
→ AI training and inference
```

### Training vs Inference

```text
TRAINING
Data
 ↓
Forward Pass
 ↓
Loss
 ↓
Backpropagation
 ↓
Gradients
 ↓
Optimizer
 ↓
Updated Parameters
 ↓
Repeat

INFERENCE
Input
 ↓
Model
 ↓
Output
```

### RAG

```text
Documents
 ↓
Chunking
 ↓
Embeddings
 ↓
Vector / Hybrid Search
 ↓
Relevant Context
 ↓
LLM
 ↓
Answer
```

### Agent

```text
Goal
 ↓
Reason / Plan
 ↓
Choose Tool
 ↓
Tool Call
 ↓
Observe Result
 ↓
Continue or Finish
```

---

## Repository Principles

This repository aims to:

- Explain terminology in plain English without losing technical meaning.
- Separate **capacity**, **bandwidth**, **latency**, and **throughput**.
- Distinguish model concepts from hardware concepts.
- Prefer durable concepts over rapidly changing product specifications.
- Use examples and mental models where they improve understanding.
- Link related concepts so the repository can be read as a connected knowledge map.

### Important terminology rule

A simplified analogy is useful, but it should not replace the real architecture.

For example:

> "A GPU has thousands of workers."

is a useful intuition.

But it should not be interpreted as:

> "A GPU core is exactly equivalent to a CPU core."

The detailed architecture matters.

---

## Contributing

Contributions are welcome.

When adding a cheatsheet:

1. Keep the topic focused.
2. Define acronyms on first use.
3. Explain why the concept matters.
4. Include a mental model where useful.
5. Distinguish simplified explanations from technical details.
6. Add links to related cheatsheets.
7. Prefer primary documentation for implementation-specific claims.

---

## Disclaimer

This repository is an educational reference, not a substitute for official hardware documentation, framework documentation, or research papers.

AI terminology evolves quickly. Product specifications, software APIs, model capabilities, and recommended practices should be checked against current primary sources when precision matters.
