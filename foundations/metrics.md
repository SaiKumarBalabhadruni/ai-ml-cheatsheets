# AI & ML Metrics Cheat Sheet

## Classification

### Accuracy

```text
Accuracy = Correct Predictions / Total Predictions
```

Useful when classes are reasonably balanced and the cost of errors is similar.

### Precision

```text
Precision = True Positives / (True Positives + False Positives)
```

Question:

> When the model says "positive," how often is it correct?

### Recall

```text
Recall = True Positives / (True Positives + False Negatives)
```

Question:

> Of the actual positives, how many did the model find?

### F1 Score

```text
F1 = 2 × Precision × Recall / (Precision + Recall)
```

F1 balances precision and recall.

## Regression

### MAE — Mean Absolute Error

Average absolute difference between predictions and targets.

### MSE — Mean Squared Error

Average squared difference between predictions and targets.

### RMSE — Root Mean Squared Error

Square root of MSE.

## Language Models

### Perplexity

A measure related to how well a language model predicts a sequence.

Lower values generally indicate better predictive likelihood under the same evaluation setup, but perplexity is not a universal measure of usefulness.

## Generation

Useful system metrics include:

- **TTFT — Time to First Token**
- **TPS — Tokens Per Second**
- **ITL — Inter-Token Latency**
- **E2E Latency — End-to-End Latency**

## System Metrics

- GPU utilization
- Memory utilization
- Memory bandwidth
- Power
- Throughput
- Request latency
- Error rate
- Cost per request

## Important Principle

A single metric rarely describes an AI system.

A production system may need to balance:

```text
Quality
+
Latency
+
Throughput
+
Memory
+
Cost
+
Reliability
```
