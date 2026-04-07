# Hands-on L11: AWS Core Services (S3, Glue, CloudWatch, Athena)

AWS (Amazon Web Services) is a cloud platform that offers services for storing, processing, and analyzing data. In this hands-on, we used AWS services such as S3, Glue, CloudWatch, and Athena to process a dataset and run queries.

---

## Amazon S3

Amazon S3 (Simple Storage Service) is used to store data in the cloud. It is scalable, secure, and reliable.

### Steps to create an S3 bucket:
- Log in to AWS Console and search for S3  
- Click on "Create bucket"  
- Enter a unique bucket name  
- Create folders named **raw** and **processed**  
- Upload the dataset into the **raw** folder  

### Screenshot:
![S3](add-your-s3-image.png)

---

## IAM Roles

IAM (Identity and Access Management) is used to manage access and permissions.

### Steps to create IAM role:
- Search IAM in AWS Console  
- Click on "Roles" → Create role  
- Select AWS service → Glue  
- Attach policies:
  - AmazonS3FullAccess  
  - AWSGlueServiceRole  
- Create the role  

### Screenshot:
![IAM](add-your-iam-image.png)

---

## AWS Glue Crawler

Glue crawler is used to scan data and create tables automatically.

### Steps:
- Open AWS Glue  
- Go to Crawlers → Create crawler  
- Select data source from S3  
- Choose IAM role  
- Set database name  
- Run the crawler  

### Screenshot:
<img width="1470" height="956" alt="Screenshot 2026-04-07 at 17 28 26" src="https://github.com/user-attachments/assets/14247e01-b5bf-48a4-9a82-fd4d46fefbcb" />


---

## CloudWatch

CloudWatch is used to monitor logs and crawler execution.

### Steps:
- Open CloudWatch  
- Go to Logs  
- Check crawler logs  

### Screenshot:
![CloudWatch](add-your-cloudwatch-image.png)

---

## Athena

Athena is used to query data using SQL directly from S3.

### Steps:
- Open Athena  
- Select database created by Glue  
- Run SQL queries  

---

## SQL Queries

### Query 1 – Basic Table
```sql
SELECT *
FROM raw
LIMIT 10;
