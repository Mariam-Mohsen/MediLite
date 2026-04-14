# MediLite: AI-Powered Multi-Agent Medical Assistant

> **A coordinated multi-agent system designed to bridge the gap between complex clinical data and patient understanding.**

---

## Overview
**MediLite** is an intelligent orchestration framework built to simplify medical reports and provide safe, accurate, and context-aware responses to health concerns. By leveraging the **CrewAI** multi-agent framework, MediLite coordinates specialized LLM agents to process medical inputs and deliver actionable insights.

### Key Objectives
* **Simplify Complex Reports:** Translate lab results and clinical jargon into layman-friendly summaries.
* **Symptom Reflection:** Analyze symptom patterns without offering a formal diagnosis to ensure patient safety.
* **Real-time Knowledge:** Retrieve and summarize information from verified medical sources.
* **Conversation Continuity:** Maintain long-term memory of patient interactions for personalized assistance.

---

## Demo & Resources
* **[Watch the System Demo](./demo/MediLite_Demo.mp4)**: A screen recording of the Telegram bot in action.
* **[Exploratory Notebook](./notebooks/MediLite_Core.ipynb)**: The core Python logic and agent prompts.

---

## System Architecture
MediLite utilizes a modular, agent-based architecture designed for clarity and safety:

| Agent | Responsibility | Technology |
| :--- | :--- | :--- |
| **Simplifier** | Interprets clinical reports into plain language. | DeepSeek / Phi-3 |
| **Symptom Analyzer** | Evaluates patterns and offers non-diagnostic insights. | LLM Reasoning |
| **QA Assistant** | Answers general health-related questions. | Internal Memory |
| **Web Researcher** | Gathers real-time data from verified medical sources. | LangChain Tools |

###  The Workflow
1. **User Interaction:** Users input text or report data via the **Telegram Bot**.
2. **Input Classification:** A lightweight LLM classifies the input into specific task categories.
3. **Agent Coordination:** **CrewAI** triggers the relevant agents in sequence or parallel based on task complexity.
4. **Safety Filter:** All outputs are formatted with non-diagnostic disclaimers before being sent back to the user.

---

## Technical Stack
* **Frameworks:** CrewAI, LangChain
* **Models:** DeepSeek, Phi-3 (Instruction-tuned for medical reasoning)
* **Interface:** Telegram Bot API
* **Database/Memory:** CrewAI Memory Modules
* **Environment:** Python 3.10+

---

## Evaluation & Testing
The system was tested against various medical scenarios, including:
* **Report Simplification Accuracy:** Verified that technical lab values were correctly translated to basic health indicators.
* **Agent Delegation:** Tested the Web Agent’s ability to successfully consult the Knowledge Assistant for specialized queries.
* **Safety Boundaries:** Ensured the assistant consistently redirects users to medical professionals for critical concerns.

---

## Ethical Disclaimer
*MediLite is an educational project designed for information simplification and general health awareness. It is **not** a clinical diagnostic tool. Users are strictly advised to consult licensed healthcare professionals for medical advice.*
