# AI Model Training Cheat Sheet

## Training Loop

```text
Dataset
 ↓
Batch
 ↓
Forward Pass
 ↓
Prediction
 ↓
Loss
 ↓
Backpropagation
 ↓
Gradients
 ↓
Optimizer
 ↓
Updated Parameters
 ↓
Repeat
```

## Forward Pass

The model processes inputs and produces outputs.

## Loss

Measures how well the model performed according to its training objective.

## Backpropagation

Calculates gradients of the loss with respect to model parameters.

## Optimizer

Uses gradients to update parameters.

Examples:

- SGD
- Adam
- AdamW

## Learning Rate

Controls the magnitude of parameter updates.

## Batch Size

Number of examples processed before an optimization update, subject to the exact training setup.

## Gradient Accumulation

Accumulates gradients across multiple smaller batches before an update.

Useful when the desired effective batch size does not fit in memory.

## Epoch

One complete pass through a dataset.

## Checkpoint

A saved model/training state.

Checkpoints are useful for:

- Recovery
- Resuming training
- Evaluation
- Experiment comparison

## Mixed Precision

Uses different numerical formats for different operations.

Common formats include FP16 and BF16.

Benefits can include:

- Lower memory use
- Higher throughput
- Reduced memory traffic

## Training Memory

A rough conceptual model:

```text
Weights
+
Gradients
+
Optimizer State
+
Activations
+
Temporary Buffers
+
Framework Overhead
```

## Distributed Training

Large workloads can be distributed across multiple accelerators.

Common approaches:

- Data parallelism
- Tensor parallelism
- Pipeline parallelism
- Sharding

## Training Efficiency

A useful optimization process is:

```text
Measure
 ↓
Find bottleneck
 ↓
Change one thing
 ↓
Measure again
```

Avoid optimizing based solely on intuition.
