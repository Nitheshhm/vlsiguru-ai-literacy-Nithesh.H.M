# Mission 2 — What Makes Deep Learning Different?

## 1. Introduction
Artificial Intelligence (AI), Machine Learning (ML), and Deep Learning (DL) are related concepts, but they are not the same.

- **Artificial Intelligence (AI):** The broad field of building systems that perform tasks requiring capabilities such as reasoning, planning, perception, or decision-making.
- **Machine Learning (ML):** A subset of AI in which models learn patterns from data instead of relying only on manually written rules.
- **Deep Learning (DL):** A subset of machine learning that uses neural networks with multiple layers to learn complex patterns and representations from data.
- **Neural Network:** A computational model made of interconnected units called neurons or nodes. The connections have learnable weights, and the units may have biases and activation functions.

A rule-based system can be part of an AI application without using machine learning. Traditional ML often uses algorithms such as decision trees or logistic regression, while deep learning commonly uses multilayer neural networks.

## 2. How Are Neural Networks Different?
A traditional ML workflow often requires people to decide which features should be extracted from the input data. For example, an inspection system might use measurements such as defect size, shape, contrast, and edge characteristics.

Deep learning can learn useful representations directly from more complex inputs, such as image pixels, during training. Its layers progressively transform the input into representations that help the model make a prediction.

The network learns by adjusting its parameters to reduce prediction errors on training examples. However, useful learning depends on suitable data, an appropriate model, and reliable evaluation.

## 3. Comparison of the Three Approaches

| Approach | How it works | Advantages | Example | Limitations |
|---|---|---|---|---|
| Rule-based system | A human defines explicit rules and conditions. | Easy to understand, predictable for stable requirements, and straightforward to audit. | Flag an inspection measurement if it exceeds a specified threshold. | May miss unfamiliar patterns and require manual updates when conditions change. |
| Traditional machine learning | An algorithm learns patterns from examples, often using selected or engineered features. | Can work well with structured data and useful features; may require fewer computing resources than deep learning. | Predict defect risk using measurements such as defect size, contrast, and shape. | Performance depends on data quality and feature selection; complex patterns may be difficult to represent using the chosen features. |
| Deep learning | A multilayer neural network learns representations and patterns from training data. | Can learn complex features from images and other unstructured data, reducing the need to manually design every feature. | Classify semiconductor inspection images as defective or non-defective. | May require substantial training data and computing resources, can be difficult to interpret, and may fail on unfamiliar data. |

These are general tendencies, not guarantees. Actual performance depends on the problem, available data, and implementation.

## 4. How Does a Model Learn Useful Patterns?
A machine learning model is trained using examples. In supervised learning, each training example contains input data and a target label or value.

For example, a semiconductor inspection dataset might contain images labelled "Defect" or "No defect."

During training:
1. The model receives an input.
2. It produces a prediction.
3. The prediction is compared with the target answer using a loss function.
4. The learning algorithm updates the model's parameters to reduce the loss.
5. The process repeats over training examples.

The model can then be evaluated on separate data to determine whether it has learned patterns that generalise beyond the examples used for training.

A model does not automatically understand the physical cause of a defect. It learns statistical patterns present in its data, and those patterns may be misleading if the dataset contains errors or biases.

## 5. Why Is Deep Learning Useful for Complex Inputs?

Images, audio, and language can contain complicated patterns that are difficult to describe completely with manually written rules.

For example, two semiconductor inspection images might show the same defect under different lighting conditions or at different orientations. A suitably trained deep learning model may learn visual representations that help identify the defect despite these variations.

Outside semiconductors, a speech-recognition system can use deep learning to map audio signals to words. The model learns patterns in the audio data rather than requiring a separate manually written rule for every possible pronunciation.

Deep learning is not automatically the best option for these tasks. It must be compared with suitable alternatives using representative evaluation data.

## 6. Do More Layers Automatically Make a Model Better?

No. Adding more layers or neurons increases a neural network's capacity to represent complex patterns, but it does not guarantee better predictions.

A more complex network may:
- Learn useful patterns that a simpler network cannot represent.
- Require more training data and computing resources.
- Take longer to train and evaluate.
- Overfit the training data if it learns patterns that do not generalise.
- Become harder to analyse and maintain.

A smaller model may perform just as well or better when the problem is simple or the available dataset is limited.

The correct approach is to compare model configurations using suitable validation data, then evaluate the selected model on an independent test set.

## 7. When Is a Simpler Approach Better?
A rule-based system may be preferable when the requirements are clear, the rules are stable, and decisions need to be easy to trace.

Traditional ML may be appropriate when the dataset is relatively small or structured, and useful features can be calculated reliably.

Deep learning may be worth investigating when inputs are complex, sufficient representative data is available, and simpler methods do not achieve the required performance.

For example, a fixed rule might be sufficient to flag an inspection measurement above an engineering limit. A traditional ML model might predict a defect from several numerical measurements, while deep learning might be evaluated for classifying complex inspection images.

The most complex method is not always the most useful. The choice should be based on evidence, accuracy requirements, cost, interpretability, and the consequences of incorrect predictions.

## 8. Engineering Reflection — Physical Design
In Physical Design (PD), AI and ML could potentially assist with tasks such as predicting timing-violation risk, identifying congestion-prone regions, or analysing implementation reports.

A rule-based approach could flag a report value that violates a known engineering limit. A traditional ML model could predict risk from structured features such as cell counts, utilization, or timing measurements. A deep learning model could be investigated for learning more complex relationships from suitable design-related data.

These are potential applications, not proof that deep learning will outperform existing EDA analysis or optimization methods. The model's predictions would need to be evaluated against reliable reference results and reviewed by engineers. Confidential RTL, netlists, timing constraints, and proprietary design data must not be uploaded to public AI tools.

## 9. Conclusion
Rule-based systems follow explicit human-defined rules, traditional ML learns patterns using a selected representation of data, and deep learning uses multilayer neural networks to learn complex representations.

Deep learning is especially useful to investigate when the data contains complex patterns, but increased model complexity also brings costs and risks. A suitable solution is the simplest approach that meets the engineering requirements and demonstrates reliable performance on unseen data.

## References

1. Google Machine Learning Crash Course — [Course Overview](https://developers.google.com/machine-learning/crash-course/)
2. Google Machine Learning Crash Course — [Neural Networks](https://developers.google.com/machine-learning/crash-course/neural-networks)
3. Google Machine Learning Crash Course — [Classification](https://developers.google.com/machine-learning/crash-course/classification)
4. Google Machine Learning Crash Course — [Overfitting](https://developers.google.com/machine-learning/crash-course/overfitting/overfitting)
