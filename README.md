# ❤️ Heart Disease Risk Prediction

A machine learning-based web application that predicts the likelihood of heart disease using patient health information.

The project compares multiple classification algorithms and deploys the best-performing model, K-Nearest Neighbors (KNN), through a Streamlit web application.

## 🚀 Live Demo

🔗 [Try the Heart Disease Risk Prediction App](https://heart-disease-detection-v2gt7efcsubak47jgidrk6.streamlit.app/)

## 📌 Project Overview

Heart disease is one of the major health concerns worldwide. This project uses machine learning to estimate the likelihood of heart disease based on medical and physiological attributes such as age, blood pressure, cholesterol, chest pain type, maximum heart rate, and other clinical indicators.

The project covers the complete machine learning workflow:

- Exploratory Data Analysis
- Data Cleaning
- Feature Encoding
- Feature Scaling
- Model Training
- Model Comparison
- Model Evaluation
- Model Serialization
- Streamlit Deployment

## 🎯 Objectives

- Analyze the heart disease dataset.
- Identify patterns and relationships between patient characteristics and heart disease.
- Preprocess categorical and numerical features.
- Compare multiple machine learning classification algorithms.
- Select the best-performing model.
- Build an interactive Streamlit application for predictions.

## 📊 Machine Learning Workflow

### 1. Exploratory Data Analysis

The dataset was explored using:

- Dataset structure and dimensions
- Statistical summaries
- Duplicate-value checks
- Missing-value checks
- Distribution plots
- Count plots
- Box plots
- Violin plots
- Correlation heatmap

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Zero values in `Cholesterol` were replaced with the mean of non-zero values.
- Zero values in `RestingBP` were replaced with the mean of non-zero values.
- Categorical variables were converted using one-hot encoding.
- The target variable was separated from the input features.
- Features were standardized using `StandardScaler`.

## 🤖 Models Compared

Five classification algorithms were evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Gaussian Naive Bayes
4. Decision Tree
5. Support Vector Machine (SVM with RBF Kernel)

## 📈 Model Performance

| Model | Accuracy | F1 Score |
|---|---:|---:|
| Logistic Regression | 87.50% | 88.78% |
| **KNN** | **88.59%** | **89.86%** |
| Naive Bayes | 86.96% | 87.88% |
| Decision Tree | 75.54% | 76.92% |
| SVM (RBF Kernel) | 86.41% | 88.04% |

### 🏆 Best Model: KNN

K-Nearest Neighbors achieved the highest performance among the evaluated models:

- **Accuracy: 88.59%**
- **F1 Score: 89.86%**

The KNN model was therefore selected for deployment.

## 🌐 Streamlit Application

The trained KNN model was integrated into an interactive Streamlit application.

Users can provide:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise-Induced Angina
- Oldpeak
- ST Slope

The application processes the inputs using the same preprocessing pipeline and generates a heart disease risk prediction.

## 🗂️ Project Structure

```text
Heart-Disease-Detection/
│
├── App.py
├── heart.csv
├── heart (1).ipynb
├── KNN_heart.pkl
├── scaler.pkl
├── columns.pkl
├── requirements.txt
└── README.md
