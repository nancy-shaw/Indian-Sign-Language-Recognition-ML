# Paper 02

## Title

Sign Language Recognition Using Convolutional Neural Networks

## Authors

Lionel Pigou, Sander Dieleman, Pieter-Jan Kindermans, Benjamin Schrauwen

## Institution

Ghent University, Belgium

## Publication

ECCV Workshops, 2015

## Paper Type

Research Paper

---

## Objective

The objective of this paper is to develop an automatic sign language recognition system using Convolutional Neural Networks (CNNs) and Microsoft Kinect data.

The authors aim to reduce the communication gap between the Deaf community and the hearing population by recognizing sign language gestures automatically.

---

## Dataset

The authors used the ChaLearn Looking at People 2014 (CLAP14) dataset.

Dataset characteristics:

* 20 Italian gestures
* 27 different users
* Variations in lighting, clothing and background
* RGB images
* Depth maps
* Skeleton joint information from Kinect

Dataset split:

* Training samples: 4600
* Validation samples: 2000
* Test samples: 3543

---

## Preprocessing Techniques

The preprocessing stage was one of the most important parts of the system.

The authors:

1. Cropped the highest hand region.
2. Cropped the upper body region.
3. Mirrored left-hand gestures to reduce variation.
4. Removed background using user index information.
5. Applied thresholding.
6. Applied median filtering for noise reduction.
7. Generated four input channels:

   * Hand depth
   * Hand grayscale
   * Body depth
   * Body grayscale

Final input size:

64 × 64 × 32 frames

---

## Proposed Architecture

The system consists of:

### Feature Extraction

Two separate CNN networks:

* CNN 1 → Hand Features
* CNN 2 → Upper Body Features

Each CNN contains:

* 3 convolutional layers
* Max pooling layers
* ReLU activation functions
* Local Contrast Normalization (LCN)

### Classification

After feature extraction:

* Outputs of both CNNs are concatenated.
* A traditional Artificial Neural Network (ANN) performs final classification.

---

## Training Strategy

To improve generalization and reduce overfitting, the authors used:

### Dropout

Randomly disables neurons during training.

### Data Augmentation

Applied:

* Zooming
* Rotation
* Spatial Translation
* Temporal Translation

### Optimization

* Nesterov Accelerated Gradient (NAG)
* Momentum = 0.9
* Mini-batch size = 20

---

## Results

Best Validation Accuracy:

91.7%

Test Accuracy:

95.68%

Competition Performance:

Mean Jaccard Index = 0.7888

The model ranked among the top-performing teams in the ChaLearn Gesture Spotting Challenge.

---

## Key Learnings

### CNNs Automatically Learn Features

Unlike traditional methods that require handcrafted features, CNNs automatically learn useful gesture representations from image data.

### Preprocessing Significantly Improves Performance

The paper shows that cropping, normalization, background removal, and noise reduction directly improve recognition accuracy.

### Data Augmentation Reduces Overfitting

Data augmentation helped improve model robustness to different users and environments.

### Generalization Is Important

The model successfully recognized gestures from users and backgrounds not seen during training.

---

## Relevance to Our ISL Project

This paper is highly relevant to our project because:

* It demonstrates a complete sign language recognition pipeline.
* It highlights the importance of preprocessing.
* It provides practical CNN architecture ideas.
* It shows methods to improve generalization.
* It offers useful evaluation metrics and training strategies.

Many preprocessing techniques described in this paper are conceptually similar to the preprocessing stage completed in our project.

---

## Limitations

* Dataset limited to 20 gestures.
* Uses Kinect sensor data which may not always be available.
* Focuses on isolated gesture recognition rather than full sentence interpretation.

---

## Impact on Our Work

This paper helped us understand:

* CNN-based sign language recognition.
* Gesture preprocessing workflows.
* Data augmentation strategies.
* Model training and evaluation procedures.

The paper will be useful during our upcoming model training phase as a reference for architecture design and training methodology.
