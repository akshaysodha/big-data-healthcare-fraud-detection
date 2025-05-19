# 🩺 Medicare Fraud Detection with Big Data

A real-time, scalable fraud detection system built using Apache Spark, Apache Kafka, Docker, and machine learning. This term project was developed as part of **DATA 228 - Big Data Technologies** during the MS in Data Analytics program at **San José State University**.

## 📌 Project Summary

Billions of dollars are lost every year due to Medicare fraud. This project tackles the issue using a distributed big data pipeline that ingests, processes, and analyzes healthcare data in real-time. We combine the power of Apache Kafka, Spark, and logistic regression to build a responsive system that flags potentially fraudulent cases from multiple data sources.

## 🛠️ Tech Stack

- **Apache Kafka** – Real-time data ingestion via producer/consumer topics
- **Apache Spark** – Distributed stream processing and transformations
- **Docker** – Containerized orchestration for scalable deployment
- **Python (scikit-learn)** – Logistic regression model for fraud prediction
- **Pandas, Seaborn, Power BI, Tableau** – Data analysis & visualization
- **Trello, Google Colab, GitHub** – Agile collaboration & version control

---

## 🧱 Architecture Overview

The pipeline is composed of the following components:

1. **Data Sources**:  
   - CMS Part D Prescriber Dataset: Over 25M rows of Medicare prescription data  
   - LEIE Exclusion Dataset: Exclusion records for fraudulent providers  
   - Payments Received by Physicians Dataset: Pharmaceutical payments & transactions (~11M rows)

2. **Data Ingestion with Kafka**:  
   Each dataset is streamed through a dedicated Kafka topic.

3. **Stream Processing with Spark**:  
   Spark subscribes to the topics, transforms the data, and performs aggregations.

4. **Data Cleaning & Feature Engineering**:  
   Cleaning scripts handle duplicates, missing values, and inconsistencies. Locality-Sensitive Hashing (LSH) is applied to group similar exclusions.

5. **Machine Learning (Logistic Regression)**:  
   A binary classification model identifies fraudulent vs non-fraudulent cases, achieving **AUC = 0.92**.

6. **Containerization with Docker**:  
   Kafka and Spark components are containerized for portability and consistency across environments.

<!--![Pipeline Overview](https://github.com/leoncorreia/DATA228-termproject/blob/main/docs/pipeline-overview.png)  -->

## 📊 Key Features

- Real-time streaming fraud detection
- Scalable architecture using Spark and Kafka
- Intelligent grouping of fraud types using LSH
- Logistic Regression model trained on historical patterns
- Clean, modular codebase with Docker-based deployment


## 📁 Repository Structure
```bash

├── spark/ # Spark scripts and config
├── producer/ # Kafka producer code
├── cql/ # CQL queries and setup
├── Scripts/ # Data transformation scripts
├── Data_cleaning_spark.py # Data cleaning logic
├── main.ipynb # ML model training and evaluation
├── docker-compose.yml # Docker orchestration
├── TestProject.ipynb # End-to-end pipeline walkthrough
└── README.md
```

## 🤝 Team Collaboration

- ✅ Agile Scrum with 1-week sprints  
- ✅ Version control with GitHub  
- ✅ Pair programming using Google Colab  
- ✅ Task tracking with Trello

## 🧪 Evaluation

- **Metric Used**: AUC-ROC  
- **Result**: 0.92  
- **Insights**: Feature importance revealed EXCLTYPE categories and physician payment patterns as strong fraud indicators.
- Balanced feature contribution: ensured via scaling and correlation analysis

<!-- ![AUC ROC Curve](https://github.com/leoncorreia/DATA228-termproject/blob/main/docs/auc-roc.png)  --> 

## 📎 Report & Presentation

- [📄 Final Project Report (PDF)](https://github.com/akshaysodha/big-data-healthcare-fraud-detection/blob/main/Big%20Data%20Medicare%20Fraud%20Detection%20Project%20Report.pdf)

- [🎥 Elevator Pitch Video](https://youtu.be/H5RJK-znUAQ?si=SrhkfppODR45VWNp)
- [🗂️ Trello Dashboard](https://trello.com/invite/b/vWHhpPvj/ATTI35053ec29557657968413232b04859899E4D863A/big-data)


## 🧠 Key Skills Demonstrated

| Category             | Skills & Tools Used                                                                 |
|----------------------|--------------------------------------------------------------------------------------|
| Real-Time Streaming  | Apache Kafka (topics, producers, consumers), Spark Streaming                        |
| Big Data Processing  | Apache Spark (dataframes, transformations, aggregations)                            |
| Containerization     | Docker, Docker Compose (for reproducible Kafka + Spark setup)                       |
| Machine Learning     | Logistic Regression (scikit-learn), AUC-ROC Evaluation, Feature Scaling             |
| ETL & Data Cleaning  | PySpark, Pandas, Python scripting                                                   |
| Similarity Analysis  | Locality-Sensitive Hashing (LSH), MinHash, Bucketing                                |
| Visualization        | Seaborn, Power BI, Tableau                                                          |
| Version Control      | Git, GitHub (repo structure, commits, collaborative code development)               |
| Agile Development    | Scrum methodology, Trello board, Google Colab for pair programming                  |
| Communication & Teamwork | Pair programming, Sprint planning, Regular team stand-ups, Joint documentation efforts |


---

