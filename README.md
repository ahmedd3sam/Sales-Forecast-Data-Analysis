📊 E-Commerce ETL Pipeline & Sales Analytics
📌 Project Overview

This project demonstrates an end-to-end Data Analytics solution starting from unstructured JSON data through Python ETL processing, data modeling, and Power BI analytics.

The objective is to transform raw e-commerce sales and forecast data into clean, analytics-ready datasets and provide business insights such as sales trends, year-over-year comparison, top products, customer behavior, and forecast vs actual analysis.

🧠 Business Objectives

The solution answers the following business questions:

What is the total sales performance at different granularities (year, month, product, geography)?

How do sales in 2009 compare to 2008?

Which are the Top 10 products and their contribution to total sales?

How does forecasted sales compare to actual sales?

Who is the top customer, and how do their purchases behave over time?

Enable the sales team to filter insights by Country and State.

🏗️ Architecture Overview
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
1️⃣ Extract

Loaded raw JSON files using Python

Handled column-oriented JSON structure in sales data

Read forecast data stored as a list of JSON objects

2️⃣ Transform

Converted unstructured JSON into row-based DataFrames

Cleaned column names and removed unnecessary whitespace

Converted data types:

Dates → datetime

Numeric values → float / int

Handled missing or invalid values

Created a Date Dimension for analytical slicing

3️⃣ Load

Exported cleaned data into CSV files

Data is ready for Power BI or relational databases

🧾 Output Tables
📌 Fact Tables

fact_sales

SalesAmount

OrderQuantity

OrderDate

ProductKey

CustomerKey

Geography attributes

fact_forecast

CountryRegion

Brand

Year

Forecast Amount

📌 Dimension Tables

dim_date

Date

Year

Month

Month Name

⭐ Data Modeling

A Star Schema is used to ensure:

High performance

Clean relationships

Accurate aggregations

Easy filtering by geography and time

Shared Date Dimension enables comparison between:

Actual Sales

Forecasted Sales

📊 Power BI Analytics & Measures
🔹 Key DAX Measures
Total Sales ($) :=
SUM ( FactSales[SalesAmount] )

Sales 2008 :=
CALCULATE ( [Total Sales ($)], DimDate[Year] = 2008 )

Sales 2009 :=
CALCULATE ( [Total Sales ($)], DimDate[Year] = 2009 )

YoY Growth % :=
DIVIDE ( [Sales 2009] - [Sales 2008], [Sales 2008] )

Total Forecast :=
SUM ( FactForecast[Forecast] )

% of Total Sales :=
DIVIDE (
    [Total Sales ($)],
    CALCULATE ( [Total Sales ($)], ALL ( DimProduct ) )
)

📈 Dashboard Features

Total Sales KPIs

Sales Trend over Time

Sales 2008 vs 2009 Comparison

Top 10 Products & % Contribution

Forecast vs Actual Comparison

Top Customer Purchase Behavior

Dynamic filtering by:

Country

State

Year

📌 Single-page dashboard designed for business users.

🛠️ Technologies Used

Python (Pandas, JSON)

Power BI

DAX

Data Modeling (Star Schema)

GitHub

🎯 Key Skills Demonstrated

ETL Development

Data Cleaning & Transformation

Analytical Thinking

Data Modeling

DAX & Power BI

Business-oriented reporting

📌 Conclusion

This project simulates a real-world analytics workflow, handling unstructured data and transforming it into meaningful insights for decision-makers. It highlights strong foundations in data engineering, analytics, and visualization.

If you want, next I can:

🔹 Customize this README specifically for Orion Digital Solutions

🔹 Shorten it for recruiter scanning

🔹 Review your repo structure & naming

🔹 Help you write a LinkedIn post linking this project

Just tell me 🚀
