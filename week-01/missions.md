# Mission 1 — Find AI Around You

## Three Everyday Systems

| System / Feature | What I Think It Does | Category |
|---|---|---|
| YouTube recommendations | Suggests videos based on my viewing activity and interests. | Recommendation |
| Phone face unlock | Checks whether the face matches the authorised user. | Recognition / classification |
| Email spam filter | Identifies unwanted or suspicious emails and separates them from normal messages. | Classification |

## Evidence and Verification

**Chosen example: Email spam filter**
I chose the email spam filter to investigate whether AI/ML is actually involved. Spam filters can use machine-learning techniques to identify patterns associated with unwanted messages. I should verify this using documentation from the email provider I actually use.

**Verification source:** [Google Gmail — How Gmail handles spam](https://support.google.com/mail/answer/1366858)

## Could Rules Alone Produce Similar Behaviour?
Yes, a rule-based program could detect some spam using fixed conditions, such as blocking messages from a particular address or flagging specific words. However, spam changes frequently, and machine-learning methods can identify more complex patterns. Rules may still be used alongside machine learning.

## Conclusion
AI-powered features are present in everyday systems. Recommendations, face verification, and spam filtering perform different tasks. I learned that a system appearing intelligent does not automatically prove that it uses AI, so I need reliable evidence before making that claim. 

# Mission 2 — AI, ML, GenAI: Put the Pieces Together

## 1. Explanation of the Terms

| Term | Explanation in My Own Words | Example |
|---|---|---|
| Artificial Intelligence (AI) | AI is the broad field of creating computer systems that perform tasks that normally require human-like intelligence. | A system that helps plan a route. |
| Machine Learning (ML) | ML is a part of AI in which computers learn patterns from data instead of relying only on explicitly written rules. | An email spam filter that learns patterns from examples. |
| Deep Learning (DL) | DL is a type of machine learning that uses neural networks with many layers to learn complex patterns. | A neural network that recognises objects in images. |
| Generative AI (GenAI) | GenAI is AI that creates new content, such as text, images, audio, or code. | An AI assistant generating a summary of a document. |

## 2. Relationship Diagram
```text
Artificial Intelligence (AI)
└── Machine Learning (ML)
    └── Deep Learning (DL)

Generative AI (GenAI)
└── Creates new content and commonly uses deep-learning models
```
**Note:** AI is the broad field, ML is a subset of AI, and DL is a subset of ML. Generative AI describes systems that create new content and commonly uses deep learning, but the terms represent different concepts.

## 3. AI Assistant Review
I asked an AI assistant to review the diagram and explanations. The main relationship—ML as a part of AI and DL as a part of ML—is correct. I also noted that generative AI is not strictly a subset of deep learning in every possible case, so the diagram is a simplified view of common modern AI systems.

## 4. Conclusion
I learned that AI is the broad field, machine learning allows systems to learn patterns from data, deep learning uses multilayer neural networks, and generative AI creates new content. These terms are related, but they do not all mean the same thing.

# Mission 3 — Is It Really AI?

## 1. Classification of Systems

| System | Classification | Reason |
|---|---|---|
| Calculator | Rule-based / traditional software | It follows programmed arithmetic operations to calculate results. |
| Temperature warning rule | Rule-based / traditional software | It compares the temperature with a fixed threshold and triggers a warning. |
| Spam filter | ML-based AI | It can learn patterns from examples to identify unwanted emails. |
| Document summariser | Generative AI | It generates a shorter version of a document while preserving important information. |
| Traffic ETA prediction | ML-based AI | It can use historical and current traffic data to predict travel time. |

## 2. One Easy Classification
**Calculator:** This was easy to classify because a basic calculator follows explicitly programmed mathematical operations. It does not need to learn from examples to perform ordinary calculations.

## 3. One Difficult Classification
**Traffic ETA prediction:** This was more difficult because not every ETA system necessarily uses AI. A simple system could estimate travel time using distance and a fixed speed. A more advanced system may use machine learning and live traffic data to improve predictions.

## 4. My Own Example
**Example: YouTube video recommendations**
I classify this as recommendation-based AI when the recommendations use machine-learning models to estimate which videos a user may find interesting. The system uses signals such as viewing activity and interactions to personalise suggestions.

## Conclusion
I learned that a system is not automatically AI just because it performs a useful or intelligent-looking task. Simple rule-based software can solve many problems, while machine learning can identify patterns from data. Understanding how a system works is important before classifying it as AI.

# Mission 4 — Make AI Explain Itself, Then Test It

## 1. Questions Asked

**Question 1:** Explain how a Large Language Model (LLM) produces an answer to my prompt.

**Question 2:** Now explain it to me as a beginner using a simple example.

## 2. My Final Explanation
A Large Language Model (LLM) is an AI model trained on large amounts of data to learn patterns in language. When I enter a prompt, the text is processed into smaller units called tokens. The model uses the context and patterns it learned during training to predict and generate the next token. It repeats this process until it produces a complete response or reaches a stopping condition.
For example, if I enter “The sun rises in the…”, the model may predict “east” as a likely next word. It continues generating tokens based on the prompt and the text already produced. This is how an LLM can generate explanations, summaries, and other text.

## 3. Verification of Important Claims

**Claim 1:** LLMs process text as tokens.
**Verification:** OpenAI's documentation explains that text is divided into tokens before being processed by a model.
**Source:** [OpenAI — Understanding and counting tokens](https://help.openai.com/en/articles/4936856-understanding-and-counting-tokens)
**Result:** Verified.

**Claim 2:** LLMs generate text by predicting the next token repeatedly.
**Verification:** OpenAI's explanation of ChatGPT's development describes how models learn patterns from training data and use them to predict the next word or token when generating a response.
**Source:** [OpenAI — How ChatGPT and our foundation models are developed](https://help.openai.com/en/articles/7842364-how-chatgpt-and-our-foundation-models-are-developed)
**Result:** Verified.

## 4. What AI Explained Well
The AI explained the basic process of tokenisation and next-token prediction in an understandable way. The simple sentence example helped me understand how a response is generated step by step.

## 5. What I Clarified or Corrected
I clarified that an LLM generally generates a response using patterns learned during training and the context of the current prompt, rather than simply retrieving a complete answer from a database. However, models can sometimes reproduce memorized text, and their generated answers can contain errors. Therefore, important claims should be checked independently.

## 6. Conclusion
I learned that an LLM generates text incrementally using tokens and patterns learned during training. Its response can sound convincing without necessarily being correct, so understanding the process and verifying important claims are both necessary.

# Mission 5 — Verify an AI Answer

## 1. Question Asked
**Question:** What is the difference between RAM and storage in a computer?

## 2. AI Answer
RAM is temporary memory used by a computer to hold data and programs that are currently in use. Storage, such as an SSD or HDD, keeps files, applications, and the operating system even when the computer is turned off. RAM is generally faster than storage, but storage usually provides much more capacity.

## 3. Verification
**Verification result:** The source confirms that RAM is working memory used while programs are running, while SSDs and HDDs provide storage that retains data when the computer is powered off. The main distinction in the AI answer is accurate.

## 4. What I Learned
I learned that an AI-generated answer should not be accepted without checking it. Comparing the answer with a reliable source helped me confirm whether the information was accurate.

## 5. Lesson
AI can provide a useful starting point, but independent verification is important. I should check important facts using reliable sources before relying on them or including them in my work.

# Mission 6 — Understanding AI Systems and Agents

## 1. Important Concepts

| Concept | Explanation | Example |
|---|---|---|
| Large Language Model (LLM) | An AI model trained to understand and generate language by learning patterns from text and other data. | ChatGPT generating an explanation. |
| AI Application | Software that uses an AI model to perform a useful task for a user. | An AI chatbot that answers questions. |
| Retrieval-Augmented Generation (RAG) | A method that retrieves relevant information from external sources and provides it to an AI model to help generate a grounded answer. | A chatbot answering questions using uploaded PDFs. |
| Tool-Using Assistant | An AI assistant that can use external tools to perform tasks or obtain information. | An assistant using a calculator to solve a calculation. |
| AI Agent | An AI system that can work toward a goal by selecting actions, using tools, and responding to results, sometimes across multiple steps. | An assistant that searches for information, compares options, and prepares a plan. |

## 2. System Diagram
```text
User
  |
  v
AI Application
  |
  v
LLM / AI Model
  |
  v
Tool or Retrieval System
  |
  v
Result returned to the model
  |
  v
Response or Action
  |
  v
User
```
**Explanation:** The user provides a request through an AI application. The application sends relevant input to the model. When needed, the system retrieves information or uses a tool. The result can be sent back to the model to help produce a response or guide an action.

Not every AI application uses retrieval or tools. A basic chatbot may generate a response directly from the user's prompt.

## 3. Everyday Example of an Agentic Workflow

**Task:** Plan a weekend trip within a budget.

1. The user asks the AI system to plan a weekend trip within a specified budget.
2. The system identifies the destination, dates, and budget requirements.
3. It searches for travel options and accommodation using available tools.
4. It compares the retrieved results against the user's requirements.
5. It prepares an itinerary and estimated budget.
6. The user reviews the plan and decides whether to proceed with bookings.

This is an example of an agentic workflow because the system can carry out several connected steps toward a goal using tools and the results it receives. Any booking or payment should require the appropriate user approval.

## 4. What I Learned
I learned that an LLM is only one component of a larger AI system. An AI application provides the user interface, RAG supplies relevant external information, and tools allow a system to perform operations beyond generating text.
An AI agent can coordinate multiple steps toward a goal. However, not every chatbot is an agent, and not every AI system needs tools or retrieval.

## 5. Conclusion
Understanding the difference between a model, an application, RAG, tool use, and an AI agent helps me understand how practical AI systems are designed. This mission helped me see that useful AI systems can combine models, information sources, and tools to complete tasks.

# Mission 7 — AI Hardware and Compute

## 1. Important Concepts
| Concept | Explanation | Example |
|---|---|---|
| CPU (Central Processing Unit) | A general-purpose processor that executes instructions and manages many system tasks. | Running an operating system and coordinating program execution. |
| GPU (Graphics Processing Unit) | A processor designed to perform many operations in parallel, making it useful for graphics and AI workloads. | Training a deep-learning model using many parallel calculations. |
| NPU / AI Accelerator | Specialised hardware designed to accelerate certain AI computations efficiently. | An NPU performing AI tasks on a laptop or smartphone. |
| Parallel Computation | Performing multiple calculations at the same time rather than executing every calculation sequentially. | A GPU processing many matrix operations in parallel. |
| Compute and Memory | Compute refers to processing operations, while memory stores the data and model parameters needed for those operations. | An AI model needs both processing power and memory to run efficiently. |
| Training vs Inference | Training adjusts a model's parameters using data; inference uses a trained model to produce predictions or responses. | Training a model on examples versus using it to classify a new image. |

## 2. Hardware and Software Diagram
```text
AI Application
      |
      v
AI Model
      |
      v
Software / Framework
      |
      v
CPU / GPU / AI Accelerator
      |
      v
Memory
```
**Explanation:** The AI application uses a model, while software and frameworks help execute the model's operations. The CPU, GPU, or specialised accelerator performs the computations and uses memory to access model parameters and other data. The exact arrangement depends on the system and workload.

## 3. Real-World Workload Example
**Workload:** Running an image-recognition model.

- **AI application:** A photo app that identifies objects in an image.
- **AI model:** A trained neural network that recognises objects.
- **Software/framework:** Software loads the model and schedules its operations.
- **Hardware:** The CPU may coordinate the task, while a GPU or NPU can accelerate supported calculations.
- **Memory:** Stores the model parameters, input image, and intermediate data.
- **Inference:** The trained model processes a new image and returns predicted labels.

A GPU can be useful because image-recognition models often involve many mathematical operations that can be performed in parallel. However, the best hardware depends on the model, software support, memory requirements, and performance or power constraints.

## 4. Training vs Inference
**Training:** The model learns from examples by adjusting its parameters. Training can require substantial compute and memory resources.
**Inference:** The trained model processes new inputs to generate predictions or responses. Inference also needs compute and memory, but its requirements depend on the model size, input, and workload.

## 5. What I Learned
I learned that AI performance depends on more than the model alone. CPUs, GPUs, accelerators, software, and memory all contribute to executing AI workloads. Parallel computation can speed up suitable tasks, while insufficient memory or limited hardware support can affect performance.

## 6. Conclusion
Understanding AI hardware helps explain why different workloads benefit from different processors. Training and inference have different goals, and choosing suitable hardware depends on the computational workload, memory needs, software support, and efficiency requirements.
