
# Global Superstore Sales Performance Dashboard

## Project Overview
This capstone project is a comprehensive Business Intelligence solution designed for the executive team of Global Superstore, a fictional global retail giant. The goal was to transform raw, denormalized sales data into a professional, interactive dashboard that provides a business performance.

## Problem Statement
Global Superstore had a growing dataset of over 50,000 transactions but lacked a centralized reporting tool. Management relied on static spreadsheets, leading to:
* **Lack of Visibility**: Executives couldn't easily see Big Picture trends (YoY Growth) or drill down into specific regional performance.
* **Inefficiency**: Manual reporting was time consuming and prone to errors.
**The Solution:** A dynamic, one page Executive Dashboard built in Power BI that answers:
* Are we profitable?
* Which products and regions are driving growth?
* How does this year compare to last year?

## The ETL Process (Extract, Transform, Load)
The data journey began with raw CSV files containing messy, denormalized transaction records. I used Power Query to clean and structure the data.
* **Data Cleaning**: Removed duplicate rows, fixed data types, and handled null values.
* **Normalization:** The raw flat file was split into a Star Schema to optimize performance.
* **Fact Table:** Created Sales Table containing only transactional data.
* **Dimension Tables**: Extracted unique attributes into Customer, Product, and Location tables.
* Created a Surrogate Key (Location_Key) to accurately link sales to specific City State Country combinations.
* Generated a dynamic Date Table to support advanced Time Intelligence analysis.

## Data Modeling
Built a Star Schema with one to many relationships flowing from 
dimension tables to the fact table.

## Schema
<img width="1280" height="733" alt="schema " src="https://github.com/user-attachments/assets/ed0de26c-65e8-4068-86be-68ded36a26d1" />

## Created DAX
* Sales YoY % = Calculated year over year growth to show momentum.
* Sales Last Year = Used CALCULATE and SAMEPERIODLASTYEAR to create a dynamic benchmark.
* Profit Margin % = DIVIDE([Total Profit], [Total Sales])
* Top 5 Products = Used TOPN and RANKX to dynamically isolate high performers without manual filtering.

## Tools Used
* Power BI Desktop (Data Modelling, DAX, Visualization)
* Power Query (ETL, Data Cleaning)
* DAX (Time Intelligence, Calculated Measures)

<img width="1360" height="770" alt="Screenshot 2025-11-27 005610" src="https://github.com/user-attachments/assets/d7625b5a-ce73-4980-ab92-13b50d9f7e8e" />




