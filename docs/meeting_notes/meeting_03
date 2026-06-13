# Meeting 03

## Date

13 June 2026

## Objective

To review the current model performance, evaluate the impact of data augmentation, discuss model improvement strategies, and plan future dataset expansion and experimentation.

---

## Progress Presented

The current implementation of the Indian Sign Language (ISL) Recognition system was demonstrated, including the preprocessing pipeline, model architecture, and training results.

Project progress at the time of the meeting:

* Literature review completed
* Dataset collection completed
* Data cleaning completed
* Data preprocessing completed
* Landmark generation completed
* Initial model training completed

The current model achieved an accuracy of approximately 94%.

---

## Discussion

### Model Evaluation

The current results were reviewed and it was discussed that accuracy alone is not sufficient for evaluating model performance.

To obtain a more comprehensive assessment of the model, the following evaluation metrics will also be considered:

* Precision
* Recall
* F1-Score

These metrics will help evaluate class-level performance and provide a clearer understanding of the model's generalization capability.

---

### Dataset Size and Data Augmentation

The available dataset contained approximately 5000 samples, which was considered relatively small for training an LSTM-based model.

To address this limitation, data augmentation techniques were applied to increase the amount of training data and improve model performance.

During the discussion, concerns were raised regarding the possibility of introducing bias through augmented samples. It was suggested that model performance should also be evaluated using the original non-augmented dataset to establish a reliable baseline and determine whether augmentation is influencing the results.

---

### Overfitting Analysis

The model showed indications of overfitting during training.

To better understand the impact of augmentation and model generalization, it was suggested that:

* The model should be trained without augmentation.
* Results should be compared against the augmented version.
* Evaluation metrics should be analyzed across both experiments.

This comparison will help determine whether the observed performance improvements are genuine or influenced by dataset bias introduced during augmentation.

---

### LSTM Architecture Exploration

The current implementation uses an LSTM-based architecture.

It was suggested that different LSTM variants and sequence-learning architectures should be explored and compared to identify the most suitable approach for the project.

Potential areas of investigation include:

* Single-layer LSTM
* Multi-layer LSTM
* Bidirectional LSTM (BiLSTM)
* CNN-LSTM architectures
* GRU-based architectures
* Hybrid LSTM-GRU models

The objective is to compare performance, robustness, and generalization capability across different architectures.

---

### Data Augmentation Research

In addition to evaluating the current augmentation strategy, it was suggested that different augmentation techniques suitable for sign language recognition should be researched.

Areas for future investigation include:

* Geometric transformations
* Temporal augmentation methods
* Landmark-based augmentation
* Noise injection techniques
* Sequence-level augmentation approaches

The goal is to identify augmentation methods that improve generalization while minimizing the risk of introducing artificial patterns or bias.

---

### Future Dataset Expansion

The next phase of the project will focus on expanding the available training data.

Two potential approaches were discussed.

#### Approach 1: Public Datasets

* Identify additional sign language datasets from Kaggle and other public sources.
* Explore both word-level and sentence-level datasets.
* Perform data cleaning, preprocessing, and integration into the existing workflow.

#### Approach 2: YouTube Dataset Creation

* Collect sign language videos from YouTube.
* Develop a structured storage and organization process.
* Explore manual and AI-assisted labeling approaches.
* Convert collected videos into a usable training dataset.

This approach would help increase dataset diversity and improve model robustness.

---

## Key Outcomes

* The current model achieved approximately 94% accuracy.
* Accuracy alone was considered insufficient for evaluation.
* Precision, Recall, and F1-Score will be incorporated into future evaluations.
* Potential bias introduced by data augmentation was identified as a concern.
* A baseline experiment without augmentation will be conducted.
* Different LSTM-based architectures will be explored and compared.
* Appropriate augmentation techniques for sign language recognition will be researched and evaluated.
* Additional datasets will be explored to increase training data diversity.
* YouTube-based dataset collection was identified as a potential future direction.

---

## Action Items

* Train and evaluate the model without data augmentation.
* Calculate Precision, Recall, and F1-Score.
* Compare augmented and non-augmented model performance.
* Research different LSTM architectures and sequence-learning approaches.
* Study augmentation techniques suitable for sign language datasets.
* Evaluate the impact of augmentation on model generalization.
* Research additional public sign language datasets.
* Explore YouTube data collection and labeling workflows.
