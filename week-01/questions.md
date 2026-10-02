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
**Status: Completed.**
- [x] I checked IBM's definitions of AI, ML, DL, and GenAI.
- [x] I checked Google Cloud's explanation of AI agents and tool use.
- [x] I confirmed that ML is a subset of AI and DL is a subset of ML.
- [x] I confirmed that generative models create content and that agents can use models and tools to perform multi-step tasks.
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
- **Prompt:** The input or instruction given by the user to the model.
- **Token:** A piece of text processed by the model. It may be a whole word, part of a word, punctuation, or another text unit.
- **Context:** The information available to the model for the current response, such as the prompt and relevant conversation history, within its context limit.
- **Probability:** A numerical value representing how likely a possible next token is according to the model's current prediction.
- **Next-token prediction:** The process of estimating a probability distribution over possible next tokens, given the tokens already available.
- **Generated response:** The text produced by repeatedly selecting tokens and converting the resulting sequence back into readable text.

### Training vs inference
**Training** is when the model learns patterns by adjusting its internal parameters using training data. **Inference** is when the already-trained model processes a prompt and generates an output. In ordinary inference, the model's learned parameters are not updated for every question asked.

### Flow Diagram
```text
User submits a prompt
        ↓
Text is split into tokens
        ↓
Tokens + available context
        ↓
Model processes the input
        ↓
Probability distribution over possible next tokens
        ↓
Select one next token
        ↓
Append token to the sequence
        ↓
More text needed?
   ↓ Yes        ↓ No
Process again   Generated response
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
Status: Complete.
- [x] I checked Microsoft's explanation of tokens and inference.
- [x] I checked the educational source's explanation of next-token prediction.
- [x] I confirmed that training adjusts model parameters, whereas inference uses a trained model to generate a response.
- [x] I confirmed that fluent output is not a guarantee of factual accuracy.
**Verification note:** I will mark these items after I directly check the referenced sources.

### R — Reflection
I learned that an LLM generates text step by step by predicting the next token using the prompt and available context. Training teaches the model patterns, while inference uses those learned patterns to generate a response. Since the model predicts plausible text rather than guaranteeing truth, I should verify important claims using reliable sources.

## Q4. Hallucination Experiment: Can AI Sound Confident and Still Be Wrong?
### A — Answer
**Exact question asked to both AI assistants:**
"In Python, what does list.sort() return? Does it modify the original list? Also explain the difference between list.sort() and sorted()."

### Experiment Results
| AI Assistant | Response Summary | Verified Claim | Result |
|---|---|---|---|
| ChatGPT | Explained that `list.sort()` returns `None` and modifies the original list in place. It explained that `sorted()` returns a new sorted list while leaving the original list unchanged. | `list.sort()` returns `None`, modifies the list in place, and `sorted()` returns a new sorted list. | Correct |
| Claude | Explained that `list.sort()` returns `None` and modifies the original list in place. It also explained that `sorted()` returns a new sorted list and does not modify the original list. It provided examples and additional details about iterables and sorting options. | `list.sort()` returns `None`, modifies the list in place, and `sorted()` returns a new sorted list. | Correct |

### E — Evidence
**Verification source — Python Documentation: Sorting Techniques**
https://docs.python.org/3.13/howto/sorting.html
The Python documentation explains that `list.sort()` sorts a list in place and returns `None`. It also explains that `sorted()` returns a new sorted list.

### V — Verification
I compared the important claims from both AI assistants with the official Python documentation.
- [x] ChatGPT's explanation of `list.sort()` was checked.
- [x] Claude's explanation of `list.sort()` was checked.
- [x] I confirmed that `list.sort()` modifies the original list in place.
- [x] I confirmed that `list.sort()` returns `None`.
- [x] I confirmed that `sorted()` returns a new sorted list.
**Verification result:** Both ChatGPT and Claude gave answers consistent with the official Python documentation. No contradictory or incorrect claim was found in the main answer.

### R — Reflection
Both AI assistants produced correct answers, so this particular test did not expose a hallucination. However, the experiment showed that a confident and detailed answer should still be checked against a reliable reference. Claude provided more detail than ChatGPT, but the additional detail did not change the main verified conclusion. I learned that verification is useful even when the AI answer appears clear and convincing.

## Q5. AI Assistant vs Search vs Authoritative Reference
### A — Answer
**Common technical question:**
> What does HTTP status code 404 mean?
| Method | Findings |
|---|---|
| **AI Assistant — ChatGPT** | ChatGPT explained that HTTP status code 404 means the server could not find the requested resource. It also explained that 404 is a 4xx client error and that it does not by itself indicate whether the resource is temporarily or permanently unavailable. |
| **Web Search — Google** | I searched the exact same question on Google. The search results showed MDN Web Docs as a top result. MDN explains that a 404 response means the server cannot find the requested resource. |
| **Authoritative Reference — RFC 9110** | RFC 9110, Section 15.5.5, gives the formal definition of 404 Not Found. It states that the origin server did not find a current representation for the target resource, or is not willing to disclose that one exists. It also states that 404 does not indicate whether the condition is temporary or permanent. |

### Comparison
| Criterion | AI Assistant | Web Search | Authoritative Reference |
|---|---|---|---|
| **Accuracy** | Good for a direct explanation | Depends on the quality of the result selected | Provides the formal specification |
| **Explanation** | Easy to understand and conversational | Can provide several explanations from different sources | More formal and technical |
| **Traceability** | Depends on whether sources are provided | Source pages can be opened directly | Directly traceable to the HTTP specification |
| **Ease of verification** | Easy to understand, but claims should still be checked | Easy to compare multiple sources | Best for checking the exact standard definition |

### Final Conclusion
I would use an AI assistant when I need a quick explanation, examples, or help understanding a technical concept.
I would use web search when I need to discover relevant sources, compare explanations, or find documentation.
I would require a primary or authoritative source before making an important technical decision when the exact specification, standard, requirement, or official behavior matters.

### E — Evidence
**AI source:** ChatGPT response to the exact question:

> What does HTTP status code 404 mean?
**Web search evidence:** Google search for the exact question. The search results showed MDN Web Docs and other explanatory sources.

**Secondary technical source — MDN Web Docs:**
https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/404
MDN explains that HTTP 404 Not Found indicates that the server cannot find the requested resource.

**Authoritative/primary source — RFC 9110, Section 15.5.5:**
https://www.rfc-editor.org/rfc/rfc9110.html#name-404-not-found
RFC 9110 gives the formal definition of the 404 status code and explains that it does not indicate whether the missing representation is temporary or permanent.

### V — Verification
I compared the ChatGPT answer and Google search findings with the official HTTP specification.
- [x] ChatGPT's explanation that 404 means the requested resource was not found was confirmed.
- [x] The Google search result from MDN was checked against the MDN page.
- [x] The MDN explanation was compared with RFC 9110.
- [x] The statement that 404 does not indicate whether the condition is temporary or permanent was confirmed in RFC 9110.
Verification result: The main explanation from ChatGPT and the MDN search result agree with the authoritative definition in RFC 9110.

### R — Reflection
I learned that an AI assistant, a search engine, and an authoritative reference serve different purposes. AI is useful for getting a quick explanation, while search helps locate information and relevant sources. An authoritative source is important when the exact technical definition or standard behavior matters. I should therefore use AI and search as ways to understand and find information, but verify important technical decisions against an appropriate authoritative source.

## Q6. What Is an AI Agent?
### A — Answer
| Concept                  | Explanation                                                                                                                                                                                                                      |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **LLM**                  | A Large Language Model is a model trained on large amounts of data that can understand and generate language by predicting and producing tokens based on the input context.                                                      |
| **LLM Application**      | An LLM application is a software application that uses an LLM as one of its components to provide a specific feature or solve a particular problem.                                                                              |
| **RAG System**           | Retrieval-Augmented Generation (RAG) is a system that retrieves relevant information from an external source, such as documents or a database, and provides that information as context to the LLM before generating a response. |
| **Tool-using Assistant** | A tool-using assistant is an AI application that can call external tools or services, such as calculators, search systems, APIs, or databases, to obtain information or perform an operation.                                    |
| **AI Agent**             | An AI agent is a system that uses a model together with tools and orchestration to pursue a goal, decide what actions or tools are needed, use their results, and continue through a workflow until it can produce a result.     |

RAG adds retrieved information to the LLM's context, while an agent can use tools and make decisions about actions as part of a multi-step workflow.

### Comparison
| System                   | Main capability                                                                          |
| ------------------------ | ---------------------------------------------------------------------------------------- |
| **LLM**                  | Generates or processes language                                                          |
| **LLM Application**      | Uses an LLM inside a larger software application                                         |
| **RAG System**           | Retrieves external information and uses it as context for generation                     |
| **Tool-using Assistant** | Can call available tools to perform specific operations                                  |
| **AI Agent**             | Can use models, tools, and orchestration to work toward a goal through one or more steps |

### Architecture Diagram
```text
User Request
     ↓
   Model / LLM
     ↓
Decide whether a tool is needed
     ↓
   Tool Call
     ↓
 External Tool / Data Source
     ↓
   Tool Result
     ↓
Model processes the result
     ↓
Decision / Next Action
     ↓
Final Response
```
The important difference is that the tool result can influence what the system does next. In a multi-step agentic workflow, the system can continue using tools or actions until the task is completed. Google Cloud describes agents as applications that process input, use available tools, and take actions based on decisions.

### What makes an agent different from a simple chatbot?
A simple chatbot may mainly receive a prompt and generate a response. An agentic system can go beyond producing text by deciding when to use tools, obtaining information or performing actions, examining the results, and continuing through a multi-step workflow toward a goal. The exact amount of autonomy depends on how the system is designed.

### Non-VLSI Example
A travel-booking assistant can be designed as an agentic workflow. A user could ask it to plan a trip. The system could search available flights and hotels using tools, compare the results with the user's requirements, ask for missing information if necessary, and then prepare the final itinerary. The model is therefore not only generating text; it is participating in a workflow that uses external tools and decisions.

### E — Evidence
**Source 1 — Google Cloud: Generative AI Glossary — AI Agents**
[https://docs.cloud.google.com/docs/generative-ai/glossary](https://docs.cloud.google.com/docs/generative-ai/glossary)
Google Cloud describes an AI agent as an application that achieves a goal by processing input, reasoning with available tools, and taking actions based on its decisions.

**Source 2 — Google Cloud: What is Retrieval-Augmented Generation (RAG)?**
[https://cloud.google.com/use-cases/retrieval-augmented-generation](https://cloud.google.com/use-cases/retrieval-augmented-generation)
Google Cloud explains that RAG combines information retrieval with LLM generation and uses retrieved information to augment the model's context.

### V — Verification
I compared the definitions and workflow described above with the referenced Google Cloud documentation.
- [x] I checked the AI agent definition.
- [x] I checked the explanation of tools and agent workflows.
- [x] I checked the explanation of RAG and retrieved context.
- [x] I confirmed the difference between generating a response and taking actions through tools.
**Verification status: Complete.**

### R — Reflection
I learned that an LLM, an LLM application, RAG system, tool-using assistant, and AI agent are related but are not the same thing. An LLM mainly provides the language or reasoning capability, while an application adds software around it. RAG adds retrieved information, and tool use allows the system to interact with external capabilities. An agent adds goal-directed orchestration and can use tools through a multi-step workflow.

## Q7. Where Should Humans Still Make the Decision?
### A — Answer
AI can be useful for reading documents, answering questions, summarizing information, generating text, and suggesting actions. However, I would still require a human to inspect or approve the output before acting in situations where an incorrect result could cause significant consequences.
| Situation | Possible Failure | Required Verification | Who/What Approves |
|---|---|---|---|
| **1. Medical information or health-related recommendation** | The AI could misunderstand symptoms, provide incomplete information, or give an unsuitable recommendation. | Check the information against reliable medical sources and consult a qualified healthcare professional. | Qualified healthcare professional |
| **2. Financial decision or investment recommendation** | The AI could use incomplete information, misunderstand risk, or produce an incorrect calculation. | Check calculations, current information, assumptions, and relevant financial documentation. | Person responsible for the financial decision |
| **3. Legal advice or interpretation of a legal document** | The AI could misunderstand the law, miss an important condition, or interpret a document incorrectly. | Check the relevant law, official legal sources, and the original document. | Qualified legal professional or responsible decision-maker |
| **4. Safety-critical instruction or procedure** | An incorrect instruction could create a physical safety risk or cause equipment damage. | Compare the output with approved procedures, manuals, standards, and safety requirements; test where appropriate. | Qualified engineer or authorized safety personnel |
| **5. Important academic or engineering result** | The AI could make a calculation error, use a wrong assumption, or provide unsupported technical information. | Recalculate independently, test the result, inspect assumptions, and check reliable technical references. | Human engineer, student, or responsible reviewer |

### Simple Rule for Responsible AI-Assisted Work
I should not act on an AI-generated recommendation merely because it sounds correct. When the result could have important consequences, a human should inspect the assumptions, verify the evidence, test the result where possible, and approve the final decision.

### E — Evidence
The Week 1 guide emphasizes that AI-assisted engineering is intended to support human judgment rather than transfer responsibility to an AI system. It asks for five situations in which a human should inspect or approve the output, together with the possible failure, required evidence, and responsible approver.
The guide also states that important factual or technical claims should be verified using appropriate evidence and that AI output should not be treated as proof by itself.

### V — Verification
I checked each situation to make sure it includes:
- [x] A situation where human inspection or approval is required.
- [x] A possible failure if the AI output is accepted without verification.
- [x] Evidence or checks needed before trusting the result.
- [x] A person or authority responsible for approving the result.
**Verification status: Complete.**

### R — Reflection
I learned that using AI does not remove human responsibility for important decisions. The level of checking should increase when an incorrect AI result could cause greater harm, loss, or other consequences. I should treat AI as a tool that supports my reasoning while keeping the final decision and accountability with a human.

## Q8. Find AI Around You
### A — Answer
| System / Feature | AI/ML Involvement | Task Type | Evidence / Source | Conclusion |
|---|---|---|---|---|
| **1. Gmail Spam Filter** | Yes | Classification | Google explains that Gmail uses machine learning to predict which emails are likely to be spam. | AI/ML is involved in classifying messages as spam or not spam. |
| **2. Google Maps ETA** | Yes | Prediction | Google explains that Maps uses machine-learning models, including Graph Neural Networks, to improve ETA predictions using traffic and historical patterns. | AI/ML is involved in predicting travel time. |
| **3. YouTube Recommendations** | Yes | Recommendation / Prediction | YouTube explains that its recommendation system uses machine learning and signals such as clicks, watch time, likes, dislikes, and survey responses to recommend videos. | AI/ML is involved in selecting and ranking personalized recommendations. |
| **4. Google Photos Face Groups** | Yes | Recognition / Classification | Google explains that Face Groups detects faces, creates face models, estimates similarity between faces, and groups photos that are likely to contain the same person. | AI/ML-style modeling is involved in recognizing and grouping similar faces. |
| **5. Android System Intelligence – Now Playing** | Yes | Recognition | Google states that Android System Intelligence provides machine-learning features and includes Now Playing, which recognizes music around you. | AI/ML is involved in recognizing music. |

### Simpler Rule-Based Alternative
For **YouTube recommendations**, a simpler traditional approach could recommend videos using fixed rules such as:
- show the most-viewed videos;
- show videos from subscribed channels;
- show videos from a selected category.
This could produce recommendations, but it would be less personalized than a system that learns from signals such as viewing habits, watch time, likes, dislikes, and other feedback. YouTube explains that its earlier recommendation approach relied more heavily on popularity, while later systems used machine learning to personalize recommendations. Therefore, a simpler rule-based system could produce similar-looking behavior, but with less adaptive personalization.

### E — Evidence
**1. Gmail**
Google — *How machine learning in G Suite makes people more productive*  
https://blog.google/products-and-platforms/products/workspace/how-machine-learning-g-suite-makes-people-more-productive/

Google explains that Gmail uses machine learning to predict which emails are most likely to be spam. 

**2. Google Maps**
Google — *Google Maps 101: How AI helps predict traffic and determine routes*  
https://blog.google/products-and-platforms/products/maps/google-maps-101-how-ai-helps-predict-traffic-and-determine-routes/

Google explains that machine-learning models are used to improve ETA predictions using traffic and historical patterns.

**3. YouTube**
YouTube Blog — *On YouTube's recommendation system*  
https://blog.youtube/inside-youtube/on-youtubes-recommendation-system/
YouTube explains that machine learning is used in its recommendation system and that signals such as clicks, watch time, likes, dislikes, and survey responses help inform recommendations.

**4. Google Photos**
Google Photos Help — *Set up and manage your face groups*  
https://support.google.com/photos/answer/6128838
Google explains that Face Groups detects faces, creates face models, estimates similarity between faces, and groups similar faces.

**5. Android System Intelligence**
Google Pixel Help — *Android System Intelligence*  
https://support.google.com/pixelphone/answer/12112173
Google states that Android System Intelligence provides machine-learning features and lists Now Playing as a feature that recognizes music around you.

### V — Verification
I checked the public documentation for each system rather than assuming that a feature is AI simply because it appears intelligent.
- [x] Gmail documentation supports machine-learning-based spam detection.
- [x] Google Maps documentation supports machine-learning-based ETA prediction.
- [x] YouTube documentation supports machine-learning-based recommendations.
- [x] Google Photos documentation supports face detection, face models, and face-similarity prediction.
- [x] Android System Intelligence documentation identifies Now Playing as a machine-learning feature involving music recognition.
- [x] I investigated a simpler rule-based approach for YouTube recommendations.
**Verification status: Complete.**

### R — Reflection
I learned that AI can appear in many everyday features, but the type of task can be different. Gmail mainly performs classification, Google Maps performs prediction, YouTube performs recommendation, and Google Photos and Now Playing perform recognition-related tasks. I also learned that a simpler rule-based system can sometimes produce similar behavior, but it may not adapt to user data and patterns as effectively as a learned system. I should check public evidence before claiming that a product feature uses AI.

## Q9. Prediction, Classification, and Generation
### A — Answer
| Example | Primary Task Type | Reason |
|---|---|---|
| **A. Predicting house prices** | **Prediction** | The system estimates a numerical value, such as the expected price of a house, from available information. |
| **B. Detecting whether an image contains a cat** | **Classification** | The system assigns the image to a category such as "cat present" or "cat not present." |
| **C. Writing an email from a short instruction** | **Generation** | The system creates new text based on the instruction. |
| **D. Predicting whether a customer will cancel a subscription** | **Prediction** | The system estimates the likelihood that a future event, such as cancellation, will occur. |
| **E. Summarizing a research paper** | **Generation** | The system produces new text that represents the important information from the original paper. |
| **F. Identifying whether a transaction is fraudulent** | **Classification** | The system assigns a transaction to a category such as fraudulent or legitimate. |
| **G. Generating an image from a text description** | **Generation** | The system creates new image content from the supplied text description. |
| **H. Predicting the next word/token in a sentence** | **Prediction** | The model estimates which token is most likely to come next based on the tokens already available. |

### Why Next-Token Prediction Is Fundamental
Next-token prediction is fundamental to modern language models because the model can generate a complete response by repeatedly predicting what token should come next from the available context. By continuing this process, the model can produce many different kinds of language output, including emails, summaries, answers to questions, and computer code. The final application may look like a different task, but language generation can still be built from repeated next-token predictions.
Some real systems can involve more than one task type. For example, summarization involves understanding or processing the input and then generating a summary. In this table, the classification is based on the **primary visible behavior** of the task.

### E — Evidence
The Week 1 guide defines prediction, classification, and generation as broad AI task types and specifically includes the eight examples above. It also asks for an explanation of why next-token prediction is fundamental to modern language models.

### V — Verification
I checked each example against the basic distinction between prediction, classification, and generation.
- [x] House-price and customer-cancellation examples estimate an outcome or value, so they are prediction tasks.
- [x] Cat detection and fraud detection assign examples to categories, so they are classification tasks.
- [x] Email writing, research-paper summarization, and text-to-image generation create new output, so they are generation tasks.
- [x] Next-token prediction is a prediction task and can be repeated to generate longer language output.
**Verification status: Complete.**

### R — Reflection
I learned that prediction, classification, and generation describe different kinds of AI behavior. Classification assigns an input to a category, prediction estimates a value or outcome, and generation produces new content. I also learned that the final application can look more complex than the underlying task, and that many language applications can be built from repeated next-token prediction.

## Q10. Design Your Personal AI Verification Protocol
### A — Answer
My seven-step procedure for checking an AI-generated result before accepting it for engineering work is:
**1. Define the problem**  
Clearly state what needs to be solved, what the expected result is, and what constraints apply.  
**Why:** This helps prevent the AI from solving the wrong problem or producing an answer that does not match the actual requirement.

**2. Inspect the assumptions**  
Identify the assumptions made by the AI and check whether they are reasonable and relevant to the problem.  
**Why:** An incorrect or hidden assumption can make the final result wrong even when the reasoning looks convincing.

**3. Check the evidence and sources**  
Identify important factual or technical claims and check them against reliable documentation, references, or other appropriate evidence.  
**Why:** This catches unsupported claims and prevents treating AI output itself as proof.

**4. Test the result**  
Use calculations, examples, experiments, or other suitable tests to check whether the result behaves as expected.  
**Why:** Testing can reveal errors that are not obvious from reading the answer.

**5. Compare with an independent result**  
Compare the AI-generated result with a trusted reference, known result, or an independently worked-out solution.  
**Why:** Independent comparison can reveal mistakes or missing information.

**6. Check limitations and uncertainty**  
Identify anything that is unclear, unsupported, or dependent on assumptions.  
**Why:** This prevents uncertain information from being treated as a confirmed result.

**7. Decide whether to accept, reject, or revise**  
Based on the checks above, decide whether the output can be accepted, should be rejected, or needs revision and further verification.  
**Why:** The final decision remains a human engineering judgment rather than an automatic acceptance of the AI output.

### E — Evidence
The Week 1 guide requires a seven-step procedure and specifically says the protocol must include defining the problem, inspecting assumptions, checking evidence/source, testing the result, and deciding whether to accept, reject, or revise the output.
The Week 1 workflow also emphasizes defining, investigating, inspecting, verifying, concluding, documenting, and reflecting before accepting an AI result.

### V — Verification
I compared my seven-step protocol with the Week 1 assessment requirements.
- [x] The protocol contains seven steps.
- [x] It defines the problem.
- [x] It inspects assumptions.
- [x] It checks evidence and sources.
- [x] It tests the result.
- [x] It includes an accept, reject, or revise decision.
- [x] Each step explains its purpose and the failure it is intended to catch.
- [x] A non-VLSI worked example is included.
**Verification status: Complete.**

### R — Reflection
I learned that verifying an AI result is not just checking whether the final answer looks correct. I need to understand the problem, inspect the assumptions, check the evidence, test the result, and make a final human judgment. This protocol can be improved later in the program as I learn more about AI-assisted engineering.

### Worked Example — Non-VLSI Task
Suppose I ask an AI assistant to calculate the total cost of a purchase after applying discounts.

**1. Define the problem:**  
I provide the prices, quantities, discounts, and any tax or shipping requirements.

**2. Inspect the assumptions:**  
I check whether the AI assumed that the discount applies before or after tax and whether the quantities are correct.

**3. Check the evidence and sources:**  
I verify the prices and discount values against the information provided by the seller.

**4. Test the result:**  
I calculate the total independently.

**5. Compare with an independent result:**  
I compare my calculation with the AI-generated total.

**6. Check limitations and uncertainty:**  
I check whether any required information, such as tax or shipping charges, is missing.

**7. Accept, reject, or revise:**  
If the calculation is correct and the assumptions are valid, I accept it. If there is an error, I revise the inputs or reject the result and calculate it again.
