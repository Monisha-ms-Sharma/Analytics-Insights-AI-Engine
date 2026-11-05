# Analytics & Insights - AI Engine

Evidence-based business intelligence from your own data, written in plain English.

**Live app:** https://analytics-insights-engine.lovable.app/

---

## 1. Why this application was built

Most organizations have plenty of data but struggle to turn it into reliable decisions:

- **Traditional analytics tools are complex.** They often need technical skills, coding, or a dedicated analyst.
- **Generic AI tools can make things up.** They may give confident answers the data does not support.
- **Privacy matters.** Many people do not want to upload sensitive business files to outside servers.

Analytics & Insights - AI Engine fixes this. Anyone, with or without an analytics background, can upload data and get trustworthy insights about business events and outcomes. Every insight is calculated directly from the uploaded data.

## 2. What this application does

The app automatically models and analyzes one or more uploaded datasets. It then explains:

- What happened
- Why it may have happened
- What could happen next
- What actions to consider

```text
Upload files (CSV, Excel, Text, Parquet, JSON, XML, ZIP, ...) or a cloud-storage link
        |
        v
Read & preserve originals (large files read in pieces)
        |
        v
Profile columns, data quality & industry recognition
        |
        v
Data model canvas: connect tables (star or chained)  -->  Combined model
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
|  Machine learning                                         |
|  Supervised | Unsupervised | Reinforcement (offline) |    |
|  Semi-supervised | Self-supervised                        |
+-----------------------------------------------------------+
        |
        v
Interactive charts | Ask your data (AI) | Guided walkthrough | Industry measures
        |
        v
Custom PDF report  |  Saved workspaces  |  Shareable results (no data rows)
```

## 3. What this application is capable of

### Supported file types

| Category | Formats |
| --- | --- |
| Delimited text | CSV, TSV, TXT, PSV, DAT, TAB |
| Spreadsheets | Excel (XLSX, XLS, XLSM, XLSB), OpenDocument (ODS) |
| Big data / columnar | Parquet, Arrow, Feather |
| Structured data | JSON, JSONL, NDJSON, GeoJSON, XML |
| Databases | SQLite files (every table is loaded) |
| Compressed | ZIP folders (including nested folders), GZIP files |
| Cloud links | Google Drive, OneDrive, Dropbox, SharePoint share links (passed straight to your browser, never stored) |

- Upload a single file or many files at once.
- Original data is never changed.

### Large and big data files

- CSV and text files over 50 MB are read in pieces, and Parquet files are read in sections, so they don't need to fit in memory all at once. A 2.6-million-row CSV has been tested successfully.
- Tables are analyzed in full up to a size budget (about 40 million cells). Beyond that, a reproducible sample covering the whole file is used, and the app always says so.
- A progress bar shows each step while large files are read and analyzed.

### Data understanding

- Automatic column profiling: type, role, statistics, and meaning in plain English.
- A column dictionary that labels each meaning as supported by the data or inferred, with space to add your own explanation.
- Automatic detection of shared fields between tables.
- Recognition of 27 industries (healthcare, finance, education, engineering, technology, cybersecurity, aviation, research, geospatial, hospitality, law, food, entertainment, casino, travel and more), with industry measures shown only when matching columns exist — never estimated.

### Data model canvas (multiple tables)

- Choose a main table and connect the others around it, directly (star) or in chains (for example sales → customers → regions).
- Connect tables by clicking a matching field in each, or with one click on a suggested match.
- Each connection is checked before use. It shows the match rate and blocks connections that would duplicate records.
- **Build model & analyze** combines connected tables into a new table. Your original tables stay unchanged.

### Core analysis

| # | Type | Question it answers | What it includes |
| --- | --- | --- | --- |
| 1 | Descriptive | What happened? | Mean, median, mode, percentages, KPIs, trends, segments, distributions, dashboards |
| 2 | Diagnostic | Why did it happen? | Correlations with significance, key drivers, high vs. low comparisons, contribution analysis, anomaly detection |
| 3 | Predictive | What is likely next? | Time-series forecasting (naive, linear, Holt, seasonal) with holdout validation; regression and classification; leakage protection |
| 4 | Prescriptive | What should we do? | Prioritized, evidence-backed recommendations; interactive what-if scenario simulator |

### Additional analysis

| # | Type | What it does |
| --- | --- | --- |
| 5 | Inferential | Confidence intervals, t-tests, chi-square tests and correlation significance, with correction for multiple tests |
| 6 | Causal | Compares experiment groups when present (e.g. treatment vs. control); otherwise gives regression-adjusted effects and states the limits of observational data |
| 7 | Mechanistic | Finds exact arithmetic relationships (e.g. revenue = price × units), contribution shares and elasticities |
| 8 | Quantitative + Qualitative | Each group's share of records vs. its share of the outcome |
| 9 | Text & Sentiment | Themes, top terms, phrases and positive/negative/neutral sentiment in free text, how outcomes differ by sentiment, with example quotes |

### Machine learning

| Family | Methods |
| --- | --- |
| Supervised | Ridge and logistic regression, decision tree, random forest, bagged trees, gradient boosting, linear SVM/SVR, k-nearest neighbours, Naive Bayes — each scored on held-out records |
| Unsupervised | k-means, hierarchical clustering, principal component analysis, association rules |
| Reinforcement (offline) | Learns which logged action did best in each situation; methods needing a live environment are reported as not applicable, never simulated |
| Semi-supervised | Self-training with pseudo-labels |
| Self-supervised | Masked-feature reconstruction |

## 4. Key features and how to use them

| Feature | What it does | How to use it |
| --- | --- | --- |
| Upload area | Accepts files, ZIP folders or a cloud-storage link | Drop files in, paste a link, or click **Try sample data** |
| Overview | Headline metrics, charts, ranked findings and industry measures | Opens automatically after upload |
| Guided walkthrough | Step-by-step tour using your live results | Open **Guided walkthrough** and press Next |
| Ask your data | Plain-English questions answered from calculated findings, with figures and caveats | Type a question or pick a suggested one |
| Analysis controls | Choose the outcome, time field and filters | Selectors at the top of the workspace |
| Analysis sections | One section per analysis type, plus Machine learning | Click any item in the left menu (it scrolls on small screens) |
| Scenario simulator | Tests "what if" changes to key factors | Predictive section → adjust a factor |
| Data model canvas | Connect multiple tables before analysis | Relationships → choose main table → click matching fields → **Build model & analyze** |
| Column dictionary | Plain-English meaning of every column | Search, expand and add clarifications |
| Data quality | Issues rated High / Medium / Low with next steps | Open **Data quality** |
| Original data | Your untouched data, page by page | Open **Original data** |
| PDF report builder | Choose sections, charts and branding for the report | Click **Download report** |
| Saved workspaces | Keeps files, settings, notes and models in your browser | Click **Save workspace**; reopen from the start screen |
| Share results | Exports findings without any data rows for colleagues | Click **Share results**; colleagues open it from the start screen |

## 5. Plans and access

| Option | Price | What you get |
| --- | --- | --- |
| Early Access | Free | 3 full analyses per signed-in person, including reports and Ask your data |
| Single Data File Analysis | $100 one-time | One full analysis + report for one file |
| Full Data Set Analysis | $200 one-time | One full analysis + report for multiple files |
| Monthly | $50 / month | Unlimited analyses + Ask your data |
| Yearly | $250 / year | Unlimited analyses + Ask your data |

Overview, Guided walkthrough, Descriptive, Data quality, Column dictionary, Relationships and Original data are free on every dataset. Payments are handled by Paddle as merchant of record. Cancelled subscriptions keep access until the period ends; plan changes are prorated. See the Terms, Refund (30-day money-back) and Privacy pages in the app.

## 6. Who this is for

- Business owners and managers
- Product, marketing, sales and operations teams
- Finance and strategy professionals
- Data analysts and consultants who want a fast, reliable first pass
- Researchers, educators and students
- Anyone who needs answers from data without coding

## 7. How it benefits users

- **Plain English:** results are explained without jargon.
- **Reliable:** every finding is calculated from your data. Facts, relationships, hypotheses, predictions and recommendations are labeled separately.
- **Honest:** correlation is never presented as causation, and financial gains or costs are never invented.
- **Private:** files are processed in your browser and never stored in the cloud. The AI assistant only receives calculated summaries, never raw rows.
- **Works with real-world data:** many file types, multiple related tables and very large files.
- **Fast:** analysis runs in the background so the screen stays responsive.
- **Consistent:** the screen and the PDF use the same calculations, so figures always match.
- **Transparent:** sampling, data changes, assumptions and uncertainty are always disclosed.

## 8. Limitations

- **Correlation is not causation.** Proving cause and effect needs experiment data; other causal results are estimates.
- **Very large tables may be sampled** beyond the size budget; totals then describe the sample.
- **Some formats load whole.** Excel, JSON, XML, SQLite and ZIP contents must fit in browser memory; the practical limit depends on your device.
- **Not yet supported:** SAS, SPSS, Stata, Avro and ORC files, PDFs and images. Save these as CSV, Excel or Parquet first.
- **Forecasts need history.** Short or patchy history gives wider uncertainty.
- **Text analysis** uses a word-list sentiment method, not a deep language model.
- **Saved workspaces live in your browser** — they don't follow you to another device.
- **AI assistant answers** depend on calculated summaries and can still be wrong; check them against the figures shown. It needs an internet connection.
- **Machine learning** runs on a capped, reproducible selection of records to keep the browser responsive.
- Statistical methods suit business decision support, not regulated scientific studies.

## 9. Upcoming enhancements

- More formats: SAS, SPSS, Stata, Avro, ORC, plus SQL database connections
- Advanced optimization: goal-seeking and constraint-based recommendations
- Multi-factor sensitivity analysis in one scenario
- Deeper AI-powered text themes, topics and sentiment
- Data drift monitoring between uploads

---

Seller: Monisha Sharma, AI Engine, USA.

**Analytics & Insights - AI Engine: from raw data to reliable, evidence-backed decisions.**
