# Paper 05

## Title

Deepsign: Sign Language Detection and Recognition Using Deep Learning

## Authors

Deep Kothadiya, Chintan Bhatt, Krenil Sapariya, Kevin Patel, Ana-Belén Gil-González, Juan M. Corchado

## Publication

Electronics, MDPI (2022)

## Paper Type

Research Paper

---

## Objective

The objective of this paper is to develop a deep learning-based Indian Sign Language (ISL) recognition system capable of recognizing dynamic sign language gestures from video sequences.

The proposed system aims to bridge communication barriers between hearing-impaired individuals and the general population by converting sign gestures into meaningful words using deep learning techniques.

---

## Problem Statement

Most sign language recognition systems focus on static gestures or require external devices such as gloves, sensors, or controlled environments.

The authors aim to develop a real-world sign language recognition system that:

* Works with normal video input.
* Does not require gloves or sensors.
* Operates under natural lighting conditions.
* Recognizes dynamic Indian Sign Language gestures.

---

## Dataset

### IISL2020 Dataset

The authors created their own dataset called IISL2020.

Dataset Characteristics:

* 11 commonly used ISL words
* Approximately 1100 video samples per word
* 16 participants
* Male and female signers
* Average video length: 2 seconds
* Resolution: 1920 × 1080
* Average frame rate: 28 FPS

Examples of words included:

* Hello
* Bye
* Good Morning
* Good
* Nice
* House
* Thank You
* Welcome
* Yes
* No
* Work

The dataset was collected in real-world conditions without using gloves, sensors, or controlled backgrounds.

---

## Proposed Methodology

The recognition pipeline consists of:

### Step 1: Video Acquisition

Input videos containing ISL gestures are collected.

### Step 2: Frame Extraction

Video sequences are divided into individual frames.

### Step 3: Feature Extraction

The authors use InceptionResNetV2 as the feature extraction backbone.

The extracted feature vectors represent visual information from each frame.

### Step 4: Sequence Modeling

The extracted features are passed to recurrent neural networks:

* LSTM
* GRU
* Hybrid LSTM-GRU architectures

### Step 5: Classification

A Softmax layer predicts the final sign class.

---

## Deep Learning Models Evaluated

The paper compares multiple architectures:

### Single Models

* Single-layer LSTM
* Single-layer GRU

### Hybrid Models

* LSTM-LSTM
* GRU-GRU
* GRU-LSTM
* LSTM-GRU

The purpose of the comparison was to determine the most effective sequence-learning architecture for sign language recognition.

---

## Architecture Details

The best-performing architecture consists of:

1. InceptionResNetV2 Feature Extractor
2. LSTM Layer
3. GRU Layer
4. Dense Layer
5. Dropout Layer
6. Softmax Classification Layer

Training Parameters:

* Batch Size: 16
* Dropout: 0.3
* 10-Fold Cross Validation
* TensorFlow/Keras Framework

The model processes video sequences represented as 40 time-step feature vectors.

---

## Results

### IISL2020 Dataset

| Model     | F1 Score |
| --------- | -------- |
| GRU-GRU   | 0.90     |
| LSTM-LSTM | 0.95     |
| GRU-LSTM  | 0.89     |
| LSTM-GRU  | 0.97     |

The LSTM-GRU architecture achieved the highest performance.

Overall Accuracy:

97% Recognition Accuracy

The model also performed well on other benchmark sign language datasets including ASL, GSL, and AUTSL.

---

## Key Findings

### 1. Hybrid Models Outperform Individual Models

Combining LSTM and GRU produced better results than using either architecture alone.

### 2. Temporal Information Matters

Video-based recognition captures gesture movement information that static image approaches cannot represent effectively.

### 3. Real-World Data Collection Is Possible

The dataset was collected without special equipment, making the approach more practical for deployment.

### 4. Deep Learning Improves Dynamic Sign Recognition

Sequential deep learning models effectively learn temporal dependencies between gesture frames.

---

## Relevance to Our Project

This paper is highly relevant because it demonstrates:

* Indian Sign Language recognition.
* Deep learning-based sequence modeling.
* Real-time recognition concepts.
* Video-based gesture analysis.
* Dataset collection under natural conditions.

The paper provides valuable insights for future expansion of our project from isolated gesture recognition toward dynamic sign and sentence recognition.

---

## Limitations

* Limited to 11 words.
* Focuses on isolated sign recognition.
* Does not perform complete sentence translation.
* Dataset size can be further expanded.

---

## Key Learning

Dynamic sign language recognition requires both spatial feature extraction and temporal sequence learning. Combining a CNN-based feature extractor with recurrent neural networks such as LSTM and GRU significantly improves recognition performance.

---

## Impact on Our Work

This paper helped us understand:

* Video-based sign language recognition pipelines.
* Deep learning architectures for sequential gesture data.
* LSTM and GRU-based sequence modeling.
* Real-world dataset collection practices.
* Future possibilities for continuous sign language interpretation.

The study serves as an important reference for extending our project beyond static sign recognition toward more advanced dynamic gesture understanding.
