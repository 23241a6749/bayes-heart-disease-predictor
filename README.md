# 🩺 Bayes to the Future: Predicting Heart Disease with Bayesian Networks

A beginner-friendly project using **Bayesian Networks** to model and infer the **risk of heart disease** based on key health indicators like age, cholesterol, fasting blood sugar, and maximum heart rate.

---

## 📌 Project Overview

This project was built as part of the [HackWeek AI/ML Challenge - "Bayes to the Future"](https://bit.ly/3T1A7Rs). Using the Python library `pgmpy`, we created a **Bayesian Network** from a simulated dataset of patient records to estimate the probability of heart disease.

---

## 🧠 Problem Statement

Given a patient’s **age**, **fasting blood sugar**, **cholesterol**, and **max heart rate**, can we **predict the probability of heart disease**?

We model this using the following Bayesian Network structure:

age → fbs → target → {chol, thalach}


Where:
- `age` = Age of the patient (normalized)
- `fbs` = Fasting blood sugar (>120 mg/dl)
- `target` = Presence of heart disease (1 = disease, 0 = no disease)
- `chol` = Serum cholesterol in mg/dl (normalized)
- `thalach` = Max heart rate achieved (normalized)

---

## 📂 Project Structure

bayes-heart-disease-predictor/
├── data/
│ └── heart_disease.csv
├── notebooks/
│ └── Bayesian_Heart_Disease_Predictor.ipynb
├── README.md
└── requirements.txt


## 🔧 Setup Instructions

### 🔹 Requirements
Install dependencies:

```bash
pip install -r requirements.txt
'''

---
**🔹 Running the Project**
1. Open Bayesian_Heart_Disease_Predictor.ipynb (use Google Colab or Jupyter)

2. Upload the dataset: heart_disease.csv

3. Run all the cells step-by-step

**🧹 Data Preprocessing Steps**
1. Removed duplicate records

2. Dropped rows with missing values

3. Applied Min-Max Normalization to numeric columns like age, chol, thalach

**🧠 Bayesian Network Training**
1. Built structure: age → fbs → target → {chol, thalach}

2. Trained the model using Maximum Likelihood Estimation (MLE) via pgmpy

3. Learned Conditional Probability Distributions (CPDs) from data

**🔮 Inference Examples**
✅ 1. What is the probability of heart disease given age?
P(target | age = 0.8125)
✅ 2. What is the cholesterol distribution for people with heart disease?
P(chol | target = 1)
✅ 3. What is the max heart rate distribution for age and fasting blood sugar?
P(thalach | age = 0.75, fbs = 0)

**📸 Sample Output**
Inference Result
![image](https://github.com/user-attachments/assets/cd3ba7f0-7677-449f-8f99-7b405224c631)

CPD Table (Conditional Probability Distribution)
![image](https://github.com/user-attachments/assets/a06e6404-f787-45fb-9860-631d699a8c56)
![image](https://github.com/user-attachments/assets/18d2a713-bb2a-4916-a382-6fb4430f991e)
![image](https://github.com/user-attachments/assets/3f3a31a9-46be-4131-ae7b-07787e23c5bf)
![image](https://github.com/user-attachments/assets/c00afa4e-1b72-486d-aeea-e9501fe50fa4)

**🔬 Libraries Used**
pgmpy - For building and training Bayesian Networks
pandas - Data manipulation
numpy - Numeric operations
scikit-learn - Min-Max normalization
matplotlib - Optional: for visualizations

**🏁 Conclusion**
This project demonstrates how probabilistic models like Bayesian Networks can be used for simple but powerful medical inference tasks. It's an easy-to-extend base for applying machine learning to healthcare!



