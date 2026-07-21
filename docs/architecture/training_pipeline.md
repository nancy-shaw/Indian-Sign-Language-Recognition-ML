# Training Pipeline

## Overview

All deep learning models evaluated in this project followed the same data preparation and training workflow. Maintaining a consistent pipeline ensured that performance differences were primarily due to model architecture rather than preprocessing or training variations.

---

## Step 1: Dataset Preparation

The ISL video dataset was collected and processed to create a landmark-based dataset suitable for temporal deep learning models.

Each sample represents a single ISL word.

Dataset Characteristics:

* 129 gesture classes
* 30 frames per sequence
* 126 landmark features per frame

---

## Step 2: Landmark Extraction

MediaPipe Holistic was used to extract hand landmark coordinates from each video.

Only hand landmarks were retained for model development.

---

## Step 3: Coordinate Normalization

All landmark coordinates were normalized relative to the wrist, making the wrist the origin of the coordinate system.

This reduced variations caused by different camera positions and signer locations.

---

## Step 4: Dataset Splitting

The processed dataset was divided into:

* Training Set
* Validation Set
* Test Set

using stratified sampling to preserve class distribution.

---

## Step 5: Data Augmentation

Coordinate-level augmentation was applied only to the training data.

The augmentation techniques included:

* Gaussian Noise
* Scale Jitter
* Time Warp

The same augmentation strategy was used across all model architectures to ensure fair comparison.

---

## Step 6: Model Training

The following architectures were evaluated:

* LSTM + Attention
* BiLSTM + Attention
* GRU + Attention
* BiGRU + Attention
* Temporal Convolutional Network (TCN)

Each model was trained independently using the same dataset split and preprocessing pipeline.

---

## Step 7: Hyperparameter Optimization

Hyperparameters were tuned independently for each architecture.

The explored parameters included:

* Hidden dimensions / Channel width
* Number of layers
* Dropout rate
* Learning rate
* Weight decay
* Random seed

Multiple experiments were conducted to identify the most stable and generalizable configuration.

---

## Step 8: Training Strategy

Depending on the architecture, the following techniques were incorporated during training:

* Adam Optimizer
* ReduceLROnPlateau Learning Rate Scheduler
* Early Stopping
* Layer Normalization
* Label Smoothing
* Dropout

Each experiment saved the model achieving the best validation performance.

---

## Step 9: Model Evaluation

The trained models were evaluated on the independent test set using:

* Accuracy
* Precision
* Recall
* Macro F1-Score
* Weighted F1-Score
* Confusion Matrix
* Classification Report
* Train–Validation Gap

These metrics were used to compare different architectures and identify the most effective model.

---

## Step 10: Model Selection

The final architecture was selected based on:

* Test Accuracy
* Macro F1-Score
* Validation Performance
* Generalization Ability
* Overfitting Analysis

Among the evaluated architectures, the Temporal Convolutional Network (TCN) achieved the best overall performance and was selected as the final model.
