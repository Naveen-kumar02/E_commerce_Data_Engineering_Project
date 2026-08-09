# 🛒 E-commerce Data Engineering Project

An end-to-end data engineering pipeline that ingests, processes, and stores e-commerce data for analysis and reporting.

## 📐 Architecture

The overall pipeline architecture is documented in [`architecture_diagram.drawio.png`](./architecture_diagram.drawio.png).
Open it with [draw.io](https://app.diagrams.net/) or the VS Code Draw.io extension to view/edit.

**Pipeline Overview:**
1. **Data Source**
   Raw e-commerce data is sourced from a GitHub repository, simulating an external/upstream data provider.

2. **Data Ingestion**
   Initial ingestion and exploration is handled via `data_ingestion_into_database.ipynb`, validating data structure and quality before pipeline integration.

3. **Bronze Layer — Raw Data Ingestion**
   **Azure Data Factory (ADF)** orchestrates the extraction of raw data from GitHub and lands it, unmodified, into the **Bronze layer** of **Azure Blob Storage**, preserving the original source data for traceability and reprocessing.

4. **Silver Layer — Data Transformation**
   **Azure Databricks** performs cleansing, transformation, and enrichment on the Bronze data — including deduplication, schema standardization, and business rule application — before writing the refined output to the **Silver layer** in Azure Blob Storage.

5. **Gold Layer — Curated Data for Analytics**
   **Azure Synapse Analytics** consumes the Silver layer data to build structured **schemas and views** optimized for reporting and analytics, persisting the final curated datasets into the **Gold layer** on **Azure Data Lake Storage (ADLS) Gen2**.

6. **Consumption**
   The Gold layer serves as the analytics-ready data source for **Data Analysts** and **Data Scientists**, enabling dashboards, reporting, and downstream machine learning workflows.

## 📁 Project Structure
