🚚 Autonomous Logistics Intelligence System (ALIS)
Agentic Orchestration & Big Data Analytics (5.2M Records)
📌 Project Overview
ALIS is an end-to-end intelligence platform designed to navigate the "Digital Samsara" of modern supply chains. It leverages a custom-built Orchestrator-Executor framework to perform autonomous EDA and KPI monitoring across a high-volume (2.4 GB) logistics star schema.

The system transitions from raw data to actionable insight by separating the Physical Data Mapping (The Architect) from the Cognitive Reasoning (The Specialist).

🏗️ Technical Architecture
The core engine follows a two-pass "Omni-Protocol" design to ensure scalability and quota efficiency:

The Architect (Local Context): Scans the DuckDB metadata, performing range-checks on telemetry (GPS, IoT Temp) and schema mapping. It generates a "Semantic Essence" of the database.

The Specialist (Gemini-Flash): Uses the Semantic Essence to generate domain-specific SQL and Python visualization code (Plotly/Seaborn) without ever seeing the raw sensitive data.

The Executor: A sandboxed Python environment that renders interactive visuals and KPI summaries.

📊 Data Modeling & Scale
Volume: 5.2 Million records across 5 normalized tables.

Engine: DuckDB (In-process OLAP) for sub-second analytical performance.

Schema: Star Schema design consisting of:

fact_shipments: High-precision telemetry and fulfillment data.

dim_drivers: Behavior and fatigue monitoring metrics.

dim_vehicles: Fuel consumption and asset health tracking.

dim_routes: Geospatial risk and port congestion mapping.

dim_suppliers: Reliability and SLA performance scores.

🚩 Intelligence Layer (KPIs & Red Flags)
The system is pre-configured to monitor 21 KPIs and 19 Operational Red Flags, including:

Efficiency: OTIF% (On-Time In-Full), Route Density, and Lead Time Variance.

Risk: Critical Driver Fatigue (>85 score), Cold Chain Breaches, and Congestion Traps.

Finance: Cost Outliers (3x Mean) and Supplier Reliability Drops.

🛠️ Tech Stack
Language: Python 3.11+

Database: DuckDB, SQL Server (Logic Prep)

AI: Google Gemini API (LangChain/LLM-Orchestration)

Viz: Power BI (Advanced DAX), Plotly, Seaborn

Engineering: Git/GitHub, dbt (Planned), Prompt Engineering

🚀 Installation & Usage
Clone the Repo:

Bash
git clone https://github.com/YOUR_USERNAME/Logistics-AI-Orchestrator.git
Install Dependencies:

Bash
pip install -r requirements.txt
Data Access:

Due to GitHub size limits, the 2.4 GB .db file is hosted on [Insert Kaggle/Drive Link Here].

Place the database file in the /data folder.

Run the Orchestrator:

Python
python src/orchestrator.py
📅 Roadmap (2026 Phase)
[x] Phase 1: Multi-Brain Orchestrator Logic.

[x] Phase 2: Star Schema Normalization & DuckDB Optimization.

[ ] Phase 3: Power BI Advanced Dashboard (KPI subject areas).

[ ] Phase 4: dbt Integration for automated testing and documentation.

💡 How to use this file:
Replace YOUR_USERNAME and the Data Link with your actual details.

Add Images: Take a screenshot of your ERD and your code running. Put them in an /assets folder and link them in the README.

The "Why" Section: I included the "Digital Samsara" and "Orchestrator-Executor" terms because they match your CV's unique narrative.