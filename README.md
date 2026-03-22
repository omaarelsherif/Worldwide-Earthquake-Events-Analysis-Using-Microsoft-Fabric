# Worldwide Earthquake Events Analsis Using Microsoft Fabric

An end-to-end **Data Engineering project** built using **Microsoft Fabric**, implementing a full **Medallion Architecture (Bronze → Silver → Gold)** with **CI/CD using Fabric Deployment Pipelines**.

---

## 🚀 Overview

This project ingests real-time earthquake data from the **USGS API**, processes it through layered transformations, and delivers interactive insights via Power BI.

### 🔑 Highlights:

* API-based ingestion (real-world scenario)
* Medallion architecture using Lakehouse
* Parameterized pipeline orchestration
* Full Fabric asset export
* CI/CD using Deployment Pipelines (Dev → Test → Prod)
* Interactive reporting with filters and map visualization

---

## 🗂️ Repository Structure

```id="repo123"
📦 Main
 ┣ 📂 Notebooks
 ┃ ┣ 📜 Earthquake Events API - Bronze Layer.ipynb
 ┃ ┣ 📜 Earthquake Events API - Silver Layer.ipynb
 ┃ ┗ 📜 Earthquake Events API - Gold Layer.ipynb
 ┣ 📂 Pipeline
 ┃ ┗ 📜 Earthquake Data Pipeline.zip
 ┣ 📂 Report
 ┃ ┗ 📜 Worldwide Earthquakes Events.pbix
 ┣ 📂 Raw Data
 ┃ ┗ 📜 2026-03-21_earthquake_data.json
 ┣ 📂 Screenshots
 ┃ ┣ 📸 Architecture.png
 ┃ ┣ 📸 Pipeline.png
 ┃ ┣ 📸 Report.png
 ┃ ┗ 📸 Deployment_pipeline.png
 ┗ 📜 README.md
```

---

## 🧱 Architecture
The below diagram shows project architecture

---

## 🥉 Bronze Layer — Ingestion

* Source: **USGS Earthquake API**
* Tool: Fabric Notebook (Python Requests)

✔️ Stores raw JSON data in Lakehouse

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

## 📊 Reporting

Power BI dashboard built on top of Gold layer.

### Features:

* 🗺️ Earthquake map
* 🎚️ Date range slider
* 🎚️ Significance filter
* 📈 Interactive insights

---

## 🔁 CI/CD — Deployment Pipeline

This project implements **CI/CD using Fabric Deployment Pipelines** across three environments as below snapshot:

---

## 📌 Key Learnings

* Implementing Medallion Architecture
* Handling API-based ingestion
* Building parameterized pipelines
* Applying CI/CD in Fabric
* Managing multi-environment deployment
