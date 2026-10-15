# Mission 6 — Evaluation and Generalization

## Research Question

How do we know whether a machine learning model performs well on new, unseen data?

## 1. Training, Validation, and Test Sets
| Dataset | Purpose |
|---|---|
| Training set | Used to train the model and learn its parameters. |
| Validation set | Used to compare models and tune hyperparameters. |
| Test set | Used to evaluate the final model on unseen data. |

Keeping these datasets separate helps estimate how well a model generalizes to new data.

## 2. Overfitting and Underfitting
**Overfitting:** A model learns the training data too closely, including noise or accidental patterns. It performs well on training data but poorly on unseen data.

**Underfitting:** A model is too simple or has not learned enough from the data. It performs poorly on both training data and unseen data.

A good model should learn meaningful patterns that generalize to new examples.

## 3. Classification Evaluation Metrics
- **Accuracy:** The proportion of all predictions that are correct.
- **Precision:** Of all positive predictions, the proportion that are actually positive.
- **Recall:** Of all actual positive cases, the proportion correctly identified.
- **False positive (FP):** The model predicts positive when the actual result is negative.
- **False negative (FN):** The model predicts negative when the actual result is positive.

## 4. Confusion Matrix
Consider a hypothetical ML model that predicts whether a semiconductor design will meet timing.

|  | Actual: Meets Timing | Actual: Fails Timing |
|---|---:|---:|
| **Predicted: Meets Timing** | 80 (True Positive) | 10 (False Positive) |
| **Predicted: Fails Timing** | 5 (False Negative) | 5 (True Negative) |

In this example:

- True positives (TP) = 80
- False positives (FP) = 10
- False negatives (FN) = 5
- True negatives (TN) = 5
- Total predictions = 100

### Calculating the Metrics

**Accuracy**
Accuracy = (TP + TN) / Total

= (80 + 5) / 100 = **85%**

**Precision**
Precision = TP / (TP + FP)

= 80 / (80 + 10) = **88.89%**

**Recall**
Recall = TP / (TP + FN)

= 80 / (80 + 5) = **94.12%**

These values are illustrative and do not represent measured semiconductor design results.

## 5. Why Accuracy Alone Can Be Misleading
Accuracy can be misleading when the classes are imbalanced.

For example, suppose 95 out of 100 designs meet timing and only 5 fail. A model that predicts every design will meet timing achieves 95% accuracy, but it identifies none of the timing failures.

In Physical Design, missing a timing failure could lead engineers to overlook a design that needs further investigation. Therefore, recall for the timing-failure class may be particularly important. Precision also matters because too many false alarms can waste engineering time.

The appropriate metric depends on the engineering objective and the cost of different errors.

## 6. Connection to VLSI Physical Design
An ML model could help predict whether a design is likely to meet timing based on features such as cell count, congestion estimates, and historical timing data.

However, evaluation must use data that was not used to train the model. Engineers should also consider false positives and false negatives before relying on predictions.

ML predictions can support early investigation and prioritization, but they must not replace required timing analysis and engineering sign-off.

## Conclusion

Training, validation, and test sets serve different purposes. Overfitting and underfitting affect generalization, while accuracy, precision, and recall provide different views of model performance. In engineering applications, selecting suitable metrics requires understanding the consequences of incorrect predictions.

## Sources
- Google for Developers — Machine Learning Crash Course: https://developers.google.com/machine-learning/crash-course
- Google for Developers — Classification: https://developers.google.com/machine-learning/crash-course/classification

Verification note: The confusion-matrix values are hypothetical examples created for this assignment. The semiconductor application is illustrative.
