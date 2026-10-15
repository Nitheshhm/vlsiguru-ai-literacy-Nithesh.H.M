# Mission 7 — Failure Modes and Risks

## Research Question
How can a machine learning model fail, and what risks should engineers consider before relying on its predictions?

## 1. Common ML Failure Modes
Machine learning models can fail when the training data is poor, the real-world data changes, or the model is used in situations different from those for which it was developed.

| Failure Mode | Cause | Possible Impact |
|---|---|---|
| Poor data quality | Incorrect values, inconsistent formats, or measurement errors | The model may learn misleading patterns and produce unreliable predictions. |
| Unrepresentative training data | Training examples do not cover the range of real-world conditions | The model may perform poorly on cases it has not seen before. |
| Missing or noisy data | Important features are absent or measurements contain errors | Predictions may become less accurate or unstable. |
| Data drift | The characteristics of new input data change over time | Model performance may decrease after deployment. |
| Incorrect labels | Training examples have wrong target values | The model may learn incorrect relationships. |
| Overfitting | The model learns noise or specific details of the training set | It may perform well on training data but poorly on new data. |
| Lack of human oversight | Predictions are accepted without appropriate review | Incorrect predictions may lead to poor engineering decisions. |

## 2. How Engineers Can Detect These Failures
- **Poor data quality:** Check missing values, duplicates, inconsistent units, and suspicious measurements.
- **Unrepresentative data:** Compare training data with the conditions expected in actual use.
- **Missing or noisy data:** Inspect feature completeness and measurement reliability.
- **Data drift:** Monitor input distributions and model performance over time.
- **Incorrect labels:** Review a sample of labels against trusted measurements or records.
- **Overfitting:** Compare training performance with validation and test performance.
- **Lack of human oversight:** Define review procedures and escalation rules for uncertain or high-impact predictions.

## 3. Semiconductor Physical Design Example
Consider an ML model intended to predict whether a design is likely to meet timing.

The model is trained using historical design data containing cell counts, congestion estimates, and measured timing results.

Several problems could affect its predictions:
1. **Poor data quality:** Timing values may contain measurement or recording errors.
2. **Unrepresentative data:** The training set may contain mostly small designs, while a new design is much larger.
3. **Missing features:** Important characteristics, such as congestion or design constraints, may be unavailable.
4. **Data drift:** Changes in process technology, design libraries, tools, or implementation settings may make historical patterns less reliable.
5. **Incorrect labels:** A design may be incorrectly labelled as meeting timing.
6. **Overfitting:** The model may perform well on historical examples but poorly on new designs.
7. **Lack of oversight:** Engineers may trust a predicted timing result without running the required timing analysis.

These issues can produce misleading predictions and cause engineers to overlook designs that need further investigation.

## 4. Risk Reduction Strategies
- Validate and clean data before training.
- Use representative datasets covering different design conditions.
- Check labels against trusted engineering results.
- Evaluate models on data that was not used for training.
- Monitor performance when tools, libraries, or design conditions change.
- Investigate uncertain predictions and unexpected results.
- Keep qualified engineers involved in decisions that affect design quality.

No single strategy eliminates every failure mode. Risk reduction requires suitable data, careful evaluation, ongoing monitoring, and engineering judgement.

## 5. Why These Risks Matter

An ML prediction is an estimate based on learned patterns, not a guarantee of correctness.

In Physical Design, an incorrect prediction could waste engineering effort or cause a timing problem to receive insufficient attention. The impact depends on the prediction's purpose and how engineers use it.

ML can support early investigation and prioritisation, but it should not replace required timing analysis, verification, or engineering sign-off.

## Conclusion
Machine learning models can fail because of poor data, unrepresentative samples, missing information, incorrect labels, overfitting, changing conditions, and insufficient human oversight. Engineers should identify these risks, evaluate model behaviour, and monitor performance before relying on predictions in real-world workflows.

## Sources
- Google for Developers — Machine Learning Crash Course: https://developers.google.com/machine-learning/crash-course
- Google for Developers — Data Preparation: https://developers.google.com/machine-learning/crash-course/data-preparation

Verification note: The semiconductor Physical Design scenario is illustrative. The listed failure modes describe general ML risks and are not measurements from an actual design project.
