# Advanced AI Search Assistant with LangGraph Ecosystem

A stateful, iterative AI Research Assistant built with **LangGraph** and **LangChain**. This project demonstrates how to build complex, multi-step agentic workflows that can search the web, synthesize information, and maintain state over multiple research loops.

It supports both **Cloud LLMs** (GPT-4) and **Local LLMs** (via Ollama/Llama 3.1), providing a flexible environment for privacy-focused or production-grade research.

---

## 🚀 Key Features

* **Stateful Iterative Research:** Uses LangGraph to manage research states, allowing the assistant to "think," search, and refine its answers iteratively.
* **Dual LLM Support:**
    * **OpenAI:** High-performance research using GPT-4.
    * **Ollama:** Fully local research using Llama 3.1 or other local models.
* **Web Integration:** Real-time web searching capabilities powered by DuckDuckGo.
* **Interactive UI:** Streamlit-based dashboard for real-time monitoring of the agent's thought process and final report generation.
* **Component Demos:** Includes standalone scripts to learn LangGraph primitives (Nodes, Edges, Memory, and Loops).

---

## 🏗️ Project Architecture

The assistant operates as a **Stateful Graph**:

1.  **START:** Receives a user query.
2.  **Search Node:** Formulates search queries and fetches results.
3.  **Process Node:** Filters and synthesizes information.
4.  **Reflect/Loop:** Determines if more information is needed. If yes, it loops back; if no, it proceeds to finalization.
5.  **END:** Generates a comprehensive final report.

---

## 📁 Repository Structure

| File | Description |
| :--- | :--- |
| `research_assistant.py` | Core logic for the OpenAI-powered research agent. |
| `research_assistant_local_llm.py` | Version optimized for local execution via Ollama. |
| `streamlit_app.py` | The web interface for the assistant. |
| `stateful_graph.py` | Implementation of the LangGraph state machine. |
| `compare_approaches.py` | Script comparing sequential chains vs. stateful graphs. |
| `*_demo.py` | Educational scripts for learning LangGraph step-by-step. |

---

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/cook-cxb/Advanced-AI-Search-Assistant-with-LangGraph-Ecosystem.git](https://github.com/cook-cxb/Advanced-AI-Search-Assistant-with-LangGraph-Ecosystem.git)
cd Advanced-AI-Search-Assistant-with-LangGraph-Ecosystem```


## Install Dependencies
```pip install -r requirements.txt

### 2.Environment Configuration

Create a .env file in the root directory:
```bash
OPENAI_API_KEY=your_openai_api_key_here
# Optional: For LangSmith tracing
LANGCHAIN_TRACING_V2=true
LANGCHAIN_API_KEY=your_langchain_api_key

### 4. Local LLM Setup (Optional)
If you wish to run the assistant locally:

Install [Ollama](ollama.com).
Pull the Llama 3.1 model:

```Bash

ollama run llama3.1

