# 🛒 E-commerce Data Engineering Project

An end-to-end data engineering pipeline that ingests, processes, and stores e-commerce data for analysis and reporting.

## 📐 Architecture

The overall pipeline architecture is documented in [`architecture_diagram.drawio`](./architecture_diagram.png).
Open it with [draw.io](https://app.diagrams.net/) or the VS Code Draw.io extension to view/edit.

**Pipeline Overview:**
1. Raw e-commerce data is collected/sourced
2. Data is ingested into the database (see `data_ingestion_into_database.ipynb`)
3. SQL scripts transform and structure the data
4. Processed data is ready for analysis/reporting

## 📁 Project Structure
