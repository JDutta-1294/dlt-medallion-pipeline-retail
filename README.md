Designed and implemented an end-to-end Medallion Architecture pipeline in Databricks ON AWS using Delta Live Tables (DLT), Spark SQL API, and Delta Lake, auto-loader. Built Bronze, Silver, and Gold layers for scalable data ingestion, transformation, and aggregation. Implemented Slowly Changing Dimension (SCD) Type 1 and Type 2 logic using AUTO CDC INTO on Delta Streaming Tables for efficient CDC and historical data tracking. Configured and optimized Databricks clusters for pipeline execution and performance tuning. Integrated Git-based version control for pipeline management and deployment workflows.
 
Implemented a Medallion Architecture pipeline using Databricks Delta Live Tables (DLT), Spark SQL,auto-loader and Delta Lake. Developed Bronze, Silver, and Gold layers with SCD Type 1 and Type 2 implementation using AUTO CDC INTO on Delta Streaming Tables. Created external storage location to access S3 bucket, Configured Databricks clusters on AWS for scalable pipeline execution and integrated GitHub for version control.
 
Built a Databricks DLT Medallion Architecture pipeline with Bronze, Silver, and Gold layers, implementing SCD Type 1 and Type 2 using APPLY CHANGES INTO on Delta Streaming Tables, along with cluster configuration and Git integration.
 
# Databricks Delta Live Tables (DLT) Pipeline
 
## Project Overview
 
This project demonstrates an end-to-end Medallion Architecture pipeline built using Databricks Delta Live Tables (DLT), PySpark, and Delta Lake.
 
The pipeline processes data through multiple layers:
 
- Bronze Layer → Raw data ingestion from S3 using auto-loader
- Silver Layer → Cleansed and transformed data and performed SCD1 and SCD2 using AUTO CDC INTO on Delta Streaming Tables
- Gold Layer → Business-ready aggregated data
 
## Features Implemented
- AWS S3
- Delta Live Tables (DLT)
- Medallion Architecture
- Auto loader
- Delta Streaming Tables
- SCD Type 1 and SCD Type 2
-  AUTO CDC INTO
- Change Data Capture (CDC)
- Incremental Data Processing
- Data Quality Validations(Constraints)
- GitHub Version Control Integration
- Databricks Cluster Configuration
- External storage location created to access S3 bucket(source data)
- IAM roles created for External storage location 
  
 
## Technologies Used
 
- Databricks
- AWS S3
- AWS IAM roles
- Spark SQL
- Delta Live Tables (DLT)
- Git & GitHub
 
## Pipeline Architecture
 
```text
Source Data(S3 CSV data(External storage location created to access S3 bucket(source data))
     ↓
Bronze Layer(using autoloader)
     ↓
Silver Layer(CDC with Auto CDC INTO)
     ↓
Gold Layer
```
 
## SCD Implementation
 
Implemented Slowly Changing Dimension (SCD) Type 1 and Type 2 using AUTO CDC INTO on Delta Streaming Tables for handling historical and incremental changes efficiently.
Also found a way to prune unwanted records from a source without requiring the entire sink table be recalculated with DLT by using skipChangeCommits = "true"
 
## Cluster Configuration
 
Configured Databricks clusters (job clusters) for scalable pipeline execution on AWS , optimized resource allocation, and efficient streaming data processing.
 
## Version Control
 
Integrated GitHub with Databricks Repos for version-controlled pipeline development and deployment.
 
## Future Enhancements
 
- Unity Catalog Integration
- CI/CD Automation
- Workflow Scheduling
- Monitoring & Alerting
- Performance Optimization
 
