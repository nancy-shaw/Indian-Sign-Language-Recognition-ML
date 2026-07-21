# Model Architecture

## Overview

Multiple deep learning architectures were investigated for Indian Sign Language recognition using identical preprocessed landmark sequences. All models were trained on the same 129-class dataset with the same preprocessing pipeline to ensure a fair comparison.

The evaluated architectures include:

* LSTM with Attention
* BiLSTM with Attention
* GRU with Attention
* BiGRU with Attention
* Temporal Convolutional Network (TCN)

---

## Common Input Representation

All architectures receive the same input.

Input:

* Sequence Length: 30 Frames
* Features per Frame: 126
* Wrist-relative normalized landmark coordinates

Input Shape:

```
(batch_size, 30, 126)
```

Every model receives identical landmark sequences generated from the preprocessing pipeline.

---

## LSTM with Attention

The LSTM model processes landmark sequences in chronological order to capture temporal dependencies.

Pipeline:

Input

↓

LSTM

↓

Attention

↓

Context Vector

↓

Layer Normalization

↓

Dropout

↓

Fully Connected Layer

↓

Softmax Classifier

---

## BiLSTM with Attention

The BiLSTM extends the LSTM by processing the sequence in both forward and backward directions before applying attention.

Pipeline:

Input

↓

Forward LSTM

↓

Backward LSTM

↓

Concatenation

↓

Attention

↓

Context Vector

↓

Layer Normalization

↓

Dropout

↓

Fully Connected Layer

↓

Softmax Classifier

---

## GRU / BiGRU

The GRU-based architectures replace LSTM memory cells with Gated Recurrent Units to reduce model complexity while preserving temporal learning capability.

Pipeline:

Input

↓

GRU / BiGRU

↓

Attention

↓

Dense Layer

↓

Dropout

↓

Output Layer

↓

Softmax Classifier

---

## Temporal Convolutional Network (TCN)

The TCN architecture replaces recurrent processing with stacked temporal convolutional blocks.

Pipeline:

Input Landmark Sequence

↓

Transpose

↓

Temporal Block 1

↓

Temporal Block 2

↓

Temporal Block 3

↓

Temporal Block 4

↓

Global Average Pooling

↓

Dropout

↓

Fully Connected Layer

↓

Softmax Classifier

---

## Comparative Study

All architectures were trained using the same landmark dataset, preprocessing pipeline, augmentation strategy, and evaluation protocol.

This enabled an unbiased comparison of recurrent and convolutional temporal models for Indian Sign Language recognition.

The TCN architecture achieved the strongest overall performance and was selected as the final model for the project.
