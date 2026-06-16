# Dataset Source

## Dataset Information

The primary dataset used in this project was obtained from Kaggle:

Dataset: ISL Video Dataset

Source:
https://www.kaggle.com/datasets/swaptr/isl-video

---

## Dataset Type

* Video Dataset
* Indian Sign Language (ISL)
* Word-level Sign Recognition

Each sample in the dataset represents a signed word performed through hand gestures and body movements.

---

## Initial Dataset Structure

The dataset consisted of video samples corresponding to multiple ISL word classes.

The number of video samples varied across classes, resulting in an uneven distribution of training data.

The dataset was collected and organized before further processing and feature extraction.

---

## Feature Generation

Since sequence-based deep learning models were planned for experimentation, raw video frames were not used directly for training.

Instead, MediaPipe was used to extract hand landmarks from video sequences.

The generated landmarks provided a compact representation of gesture movement while significantly reducing data dimensionality.

---

## Training Data Representation

Final model inputs were generated using sequences of landmark coordinates extracted from video samples.

Training data therefore consisted of:

* MediaPipe landmark coordinates
* Sequential landmark representations
* Processed feature sequences suitable for LSTM-based architectures

---

## Purpose

The dataset serves as the primary source for training and evaluating machine learning and deep learning models for Indian Sign Language recognition.

## Future Dataset Expansion

Additional publicly available datasets and custom-collected datasets may be incorporated in future project phases to improve data diversity, model robustness, and generalization performance.
