 Loan Payment Prediction System

## Table of Contents
- [Overview](#overview)
- [Project Workflow](#project-workflow)
- [Tech Stack](#tech-stack)
- [Detailed Steps](#detailed-steps)
  1. [Exploratory Data Analysis (EDA)](#1-exploratory-data-analysis-eda)
  2. [Data Preprocessing](#2-data-preprocessing)
  3. [Model Development](#3-model-development)
  4. [Experiment Tracking with MLflow](#4-experiment-tracking-with-mlflow)
  5. [API Deployment with FastAPI](#5-api-deployment-with-fastapi)
  6. [Frontend Visualization with Streamlit](#6-frontend-visualization-with-streamlit)
  7. [Monitoring with Arize AI](#7-monitoring-with-arize-ai)
- [How to Run the Project](#how-to-run-the-project)
- [Future Enhancements](#future-enhancements)

## Overview
This project focuses on building a predictive system for determining loan payment outcomes. The pipeline is designed to handle real-world complexities like missing data, imbalanced classes, and scalable deployment.

### Key Objectives:
- Build a robust machine learning model for loan payment prediction.
- Deploy the model using FastAPI for integration with external systems.
- Provide an interactive Streamlit dashboard for users to visualize predictions and explore insights.
- Implement model monitoring with Arize AI to ensure consistent performance post-deployment.

## Project Workflow
1. Data Analysis and Preprocessing.
2. Model Development and Evaluation.
3. Experiment Tracking with MLflow.
4. API Deployment for Predictions.
5. Interactive Dashboard for End Users.
6. Continuous Monitoring and Feedback Loop.

## Tech Stack
- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, XGBoost, FastAPI, Streamlit
- **Model Tracking**: MLflow
- **Deployment Tools**: FastAPI, Streamlit
- **Monitoring**: Arize AI

## Detailed Steps

### 1. Exploratory Data Analysis (EDA)
- Understand the dataset and identify patterns, trends, and outliers.
- Key activities include descriptive statistics, visualizations, and class imbalance analysis.

**Tools Used**: Matplotlib, Seaborn, Pandas Profiling

### 2. Data Preprocessing
- Handle missing values using imputation techniques.
- Create new features (e.g., loan-to-income ratio).
- Normalize numeric data and encode categorical variables.
- Split the dataset into training and testing sets.
- Address class imbalance using SMOTE.

**Tools Used**: Scikit-learn, Imbalanced-learn

### 3. Model Development
- Test algorithms such as Logistic Regression, Random Forest, and XGBoost.
- Evaluate models using metrics like accuracy, precision, recall, F1 score, and ROC-AUC.
- Finalize the XGBoost model for deployment.

**Tools Used**: Scikit-learn, XGBoost

### 4. Experiment Tracking with MLflow
- Capture key metrics and hyperparameters for reproducibility.
- Save the best-performing model for deployment.

**Tools Used**: MLflow, SQLite

### 5. API Deployment with FastAPI
- Develop a FastAPI-based RESTful API with endpoints for predictions and health monitoring.
- Dockerize the application for portability.

**Endpoints**:
- `/predict`: Accepts JSON payloads and returns predictions.
- `/health`: Monitors API health.

**Tools Used**: FastAPI, Uvicorn

### 6. Frontend Visualization with Streamlit
- Create an interactive dashboard for model predictions and insights.
- Enable users to upload datasets and analyze trends.

**Tools Used**: Streamlit

### 7. Monitoring with Arize AI
- Log training and inference datasets with features, predictions, and actual outcomes.
- Track metrics like accuracy drift, data drift, and feature importance changes.

**Tools Used**: Arize AI SDK

## How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/LeithMbarek/Mlops.git
cd Mlops
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Start MLflow Tracking Server
```bash
mlflow ui
```

### 4. Run FastAPI Server
```bash
uvicorn main:app --reload
```

### 5. Launch Streamlit Dashboard
```bash
streamlit run main.py
```

### 6. Monitor with Arize AI
- Set up Arize API keys in your environment variables.
- View logged data on the Arize Dashboard.

## Future Enhancements
- **Advanced Hyperparameter Tuning**: Use Bayesian Optimization or Hyperopt.
- **Real-Time Predictions**: Integrate Kafka or RabbitMQ for streaming data.
- **Enhanced Monitoring**: Incorporate advanced drift detection techniques.
- **Support for Multiple Models**: Extend the pipeline to handle multiple model versions.

Feel free to contribute to this project by submitting pull requests or raising issues. 😊
