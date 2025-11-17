# Agentic AI Architectures: Multi-Agent Loop  
### Designing, Coordinating, and Refining Collaborative AI Systems with ADK & Gemini

---

## 📘 Project Overview

This project extends the foundation built in **[Building a Reasoning AI Agent](../01_reasoning_agent/README.md)** by advancing into **multi-agent architectures** using Google’s **Agent Development Kit (ADK)** and **Gemini** models.

While the previous notebook demonstrated reasoning within a single agent, this project explores **collaborative orchestration** — where multiple specialized agents work together in structured workflows.  
The focus is on three core patterns of **agent coordination**:

- **Sequential Workflows** – Deterministic task pipelines  
- **Parallel Workflows** – Concurrent execution for speed and scalability  
- **Loop Workflows** – Iterative refinement and self-improvement  

Together, these patterns form the architectural backbone of **agentic AI systems** capable of reasoning, delegation, and continuous optimization.

---

## 🧩 Key Features

- **Multi-Agent Orchestration**  
  Build and coordinate multiple agents through Sequential, Parallel, and Loop patterns.

- **Role-Specialized Agents**  
  Implement distinct agents such as Researcher, Writer, Editor, and Critic for modular collaboration.

- **Deterministic Execution Control**  
  Use `SequentialAgent` for ordered pipelines and `ParallelAgent` for concurrent tasks.

- **Iterative Refinement (LoopAgent)**  
  Enable self-critiquing and improvement cycles where agents refine their own outputs until quality thresholds are met.

- **Composability & Scalability**  
  Each agent can be reused or extended, supporting scalable system design and orchestration at enterprise level.

---

## 🏗️ Tech Stack

| Category | Technologies |
|-----------|--------------|
| Language | Python 3.x |
| Framework | Google **Agent Development Kit (ADK)** |
| Model | **Gemini 2.5 Flash Lite** |
| Tools | `SequentialAgent`, `ParallelAgent`, `LoopAgent`, `FunctionTool`, `google_search` |
| Environment | Kaggle / Jupyter Notebooks |
| Libraries | `google-generativeai`, `adk`, `IPython.display`, `types`, `os`, `re` |

---

## 📚 Workflow Patterns Demonstrated

| Pattern | Description | Example Use Case |
|----------|--------------|------------------|
| **SequentialAgent** | Executes sub-agents in fixed order — output of one becomes input of next. | Blog generation pipeline (Outline → Writer → Editor) |
| **ParallelAgent** | Runs independent sub-agents concurrently for efficiency. | Multi-domain research (Tech, Health, Finance) |
| **LoopAgent** | Iteratively refines work until approved or max iterations reached. | Writer ↔ Critic story refinement loop |

---

## 🧠 Architecture Highlights

### 1️⃣ **Sequential Workflow — “The Assembly Line”**
A fixed-order pipeline ensuring predictable execution and deterministic outcomes.  
Used to build a blog generation workflow where agents act as Outline, Writer, and Editor.

### 2️⃣ **Parallel Workflow — “Independent Researchers”**
Multiple agents work simultaneously on unrelated subtasks.  
After completion, an Aggregator Agent merges their outputs into a unified report.

### 3️⃣ **Loop Workflow — “The Refinement Cycle”**
A feedback-driven loop between a Writer and a Critic.  
The system revises its own story drafts until the Critic returns the token `APPROVED` or the loop reaches its iteration cap.

---

## 🚀 Example Execution

```python
await run_and_print("What are the top AI conferences in 2025?")
````

**Example Output:**

> The top AI conferences in 2025 include **NeurIPS (San Diego)**, **ICML (Vancouver)**, and **World Summit AI (Amsterdam)**.
> Each event showcases advancements in reasoning systems, multi-agent orchestration, and AI safety.
>
> **Sources:**
>
> * [NeurIPS 2025 — Official Site](https://neurips.cc/Conferences/2025)
> * [ICML 2025 — Conference Page](https://icml.cc/Conferences/2025)
> * [World Summit AI 2025](https://www.worldsummit.ai/)

---

## ⚙️ Engineering Principles

* **Modularity:** Each agent performs a narrow, well-defined role.
* **Orchestration:** Control flows via Sequential, Parallel, or Loop controllers.
* **Traceability:** Every agent’s input and output is logged in the shared session state.
* **Determinism:** Execution order and loop termination are explicitly defined, not left to model interpretation.
* **Reusability:** Agents can be repurposed in other orchestration designs with minimal modification.

---

## 🧭 Key Learnings

* Moving from *single-agent reasoning* to *multi-agent orchestration* introduces new design dimensions: coordination, state management, and termination logic.
* Effective agent systems rely on **explicit control flow** — not just prompt chaining.
* The `LoopAgent` pattern represents a step toward **autonomous self-improvement**, laying the groundwork for future *self-evaluating* AI systems.

---

## 🔄 Relationship to Previous Work

This notebook builds directly on the foundation established in:

> [**Building a Reasoning AI Agent with ADK & Gemini**](../01_reasoning_agent/README.md)
> Focused on reasoning and tool-use within a single agent.

This second notebook extends that foundation into **multi-agent architecture and system coordination**.
