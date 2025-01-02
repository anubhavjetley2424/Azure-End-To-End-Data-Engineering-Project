# Azure End-to-End Data Engineering Real-Time Project
This project is an Microsoft Azure based data engineering pipeline solution to a made-up business problem.

# Goal
The goal is to extract customer and sales data from an on-premises SQL database (Microsoft SQL Server), transform it in the cloud, and generate actionable insights through a Power BI dashboard.

![image](https://github.com/user-attachments/assets/32b632e7-c817-4909-b9cc-e07c93139799)


# Solution Overview

1. Data Ingestion:
Extract customer and sales data from an on-premises SQL database, in my case, Microsoft SQL Server Management Studio
Load the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

2. Data Transformation:
Use Azure Databricks to clean and transform the data.
Organize the data into Bronze, Silver, and Gold layers for raw, cleansed, and aggregated data respectively.

3. Data Loading and Reporting:
Load the transformed data into Azure Synapse Analytics.
Build a Power BI dashboard to visualize the data, allowing stakeholders to explore sales and demographic insights.

4.Automation:
Schedule the pipeline to run daily, ensuring that the data and reports are always up-to-date.

# Azure Data Factory Pipeline:

![image](https://github.com/user-attachments/assets/82631415-673d-4de1-9303-21b5c7441445)

# Synapse Gold Data Load Pipeline

![image](https://github.com/user-attachments/assets/bcc677b8-6983-45a9-bda0-164d1bc18fc3)

# Technology Stack
- Azure Data Factory (ADF): For orchestrating data movement and transformation.
- Azure Data Lake Storage (ADLS): For storing raw and processed data.
- Azure Databricks: For data transformation and processing.
- Azure Synapse Analytics: For data warehousing and SQL-based analytics.
- Power BI: For data visualization and reporting.
- Azure Key Vault: For securely managing credentials and secrets.
- SQL Server (On-Premises): Source of customer and sales data.


