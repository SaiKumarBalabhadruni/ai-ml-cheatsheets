# Fine-Tuning & PEFT Cheat Sheet

## Fine-Tuning

Fine-tuning continues training from an existing model checkpoint.

It can adapt a model to:

- A domain
- A task
- A style
- A desired instruction-following behavior

## Full Fine-Tuning

All or most model parameters are updated.

Advantages:

- Maximum flexibility

Costs:

- High memory requirements
- More compute
- Larger optimizer state
- More storage for model variants

## PEFT — Parameter-Efficient Fine-Tuning

Updates only a small portion of trainable parameters or adds trainable components.

Benefits:

- Lower memory
- Lower training cost
- Smaller adapters
- Easier model sharing

## LoRA — Low-Rank Adaptation

LoRA adds trainable low-rank matrices while keeping the base model weights frozen.

Conceptually:

```text
Base Model
   +
Small Trainable Adapter
   ↓
Adapted Model
```

## QLoRA

QLoRA combines a quantized base model with LoRA-style adapters to reduce fine-tuning memory requirements.

## SFT — Supervised Fine-Tuning

Fine-tuning using examples containing desired outputs.

## Instruction Tuning

Training designed to improve the model's ability to follow instructions.

## Preference Optimization

Uses preference data to favor better responses.

## DPO — Direct Preference Optimization

A preference-optimization method that directly trains on preference comparisons.

## Adapter

A small trainable component that modifies model behavior without changing the entire base model.

## Choosing a Method

```text
Need maximum adaptation?
        ↓
Full Fine-Tuning

Need lower cost / memory?
        ↓
PEFT / LoRA

Need lower base-model memory?
        ↓
Quantization + PEFT
```
