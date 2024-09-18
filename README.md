**Project-1**

This project focuses on conducting a descriptive analysis of voting decisions made by the Vancouver Council in 2023 and 2024. The goal is to analyze voting patterns, summarize key insights, and visualize the results to inform stakeholders about council voting trends.

**Step 1**: Data Analytical Question Formulation

a)Goal: To analyze the voting decisions made in 2023 and 2024.

b)Parameter: Voting decisions for both years.
This analysis provides a descriptive view of the voting records, highlighting trends and providing insights based on the data collected for these years.

**Step 2**: Data Discovery

The dataset was downloaded from the Vancouver Open Data Portal:

a)Website: Vancouver Open Data

b)Data: Council Voting Analysis

The data files were available in Excel format for download.

**Step 3**: Data Storage Design

AWS S3 Buckets were designed to store and organize the data at various stages of processing:

a)Raw Data Bucket: Contains the unprocessed data in its original format.
	
b)Curated Data Bucket: Stores the cleaned and structured dataset after data transformation.

![image](https://github.com/user-attachments/assets/1862f2c5-7f62-4133-ba69-056e069ff957)

![image](https://github.com/user-attachments/assets/d9450aea-fa4d-4e49-9652-8575a4ad1a56)

**Step 4**: Dataset Preparation

The dataset was prepared for analysis after being downloaded in Excel format. The preparation included:

a)Handling missing values.

b)Ensuring the Voting Decision field is properly structured for analysis.

**Step 5**: Data Ingestion

a)The dataset was moved from the local environment into the AWS environment, specifically stored in Amazon S3 for further processing.

b)S3 Bucket used:

s3://council-voting-analysis/raw – Storing the raw voting data for further analysis.

**Step 6**: Data Storage (S3 Buckets)

AWS S3 was used to store the dataset at different stages:

a)Raw Data Bucket: Stores the original voting records.

b)Curated Data Bucket: Contains the cleaned and structured data ready for analysis.

![image](https://github.com/user-attachments/assets/3266c3dd-164b-47a9-9278-346bb207a44b)

![image](https://github.com/user-attachments/assets/a47bfe46-babd-499f-9816-682b398faed0)

**Step 7**: Data Pipeline Design

A data pipeline was designed using AWS services, including:

a)AWS Glue Databrew: For initial data cleaning and transformation.

b)AWS Glue: For running complex ETL (Extract, Transform, Load) jobs on the dataset.

![image](https://github.com/user-attachments/assets/806baa2d-a2f1-499a-a43a-2a752540fefe)

**Step 8 & 9**: Data Cleaning and Structuring (AWS Glue Databrew)

AWS Glue Databrew was used to clean and explore the dataset. Key cleaning steps included:

a)Removing duplicate voting records.

b)Handling missing Voting Decision values.

c)Normalizing date formats for consistency.

d)The cleaned data was stored back into Amazon S3 for further processing.

![image](https://github.com/user-attachments/assets/1cdb7f04-d11b-4ec8-a206-113e63e05e76)

![image](https://github.com/user-attachments/assets/7c35297c-e277-472f-a475-ab350cccbd71)

![image](https://github.com/user-attachments/assets/686405f3-99af-4320-92c9-d250733d0bf0)

**Step 10**: Data Pipeline Implementation (AWS Glue)

AWS Glue was used to implement an ETL pipeline to process the cleaned dataset, applying further transformations like aggregations and filtering based on the analysis goals.

![image](https://github.com/user-attachments/assets/cf310476-de56-4017-9051-a68a231d0412)

**Step 11**: Data Analysis (Athena)

The cleaned and transformed dataset was analyzed using Amazon Athena:

a)Athena Queries were run to extract key insights from the data.

b)Some key queries included analyzing the number of votes in favor versus against and identifying voting trends over time.

![image](https://github.com/user-attachments/assets/e4dfcf5c-5d15-4209-bb34-ab1be0e05d60)

**Step 12**: Data Publishing

The results were published as part of a final presentation, shared with stakeholders in both image (PNG) and document formats. The final data and visualizations were stored back in S3 for reference.
Deliverables:

Dataset: Cleaned and structured dataset for 2023-2024 voting records.

This project provides a comprehensive descriptive analysis of the voting decisions made by the Vancouver Council for the years 2023 and 2024. The AWS-based pipeline ensures a smooth and automated process for data ingestion, cleaning, transformation, analysis, and visualization.

![image](https://github.com/user-attachments/assets/eb7675df-bab6-4aff-9bd5-a48822800b3f)


**Project-2**
The key objective of this section is to implement a Data Analytics Platform (DAP) that securely manages, monitors, and governs the council voting data. The analysis also focuses on ensuring compliance with data governance standards while diagnosing potential inefficiencies in data workflows.

**Step-1**: **Data Protection**

**Objective**: Protect sensitive council voting data during storage, processing, and transfer.

**Actions Taken**:

a)**Encryption**: All sensitive voting data stored in Amazon S3 is encrypted.

b)**Access Control**: Implemented role-based access control (RBAC) using AWS Identity and Access Management (IAM) to restrict access to authorized personnel.

c)**Audit Logging**: Enabled AWS CloudTrail to log and monitor all access and modifications to voting data for security audits

**Tools**:

a)Amazon S3 for secure data storage.

b)AWS IAM for enforcing access control policies.

c)AWS CloudTrail for logging and auditing activities

![image](https://github.com/user-attachments/assets/dffaa334-4952-4de9-b190-ff134f86a9e0)

![image](https://github.com/user-attachments/assets/a4dfe19d-b8da-473f-9c93-74783bc648ca)

![image](https://github.com/user-attachments/assets/607cbf36-2f32-4d39-afde-f87b4afda0c9)

**Step-2**: **Data Governance**

**Objective**: Ensure proper data governance by implementing policies that manage data quality, access, and lifecycle.

**Actions Taken**:

a)Defined data retention policies for council voting records

b)Utilized AWS Glue Data Catalog to organize and label datasets, enabling structured and secure access to the voting data

c)Established metadata tagging in S3 buckets for better data classification and discovery

**Tools**:

a)AWS Glue Data Catalog for data organization and governance

b)AWS IAM to define data governance roles and permissions

c)AWS Config for monitoring governance policy compliance

![image](https://github.com/user-attachments/assets/aab27d34-abb3-4623-99bd-003652cb9e2e)

![image](https://github.com/user-attachments/assets/2e2c6ce6-1efc-404e-89c9-c52cfe874d68)

![image](https://github.com/user-attachments/assets/d1772725-79c4-4a2d-b9d2-d446495a1150)

![image](https://github.com/user-attachments/assets/f3628e39-d2d3-43d4-acf5-2880d880d88a)

![image](https://github.com/user-attachments/assets/099f84c4-91e3-4ead-a52e-adff14cf4e65)

![image](https://github.com/user-attachments/assets/033f6fbf-d4b3-4e56-9cb9-73489b050c8a)

**Step-3**: **Data Monitoring**

**Objective**: 
Monitor data pipelines, access control, and data activities in real-time.

**Actions Taken**:

a)Set up monitoring for the entire data pipeline using Amazon CloudWatch, tracking data ingestion and processing metrics in real time.

b)Configured AWS Lambda to send alerts for unauthorized data access or unexpected activity.

c)Created dashboards in CloudWatch for live monitoring of voting data metrics.

**Tools**:

a)Amazon CloudWatch for monitoring system and data activity.

b)AWS Lambda for automated alerts and responses.

c)Amazon S3 for continuous monitoring of data access logs.

![image](https://github.com/user-attachments/assets/27be9b73-f838-45cd-9498-7f113e18724b)

![image](https://github.com/user-attachments/assets/957b3b78-2268-4129-b31d-6ecff58f1ef9)

![image](https://github.com/user-attachments/assets/4643313a-2d3f-445e-963c-a3e26c82f682)

![image](https://github.com/user-attachments/assets/dc74e674-722c-406f-a0e4-fdd7c6b01f57)

![image](https://github.com/user-attachments/assets/51b01db7-4e23-4880-8ce7-029cfa83b1e8)

The type of analysis used here is a Diagnostic Analysis. This analysis is designed to diagnose and address issues related to data protection, governance, and monitoring within the data platform. It focuses on identifying potential security vulnerabilities, inefficiencies in data governance, and irregularities in data access or usage patterns

