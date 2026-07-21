# Meeting 04

**Date:** 24 June 2026

## Objective

To discuss the overfitting observed in the baseline BiLSTM model, analyze the limitations of the current dataset, and identify possible strategies to improve model generalization.

---

## Discussion

The current model architecture, training behavior, and dataset characteristics were reviewed with the project supervisor.

Key observations included:

* The project uses the PyTorch framework.
* The baseline model consists of a BiLSTM with an attention mechanism.
* A dropout rate of 0.6 was being used for regularization.
* The input consists of 30-frame sequences of wrist-relative normalized MediaPipe hand landmark coordinates.
* The problem was identified as a time-series classification task.

During training, the model showed clear signs of overfitting. Training loss continued to decrease while validation loss plateaued after several epochs, indicating limited generalization.

The supervisor noted that the dataset contains a large number of classes with relatively few samples per class, making the task similar to a few-shot learning problem. This increases the likelihood of overfitting when using high-capacity recurrent models.

---

## Recommendations

The following improvements were suggested:

* Apply coordinate-level data augmentation, including temporal jittering, scale perturbation, and spatial rotation.
* Investigate ArcFace Loss to improve feature separation between gesture classes.
* Introduce Layer Normalization to improve training stability.
* Reduce model capacity where appropriate.
* Explore Temporal Convolutional Networks (TCNs) as an alternative to BiLSTM architectures for sequence modeling.

The supervisor also recommended focusing on the subset of 128 classes, which have a more balanced number of samples, before attempting to scale the model to all 260 classes.

---

## Decisions Taken

Following the discussion, the project team decided to:

* Continue experiments using the 128-class dataset.
* Re-evaluate the existing BiLSTM model with the suggested improvements where feasible.
* Explore alternative temporal architectures, particularly TCNs.
* Compare future models using accuracy, precision, recall, and F1-score.

---

## Action Items

* Perform additional experiments to reduce overfitting.
* Investigate TCN-based architectures.
* Evaluate different regularization and augmentation strategies.
* Compare the optimized models with the baseline BiLSTM model.
