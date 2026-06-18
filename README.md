# 🏥 Healthcare Data Lake ETL Pipeline on AWS

An end-to-end Healthcare Data Lake built on AWS using the Medallion Architecture (**Bronze → Silver → Gold**) to ingest, transform, catalog, and query healthcare data.

---

## 📌 Project Overview

This project demonstrates how raw healthcare data can be converted into analytics-ready datasets using AWS serverless services.

The pipeline processes healthcare datasets such as:

* Patients Data
* Billing Data
* Lab Results Data

The project follows the Medallion Architecture:

### 🥉 Bronze Layer (Raw Data)

* Raw CSV files stored in Amazon S3
* No transformations applied
* Maintains original historical data

### 🥈 Silver Layer (Cleaned Data)

* Data cleaned and standardized using AWS Glue ETL Jobs (PySpark)
* Removed duplicates and handled missing values
* Converted data into Parquet format

### 🥇 Gold Layer (Analytics Data)

* Created business-ready datasets:

  * patient_summary
  * disease_statistics
  * revenue_summary
* Optimized for querying and analytics

---

## 🏗️ Architecture

![Architecture](https://github.com/Payal930-ui/healthcare-data-etl-pipeline-aws/blob/main/architecture/architecture.jpeg)

---

## ☁️ AWS Services Used

| Service               | Purpose                                               |
| --------------------- | ----------------------------------------------------- |
| Amazon S3             | Data Lake storage for Bronze, Silver, and Gold layers |
| AWS Glue ETL Jobs     | Data cleaning and transformation using PySpark        |
| AWS Glue Crawlers     | Automatic schema discovery                            |
| AWS Glue Data Catalog | Centralized metadata management                       |
| Amazon Athena         | SQL querying on data stored in S3                     |

---

## 🔄 Pipeline Workflow

Raw CSV Files → Amazon S3 (Bronze) → Glue Crawlers → Glue Data Catalog → AWS Glue ETL Jobs → Amazon S3 (Silver) → AWS Glue ETL Jobs → Amazon S3 (Gold) → Amazon Athena

---

## 📂 Project Structure

```text
healthcare-data-etl-pipeline-aws/
├── README.md
├──architecture/
│    ├── architecture.jpeg
├── data/
│   ├── patients.csv
│   ├── billing.csv
│   └── lab_results.csv
└── screenshots/
    ├── s3_bucket.png
    ├── glue_jobs.png
    ├── glue_crawler.png
    └── athena_results.png
```

## 📊 Output Datasets

### patient_summary

Consolidated patient information.

### disease_statistics

Disease-wise patient counts and statistics.

### revenue_summary

Revenue insights generated from billing data.

---

## 🎯 Key Learnings

Through this project, I learned:

* Building an end-to-end Data Lake on AWS
* Implementing Medallion Architecture
* Creating ETL pipelines using AWS Glue and PySpark
* Managing metadata using Glue Crawlers and Data Catalog
* Querying data directly from S3 using Amazon Athena
* Designing analytics-ready datasets for reporting

---

## 🚀 Future Improvements

* Add automated data quality checks
* Implement event-driven orchestration
* Create interactive dashboards for reporting and visualization
* Add monitoring and logging for ETL jobs

---

