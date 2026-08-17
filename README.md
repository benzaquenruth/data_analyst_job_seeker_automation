# Data Analyst Job Seeker pipeline

## 🎯 Project Goal
Automatically identify which Data Analyst jobs are the best fit for me, avoiding endless scrolling through job boards! and analyze the Israeli job market through data analysis and visualization.

This project also includes an AI-powered cv and cover letter personalization workflow for job applications.


<img width="1536" height="1024" alt="ChatGPT Image May 24, 2026, 12_40_46 PM" src="https://github.com/user-attachments/assets/8600e343-36aa-4877-b729-3a693e02e286" />


---

## ⚙️ What the Project Does
- Collects job postings automatically on a daily basis  (from Indeed and LinkedIn)
- Extracts and structures relevant job information  
- Adds personalized scoring:
  - **Job relevance score** – how relevant the position is for me  
  - **Fit score** – how well my profile matches the job  
- Generates **cover letters automatically** for selected jobs  
- Stores and processes data in a scalable cloud environment  
- Enables data analysis and insight generation  

---

## 💡👀 A Peek at the Job Dataset

<img width="1189" height="395" alt="Screenshot 2026-08-17 063551 two" src="https://github.com/user-attachments/assets/852835f9-a7b3-42da-a9e5-e2e1d4e77f38" />
<img width="951" height="395" alt="example data job seeker 2" src="https://github.com/user-attachments/assets/459506fd-15e5-4233-9960-77de0cc51794" />


- Title : Job title.
- Job Description : Full job description.
- Platform : Source platform (LinkedIn or Indeed).
- Link : Original job posting URL.
- Date : Date the job was posted.
- Rating :  Overall job rating - includes 'fit for the job' score and others. Example, if in Tel Aviv, add 2 points.
- Fit for the job : From 1 to 4, how well my skills match the job requirements. 
- Reasoning — Explanation behind the scores ('Rating' and 'Fit for the job' scores)
- Company Name : Hiring company.
- Cover Letter : Text of the Generated cover letter, when applicable.
- City : Job location.
- Remote : Whether the role is remote.
- Status : Application status.
- Cover trigger — Checking the box triggers cover letter generation.
- CV trigger — Whether a tailored CV should be generated.
- experience_bucket : Required experience level.
- experience_reason : Checking the box triggers tailored CV generation.
- skills : Skills extracted from the job description.

---

## 🔄 Current Pipeline
1. Collect job postings automatically (n8n workflows)  
2. Extract and structure job data using AI agents  
3. Score jobs based on relevance and personal fit  
4. Store raw data in **Google Sheets / BigQuery**  
5. Transform and normalize data using **BigQuery (SQL)**  
6. Create analytics-ready tables  
7. Build dashboards in **Looker Studio**  

---

## 🛠️ Tech Stack
- **n8n** – workflow orchestration  
- **Python** – analysis & exploration  
- **Pandas**  
- **Jupyter Notebook**  
- **Google BigQuery** – data warehouse & transformations  
- **Looker Studio** – dashboards & visualization  --> https://datastudio.google.com/s/n_7K3BRZGzY

---

## ❓ Key Questions
- How many Data Analyst jobs were posted? Weekly? Montly?  
- Which platforms publish the most positions?  
- What percentage of jobs am I a **strong fit** for?  
- How does demand change over time?  
- What experience levels are most in demand?  

---

## 🧹 Data Processing & Modeling
- Data is cleaned and standardized using **BigQuery SQL transformations**  
- Duplicate jobs are removed using a unique key (**Title + Company**)  
- Location data is normalized into a consistent format  
- Experience requirements are categorized into structured buckets  
- Final datasets are optimized for analytics and dashboarding  

---

## 🚀 Future Improvements
- Improve AI scoring accuracy (better prompts & evaluation logic)  
- Add salary estimation and compensation analysis  
- Build a personalized job recommendation engine  
- Develop a lightweight app for browsing top matches  
- Add real-time alerts for high-fit job postings  

## ✍️ Personalized CV & Cover Letter Workflow

Using checkboxes inside the Google Sheets job database, I can instantly trigger workflows that generate tailored CVs and cover letters for specific positions.

The AI adapts my existing templates using:
- My professional background and experience  
- My personal writing style and tone  
- Detailed instructions and optimization rules  
- The requirements of the specific job posting  

The goal is to create applications that feel authentic, personalized, and highly relevant — while still sounding completely natural and like me.

Final versions are automatically generated and saved to Google Drive, ready to send.

---


## 📁 Repository Structure

This repository includes all the main components used to build and analyze the job market pipeline:

### 🔄 8n8 Data Collection Workflow
**File:** `8n8 Data Collection Workflow.md`  
Contains a visual and explanation of the n8n workflow used to automatically collect job postings.  
This is the **data ingestion layer** of the project — responsible for scraping, initial processing, and feeding the pipeline.


### 📊 Initial Dataset
**File:** `Job Listings Database.xlsx`  
A sample of the first job postings collected at the beginning of the project.  
- Represents the **raw structure of the data before improvements**  
- Useful for understanding how the data originally looked  
- The current pipeline includes additional enhancements and better structuring  


### 🔍 Exploratory Data Analysis (EDA)
**File:** `01_job_market_eda.ipynb`  
Jupyter Notebook used for the **initial exploration of the dataset**.

Includes:
- Data cleaning and preprocessing  
- First-level analysis and aggregations  
- Identification of data quality issues  
- Early insights and visualizations  

This step was critical to:
- Understand the dataset  
- Define normalization and transformation logic in BigQuery  
- Improve the data collection process in n8n  
- Build a more structured and scalable pipeline  


