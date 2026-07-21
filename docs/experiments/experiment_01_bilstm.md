# Experiment 01: BiLSTM with Attention (Baseline Model)

## Objective

The objective of this experiment was to develop a baseline deep learning model capable of recognizing Indian Sign Language (ISL) gestures from sequences of hand landmark coordinates extracted using MediaPipe Holistic.

---

## Dataset

* Landmark-based dataset
* 260 ISL word classes
* Sequence length: 30 frames
* Features per frame: 126
* Wrist-relative normalized hand coordinates

---

## Model Architecture

The baseline model consisted of:

* Bidirectional Long Short-Term Memory (BiLSTM)
* Attention Mechanism
* Fully Connected Classification Layer
* Dropout (0.6)

The BiLSTM was used to learn temporal dependencies from landmark sequences, while the attention mechanism enabled the model to focus on the most informative frames before classification.

---

## Training Configuration

Framework: PyTorch

Training setup:

* Loss Function: CrossEntropy Loss
* Optimizer: Adam
* Learning Rate Scheduler: ReduceLROnPlateau
* Early Stopping
* Dropout: 0.6

---

## Evaluation Metrics

The model was evaluated using:

* Training Accuracy
* Validation Accuracy
* Test Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report
* Overfitting Analysis

---

## Results

The baseline model achieved good training performance but exhibited signs of overfitting during later epochs.

Training loss continued to decrease, whereas validation loss plateaued, indicating limited generalization to unseen samples.

This suggested that the model was memorizing training patterns rather than learning robust gesture representations.

---

## Key Observations

* Strong learning capability on the training set.
* Validation performance saturated after several epochs.
* Large gap between training and validation accuracy.
* Performance was affected by limited samples per class and class imbalance.

---

## Conclusion

The BiLSTM with Attention model established a strong baseline for sequence classification. However, the observed overfitting highlighted the need for further experimentation with data augmentation, architectural modifications, and alternative temporal models to improve generalization.
