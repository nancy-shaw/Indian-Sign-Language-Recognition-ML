# Paper 06

## Title

INCLUDE: A Large Scale Dataset for Indian Sign Language Recognition

## Authors

Advaith Sridhar, Rohith Gandhi Ganesan, Pratyush Kumar, Mitesh Khapra

## Publication

ACM Multimedia Conference (MM'20), 2020

---

## Objective

The primary objective of this paper is to introduce the first large-scale publicly available Indian Sign Language dataset called INCLUDE (Indian Lexicon Sign Language Dataset) and benchmark deep learning methods for ISL recognition.

The authors aimed to address the lack of high-quality, publicly available ISL datasets and establish baseline performance for sign language recognition models.

---

## Problem Statement

Before this work:

* Most ISL datasets were small.
* Many datasets were not publicly available.
* Existing datasets often used controlled environments.
* Vocabulary size was very limited.

These limitations made it difficult to develop and compare sign language recognition systems.

The authors therefore created a large-scale dataset that resembles real-world signing conditions.

---

## Dataset

### INCLUDE Dataset

Key Statistics:

* 263 ISL word classes
* 4,287 videos
* 0.27 million frames
* 15 word categories
* 7 experienced signers
* Full HD resolution (1920×1080)
* 25 FPS videos
* Average video duration: 2.57 seconds

Categories include:

* Greetings
* Animals
* Occupations
* Electronics
* Places
* Society
* Colours
* Seasons
* Pronouns
* Clothing
* Transportation

and several others.

---

## INCLUDE-50 Subset

To allow faster experimentation, the authors also created:

### INCLUDE-50

Characteristics:

* 50 selected ISL words
* 958 videos
* 60,897 frames
* Covers all 15 categories

This subset was used for rapid model evaluation and hyperparameter tuning.

---

## Data Collection Process

The dataset was collected:

* At St. Louis College for the Deaf and Blind
* With support from experienced ISL signers
* Under natural classroom environments
* Without controlled backgrounds
* Without gloves or sensors

Important Characteristics:

* Real-world lighting
* Real-world backgrounds
* Different signer styles
* Multiple recordings per class

This improves practical applicability compared to earlier datasets.

---

## Proposed Methodology

The recognition pipeline consists of four stages:

### 1. Data Augmentation

Techniques used:

* Center Crop
* Horizontal Flip
* Up-sampling
* Down-sampling

These methods increased dataset diversity and improved generalization.

### 2. Feature Extraction

The authors use OpenPose.

Extracted features:

* Body keypoints
* Hand keypoints
* Pose maps
* Part Affinity Fields (PAF)

OpenPose converts raw video frames into meaningful skeletal representations.

### 3. Feature Encoding

Several pretrained CNN architectures were evaluated:

* MobileNetV2
* ResNet50V2
* DenseNet201
* InceptionV3

These networks generated compact frame-level embeddings.

### 4. Sequence Modeling

Temporal information was modeled using:

* BiLSTM (Bidirectional Long Short-Term Memory)

The BiLSTM processes sign movements across video frames and predicts the final sign class.

---

## Alternative Method Evaluated

The authors also experimented with:

### OpenPose Keypoints + XGBoost

Pipeline:

OpenPose → Keypoint Extraction → Feature Vector → XGBoost Classifier

This approach achieved strong performance while requiring significantly lower computational resources.

---

## Best Performing Model

Architecture:

OpenPose Pose Video
→ MobileNetV2 Encoder
→ BiLSTM Decoder
→ Softmax Classifier

This configuration produced the highest accuracy on the dataset.

---

## Experimental Results

### INCLUDE-50

Best Accuracy:

94.5%

Model:

MobileNetV2 + BiLSTM

---

### Full INCLUDE Dataset

Best Accuracy:

85.6%

Model:

MobileNetV2 + BiLSTM

---

### ASLLVD Dataset (American Sign Language)

The same pipeline was evaluated on ASLLVD.

Accuracy:

92.1%

This demonstrated strong generalization across sign languages.

---

## Key Findings

### 1. Dataset Quality Matters

Large-scale and diverse datasets significantly improve model performance.

### 2. OpenPose Features Are Effective

Pose-based representations provide strong sign recognition performance.

### 3. MobileNetV2 + BiLSTM Performs Best

Among all evaluated architectures, this combination achieved the highest recognition accuracy.

### 4. Data Augmentation Improves Accuracy

Augmentation increased recognition accuracy substantially.

### 5. Transfer Learning Works Well

The same architecture generalized successfully to American Sign Language datasets.

---

## Relevance to Our Project

This paper is extremely relevant because our project also focuses on:

* Indian Sign Language recognition
* Video-based sign detection
* Real-time interpretation
* Deep learning approaches
* Pose estimation techniques

The paper provides valuable guidance for:

* Dataset collection
* Data preprocessing
* Feature extraction
* Model architecture selection
* Evaluation methodology

---

## Limitations

* Focuses on isolated word recognition.
* Does not perform sentence-level translation.
* Uses OpenPose, which can be computationally expensive.
* Real-time deployment challenges remain.

---

## Key Learning

A combination of pose estimation, transfer learning, and sequence modeling can achieve highly accurate Indian Sign Language recognition without requiring special sensors or gloves.

---

## Impact on Our Work

This paper helped us understand:

* Large-scale ISL dataset creation.
* OpenPose-based feature extraction.
* CNN + BiLSTM architectures.
* Practical ISL recognition pipelines.
* Benchmark performance for future comparison.

The INCLUDE dataset can serve as an important benchmark dataset for evaluating future versions of our ISL recognition system.
