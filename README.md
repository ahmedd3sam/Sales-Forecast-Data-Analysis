# 📊 E-Commerce ETL Pipeline & Sales Analytics

## 📌 Project Overview
This project demonstrates an **end-to-end Data Analytics solution** starting from **unstructured JSON data** through **Python ETL processing**, **data modeling**, and **Power BI analytics**.

The goal is to transform raw e-commerce sales and forecast data into **clean, analytics-ready datasets** and provide **actionable business insights**.

---

## 🧠 Business Objectives
This solution answers the following business questions:

- Analyze **total sales performance** across different granularities (year, month, product, geography)
- Compare **sales in 2009 vs 2008**
- Identify **Top 10 products** and their share of total sales
- Compare **forecasted vs actual sales**
- Analyze **top customer behavior** and purchasing patterns
- Enable filtering by **Country and State** for sales teams

---

## 🏗️ Architecture Overview

Raw JSON Data
     ↓
Python ETL (Extract – Transform – Load)
     ↓
Clean CSV Fact & Dimension Tables
     ↓
Power BI Star Schema Model
     ↓
Interactive Dashboard & Analytics

🗂️ Project Structure
E-Commerce-ETL-Pipeline/
│
├── etl/
│   └── etl_pipeline.py        # Python ETL script
│
├── data/
│   ├── sales-part1.json       # Raw unstructured sales data
│   └── forecast.json          # Raw forecast data
│
├── output/
│   ├── fact_sales.csv
│   ├── fact_forecast.csv
│   └── dim_date.csv
│
├── powerbi/
│   └── Sales_Analytics.pbix   # Power BI dashboard
│
├── model/
│   └── data_model.png         # Star schema diagram
│
└── README.md

🔄 ETL Process (Python)

---

## ETL Process

### Extract
- Loaded raw sales and forecast data from JSON files
- Handled unstructured and column-oriented JSON formats

### Transform
- Converted raw JSON into structured DataFrames
- Cleaned column names and standardized data types
- Converted dates and numeric values
- Created a reusable Date dimension
- Prepared data for analytical modeling

### Load
- Exported clean data into CSV files
- Data is ready for Power BI or database ingestion

---

## Data Model
A **Star Schema** was implemented to ensure:
- Accurate aggregations
- High performance queries
- Simplified DAX calculations
- Dynamic filtering by geography and time

---

## Power BI Analytics

### Key Metrics & Insights
- Total Sales ($)
- Sales comparison between 2008 and 2009
- Year-over-Year growth
- Top 10 products and percentage contribution
- Forecast vs actual sales
- Top customer purchasing behavior

### Filtering
- Country
- State
- Year

---

## Technologies Used
- Python (Pandas, JSON)
- Power BI
- DAX
- Data Modeling (Star Schema)
- Git & GitHub

---

## Skills Demonstrated
- ETL development using Python
- Data cleaning and transformation
- Analytical data modeling
- Business-focused reporting
- Data visualization with Power BI

---

## Conclusion
This project reflects a real-world data analytics workflow, from handling unstructured data to delivering actionable insights for business stakeholders.

---

## Author
Ahmed Essam  
GitHub: https://github.com/ahmedd3sam
