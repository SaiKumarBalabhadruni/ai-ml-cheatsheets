# RAG — Retrieval-Augmented Generation

## What Is RAG?

RAG combines information retrieval with generative models.

Instead of relying only on model parameters:

```text
Question
 ↓
Retrieve Relevant Information
 ↓
Provide Context to Model
 ↓
Generate Answer
```

## Basic Architecture

```text
Documents
 ↓
Chunking
 ↓
Embedding
 ↓
Index
 ↓
Retriever
 ↓
Relevant Chunks
 ↓
Prompt + Context
 ↓
LLM
 ↓
Answer
```

## Why Use RAG?

RAG can help when information is:

- Private
- Frequently changing
- Too large to put directly into every prompt
- Better represented as documents
- Required to be traceable to sources

## Chunking

Documents are split into smaller retrieval units.

Trade-offs:

**Small chunks:**

- More precise retrieval
- Less context per chunk

**Large chunks:**

- More context
- Potentially less precise retrieval
- More tokens per request

## Retriever

Finds candidate information.

Retrieval can use:

- Keyword search
- Vector search
- Hybrid search

## Reranker

Reorders retrieved candidates using a more detailed relevance model.

## Grounding

The model's response is tied to retrieved or external information.

## Common Failure Modes

- Poor chunking
- Weak embeddings
- Irrelevant retrieval
- Missing metadata filters
- Too much retrieved context
- Conflicting sources
- Model ignores retrieved evidence

## RAG Is Not Fine-Tuning

**RAG:** changes the information supplied at inference time.

**Fine-tuning:** changes model parameters through additional training.

They can also be used together.
