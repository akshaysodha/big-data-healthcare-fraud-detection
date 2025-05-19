# 🩺 Medicare Fraud Detection with Big Data

A real-time, scalable fraud detection system built using Apache Spark, Apache Kafka, Docker, and machine learning. This term project was developed as part of **DATA 228 - Big Data Technologies** during the MS in Data Analytics program at **San José State University**.

## 🔍 Problem Statement

Medicare fraud results in billions of dollars in annual losses and threatens the integrity of the U.S. healthcare system. Our project aims to build a big data pipeline capable of identifying fraudulent activities by leveraging real-time data processing and machine learning models.

## 🛠️ Tech Stack

- **Apache Kafka** – Real-time data ingestion  
- **Apache Spark** – Distributed data processing  
- **Docker** – Containerization of the pipeline  
- **Python (scikit-learn)** – Logistic Regression model  
- **Pandas, Seaborn, Power BI, Tableau** – Data analysis & visualization  
- **Google Colab, GitHub** – Collaboration & version control

## 🧱 Architecture Overview

The pipeline is composed of the following components:

1. **Data Sources**:  
   - CMS Part D Prescriber Dataset  
   - LEIE Exclusion Dataset  
   - Payments Received by Physicians Dataset

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

![Pipeline Overview](https://github.com/leoncorreia/DATA228-termproject/blob/main/docs/pipeline-overview.png) <!-- Replace with your image path -->

## 📊 Key Features

- Real-time streaming fraud detection
- Scalable architecture using Spark and Kafka
- Intelligent grouping of fraud types using LSH
- Logistic Regression model trained on historical patterns
- Clean, modular codebase with Docker-based deployment

## 📁 Repository Structure

├── spark/ # Spark scripts and config
├── producer/ # Kafka producer code
├── cql/ # CQL queries and setup
├── Scripts/ # Data transformation scripts
├── Data_cleaning_spark.py # Data cleaning logic
├── main.ipynb # ML model training and evaluation
├── docker-compose.yml # Docker orchestration
├── TestProject.ipynb # End-to-end pipeline walkthrough
└── README.md


## 🤝 Team Collaboration

- ✅ Agile Scrum with 1-week sprints  
- ✅ Version control with GitHub  
- ✅ Pair programming using Google Colab  
- ✅ Task tracking with Trello

## 🧪 Evaluation

- **Metric Used**: AUC-ROC  
- **Result**: 0.92  
- **Insights**: Feature importance revealed EXCLTYPE categories and physician payment patterns as strong fraud indicators.

![AUC ROC Curve](https://github.com/leoncorreia/DATA228-termproject/blob/main/docs/auc-roc.png) <!-- Replace with your image -->

## 🔒 Privacy Considerations

Although k-anonymity wasn't implemented, the project highlights the importance of privacy-preserving techniques like k-anonymity and differential privacy for future deployment in production healthcare systems.

## 🚀 Future Scope

- Integration of deep learning models (e.g. autoencoders, ensemble models)
- CI/CD pipeline for real-time model updates
- Deployment to a cloud-based scalable infrastructure (e.g., GCP or AWS)

## 📎 Report & Presentation

- [📄 Final Project Report (PDF)](link) <!-- Replace with your own link -->
- [🎥 Elevator Pitch Video](link)
- [🗂️ Trello Dashboard](https://trello.com/invite/b/vWHhpPvj/ATTI35053ec29557657968413232b04859899E4D863A/big-data)


## 🧠 Lessons Learned

This project demonstrated the complexity of building production-ready big data pipelines and the importance of integrating distributed systems, real-time streaming, and privacy-aware machine learning models in modern healthcare analytics.

---

## 📌 Suggested Repository Name

Consider renaming your GitHub repository to something like:

