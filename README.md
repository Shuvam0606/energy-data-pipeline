# ⚡ Energy Data Pipeline (Azure Databricks + PySpark + Data Lake)

## 📌 Project Overview
This project demonstrates how to build a **Big Data Pipeline** for the **Energy & Power Distribution sector** using **Azure Databricks, PySpark, and Azure Data Lake Storage Gen2 (ADLS)**.  

The pipeline follows the **Medallion Architecture (Bronze → Silver → Gold)** to ensure scalability, performance, and reliability in handling large datasets from the **Open Energy System Database (OPSD)**.  

By the end of this project, the pipeline will produce **analytics-ready data** that can be used to analyze energy generation, consumption, and renewable energy trends—similar to real-world Data Engineering workflows in power companies.

---

## 🏗️ Architecture

flowchart LR
    A[Open Energy Dataset] -->|Ingest| B[Bronze Layer (Raw Data in ADLS)]
    B -->|Clean & Transform| C[Silver Layer (Standardized Data in ADLS)]
    C -->|Aggregate & Optimize| D[Gold Layer (Analytics-Ready Data in ADLS)]
    D -->|Visualize| E[Power BI / Reporting]
    C -->|Exploration| F[Databricks Notebooks (PySpark)]

---

## 🔧 Azure Resources
- **Resource Group**: `rg-energy-pipeline`  
- **Storage Account (ADLS Gen2)**: `stenergydatalake`  
  - Containers: `bronze`, `silver`, `gold`  
- **Databricks Workspace**: `db-energy-project`  
- **Databricks Cluster**: `dev-small` (auto-terminate enabled)  

---

## 📊 Dataset
- **Source**: [Open Energy System Database (OPSD)](https://open-power-system-data.org/)  
- **Domain**: Power generation, consumption, and renewable energy data  
- **Format**: CSV / Parquet  
- **Use Case**:  
  - Regional electricity consumption trends  
  - Renewable vs non-renewable energy mix  
  - Time-series insights on power demand  

---

## ⚙️ Pipeline Workflow
1. **Ingestion (Bronze)** → Raw data stored in ADLS `bronze` container.  
2. **Transformation (Silver)** → Clean, deduplicate, and standardize data with PySpark in Databricks.  
3. **Aggregation (Gold)** → Summarized analytics tables for reporting and dashboards.  
4. **Visualization** → Power BI dashboards built on top of `gold` layer.  

---

## 📸 Screenshots
Screenshots of setup, transformations, and dashboards will be added as implementation progresses.  

All screenshots will be stored in a `/screenshots/` folder.

---

## 🚀 Business Impact
This pipeline simulates what a **Data Engineer in the Energy/Utilities sector** would build:  
- Provides **scalable big data processing** on cloud.  
- Enables **data-driven decision-making** (renewable adoption, peak demand analysis).  
- Serves as a **portfolio project** to showcase Big Data + Azure Data Engineering skills.  

---

## 🛠️ Tech Stack
- **Azure Data Lake Storage Gen2 (ADLS)**  
- **Azure Databricks (PySpark)**  
- **Medallion Architecture** (Bronze/Silver/Gold)  
- **Power BI**  
- **GitHub**  

---

## 📂 Repository Structure
```
energy-data-pipeline/
│── notebooks/           # Databricks PySpark notebooks
│── scripts/             # Helper scripts (if needed)
│── screenshots/         # Setup & execution screenshots
│── README.md            # Project documentation
```

---

✍️ **Author**: [Shuvam Karmakar](https://linkedin.com/in/shuvam-karmakar-sk)  
📂 **GitHub Repo**: [energy-data-pipeline](https://github.com/Shuvam0606/energy-data-pipeline)
