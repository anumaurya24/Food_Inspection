
# 🍽️ **Chicago & Dallas Food Inspection Pipeline**

### *End-to-End ETL • Data Quality • Delta Live Tables • Power BI Dashboard*

This project implements a complete **data engineering pipeline** for analyzing food inspection data from **Chicago** and **Dallas**. The workflow covers **data ingestion, transformation, validation, modeling, and visualization**, following Medallion Architecture principles using **Bronze → Silver → Gold** layers.

The repo includes:

* ✔️ **Delta Live Tables (DLT) pipeline** for ETL & data quality
* ✔️ **ER/Dimensional data model** for downstream analytics
* ✔️ **Interactive Power BI dashboard** with insights
* ✔️ **Full end-to-end process**, ready for enterprise-scale data pipelines

---

## 🚀 **Project Overview**

Many U.S. cities publish food inspection datasets, but schemas differ widely.
This project **consolidates Chicago and Dallas inspection data** into a unified analytical model by:

1. **Profiling and cleansing raw delimited files**
2. **Applying validation rules and schema alignment**
3. **Building ETL pipelines using Delta Live Tables**
4. **Creating a dimensional model (ER Studio)**
5. **Delivering business insights through Power BI**

---

## 🏗️ **Architecture**

### **Medallion Architecture:**

```
Bronze  →  Silver  →  Gold
Raw        Cleaned     Analytics-Ready Tables
```

### **Pipeline Components**

| Layer      | Description                                                                       |
| ---------- | --------------------------------------------------------------------------------- |
| **Bronze** | Raw ingestion of Chicago & Dallas CSV files using Databricks Auto Loader          |
| **Silver** | Cleansing, schema normalization, type casting, null handling, and DQ checks       |
| **Gold**   | Dimensional model (dim_facility, dim_address, fact_inspection) for BI consumption |

---

## 📁 **Repository Structure**

```
Food_Inspection/
│
├── FoodInspectionDLT.ipynb            # Databricks Delta Live Tables ETL pipeline
├── er model-FoodInspection-.DM1       # ER/Studio Dimensional Model
├── Food_Inspection_Dashboard.pbix     # Power BI interactive dashboard
└── README.md                           # Project documentation
```

---

## 🔧 **Technologies Used**

* **Databricks** (Delta Live Tables, Auto Loader, Spark SQL)
* **Python** for transformations
* **Delta Lake** for ACID, versioning, schema evolution
* **Power BI** for data visualization
* **ER/Studio** for dimensional modeling
* **SQL** for data cleaning & modeling

---

## 🔍 **Key Features**

### ✔ **1. Data Ingestion**

* Ingests CSV files from two different city datasets
* Handles schema differences automatically

### ✔ **2. Data Quality Checks**

Built into DLT pipeline:

* Completeness (null threshold)
* Uniqueness / duplicate detection
* Out-of-range values
* Schema drift identification
* Referential integrity between dimensions/facts

### ✔ **3. Dimensional Modeling**

Designed a **star schema** including:

* `dim_facility`
* `dim_location`
* `dim_violation`
* `fact_inspection`

### ✔ **4. Power BI Dashboard**

Provides insights such as:

* Violations trends
* Risk level distribution
* Inspection frequency
* City-level comparisons
* High-risk facilities

---

## 📊 **Screenshots (Optional to Add)**

You can upload and embed dashboard/architecture images here.

---

## 📦 **How to Run**

### **1. Import the notebook**

Upload `FoodInspectionDLT.ipynb` into Databricks workspace.

### **2. Create a DLT Pipeline**

* Choose **Notebook Pipeline**
* Set target database: `food_inspection_project`
* Set storage location: `/Volumes/.../food_inspection`
* Run pipeline

### **3. Connect Power BI**

* Export Gold-layer tables to Power BI
* Open `Food_Inspection_Dashboard.pbix`

---

## 📘 **ER Model**

The `.DM1` file contains the full conceptual + logical schema built using ER/Studio, matching the Gold-layer output.

---

## 🙌 **Contributors**

* **Ananya Maurya** — Data Engineering, ETL, Modeling, Dashboards
* **Nitish Chowdary K** — Project Support

---

## ⭐ **Future Enhancements**

* Add Great Expectations for advanced data quality
* Automate dashboard refresh
* Deploy orchestration via Airflow / ADF
* Add unit tests for pipeline validation

---

# 🎉 **If you want, I can also generate:**

✔ A professional project description for your **resume**
✔ A **LinkedIn post** showcasing this project
✔ An **architecture diagram**
✔ A **GIF animation** of the pipeline flow

Just tell me **“make project summary”** or **“make LinkedIn post”**.
