# 🏦 Bank Customer Segmentation & Data Warehouse Project

---

## 📌 Project Overview

This project builds an end-to-end **data warehouse and analytical pipeline** for banking transaction data.

Raw transactional data is transformed into a **Kimball-based dimensional model**, enriched with business logic, and prepared for **customer behavior analysis and BI reporting**.

---

## 🎯 Objectives

- Clean and standardize raw financial transaction data  
- Design and implement a **Star Schema Data Warehouse**  
- Enrich data with **business-driven features**  
- Perform **behavioral transaction classification**  
- Enable **analytics-ready datasets for BI tools**

---

## 🔄 Data Pipeline

Raw Data → Data Cleaning → Feature Engineering → Data Warehouse → Enrichment → Analytics Ready


---

## 🧹 Data Cleaning & Preparation

Key transformations:

- Standardized schema for SQL compatibility  
- Corrected invalid date-of-birth values  
- Derived **customer age**  
- Handled missing values:
  - Gender → "Unknown"
  - Location → standardized
  - Balance → median imputation  
- Removed unrealistic values using domain rules  
- Ensured **primary key integrity**

---

## 🧱 Data Warehouse Design (Kimball)

### Fact Table
- `fact_transactions` → transaction-level grain  

### Dimension Tables
- `dim_customer` → demographic attributes  
- `dim_date` → calendar hierarchy  
- `dim_location` → geographical attributes  

✔ Fully implemented with **PK/FK constraints**

---

## ⚡ Data Enrichment

### 👥 Customer Enrichment
- Household simulation  
- Marital status derivation  
- Account status classification (Active / Suspended / Closed)

---

### 💳 Transaction Enrichment

Transactions were classified into behavioral categories using a hybrid approach:

#### 🔹 Recurrence Detection
- Repeated transactions (≥2) identified per customer  
- Highest recurring amount → **Loan Payment**  
- Smaller recurring amounts → **Bill Payment**

#### 🔹 Distribution-Based Classification
- `< 1500` → Purchase  
- `>= 1500` → Transfer  

✔ Combines **pattern detection + statistical thresholds**

---

## 📊 Key Outcomes

- Built a fully functional **Data Warehouse (PostgreSQL-ready)**  
- Created **behavioral transaction segmentation**  
- Enabled:
  - Customer analysis  
  - Financial pattern detection  
  - BI-ready datasets  

---

## ⚙️ Technologies Used

- Python (Pandas, NumPy)  
- SQL (PostgreSQL)  
- Jupyter Notebook  
- Git & GitHub  

---

## 🚀 Next Steps

- Build **Data Mart layer (aggregations)**  
- Develop **Power BI dashboards**  
- Perform **customer behavior analysis**  
- Implement advanced segmentation (RFM, clustering)

---

## 💡 Future Vision

- Customer Lifetime Value (CLV)
- Fraud / anomaly detection
- Predictive segmentation models

---

## 👤 Author

**Eser Karaceper**  
Senior BI & Data Analyst  
Power BI | SQL | Data Modeling
