# Distributed AI Training Cheat Sheet

## Why Distribute Training?

A model or dataset may be too large or too slow for one accelerator.

Multiple accelerators can divide the work.

## Data Parallelism

Each device holds a copy of the model and processes different data.

```text
GPU 1 → Batch A
GPU 2 → Batch B
GPU 3 → Batch C
GPU 4 → Batch D
       ↓
Synchronize Gradients
```

## Model Parallelism

Different parts of a model are placed on different devices.

## Tensor Parallelism

Individual tensor operations are divided across devices.

Useful when a single model layer is too large or when additional parallel compute is beneficial.

## Pipeline Parallelism

Different model layers are assigned to different devices.

```text
GPU 1 → Layers 1–10
GPU 2 → Layers 11–20
GPU 3 → Layers 21–30
```

Microbatches can be pipelined through the stages.

## Sharding

Model parameters, optimizer state, or other data are split across devices.

## All-Reduce

A collective operation that combines values across devices and distributes the result.

It is commonly used for gradient synchronization.

## Communication Matters

Distributed training is not just:

```text
More GPUs = More speed
```

You also pay for:

- GPU-to-GPU communication
- Synchronization
- Network latency
- Network bandwidth
- Load imbalance

## Scaling Efficiency

Ideal scaling would double useful throughput when doubling resources.

Real systems experience overhead.

A useful conceptual model:

```text
Total Speedup
≈
Compute Benefit
− Communication
− Synchronization
− Imbalance
− Other Overhead
```

## Interconnects

Common technologies include:

- PCIe
- NVLink
- High-performance Ethernet
- InfiniBand

The appropriate technology depends on system design.
