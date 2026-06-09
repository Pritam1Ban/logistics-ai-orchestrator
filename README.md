# logistics-ai-orchestrator
An enterprise-grade Local AI Data Orchestrator utilizing a cached Semantic Metadata Layer (ChromaDB) and a strict SQL Security Validator gate over a 5.0M row DuckDB pipeline.

# 🚛 Supply Chain & Logistics AI Data Orchestrator (CLI Edition)

An enterprise-grade, localized **Text-to-SQL & Dynamic EDA (Exploratory Data Analysis) Orchestration Engine** that allows non-technical business managers to query over 5.0M supply chain records using plain, natural language right from the terminal. 

The application bypasses complex cloud subscription fees by utilizing an incredibly fast local OLAP database and a cached semantic metadata layer, translating conversational intent directly into interactive inline charts and terminal metric frames.

---

## 🚀 Key Architectural Features

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
