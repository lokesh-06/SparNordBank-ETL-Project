# SparNordBank-ETL-Project

Project Overview:
This project involves analyzing Danish ATM transaction data from Spar Nord Bank to optimize refill frequency and gain valuable insights from the data. The data includes over 2.5 million records of withdrawal data from 113 ATMs, spanning the year 2017, and includes weather information at the time of the transactions.

ETL Pipeline:
Primary task is to build a batch ETL (Extract, Transform, Load) pipeline to:

1) Extract transactional data from a MySQL RDS server to an EC2 instance using Sqoop.
2) Transform the data to match the target schema using PySpark.
3) Load the transformed data into an Amazon S3 bucket.
4) Create Redshift tables according to the provided schema.
5) Load data from Amazon S3 into Redshift tables.

Data Set Details:

1) The dataset consists of 2.5 million records from 113 ATMs in Denmark, including weather information.
2) It is divided into two files totaling about 503 MB.
3) A data dictionary is provided, defining the 33 columns in the dataset.
4) Data includes transaction date and time, ATM status, ATM details, weather data, and transaction specifics.

Important Note:

1) The transaction amount field in the dataset was artificially generated for analysis purposes.
2) Spar Nord Bank has created a dimensional model datastore (ATM Data Mart) based on this dataset, which will serve as the target schema for creating Redshift tables.

Analysis Queries:
Upon loading the data into Redshift, We implemented the analytical queries to gain insights into ATM transaction patterns and optimize refill strategies.
