#  Building ReAct Agents

This repository documents my learning and implementation journey in building **Reasoning + Acting (ReAct)** based AI Agents — systems that think, act, observe, and learn iteratively.

Each notebook represents a key stage in understanding agent reasoning and autonomy — from an initial conceptual prototype to a more structured, tool-using query agent.


##  Project Structure

```
Building-ReAct-Agent/
│
├── ReAct_Agent.ipynb        # Initial prototype exploring the ReAct pattern
├── Query_Agent.ipynb        # Refined agent implementing full Thought → Action → PAUSE → Observation loop
├── README.md
└── (more agents coming soon...)
```

---

##  Current Agents

###  1. ReAct Agent (Prototype)

**Notebook:** `ReAct_Agent.ipynb`
**Purpose:**
A rough experimental notebook built to understand the logic of reasoning loops and tool use within the ReAct framework.

**Highlights:**

* Demonstrates the **Thought → Action → Observation → Answer** cycle.
* Focuses on concept formation rather than execution reliability.
* Includes initial prompt and control flow design.
* Serves as a learning foundation for more advanced agents.

---

###  2. Query Agent (Refined Implementation)

**Notebook:** `Query_Agent.ipynb`
**Purpose:**
A **polished and functional ReAct-agent** capable of autonomous reasoning and querying multiple knowledge sources.

**Operational Loop:**

```
Thought → Action → PAUSE → Observation → Repeat
```

**Highlights:**

* Implements a full ReAct reasoning loop with clear phase separation.
* Uses a **custom knowledge base** for system analysis (built from PDF, DOCX, TXT course materials).
* Integrates **Wikipedia Search** for open-domain knowledge.
* Manages contextual memory with a `shared_agent` for topic continuity.
* Includes an `AgentManager` that decides when to reuse or spawn a new agent instance.
* Structured design and markdown-rich documentation for clarity.

**Core Components:**

* **Knowledge Base Creation:** Document loading, chunking, embedding, and FAISS vector store.
* **Prompt Engineering:** Defines explicit rules for Thought, Action, PAUSE, and Observation phases.
* **Tool Integration:**

  * `system_analysis_qa` – Queries course-specific materials.
  * `wiki_search` – Handles general topics via Wikipedia.
* **Autonomous Control Loop:** The agent executes actions, pauses for observations, and continues reasoning until a final answer is reached.

---

##  Framework Overview

###  The ReAct Agent Loop

Each agent follows a predictable cognitive loop:

| Step            | Purpose                                                                        |
| --------------- | ------------------------------------------------------------------------------ |
| **Thought**     | The agent reasons internally — analyzing the question and deciding next steps. |
| **Action**      | Executes a specific tool or query based on its reasoning.                      |
| **PAUSE**       | Temporarily halts to await results of the previous action.                     |
| **Observation** | Incorporates the returned result into its reasoning context.                   |
| **Repeat**      | Continues until a final **Answer** is confidently produced.                    |

This **loop** enables agents to perform complex reasoning transparently and interact with tools or environments dynamically.

---

##  Setup & Usage

1. **Clone the repository**

   ```bash
   git clone https://github.com/TasnimTamanna02/Building-ReAct-Agent.git
   cd Building-ReAct-Agent
   ```

2. **Run in Jupyter or Google Colab**

   * Start with `ReAct_Agent.ipynb` for conceptual understanding.
   * Move to `Query_Agent.ipynb` for the production-style agent loop.

3. **Follow the Markdown sections**
   Each section explains not only *what* the code does, but *why* — providing conceptual grounding for future agent designs.

---

##  Learning Focus

This repository serves as a **progressive learning framework** for:

* Building reasoning-driven agentic architectures.
* Understanding and implementing **Thought → Action → PAUSE → Observation** control loops.
* Practicing **prompt engineering** and **tool orchestration**.
* Laying the groundwork for future AI systems such as *Teaching Assistant AI* or *Study Companion AI*.

---

##  Author

**Tasnim Tamanna**
*Computer Science & Engineering Student | AI/ML Learner | Exploring Agentic Reasoning Systems*

