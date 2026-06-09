# logistics-ai-orchestrator
An enterprise-grade Local AI Data Orchestrator utilizing a cached Semantic Metadata Layer (ChromaDB) and a strict SQL Security Validator gate over a 5.0M row DuckDB pipeline.

# 🚛 Supply Chain & Logistics AI Data Orchestrator (CLI Edition)

An enterprise-grade, localized **Text-to-SQL & Dynamic EDA (Exploratory Data Analysis) Orchestration Engine** that allows non-technical business managers to query over 5.0M supply chain records using plain, natural language right from the terminal. 

The application bypasses complex cloud subscription fees by utilizing an incredibly fast local OLAP database and a cached semantic metadata layer, translating conversational intent directly into interactive inline charts and terminal metric frames.

---

## 🚀 Key Architectural Features

* **Metadata-Driven RAG (Semantic Layer Abstraction):** Utilizes a true Retrieval-Augmented Generation (RAG) architecture powered by ChromaDB to isolate raw database tables from the LLM. Instead of passing massive database dumps, the system dynamically fetches only the relevant localized JSON schemas and column dictionaries matching the user's natural language intent, completely eliminating schema hallucination vectors.
* **Semantic Layer Abstraction (Metadata-Driven RAG):** Isolates raw, sensitive database tables from the LLM. The agent queries a highly optimized, localized JSON schema context to eliminate hallucination vectors.
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
```

---

## ⚙️ Local Sandbox Setup & Installation

To run this data engine within your local workspace environment, follow the steps below:

1. **Clone the project repository:**
   ```bash
   git clone https://github.com
   cd logistics-ai-orchestrator
   ```

2. **Configure your localized environment file:**
   Create an environment file named `LLM_API.env` inside your designated configuration folder containing your Google GenAI credentials:
   ```text
   GOOGLE_API_KEY="your_free_google_gemini_api_key_here"
   ```

3. **Install the required technical library bundle:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the interactive Terminal Agent Loop:**
   ```bash
   python agent_cli.py
   ```

   ---

## 🛑 Current Limitations & Future Engineering Roadmap

This architecture is currently a fully functional production prototype optimized for single-node local execution. The following structural boundaries have been intentionally mapped to be resolved in the next development phase:

1. **Enterprise Query Guardrails (Security Phase):**
   * *Current Status:* Queries run on safe read-only loops due to database-level constraints.
   * *Next Step:* Implementing an explicit rule-based abstract syntax tree (AST) parser or regex query validator gate directly into the pipeline to intercept and drop raw SQL mutation tokens (`DROP`, `DELETE`, `ALTER`) before they hit the compiler layer.

2. **In-Memory Data Export Arrays (Delivery Phase):**
   * *Current Status:* Data metrics are currently output directly as standard terminal Pandas string matrices.
   * *Next Step:* Engineering an in-memory binary stream pipe utilizing `io.BytesIO` and `openpyxl` to allow end-users to instantly package extracted data frames into formatted Excel (`.xlsx`) matrices without hitting local hard drive disk write operations.

3. **Web Interface Migration (Presentation Phase):**
   * *Current Status:* The engine runs within a continuous interactive CLI loop inside the VS Code terminal.
   * *Next Step:* Porting the runtime execution loop into an interactive browser dashboard using the **Streamlit web framework**, mapping dynamic multi-mode router outputs natively to reactive Plotly Express visual canvases.

4. **API Quota & Scale Hardening (Orchestration Phase):**
   * *Current Status:* Aggressive sequential text operations face Google Free Tier Requests-Per-Minute (RPM) throttles.
   * *Next Step:* Implementing query result caching structures via `@st.cache_data` paired with asynchronous batch execution handlers to minimize outbound API tokens during intense multi-turn business deep-dives.

