# Multimodal AI Cheat Sheet

## What Is Multimodal AI?

Multimodal AI works with multiple data modalities.

Examples:

- Text
- Images
- Audio
- Video
- Sensor data

## Modality

A type of information.

Examples:

```text
Text
Image
Audio
Video
```

## Vision-Language Model — VLM

A model capable of working with visual and language information.

## Embedding-Based Architecture

Different modalities can be mapped into shared or related representation spaces.

```text
Image ─────┐
           ├→ Representation Space
Text ──────┘
```

## Multimodal Fusion

Information from different modalities is combined.

Fusion may happen:

- Early
- Within intermediate layers
- Late

The architecture determines the mechanism.

## Example Workflow

```text
Image
  +
Question
  ↓
Vision Encoder
  +
Text Representation
  ↓
Multimodal Model
  ↓
Answer
```

## Challenges

Multimodal systems must handle:

- Different data rates
- Different representations
- Alignment between modalities
- Large input sizes
- Temporal information
- Missing modalities
- Evaluation complexity
