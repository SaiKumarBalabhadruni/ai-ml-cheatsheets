# CPU vs GPU for AI

## CPU — Central Processing Unit

A CPU is a general-purpose processor optimized for flexible execution.

Typical strengths:

- Complex control flow
- Branching
- Low-latency tasks
- Operating-system workloads
- Sequential processing
- General-purpose applications

## GPU — Graphics Processing Unit

A GPU is designed to execute many operations in parallel.

Typical strengths:

- High-throughput numerical computation
- Matrix operations
- Tensor operations
- Large batches
- Neural-network workloads

## The Key Difference

The useful distinction is not simply:

> CPU = slow, GPU = fast.

Instead:

> **CPU = flexible general-purpose computation**

> **GPU = highly parallel throughput-oriented computation**

## Why AI Maps to GPUs

A neural network may require enormous numbers of similar operations.

For example:

```text
A × B

Millions of numerical operations
            ↓
Many can be performed concurrently
            ↓
GPU parallelism
```

## CPU + GPU

A practical AI system normally uses both.

```text
CPU
 ↓
Prepare / coordinate data
 ↓
GPU
 ↓
Compute model operations
 ↓
CPU / network
 ↓
Return result
```

## Common Mistake

A GPU "core" is not simply equivalent to a CPU core.

Modern GPUs use hierarchical execution structures such as:

```text
GPU
 ↓
SMs / Compute Units
 ↓
Threads / Warps / Wavefronts
 ↓
Arithmetic + Matrix Hardware
```

The exact terminology differs by vendor.

## When a CPU May Be Better

- Small workloads
- Branch-heavy algorithms
- Operating-system work
- Serial workloads
- Tasks where accelerator transfer overhead dominates

## When a GPU Is Better

- Large tensor operations
- Matrix multiplication
- Large-batch inference
- Neural-network training
- Parallel numerical workloads
