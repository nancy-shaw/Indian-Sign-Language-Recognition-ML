# Phase 03: Model Development

## Status

In Progress

---

## Objective

To develop, train, and evaluate machine learning and deep learning models for Indian Sign Language recognition.

---

## Progress Made

### Feature Preparation

* Generated landmark-based features from the processed dataset.
* Prepared training data for sequence-based learning models.

### Initial Model Training

* Implemented an LSTM-based architecture.
* Trained the model on the prepared dataset.
* Achieved an initial accuracy of approximately 94%.

### Evaluation

Initial evaluation highlighted the need for additional performance metrics beyond accuracy.

Future evaluations will include:

* Precision
* Recall
* F1-Score

---

## Challenges Identified

### Limited Dataset Size

The available dataset contained approximately 5000 samples, which may be insufficient for robust sequence-model training.

### Overfitting

The model showed indications of overfitting during training.

### Data Augmentation Bias

Data augmentation was applied to increase dataset size. Further experiments are required to determine whether augmentation introduces bias or artificially influences performance.

---

## Current Focus

## Current Focus

* Establish a baseline using the non-augmented dataset.
* Compare augmented and non-augmented performance.
* Explore different LSTM architectures and sequence-learning approaches.
* Research augmentation techniques suitable for sign language datasets.
* Investigate additional publicly available datasets.
* Expand available training data.

---

## Next Steps

* Calculate Precision, Recall, and F1-Score.
* Train and evaluate the model without augmentation.
* Compare augmented and non-augmented results.
* Research and experiment with different LSTM architectures.
* Study augmentation techniques suitable for sign language recognition.
* Collect and integrate additional datasets.
* Continue model experimentation and performance evaluation.

---

## Outcome So Far

The initial model development phase has successfully established a working training pipeline and provided a foundation for future experimentation and optimization.
