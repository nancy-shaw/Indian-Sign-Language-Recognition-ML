# Baseline Model Results

## Model

BiLSTM with Attention

---

## Evaluation Metrics

The baseline model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

---

## Observations

The baseline model successfully learned temporal gesture patterns from landmark sequences.

However, during later epochs, training accuracy continued to improve while validation performance saturated, indicating overfitting.

The model demonstrated strong learning capability but limited generalization due to the small number of samples available for each gesture class.

---

## Conclusion

The baseline experiment established a strong reference point for subsequent experiments and highlighted the need for improved regularization, dataset refinement, and alternative temporal architectures.
