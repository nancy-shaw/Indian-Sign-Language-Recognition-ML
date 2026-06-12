# Paper 03

## Title

Indian Sign Language Recognition System

## Authors

Yogeshwar I. Rokade and Prashant M. Jadav

## Publication

International Journal of Engineering and Technology (IJET), 2017

## Paper Type

Research Paper

---

## Objective

The objective of this paper is to develop an automatic Indian Sign Language (ISL) recognition system capable of recognizing static hand gestures used by deaf and mute individuals.

The system aims to reduce communication barriers between hearing-impaired individuals and the general population through automated sign recognition.

---

## Dataset

The study focuses on 17 Indian Sign Language alphabet gestures:

A, B, D, E, F, G, H, J, K, O, P, Q, S, T, X, Y and Z.

Dataset Details:

* Total Images: 848
* Training Images: 548
* Testing Images: 300
* Resolution: 320 × 240
* Black background images

The dataset consists of static gesture images representing ISL alphabets.

---

## Approach Used

The paper follows a traditional computer vision pipeline:

Input Image
→ Skin Segmentation
→ Noise Removal
→ Feature Extraction
→ Classification
→ Gesture Recognition

This workflow is useful for understanding the foundations of sign language recognition systems.

---

## Preprocessing Techniques

### Hand Segmentation

The authors use:

* RGB color space analysis
* Skin color detection
* Adaptive probabilistic skin model
* Binary image generation

to isolate the hand region from the image.

### Noise Removal

The paper applies:

* Morphological operations
* Erosion
* Dilation

to reduce segmentation noise.

---

## Feature Extraction

The paper uses several handcrafted feature extraction techniques:

### Distance Transform

Converts the segmented binary image into a distance representation using Euclidean distance.

### Row and Column Projection

Used to generate shape descriptors representing the hand gesture.

### Fourier Descriptors

Applied to capture shape information from projection vectors.

### Central Moments

Used to describe distribution characteristics of gesture features.

### Hu Moments

Used for shape representation and invariance to:

* Translation
* Rotation
* Scaling

A total of 13 features are extracted from each gesture image.

---

## Classification Models

The authors compare two classifiers:

### Artificial Neural Network (ANN)

* Feed-forward neural network
* Supervised learning approach

### Support Vector Machine (SVM)

* Polynomial kernel
* Tested using multiple feature combinations

Both models are trained and evaluated on the extracted feature vectors.

---

## Results

### ANN Performance

| Feature Set | Accuracy |
| ----------- | -------- |
| 6 Features  | 88.3%    |
| 8 Features  | 91.94%   |
| 13 Features | 94.37%   |

### SVM Performance

| Feature Set | Accuracy |
| ----------- | -------- |
| 6 Features  | 69.92%   |
| 8 Features  | 89.33%   |
| 13 Features | 92.12%   |

ANN achieved the highest overall accuracy of 94.37%.

---

## Key Findings

### 1. Feature Engineering Matters

Increasing the number of extracted features significantly improved recognition accuracy.

### 2. ANN Outperformed SVM

The Artificial Neural Network consistently achieved higher accuracy than SVM across all experiments.

### 3. Effective Preprocessing Is Critical

Skin segmentation and feature extraction played an important role in overall system performance.

---

## Relevance to Our ISL Project

This paper is useful because:

* It focuses specifically on Indian Sign Language.
* It demonstrates a complete recognition pipeline.
* It highlights the importance of preprocessing.
* It provides insight into feature extraction techniques.
* It offers a baseline approach for comparison with modern deep learning methods.

---

## Limitations

* Only static gestures are recognized.
* Dataset size is relatively small.
* No real-time implementation.
* Does not use modern CNN or Transformer architectures.

---

## Key Learning

Traditional computer vision methods can achieve strong performance on ISL recognition tasks, but they rely heavily on handcrafted features. Modern deep learning approaches can automate feature extraction and scale better to larger datasets.

---

## Impact on Our Work

This paper helped us understand:

* Classical ISL recognition pipelines.
* The importance of preprocessing and segmentation.
* Feature extraction strategies.
* ANN and SVM-based classification methods.

The study serves as a useful baseline for comparing traditional approaches with modern deep learning models in our project.
