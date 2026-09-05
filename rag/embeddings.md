# Embeddings & Vector Search Cheat Sheet

## Embedding

An embedding is a numerical vector representation of an object.

Examples:

- Text
- Images
- Audio
- Documents

The goal is to represent useful relationships geometrically.

## Example

```text
"How do GPUs work?"
        ↓
[0.12, -0.44, 0.81, ...]
```

The vector is not inherently meaningful to a human. Its usefulness comes from how the embedding model organizes representations.

## Similarity

Common similarity measures include:

- Cosine similarity
- Dot product
- Euclidean distance

The correct metric depends on the embedding and indexing setup.

## Vector Search

Given a query vector:

```text
Query
 ↓
Embedding
 ↓
Search Vector Index
 ↓
Nearest / Similar Vectors
 ↓
Documents
```

## Vector Database

A system that stores vectors and supports efficient similarity search.

## ANN — Approximate Nearest Neighbor

Search methods that trade some exactness for faster retrieval at scale.

Examples of indexing approaches include graph-based and quantized indexes.

## Semantic Search

Search based on meaning rather than exact keyword matches.

## Hybrid Search

Combines semantic/vector retrieval with lexical/keyword retrieval.

## Metadata Filtering

Adds structured constraints such as:

```text
department = "finance"
date > 2025-01-01
document_type = "policy"
```

## Reranking

A second-stage model can reorder the top retrieved candidates.

## Key Principle

Retrieval quality is not only about the vector database.

It depends on:

```text
Chunking
+
Embedding Model
+
Index
+
Search Parameters
+
Metadata
+
Reranking
+
Evaluation
```
