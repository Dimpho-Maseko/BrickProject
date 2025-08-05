# 🪙 Bitcoin Data Engineering Project

This project was developed for a **Bitcoin investment advisory firm** to build a robust and scalable data pipeline using **Apache Spark, Delta Lake**, and **Databricks**. The goal was to transform raw Bitcoin market data into reliable, feature-rich datasets for strategic decision-making, performance analysis, and potential predictive modeling.

---

## 📊 Dataset Description

The dataset used in this project contains **historical Bitcoin market data** and was sourced from [Kaggle](https://www.kaggle.com/). It includes:

- `market_date`: Trading date
- `open`, `high`, `low`, `close`: Price metrics per day
- `volume`: Daily trading volume
- `market_cap`: Market capitalization of Bitcoin

This dataset enables the firm to analyze trends, understand market volatility, and track Bitcoin's trading performance over time.

---

## 🎯 Project Objectives

As a Data Engineer, my objective was to:
- Build a **modular, layered ETL pipeline** using the **medallion architecture**
- Ensure **data accuracy, consistency, and usability** through validation checks
- Enrich the data with engineered features to support:
  - Market trend analysis
  - Investment timing
  - Risk evaluation

---

## 🧱 Data Pipeline Architecture (Medallion)

| Layer  | Description |
|--------|-------------|
| **Bronze** | Raw ingestion of CSV data as-is into a Delta table |
| **Silver** | Cleaned, standardized, and validated data for analytics |
| **Gold**   | Enriched data with engineered features for insight generation |

---

## 📁 Notebook Breakdown

### 📌 `01_Ingest_Data(Bronze Layer).ipynb`
- Read raw CSV files into Databricks
- Added ingestion metadata (e.g., load timestamp)
- Stored data in **Delta Lake Bronze table**
- Ensured schema consistency for long-term maintainability

### 📌 `02_Clean_&_Transform(Silver Layer).ipynb`
- Removed invalid or null records
- Casted data types to appropriate formats (e.g., `market_date` to `DateType`)
- Filtered for relevant date ranges
- Created the **Silver table** with clean and structured data

### 📌 `03_Feature_Engineering.ipynb`
- Generated business-relevant features:
  - `daily_change_pct`: % change in closing price
  - `rolling_avg_close_7d`: 7-day moving average of closing price
  - `volatility`: based on price variance
- These metrics help the firm:
  - Detect bullish or bearish patterns
  - Assess market momentum
  - Optimize investment timing

### 📌 `04_Data_Quality.ipynb`
- Validated completeness and accuracy:
  - Checked for nulls, duplicates, and schema mismatches
  - Verified that feature values aligned with expectations (e.g., no negative volume)
- Logged failed records separately
- Final output written to **Gold table (`verified_features`)**

---

## 💼 Business Value to the Advisory Firm

By cleaning and transforming this Bitcoin market data, the firm gains:

✔️ **Trustworthy historical data** for backtesting strategies  
✔️ **Advanced metrics** for client advisory reports  
✔️ **Early warning indicators** from engineered features  
✔️ A foundation for **predictive models** like price forecasting or anomaly detection

This data pipeline ensures that investment decisions are **based on accurate, timely, and enriched market intelligence**.

---

## 🧰 Tech Stack

- **Databricks** (Notebooks, Delta Live Tables, DBFS)
- **Apache Spark / PySpark**
- **Delta Lake**
- **Python**
- **Git & GitHub**

---

## 🧪 How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/bitcoin-data-pipeline.git
