# nyc_mta_turnstile_data_spark
Spark project to analyze NYC MTA Turnstile Data
---

# 📂 Take-Home Assignment: NYC Subway Ridership Analysis with Spark

### **Objective**

Your task is to build a small data pipeline using **Apache Spark (PySpark)** to process and analyze New York City subway ridership data. The goal is to demonstrate your ability to work with distributed data processing, perform data cleaning, apply transformations, and derive insights from real-world data.

---

### **Dataset**

* **NYC MTA Turnstile Data** (publicly available)

  * Source: [https://catalog.data.gov/dataset/mta-turnstile-data](https://catalog.data.gov/dataset/mta-turnstile-data)
  * Format: CSV
  * Size: \~50–100 MB per weekly file
  * Columns include station, date, time, entries, exits, etc.

Download at least **2–3 weeks of data** to simulate a larger dataset for Spark processing.

---

### **Assignment Tasks**

#### **1. Data Ingestion**

* Load the CSV files into Spark DataFrames.
* Apply schema inference or define a schema explicitly.
* Combine multiple weeks into a single DataFrame.

#### **2. Data Cleaning & Preparation**

* Convert date and time fields into a proper timestamp column.
* Deduplicate rows if necessary.
* Calculate *daily entries and exits* per station (since the raw data uses cumulative counters).

#### **3. Data Transformation / Analysis**

Answer the following **core business question**:

> **What are the busiest subway stations and peak travel times in NYC?**

To answer this, you should:

* Aggregate ridership counts by **station**, **day of week**, and **hour of day**.
* Identify the **top 10 busiest stations** overall.
* Determine **peak commute windows** (e.g., weekday mornings vs evenings).

#### **4. Deliverables**

* Spark code written in **PySpark** (Jupyter Notebook or `.py` script).
* Clean and well-commented transformations.
* A short summary (Markdown/README) of your approach and results.
* Optional: simple visualization of ridership trends (e.g., matplotlib or seaborn after converting to Pandas).

---

### **Stretch Goals (Optional, if time allows)**

* Integrate external weather data (e.g., NOAA datasets) to test if weather affects subway usage.
* Deploy your code to a cloud Spark environment (Databricks Community Edition, AWS EMR, GCP Dataproc, or Azure HDInsight).
* Store processed data in a **Parquet** format for efficient querying.

---

### **Expected Skills Demonstrated**

* Spark DataFrame API usage
* Data cleaning and transformation logic
* Aggregation and groupBy operations
* Clear documentation and reproducibility

---

📌 **Submission Format (for practice):**

* GitHub repository containing:

  * `/notebooks` or `/src`: Your Spark code
  * `README.md`: Description of dataset, pipeline steps, results, and insights
  * (Optional) `/output`: Processed data or plots

---
