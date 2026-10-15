# Mission 3 — Understand the Main ML Approaches

## Research Question

How does a system learn when it has labels, no labels, or feedback from actions?

## 1. Supervised Learning

Supervised learning uses labelled training data. Each training example contains input features and a known target. The model learns a relationship between the inputs and target so it can make predictions on new data.

**Example:** Predicting whether a semiconductor design run will meet its timing target using historical design data with known outcomes.

**Training signal:** Known labels or target values.

**Limitation:** The model depends on suitable, accurate, and representative labelled data.

## 2. Unsupervised Learning

Unsupervised learning works with unlabelled data. It aims to discover patterns, groups, or structure without being given a target label for every example.

**Example:** Grouping semiconductor design runs with similar congestion levels and other characteristics.

**Training signal:** Structure and patterns in the input data, without target labels.

**Limitation:** The discovered groups may not always be meaningful or useful for the engineering problem.

## 3. Reinforcement Learning

Reinforcement learning involves an agent taking actions in an environment and receiving rewards or penalties. The agent learns a policy intended to maximise cumulative reward over time.

**Example:** Learning a strategy for selecting design actions in a simulated environment.

**Training signal:** Rewards or penalties resulting from actions and interactions.

**Limitation:** It may require extensive interaction, careful reward design, and safety controls. A poorly designed reward can encourage undesirable behaviour.

## 4. Comparison Table

| Approach | Training Signal | Main Purpose | Example |
|---|---|---|---|
| Supervised learning | Labelled examples | Predict target values or classes | Predict timing pass/fail |
| Unsupervised learning | Unlabelled data | Discover patterns or groups | Group similar design runs |
| Reinforcement learning | Rewards and penalties | Learn actions or strategies | Optimise design actions in simulation |

## 5. When Is Each Approach Suitable?

- **Supervised learning:** When reliable labelled examples exist and the desired output is known.
- **Unsupervised learning:** When the goal is to explore data and discover structure without predefined labels.
- **Reinforcement learning:** When a problem involves sequential decisions, actions, and feedback from an environment.

## 6. Connection to VLSI Physical Design

These approaches could support different engineering tasks:

- **Supervised learning:** Predicting timing outcomes from historical design-run data.
- **Unsupervised learning:** Grouping design runs according to congestion or other measured characteristics.
- **Reinforcement learning:** Exploring design-action strategies in a simulator.

These are potential applications, not claims that a particular ML system will necessarily improve design results. Each approach must be evaluated using appropriate data, metrics, and engineering constraints.

## Conclusion

Supervised, unsupervised, and reinforcement learning differ mainly in their learning signals and objectives. Selecting an approach depends on the engineering problem, the available data, and how success will be evaluated.

## Sources

- Google for Developers — Machine Learning Crash Course  
  https://developers.google.com/machine-learning/crash-course

- IBM — What Is Machine Learning?  
  https://www.ibm.com/think/topics/machine-learning

**Verification note:** Check the relevant sections of these resources and record which claims they support.
