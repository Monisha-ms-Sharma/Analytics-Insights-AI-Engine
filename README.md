# Insights-and-Analytics-Engine
https://insights-analytics-engine.lovable.app

# Insights & Analytics Engine

> **Data-Derived, Reliable Business Intelligence & Modeling**  
> Automated, client-side exploratory data analysis, diagnostic profiling, predictive modeling, and prescriptive decision simulation for one or multiple datasets.

---

## 1. Why This Application Was Built

Modern decision-makers face a persistent dilemma when attempting to make sense of their data:

* **Complex Legacy Tools:** Traditional Business Intelligence (BI), statistical platforms, and data science notebooks require specialized knowledge of SQL, Python, R, schema normalization, and advanced statistical theory. Non-technical leaders, operators, and domain experts are frequently locked out or bottlenecked waiting for data engineering teams.
* **Generative AI Risks:** Generic Large Language Model (LLM) prompts often suffer from calculation hallucinations, invent imaginary financial returns or costs, and conflate statistical correlation with real-world causation.
* **Data Privacy Concerns:** Uploading proprietary, confidential spreadsheets or operational databases to cloud-based analytics providers exposes sensitive customer, operational, and financial records.
**Insights & Analytics Engine** bridges this divide. It provides an automated, evidence-backed, client-side data analytics platform that guides users from raw files to defensible business decisions—without requiring a technical or analytical background.

---

## 2. What This Application Does

The application automatically ingests, profiles, and analyzes one or multiple datasets, translating raw numbers into an end-to-end analytical framework covering the four classical pillars of data analytics:

```text
+--------------------------------------------------------------------------+
|                       INSIGHTS & ANALYTICS ENGINE                        |
+--------------------------------------------------------------------------+
|  [ Ingest ] CSV, TSV, Excel (.xlsx/.xls), JSON, GeoJSON, NDJSON, ZIP     |
+--------------------------------------------------------------------------+
|  [ Worker ] Client-Side Web Worker (Isolated parsing & computation)      |
+--------------------------------------------------------------------------+
                                     |
         +---------------------------+---------------------------+
         |                           |                           |
         v                           v                           v
+-------------------+       +-------------------+       +------------------+
|    Descriptive    |       |    Diagnostic     |       |    Predictive    |
| "What happened?"  |  ==>  | "Why did it occur"|  ==>  | "What comes next"|
| Trends, Segments, |       | Drivers, Quartiles|       | Forecasts, MAPE, |
|   Aggregations    |       |   Correlations    |       | Leakage-Checked  |
+-------------------+       +-------------------+       +------------------+
                                                                 |
                                                                 v
                                                        +------------------+
                                                        |   Prescriptive   |
                                                        | "What to do now" |
                                                        | Prioritized Recs |
                                                        | What-if Scenario |
                                                        +------------------+
                                                                 |
                                                                 v
                                                        +------------------+
                                                        |  Executive PDF   |
                                                        | Auditable Report |
                                                        +------------------+

## 3. What the Engine Is Capable Of
* **Automated Data Profiling & Quality Auditing**
* Zero-Configuration Type & Role Inference: Distinguishes continuous metrics, temporal dates, categorical dimensions, identifiers, and flags without manual configuration.
* Data Health Verification: Inspects missing-value rates, duplicate row counts, zero-variance columns, extreme outliers, and distribution skewness.
* Target & Date Candidate Detection: Automatically detects target KPIs (revenue, profit, churn, quantity) and primary time series anchors.
* Transparent Column Dictionary: Explains every column’s business meaning in plain English.
* Transparently distinguishes between supported facts and inferred interpretations.
* Allows users to enter plain-English business clarifications to eliminate ambiguity before report generation.

* **Multi-Table Relational Modeling**
Analyzes shared column key overlap across multiple tables.
Provides a safe Dimensional Enrichment (Lookup) engine that strictly enforces key uniqueness on lookup tables, rejecting non-unique keys to guarantee against row-multiplication errors.

* **The Four Analytics Disciplines**
1. Descriptive: Automated time-grain aggregation (sum, mean, rate), trendlines, segment distributions, and Pareto concentrations.
2. Diagnostic: Correlation matrices with p-values, driver importance ranking (R2, Pearson r, η2), top-vs-bottom quartile contrasts, and z-score anomaly detection.
3. Predictive: Multi-algorithm time-series forecasting (Holt-Winters, seasonal, linear trend) validated against a 20% empirical holdout with Mean Absolute Percentage Error (MAPE) scores, plus regression and classification modeling with automated data-leakage guards.
4. Prescriptive: Generates prioritized, evidence-backed recommendations tied directly to quantified data points, paired with interactive what-if simulation sliders.

## 4. Key Features & How to Use It
* Feature: Multi-File & ZIP Ingestion: Accepts single/bulk files or recursive ZIP archives (.csv, .tsv, .xlsx, .xls, .json, .geojson, .ndjson, .zip).	
  How to Use: Drag and drop files onto the upload zone or click Load Sample Retail Data for immediate exploration.
* Feature:	9-Tab Analysis Workspace: Dedicated screens for Overview, Descriptive, Diagnostic, Predictive, Prescriptive, Column Dictionary, Quality, Relationships, and Original Data.	
  How to Use: Click any tab header to switch perspectives without losing your analysis state.
* Feature:	KPI & Date Targeting: Dynamic focus selector that updates calculations across all diagnostic, predictive, and prescriptive modules.	
  How to Use: Use the top toolbar dropdowns to switch the target metric or primary date column.
* Feature:	Interactive Visualizations: Responsive charts for trendlines, segment rankings, distributions, scatter plots, and forecast bands.	
  How to Use: Hover over data points to inspect exact values, standard errors, and confidence intervals.
* Feature: What-If Scenario Simulator: Interactively adjust key driver inputs to simulate potential KPI outcomes.
  How to Use: Navigate to the Prescriptive tab, select a driver, and adjust the scenario slider.
* Feature: Executive PDF Export: Generates an auditable, multi-page PDF report matching on-screen calculations.	
  How to Use: Click the Export PDF Report button in the header; downloads locally in seconds.
  
## 5. Who This Is For
* Business Owners & Operators: Make reliable, data-backed operational, pricing, and inventory decisions if you are without a dedicated data analyst on staff.
* Product & Marketing Managers: Rapidly audit campaign performance, user cohorts, and conversion drivers directly from raw CSV exports.
* Operations & Financial Analysts: Automate routine exploratory profiling, anomaly scans, and baseline forecasts.
* Consultants & Advisors: Ingest client data archives and produce executive-ready, defensible diagnostic reports in minutes.
* Non-Technical Professionals: Anyone with a spreadsheet who needs reliable business clarity rather than statistical jargon.

## 6. How It Benefits Users
* Plain-English Explanations: Statistical metrics (p-values, skewness, variance) are translated into clear, actionable business takeaways.
* Strict Evidence Standard: Never invents unobserved revenue, costs, or facts. Hypotheses and predictions are explicitly labeled as such.
* Session Privacy by Design: 100% of parsing and model computation runs in a browser Web Worker. Data stays on your device and is not saved to external servers.
* Rapid Time-to-Insight: Replaces hours of manual spreadsheet formula debugging and charting with automated multi-dimensional analysis.
* Auditability: UI calculations, data dictionaries, and PDF exports consume the identical deterministic calculation pipeline.

## 7. Limitations & Boundaries
To maintain credibility and analytical rigor, the application operates under explicit boundaries:
* Correlation Is Not Causation: Driver analysis reveals mathematical associations (r, η2), not proven causal links. Real-world business causality requires controlled experimentation (A/B testing) or domain validation.
* Browser Memory & Row Caps: Ingestion runs within client-side browser memory. Files with over 200,000 rows undergo systematic sampling to ensure performance without browser crashes (fully disclosed in the data quality audit).
* Historical Continuity Assumption: Forecasts assume historical patterns persist. Unexpected external shocks, regulatory shifts, or variables not present in the dataset cannot be anticipated.
* Structured Tabular Data Focus: Optimized for structured tables, spreadsheets, and nested JSON. Unstructured media (PDF documents, audio, raw images) or proprietary formats requiring heavy native binaries (e.g., Parquet without WebAssembly bindings) are bypassed.
* Session-Scoped Storage: By default, datasets exist only in the active browser tab session for privacy and are cleared on page reload unless exported to PDF.

## 8. Upcoming Enhancements
* Visual Star-Schema Canvas: Interactive drag-and-drop entity-relationship canvas for connecting multiple fact and dimension tables.
* Wasm / DuckDB In-Browser Engine: WebAssembly-powered streaming execution allowing local multi-million-row querying and direct Parquet file ingestion.
* Multivariate Sensitivity Matrices: Simultaneous multi-variable scenario simulation and target-seeking goal solvers.
* Data Drift & Period Comparison: Side-by-side comparison of historical datasets to track pipeline changes and metric migration over time.
* Optional Collaborative Workspaces: Secure, opt-in cloud project synchronization and scheduled team report distributions.
