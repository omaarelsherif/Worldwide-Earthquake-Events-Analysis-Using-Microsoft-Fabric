# Worldwide-Earthquake-Events-Tracking-Using-Microsoft-Fabric

An end-to-end **Data Engineering project** built using **Microsoft Fabric**, implementing a full **Medallion Architecture (Bronze → Silver → Gold)** with **CI/CD using Fabric Deployment Pipelines**.


## Overview

This project ingests real-time earthquake data from the **USGS API**, processes it through layered transformations, and delivers interactive insights via Power BI.

### Highlights:

* API-based ingestion (real-world scenario)
* Medallion architecture using Lakehouse
* Parameterized pipeline orchestration
* Full Fabric asset export
* CI/CD using Deployment Pipelines (Dev → Test → Prod)
* Interactive reporting with filters and map visualization

## Architecture

The below diagram shows project architecture


## CI/CD — Deployment Pipeline

This project implements **CI/CD using Fabric Deployment Pipelines** across three environments:

```id="cicd123"
Dev Workspace  →  Test Workspace  →  Prod Workspace
```

### 🏗️ Environments:

* **🧪 Dev**

  * Development & experimentation
  * Notebook changes & testing

* **🔍 Test**

  * Validation & QA
  * Ensures pipeline stability

* **🚀 Prod**

  * Production-ready environment
  * Connected to reporting layer

---

### ⚙️ Deployment Process:

* Assets developed in **Dev workspace**
* Promoted to **Test workspace** for validation
* Deployed to **Prod workspace** for final usage

### ✅ Deployed Assets:

* Notebooks
* Data Pipeline
* Lakehouse
* Environment
* Semantic Model & Report

✔️ Ensures consistency across environments
✔️ Enables controlled releases

---

## 🗂️ Repository Structure

```id="repo123"
📦 earthquake-fabric-project
 ┣ 📂 Notebooks
 ┃ ┣ 📜 01_bronze_ingestion.ipynb
 ┃ ┣ 📜 02_silver_transformation.ipynb
 ┃ ┗ 📜 03_gold_layer.ipynb
 ┣ 📂 Pipeline
 ┃ ┗ 📜 data_factory_pipeline.json
 ┣ 📂 Environment
 ┃ ┗ 📜 fabric_environment.json
 ┣ 📂 Lakehouse
 ┃ ┗ 📜 lakehouse_definition.json
 ┣ 📂 Report
 ┃ ┗ 📜 earthquake_report.pbix
 ┣ 📂 Raw Data
 ┃ ┗ 📜 earthquake_raw.json
 ┣ 📂 Screenshots
 ┃ ┣ 📸 pipeline.png
 ┃ ┣ 📸 report.png
 ┃ ┗ 📸 deployment_pipeline.png
 ┗ 📜 README.md
```

---

## 🥉 Bronze Layer — Ingestion

* Source: **USGS Earthquake API**
* Tool: Fabric Notebook (PySpark)

✔️ Stores raw JSON data in Lakehouse
✔️ Preserves original format for replay

---

## 🥈 Silver Layer — Transformation

* Converts raw JSON into structured format

### Steps:

* Flatten nested JSON
* Clean & standardize schema
* Cast data types

✔️ Output: Delta Table

---

## 🥇 Gold Layer — Analytics

* Prepares business-ready dataset

### Enhancements:

* 🌍 Country code extraction
* 📊 Significance classification (Low / Medium / High)
* 🧮 Derived calculations

✔️ Output: Analytics-ready table

---

## 🔄 Pipeline (Orchestration)

Fabric **Data Factory Pipeline** orchestrates execution:

* Runs Bronze → Silver → Gold
* Parameterized:

  * 📅 Start Date
  * 📅 End Date

✔️ Dynamic & reusable pipeline

---

## ⚙️ Environment

Custom Fabric **Environment**:

* Dependency management
* Consistent execution across environments

---

## 🗄️ Lakehouse

* Central storage using **OneLake**
* Stores:

  * Raw files (Bronze)
  * Delta tables (Silver & Gold)

---

## 📊 Reporting

Power BI dashboard built on top of Gold layer.

### Features:

* 🗺️ Earthquake map
* 🎚️ Date range slider
* 🎚️ Significance filter
* 📈 Interactive insights

---

## 🖼️ Screenshots

### 🔄 Pipeline Execution

![Pipeline](Screenshots/pipeline.png)

### 🔁 Deployment Pipeline

![Deployment](Screenshots/deployment_pipeline.png)

### 📊 Power BI Dashboard

![Report](Screenshots/report.png)

---

## 🛠️ Tech Stack

* **Microsoft Fabric**

  * Lakehouse
  * Notebooks (PySpark)
  * Data Factory Pipeline
  * Deployment Pipeline (CI/CD)
  * Environment
* **Delta Lake**
* **REST API (USGS)**
* **Power BI**

---

## 📦 Exported Assets

* Notebooks
* Pipeline
* Lakehouse
* Environment
* Report

✔️ Full project reproducibility

---

## 📌 Key Learnings

* Implementing Medallion Architecture
* Handling API-based ingestion
* Building parameterized pipelines
* Applying CI/CD in Fabric
* Managing multi-environment deployment

---

## ⚡ How to Run

1. Import assets into **Dev workspace**
2. Configure Lakehouse connections
3. Run pipeline with parameters:

   * Start Date
   * End Date
4. Validate in Test
5. Deploy to Prod via Deployment Pipeline

---

## 🚀 Future Improvements

* Incremental loading strategy
* Data quality framework
* Monitoring & alerting
* Git integration for version control

---

## ⭐ Support

If you found this project useful, give it a ⭐ on GitHub!

