# Analytics & Insights - AI Engine
**Evidence-based business intelligence from your own data, written in plain English.**
https://analytics-insights-engine.lovable.app/

---

## 1. Why This Application Was Built

Most organizations have plenty of data but struggle to turn it into reliable decisions:

- **Traditional analytics tools are complex.** They often need technical skills, coding, or a dedicated analyst.
- **Generic AI tools can make things up.** They may produce confident answers that the data does not support.
- **Privacy matters.** Many people do not want to upload sensitive business files to outside servers.

Insights & Analytics Engine was built to fix this. Anyone, with or without an analytics background, can upload their data and get trustworthy insights about business events and outcomes. Every insight is calculated directly from the uploaded data.

---

## 2. What This Application Does

The app automatically models and analyzes one or more uploaded datasets. It then explains:

- **What happened**
- **Why it may have happened**
- **What could happen next**
- **What actions to consider**

```text
Upload files (CSV, Excel, Text, Parquet, JSON, XML, ZIP, ...)
        |
        v
Read & preserve originals (large files read in pieces)
        |
        v
Profile columns & data quality
        |
        v
Data model canvas: connect tables visually  -->  Combined model
        |
        v
+-----------------------------------------------------------+
|  Core analysis                                            |
|  Descriptive | Diagnostic | Predictive | Prescriptive     |
+-----------------------------------------------------------+
|  Additional analysis                                      |
|  Inferential | Causal | Mechanistic |                     |
|  Quantitative + Qualitative | Text & Sentiment            |
+-----------------------------------------------------------+
        |
        v
Interactive charts  |  Ask your data (AI)  |  Guided walkthrough
        |
        v
Downloadable PDF report (all sections + charts)
```

---

## 3. What This Application Is Capable Of

### Supported file types
| Category | Formats |
|----------|---------|
| Delimited text | CSV, TSV, TXT, PSV, DAT |
| Spreadsheets | Excel (XLSX, XLS, XLSM, XLSB), OpenDocument (ODS) |
| Big data / columnar | Parquet, Arrow, Feather |
| Structured data | JSON, JSONL, NDJSON, GeoJSON, XML |
| Databases | SQLite files (every table is loaded) |
| Compressed | ZIP folders (including nested folders), GZIP files |

- Upload a **single file or many files** at once
- Original data is never changed

### Large and big data files
- CSV and text files over 50 MB are **read in pieces**, and Parquet files are read in sections, so they don't need to fit in memory all at once. A 2.6-million-row CSV has been tested successfully.
- Tables over 200,000 rows are analyzed from a **reproducible sample that covers the whole file**. The app always tells you when it uses a sample.

### Data understanding
- Automatic column profiling: type, role, statistics, and meaning in plain English
- A column dictionary that labels each meaning as *supported by the data* or *inferred*, with space to add your own explanation
- Automatic detection of shared fields between tables

### Data model canvas (multiple tables)
- Visual star-schema builder: choose a main table and drag the other tables around it
- Connect tables by clicking a matching field in each, or with one click on a suggested match
- Each connection is checked before it is used. It shows the match rate and blocks connections that would duplicate records.
- **Build model & analyze** combines the connected tables into a new table for analysis. Your original tables stay unchanged.

### Core analysis
| # | Type | Question it answers | What it includes |
|---|------|---------------------|------------------|
| 1 | **Descriptive** | What happened? | Mean, median, mode, percentages, KPIs, trends, segments, distributions, dashboards |
| 2 | **Diagnostic** | Why did it happen? | Correlations with significance, key drivers, high vs. low comparisons, contribution analysis, anomaly detection |
| 3 | **Predictive** | What is likely next? | Time-series forecasting (naive, linear, Holt, seasonal) with holdout validation; regression and classification models; leakage protection |
| 4 | **Prescriptive** | What should we do? | Prioritized, evidence-backed recommendations; interactive what-if scenario simulator |

### Additional analysis
| # | Type | What it does |
|---|------|--------------|
| 5 | **Inferential** | Confidence intervals, t-tests, chi-square tests, and correlation significance, with correction for multiple tests |
| 6 | **Causal** | Compares experiment groups when the data has them (e.g. treatment vs. control). Otherwise gives regression-adjusted effects and clearly states the limits of observational data |
| 7 | **Mechanistic** | Finds exact arithmetic relationships (e.g. revenue = price × units), contribution shares, and elasticities |
| 8 | **Quantitative + Qualitative** | Combines numeric outcomes with categories: each group's share of records vs. its share of the outcome |
| 9 | **Text & Sentiment** | Finds themes, top terms, phrases, and positive/negative/neutral sentiment in free-text columns, plus how outcomes differ by sentiment, with example quotes |

---

## 4. Key Features and How to Use Them

| Feature | What it does | How to use it |
|---------|--------------|---------------|
| **Upload area** | Accepts one or many files and ZIP folders by drag-and-drop | Drop files in, or click **Try sample data** |
| **Overview** | Headline metrics, charts, and ranked findings | Opens automatically after upload |
| **Guided walkthrough** | Step-by-step tour from data quality through descriptive, diagnostic, predictive, and prescriptive analysis, using your live results | Open **Guided walkthrough** and press **Next** |
| **Ask your data** | Ask questions in plain English. AI explains the relevant findings with supporting figures and caveats | Type a question or pick a suggested one |
| **Analysis controls** | Choose the outcome to study, the time field, and filters | Use the selectors at the top of the workspace |
| **Analysis tabs** | One tab for each of the nine analysis types | Click any tab in the sidebar |
| **Scenario simulator** | Tests "what if" changes to key factors | Predictive tab → adjust a factor |
| **Data model canvas** | Connect multiple tables visually before analysis | **Relationships** → choose the main table → click matching fields → **Build model & analyze** |
| **Column dictionary** | Plain-English meaning of every column | Search, expand, and add clarifications |
| **Data quality dashboard** | Summary of issues rated **High / Medium / Low**, with recommended next steps | Open **Data quality** |
| **Original data** | View your untouched data, page by page | Open **Original data** |
| **PDF report** | Saves a formatted report file with every analysis section (including Inferential, Causal, and Mechanistic) plus charts | Click **Download report** |

---

## 5. Who This Is For

- Business owners and managers
- Product, marketing, sales, and operations teams
- Finance and strategy professionals
- Data analysts and consultants who want a fast, reliable first pass
- Researchers, educators, and students
- **Anyone who needs answers from data without coding**

The app works across industries, including retail, finance, healthcare, SaaS, logistics, and manufacturing.

---

## 6. How It Benefits Users

- **Plain English:** results are explained without jargon.
- **Reliable:** every finding is calculated from your data. Facts, relationships, hypotheses, predictions, and recommendations are labeled separately.
- **Honest:** correlation is never presented as causation, and financial gains or costs are never invented.
- **Private:** files are processed in your browser and are not saved anywhere. The AI assistant only receives calculated summaries, never your raw rows.
- **Works with real-world data:** handles many file types, multiple related tables, and very large files.
- **Fast:** analysis runs in the background, so the screen stays responsive.
- **Consistent:** the screen and the PDF report use the same calculations, so the figures always match.
- **Transparent:** sampling, data changes, assumptions, and uncertainty are always disclosed.

---

## 7. Limitations

- **Correlation is not causation.** Proving cause and effect needs experiment data (e.g. treatment vs. control). Other causal results are estimates only.
- **Very large tables are sampled.** Tables over 200,000 rows are analyzed from a representative sample, so totals describe the sample rather than the full dataset.
- **Some formats are loaded whole.** Excel, JSON, XML, SQLite files, and ZIP contents must fit in browser memory. The practical size limit depends on your device.
- **Formats not yet supported:** SAS, SPSS, Stata, Avro, and ORC files, as well as PDFs and images. Save these as CSV, Excel, or Parquet first.
- **Data model canvas:** connections go from one main table to each other table (star schema). Chained connections (e.g. customers → regions) are not supported yet.
- **Forecasts need history.** Reliable forecasts need enough regular time periods. Short or patchy history gives wider uncertainty.
- **Text analysis** uses a word-list sentiment method, not a deep language model.
- **Session only.** Data and results disappear when you close the page. There are no saved projects yet.
- **AI assistant.** Answers depend on the calculated summaries and can still be wrong. Always check them against the figures shown. The assistant needs an internet connection.
- **PDF report size.** Reports with many charts can be large files.
- **Statistical methods are approximations** suited to business decision support, not regulated scientific studies.

---

## 8. Upcoming Enhancements

1. **Snowflake data models:** chained table connections on the data model canvas
2. **Full-dataset analysis for very large files:** in-browser database technology to analyze every row instead of a sample
3. **More formats:** SAS, SPSS, Stata, Avro, ORC, plus SQL database and cloud storage connections
4. **Advanced optimization:** goal-seeking and constraint-based recommendations
5. **Multi-factor sensitivity analysis:** test several factors in one scenario
6. **Deeper text analysis:** AI-powered themes, topics, and sentiment
7. **Data drift monitoring:** compare new uploads with earlier ones and flag changes
8. **Saved workspaces and sharing:** optional accounts to save, revisit, and work on analyses together
9. **Custom report builder:** choose which sections, charts, and branding go into the PDF, with smaller file sizes

---

*Insights & Analytics Engine: from raw data to reliable, evidence-backed decisions.*

---
