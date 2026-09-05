# Large Language Model Fundamentals

## LLM — Large Language Model

An LLM is a neural network trained to model language.

Many modern LLMs use Transformer architectures.

## Token

A token is a unit processed by the model.

It may correspond to:

- A complete word
- Part of a word
- Punctuation
- Another tokenizer-defined fragment

## Tokenization

Converts text into token IDs.

```text
Text
 ↓
Tokenizer
 ↓
Token IDs
 ↓
Model
```

## Vocabulary

The set of tokens recognized by a tokenizer.

## Embedding

A learned numerical representation of a token or other object.

## Parameters

Learned numerical values in the model.

Parameter count is a rough measure of model scale, not a complete measure of capability.

## Context Window

The amount of tokenized information available to the model for a particular request.

Context includes whatever the specific system counts as input/state.

## Logits

Raw model outputs before conversion into a probability distribution.

## Softmax

Converts logits into probabilities.

## Temperature

A sampling parameter that changes the concentration of the output distribution.

Higher temperature generally makes sampling more varied.

## Top-k

Restricts sampling to the k highest-probability candidate tokens.

## Top-p

Restricts sampling to a set of candidate tokens whose cumulative probability reaches a chosen threshold.

## Prompt

Input supplied to a model.

## Instruction Tuning

Training a model to follow natural-language instructions.

## Fine-Tuning

Additional training that adapts an existing model.

## Pretraining

Large-scale initial training that teaches general patterns.

## Hallucination

A generated statement that is incorrect, fabricated, or unsupported while appearing plausible.

## Model Size

A model's parameter count is useful context, but runtime requirements also depend on:

- Precision
- Architecture
- Context length
- Batch size
- KV cache
- Runtime implementation
- Additional buffers
