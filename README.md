# ETL Pipeline using AWS [S3, Glue, Lambda, IAM]

## Business Use Case

Retail businesses generate vast amounts of sales data daily. However, unstructured and inconsistent data—such as missing values, formatting inconsistencies, and duplicate entries—can hinder accurate analysis. To overcome this, we implemented a serverless ETL pipeline using AWS S3, Glue, and Lambda to automate data cleaning and preparation for business intelligence and reporting.

## Dataset Overview

The dataset used for this project is a Superstore Sales dataset, containing 9,994 records and 13 attributes related to:
* Order Details: Sales, Quantity, Discount, Profit
* Customer Segments: Consumer, Corporate, Home Office
* Geographic Data: City, State, Region
* Product Categories: Furniture, Office Supplies, Technology
* Shipping Information: Ship Mode, Postal Code

## Challenges in Data Processing

* Missing Values: Some fields (e.g., profit, discount) may have null values impacting financial analysis.
* Data Consistency: Variations in text fields (e.g., different spellings of the same city) need standardization.
* Real-time Processing: Manual updates and batch uploads delay decision-making.
* Scalability: Growing data volume requires an automated and scalable solution.

## Solution: Serverless ETL Pipeline

* AWS S3: Raw sales data is uploaded to an S3 bucket.
* AWS Glue: A Glue job cleans and standardizes data by:-
    * Handling missing values
    * Standardizing text fields (e.g., city names, categories)
    * Ensuring numerical consistency for sales, discount, and profit calculations
* AWS Lambda: Automatically triggers when a file is uploaded to S3, processes the data, and moves cleaned files to a processed folder in S3 for further analytics.

## Business Impact

✅ Automated Data Cleaning: Eliminates manual intervention, ensuring accuracy.

✅ Real-time Processing: Enables near-instant updates for reporting.

✅ Scalability: Serverless architecture handles increasing data volumes efficiently.

✅ Data-Driven Decisions: Cleaned data powers dashboards for sales trends, profit analysis, and demand forecasting.

