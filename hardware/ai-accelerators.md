# AI Accelerators Cheat Sheet

## AI Accelerator

Hardware designed to accelerate machine-learning computation.

Common categories include:

- GPU
- TPU
- NPU
- ASIC
- FPGA

## GPU

General-purpose parallel accelerator widely used for AI.

Strengths:

- Flexible programming
- Large software ecosystem
- High throughput
- Broad model support

## TPU — Tensor Processing Unit

Google's specialized accelerator family designed for machine-learning workloads.

## NPU — Neural Processing Unit

A processor optimized for neural-network operations.

NPUs are increasingly integrated into client devices for on-device AI.

## ASIC — Application-Specific Integrated Circuit

A chip designed for a particular workload or class of workloads.

Advantages:

- Potentially high efficiency
- Specialized data paths
- Predictable workload optimization

Trade-off:

- Less flexible than general-purpose accelerators

## FPGA — Field-Programmable Gate Array

Reconfigurable hardware.

It can sit between general-purpose processors and fixed-function ASICs in terms of flexibility and specialization.

## Accelerator Selection

A useful decision framework:

```text
Need maximum flexibility?
        ↓
GPU

Need specialized AI processing?
        ↓
TPU / NPU / ASIC

Need reconfigurability?
        ↓
FPGA
```

Actual selection depends on workload, software, cost, power, deployment environment, and ecosystem.
