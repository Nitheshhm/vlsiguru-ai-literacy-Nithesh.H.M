# Mission 5 — TensorFlow Playground Experiment

## 1. Objective

The objective was to investigate whether increasing neural network complexity always improves classification performance.

I used TensorFlow Playground to compare a baseline network with two hidden layers against a modified network with three hidden layers.

## 2. Experiment A — Baseline Configuration

- **Problem type:** Classification
- **Dataset:** Circle
- **Hidden layers:** 2
- **Neurons per layer:** 4 and 2
- **Activation function:** Tanh
- **Learning rate:** 0.03
- **Regularization:** None
- **Noise:** 0
- **Training-to-test ratio:** 50%

### Observations

At epoch 1,500, the displayed training loss was 0.000 and the displayed test loss was 0.001. The decision boundary separated the central blue points from the surrounding orange points.

The baseline network learned the Circle classification pattern successfully.

## 3. Experiment B — Modified Configuration

I added one hidden layer while keeping the other settings unchanged.

- **Problem type:** Classification
- **Dataset:** Circle
- **Hidden layers:** 3
- **Neurons per layer:** 4, 2, and 2
- **Activation function:** Tanh
- **Learning rate:** 0.03
- **Regularization:** None
- **Noise:** 0
- **Training-to-test ratio:** 50%

### Observations

At epoch 1,500, the displayed training loss was 0.000 and the displayed test loss was 0.000. The decision boundary separated the central blue points from the surrounding orange points well.

The modified network showed a slightly lower displayed test loss than the baseline in this experiment.

## 4. Comparison

| Measurement | Experiment A | Experiment B |
|---|---:|---:|
| Hidden layers | 2 | 3 |
| Neurons per layer | 4, 2 | 4, 2, 2 |
| Epoch | 1,500 | 1,500 |
| Training loss | 0.000 | 0.000 |
| Test loss | 0.001 | 0.000 |
| Activation function | Tanh | Tanh |
| Learning rate | 0.03 | 0.03 |
| Regularization | None | None |
| Regularization rate | 0 | 0 |
| Noise | 0 | 0 |
| Training-to-test ratio | 50% | 50% |
| Batch size | 10 | 10 |

Both experiments were compared at the same displayed epoch with the same displayed settings, except for the additional hidden layer. The displayed loss values are rounded, so the small difference in test loss does not prove that a deeper network always performs better.

## 5. Answers to the Investigation Questions

### What changed when I modified the network?

I added a third hidden layer containing two neurons. The network became more complex, but the dataset and the other displayed settings remained unchanged.

### Did the more complex network always perform better?

No. In these runs, the baseline displayed a test loss of 0.001, while the modified network displayed a test loss of 0.000. Both learned a good decision boundary. However, the small difference in rounded loss values does not prove that a deeper network always performs better.

### What did I observe about model complexity?

A network with more hidden layers can learn complex patterns, but increasing its size does not guarantee better results. A simpler model can be sufficient when the classification problem is relatively easy.

### Why should training performance not be the only measure of success?

Training loss measures performance on training examples. Test loss provides evidence about performance on separate examples. A model that performs well on training data may still generalise poorly to new data.

### How is this experiment different from semiconductor inspection?

The Playground uses a simple synthetic Circle dataset with two-dimensional points. Real semiconductor inspection involves images, image quality issues, different defect types, and manufacturing variations. Results on the Playground do not establish that the same architecture would work well for semiconductor inspection.

### What additional evidence would be needed for practical use?

A practical application would require representative labelled inspection images, reliable evaluation on unseen data, testing under different inspection conditions, analysis of false positives and false negatives, and engineering review.

## 6. Conclusion

Both network configurations learned the Circle classification pattern at epoch 1,500. The three-hidden-layer network displayed a test loss of 0.000, compared with 0.001 for the two-hidden-layer baseline. Both displayed training losses of 0.000.

The experiment suggests that adding a hidden layer did not produce a large visible change in performance. Because the loss values are rounded, the small difference does not establish that a deeper network is consistently better.

Model complexity should be evaluated using appropriate data, model performance, and the requirements of the problem.

## 7. Evidence

### Experiment A — Baseline
![Baseline experiment](playground_baseline.png)

### Experiment B — Three hidden layers
![Modified experiment](playground_three_hidden_layers.png)
