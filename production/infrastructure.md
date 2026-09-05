# AI Infrastructure Cheat Sheet

## Data Center

A facility containing computing, networking, storage, power, cooling, and supporting systems.

## Server

A computer that provides computation or services to other systems.

## Node

One machine in a cluster.

## Cluster

A group of connected machines working together.

## GPU Cluster

A cluster containing accelerators for AI workloads.

## Network

Connects machines and accelerators.

Important characteristics:

- Bandwidth
- Latency
- Topology
- Congestion
- Reliability

## Interconnect

A connection between computing components.

Examples:

- PCIe
- NVLink
- Ethernet
- InfiniBand

## Storage

AI systems may use:

- Local SSDs
- Network storage
- Object storage

Training workloads can be sensitive to data loading throughput.

## Container

A packaged application environment containing software and dependencies.

## Kubernetes

A system for orchestrating containerized workloads across clusters.

## GPU Scheduling

In shared environments, schedulers decide where GPU workloads run.

Important concerns include:

- Capacity
- Isolation
- Fairness
- Utilization
- Priority

## Power

Large AI clusters can consume substantial electrical power.

Power considerations affect:

- Operating cost
- Cooling
- Rack density
- Facility design

## Cooling

Accelerator density creates significant heat.

Data-center cooling approaches can include:

- Air cooling
- Direct-to-chip liquid cooling
- Other liquid-cooling architectures

## Infrastructure Bottlenecks

Potential bottlenecks include:

```text
GPU compute
GPU memory
CPU
RAM
Storage
PCIe
Network
Power
Cooling
Scheduling
```

## Scale

At large scale, system performance is determined by the interaction between compute, memory, networking, storage, software, and operations.
