# Week 04 — Data & Deep Learning Foundations

## Student Information

- **Name:** Nithesh H. M.
- **Track:** Physical Design (PD)

## Week 04 Objectives

- Understand how raw data is prepared for deep learning.
- Compare rule-based systems, traditional machine learning, and deep learning.
- Explain the basic components of a neural network.
- Understand how neural networks learn through prediction, loss, and parameter updates.
- Experiment with neural network configurations and observe their behaviour.
- Evaluate a deep learning application relevant to engineering.

## Missions and Deliverables

### Mission 1 — Data Behind Deep Learning

- [x] Explain numerical image representation, data preparation, labels, data quality, and dataset splitting.
- [x] Create a labelled data-preparation flow diagram.

**File:** [Data Behind Deep Learning](data_behind_deep_learning.md)

### Mission 2 — What Makes Deep Learning Different?

- [x] Compare rule-based systems, traditional machine learning, and deep learning.
- [x] Include examples, advantages, and limitations.

**File:** [ML vs Deep Learning](ml_vs_deep_learning.md)

### Mission 3 — Open the Neural Network

- [x] Explain input layers, hidden layers, output layers, neurons, weights, biases, and activation functions.
- [x] Create a labelled neural network diagram.

**File:** [Neural Network Diagram](neural_network_diagram.png)

**How it works:** A semiconductor inspection image is converted into numerical pixel values and passed to the input layer. Hidden-layer neurons process the values using learned weights, biases, and activation functions to identify patterns. The output layer produces probabilities for classes such as “Defect” and “No defect,” and the class with the highest probability becomes the model's prediction.

A prediction is not proof that a physical defect exists. The result should be verified using reliable inspection methods and engineering judgment. The probabilities in the diagram are illustrative, not results from a trained model.

### Mission 4 — How Does a Neural Network Learn?

- [x] Explain forward propagation, loss, backpropagation, parameter updates, epochs, and generalisation.
- [x] Create a training-process flowchart.

**File:** [How Neural Networks Learn](how_neural_networks_learn.md)

### Mission 5 — Experiment and Observe

- [x] Explore TensorFlow Playground.
- [x] Record the initial and modified configurations.
- [x] Document observations, evidence, and conclusions.

**Experiment report:** [Playground Experiment](playground_experiment.md)

**Evidence screenshots:**
- [Baseline experiment](playground_baseline.png)
- [Three-hidden-layer experiment](playground_three_hidden_layers.png)

### Final Challenge — Engineering Case Study

- [x] Select an engineering problem.
- [x] Describe the inputs, data preparation, labels, and proposed model.
- [x] Explain evaluation methods, possible errors, limitations, and the need for human review.
- [x] Support the case study with at least two reliable sources.

**File:** [Engineering Case Study](engineering_case_study.md)

## References

This document lists the technical resources and research papers consulted to verify concepts related to deep learning, neural networks, model evaluation, and machine learning applications in Physical Design.

[View Sources and References](sources.md)

## Reflection

This reflection summarizes what I learned about data preparation, neural networks, model training, generalisation, and the importance of evaluating models on unseen data.

[Read Week 04 Reflection](reflection.md)

## Engineering Journal

This journal records my Week 04 learning progress, observations from the TensorFlow Playground experiments, challenges encountered, and key takeaways related to applying AI and machine learning in Physical Design.

[Read Week 04 Engineering Journal](../../journal/week-04.md)

## Responsible Use of AI

AI tools may be used to clarify concepts and explore examples. Important technical claims must be checked against reliable sources. The final explanations should reflect my own understanding. Confidential RTL, netlists, timing constraints, and proprietary design data must not be uploaded to public AI services.
