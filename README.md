# Student Loan ETL Pipeline

An end-to-end **ETL pipeline** built using **Talend** and **PostgreSQL** to transform student loan operational data into a **dimensional data warehouse (star schema)** for loan default analytics.

This project demonstrates practical **data engineering and analytics engineering skills**, including schema design, ETL development, and warehouse modeling.

---

## Project Overview

The objective of this project is to design and implement a complete ETL workflow that:

- Ingests normalized **operational (source) data** into PostgreSQL  
- Uses **Talend ETL jobs** to clean, transform, and integrate data  
- Loads analytics-ready **dimension tables** and a **fact table**  
- Enables efficient analysis of **student loan default behavior**

All schemas, transformations, and pipelines are documented using screenshots included in this repository.

---

## Architecture Overview

### Operational Database Schema
The diagram below shows the **source PostgreSQL database schema**, representing normalized operational tables.

<img width="786" height="575" alt="image" src="https://github.com/user-attachments/assets/93be1815-a34a-4efc-9abe-de3722168f54" />

---

### Data Warehouse Schema (Star Schema)
The diagram below shows the **data warehouse star schema**, consisting of dimension tables and a central fact table.

<img width="860" height="514" alt="image" src="https://github.com/user-attachments/assets/394d9251-d036-481f-99eb-8250a6da9737" />

---

### End-to-End ETL Pipeline (Talend)
The diagram below shows the **complete Talend ETL pipeline**, from source extraction through transformations to warehouse loading.

<img width="1628" height="830" alt="image" src="https://github.com/user-attachments/assets/ffcf459d-bee9-438d-8982-9a79a5e3b3e8" />


---

## Tech Stack

- **ETL Tool:** Talend  
- **Database:** PostgreSQL  
- **Query Language:** SQL  
- **Version Control:** GitHub  

---

## Repository Structure

The repository is organized to clearly separate source data, ETL logic, and warehouse outputs:

- **architecture/**  
  High-level diagrams of the operational schema, data warehouse schema, and ETL pipeline.

- **sql_files/**  
  SQL scripts defining the operational and data warehouse schemas.

- **database_tables/**  
  Screenshots of PostgreSQL **source tables** before transformation.

- **datawarehouse_tables/**  
  Screenshots of **dimension and fact tables** after warehouse loading.

- **etl_jobs/**  
  Talend job screenshots showing:
  - tMap transformations  
  - Dimension table loads  
  - Fact table load pipelines  

---

## Source Database (Operational Layer)

The operational database consists of normalized tables representing student loan data, including:

bank, loan, student, school, repayment, regulation, collateral, guarantor, indicator, and indicates.

These tables represent the raw transactional layer prior to ETL processing.

---

## Data Warehouse Design

The analytics layer is modeled using a **star schema** to support analytical queries.

### Dimension Tables
dim_bank, dim_city, dim_date, dim_degree, dim_guarantor, dim_month, dim_riskvalue,  
dim_school, dim_schooltype, dim_state, dim_student, dim_year

### Fact Table
fact_loan_default

This design enables efficient joins and aggregations for loan default analysis.

---

## ETL Pipeline (Talend)

Each dimension and the fact table is populated using dedicated Talend jobs.

### ETL Design Highlights
- Extraction from PostgreSQL source tables  
- Transformations using **tMap** (joins, lookups, derived fields)  
- Data cleansing and standardization  
- Dimension tables loaded before the fact table  
- Fact table populated using surrogate keys from dimensions  

All ETL logic and flows are documented via screenshots in the `etl_jobs` folder.

---

## Key Skills Demonstrated

- End-to-end ETL pipeline development  
- Dimensional modeling (star schema)  
- Talend ETL design with complex tMap transformations  
- PostgreSQL schema design (operational and warehouse)  
- Clear, structured data engineering documentation  
