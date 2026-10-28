# Week 04 — AI Engineering Journal

**Date:** Wednesday, 28 October 2026  
**Track:** Physical Design (PD)  
**Topic:** Data & Deep Learning Foundations

## 1. Week 04 Activities

During Week 04, I studied data preparation, machine learning approaches, neural network architecture, and the training process of deep learning models.

The main activities were:

- Studied how images are represented numerically and how data is cleaned, labelled, normalised, and split into training, validation, and test sets.
- Compared rule-based systems, traditional machine learning, and deep learning, including their advantages, limitations, and possible applications.
- Created a neural network diagram using semiconductor inspection as an example to explain input layers, hidden layers, output layers, weights, biases, and activation functions.
- Studied forward propagation, loss calculation, backpropagation, parameter updates, epochs, training, inference, and generalisation.
- Experimented with TensorFlow Playground using the Circle classification dataset and compared two network configurations.
- Prepared an engineering case study proposing machine learning for early timing-violation risk prediction in Physical Design.
- Documented references, observations, and reflections in the Week 04 portfolio.

## 2. TensorFlow Playground Experiment

I compared two configurations at epoch 1,500.

| Setting | Experiment A | Experiment B |
|---|---|---|
| Hidden layers | 2 | 3 |
| Neurons per hidden layer | 4, 2 | 4, 2, 2 |
| Activation function | Tanh | Tanh |
| Learning rate | 0.03 | 0.03 |
| Training loss displayed | 0.000 | 0.000 |
| Test loss displayed | 0.001 | 0.000 |

Both configurations learned the Circle classification pattern in the observed experiment. However, the displayed loss values are rounded. This comparison does not establish that deeper networks always perform better.

**Evidence:** The experiment settings and observations are documented in `week-04/playground_experiment.md`, with screenshots of both configurations.

## 3. Key Technical Learnings

I learned that data quality and reliable labels are fundamental to model training. Incorrect labels, duplicate examples, class imbalance, and unrepresentative data can affect model performance and make evaluation misleading.

I also learned that neural networks use repeated forward passes, loss calculation, backpropagation, and parameter updates during training. Validation data supports model selection, while independent test data helps assess performance after model choices have been made.

Increasing the number of layers does not guarantee better results. Model complexity, data quality, generalisation, computing requirements, and evaluation results all matter.

## 4. Application to Physical Design

For the engineering case study, I proposed investigating a machine learning classifier that predicts timing-violation risk from early-stage Physical Design information.

Potential inputs include estimated slack, logic depth, cell counts, net characteristics, placement density, congestion indicators, and timing constraints. Labels would be generated from reliable later-stage timing-analysis results.

The model would need to be evaluated on unseen design blocks or implementation runs using metrics such as precision, recall, F1 score, false negatives, and false positives.

This is a proposed application, not a model I have trained or experimentally validated. Machine learning predictions would support engineering investigation rather than replace static timing analysis or final signoff verification.

## 5. Responsible and Ethical Use

I documented the limitations of AI-generated explanations and the need to verify technical claims against reliable sources. I also noted that confidential RTL, netlists, timing constraints, and proprietary design data must not be uploaded to public AI services.

For engineering applications, predictions must be assessed critically because false negatives and false positives can have practical consequences.

## 6. Challenges and Improvements

One important challenge was distinguishing what the experiment actually demonstrated from what could be concluded more generally. The small difference in displayed test loss was not sufficient to establish that one architecture would consistently outperform the other.

In future experiments, I would like to examine additional configurations, understand evaluation metrics more deeply, and explore Python-based machine learning workflows.

## 7. Week 04 Reflection

This week improved my understanding of the relationship between data preparation, neural network architecture, training, and evaluation. I learned that choosing a model is only one part of building a reliable machine learning system.

I also explored how machine learning might support Physical Design engineering while recognising that practical usefulness must be demonstrated through appropriate testing and engineering review.

**Overall status:** Week 04 learning activities and portfolio deliverables documented.
