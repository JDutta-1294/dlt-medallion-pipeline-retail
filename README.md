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

## Screenshots of DLT pipeline
Raw files inside s3 bucket
<img width="1903" height="956" alt="image" src="https://github.com/user-attachments/assets/98301910-d57c-4803-8794-bedcf75f2288" />
DLT Pipeline DAG
<img width="1618" height="919" alt="image" src="https://github.com/user-attachments/assets/0b882928-7169-479f-9cec-16d507e15da6" />
DLT Pipeline success
<img width="1596" height="862" alt="image" src="https://github.com/user-attachments/assets/ee2ec762-d612-4454-97c5-e81bbee63587" />
SCD 1 on product_silver table
<img width="1670" height="693" alt="image" src="https://github.com/user-attachments/assets/d2d3a9a4-9c36-46c9-8d1e-a7fafe4a4dd3" />
SCD 2 on customers_silver table
<img width="1532" height="849" alt="image" src="https://github.com/user-attachments/assets/51f4f68b-3a73-4e0e-b778-29bb77c9bd6d" />
<img width="1469" height="754" alt="image" src="https://github.com/user-attachments/assets/7c760625-bb10-4ae8-8238-0917015a7034" />

## screenshots of databricks storage configs on AWS
Databrick spot Ec2 instances provisioned
<img width="1619" height="859" alt="image" src="https://github.com/user-attachments/assets/ff0ab101-777b-404e-9eca-3be438d8c04b" />
Databricks storage configs for workspace
<img width="1474" height="756" alt="image" src="https://github.com/user-attachments/assets/853481d7-8e55-49af-b362-2a61153957ab" />
Delta transction log(_delta_log)
<img width="1905" height="959" alt="image" src="https://github.com/user-attachments/assets/fd4dde88-6293-439a-aa41-7aa86254783f" />
Inside Delta transction log we can see _autostats and _stagedcommits to keep track of min-max statistics and number of commits for _delta_log
<img width="1919" height="1022" alt="image" src="https://github.com/user-attachments/assets/6e67af84-d5fa-4ace-ae00-ddb0589ca0b2" />
Min-max statistics inside _autostats.json
<img width="1802" height="157" alt="image" src="https://github.com/user-attachments/assets/fcffa0f2-1dc8-4200-9b1c-5dd613887e84" />




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
 
