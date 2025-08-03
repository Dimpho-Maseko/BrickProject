# BrickProject

# 💹 Bitcoin Market Data Engineering Project

## 🧠 Project Overview

This project delivers a robust data engineering pipeline designed to ingest, clean, and enrich historical Bitcoin market data for a Bitcoin Investment Advisory Firm. The pipeline transforms raw data into a high-quality, analytics-ready dataset that supports trend analysis, volatility tracking, anomaly detection, and investment decision-making.

---

## 🎯 Project Objective

To build an automated and scalable data pipeline that processes Bitcoin’s daily market behavior and delivers reliable, enriched datasets with engineered features that power investment analytics, client reporting, and forecasting models.

---

## 🏢 Client

**Bitcoin Investment Advisory Firm**

> A financial advisory company providing expert investment guidance in the cryptocurrency space. Their success relies on timely, accurate, and insightful analysis of digital asset trends, especially Bitcoin.

---

##  Key Features & Deliverables

-  **Ingest** raw daily Bitcoin data (Open, High, Low, Close, Volume, Market Cap)
-  **Clean & validate** data for quality, completeness, and consistency
-  **Engineer features** like:
  - Daily returns
  - Price volatility
  - Rolling averages
  - Lagged features
-  **Detect outliers and anomalies** using statistical methods and visualizations (e.g., boxplots)
-  **Store in bronze, silver, and gold layers** using Delta/Parquet
-  **Enable integration** with dashboards or ML models
-  **Automate** with scheduling tools like Databricks Workflows or Airflow

---

## ⚒ Tech Stack

| Component | Tools Used |
|-----------|------------|
| Data Processing | PySpark (Apache Spark) |
| Data Storage | Delta Lake / Parquet / DBFS |
| Environment | Databricks / Jupyter Notebook |
| Scheduling | Databricks Workflows / Airflow (optional) |
| Version Control | Git / GitHub |
| Visualization | Matplotlib, Pandas, Power BI (optional) |
| Data Quality | Custom checks / Great Expectations (optional) |

---

##  Project Structure

