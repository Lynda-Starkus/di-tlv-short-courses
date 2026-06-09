# LLMOps quiz


## Questions

### 1. What is the main purpose of LLMOps?

A. To write longer prompts.  
B. To make LLM applications repeatable, testable, deployable, and monitorable.  
C. To replace backend engineering.  
D. To avoid evaluating model outputs.

---

### 2. A team tuned and evaluated a model with an instruction template, but production sends only the raw user question. What is the likely issue?

A. The production input no longer matches the training/evaluation input format.  
B. The model will always become faster.  
C. The evaluation set becomes unnecessary.  
D. The data warehouse is automatically updated.

---

### 3. Why do we often transform large datasets inside a data warehouse instead of loading everything into a notebook?

A. Notebooks cannot display tables.  
B. SQL is always more accurate than Python.  
C. Large data may not fit into notebook memory, and warehouses are designed for scalable filtering/joining.  
D. JSONL files cannot be created from notebooks.

---

### 4. In a pipeline, why is it useful to pass a file URI instead of the full dataset object?

Write a 2–3 sentence answer.

---

### 5. Match the concept to the description.

| Concept | Description |
|---|---|
| A. Orchestration | 1. Running the workflow without a human manually executing every step. |
| B. Automation | 2. Making the model available to another system through batch or API. |
| C. Deployment | 3. Defining step order and dependencies. |

---

### 6. Which artifact should usually be versioned?

A. Training dataset  
B. Prompt template  
C. Evaluation set  
D. All of the above

---

### 7. Which deployment style is usually better for “summarize all tickets every Friday night”?

A. Batch  
B. Real-time API only  
C. Manual notebook execution only  
D. No deployment needed

---

### 8. Which deployment style is usually better for “draft a reply while a support agent is viewing a ticket”?

A. Batch only  
B. Real-time API  
C. Once-per-month offline report  
D. Static CSV export

---

### 9. What is the beginner-friendly reason to care about containers?

A. They make every model more accurate.  
B. They package code and dependencies so a pipeline step can run more consistently across environments.  
C. They remove the need for monitoring.  
D. They replace evaluation datasets.

---

### 10. A new model version has lower latency but worse review pass rate. What should the team do first?

A. Deploy it immediately because it is faster.  
B. Ignore the review pass rate.  
C. Compare against the evaluation set and decide whether the quality tradeoff is acceptable.  
D. Delete the previous model version.

---

### 11. Give one example of an operational metric and one example of a quality metric for an LLM application.

Write a short answer.

---

### 12. Mini design question

You are building a support-ticket assistant. The team wants to release a new prompt template. Name three checks or artifacts you would want before releasing it.

---

<details>
<summary>Answer key</summary>

1. B  
2. A  
3. C  
4. Strong answer: because large datasets can be too heavy to pass through memory or pipeline task objects. Passing a URI lets each component read or stream the data from storage and makes the workflow more scalable and reproducible.  
5. A → 3, B → 1, C → 2  
6. D  
7. A  
8. B  
9. B  
10. C  
11. Examples: operational = latency, error rate, throughput; quality = eval score, human review pass rate, user rating.  
12. Examples: prompt template version, evaluation results, rollback plan, safety checks, sample outputs reviewed by humans, deployment manifest, monitoring thresholds.

</details>
