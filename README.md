# nyc_mta_turnstile_data_spark
Spark project to analyze NYC MTA Turnstile Data
---
# 📂 Take-Home Assignment: NYC Subway Ridership Analysis with Spark

### **Objective**

Your task is to build a **data pipeline using Apache Spark (PySpark)** to process and analyze New York City subway ridership data. The goal is to demonstrate your ability to work with distributed data, perform data cleaning, transformations, and derive actionable insights from real-world data.

---

### **Dataset**

* **NYC MTA Turnstile Data (Weekly CSVs)**

  * Source: [NYC Open Data – Turnstile Usage](https://data.ny.gov/api/views/k7j9-jnct/rows.csv?accessType=DOWNLOAD)
  * Updated weekly by the MTA. Each file represents **one week of subway turnstile readings**.
  * For this assignment, download **2–4 weeks of data** to simulate a larger dataset for Spark processing.
  * Key columns: `STATION`, `DATE`, `TIME`, `ENTRIES`, `EXITS`, etc.

---

### **Assignment Tasks**

#### **1. Data Ingestion**

* Load multiple weekly CSVs into Spark DataFrames.
* Define schema explicitly or use schema inference.
* Combine all weeks into a single DataFrame for analysis.

#### **2. Data Cleaning & Preparation**

* Convert `DATE` and `TIME` fields into a proper timestamp column.
* Deduplicate rows if necessary.
* Calculate **daily entries and exits per station** (the raw data uses cumulative counts).

#### **3. Data Transformation / Analysis**

Answer the core question:

> **“What are the busiest subway stations and peak travel times in NYC?”**

To do this, you should:

* Aggregate ridership counts by **station**, **day of the week**, and **hour of the day**.
* Identify the **top 10 busiest stations overall**.
* Determine **peak commute windows** (e.g., weekday mornings vs evenings).

---

### **4. Deliverables**

* Spark code in **PySpark** (Jupyter Notebook or `.py` script).
* Well-commented transformations and analysis.
* A short summary (Markdown/README) of your approach, results, and insights.
* Optional: visualization of ridership trends using matplotlib or seaborn.

---

### **Stretch Goals (Optional)**

* Integrate external datasets, like **weather data** from NOAA, to analyze factors affecting ridership.
* Deploy the Spark pipeline on a cloud platform (Databricks Community Edition, AWS EMR, or GCP Dataproc).
* Save the processed data in **Parquet format** for efficient querying.

---

### **Expected Skills Demonstrated**

* Spark DataFrame API (PySpark) usage
* Data cleaning and transformation logic
* Aggregation and groupBy operations
* Clear documentation and reproducibility

---

### **Submission Format (for practice)**

* GitHub repository containing:

  * `/notebooks` or `/src`: Spark code
  * `README.md`: Description of dataset, pipeline steps, results, and insights
  * (Optional) `/output`: Processed data or plots

---
