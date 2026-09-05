# AI & Machine Learning Glossary

A broad reference covering the vocabulary used across AI, machine learning, deep learning, LLMs, Generative AI, and production AI systems.

## AI and ML

- **AI — Artificial Intelligence:** The broad field of building systems capable of tasks associated with intelligence, such as perception, prediction, reasoning, generation, and decision-making.
- **ML — Machine Learning:** A subset of AI in which systems learn patterns from data rather than relying entirely on explicitly programmed rules.
- **Deep Learning:** Machine learning based primarily on multi-layer neural networks.
- **Model:** A mathematical system that maps inputs to outputs.
- **Training:** Adjusting model parameters using data.
- **Inference:** Running a trained model to produce an output.
- **Dataset:** A collection of examples used for training, validation, or testing.
- **Feature:** An input variable used by a model.
- **Label:** A target associated with a training example.
- **Parameter:** A value learned by a model.
- **Hyperparameter:** A configuration selected outside the normal parameter-learning process.

## Learning Types

- **Supervised Learning:** Learning from examples with known targets.
- **Unsupervised Learning:** Finding structure in data without explicit target labels.
- **Self-Supervised Learning:** Learning from training signals constructed from the data itself.
- **Reinforcement Learning (RL):** Learning through interaction and reward signals.
- **Transfer Learning:** Reusing knowledge from a model trained on one task or dataset for another task.

## Common Tasks

- **Classification:** Predicting a discrete category.
- **Regression:** Predicting a continuous value.
- **Clustering:** Grouping similar examples.
- **Ranking:** Ordering items according to relevance or preference.
- **Generation:** Producing new content.
- **Prediction:** Estimating an output from input data.

## Neural Network Terms

- **Neuron:** A mathematical unit that transforms inputs into an output.
- **Layer:** A stage of computation in a neural network.
- **Weight:** A learned parameter controlling the contribution of an input.
- **Bias:** A learned value added to a transformation.
- **Activation:** An intermediate output produced by a model.
- **Activation Function:** A nonlinear function applied within a neural network.
- **Loss Function:** Measures how far a model output is from a target or desired behavior.
- **Gradient:** Measures how the loss changes with respect to parameters.
- **Backpropagation:** Computes gradients through a neural network.
- **Optimizer:** Updates parameters using gradients.

## Evaluation

- **Accuracy:** Fraction of predictions that are correct.
- **Precision:** Among predicted positives, the fraction that are actually positive.
- **Recall:** Among actual positives, the fraction that are correctly identified.
- **F1 Score:** Harmonic mean of precision and recall.
- **Benchmark:** A standardized evaluation used to compare models or systems.
- **Eval:** A systematic test of model behavior.
- **Ground Truth:** Reference information used to evaluate predictions.

## Common Confusions

### Parameter vs Hyperparameter

**Parameter:** learned by the model.

**Hyperparameter:** selected or configured by the developer/training process.

### Training vs Inference

**Training:** changes model parameters.

**Inference:** uses trained parameters to produce outputs.

### Precision vs Accuracy

**Precision:** a numerical representation such as FP16.

**Accuracy:** an evaluation metric.

They are unrelated concepts despite sharing the word "precision."

### Overfitting vs Underfitting

**Overfitting:** model fits training data too specifically.

**Underfitting:** model is too limited to capture important patterns.
