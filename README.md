# Analytics & Insights - Engine
Evidence-based business intelligence from your own data, written in plain English.
**Live Application:** https://ai-engine.app/  

<img width="1920" height="973" alt="Analytics   Insights - AI Engine" src="https://github.com/user-attachments/assets/96522dbb-d8c8-4d3d-8fc8-e855d8a53a77" />

---

## 1. Why This Application Was Built

Most organizations have plenty of data but struggle to turn it into reliable decisions:

* **Traditional analytics tools are complex:** They often require specialized technical skills, programming knowledge, or a dedicated data team.
* **Generic AI tools can hallucinate:** They may present plausible-sounding assertions that the underlying numbers do not substantiate.
* **Data privacy is non-negotiable:** Organizations cannot risk uploading confidential business files to external third-party servers.

**Analytics & Insights - Engine** solves this. Anyone—with or without a data science background—can drop in data and immediately receive trustworthy, evidence-backed insights. Every calculation runs locally inside the browser Web Worker, and every finding is derived deterministically from the uploaded data.

---

## 2. What This Application Does

The application automatically parses, profiles, models, and analyzes single or multi-table datasets, answering four primary questions:

1. **What happened?** *(Descriptive Analytics)*
2. **Why did it happen?** *(Diagnostic Analytics)*
3. **What could happen next?** *(Predictive Analytics)*
4. **What actions should we consider?** *(Prescriptive Analytics)*

### Architecture & Analytical Flow

```text
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                               DATA INGESTION & PARSING                                 │
│  CSV · Excel · Parquet · JSON · Arrow · XML · Text · Word · PDF · SQL Dumps · ZIP      │
│  (100% in-browser WebAssembly & Web Worker · Zero cloud upload · Streams large files)  │
└──────────────────────────────────────────┬─────────────────────────────────────────────┘
                                           │
                                           ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DATA PROFILING & AUTOMATIC HYGIENE                              │
│  • Column Type & Role Inference          • 0–100 Data Quality Health Score             │
│  • Plain-English Column Dictionary       • 27 Industry KPI Sector Classifiers          │
└──────────────────────────────────────────┬─────────────────────────────────────────────┘
                                           │
                                           ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                       MULTI-TABLE MODELING & DIY TOOLS                                 │
│  • Auto Generated Data Models (star-schema combinations with row-preservation checks)  │
│  • Interactive Visual Canvas & Menus (contextual relationship safety validation)       │
│  • Data Transformation Engine (18 operations: cleaning, reshaping, feature engineering)│
└──────────────────────────────────────────┬─────────────────────────────────────────────┘
                                           │
                                           ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                               ANALYTICAL ENGINE (14 LENSES)                            │
│ ┌────────────────────────────────────────────────────────────────────────────────────┐ │
│ │ CORE BUSINESS LENSES                                                               │ │
│ │ • Descriptive (Distributions, KPIs)      • Diagnostic (Key Drivers, Variance ANOVA)│ │
│ │ • Predictive (Regression, Scenarios)     • Prescriptive (Optimization Frontiers)   │ │
│ └────────────────────────────────────────────────────────────────────────────────────┘ │
│ ┌────────────────────────────────────────────────────────────────────────────────────┐ │
│ │ ADVANCED STATISTICAL & CAUSAL LENSES                                               │ │
│ │ • Time Series (Calendar Trends, Holdout) • Inferential (Hypothesis Testing)        │ │
│ │ • Survival Analysis (Kaplan–Meier, RMST) • Causal (Treatment Effects, Confounders) │ │
│ │ • Mechanistic (Path & Mediator Analysis) • Quant + Qual (Group Disproportions)     │ │
│ │ • Text & Sentiment (Trained In-Browser RoBERTa Transformer & Polarities)           │ │
│ └────────────────────────────────────────────────────────────────────────────────────┘ │
│ ┌────────────────────────────────────────────────────────────────────────────────────┐ │
│ │ MACHINE LEARNING SUITE                                                             │ │
│ │ • Supervised (Ridge, Logistic, Decision Trees, Random Forest, Boosted Trees, SVM)  │ │
│ │ • Unsupervised (K-Means, Hierarchical, PCA, Association Rules)                     │ │
│ │ • Offline Reinforcement (Q-Learning)   • Semi-Supervised    • Self-Supervised      │ │
│ └────────────────────────────────────────────────────────────────────────────────────┘ │
└──────────────────────────────────────────┬─────────────────────────────────────────────┘
                                           │
                                           ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                             PRESENTATION & DELIVERABLES                                │
│  • Executive Overview & KPIs             • Ask Your Data (Privacy-Preserving AI)       │
│  • Step-by-Step Guided Walkthrough       • Zero-Row Shared Results (.json)             │
│  • Interactive Scenario Simulators       • Custom Executive PDF Report Builder         │
│  • Local Browser Workspaces (IndexedDB)  • White-Label Customized Results              │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. What This Application Is Capable Of

### Supported File Types

| Category | Supported Formats | Processing Method |
| :--- | :--- | :--- |
| **Delimited Text** | CSV, TSV, TXT, PSV, DAT, TAB | Chunked progressive streaming; zero sampling |
| **Spreadsheets** | Excel (`.xlsx`, `.xls`, `.xlsm`, `.xlsb`), OpenDocument (`.ods`) | In-browser parsing; preserves all sheets |
| **Columnar & Big Data** | Parquet, Apache Arrow, Feather | Range-based reads without loading entire file |
| **Semi-Structured** | JSON, JSONL, NDJSON, GeoJSON, XML | Hierarchical flattening and type discovery |
| **Documents** | Microsoft Word (`.docx`), PDF tables | Extracts structured tables; isolates prose |
| **Databases** | Raw `.sql` dumps, SQLite databases | Sandboxed in-browser SQLite WebAssembly engine |
| **Compressed Archives** | ZIP (nested directories), GZIP (`.gz`) | Unpacks and mounts tables in memory |
| **Cloud Storage Links** | Google Drive, OneDrive, Dropbox, SharePoint | Direct stream to browser memory; zero cloud retention |

* Upload a single file or multiple related tables simultaneously.
* **Original data is never modified:** Transformations and joins create separate derived tables.

---

### Large & Big Data Handling

* **Streaming Engine:** CSV and text files over 50 MB are parsed in progressive chunks; Parquet files are read in block ranges to protect client memory.
* **Full-Dataset Guarantee (Zero Sampling):** Datasets are processed in full up to an 80-million-cell capacity. If a dataset exceeds memory or capacity thresholds, it is safely rejected with transparent row/cell counts and splitting guidance—it is never sampled.
* **Responsive Background Execution:** Computations run in a dedicated Web Worker so the browser interface remains fluid.

---

### Data Understanding & Governance

* **Automatic Column Profiling:** Identifies column types, semantic roles, cardinality, null counts, and business meanings.
* **Interactive Column Dictionary:** Classifies definitions as data-supported or inferred, with editable notes and user-defined formulas.
* **27 Sector KPI Packages:** Detects domain contexts (Healthcare, Finance, SaaS, Retail, Logistics, Aviation, Cybersecurity, Engineering, Manufacturing, and more) and computes industry-standard ratios only when verified columns exist.
* **14 Selectable Synthetic Sample Datasets:** Ready-to-explore multi-table sample models across major industry domains.

---

### Multi-Table Modeling (DIY Tools)

* **Star & Snowflake Schemas:** Choose a central fact table and connect lookup dimension tables outward.
* **Safety Verification:** Validates primary/foreign key overlap and cardinality prior to join creation. Prevents invalid relationships that duplicate rows.
* **Auto Generated Models:** Enumerates row-preserving connection paths automatically with one-click build and analysis.

---

### Core Analytical Lenses

| # | Lens | Primary Question | Core Capabilities |
| :-: | :--- | :--- | :--- |
| **1** | **Descriptive** | *What happened?* | Mean, median, mode, percentages, KPI cards, trend trajectories, distributions, segmentation breakdowns. |
| **2** | **Diagnostic** | *Why did it happen?* | Pearson/Spearman correlation matrices, ANOVA variance decomposition, key driver rankings, anomaly flags. |
| **3** | **Predictive** | *What is likely next?* | Time-series forecasting (Holt-Winters, seasonal, naive), linear/tree regressions, out-of-fold validation, leakage protection. |
| **4** | **Prescriptive** | *What should we do?* | Prioritized recommendation matrices, trade-off efficiency curves, and interactive scenario simulators. |

---

### Specialized & Advanced Analytics

| # | Lens | Scope & Methods |
| :-: | :--- | :--- |
| **5** | **Time Series** | Calendar aggregation, linear direction, trailing averages, detrended autocorrelation, and seasonal holdout evaluation. |
| **6** | **Inferential** | Two-sample t-tests, Mann-Whitney U, Chi-Square independence, multiple testing adjustments (Benjamini-Hochberg). |
| **7** | **Survival Analysis** | Full-record Kaplan–Meier curves, right censoring, Greenwood intervals, median survival, RMST, and log-rank tests. |
| **8** | **Causal** | Propensity score matching, Average Treatment Effect (ATE), confounding controls, and observational limit disclosures. |
| **9** | **Mechanistic** | Structural equation modeling, path coefficient decomposition, mediator effects, and formulaic dependencies. |
| **10** | **Quant + Qual** | Share of voice vs. share of impact, categorical volume vs. outcome contribution matrices. |
| **11** | **Text & Sentiment** | In-browser quantized RoBERTa transformer, polarity classification, TF-IDF top terms, and sentiment outcome correlations. |

---

### Complete Machine Learning Suite

| Family | Algorithms & Implementations |
| :--- | :--- |
| **Supervised Learning** | Ridge Regression, Logistic Regression, Decision Trees, Random Forests, Bagged Trees, Gradient Boosted Trees, Linear SVM/SVR, k-Nearest Neighbors, Gaussian Naive Bayes (validated on held-out test splits). |
| **Unsupervised Learning** | K-Means clustering, Hierarchical Agglomerative clustering, Principal Component Analysis (PCA), Apriori Association Rules. |
| **Offline Reinforcement** | Tabular Q-learning policy estimation on observational logs; live-environment dependencies are noted as non-applicable. |
| **Semi-Supervised** | Self-training pseudo-labeling wrapper for sparse labeled datasets. |
| **Self-Supervised** | Masked-feature autoencoding reconstruction. |

---

## 4. Key Features & How to Use Them

| Feature | Description | Where to Access |
| :--- | :--- | :--- |
| **Upload Zone** | Accepts single/multi-file uploads, archives, and cloud links | Homepage start screen |
| **Overview Dashboard** | Executive summary, KPIs, quality rating, and top findings | First tab in Data Analysis |
| **Guided Walkthrough** | Plain-English narrative tour walking through your results | Data Analysis → Guided Walkthrough |
| **Auto Generated Models** | Pre-computed, row-preserving multi-table combinations | Data Analysis → Auto Generated Data Models |
| **Ask Your Data** | Natural-language query assistant backed by verified statistics | Data Analysis → Ask Your Data |
| **Scenario Simulator** | Interactive slider-based what-if forecasting | Data Analysis → Predictive / Prescriptive |
| **DIY Columns** | Custom user-defined formulas and column derivations | DIY Tools → DIY Columns |
| **DIY Transformations** | 18 cleaning, reshaping, and feature engineering operations | DIY Tools → DIY Transformations |
| **DIY Data Models** | Visual canvas and menu builder for star-schema joins | DIY Tools → DIY Data Models |
| **DIY Comparisons** | Compare completed profiles and metrics across uploads | DIY Tools → DIY Comparisons |
| **DIY Bookmarks** | Save and recall specific charts and insights locally | DIY Tools → DIY Bookmarks |
| **DIY Saved Workspaces** | Preserves files, models, and definitions locally in IndexedDB | DIY Tools → DIY Saved Workspaces |
| **Customize Results** | Organization white-labeling, custom branding, and sources | Workspace top bar → Customize Results |
| **PDF Report Builder** | Customizable executive reporting with chart selection | Top action bar → *Download report* |
| **Share Results** | Exports zero-row summary package (`.json`) for team review | Top action bar → *Share results* |
| **Workspace Reset** | Clears active workspace and returns cleanly to upload screen | Top of sidebar → *Reset* |

---

## 5. Plans & Access

| Tier | Price | Scope & Entitlements |
| :--- | :--- | :--- |
| **Early Access** | **Free** | **3 full dataset analyses** per signed-in user or device (unlocks all 14 lenses, ML, PDF reports, and DIY tools). |
| **Single Data File Analysis** | **$99.99** one-time | Unlocks full analysis and PDF reporting for a single uploaded table. |
| **Full Data Set Analysis** | **$199.99** one-time | Unlocks full analysis and PDF reporting for multi-table datasets and star models. |
| **Monthly Subscription** | **$99.99 / month** | Unlimited analyses, unlimited PDF reports, full ML suite, and Ask Your Data / AI Insights. |
| **Yearly Subscription** | **$999.99 / year** | Unlimited annual access (save ~$199.89 vs. monthly) with all features included. |

* **Free Notice:** Free analyses are limited to one account per user or device. Ask Your Data & Generate AI Insights require a paid subscription.
* **Always Free:** Overview, Guided Walkthrough, Descriptive Analytics, Data Quality, Column Dictionary, and synthetic sample explorations require no payment.
* **Merchant of Record:** Transactions are processed securely by Paddle. Customers may request a full refund within 14 days of the order date for monthly/yearly subscriptions and one-time purchases.

---

## 6. Who This Is For

* **Business Owners & Executives:** Make strategic decisions grounded in hard evidence without waiting on analyst backlogs.
* **Product, Marketing, & Operations Teams:** Identify key growth drivers, evaluate campaign performance, and simulate outcomes.
* **Finance & Strategy Professionals:** Run scenario analyses, budget impact forecasts, and variance decompositions.
* **Analysts & Data Scientists:** Accelerate initial exploratory data analysis (EDA), data cleaning, and model benchmarking.
* **Privacy-Conscious Organizations:** Analyze confidential internal data without sending raw records across the public internet.

---

## 7. How It Benefits You

* **Plain English First:** Complex mathematical findings are translated into clear, actionable executive summaries.
* **Deterministic Reliability:** Visualizations, statistical tables, and exported PDF reports consume identical worker outputs.
* **Uncompromising Privacy:** Files remain inside your browser sandbox. The AI assistant receives only aggregate summaries, never raw data rows.
* **Speed & Interactivity:** Background Web Worker execution keeps charts, filtering, and model generation instant and responsive.
* **Scientific Integrity:** The engine explicitly separates correlation from causation and never fabricates financial projections.
* **Zero Sampling:** Full datasets are computed directly up to capacity; data is never thinned out or approximated.

---

## 8. Limitations & Disclosures

* **Causal Observational Limits:** Establishing true causality requires experimental randomized control data; observational causal findings represent statistical estimations.
* **Browser Memory Boundaries:** Non-streaming formats (Excel, JSON, XML, SQLite) load in browser memory; practical limits reflect device RAM.
* **Capacity Limits:** Tables exceeding 80 million cells are rejected with split guidance, never sampled.
* **Time-Series Horizon:** Predictive models require historical depth; short series produce wider confidence intervals.
* **Local Workspaces:** Stored in your local browser’s IndexedDB; workspaces do not sync across distinct physical devices unless exported via *Share Results*.
* **Clinical Data Notice:** Local execution alone is not HIPAA compliance or a Business Associate Agreement; survival and clinical insights are not medical advice.

---
