# student-loan-etl-pipeline

An end-to-end **ETL pipeline** built using **Talend** and **PostgreSQL** to transform student loan operational data into a **dimensional data warehouse (star schema)** for loan default analytics.

This project demonstrates real-world **data engineering and analytics engineering practices**, including schema design, ETL orchestration, and warehouse loading.

---

## Project Overview

The pipeline performs the following steps:

1. Loads normalized **operational/source tables** into PostgreSQL  
2. Transforms and enriches data using **Talend ETL jobs**
3. Loads clean, analytics-ready **dimension tables** and a **fact table**
4. Produces a star-schema data warehouse optimized for reporting and analysis

---

## Architecture Overview

### Operational Database Architecture
The diagram below shows the normalized PostgreSQL source schema used as input to the ETL pipeline.

![Operational Database Architecture](architecture/database_architecture.png)

---

### Data Warehouse Architecture
The analytics layer follows a **star schema** design, with multiple dimension tables connected to a central fact table.

![Data Warehouse Architecture](architecture/datawarehouse_architecture.png)

---

### End-to-End ETL Pipeline
This diagram shows the complete Talend ETL flow from source tables through transformations to warehouse loading.

![ETL Pipeline Overview](architecture/etl_pipeline_overview.png)

---

## Tech Stack

- **ETL Tool:** Talend  
- **Database:** PostgreSQL  
- **Query Language:** SQL  
- **Version Control:** GitHub  

---

## Repository Structure

```text
student-loan-etl-pipeline/
├── README.md
│
├── architecture/
│   ├── database_architecture.png
│   ├── datawarehouse_architecture.png
│   └── etl_pipeline_overview.png
│
├── sql_files/
│   ├── 01_operational_schema.sql
│   ├── 02_modifications.sql
│   └── 03_datawarehouse_schema.sql
│
├── database_tables/
│   └── Screenshots of source (operational) tables
│
├── datawarehouse_tables/
│   └── Screenshots of dimension and fact tables
│
└── etl_jobs/
    └── Talend job screenshots (tMap + load jobs)
