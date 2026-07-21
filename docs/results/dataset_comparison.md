# Dataset Comparison

## Objective

To compare model performance using the original dataset and the refined dataset after reducing the impact of class imbalance.

---

## Performance Comparison

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

The refined dataset produced more stable validation performance and improved evaluation metrics.

Reducing extremely low-sample classes improved model generalization while reducing the severity of overfitting.

---

## Conclusion

Based on these findings, subsequent experiments focused on the 128-class dataset before exploring additional architectural improvements.
