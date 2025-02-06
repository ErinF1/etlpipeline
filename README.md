# Self-Serve Data Analytics ETL Pipeline

## Project Overview
This project is an **ETL (Extract, Transform, Load) pipeline** designed for a **self-serve data analytics and reporting service**. It enables users to upload data files to an AWS S3 bucket, where the pipeline **automatically processes and cleans the data** before delivering structured reports.

## Technologies Used
- Python  
- AWS S3  
- Boto3  
- Pandas  

## How It Works
1. Clients receive a **custom link** to upload their data files.  
2. The files are stored in an **S3 bucket** under their designated folder.  
3. The ETL pipeline is **triggered by file upload** (no scheduling tools used).  
4. The script processes, cleans, and structures the data.  
5. The transformed data is **stored back in S3 or emailed to the client**.  

## How to Run Locally
1. Install dependencies:
   pip install boto3 pandas
2. Run the script:

python etlpipeline.py

## Future Improvements
- Automate report generation and delivery.  
- Build a client dashboard for data uploads and results tracking.  
- Implement AI-powered data insights.  

### Notes:
- This **does NOT** use cron jobs, Airflow, or scheduled tasks—ETL is triggered on **file upload events** in S3.  
- The pipeline is **event-driven**, meaning it runs **only when a file is uploaded** to the cloud.  



