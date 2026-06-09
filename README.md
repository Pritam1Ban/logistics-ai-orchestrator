# logistics-ai-orchestrator
An enterprise-grade Local AI Data Orchestrator utilizing a cached Semantic Metadata Layer (ChromaDB) and a strict SQL Security Validator gate over a 5.0M row DuckDB pipeline.

# 🚛 Supply Chain & Logistics AI Data Orchestrator (CLI Edition)

An enterprise-grade, localized **Text-to-SQL & Dynamic EDA (Exploratory Data Analysis) Orchestration Engine** that allows non-technical business managers to query over 5.0M supply chain records using plain, natural language right from the terminal. 

The application bypasses complex cloud subscription fees by utilizing an incredibly fast local OLAP database and a cached semantic metadata layer, translating conversational intent directly into interactive inline charts and terminal metric frames.

---

## 🚀 Key Architectural Features

* **Metadata-Driven RAG (Semantic Layer Abstraction):** Utilizes a true Retrieval-Augmented Generation (RAG) architecture powered by ChromaDB to isolate raw database tables from the LLM. Instead of passing massive database dumps, the system dynamically fetches only the relevant localized JSON schemas and column dictionaries matching the user's natural language intent, completely eliminating schema hallucination vectors.
* **Autonomous Multi-Mode Router:** Programmatically analyzes user prompts under the hood via keyword matrix scanning to automatically switch execution paths between raw numerical extraction (**KPI Mode**) and automated visualization sandboxing (**EDA Mode**).
* **Isolated Script Execution Sandbox:** Utilizes Python's runtime environment (`exec()` with localized namespaces) to safely execute dynamically generated plotting pipelines without corrupting global application memory.
* **High-Speed Columnar Storage Integration:** Integrates seamlessly with local DuckDB database engines to run sub-second analytical aggregations across massive historical datasets.

---

## 🛠️ The Core Tech Stack

* **Orchestration Brain:** LangChain + Google Gemini 2.0 Flash (Optimized with `max_retries=5` for rate-limit protection)
* **Local Database Engine:** DuckDB (High-speed columnar OLAP workspace processing millions of rows)
* **Execution Interface:** VS Code Terminal Console Engine (CLI Interactive Loop)
* **Data & Visualization Canvas:** Pandas, NumPy, Matplotlib, Seaborn

---

## 📦 System Architecture Workflow

```text
[User Input Query] 
        │
        ▼
[Automated Router] ─── (Matches Keywords) ───► [EDA Mode / KPI Mode Selection]
        │
        ▼
[Schema / Metadata Extract] ─── (Fetches Context) ──► [Gemini 2.0 Flash Brain]
        │
        ▼
[In-Memory Data Sandbox Engine] ────────► [DuckDB OLAP Execution]
        │
        ▼
[Local CLI Console Output] ◄───────── [Dynamic Inline Plot & Pandas Metric View]
