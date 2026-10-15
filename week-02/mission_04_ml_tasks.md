# Mission 4 — Understand ML Task Types

## Research Question

What kinds of problems can machine learning solve?

## 1. Classification

**Definition:** Classification predicts a category or class from input data.

**Input:** Features describing an example.

**Output:** A predicted class or category.

**Example:** Predicting whether a semiconductor design run will meet its timing target.

**Why it fits:** The output belongs to one of two categories: pass or fail.

## 2. Regression

**Definition:** Regression predicts a numerical value.

**Input:** Features related to the quantity being predicted.

**Output:** A continuous numerical value.

**Example:** Predicting the estimated delay of a semiconductor design run.

**Why it fits:** Delay is measured numerically, such as in nanoseconds.

## 3. Clustering

**Definition:** Clustering groups examples based on similarities in their features, without requiring predefined class labels.

**Input:** Feature measurements for multiple examples.

**Output:** Groups or clusters of similar examples.

**Example:** Grouping design runs with similar congestion and cell-count characteristics.

**Why it fits:** The objective is to discover groups of similar runs rather than predict a known target.

## 4. Dimensionality Reduction

**Definition:** Dimensionality reduction represents data using fewer features or dimensions while preserving useful information as much as possible.

**Input:** Data containing many features.

**Output:** A lower-dimensional representation of the data.

**Example:** Reducing hundreds of design metrics to a smaller set of dimensions for visualising patterns among design runs.

**Why it fits:** It helps explore complex data and may make visualisation or subsequent analysis easier.

## 5. Recommendation and Ranking

**Definition:** Recommendation suggests relevant items or options, while ranking orders candidates according to a scoring method or predicted relevance.

**Input:** Candidate items and relevant features, such as preferences, characteristics, or historical outcomes.

**Output:** Recommended items or an ordered list of candidates.

**Example:** Ranking semiconductor design configurations for further investigation based on predicted timing and congestion.

**Why it fits:** The objective is to prioritise candidate options rather than simply assign a category or predict a single numerical value.

## 6. Anomaly Detection

**Definition:** Anomaly detection identifies observations that differ significantly from expected patterns.

**Input:** Measurements or observations describing system behaviour.

**Output:** An anomaly score, flag, or list of unusual observations.

**Example:** Flagging a design run with unusually high congestion or an unexpected increase in delay.

**Why it fits:** The goal is to identify unusual behaviour that may require investigation. Anomaly detection can use statistical or ML methods.

## 7. Real-World Problem Comparison

| Problem | Input | Output | Task Type | Reason |
|---|---|---|---|---|
| Predict whether a design run meets timing | Design metrics and historical measurements | Pass or fail | Classification | The output is a category. |
| Predict chip-design delay | Design characteristics and available measurements | Delay in nanoseconds | Regression | The output is numerical. |
| Group similar design runs | Cell count, congestion, and other metrics | Clusters of runs | Clustering | The goal is to discover similarities. |
| Simplify a dataset with hundreds of metrics | High-dimensional design measurements | Lower-dimensional representation | Dimensionality reduction | The goal is to represent complex data more compactly. |
| Rank design configurations for investigation | Candidate configurations and their characteristics | Ordered list of candidates | Recommendation / ranking | The goal is to prioritise options. |
| Detect an unusual timing result | Historical and current design measurements | Anomaly flag or score | Anomaly detection | The goal is to identify unusual behaviour. |

## 8. How to Choose the Correct Task Type

The task type depends on the engineering question and the required output.

- If the output is a category, consider **classification**.
- If the output is a numerical value, consider **regression**.
- If the goal is to discover groups, consider **clustering**.
- If the data has many features and needs a compact representation, consider **dimensionality reduction**.
- If the goal is to suggest or prioritise options, consider **recommendation or ranking**.
- If the goal is to find unusual observations, consider **anomaly detection**.

The same dataset can support different task types depending on the problem being solved.

## 9. Connection to VLSI Physical Design

Machine-learning task types could support different stages of Physical Design. Classification could predict timing pass/fail, regression could estimate delay, clustering could group similar design runs, and anomaly detection could flag unusual measurements.

These are potential applications. Their practical value depends on reliable data, appropriate evaluation, and engineering validation. ML predictions should not replace required sign-off analysis.

## Conclusion

Machine learning includes several task types, each suited to a different objective. Identifying the required output first helps select an appropriate task and evaluate whether the solution is useful.

## Sources

- Google for Developers — Machine Learning Crash Course  
  https://developers.google.com/machine-learning/crash-course

- IBM — What Is Machine Learning?  
  https://www.ibm.com/think/topics/machine-learning

**Verification note:** Check the relevant source sections and record which claims they support. The semiconductor examples are illustrative applications, not measured engineering results.
