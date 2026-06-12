# Paper 04

## Title

Real-time Vernacular Sign Language Recognition using MediaPipe and Machine Learning

## Authors

Arpita Halder, Akshit Tayade

## Publication

International Journal of Research Publication and Reviews (IJRPR), Volume 2, Issue 5, 2021

## Paper Type

Research Paper

---

## Objective

The objective of this paper is to develop a lightweight and real-time sign language recognition system using MediaPipe and machine learning techniques. The proposed system aims to bridge the communication gap between deaf-mute individuals and the general population by enabling accurate hand gesture recognition without requiring wearable sensors.

---

## Problem Statement

Traditional sign language recognition systems often rely on:

* Wearable sensors
* Colored gloves
* Complex image processing techniques
* High computational resources

These approaches can be expensive, inconvenient, and difficult to deploy on real-time devices.

The paper proposes a simpler and more efficient approach using MediaPipe's hand-tracking framework combined with machine learning algorithms.

---

## Datasets Used

The study evaluates the proposed approach on multiple sign language datasets:

| Dataset                            | Classes | Images  |
| ---------------------------------- | ------- | ------- |
| American Sign Language (Alphabets) | 26      | 156,000 |
| Indian Sign Language (Alphabets)   | 24      | 4,972   |
| Italian Sign Language (Alphabets)  | 22      | 12,856  |
| American Sign Language (Numbers)   | 10      | 1,400   |
| Turkey Sign Language (Numbers)     | 10      | 4,124   |

---

## Proposed Architecture

The proposed system consists of three major stages:

### Stage 1: Hand Landmark Extraction

* Input images are processed using MediaPipe Hands.
* MediaPipe detects hand regions and extracts hand landmarks.
* A total of 21 hand landmarks are generated for each detected hand.
* Landmark coordinates are stored in CSV format for model training.

### Stage 2: Data Cleaning and Normalization

* Landmark datasets are checked for missing values.
* Samples with detection failures are removed.
* Coordinate values are normalized.
* Data is divided into training and validation sets.

### Stage 3: Machine Learning Classification

The cleaned landmark dataset is used to train machine learning models for gesture classification.

---

## MediaPipe Framework

The paper highlights MediaPipe as a lightweight and efficient framework for hand tracking.

Key features:

* Real-time hand detection
* 21 three-dimensional hand landmarks
* Robust performance under varying conditions
* Low computational requirements
* Suitable for mobile and edge devices

The framework significantly simplifies feature extraction compared to traditional computer vision approaches.

---

## Machine Learning Models Evaluated

The authors compared multiple classification algorithms:

* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)
* Random Forest
* Decision Tree
* Naive Bayes
* Artificial Neural Network (ANN)
* Multi-Layer Perceptron (MLP)

---

## Evaluation Metrics

The following performance metrics were used:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix Analysis

The study also employed 10-Fold Cross Validation to ensure reliable evaluation.

---

## Results

### Indian Sign Language Dataset

| Metric            | Value  |
| ----------------- | ------ |
| Training Accuracy | 99.92% |
| Testing Accuracy  | 99.29% |
| Precision         | 99.29% |
| Recall            | 99.29% |
| F1-Score          | 99.29% |

### Overall Findings

* SVM achieved the highest accuracy among all evaluated models.
* The proposed MediaPipe + SVM pipeline achieved approximately 99% accuracy across multiple datasets.
* The system demonstrated strong generalization performance and real-time usability.

---

## Key Findings

### 1. MediaPipe Simplifies Feature Extraction

The framework automatically extracts hand landmarks, eliminating the need for complex image segmentation and handcrafted feature engineering.

### 2. Landmark-Based Features Are Effective

Hand landmark coordinates provide sufficient information for accurate gesture recognition.

### 3. SVM Outperformed Other Models

Support Vector Machines achieved the best performance compared to KNN, Random Forest, Decision Trees, ANN, and MLP.

### 4. Real-Time Deployment Is Feasible

The proposed system requires low computational resources, making it suitable for mobile and smart-device deployment.

---

## Relevance to Our Project

This paper is highly relevant to our Indian Sign Language Recognition project because it follows a workflow very similar to our implementation strategy.

Similarities include:

* MediaPipe-based hand landmark extraction
* Data cleaning and preprocessing
* Feature generation using landmark coordinates
* Machine learning-based classification
* Real-time sign recognition objective

The paper validates our current project pipeline and provides a strong baseline for future experimentation.

---

## Limitations

* Focuses primarily on finger-spelling recognition.
* Does not perform sentence-level interpretation.
* Uses landmark-based features rather than deep learning-based visual representations.
* Limited exploration of sequential gesture recognition.

---

## Key Learning

This paper demonstrates that high-accuracy sign language recognition can be achieved without complex deep learning architectures. MediaPipe landmark extraction combined with a suitable machine learning classifier can produce accurate, lightweight, and real-time sign language recognition systems.

---

## Impact on Our Work

The paper helped us understand:

* Practical use of MediaPipe for hand tracking.
* Landmark-based feature extraction techniques.
* Data cleaning and normalization workflows.
* Machine learning model selection.
* Real-time deployment considerations.

It serves as one of the most relevant references for our current project implementation.
