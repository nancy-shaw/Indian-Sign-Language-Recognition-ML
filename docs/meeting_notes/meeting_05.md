# Meeting 05

**Date:** 07 July 2026

## Objective

To present the progress made after the previous meeting, discuss improvements implemented based on earlier feedback, and compare the performance of multiple deep learning architectures for Indian Sign Language recognition.

---

## Progress Since the Previous Meeting

Following the recommendations from the previous meeting, the project team revisited the complete training pipeline.

During experimentation, it was observed that the initial landmark augmentation strategy was not producing the desired improvements and was affecting model performance.

The augmentation pipeline was therefore redesigned and implemented correctly while keeping the remaining preprocessing pipeline unchanged. This resulted in improved training stability and significantly better model performance across all architectures.

The preprocessing steps maintained across all experiments included:

* Landmark extraction
* Wrist-relative coordinate normalization
* Scaling
* Coordinate-level augmentation
* Consistent train-validation-test split

This ensured that all model comparisons were conducted under identical data preparation conditions.

---

## Model Development

The team divided the experimentation among different temporal architectures.

* Nancy Shaw – Temporal Convolutional Network (TCN)
* Muskan Sah – GRU and BiGRU
* Muskan – LSTM and BiLSTM

Each model was independently optimized through hyperparameter tuning while maintaining the same preprocessing pipeline.

---

## TCN Results

A comparative analysis of three TCN configurations was conducted by varying channel width and dropout while keeping the remaining architecture fixed.

The experiments demonstrated that:

* The best-performing configuration used 64 channels with a dropout rate of 0.3.
* Test Accuracy reached approximately 90.86%.
* Test Macro F1 reached approximately 90.06%.
* Reducing channel width decreased overall performance.
* Increasing dropout improved validation performance but did not consistently improve test performance.

The results suggested that limited training samples per class remained the primary bottleneck rather than excessive model capacity.

---

## LSTM and BiLSTM Results

Extensive hyperparameter tuning was performed using different hidden dimensions, numbers of recurrent layers, dropout values, and random seeds.

The strongest BiLSTM configuration achieved:

* Approximately 86.77% Test Accuracy
* Approximately 87.90% Validation Accuracy
* Controlled overfitting with a relatively small train-validation gap

Reducing network depth proved more beneficial than increasing model complexity.

---

## BiGRU Results

Multiple BiGRU configurations were evaluated using different hidden sizes, dropout values, learning rates, weight decay values, and random seeds.

The best-performing configuration achieved:

* Approximately 88.25% Test Accuracy
* Approximately 86.95% Validation Accuracy
* Approximately 87.66% Macro F1-Score

The experiments demonstrated stable generalization while maintaining controlled overfitting.

---

## Discussion

The comparative study showed that maintaining a consistent preprocessing pipeline enabled a fair evaluation of different temporal architectures.

Among all evaluated models, the TCN architecture achieved the strongest overall performance and demonstrated superior generalization on the refined landmark dataset.

The meeting also highlighted the importance of carefully designing landmark-level augmentation, as inappropriate augmentation strategies can negatively influence model learning.

---

## Decisions Taken

* Continue using the corrected preprocessing pipeline.
* Adopt the improved augmentation strategy for future experiments.
* Continue development using the TCN architecture as the primary model.
* Use the remaining architectures as baseline comparisons.

---

## Action Items

* Finalize the TCN architecture.
* Perform additional validation experiments.
* Prepare the final comparative analysis.
* Begin integrating the experimental findings into the research paper.
