# Meeting 05

**Date:** 09 July 2026

## Objective

To present the progress achieved after implementing the recommendations from the previous meeting, compare the performance of multiple deep learning architectures, and discuss the next phase of the research work.

---

## Progress Since the Previous Meeting

Following the recommendations from the previous meeting, the team revisited the complete training pipeline.

During experimentation, it was observed that the initial landmark augmentation strategy was not producing the desired improvements and negatively affected model performance. The augmentation pipeline was therefore redesigned and implemented correctly while keeping the remaining preprocessing pipeline unchanged.

Additional improvements included:

* Incorporation of Layer Normalization.
* Introduction of Label Smoothing.
* Maintaining identical preprocessing across all models for fair comparison.

The common preprocessing pipeline consisted of:

* MediaPipe landmark extraction
* Wrist-relative coordinate normalization
* Scaling
* Coordinate-level data augmentation
* Consistent train-validation-test split

This ensured that every model was trained and evaluated under identical data preparation conditions.

---

## Model Development

The experimentation was divided among different temporal architectures.

* **Nancy Shaw** – Temporal Convolutional Network (TCN)
* **Muskan Sah** – BiGRU + Attention
* **Muskan** – LSTM and BiLSTM + Attention

Each architecture underwent independent hyperparameter tuning while keeping the preprocessing pipeline unchanged.

---

## Experimental Results

The team presented the comparative performance of all investigated architectures.

### Temporal Convolutional Network (TCN)

Multiple TCN configurations were evaluated by varying channel width and dropout.

The best-performing configuration achieved:

* Test Accuracy: **90.86%**
* Test Macro F1-Score: **90.06%**
* Validation Macro F1-Score: **90.11%**

The results demonstrated that reducing channel width negatively affected performance, while increasing dropout improved validation performance but did not consistently improve generalization.

---

### LSTM and BiLSTM

Extensive hyperparameter tuning was performed using different hidden sizes, numbers of recurrent layers, dropout values, and random seeds.

The best-performing BiLSTM configuration achieved:

* Test Accuracy: **86.77%**
* Validation Accuracy: **87.90%**
* Macro Precision: **87.86%**
* Macro F1-Score: **85.40%**

Reducing network depth proved more effective than increasing model complexity for controlling overfitting.

---

### BiGRU

Multiple configurations were evaluated using different hidden sizes, dropout values, learning rates, weight decay values, and random seeds.

The best-performing BiGRU model achieved:

* Test Accuracy: **88.25%**
* Validation Accuracy: **86.95%**
* Macro F1-Score: **87.66%**

The model demonstrated stable performance while maintaining controlled overfitting.

---

## Discussion

The comparative experiments showed that maintaining an identical preprocessing pipeline enabled a fair comparison between different temporal architectures.

Among all evaluated models, the Temporal Convolutional Network (TCN) demonstrated the strongest overall performance and the best generalization on the refined 129-class landmark dataset.

The meeting also emphasized the importance of correctly implementing landmark-level augmentation, as improper augmentation strategies can negatively impact model learning.

---

## Research Paper Guidance

The project supervisor also provided guidance on preparing the research paper in a clear, well-documented, and reproducible manner.

The key recommendations included:

* Present experiments in a systematic and logical sequence.
* Compare models using identical preprocessing and evaluation settings.
* Support conclusions using multiple evaluation metrics rather than accuracy alone.
* Clearly justify architectural choices and hyperparameter decisions.
* Document preprocessing, augmentation, and evaluation procedures to improve reproducibility.
* Organize the paper with well-defined sections covering methodology, experiments, results, and discussion.
* Explain how each experimental finding influenced subsequent research decisions.

---

## Decisions Taken

* Continue with the corrected preprocessing and augmentation pipeline.
* Select the TCN architecture as the primary model for further development.
* Use LSTM, BiLSTM, and BiGRU as comparative baseline models.
* Begin organizing experiments and documentation for inclusion in the research paper.

---

## Action Items

* Finalize the TCN architecture.
* Perform additional validation experiments.
* Complete the comparative analysis of all evaluated models.
* Continue documenting experiments and results in a structured manner.
* Begin drafting the research paper using the documented methodology, experiments, and evaluation results.
