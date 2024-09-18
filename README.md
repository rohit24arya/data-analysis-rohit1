# Data-Analysis-Rohit1
This project focuses on conducting a descriptive analysis of voting decisions made by the Vancouver Council in 2023 and 2024. The goal is to analyze voting patterns, summarize key insights, and visualize the results to inform stakeholders about council voting trends.
Step 1: Data Analytical Question Formulation
•	Goal: To analyze the voting decisions made in 2023 and 2024.
•	Parameter: Voting decisions for both years.
This analysis provides a descriptive view of the voting records, highlighting trends and providing insights based on the data collected for these years.
Step 2: Data Discovery
•	The dataset was downloaded from the Vancouver Open Data Portal:
o	Website: Vancouver Open Data
o	Data: Council Voting Analysis
The data files were available in Excel format for download.
Step 3: Data Storage Design
•	AWS S3 Buckets were designed to store and organize the data at various stages of processing:
o	Raw Data Bucket: Contains the unprocessed data in its original format.
o	Curated Data Bucket: Stores the cleaned and structured dataset after data transformation.
Step 4: Dataset Preparation
•	The dataset was prepared for analysis after being downloaded in Excel format. The preparation included:
o	Handling missing values.
o	Ensuring the Voting Decision field is properly structured for analysis.
Step 5: Data Ingestion
•	The dataset was moved from the local environment into the AWS environment, specifically stored in Amazon S3 for further processing.
•	S3 Bucket used:
o	s3://council-voting-analysis/raw – Storing the raw voting data for further analysis.
Step 6: Data Storage (S3 Buckets)
•	AWS S3 was used to store the dataset at different stages:
o	Raw Data Bucket: Stores the original voting records.
o	Curated Data Bucket: Contains the cleaned and structured data ready for analysis.
Step 7: Data Pipeline Design
•	A data pipeline was designed using AWS services, including:
o	AWS Glue Databrew: For initial data cleaning and transformation.
o	AWS Glue: For running complex ETL (Extract, Transform, Load) jobs on the dataset.
Step 8 & 9: Data Cleaning and Structuring (AWS Glue Databrew)
•	AWS Glue Databrew was used to clean and explore the dataset. Key cleaning steps included:
o	Removing duplicate voting records.
o	Handling missing Voting Decision values.
o	Normalizing date formats for consistency.
•	The cleaned data was stored back into Amazon S3 for further processing.
Step 10: Data Pipeline Implementation (AWS Glue)
•	AWS Glue was used to implement an ETL pipeline to process the cleaned dataset, applying further transformations like aggregations and filtering based on the analysis goals.
Step 11: Data Analysis (Athena)
•	The cleaned and transformed dataset was analyzed using Amazon Athena:
o	Athena Queries were run to extract key insights from the data.
o	Some key queries included analyzing the number of votes in favor versus against and identifying voting trends over time.
Step 12: Data Visualization (Amazon QuickSight)
Step 13: Data Publishing
•	The results were published as part of a final presentation, shared with stakeholders in both image (PNG) and document formats. The final data and visualizations were stored back in S3 for reference.
Deliverables:
1.	Dataset: Cleaned and structured dataset for 2023-2024 voting records.
2.	Python/AWS Glue Scripts: Used for data cleaning and transformation (available in the /scripts/ directory).
3.	Visualizations: PNG files of charts and graphs created in Amazon QuickSight (available in the /screenshots/ directory).
4.	Final Report: A comprehensive report summarizing the analysis (available in the /docs/ directory).

This project provides a comprehensive descriptive analysis of the voting decisions made by the Vancouver Council for the years 2023 and 2024. The AWS-based pipeline ensures a smooth and automated process for data ingestion, cleaning, transformation, analysis, and visualization.
