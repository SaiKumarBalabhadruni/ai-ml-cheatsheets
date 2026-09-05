# Transformer Architecture Cheat Sheet

## What Is a Transformer?

A Transformer is a neural-network architecture built around attention mechanisms.

Transformers became foundational to modern language models and are also used in vision, audio, multimodal systems, and other domains.

## Simplified Transformer Block

```text
Input
 ↓
Normalization
 ↓
Attention
 ↓
Residual Connection
 ↓
Normalization
 ↓
Feed-Forward Network
 ↓
Residual Connection
 ↓
Output
```

Exact ordering varies by architecture.

## Token Representations

Text is converted into tokens.

Tokens are mapped into numerical representations called embeddings.

```text
Text
 ↓
Tokenizer
 ↓
Token IDs
 ↓
Embedding
 ↓
Transformer
```

## Attention

Attention allows each token to determine which other tokens are relevant.

It is built around Query, Key, and Value representations.

## Feed-Forward Network

The FFN/MLP block applies additional transformations after attention.

## Residual Connection

A residual connection adds an earlier representation to a later transformation.

Residual pathways help deep networks train effectively.

## Layer Normalization

Normalization applied to activations within the Transformer.

## Encoder vs Decoder

### Encoder

Produces representations from input.

Commonly associated with representation-learning architectures.

### Decoder

Generates outputs, often autoregressively.

Many modern LLMs use decoder-only Transformer architectures.

## Autoregressive Generation

The model generates one token at a time:

```text
"The"
"The cat"
"The cat sat"
"The cat sat on"
...
```

Each new token becomes part of the context for the next prediction.

## Why Transformers Scale

Important factors include:

- Parallel processing during training
- Flexible attention-based representations
- Large-scale optimization
- Accelerator-friendly tensor operations
- Strong scaling properties

Scaling behavior depends on architecture, data, optimization, and compute.
