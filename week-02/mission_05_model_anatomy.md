# Mission 5 — Understand an ML Model's Anatomy

## Research Question
What is the difference between an algorithm, a model, training, and inference?

## 1. Algorithm vs. Model
**Algorithm:** An algorithm is a procedure or method used to learn patterns from data. During training, a learning algorithm adjusts model parameters to reduce errors according to a chosen objective.

**Model:** A model is the learned result of training. It contains parameters that can be used to make predictions on new inputs.

**Example:** Linear regression is a learning method. After it is trained on data, the resulting model has learned coefficients and an intercept that can be used to predict a numerical value.

## 2. Training vs. Inference
**Training:** Training is the process of using data and a learning algorithm to fit a model's parameters.

**Inference:** Inference is the process of applying a trained model to new input data to produce a prediction.

**Example:**
- During training, a model learns relationships between design characteristics and measured delay from historical design runs.
- During inference, the trained model receives the available characteristics of a new design run and estimates its delay.

## 3. Labelled ML Workflow
```text
Raw Data
   |
   v
Data Preparation
   |
   v
Training Data
   |
   v
Learning Algorithm
   |
   v
Trained Model
   |
   v
New Input Data
   |
   v
Inference
   |
   v
Prediction
   |
   v
Evaluation and Engineering Review
```

**Explanation:**
1. **Raw data:** Collect relevant examples and measurements.
2. **Data preparation:** Check data quality, handle missing values where appropriate, and prepare features.
3. **Training data:** Use suitable examples to fit the model.
4. **Learning algorithm:** Adjust the model parameters according to the learning objective.
5. **Trained model:** Retain the learned parameters for later use.
6. **New input data:** Provide inputs that were not used to fit the model.
7. **Inference:** Apply the trained model to those inputs.
8. **Prediction:** Produce the estimated value or class.
9. **Evaluation and engineering review:** Compare predictions with appropriate evidence and assess whether the model is useful and reliable.

Validation and test data should be kept separate from training data for their intended evaluation roles.

## 4. Linear Regression Example
Linear regression is a supervised learning method used to predict a numerical target.

A simple linear regression model can be written as:

\[
$\hat{y} = w_1x_1 + b$
\]

Where:
- \(x_1\) is the input feature.
- \(w_1\) is the learned coefficient or weight.
- \(b\) is the learned intercept.
- \(\hat{y}\) is the predicted value.
  
### Training Example
Suppose we want to estimate design-run delay using a simplified input feature such as cell count.

During training, the algorithm uses historical examples with known cell counts and measured delays to fit the coefficient and intercept.

The fitted model learns a relationship between the input and the numerical target. A real design may require many more features and a more suitable model than this simple example.

### Inference Example
After training, suppose a new design run has a cell count of 15,000. The trained model uses its learned coefficient and intercept to estimate the delay for that input.

The predicted delay is an estimate, not a guaranteed timing result. Actual performance must be checked using appropriate engineering analysis.

## 5. Why This Distinction Matters
- An algorithm describes how a model is fitted.
- A model contains the learned parameters used to make predictions.
- Training fits those parameters using data.
- Inference applies the fitted model to inputs to generate predictions.
- Evaluation determines how well the model performs on suitable data.

Understanding these differences helps prevent confusion between developing a model and using it.

## 6. Connection to VLSI Physical Design
A trained ML model could potentially estimate timing-related metrics from historical design data. During training, it would learn from available examples. During inference, it could estimate a metric for a new design run.

Such predictions could support early investigation and prioritisation. They should not replace sign-off timing analysis or other required engineering checks.

## Conclusion
An ML model is produced through a training process that uses an algorithm and data. Once trained, the model can perform inference on new inputs. Understanding the complete workflow helps engineers interpret predictions and evaluate their limitations.

## Sources
- Google for Developers — Machine Learning Crash Course  
  https://developers.google.com/machine-learning/crash-course

- scikit-learn — Linear Models  
  https://scikit-learn.org/stable/modules/linear_model.html

**Verification note:** Check the relevant source sections to verify the definitions and linear regression explanation. The semiconductor example is illustrative and does not represent measured design data.
