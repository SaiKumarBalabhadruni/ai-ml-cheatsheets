# Quantization Cheat Sheet

## What Is Quantization?

Quantization represents numerical values using fewer bits.

Example:

```text
FP16 → INT8 → INT4
```

Lower precision can reduce:

- Memory
- Memory traffic
- Storage
- Sometimes compute cost

But it can also affect model quality or numerical stability.

## Common Formats

- **FP32:** 32-bit floating point
- **FP16:** 16-bit floating point
- **BF16:** 16-bit floating point with a wide exponent range
- **FP8:** 8-bit floating point
- **INT8:** 8-bit integer
- **INT4:** 4-bit integer

## Weight Memory

Approximate weight storage:

```text
FP32 → 4 bytes/value
FP16 → 2 bytes/value
BF16 → 2 bytes/value
FP8  → 1 byte/value
INT8 → 1 byte/value
INT4 → 0.5 byte/value
```

Real implementations require additional metadata and may use different layouts.

## PTQ — Post-Training Quantization

Quantizes a trained model after training.

## QAT — Quantization-Aware Training

Training accounts for quantization effects.

## Calibration

Representative data can be used to determine suitable quantization scales or other parameters.

## Per-Tensor vs Per-Channel

Quantization scales can be applied at different granularities.

- **Per-tensor:** one scale for a whole tensor.
- **Per-channel:** separate scales for different channels.

The choice can affect accuracy and implementation efficiency.

## Quantization Trade-Off

```text
Fewer bits
   ↓
Less memory
   ↓
Less data movement
   ↓
Potentially faster / cheaper inference
   ↓
But potentially more numerical error
```

## Quantization Is Not Magic

A model using fewer bits is not automatically faster.

Performance depends on whether the hardware and runtime efficiently support the chosen format.

## Practical Questions

Before quantizing, check:

1. Does the target hardware support the format?
2. Does the inference runtime support it efficiently?
3. How much quality loss is acceptable?
4. What memory reduction is actually achieved?
5. Is the workload compute-bound or memory-bound?
