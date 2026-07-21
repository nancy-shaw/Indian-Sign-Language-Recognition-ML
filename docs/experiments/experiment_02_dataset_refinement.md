# Experiment 02: Dataset Refinement and Class Threshold Analysis

## Objective

The objective of this experiment was to investigate the impact of class imbalance on model performance by comparing the original dataset with a refined dataset containing only classes with sufficient training samples.

---

## Motivation

The original dataset contained 260 classes with a highly uneven distribution of samples. Several classes contained very few examples, making it difficult for the model to learn robust decision boundaries.

To reduce the effect of severe class imbalance, a second dataset was created by retaining only classes containing at least 15 samples.

This resulted in a refined dataset of 128 classes.

---

## Experimental Setup

Two datasets were evaluated:

**Dataset 1 (Threshold-5)**

* 260 classes
* Classes with fewer than 5 samples removed

**Dataset 2 (Threshold-15)**

* 128 classes
* Only classes with at least 15 samples retained

The same BiLSTM with Attention architecture and training configuration were used for both datasets to ensure a fair comparison.

---

## Results

| Metric              | Threshold-5 | Threshold-15 |
| ------------------- | ----------: | -----------: |
| Classes             |         260 |          128 |
| Test Accuracy       |      77.83% |       78.67% |
| Precision           |      79.85% |       81.25% |
| Recall              |      77.83% |       78.67% |
| F1 Score            |      76.21% |       77.48% |
| Training Accuracy   |      95.33% |       94.81% |
| Validation Accuracy |      81.44% |       82.40% |
| Overfitting Gap     |      13.88% |       12.41% |

---

## Observations

The refined dataset consistently outperformed the original dataset across the evaluation metrics.

Reducing the number of low-sample classes resulted in:

* Improved validation accuracy
* Higher precision and F1-score
* Reduced overfitting
* Better model generalization

---

## Conclusion

Based on these observations and discussions with the project supervisor, subsequent experiments focused on the 128-class dataset to enable more reliable model development before extending the approach to larger datasets.
