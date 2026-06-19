# 🤖 Data Analysis Agent v2

> Upload **ANY** Kaggle CSV → Auto-clean → Auto-analyse → Auto-plot  
> 100% free. No API key. Fully adapts to whatever CSV you upload.

---

## ✨ What's New in v2

- ✅ No fake sample data overwriting your upload
- ✅ Fully adapts to your actual column names and types
- ✅ Smarter plot selection based on what columns exist
- ✅ Works with any Kaggle dataset

---

## 🚀 What It Does

This is an **agentic data pipeline** — it thinks, plans, and executes on its own.

You upload a CSV. The agent:
1. **Inspects** your data — detects column types, missing values, duplicates, outliers
2. **Builds a plan** — decides which cleaning steps are actually needed
3. **Cleans** — executes only what's required (no hardcoded steps)
4. **Analyses** — generates 9 types of adaptive visualizations
5. **Exports** — downloads a cleaned CSV + summary report

---

## 📊 9 Types of Auto-Generated Plots

| # | Plot | When generated |
|---|---|---|
| 1 | Histograms (distributions) | Always, for all numeric columns |
| 2 | Correlation heatmap | When 2+ numeric columns exist |
| 3 | Categorical bar charts | For all low-cardinality categorical columns |
| 4 | Boxplots (outlier check) | Always, for all numeric columns |
| 5 | Category × Numeric group bars | When both types exist |
| 6 | Monthly time trends | When date columns are detected |
| 7 | Pairplot | When 2–6 numeric columns exist |
| 8 | Statistical summary table | Always |
| 9 | Key insights summary | Always |

---

## 🧠 How the Agent Works

```
Upload CSV
    ↓
Inspect → detect types, nulls, duplicates, outliers
    ↓
Plan → build action steps dynamically
    ↓
Clean → fill nulls | remove dups | cap outliers | parse dates
    ↓
Analyse → 9 adaptive visualizations + insights
    ↓
Export → cleaned_YYYYMMDD.csv + report_YYYYMMDD.txt
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas & NumPy | Data handling and cleaning |
| Matplotlib | Custom chart generation |
| Seaborn | Heatmap and pairplot |
| SciPy | Statistical analysis |
| Google Colab | Runtime + file upload/download |

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**
2. Run **Cell 1** — installs and imports everything
3. Run **Cell 2** — file picker opens, upload your CSV
4. Run **Cell 3** — agent inspects your data and builds a plan
5. Run **Cell 4** — agent cleans your data
6. Run **Cell 5** — agent generates all plots and insights
7. Run **Cell 6** — downloads your cleaned CSV + report
8. Run **Cell 7** — write your own custom Pandas queries

---

## 📋 Sample Agent Output

```
============================================================
  AGENT INSPECTION REPORT
============================================================
  Rows    : 10,000
  Columns : 12

  Numeric columns (5) :
    • age        (min=18.00, max=90.00, mean=42.30)
    • salary     (min=20000.00, max=500000.00, mean=72400.00)
    ...

  Missing values: 342 total (0.3% of dataset)
    • age        → will fill
    • department → will fill

  Duplicate rows : 23

  Outlier columns: 2
    • salary     412 outliers
    • experience  89 outliers

============================================================
  ACTION PLAN
============================================================
  Step 1: Remove 23 duplicate rows
  Step 2: Fill missing values (2 columns)
  Step 3: Cap outliers in 2 columns
  Step 4: Run full analysis + generate plots
  Step 5: Export cleaned CSV + report
```

---

## 💡 Key Features

- **Multi-encoding support** — handles utf-8, latin-1, cp1252, utf-8-sig (common in Kaggle datasets)
- **High cardinality detection** — skips plotting columns with 25+ unique values automatically
- **Date parsing** — detects and extracts year, month, weekday from date columns
- **Adaptive outlier capping** — uses IQR method, clips to 1st–99th percentile
- **Null handling** — fills numeric nulls with median, categorical with mode

---

## 📁 Project Structure

```
├── data_analysis_agent_v2.ipynb   # Main notebook (run in Google Colab)
└── README.md
```

---

## 🔮 Future Improvements

- [ ] Streamlit web app version
- [ ] GPT-powered natural language insights
- [ ] Support for Excel (.xlsx) uploads
- [ ] Auto-suggest ML models based on dataset structure

---

## 👤 Author

**Sahil Prakash** — B.Tech CSE, Galgotias University  
[github.com/Sahilp008](https://github.com/Sahilp008)

Feel free to fork, star ⭐, and raise issues. Contributions welcome!
