# Healthcare Data Lake ETL Pipeline on AWS

## Architecture
![Architecture](architecture/healthcare_etl_architecture.png)

## Tech Stack
- Amazon S3
- AWS Glue ETL Jobs
- AWS Glue Crawlers
- AWS Glue Data Catalog
- Amazon Athena
- CSV
- Parquet

## Architecture Flow
CSV Files
↓
S3 Bronze Layer
↓
AWS Glue ETL Jobs
↓
S3 Silver Layer
↓
AWS Glue ETL Jobs
↓
S3 Gold Layer
↓
Glue Data Catalog
↓
Amazon Athena

## Gold Datasets
- patient_summary
- disease_statistics
- revenue_summary
