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

Step 4: Dataset Preparation

The dataset was prepared for analysis after being downloaded in Excel format. The preparation included:

a)Handling missing values.

b)Ensuring the Voting Decision field is properly structured for analysis.

Step 5: Data Ingestion

a)The dataset was moved from the local environment into the AWS environment, specifically stored in Amazon S3 for further processing.

b)S3 Bucket used:

s3://council-voting-analysis/raw – Storing the raw voting data for further analysis.

Step 6: Data Storage (S3 Buckets)

AWS S3 was used to store the dataset at different stages:

a)Raw Data Bucket: Stores the original voting records.

b)Curated Data Bucket: Contains the cleaned and structured data ready for analysis.

![image](https://github.com/user-attachments/assets/3266c3dd-164b-47a9-9278-346bb207a44b)

![image](https://github.com/user-attachments/assets/a47bfe46-babd-499f-9816-682b398faed0)

Step 7: Data Pipeline Design

A data pipeline was designed using AWS services, including:

a)AWS Glue Databrew: For initial data cleaning and transformation.

b)AWS Glue: For running complex ETL (Extract, Transform, Load) jobs on the dataset.

![image](https://github.com/user-attachments/assets/806baa2d-a2f1-499a-a43a-2a752540fefe)

Step 8 & 9: Data Cleaning and Structuring (AWS Glue Databrew)

AWS Glue Databrew was used to clean and explore the dataset. Key cleaning steps included:

a)Removing duplicate voting records.

b)Handling missing Voting Decision values.

c)Normalizing date formats for consistency.

d)The cleaned data was stored back into Amazon S3 for further processing.

![image](https://github.com/user-attachments/assets/1cdb7f04-d11b-4ec8-a206-113e63e05e76)

![image](https://github.com/user-attachments/assets/7c35297c-e277-472f-a475-ab350cccbd71)

![image](https://github.com/user-attachments/assets/686405f3-99af-4320-92c9-d250733d0bf0)

Step 10: Data Pipeline Implementation (AWS Glue)

AWS Glue was used to implement an ETL pipeline to process the cleaned dataset, applying further transformations like aggregations and filtering based on the analysis goals.

![image](https://github.com/user-attachments/assets/cf310476-de56-4017-9051-a68a231d0412)

Step 11: Data Analysis (Athena)

The cleaned and transformed dataset was analyzed using Amazon Athena:

a)Athena Queries were run to extract key insights from the data.

b)Some key queries included analyzing the number of votes in favor versus against and identifying voting trends over time.

![image](https://github.com/user-attachments/assets/686405f3-99af-4320-92c9-d250733d0bf0)

Step 12: Data Publishing

The results were published as part of a final presentation, shared with stakeholders in both image (PNG) and document formats. The final data and visualizations were stored back in S3 for reference.
Deliverables:

Dataset: Cleaned and structured dataset for 2023-2024 voting records.

This project provides a comprehensive descriptive analysis of the voting decisions made by the Vancouver Council for the years 2023 and 2024. The AWS-based pipeline ensures a smooth and automated process for data ingestion, cleaning, transformation, analysis, and visualization.
