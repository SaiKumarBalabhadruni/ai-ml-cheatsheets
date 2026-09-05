# Diffusion Models Cheat Sheet

## Core Idea

Diffusion models learn to generate data by learning a process that reverses a noise-adding process.

A simplified view:

```text
Clean Data
   ↓
Add Noise
   ↓
More Noise
   ↓
Nearly Random
```

Training teaches a model to reverse this process.

```text
Noise
 ↓
Denoising Step
 ↓
Denoising Step
 ↓
Denoising Step
 ↓
Generated Sample
```

## Common Components

A diffusion system may include:

- Noise schedule
- Denoising network
- Conditioning mechanism
- Latent representation
- Sampler / scheduler

## Text-to-Image

A text prompt can condition generation.

```text
Prompt
 ↓
Text Encoder
 ↓
Conditioning
 ↓
Denoising Model
 ↓
Image Representation
 ↓
Decoder
 ↓
Image
```

The exact architecture varies.

## Latent Diffusion

Instead of operating directly on full-resolution pixels, diffusion can operate in a learned latent representation.

This can reduce computational cost.

## Sampling Steps

More denoising steps do not universally mean better output. Quality and speed depend on the model and sampler.

## Key Trade-Offs

- Image quality
- Generation speed
- Resolution
- Memory
- Conditioning strength
- Sampling strategy
