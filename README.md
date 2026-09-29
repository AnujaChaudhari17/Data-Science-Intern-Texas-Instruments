# Drago: Agentic Natural-Language-to-SQL & Analytics Platform

**Drago** is an intelligent, agentic natural-language interface designed to automate exploratory data analysis (EDA), database querying, and dashboard creation across large-scale enterprise databases (**Oracle** and **SQream**). By translating natural language questions into context-aware SQL and dynamic visualizations, Drago reduces query execution, data analysis, and dashboard setup times from hours to minutes.

---

## Key Features

* **Agentic State Machine Orchestration**: Built using **LangGraph** to dynamically classify user intent (data querying, chart creation, dashboard assembly, and follow-up requests) and route execution paths.
* **Schema Pruning via RAG**: Leverages **Vectara** semantic search to reduce broad enterprise schemas (200+ tables with 150+ columns each) down to the specific relevant tables and columns per query.
* **Intelligent Dual-Database Routing**: Evaluates query complexity to route tasks to either Oracle or SQream, paired with an LLM-driven retry loop that self-diagnoses and auto-corrects execution errors.
* **Automated Visualization via MCP**: Integrates **Apache Superset** using the **Model Context Protocol (MCP)** to generate interactive charts and dashboards directly from conversational prompts.
* **Persistent Multi-Turn Memory**: Uses **LangGraph Checkpointing** to retain session context and enable seamless multi-turn follow-ups.
* **Interactive UI & Reusable Server**: Built with **Chainlit** for real-time streaming, live reasoning steps, and embedded visuals, backed by SQLite for history tracking, while exposing the entire pipeline as a reusable MCP server.

---

## Tech Stack

| Component | Technology |
| :--- | :--- |
| **Agent Framework** | LangGraph, Chainlit |
| **Retrieval & RAG** | Vectara Semantic Search |
| **Databases** | Oracle, SQream, SQLite |
| **Visualizations & Protocol** | Apache Superset, Model Context Protocol (MCP) |

---

## System Architecture
