# Hands-on L11: AWS Core Services
🎯 Objective

This project demonstrates how to use AWS services to:

Store data in S3
Crawl data using AWS Glue
Monitor jobs using CloudWatch
Query data using Athena
📂 Dataset
Source: Kaggle E-commerce Sales Dataset
Uploaded as CSV file into S3
⚙️ Steps Performed
1️⃣ Created S3 Bucket
Created an S3 bucket
Uploaded CSV dataset
Organized raw data folder
2️⃣ Created IAM Role
Created IAM role with permissions:
S3 access
Glue access
Attached role to Glue crawler
3️⃣ Created Glue Crawler
Configured crawler using:
Data source: S3 bucket
IAM role
Set database name
Created tables automatically
4️⃣ Ran Crawler & Monitored (CloudWatch)
Executed crawler
Checked logs in CloudWatch
Verified successful table creation
5️⃣ Queried Data Using Athena
Opened Athena Query Editor
Selected database created by Glue
Ran SQL queries
