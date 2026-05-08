Designed and implemented an end-to-end Medallion Architecture pipeline in Databricks using Delta Live Tables (DLT), Spark SQL API, and Delta Lake. Built Bronze, Silver, and Gold layers for scalable data ingestion, transformation, and aggregation. Implemented Slowly Changing Dimension (SCD) Type 1 and Type 2 logic using APPLY CHANGES INTO on Delta Streaming Tables for efficient CDC and historical data tracking. Configured and optimized Databricks clusters for pipeline execution and performance tuning. Integrated Git-based version control for pipeline management and deployment workflows.
 
Implemented a Medallion Architecture pipeline using Databricks Delta Live Tables (DLT), PySpark, and Delta Lake. Developed Bronze, Silver, and Gold layers with SCD Type 1 and Type 2 implementation using APPLY CHANGES INTO on Delta Streaming Tables. Configured Databricks clusters for scalable pipeline execution and integrated GitHub for version control.
 
Built a Databricks DLT Medallion Architecture pipeline with Bronze, Silver, and Gold layers, implementing SCD Type 1 and Type 2 using APPLY CHANGES INTO on Delta Streaming Tables, along with cluster configuration and Git integration.
 
# Databricks Delta Live Tables (DLT) Pipeline
 
## Project Overview
 
This project demonstrates an end-to-end Medallion Architecture pipeline built using Databricks Delta Live Tables (DLT), PySpark, and Delta Lake.
 
The pipeline processes data through multiple layers:
 
- Bronze Layer → Raw data ingestion
- Silver Layer → Cleansed and transformed data
- Gold Layer → Business-ready aggregated data
 
## Features Implemented
 
- Delta Live Tables (DLT)
- Medallion Architecture
- Delta Streaming Tables
- SCD Type 1 and SCD Type 2
- APPLY CHANGES INTO
- Change Data Capture (CDC)
- Incremental Data Processing
- Data Quality Validations
- GitHub Version Control Integration
- Databricks Cluster Configuration
 
## Technologies Used
 
- Databricks
- PySpark
- Delta Lake
- Delta Live Tables (DLT)
- SQL
- Git & GitHub
 
## Pipeline Architecture
 
```text
Source Data
     ↓
Bronze Layer
     ↓
Silver Layer
     ↓
Gold Layer
```
 
## SCD Implementation
 
Implemented Slowly Changing Dimension (SCD) Type 1 and Type 2 using APPLY CHANGES INTO on Delta Streaming Tables for handling historical and incremental changes efficiently.
 
## Cluster Configuration
 
Configured Databricks clusters for scalable pipeline execution, optimized resource allocation, and efficient streaming data processing.
 
## Version Control
 
Integrated GitHub with Databricks Repos for version-controlled pipeline development and deployment.
 
## Future Enhancements
 
- Unity Catalog Integration
- CI/CD Automation
- Workflow Scheduling
- Monitoring & Alerting
- Performance Optimization
 
