# Azure Data Factory & Databricks – End-to-End Data Engineering Pipeline (Medallion Architecture)

🚀 **End-to-End Data Engineering Project** demonstrating how to design and implement a **modern data pipeline** on Azure using **Medallion Architecture** (Bronze → Silver → Gold).

This project covers ingestion, transformation, incremental loading, data modeling, and delivery of analytics-ready datasets.

---

## 📌 Project Overview

The goal of this project is to build a **scalable and reliable data platform** using **Azure Data Factory (ADF)** and **Azure Databricks (ADB)**.

Key highlights:

* ✅ Designed **Medallion Architecture** (Bronze → Silver → Gold layers).
* ✅ Ingested raw data from multiple sources (CSV, JSON, APIs).
* ✅ Implemented **incremental loading with Watermarking** (handles late-arriving data).
* ✅ Built **Fact & Dimension tables** with **Surrogate Keys**.
* ✅ Designed **Star Schema Data Warehouse Model** for analytics.
* ✅ Created **Stored Procedures** to update watermark dates automatically.
* ✅ Delivered curated datasets into **Delta Lake tables** and **Azure SQL Data Warehouse** for reporting.

---

## 🛠️ Tech Stack & Tools

* **Azure Data Factory (ADF)** → Orchestration & Ingestion
* **Azure Databricks (PySpark + Delta Lake)** → Transformations & Modeling
* **Azure Data Lake Gen2** → Storage
* **Azure SQL Data Warehouse** → Analytics & Reporting
* **Delta Lake** → ACID transactions & versioning
* **PySpark** → Distributed data processing
* **SQL (T-SQL)** → Warehouse modeling & stored procedures

---

## ⚡ Architecture (Medallion: Bronze → Silver → Gold)

1. **Bronze (Raw Data Layer)**

   * Data ingested from multiple sources using ADF pipelines.
   * Stored in ADLS (raw zone).

2. **Silver (Cleansed & Transformed Layer)**

   * Data cleaned & standardized in Databricks.
   * Watermarking applied for incremental loads.
   * Duplicate handling & schema validation.

3. **Gold (Curated & Analytics Layer)**

   * Star Schema modeled (Fact & Dimension tables with surrogate keys).
   * Data stored in **Delta Lake** and **Azure SQL Data Warehouse**.
   * Ready for Power BI / downstream reporting.

---

## 📂 Project Structure

```
📦 Azure-ADF-Databricks-Medallion
 ┣ 📂 adf_pipelines/        → JSON of ADF pipelines
 ┣ 📂 notebooks/            → PySpark transformation notebooks
 ┣ 📂 sql_scripts/          → Fact/Dimension table creation + Stored Procedures
 ┣ 📂 data_samples/         → Sample input datasets (CSV, JSON, etc.)
 ┣ 📜 README.md             → Project documentation
```

---

## 🔄 Incremental Loading & Watermarking

* Implemented watermark logic in Databricks to **load only new/changed records**.
* Stored Procedures in SQL update the **last processed date** after each load.
* Ensures **idempotency** (safe re-runs without duplication).

---

## 📊 Data Warehouse Modeling

* Designed **Star Schema**:

  * **Fact Tables** → Transactions, Sales, etc.
  * **Dimension Tables** → Customer, Product, Date, etc.
* Used **surrogate keys** for dimension linking.
* Optimized for **Power BI dashboards** and **reporting**.

---

## 🚀 How to Run This Project

1. Clone this repo:

   ```bash
   git clone https://github.com/Gurukavin/Azure-Data-Factory-and-Databricks-Medallion-End-to-End-Pipeline.git
   ```

2. Import **ADF Pipelines** into your Azure Data Factory.

3. Upload provided sample datasets into **Azure Data Lake (Raw Zone)**.

4. Open **Databricks Notebooks** and run transformations (Bronze → Silver → Gold).

5. Deploy **SQL scripts** to create Fact/Dimension tables & Stored Procedures.

6. Connect **Power BI** (or Synapse/SQL) to the Gold Layer for analytics.

---

## 📈 Output / Deliverables

* Curated **Gold Layer datasets** in Delta/SQL Warehouse.
* **Fact & Dimension tables** ready for BI.
* **Automated Incremental Pipeline** using Watermarking.
* Example Power BI dashboards (can be added).

---

## 🤝 Connect

If you’re passionate about **Data Engineering, Cloud, and Modern Data Platforms**, let’s connect! 🚀

📌 **Author:** [Guru Kavin](https://github.com/Gurukavin)
📌 **Project Repo:** [Azure Data Factory & Databricks Medallion Pipeline](https://github.com/Gurukavin/Azure-Data-Factory-and-Databricks-Medallion-End-to-End-Pipeline)

---

## 🏷️ Tags

`Azure` `ADF` `Databricks` `PySpark` `DeltaLake` `MedallionArchitecture` `DataEngineering` `WarehouseModeling` `Watermarking`
