# Deep Learning Fundamentals

## What Is Deep Learning?

Deep learning uses neural networks with multiple layers to learn increasingly useful representations.

```text
Input
 ↓
Layer
 ↓
Layer
 ↓
Layer
 ↓
Output
```

## Forward Pass

The model transforms an input through its layers to produce an output.

## Loss

The loss function measures error or undesirable behavior.

Training attempts to reduce the loss according to the chosen objective.

## Backpropagation

Backpropagation calculates how the loss changes with respect to model parameters.

Conceptually:

```text
Prediction
 ↓
Loss
 ↓
Gradient
 ↓
Parameter Update
```

## Optimizers

Common optimizers include:

- SGD — Stochastic Gradient Descent
- Adam
- AdamW

An optimizer uses gradients to update parameters.

## Learning Rate

The learning rate controls the size of parameter updates.

Too high can make training unstable.

Too low can make training slow or prevent useful progress within the available budget.

## Batch

A batch is a group of examples processed together.

Larger batches can improve hardware utilization but require more memory.

## Epoch

One complete pass through a training dataset.

## Activation Functions

Examples:

- ReLU — Rectified Linear Unit
- GELU — Gaussian Error Linear Unit
- SiLU — Sigmoid Linear Unit

Nonlinear activations allow neural networks to represent more complex functions.

## Regularization

Methods used to improve generalization.

Examples include:

- Weight decay
- Dropout
- Data augmentation
- Early stopping

## Why GPUs Help

Many neural-network operations can be expressed as large tensor operations.

That creates substantial parallel work.

```text
Large tensor operation
        ↓
Many independent arithmetic operations
        ↓
Parallel hardware
        ↓
High throughput
```

## Training Memory

Training can require memory for:

- Parameters
- Gradients
- Optimizer state
- Activations
- Temporary buffers
- Framework overhead
