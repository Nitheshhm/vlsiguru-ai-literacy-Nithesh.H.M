# Mission 2 — Understand Data

**Name:** Nithesh H. M.  
**Track:** Physical Design (PD)  
**Week:** 02 — Machine Learning Foundations

## Research Question

What does an ML system learn from?

## 1. Important Data Concepts

| Term | Explanation | Example |
|---|---|---|
| Dataset | A collection of examples used for analysis or model development | Data from multiple chip-design runs |
| Sample / Observation | One individual example in a dataset | One design run |
| Feature | An input variable used by a model | Cell count or estimated delay |
| Label / Target | The outcome a supervised model learns to predict | Whether a design meets timing |
| Structured data | Data organised in a defined format, such as rows and columns | A CSV file containing design measurements |
| Unstructured data | Data such as free-form text, images, or audio that does not naturally fit a simple table | An image of a chip layout |
| Training data | Data used to fit a model | Historical design runs used for learning |
| Validation data | Data used to compare models or tune settings | A separate set of design runs used during development |
| Test data | Data reserved for final evaluation | Unseen design runs used to assess model performance |

## 2. Example Dataset

**Problem:** Predict whether a simplified semiconductor design run meets its timing target.

The following dataset is fictional and illustrative. It is not measured semiconductor engineering data.

| Run | Cell Count | Estimated Delay (ns) | Congestion Level | Meets Timing |
|---|---:|---:|---|---|
| R1 | 12000 | 0.82 | Low | Yes |
| R2 | 18000 | 1.15 | Medium | No |
| R3 | 9500 | 0.76 | Low | Yes |
| R4 | 22000 | 1.30 | High | No |
| R5 | 15000 | 0.91 | Medium | Yes |
| R6 | 20000 | 1.22 | High | No |

## 3. Identify the Dataset Components

- **Number of samples:** 6 design runs.
- **Features:** Cell Count, Estimated Delay, and Congestion Level.
- **Target / Label:** Meets Timing.
- **Numerical features:** Cell Count and Estimated Delay.
- **Categorical feature:** Congestion Level.
- **Target type:** Binary classification because the outcome has two possible classes: Yes and No.

## 4. Why Are Training, Validation, and Test Data Different?

- **Training data:** Used by the learning algorithm to fit the model.
- **Validation data:** Used during development to compare models and tune settings.
- **Test data:** Used at the end to estimate how well the selected model performs on unseen examples.

Keeping these roles separate helps reduce overly optimistic evaluation. If information from the test set influences model development, the final evaluation may no longer be a fair estimate of performance on unseen data.

## 5. Why Does Data Quality Matter?

Data quality strongly affects the reliability of an ML system.

- **Missing values:** Important measurements may be unavailable.
- **Incorrect labels:** A model may learn from wrong outcomes.
- **Inconsistent units:** Mixing nanoseconds and picoseconds without conversion can cause errors.
- **Unrepresentative data:** The training data may not reflect the conditions encountered in real use.
- **Duplicate records:** Repeated examples can distort the learning process or evaluation.
- **Data leakage:** Information unavailable at prediction time may accidentally enter training data, making results look better than they really are.

For semiconductor engineering, data should be collected consistently across design runs, tools, configurations, and measurement conditions.

## 6. Connection to VLSI Physical Design

A potential application is predicting whether a design run will meet a timing target.

The model could use design characteristics and measurements as features and a timing outcome as its target. Before using such a model, the engineer must confirm that the measurements are reliable, the target is correctly labelled, and the dataset represents the designs on which the model will be used.

This prediction would support engineering decisions; it would not replace sign-off timing analysis.

## Conclusion

An ML system learns from the examples and learning signals provided during development. Understanding samples, features, targets, data splits, and data quality is essential before selecting or training a model.

## Sources

- IBM — What Is Machine Learning?  
  https://www.ibm.com/think/topics/machine-learning

- Google for Developers — Machine Learning Crash Course  
  https://developers.google.com/machine-learning/crash-course

**Verification note:** Consult the relevant sections of these resources and record which claims they support. The dataset above is illustrative, not evidence of actual chip-design results.
