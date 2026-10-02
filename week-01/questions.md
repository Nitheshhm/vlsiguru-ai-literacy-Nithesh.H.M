# Week 01 — Foundational Questions

## Q1. AI → ML → Deep Learning → Generative AI → Agents

### A — Answer

**1. Artificial Intelligence (AI)**
AI is the broad field of making computer systems perform tasks that normally require human-like abilities, such as understanding language, recognizing objects, solving problems, and making decisions.

**Everyday example:** A voice assistant that understands a spoken request.

**2. Machine Learning (ML)**
ML is a subset of AI in which a computer learns patterns from example data and uses them to make predictions or decisions, rather than relying only on manually written rules.

**Everyday example:** A music app recommending songs based on listening history.

**3. Deep Learning (DL)**
DL is a subset of ML that uses neural networks with multiple layers to learn complex patterns from data.

**Everyday example:** A phone recognizing faces in photos.

**4. Generative AI (GenAI)**
Generative AI creates new content, such as text, images, audio, or code, based on patterns learned during training.

**Everyday example:** An AI assistant drafting an email from a prompt.

**5. AI Agent**
An AI agent is a system that works toward a goal by processing information, selecting steps, and taking actions. Depending on its design, it may use an AI model, tools, memory, and feedback to complete a multi-step task.

**Everyday example:** A travel-planning agent that searches for suitable flights, compares options, and prepares an itinerary. Booking or payment may still require user approval.

### Concept map

```text
Artificial Intelligence (AI)
└── Machine Learning (ML)
    └── Deep Learning (DL)
        └── Many modern Generative AI models

AI Agent = a goal-directed system/workflow
           that may use a generative model or other AI
           + tools + planning/control + feedback
```

This is a simplified map, not a rule that every AI agent must use deep learning or generative AI. Agents are better understood as systems or workflows, not simply another level in the hierarchy.

### Relationship between a generative model and an agent

A generative model produces content in response to an input, such as an answer, summary, image, or code. By itself, generating a response does not necessarily mean it can carry out a complete task. An agent can use a generative model as one component, then plan steps, call tools, inspect results, and decide what to do next. For example, a model can draft a travel itinerary, while an agent could search for flight information and organize the results. Actions with real-world consequences, such as purchasing a ticket, may need human approval.

### E — Evidence

**Source 1 — IBM:** *What Is Artificial Intelligence (AI)?*
https://www.ibm.com/think/topics/artificial-intelligence

Relevant sections to review: Machine learning, Deep learning, and Generative AI. IBM explains how these concepts relate and describes generative AI as creating content.

**Source 2 — Google Cloud:** *Generative AI glossary*
https://docs.cloud.google.com/docs/generative-ai/glossary

Relevant section to review: AI agents. Google Cloud describes agents as applications that process input, reason using available tools, and take actions toward a goal.

**Source 3 — Google Cloud:** *What are AI agents? Definition, examples, and types*
https://cloud.google.com/discover/what-are-ai-agents

Relevant sections to review: Key features of an AI agent and How do AI agents work?

### V — Verification

**Status: Complete this after checking the sources.**

- [ ] I checked IBM's definitions of AI, ML, DL, and GenAI.
- [ ] I checked Google Cloud's explanation of AI agents and tool use.
- [ ] I confirmed that ML is a subset of AI and DL is a subset of ML.
- [ ] I confirmed that generative models create content and that agents can use models and tools to perform multi-step tasks.

**Verification note:** After reading the sources, record one specific fact you confirmed and any limitation or difference you noticed. Do not mark a claim verified unless you checked it.

### R — Reflection

I learned that AI is the broad field, while machine learning is one approach within AI and deep learning is one approach within machine learning. Generative AI focuses on creating content, whereas an AI agent is a goal-directed system that may use a generative model along with tools and a workflow. The categories are related but are not interchangeable. I should identify what a system actually does instead of assuming that every AI tool is an agent.


## Q2. Is everything that looks intelligent actually AI?

### A — Answer

| Scenario | Classification | Reason |
|---|---|---|
| A. A calculator produces 25 × 16 = 400. | Deterministic/traditional software (not AI) | It follows a fixed arithmetic procedure to calculate the result. It does not need to learn from data. |
| B. A rule-based program says: If temperature > 80°C, display WARNING. | Deterministic/traditional software (not AI) | A programmer explicitly defined the condition and action. The same input produces the same output. |
| C. An email system identifies spam based on patterns learned from previous email data. | Machine-learning-based AI | The system learns patterns from example emails and uses them to classify new messages as spam or not spam. |
| D. An AI assistant writes a summary of a document. | Generative AI | The model generates new text that expresses the document's main ideas in a shorter form. |
| E. A navigation application predicts estimated arrival time using traffic and historical data. | Machine-learning-based AI | It can use current traffic and historical patterns to predict travel time. The navigation application may also use traditional algorithms for routing. |

### Reasoning

**A — Calculator:** The calculator follows mathematical rules to produce an exact result. Looking intelligent does not make it AI; it performs a predefined computation.

**B — Rule-based program:** The program checks whether the temperature exceeds 80°C and displays a warning if the condition is true. The behavior is explicitly programmed rather than learned from data.

**C — Spam detection:** The system learns statistical patterns from previously labelled emails and applies them to new messages. This is machine-learning-based AI because learning from data is involved.

**D — Document summary:** The assistant generates a new, shorter piece of text based on the document. This is generative AI because it produces content rather than simply applying a fixed rule.

**E — Arrival-time prediction:** The application uses traffic information and historical data to estimate how long a journey will take. A learned prediction model makes this machine-learning-based AI, although other parts of the navigation system may use traditional software.

### Final explanation

An AI system differs from a program that simply follows explicit instructions in how it produces its results. Traditional software follows predefined rules and procedures, while machine-learning systems use patterns learned from data to make predictions or classifications. Generative AI produces new content based on learned patterns. However, AI systems still run on programmed software, and many practical applications combine learned models with traditional rules and algorithms. Therefore, not every feature that appears intelligent is necessarily AI.

### R — Reflection

I learned that automation and AI are not the same thing. A fixed rule or calculation can be useful without learning from data. I should look at how a system produces its result before classifying it as AI.

## Q3. What happens when you ask an LLM a question?

### A — Answer

When a user submits a prompt, the language model processes the input along with relevant conversation context. The text is split into tokens, which are converted into numerical representations. The model processes these representations using learned patterns and relationships between tokens. It calculates a probability distribution over possible next tokens, selects one, and adds it to the generated sequence. This process repeats until the response is complete or a stopping condition is reached.

### Key terms

- **Prompt:** The input or instruction given to the model, including any relevant context.
- **Token:** A piece of text processed by the model. It may be a whole word, part of a word, punctuation, or another text unit.
- **Context:** The information available to the model for the current response, such as the prompt and relevant conversation history, within its context limit.
- **Probability:** A numerical value representing how likely a possible next token is according to the model's current prediction.
- **Next-token prediction:** The process of estimating a probability distribution over possible next tokens, given the tokens already available.
- **Generated response:** The text produced by repeatedly selecting tokens and converting the resulting sequence back into readable text.

### Training vs inference

**Training** is when the model learns patterns by adjusting its internal parameters using training data. **Inference** is when the already-trained model processes a prompt and generates an output. In ordinary inference, the model's learned parameters are not updated for every question asked.

### B — Flow diagram

```text
User submits a prompt
          ↓
Text is split into tokens
          ↓
Tokens + available context
          ↓
Model processes the input
(using learned patterns and attention)
          ↓
Probability distribution over next tokens
          ↓
Select one next token
          ↓
Append token to the sequence
          ↓
More text needed?
     ↙ Yes       No ↘
Process again    Generated response
```

### Why fluent text can still be false

An LLM is trained to generate plausible continuations based on learned patterns; fluency does not guarantee that a statement is factually correct. If its learned patterns or available context do not support the correct answer, it may generate an incorrect claim or invent details. A model can therefore produce confident-sounding text without reliable evidence. Important factual claims should be checked against trustworthy sources.

### E — Evidence

**Source 1 — Microsoft Learn:** *LLM Fundamentals*
https://learn.microsoft.com/en-us/agent-framework/journey/llm-fundamentals

Relevant sections: What is an LLM?, How LLMs are trained, and How inference works. The article explains tokens, next-token prediction, and the inference process.

**Source 2 — University of Massachusetts Chan Medical School:** *How language models actually work*
https://biocore.umassmed.edu/next-token/

Relevant sections: The vocabulary and the explanation of next-token prediction. This educational resource explains tokens, probability distributions, training, inference, and why fluent output can be wrong.

### V — Verification

**Status: Complete after checking the sources.**

- [ ] I checked Microsoft's explanation of tokens and inference.
- [ ] I checked the educational source's explanation of next-token prediction.
- [ ] I confirmed that training adjusts model parameters, whereas inference uses a trained model to generate a response.
- [ ] I confirmed that fluent output is not a guarantee of factual accuracy.

**Verification note:** After reading the sources, record one fact you confirmed and any limitation or difference you noticed. Do not mark claims as verified until you have checked them.

### R — Reflection

I learned that an LLM generates text step by step by predicting the next token using the prompt and available context. Training teaches the model patterns, while inference uses those learned patterns to generate a response. Since the model predicts plausible text rather than guaranteeing truth, I should verify important claims using reliable sources.

## Q4. Hallucination experiment

### A — Answer and observations

### E — Evidence

### V — Verification

### R — Reflection

## Q5. AI vs Search vs Authoritative Reference

### A — Answer and comparison

### E — Evidence

### V — Verification

### R — Reflection

## Q6. What is an AI Agent?

### A — Answer

### E — Evidence

### V — Verification

### R — Reflection

## Q7. Where should humans still make the decision?

### A — Answer

### E — Evidence

### V — Verification

### R — Reflection

## Q8. Find AI around you

### A — Answer and examples

### E — Evidence

### V — Verification

### R — Reflection

## Q9. Prediction vs Classification vs Generation

### A — Answer

### E — Evidence

### V — Verification

### R — Reflection

## Q10. Personal AI verification protocol

### A — Answer

### E — Evidence

### V — Verification

### R — Reflection
