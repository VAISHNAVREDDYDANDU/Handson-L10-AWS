# AWS Core Services Hands-on (L11)

## Course
Cloud Computing for Data Analysis (ITCS 6190/8190) – Spring 2026

---

## Objective
This project shows how to use AWS services like S3, Glue, CloudWatch, and Athena to process and query data.

---

## Dataset
E-commerce sales dataset (CSV file uploaded to S3)

---

## Steps Performed

### 1. S3 Bucket
- Created S3 bucket
- Uploaded CSV dataset

### 2. IAM Role
- Created IAM role
- Added permissions for S3 and Glue

### 3. Glue Crawler
- Created crawler
- Connected to S3 data
- Created database and tables

### 4. CloudWatch
- Ran crawler
- Checked logs in CloudWatch

### 5. Athena
- Opened Athena
- Selected database
- Ran SQL queries

---

## Queries

### Query 1
```sql
SELECT * FROM table_name LIMIT 10;
