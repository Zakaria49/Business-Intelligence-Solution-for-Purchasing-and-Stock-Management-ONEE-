# Business-Intelligence-Solution-for-Purchasing-and-Stock-Management-ONEE-
This project focuses on designing and implementing a decision support system to improve purchasing and inventory management processes.  The solution simulates real-world enterprise data (SAP-like Excel sources) and transforms it into actionable insights using a complete BI pipeline.
# ⚡ BI System for Purchasing & Inventory Analysis

## 📌 Project Overview
This project was developed as part of my final-year internship at the **Office National de l’Électricité et de l’Eau Potable – Water Branch (ONEE-BO)**.

The objective was to design and implement a **complete Business Intelligence solution** to support decision-making in **purchasing and inventory management**.

The system bridges the gap between **operational ERP data (SAP)** and **strategic analytics**, enabling better visibility, control, and performance monitoring.

---

## 🎯 Business Problem
The existing system faced several limitations:
- Data scattered across multiple sources (Excel exports from SAP)
- Lack of centralized and reliable reporting
- Difficulty in tracking stock movements and purchase performance
- No proactive monitoring of stock-out risks

👉 This project addresses these challenges by building a **centralized and automated decision support system**.

---

## 🏗️ System Architecture

The solution follows a layered Business Intelligence architecture:

### 🔹 Architecture Diagram
📌 *Add your architecture diagram here (ETL → DWH → Power BI)*

![Architecture Diagram](C:\Users\Zakaria\Pictures\Screenshots\Architecture.png)

---

### 🔹 Architecture Description
1. **Data Sources**
   - Excel files simulating SAP data (Purchasing, Inventory, Products, Suppliers)

2. **ETL Layer (SSIS)**
   - Data extraction, transformation, and loading
   - Data quality checks and rejection management

3. **Data Warehouse (SQL Server)**
   - Constellation schema modeling
   - Optimized for analytical queries

4. **Visualization Layer (Power BI)**
   - Interactive dashboards
   - KPI tracking and decision support

---

## 🧩 Data Model (Constellation Schema)

### 🔹 Data Model Diagram
📌 *Add your Star/Galaxy schema diagram here*

![Data Model](C:\Users\Zakaria\Pictures\Screenshots\Star_Schema.png)

---

### 🔹 Fact Tables
- **Fact_Purchases**
  - Purchase Amount, Quantity, Unit Price

- **Fact_Stock_Movements**
  - Quantity In, Quantity Out, Stock Variation

---

### 🔹 Dimension Tables
- **Dim_Product** (Product ID, Name, Category)
- **Dim_Supplier** (Supplier ID, Name, Location)
- **Dim_Date** (Date, Month, Year, Quarter)
- **Dim_Warehouse** (Warehouse ID, Region, City)
- **Dim_Movement_Type** (Entry, Exit, Adjustment)

---

## 🔄 ETL Strategy (SSIS)

### 🔹 ETL Workflow Diagram
📌 *Add your SSIS workflow or ETL pipeline diagram here*

![ETL Process](docs/etl_flow.png)

---

### 🔹 ETL Process Description

#### 📥 Extraction
- Data extracted from Excel sources (SAP simulation)

#### 🔧 Transformation
- Data cleaning (handling nulls, formats)
- Data standardization
- Business rules validation

#### 🧠 Data Quality
- Rejected records stored in error tables
- Logging and traceability implemented

#### 📤 Loading

- **Dimensions**
  - Loaded using **SCD Type 1**
  - Overwrites old values (no history)

- **Fact Tables**
  - Incremental loading
  - Linked via surrogate keys

---

## 📊 Power BI Dashboards

### 🔹 Dashboard Overview
📌 *Add screenshots of your dashboards here*

![Dashboard 1](docs/screenshots/dashboard1.png)  
![Dashboard 2](docs/screenshots/dashboard2.png)

---

### 🔹 Features
- Interactive filtering (region, product, supplier)
- Drill-down analysis
- Real-time KPI monitoring

---

### 🔹 Key KPIs
- Total Purchase Amount
- Stock Levels
- Inventory Turnover
- Stock-out Risk Indicator
- Warehouse Utilization Rate

---

## 🛠️ Technologies Used

- **SQL Server** → Data Warehouse
- **SSIS** → ETL
- **Power BI** → Visualization
- **Excel** → Data Sources

---

## 🚀 How to Run the Project

1. Execute SQL scripts to create the database
2. Open SSIS project in Visual Studio
3. Update connection strings
4. Run ETL packages
5. Open Power BI file and refresh data

---

## 📁 Project Structure
