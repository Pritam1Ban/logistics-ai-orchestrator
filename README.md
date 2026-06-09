# logistics-ai-orchestrator
An enterprise-grade Local AI Data Orchestrator utilizing a cached Semantic Metadata Layer (ChromaDB) and a strict SQL Security Validator gate over a 5.0M row DuckDB pipeline.


# 🚛 Supply Chain & Logistics AI Data Orchestrator

An enterprise-grade, localized **Text-to-SQL & Dynamic EDA (Exploratory Data Analysis) Orchestration Engine** that allows non-technical business managers to query over 5.0M supply chain records using plain, natural language. 

The application bypasses complex cloud subscription fees by utilizing an incredibly fast local OLAP database and a cached semantic metadata layer, translating conversational intent directly into interactive browser charts and downloadable Excel reports.

---

## 🚀 Key Architectural Features

* **Semantic Layer Abstraction (Metadata-Driven RAG):** Isolates raw, sensitive database tables from the LLM. The agent queries a highly optimized, localized JSON/DataFrame schema context to eliminate hallucination vectors.
* **Autonomous Multi-Mode Router:** Programmatically analyzes user prompts under the hood to automatically switch execution execution paths between raw numerical extraction (**KPI Mode**) and automated script sandboxing (**EDA Mode**).
* **Strict SQL Security Guardrail:** Intercepts generated query tokens via a local Query Validator gate, explicitly blocking malicious mutation commands (`DROP`, `DELETE`, `ALTER`) to guarantee a 100% read-only local execution environment.
* **In-Memory Data Delivery:** Utilizes Python byte stream pipelines (`io.BytesIO`) to instantly generate clean Excel extracts directly inside memory blocks, completely eliminating physical hard disk I/O strain.

---

## 🛠️ The Core Tech Stack

* **Orchestration Brain:** LangChain + Google Gemini 2.0 Flash (Optimized with `max_retries=5` for rate-limit protection)
* **Local Database Engine:** DuckDB (High-speed columnar OLAP workspace processing millions of indices)
* **Frontend Presentation Platform:** Streamlit Web UI Framework
* **Data & Visualization Canvas:** Pandas, NumPy, Plotly Express, Seaborn, Matplotlib

---

## 📦 System Architecture Workflow

```text
[User Input Query] 
        │
        ▼
[Automated Router] ─── (Matches Keywords) ───► [EDA Mode / KPI Mode Selection]
        │
        ▼
[ChromaDB / Schema Extract] ─── (Fetches Context) ──► [Gemini 2.0 Flash Brain]
        │
        ▼
[SQL Security Validator Gate] ─── (Blocks Injection) ──► [DuckDB In-Memory Execution]
        │
        ▼
[Interactive Web Canvas] ◄─── (Renders Layout) ─── [Dynamic Plotly Chart & Excel Extract]
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
   Create a hidden folder path or file named `LLM_API.env` containing your Google GenAI credential matrix:
   ```text
   GOOGLE_API_KEY="your_free_google_gemini_api_key_here"
   ```

3. **Install the required technical library bundle:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the interactive Streamlit Web Server:**
   ```bash
   streamlit run app.py
   ```
