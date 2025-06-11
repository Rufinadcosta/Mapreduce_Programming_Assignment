# NYC Yellow Taxi Big Data Pipeline (AWS + Hadoop + MRJob) - Mapreduce Programming

## Project Overview
This end-to-end project involves ingesting large-scale NYC taxi data into a big data ecosystem using cloud and Hadoop tools. It includes data loading into AWS RDS, transferring data into HBase via Apache Sqoop and bulk imports, and running analytical MapReduce jobs using MRJob on AWS EMR.

## Dataset
NYC TLC Yellow Taxi Data for 2017 (January–April), publicly hosted CSV files containing ride-level trip data:
- Trip times, distances, fares, tips, payment types, pickup & drop-off locations.

##  Technologies & Tools Used
- **AWS RDS (MySQL)** – cloud-hosted relational database for initial data storage  
- **Apache Sqoop** – used to ingest data from RDS into HBase  
- **Apache HBase** – NoSQL store for structured trip data  
- **AWS EMR (Elastic MapReduce)** – Hadoop cluster to run processing jobs  
- **MRJob (Python)** – simplifies writing MapReduce jobs in Python  
- **HDFS, Hadoop Streaming, Python**

## Data Ingestion Pipeline
- ✅ Loaded `yellow_tripdata_2017-01.csv` and `yellow_tripdata_2017-02.csv` into AWS RDS (MySQL)  
- ✅ Used **Apache Sqoop** to move data from RDS into **HBase tables**  
- ✅ Performed **bulk import** of `2017-03.csv` and `2017-04.csv` directly into HBase using Hadoop and relevant import tools  

##  MapReduce Analytical Tasks (MRJob)
Each task is implemented using MRJob and run on AWS EMR:

1. 🔹 **Most Trips & Revenue by Vendor**
   - Count of trips and total fare revenue grouped by vendor

2. 🔹 **Top Revenue Generating Pickup Location**
   - Total revenue generated from each pickup zone

3. 🔹 **Payment Types Used**
   - Count of each payment method used by passengers (sorted)

4. 🔹 **Average Trip Duration per Pickup Location**
   - Computed from pickup and drop-off timestamps

5. 🔹 **Tips-to-Revenue Ratio by Pickup Location**
   - Average ratio of tips to total revenue by location (sorted)

6. 🔹 **Revenue Over Time**
   - Average revenue per trip by:
     - Hour of day (day vs. night)
     - Day type (weekday vs. weekend)

##  Outcome
This project showcases:
- Ability to design and implement real-world big data ingestion pipelines
- Proficiency in AWS ecosystem (RDS, EMR, HBase)
- Skill in writing scalable MapReduce jobs using MRJob
- Hands-on experience with data engineering workflows

## Notes
- All schema designs, job logs, and output files are organized per task  
- MRJob scripts are modular and optimized for distributed processing

---


