# BizInsight AI — Automated Competitive Analysis & Report Generator

## 📌 Overview

BizInsight AI is a **multi-agent competitive intelligence system** designed to automatically collect, analyze, compare, and summarize competitor insights from product reviews and public data. It transforms unstructured text into **actionable strategic reports**, helping product, marketing, and strategy teams understand competitor strengths, weaknesses, and customer sentiment.

This project demonstrates **Enterprise Agents**, **multi-agent orchestration**, **sessions & memory**, **observability**, and **structured output generation** using Python inside a single Kaggle notebook.

---

## 🚀 Motivation — Why Agents?

Competitive research usually requires manually:

* Searching for competitor information
* Reading hundreds of reviews
* Identifying key issues and customer pain points
* Comparing feature sets and pricing
* Writing a report

This is slow, repetitive, and error-prone.

Agents solve this by:

* **Splitting the workflow into specialized agents** (collector, sentiment, themes, insights, comparison)
* **Running tasks in parallel** (fast + scalable)
* **Ensuring each step is explainable and traceable** (logs, session files)
* **Automatically generating reports** that summarize all findings

BizInsight AI becomes a **virtual competitive analyst**.

---

## 🧠 Multi-Agent Architecture

### **1. Collector Agent**

Fetches and normalizes product reviews (mock + real Kaggle dataset).

### **2. Sentiment Agent**

Computes per-review and averaged sentiment scores.

### **3. Theme Agent**

Extracts recurring topics such as battery, pricing, shipping, UI, etc.

### **4. Comparison Agent**

Builds feature parity tables between companies.

### **5. Insights Agent**

Generates high-level, actionable recommendations based on patterns.

### **6. Report Generator**

Creates markdown reports and sentiment charts.

### **7. Orchestrator**

Coordinates all agents using both **parallel + sequential flow**, manages session state, logs, and outputs.

---

## 📂 Project Structure (Kaggle Notebook)

```
📘 Notebook.ipynb
└── Agents
    ├── CollectorAgent
    ├── SentimentAgent
    ├── ThemeAgent
    ├── ComparisonAgent
    ├── InsightsAgent
    └── Report Generator
└── Orchestrator
└── Output (Generated Reports & Charts)
└── Memory Bank
└── Logs
```

---

## 🧪 Demo (Built-in Mock Data)

The notebook first runs with **two mock companies**:

```
AcmeCorp
ExampleCo
```

This ensures reproducibility without external data.

**Generated Outputs:**

* `report_AcmeCorp.md`
* `report_ExampleCo.md`
* Sentiment histograms (`*.png`)
* Session file (`*_session.json`)
* Metrics file (`*_metrics.json`)

---

## 📊 Real Dataset Integration (Amazon Mobile Reviews)

The notebook integrates with the Kaggle dataset:

**Dataset:**
[https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones](https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones)

### Steps Performed:

* Load full dataset
* Auto-detect text/rating/brand columns
* Extract top 3 brands by review count
* Convert reviews into orchestrator-compatible format
* Run full agent pipeline on real brands
* Generate reports + charts for each brand

---

## 🏗️ The Build — Tools & Technologies

* Python 3 (Kaggle Notebook)
* BeautifulSoup4 — lightweight parsing
* Pandas & NumPy — data processing
* Matplotlib — sentiment charts
* Concurrent Futures — parallel agents
* Custom lightweight sentiment analyzer
* In-memory + JSON storage for sessions & memory
* Structured logging for observability

---

## 📈 If I Had More Time

Enhancements planned:

* Integrate LLMs (Gemini) for deeper summarization & extraction
* Add real-time scraping tools (NewsAPI, web crawler)
* Build a Streamlit/React dashboard
* Implement trend detection using historical memory
* Improve recommendation scoring with model-based prioritization
* Add automated alerts (Slack/Email)

---

## 📝 How to Run

1. Open the Kaggle notebook
2. Add dataset:
   *Amazon Reviews Unlocked Mobile Phones*
3. Click **Run All**
4. Inspect outputs in the **Output** tab

---

## 🎯 Track Selection

**Enterprise Agents Track** — The project focuses on business workflows, competitor intelligence, and report generation.

---

## 📌 Final Notes

The notebook is fully self-contained:

* Works offline with mock data
* Extends to real dataset for scalability
* Demonstrates core concepts required for the capstone
*
Demonstrates core concepts required for the capstone
