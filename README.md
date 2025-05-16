# 🏡 Home Sales Analysis with PySpark
This project analyzes home sales data using PySpark to demonstrate SQL-based querying, performance optimization (via caching and Parquet), and aggregation techniques.

## 📊 Objectives
- Calculate average home prices based on various features.

- Explore how features like bedrooms, bathrooms, square footage, and view ratings impact pricing.

- Compare query performance between uncached, cached, and Parquet formats.

## 🧪 Data Source
Dataset:
home_sales_revised.csv
Fields include: sale date, price, bedrooms, bathrooms, square footage, lot size, floors, waterfront status, view score, and year built.

## 🔍 Key Analysis Results
1. Average Price for 4-Bedroom Homes by Year Sold
Year	Avg Price
2019	$300,263.70
2020	$298,353.78
2021	$301,819.44
2022	$296,363.88

### 💡 Prices remained relatively stable across the years.

2. Avg Price for Homes with 3 Beds and 3 Baths by Year Built
Year Built	Avg Price
2010–2017	$288,770 – $295,962

### 🔍 Consistent pricing regardless of build year in this range.

3. Avg Price: 3 Beds / 3 Baths / 2 Floors / ≥2000 sqft
Year Built	Avg Price
2010–2017	$276,554 – $307,540

### 📈 Slightly higher pricing due to larger and multi-story homes.

4. Avg Price by View Score (Only ≥ $350K Averages)
View Rating	Avg Price
81–100	$970,402 – $1,137,373

### 🌄 View rating is a strong price driver—higher view scores correlate with higher home values.

## ⚙️ Performance Comparison
Query Type	Runtime (seconds)
Uncached	1.84
Cached	2.56
Parquet	1.84

## 🧠 Parquet performed best, matching uncached SQL speeds, while caching actually added time for this dataset size.

## 🧰 Tools & Technologies
- Python & PySpark

- Apache Spark 3.5.5

- Google Colab environment

- Parquet format for efficient data storage

## 📦 How to Run
Load and preview the dataset.

Register the DataFrame as a temporary SQL view.

Run SQL queries to extract insights.

Cache the table and compare performance.

Write and read data as Parquet.

Repeat queries and compare runtimes.

## 📈 Conclusions
View rating is the most significant factor influencing price.

Parquet format offers efficient performance with minimal setup.

Caching benefits larger datasets with multiple repeated queries.

PySpark is a powerful tool for large-scale SQL-based data analysis.

## References
Assigment was prepared using the starter file provided and referencing prior class activities and ChatGPT.  