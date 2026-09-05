# Attention & QKV Cheat Sheet

## The Core Idea

Attention answers:

> Given this token, which other information should matter?

## Q, K, V

### Q — Query

Represents what the current token is looking for.

### K — Key

Represents what information a token offers for matching.

### V — Value

Contains the information retrieved when a token is attended to.

## Simplified Flow

```text
Input
 ↓
Q projection
K projection
V projection
 ↓
Q × Kᵀ
 ↓
Scale
 ↓
Softmax
 ↓
Attention Weights
 ↓
Weighted V
 ↓
Output
```

A simplified attention equation is:

```text
Attention(Q,K,V)
=
softmax(QKᵀ / √dₖ)V
```

where `dₖ` is the key dimension.

## Self-Attention

The queries, keys, and values come from the same sequence.

## Multi-Head Attention

Multiple attention heads operate in parallel.

Different heads can learn different relationships.

## MHA — Multi-Head Attention

The standard multi-head formulation.

## MQA — Multi-Query Attention

Multiple query heads share key/value heads.

This can reduce KV-cache memory and bandwidth requirements during generation.

## GQA — Grouped-Query Attention

Groups of query heads share key/value heads.

GQA is a compromise between MHA and MQA.

## Causal Attention

In autoregressive language generation, a token is prevented from attending to future tokens.

This preserves the left-to-right generation objective.

## Attention Cost

Standard full self-attention has quadratic scaling with sequence length in the attention matrix.

This is one reason long-context inference can become computationally and memory intensive.

## FlashAttention

An optimized attention algorithm that reduces memory traffic by using tiling and efficient computation rather than materializing all intermediate attention data in the naive way.

## KV Cache

During autoregressive generation, previously computed key/value states can be cached.

```text
Without KV Cache
Recompute previous K/V repeatedly

With KV Cache
Store previous K/V
        ↓
Reuse them for future tokens
```
