# 🏦 Bank Customer Segmentation & Data Warehouse Project

---

## 📌 Project Overview

This project focuses on transforming raw banking transaction data into a structured and analysis-ready format using data engineering and data warehousing principles.

The goal is to build a scalable data model that supports customer segmentation, financial analysis, and business intelligence use cases.

---

## 🎯 Objectives

- Clean and standardize raw transactional data  
- Handle missing and inconsistent values using business-driven logic  
- Perform feature engineering (e.g., Age, High Balance segmentation)  
- Prepare data for Data Warehouse (DWH) ingestion  
- Design a dimensional model (Star Schema) for analytics  

---

## 🔄 Data Pipeline

The project follows a structured data pipeline:

Raw Data → Data Cleaning → Feature Engineering → Processed Layer → Data Warehouse


---

## 🧹 Data Cleaning & Preparation

Key steps performed:

- Standardized column names for SQL compatibility  
- Converted date fields into proper datetime format  
- Fixed incorrect date-of-birth values (century correction)  
- Derived customer age from DOB  
- Handled missing values:
  - Gender → filled with "Unknown"
  - Location → standardized & filled
  - Account Balance → imputed using median
- Removed unrealistic values using business rules  
- Ensured primary key uniqueness (TransactionID)  

---

## 📊 Exploratory Data Analysis (EDA)

- Identified highly skewed distribution in account balances  
- Applied log transformation to reveal underlying distribution  
- Observed log-normal behavior common in financial datasets  
- Created high-value customer segmentation using quantile thresholds  

---

## 🧱 Data Warehouse Design (Planned)

The project follows Kimball methodology:

### Fact Table
- `fact_transactions` → transaction-level data  

### Dimension Tables
- `dim_customer` → customer attributes (age, gender, location)  
- `dim_date` → date hierarchy (day, month, year)  

---

## ⚙️ Technologies Used

- Python (Pandas, NumPy)  
- Jupyter Notebook  
- SQL (PostgreSQL-ready schema design)  
- Git & GitHub  

---

## 🚀 Next Steps

- Build dimensional tables (dim_customer, dim_date)  
- Create fact table (fact_transactions)  
- Load data into PostgreSQL  
- Develop analytical queries (P&L, segmentation, KPIs)  
- Build a Power BI dashboard for business insights  

---

## 💡 Future Vision

The final goal of this project is to create a complete end-to-end analytics solution:

- Data ingestion  
- Data warehouse modeling  
- Business intelligence reporting  
- Decision-support system for financial analysis  

---

## 👤 Author

Eser Karaceper  
Senior BI & Data Analyst | Power BI, SQL, Data Modeling  
