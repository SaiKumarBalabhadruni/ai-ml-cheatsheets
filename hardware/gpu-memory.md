# GPU Memory & Bandwidth Cheat Sheet

## Capacity vs Bandwidth

These are different.

**Memory capacity:** How much data can fit?

**Memory bandwidth:** How quickly can data move?

A GPU can have enough capacity but still be limited by bandwidth.

## VRAM

GPU-accessible memory used to hold model and workload data.

Common contents include:

- Model weights
- Activations
- KV cache
- Temporary tensors
- Runtime buffers

## HBM — High Bandwidth Memory

A high-bandwidth memory technology commonly used with data-center accelerators.

Its design provides a very wide memory interface and high data-transfer rates.

## GDDR — Graphics Double Data Rate

A high-speed memory technology commonly used with graphics cards.

## SRAM

Fast memory technology commonly used for caches and other on-chip storage.

## DRAM

A widely used memory technology underlying many system and graphics-memory implementations.

## Cache

Fast memory used to keep frequently accessed data closer to compute.

## Memory Hierarchy

A simplified view:

```text
Fastest / Smallest
       ↓
Registers
       ↓
Shared / Local Memory
       ↓
L1 / L2 Cache
       ↓
VRAM / HBM / GDDR
       ↓
System RAM
       ↓
Storage
Slowest / Largest
```

The exact hierarchy differs by architecture.

## Why Memory Matters for LLMs

LLM workloads repeatedly move model parameters and intermediate values.

During inference, the KV cache can also become a significant memory consumer.

During training, memory may be required for:

```text
Weights
+ Gradients
+ Optimizer State
+ Activations
+ Temporary Buffers
```

## Weight-Only Estimate

A first-order estimate:

```text
Weight Memory ≈ Parameters × Bytes per Parameter
```

Examples:

```text
7B × 2 bytes  ≈ 14 GB
7B × 1 byte   ≈ 7 GB
7B × 0.5 byte ≈ 3.5 GB
```

These are weight-only estimates. Real runtime memory is higher when additional state is required.

## Bandwidth Mental Model

Think of compute as a factory and memory bandwidth as the supply road.

```text
More compute
    ↓
More data required
    ↓
Memory system must supply it
    ↓
If data arrives too slowly
    ↓
Compute units wait
```
