# Finance-Fraud-Analytics
Developed an end-to-end analytical pipeline to identify fraudulent credit card transactions and quantify financial exposure using SQL and Python.
SQL Window functions, High-value filtering
Language: Python (Pandas, NumPy, Matplotlib, Seaborn)
Database: SQL (DuckDB / BigQuery) for Window Functions
Environment: Google Colab / Jupyter Notebooks
import pandas as pd
import duckdb

# 1. Load the data
df = pd.read_csv('/content/fraudTest.csv')

# 2. Convert the time column to a proper format
df['trans_date_trans_time'] = pd.to_datetime(df['trans_date_trans_time'])

# 3. Connect DuckDB to the dataframe
con = duckdb.connect()
<img width="736" height="466" alt="image" src="https://github.com/user-attachments/assets/edb43426-c7e2-4613-8b7a-95826cce7944" />
<img width="920" height="666" alt="image" src="https://github.com/user-attachments/assets/22d44d7d-6ed9-480f-89da-82cb02f5509f" />

**Link for Google Colab:** https://colab.research.google.com/#scrollTo=HOFf7hl-36zv

**High-Value Risk Segmentation:** Performed a comparative analysis of fraud rates across transaction value buckets, identifying that High-Value transactions (>$500) accounted for [X]% of total losses.

**Merchant Category Profiling:** Engineered a risk-scoring matrix for merchant categories, discovering that [Category Name] had the highest concentration of fraudulent activity.

**Temporal Analysis:** Visualized "Peak Fraud Hours," identifying a 25% increase in suspicious activity between 11 PM and 3 AM.
