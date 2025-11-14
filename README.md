# Lakehouse ELT with Delta, PySpark, and dbt
Gold Price ETL Pipeline – An end-to-end data engineering project that ingests daily gold prices from Yahoo Finance, cleans and enriches the data, and produces analytics-ready monthly aggregates using Delta Lake and PySpark.

## Get Started
In your .venv   
```
pip install poetry
```
```
poetry install
```

## Diagram
```
[Raw Data / Bronze Parquet]
          │
          ▼
   PySpark Transformations
          │
          ▼
[Silver Delta Table] -- (Incremental / ACID)
          │
          ▼
         dbt Models
          │
          ▼
[Gold Delta Table / Aggregates]
          │
          ▼
   Streamlit Dashboard / Analytics
```
