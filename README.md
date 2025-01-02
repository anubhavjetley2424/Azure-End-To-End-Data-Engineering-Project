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

# Setup:
Step 1: Azure Environment Setup
Create Resource Group: Set up a new resource group in Azure.
Provision Services:
Create an Azure Data Factory instance.
Set up Azure Data Lake Storage with bronze, silver, and gold containers.
Set up an Azure Databricks workspace and Synapse Analytics workspace.
Configure Azure Key Vault for secret management.
Step 2: Data Ingestion
Set up SQL Server: Install SQL Server and SQL Server Management Studio (SSMS). Restore the AdventureWorks database.
Ingest Data with ADF: Create pipelines in ADF to copy data from SQL Server to the bronze layer in ADLS.
Step 3: Data Transformation
Mount Data Lake in Databricks: Configure Databricks to access ADLS.
Transform Data: Use Databricks notebooks to clean and aggregate the data, moving it from bronze to silver and then to gold.
Step 4: Data Loading and Reporting
Load Data into Synapse: Set up a Synapse SQL pool and load the gold data for analysis
Create Power BI Dashboard: Connect Power BI to Synapse and create visualizations based on business requirements.
Step 5: Automation and Monitoring
Schedule Pipelines: Use ADF to schedule the data pipelines to run daily, at selected times
Monitor Pipeline Runs: Use the monitoring tools in ADF and Synapse to ensure successful pipeline execution.
Step 6: Security and Governance
Manage Access: Set up role-based access control (RBAC) using Azure Entra ID (formerly Active Directory).
Step 7: End-to-End Testing
Trigger and Test Pipelines: Insert new records into the SQL database and verify that the entire pipeline runs successfully, updating the Power BI dashboard.

