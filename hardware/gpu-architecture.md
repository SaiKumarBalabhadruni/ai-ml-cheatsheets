# GPU Architecture Cheat Sheet

> The exact architecture differs by vendor and generation. This page uses NVIDIA terminology where terms such as SM and CUDA Core are used.

## High-Level View

```text
GPU
│
├── Compute / Execution
│   ├── SMs
│   ├── CUDA Cores
│   └── Tensor Cores
│
├── On-chip Memory
│   ├── Registers
│   ├── Shared Memory
│   └── Cache
│
└── External Memory
    └── HBM / GDDR
```

## SM — Streaming Multiprocessor

An SM is a major execution block inside an NVIDIA GPU.

It contains resources for:

- Scheduling
- Thread execution
- Registers
- Shared memory
- CUDA Cores
- Tensor Cores

## CUDA Core

A general-purpose arithmetic execution unit within an NVIDIA GPU.

Do not compare one CUDA Core directly with one CPU core.

## Tensor Core

Specialized hardware for matrix and tensor operations.

Tensor Cores are particularly important for deep learning.

## Warp

A group of threads executed together on NVIDIA GPUs.

Efficient GPU programs try to keep threads in a warp following compatible execution paths.

## Thread

A single execution instance.

Thousands or millions of threads may be launched for a workload, depending on the application.

## Thread Block

A group of threads that can cooperate and share certain resources.

## Register

Very fast per-thread storage.

Registers are limited, so excessive register use can reduce the number of active threads.

## Shared Memory

Fast memory accessible by threads in a thread block.

It is useful for data reuse and communication within a block.

## Global Memory

Large GPU memory visible to GPU workloads.

It has much higher capacity than registers or shared memory but higher access latency.

## GPU Kernel

A function executed by GPU threads.

## Occupancy

A measure related to how many active warps can reside on an SM compared with its hardware capacity.

High occupancy can help hide latency, but maximum occupancy is not automatically maximum performance.

## Key Performance Idea

GPU performance depends on much more than raw arithmetic units.

Consider:

```text
Compute
+
Memory bandwidth
+
Memory locality
+
Kernel efficiency
+
Occupancy
+
Communication
+
Synchronization
```
