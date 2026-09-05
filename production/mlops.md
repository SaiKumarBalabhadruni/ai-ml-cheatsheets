# MLOps Cheat Sheet

## MLOps — Machine Learning Operations

MLOps covers the practices and infrastructure needed to develop, deploy, monitor, and maintain ML systems.

## Typical Lifecycle

```text
Data
 ↓
Experiment
 ↓
Training
 ↓
Evaluation
 ↓
Model Registry
 ↓
Deployment
 ↓
Monitoring
 ↓
Retraining / Update
```

## Experiment Tracking

Record:

- Dataset version
- Model configuration
- Hyperparameters
- Metrics
- Code version
- Model artifacts

## Model Registry

Stores and manages model versions and metadata.

## Data Versioning

Tracks versions of datasets and data-processing inputs.

## CI/CD

Automated software practices for testing, building, and deploying changes.

## Monitoring

Production monitoring can include:

- Latency
- Throughput
- Errors
- Resource usage
- Model quality
- Data distribution

## Data Drift

The input distribution changes over time.

## Concept Drift

The relationship between inputs and desired outcomes changes.

## Model Drift

Model performance decreases as the environment changes.

## Canary Deployment

Release a new version to a small portion of traffic before wider rollout.

## A/B Testing

Compare variants using defined metrics.

## Observability

Understanding system behavior through:

- Logs
- Metrics
- Traces

## Important Principle

A model is not a production system by itself.

Production quality depends on:

```text
Model
+
Data
+
Serving
+
Infrastructure
+
Security
+
Monitoring
+
Operations
```
