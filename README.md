# ☁️ Azure Insurance Data Pipeline

## 📊 Cloud Data Pipeline & Analytics Layer Simulation

This project demonstrates how raw operational datasets can be ingested, structured, and prepared for analysis using Microsoft Azure services. The goal was to simulate the early stages of a modern analytics platform, focusing on the layers that prepare data for downstream reporting and business intelligence tools.

The pipeline moves raw insurance datasets through a cloud architecture where they are structured into staging tables and transformed into curated analytics views.

---

# 🏗 Architecture

The pipeline architecture follows a simplified enterprise analytics workflow:

Azure Blob Storage → Azure Data Factory → Azure SQL Database → Analytics SQL Views → Reporting / BI Tools

Raw datasets are stored in cloud storage, orchestrated through a data pipeline, loaded into a structured SQL warehouse, and then transformed into curated datasets for analysis.

---

# 🎯 Project Objectives

- Simulate a cloud-based analytics data pipeline  
- Implement automated data ingestion using Azure Data Factory  
- Structure raw datasets into relational tables within Azure SQL Database  
- Create a layered warehouse architecture using staging and analytics schemas  
- Prepare curated datasets suitable for business intelligence reporting  

---

# 🧰 Technologies Used

### ☁️ Cloud Platform
- Microsoft Azure

### 💾 Data Storage
- Azure Blob Storage

### ⚙️ Pipeline Orchestration
- Azure Data Factory

### 🗄 Data Warehouse
- Azure SQL Database

### 🧮 Query Language
- SQL

---

# 🔄 Data Pipeline Workflow

## 1️⃣ Data Ingestion

Raw datasets representing insurance operations were stored in Azure Blob Storage. These datasets included information such as:

- policies  
- claims  
- premium transactions  
- customer records  
- underwriters  
- catastrophe events  
- state and date dimensions  

---

## 2️⃣ Pipeline Orchestration

Azure Data Factory pipelines were created to orchestrate ingestion of the datasets into the SQL warehouse.

Each dataset was loaded through dedicated **Copy Data activities**, automatically transferring data from Azure Blob Storage into staging tables in Azure SQL Database.

Pipeline features included:

- automated dataset ingestion  
- pipeline monitoring and run validation  
- centralized orchestration of data movement  

---

## 3️⃣ Staging Layer (Azure SQL Database)

A **staging schema** was implemented to store structured raw data once it was loaded from the pipeline.

Example staging tables include:

- `staging.fact_policies`
- `staging.fact_claims`
- `staging.fact_premium_transactions`
- `staging.dim_customer`
- `staging.dim_underwriter`
- `staging.dim_date`
- `staging.dim_state`
- `staging.dim_adjuster`

This layer preserves raw structured data before analytical transformations are applied.

---

## 4️⃣ Analytics Layer

An **analytics schema** was created to support downstream analysis.

Curated SQL views were developed to combine relevant datasets and structure them for reporting use cases.

Example analytics views include:

- `analytics.vw_policy_detail`
- `analytics.vw_claim_detail`
- `analytics.vw_premium_detail`
- `analytics.vw_executive_summary`

These views prepare the data for potential consumption by reporting tools such as Power BI.

---

# 🖼 Project Visuals

### Azure Data Factory Pipeline
![Azure Data Factory Pipeline](visuals/azure%20data%20factory.png)

### Azure SQL Database (VS Code Connection)
![Azure SQL VS Code](visuals/Azure%20Sql%20Server%20Vs%20code.png)

### SQL Warehouse Tables
![Azure SQL Tables](visuals/Azure%20Sql%20Server%20Wo%20Views.png)

### Azure SQL Resource Overview
![Azure SQL Resource](visuals/azure%20sql%20server.png)

---

# 📁 Repository Structure

```
azure-insurance-data-pipeline

README.md
LICENSE

visuals/
    azure data factory.png
    Azure Sql Server Vs code.png
    Azure Sql Server Wo Views.png
    azure sql server.png
```

The visuals folder contains screenshots demonstrating the pipeline, SQL environment, and data warehouse layers used in the project.

---

# 🔎 Example System Flow

Insurance CSV Files  
↓  
Azure Blob Storage  
↓  
Azure Data Factory Pipeline  
↓  
Azure SQL Database (Staging Tables)  
↓  
Analytics SQL Views  
↓  
Reporting / Business Intelligence Tools

---

# 🧠 Key Skills Demonstrated

- Cloud data pipeline development  
- Azure Data Factory orchestration  
- SQL warehouse schema design  
- Staging vs analytics data layering  
- SQL view development for reporting  
- End-to-end analytics system architecture  

---

# 🚀 Purpose of the Project

The objective of this project was to gain hands-on experience designing the **data foundation that supports analytics systems**.

Rather than focusing on visualization, the emphasis was placed on building the **pipeline and warehouse layers that ensure data is structured, reliable, and ready for downstream analysis**.
