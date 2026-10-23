# Week 3 — AI Tools Exploration

## 1. Objective
The objective of this activity is to explore AI tools for learning and engineering tasks, improve prompts, compare AI-generated answers, and verify important claims using reliable sources.

## 2. AI Tools Explored
| AI Tool | Purpose | Observation |
|---|---|---|
| ChatGPT | Explaining concepts and improving prompts | Useful for structured explanations and step-by-step guidance |
| Claude | Comparing explanations and summarising information | Useful for reviewing longer text and comparing reasoning |

## 3. Prompt Improvement
**Topic:** Understanding machine learning in Physical Design.

**Initial prompt:**

"Explain machine learning."

**Improved prompt:**
"Explain how machine learning could help predict timing problems in VLSI Physical Design. Use beginner-friendly language, provide a simple example, identify possible input features and outputs, and explain the limitations. Do not present hypothetical results as real experimental data."

**Observation:**
The improved prompt gives clearer context, specifies the intended level of detail, and requests a relevant engineering example and limitations.

## 4. Comparing Three AI Tools

**Prompt used for all tools:**

“Explain the difference between supervised learning and unsupervised learning, with one semiconductor engineering example for each. Use beginner-friendly language. For each approach, explain the type of data required, how it learns, and what output it produces. Include one limitation of each approach. Do not invent experimental results, and provide reliable sources for factual claims.”

### Comparison Table

| Factor | ChatGPT | Gemini | Claude |
|---|---|---|---|
| Clarity | Clear, concise comparison table | Detailed explanation with bullet points | Detailed explanation with a quick comparison table |
| Supervised learning example | Predicting whether a design meets timing | Wafer defect classification | Classifying wafer defect patterns |
| Unsupervised learning example | Grouping chip designs by congestion and utilization | Detecting unusual wafer defect patterns | Clustering similar wafer maps |
| Main strength | Easy-to-understand summary | Explains concepts step by step | Gives detailed semiconductor examples |
| Limitation highlighted | Needs reliable labelled data | May struggle with unseen defect types; results need validation | Clusters may be difficult to interpret and validate |
| Verification | Referred to Google's Machine Learning Crash Course | Sources should be checked for relevance and reliability | Listed technical and educational sources that need checking |

### Observations

All three tools correctly explained that supervised learning uses labelled data, while unsupervised learning finds patterns in unlabelled data.

ChatGPT was useful for a short, structured comparison. Gemini provided detailed explanations using wafer inspection examples. Claude gave more detailed examples of wafer-map classification and clustering.

The tools used different semiconductor examples, but all connected machine learning to practical engineering tasks. Their answers should not be treated as experimental evidence. Important claims and cited sources must be verified independently.

### Conclusion

I learned that different AI tools can explain the same topic in different ways. A clear prompt with context, required details, limitations, and source requirements can improve the usefulness of the answers. AI-generated explanations are helpful starting points, but technical claims and sources must be checked before using them in engineering work.

## 5. Verification of an AI-Generated Claim
**Claim checked:** Supervised learning uses labelled examples during training.

**Verification source:** Google for Developers — Machine Learning Crash Course: Supervised Learning  
https://developers.google.com/machine-learning/intro-to-ml/supervised

**Verification method:**
I checked Google's explanation of supervised learning to determine whether training examples contain input features and corresponding labels.

**Finding:**
Google's explanation supports the claim: supervised learning uses labelled examples to learn the relationship between input features and a target label or value.

**Conclusion:**
The claim is supported by the source. However, the quality of a supervised learning model also depends on the quality and representativeness of its training data.

## 6. Responsible AI Use
AI-generated explanations are useful starting points, but important technical claims should be checked against reliable sources. I should review AI-generated content critically and avoid uploading confidential RTL, netlists, timing constraints, or proprietary design data to public AI tools.

## Summary
Prompt clarity, comparison between tools, and independent verification can improve the usefulness and reliability of AI-assisted learning.
