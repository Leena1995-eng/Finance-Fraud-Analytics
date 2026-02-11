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
