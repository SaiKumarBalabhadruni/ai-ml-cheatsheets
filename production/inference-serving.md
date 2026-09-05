# AI Inference & Model Serving

## Inference

Using a trained model to produce an output.

## Model Serving

Making a model available to applications through an API or other interface.

## Basic Architecture

```text
Client
 ↓
API Gateway
 ↓
Load Balancer
 ↓
Inference Server
 ↓
Model Runtime
 ↓
GPU / Accelerator
 ↓
Response
```

## Batch Inference

Processes many examples together.

Useful for:

- Offline scoring
- Large datasets
- Scheduled workloads

## Online Inference

Processes requests interactively.

Important metrics include:

- Latency
- TTFT
- Throughput
- Error rate

## Dynamic / Continuous Batching

Requests can be grouped dynamically to improve accelerator utilization.

## Model Runtime

The software stack that loads and executes the model.

Performance depends on:

- Kernel implementation
- Precision
- Memory management
- Batching
- Scheduling
- Hardware support

## Scaling

### Horizontal Scaling

Add more servers or accelerators.

### Vertical Scaling

Use a larger or more capable machine.

## Load Balancing

Distributes traffic across available inference workers.

## Autoscaling

Adjusts capacity according to demand.

## Production Checklist

- Model versioning
- Health checks
- Timeouts
- Retries
- Rate limits
- Authentication
- Logging
- Metrics
- Tracing
- Capacity planning
- Cost monitoring
