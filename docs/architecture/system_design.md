# System Design

## Overview

The Indian Sign Language (ISL) Recognition system is designed to convert sign language videos into corresponding word predictions using deep learning. The system follows a multi-stage pipeline, beginning with raw video acquisition and ending with gesture classification.

---

## System Workflow

The overall workflow consists of the following stages:

1. Raw Video Collection
2. MediaPipe Holistic Landmark Extraction
3. Landmark Cleaning and Verification
4. Coordinate Normalization
5. Dataset Preparation
6. Train-Validation-Test Split
7. Coordinate-Level Data Augmentation
8. Model Training
9. Model Evaluation
10. Gesture Prediction

---

## Pipeline Description

### 1. Raw Video Collection

Word-level Indian Sign Language videos are collected from the Kaggle ISL Video Dataset.

---

### 2. Landmark Extraction

Each video is processed using the MediaPipe Holistic framework to extract hand landmark coordinates for every frame.

Only hand landmarks are retained for model development.

---

### 3. Data Cleaning

The extracted landmark sequences are verified to ensure data consistency, remove invalid samples, and prepare the dataset for training.

---

### 4. Coordinate Normalization

Hand landmark coordinates are normalized relative to the wrist, making the wrist the origin of the coordinate system.

This reduces variations caused by different camera positions and signer locations.

---

### 5. Dataset Preparation

The processed landmark sequences are organized into fixed-length sequences consisting of 30 frames.

Labels are encoded into numerical values suitable for model training.

---

### 6. Dataset Splitting

The dataset is divided into training, validation, and testing subsets using stratified sampling to preserve class distribution.

---

### 7. Data Augmentation

Coordinate-level augmentation techniques are applied only to the training dataset to improve model robustness.

These include:

* Gaussian Noise
* Scale Jitter
* Time Warp

---

### 8. Model Training

The processed sequences are used to train temporal deep learning models.

The project initially employed a BiLSTM with Attention as the baseline model, followed by experiments exploring improved architectures to reduce overfitting and enhance generalization.

---

### 9. Model Evaluation

The trained models are evaluated using multiple performance metrics, including:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

---

### 10. Gesture Prediction

The final trained model predicts the corresponding ISL word for an unseen sequence of hand landmark coordinates.

---

## System Summary

The proposed pipeline transforms raw ISL videos into structured landmark sequences suitable for temporal deep learning models, enabling efficient recognition of dynamic sign language gestures.
