# Week 2 — AI Engineering Journal
**Name:** Nithesh H. M.  
**Track:** Physical Design (PD)  
**Program:** VLSIGuru AI Literacy Layer  
**Week:** 02

## 1. What I Worked On
This week, I studied the foundations of machine learning and completed nine research missions covering AI and ML concepts, data, learning approaches, ML task types, model anatomy, evaluation, failure modes, and when to use ML.

I also explored how machine learning could support semiconductor Physical Design, particularly predicting whether a design is likely to meet timing.

## 2. Key Concepts Learned
- AI is the broader field, while machine learning learns patterns from data.
- Supervised, unsupervised, and reinforcement learning use different learning approaches.
- Features are the inputs used by a model, while labels represent the target in supervised learning.
- Training builds a model, while inference uses the trained model to produce predictions.
- Accuracy, precision, recall, and confusion matrices help evaluate classification models.
- Poor data quality, overfitting, and data drift can make model predictions unreliable.

## 3. Connection to Physical Design
I explored a hypothetical ML model that predicts whether a semiconductor design will meet timing based on features such as cell count, congestion, utilisation, and clock frequency target.

This helped me understand how ML could support early investigation and prioritisation. However, predictions must be evaluated carefully and cannot replace required timing analysis or engineering sign-off.

## 4. Challenges and Observations
One challenge was distinguishing related concepts, especially algorithm versus model, and training versus inference.

I also learned that accuracy alone may not be sufficient for evaluating a model. False positives and false negatives can have different consequences depending on the engineering problem.

Creating a lifecycle map helped connect problem definition, data preparation, model training, evaluation, inference, and monitoring into one workflow.

## 5. Verification and Responsible AI Use
I referred to educational resources such as Google's Machine Learning Crash Course, IBM's AI and ML explanations, and scikit-learn's linear model documentation.

The semiconductor examples and numerical values used in my assignments are illustrative. They are not results from an actual semiconductor design project.

## 6. Next Steps
I want to practise using Python to explore datasets, prepare features, train a basic ML model, and evaluate its performance on unseen data.

I also want to learn how to apply these concepts responsibly to practical VLSI Physical Design problems.

## Weekly Summary
Week 2 helped me build a foundation in machine learning concepts and understand how data quality, evaluation, and monitoring affect model reliability. I now have a clearer idea of how ML may support Physical Design while recognising its limitations.
