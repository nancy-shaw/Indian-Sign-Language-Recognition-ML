# Experiment 03: Model Optimization and Architecture Exploration

## Objective

The objective of this phase was to investigate methods for reducing overfitting and improving the generalization performance of the baseline BiLSTM model.

---

## Background

Although the baseline BiLSTM with Attention achieved encouraging validation performance, a noticeable gap remained between training and validation accuracy.

Training loss continued to decrease while validation loss plateaued, indicating that the model was beginning to memorize the training data rather than learning generalized gesture representations.

This issue became more significant because of the limited number of samples available for each class.

---

## Discussion with Project Supervisor

The observed overfitting and dataset limitations were discussed with the project supervisor.

Based on the analysis, several recommendations were made to improve model robustness while working with a limited dataset.

The suggested directions included:

* Coordinate-level data augmentation
* ArcFace Loss
* Layer Normalization
* Reduced model capacity
* Temporal Convolutional Networks (TCN)

---

## Research Directions Explored

### Coordinate-Level Augmentation

To improve robustness without collecting additional data, augmentation techniques suitable for landmark coordinates were explored.

These included:

* Gaussian Noise
* Scale Jitter
* Time Warp
* Spatial transformations

---

### ArcFace Loss

ArcFace Loss was investigated as an alternative to standard CrossEntropy Loss.

The objective was to encourage compact intra-class feature representations while increasing separation between different gesture classes.

---

### Layer Normalization

Layer Normalization was considered to stabilize feature distributions across temporal sequences and improve training stability on the relatively small dataset.

---

### Model Capacity Reduction

Reducing model complexity was explored to decrease overfitting.

Possible modifications included:

* Smaller hidden dimensions
* Fewer recurrent layers
* Reduced attention complexity

---

### Temporal Convolutional Networks (TCN)

Based on literature review and supervisor recommendations, Temporal Convolutional Networks were identified as a promising alternative to recurrent architectures.

Compared to BiLSTM models, TCNs offer:

* Fewer trainable parameters
* Parallel computation
* Improved gradient flow
* Better generalization on limited time-series datasets

---

## Outcome

Following these investigations, the project direction shifted toward implementing and evaluating a TCN-based architecture for Indian Sign Language recognition.

This marked the transition from baseline model development to architecture optimization.
