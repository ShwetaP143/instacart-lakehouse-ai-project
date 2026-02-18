# 🛒 Instacart Lakehouse Analytics Project (Databricks)

## 📌 Project Overview
This project is an end-to-end Data Engineering and Analytics solution built on the Databricks Lakehouse platform using Medallion Architecture (Bronze, Silver, Gold).

The goal of this project is to process large-scale Instacart Market Basket Analysis data (30M+ records) and generate meaningful business insights such as customer reorder behavior, top products, and department-level analytics.

This project was developed as part of the Databricks AI Challenge to demonstrate a real-world Lakehouse implementation using Serverless Databricks and Unity Catalog.

---

## 🎯 Problem Statement
E-commerce companies like Instacart generate massive transactional data.  
The challenge is to design a scalable data pipeline that:
- Ingests raw large-scale data
- Cleans and transforms it
- Builds analytical models
- Generates business KPIs for decision-making

This project solves this by implementing a production-style Lakehouse architecture on Databricks.

---

## 🏗️ Architecture (Medallion Architecture)
This project follows the industry-standard Medallion Architecture:

- 🥉 Bronze Layer → Raw Data Ingestion (Delta Tables)
- 🥈 Silver Layer → Data Cleaning & Transformation
- 🥇 Gold Layer → Star Schema & Business Analytics

Platform Used:
- Databricks Serverless
- Unity Catalog
- Delta Lake

---

## 🧰 Tech Stack
- Databricks (Serverless)
- PySpark
- SQL (Databricks SQL Editor)
- Delta Lake
- Unity Catalog (Managed Tables)
- Kaggle Dataset (Instacart)
- Git & GitHub (Version Control)

---

## 📂 Project Structure
instacart-lakehouse-ai-project/
│
├── data/ # Dataset references
├── docs/ # Documentation & architecture
├── notebooks/ # ETL notebooks (Bronze, Silver, Gold, DQ)
├── src/ # Transformation logic (future scalable code)
├── tests/ # Data quality logic
├── README.md # Project documentation
└── .gitignore


---

## 📊 Dataset Information
Dataset: Instacart Market Basket Analysis (Kaggle)  
Size: 30+ Million Records  

Files Used:
- orders.csv (3.4M rows)
- order_products__prior.csv (32M rows)
- order_products__train.csv
- products.csv
- aisles.csv
- departments.csv

The dataset was ingested using Kaggle API into Unity Catalog Volumes.

---

## 🥉 Bronze Layer – Raw Data Ingestion
In this layer, raw CSV files were ingested into Delta tables without transformation.

Key Features:
- Data stored in Unity Catalog Volumes
- Large-scale ingestion (30M+ rows)
- Schema inference
- Managed Delta Tables creation

Bronze Tables:
- orders
- products
- departments
- aisles
- order_products__prior
- order_products__train

---

## 🥈 Silver Layer – Data Cleaning & Transformation
The Silver layer focuses on data standardization and cleaning.

Transformations Performed:
- Handling malformed values using safe casting
- Null value validation
- Schema standardization
- Data type corrections
- Deduplication logic

Outcome:
- Clean, structured, analytics-ready tables
- Improved data quality and consistency

---

## 🥇 Gold Layer – Analytics & Star Schema
Gold layer contains business-ready data models optimized for analytics and BI tools.

Data Model:
- Fact Table: `fact_order_items`
- Dimension Table: `dim_products`
- KPI Tables: Analytical aggregated tables

Business KPIs Generated:
- Total Orders
- Top Selling Products
- Reorder Rate Analysis
- Department-wise Performance
- Customer Purchase Behavior

---

## 🔍 Data Quality Checks (Production-Level)
Implemented validation framework to ensure data reliability:

Checks Performed:
- Null value checks on critical columns
- Duplicate record detection
- Row count consistency (Bronze vs Gold)
- Data integrity validation

Results:
- 0 critical null values
- No major duplicates
- Consistent row counts across layers
- Reliable analytical dataset

---

## 📈 Analytical Queries (SQL Editor)
Created dedicated SQL analytics notebook:
`05_gold_analytics_queries`

Sample Queries:
- Total Orders Count
- Top Products KPI
- Reorder Rate KPI
- Department-wise Order Analysis
- Customer Behavior Analysis

All queries executed successfully on Gold layer tables.

---

## 🚀 How to Run the Project (Step-by-Step)
1. Upload Instacart dataset to Unity Catalog Volume
2. Run 01_raw_data_landing notebook
3. Run 02_bronze_ingestion notebook
4. Run 03_silver_transformation notebook
5. Run 04_gold_analytics notebook
6. Run 05_gold_analytics_queries (SQL Editor)
7. Run 06_data_quality_checks notebook

---

## 💡 Key Project Highlights
- End-to-End Lakehouse Pipeline
- 30+ Million Records Processed
- Unity Catalog Managed Tables
- Serverless Databricks Implementation
- Medallion Architecture (Industry Standard)
- Star Schema Data Modeling
- Data Quality Validation Layer
- Portfolio-Ready Real-World Project

---

## 📊 Use Cases
- Business Intelligence Dashboards (Power BI / Tableau)
- Customer Behavior Analysis
- Product Recommendation Insights
- Reorder Prediction (Future ML Extension)
- Scalable Data Engineering Pipeline Design

---

## 👩‍💻 Author
**Shweta Pawar**  
Aspiring Data Analyst | Databricks Lakehouse Project  

GitHub: https://github.com/ShwetaP143  

Background:
- Java Developer transitioning into Data Analytics
- Experience with SQL, PySpark, Databricks, and Data Engineering concepts

---

## 🏆 Challenge Submission Note
This project was built as a complete real-world solution for the Databricks Hands-On Project Challenge, showcasing:
- Problem Definition
- Large Dataset Handling
- End-to-End Architecture
- Documentation
- GitHub Version Control
- Analytical Insights

---

## ⭐ Future Enhancements
- Machine Learning (Reorder Prediction Model)
- Real-time Streaming Pipeline
- Power BI Dashboard Integration
- Automated CI/CD for Data Pipelines

