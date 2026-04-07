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
<img width="1470" height="956" alt="Screenshot 2026-04-07 at 17 29 17" src="https://github.com/user-attachments/assets/a77c423a-96bc-4c08-99fb-054ec592777c" />


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
<img width="1470" height="956" alt="Screenshot 2026-04-07 at 17 30 06" src="https://github.com/user-attachments/assets/b0cec327-8647-4595-ac3c-853bd064cb31" />


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
<img width="1470" height="885" alt="Screenshot 2026-04-07 at 12 13 39" src="https://github.com/user-attachments/assets/25b36902-e7a7-406d-b880-0a425201063e" />

---

## Athena

Athena is used to query data using SQL directly from S3.

### Steps:
- Open Athena  
- Select database created by Glue  
- Run SQL queries  


### Screenshot:
<img width="1470" height="956" alt="Screenshot 2026-04-07 at 17 31 40" src="https://github.com/user-attachments/assets/8cb68162-23d9-4f1e-9559-b1814813e169" />

---

## SQL Queries to run in Athena

### Query 1 – Basic Table Exploration
This query displays the first 10 rows from the raw table. It is used to quickly check whether the dataset was loaded correctly in Athena.
<img width="1454" height="831" alt="Q1" src="https://github.com/user-attachments/assets/017fd1a9-a454-4014-9690-f5a7786248bd" />
<img width="1459" height="837" alt="Q1 result" src="https://github.com/user-attachments/assets/27e68b6d-176e-4f8c-8829-199c52eada91" />

### Query 2 – Orders by Category
This query counts the total number of orders in each product category. It helps identify which categories have the highest number of orders.
<img width="1452" height="809" alt="Q2" src="https://github.com/user-attachments/assets/7e5f4930-cc5e-4769-937e-9c59570b00f3" />
<img width="1465" height="795" alt="Q2 result" src="https://github.com/user-attachments/assets/efbf80a0-10c6-4bc5-96f1-87b0dfefa0ad" />

### Query 3 – Revenue and Quantity by Fulfilment
This query shows fulfilment method, total orders, total units sold, and total revenue. It excludes cancelled and pending orders to analyze only completed sales performance.
<img width="1465" height="796" alt="Q3" src="https://github.com/user-attachments/assets/c597d419-7c20-4b80-82bf-95467783563d" />
<img width="1459" height="804" alt="Q3 result" src="https://github.com/user-attachments/assets/8da533e3-8dcb-485e-a572-e16bc6e03ad5" />

### Query 4 – Monthly Sales Trend
This query groups the data by month and calculates total orders and revenue for each month. It helps observe the sales trend over time in chronological order.
<img width="1470" height="805" alt="Q4" src="https://github.com/user-attachments/assets/0890df76-a431-4905-a149-1ac57152ccf2" />
<img width="1470" height="808" alt="Q4 result" src="https://github.com/user-attachments/assets/2e751560-c921-4ae5-96fd-b655f372e7ae" />

### Query 5 – Top 5 SKUs per Category
This query finds the top 5 best-selling SKUs in each category based on revenue. It also shows total units sold and rank within each category.
<img width="1466" height="797" alt="Q5" src="https://github.com/user-attachments/assets/3b01c734-c03d-4961-a1a9-a5e82f99f424" />
<img width="1467" height="799" alt="Q5 result" src="https://github.com/user-attachments/assets/72783f34-adf4-431c-a9dc-6abd0e146df3" />
