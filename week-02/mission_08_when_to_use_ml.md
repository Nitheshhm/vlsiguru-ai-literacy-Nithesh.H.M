# Mission 8 — When Should We Use Machine Learning?

## Research Question
When should we use machine learning instead of a traditional rule-based approach?

## 1. Rule-Based Systems vs. Machine Learning
A rule-based system follows explicitly programmed rules. A machine learning system learns patterns from data and uses those patterns to make predictions.

Consider the problem of identifying whether a semiconductor design may fail timing.

**Rule-based approach:**
An engineer could define a rule that flags a design when its estimated delay exceeds a specified threshold.

**Machine learning approach:**
A model could learn relationships between historical design characteristics and timing results, then estimate the likelihood of a new design failing timing.

Both approaches can be useful, depending on the problem and available information.

## 2. Comparison Table
| Factor | Rule-Based System | Machine Learning |
|---|---|---|
| Data availability | Can work with limited historical data if rules are known | Usually requires suitable data for training and evaluation |
| How decisions are made | Uses explicitly defined rules | Uses patterns learned from training data |
| Output | Often a fixed decision based on rules | Can produce a prediction, score, category, or ranking |
| Explainability | Rules are generally easy to inspect | Some models are easier to explain than others |
| Maintenance | Rules may need manual updates when conditions change | Models may need retraining and monitoring as data changes |
| Best suited for | Stable problems with clear, known rules | Problems where useful patterns are difficult to express as explicit rules |
| Risks | Rules may miss cases not anticipated by their designers | Models can learn biased or misleading patterns from data |

## 3. When Is a Rule-Based Approach Better?
A rule-based approach may be preferable when:
- The requirements are clear and can be expressed as explicit rules.
- The problem is stable and does not require learning complex patterns.
- Historical training data is unavailable or insufficient.
- Decisions must be easy to inspect and explain.
- A simple solution is more reliable and easier to maintain.

For example, checking whether a measured value exceeds a fixed engineering limit can often be handled with a direct rule.

## 4. When Is Machine Learning Better?
Machine learning may be useful when:
- Sufficient, relevant, and reliable data is available.
- The problem contains patterns that are difficult to capture with manually written rules.
- Predictions can help prioritise work or support decisions.
- The model can be evaluated using suitable metrics and unseen data.
- The benefits justify the costs of development, monitoring, and maintenance.

For example, an ML model might estimate which designs are more likely to experience timing problems based on historical implementation data.

## 5. Decision Checklist
Before choosing machine learning, ask:
1. Can a simple rule solve the problem adequately?
2. Do we have enough relevant and reliable data?
3. Can we define a measurable target or useful output?
4. Can we evaluate performance on unseen data?
5. What are the consequences of false predictions?
6. Can the model be monitored and maintained?
7. Will ML provide enough benefit to justify its complexity?

If a simple rule performs the task reliably, machine learning may not be necessary.

## 6. Connection to VLSI Physical Design
In Physical Design, rule-based checks are useful for explicit constraints and known engineering requirements. Machine learning may complement these checks by identifying patterns in historical design data or estimating potential timing and congestion issues.

For example, a rule can flag a known threshold violation, while an ML model may estimate timing risk from several design characteristics.

The choice depends on the problem, data availability, required reliability, and engineering constraints. ML predictions should support investigation and prioritisation rather than replace required sign-off checks.

## Conclusion
Machine learning is not automatically better than rule-based systems. Rule-based methods are often suitable for clear, stable requirements, while ML can be useful when reliable data contains patterns that are difficult to express manually. The best approach is the simplest one that meets the problem's requirements with acceptable risk.

## Sources
- Google for Developers — Machine Learning Crash Course: https://developers.google.com/machine-learning/crash-course
- IBM — What Is Machine Learning?: https://www.ibm.com/think/topics/machine-learning

Verification note: The Physical Design examples are illustrative. The comparison describes general differences between rule-based systems and machine learning; the best choice depends on the specific engineering problem.
