# Machine Learning Fundamentals

## The Basic Idea

Machine learning learns a mapping from examples instead of requiring every rule to be manually programmed.

```text
Data
 ↓
Model
 ↓
Prediction
 ↓
Loss / Error
 ↓
Learning Algorithm
 ↓
Updated Model
```

## Supervised Learning

The dataset contains inputs and desired targets.

```text
Input → Target
Image → Cat
Image → Dog
```

Typical supervised tasks include classification and regression.

## Unsupervised Learning

The model searches for structure without explicit labels.

Examples:

- Clustering
- Dimensionality reduction
- Density estimation

## Self-Supervised Learning

The training target is derived from the input data.

For language models, a common objective is predicting missing or next tokens.

## Train / Validation / Test

- **Training set:** used to learn parameters.
- **Validation set:** used to make development decisions.
- **Test set:** reserved for final evaluation.

The exact split depends on the problem.

## Generalization

A useful model should perform well on unseen examples, not merely memorize its training set.

## Overfitting

Symptoms:

- Very good training performance
- Worse validation/test performance

Possible responses:

- More data
- Regularization
- Simpler model
- Data augmentation
- Early stopping
- Better validation methodology

## Underfitting

Symptoms:

- Poor training performance
- Poor validation performance

Possible responses:

- More expressive model
- Better features
- Better optimization
- More training
- Better data

## Bias and Variance

A useful conceptual decomposition:

- **High bias:** model is too constrained.
- **High variance:** model is too sensitive to training data.

The goal is good generalization, not simply maximizing training performance.

## Feature Engineering

Traditional ML often relies heavily on choosing useful input representations.

Deep learning reduces some of this manual feature engineering by learning representations directly from data.

## Data Leakage

Data leakage occurs when information unavailable at prediction time enters training or evaluation.

Leakage can produce misleadingly high metrics.

## Rule of Thumb

Before changing the model, ask:

1. Is the data correct?
2. Is the target defined correctly?
3. Is the evaluation representative?
4. Is there leakage?
5. Is the baseline strong enough?
6. What is the actual bottleneck?
