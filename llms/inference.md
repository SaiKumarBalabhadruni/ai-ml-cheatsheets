# LLM Inference Cheat Sheet

## What Is Inference?

Inference is running a trained model to produce an output.

## Two Major Phases

### Prefill

The model processes the input prompt.

The prompt can often be processed with substantial parallelism.

### Decode

The model generates output tokens sequentially.

Each generated token depends on the preceding context.

```text
Prompt
 ↓
Prefill
 ↓
First Token
 ↓
Decode
 ↓
Next Token
 ↓
Decode
 ↓
...
```

## KV Cache

During decoding, key/value states from previous tokens can be cached.

This avoids recomputing those states from scratch for every new token.

## TTFT — Time to First Token

Time from request initiation until the first generated token is available.

TTFT is strongly influenced by request processing and prefill work.

## TPS — Tokens Per Second

Generated tokens per second.

It is useful for measuring generation throughput but should be interpreted alongside latency and workload details.

## ITL — Inter-Token Latency

Time between generated tokens.

## Batching

Processing multiple requests together can improve accelerator utilization.

## Continuous Batching

Requests enter and leave an active batch dynamically as their generation progresses.

This can improve utilization in multi-user serving systems.

## Throughput vs Latency

A server may optimize for:

- Low latency for individual requests
- High aggregate throughput
- A balance of both

These goals can conflict.

## Speculative Decoding

A smaller or faster model proposes candidate tokens.

A larger model verifies them.

If many proposals are accepted, generation can be accelerated.

## Inference Bottlenecks

Potential bottlenecks include:

- GPU compute
- Memory bandwidth
- KV-cache memory
- VRAM capacity
- CPU overhead
- PCIe transfer
- Network communication
- Scheduling
- Kernel efficiency

## Cost

Production inference cost depends on:

```text
Hardware
+
Utilization
+
Model size
+
Precision
+
Context
+
Batching
+
Traffic pattern
+
Software efficiency
```
