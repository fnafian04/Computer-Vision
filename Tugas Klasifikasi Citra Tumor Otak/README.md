# 🧠 Brain Tumor MRI Classification  
### Machine Learning-Based Medical Image Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-RandomForest-orange?logo=scikitlearn)
![Accuracy](https://img.shields.io/badge/Accuracy-98.41%25-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

---

## 🚀 Project Overview

This project focuses on **automatic brain tumor detection** from MRI images using a **Machine Learning approach**.  
By leveraging **statistical texture analysis (GLCM)** and a **Random Forest Classifier**, the system can distinguish between:

- 🔴 Tumor (Abnormal tissue detected)  
- 🟢 Non-Tumor (Healthy brain condition)  

💡 *The goal is to assist early diagnosis by reducing dependency on manual visual interpretation.*

---

## 🧠 Key Highlights

- ⚡ High accuracy: **98.41%**
- 📊 Based on **13 statistical texture features**
- 🌲 Robust model using **Random Forest (100 estimators)**
- 📈 Interpretable results via **Feature Importance**
- 🏥 Applicable to **medical image analysis domain**

---

## 🔗 Important Links

- 📂 Dataset (CSV) : https://www.kaggle.com/datasets/jakeshbohaju/brain-tumor  
- 🐍 Google Colab : https://colab.research.google.com/drive/1U8uuk63oQZH4ziAKjLkYjAtztwwtRY-5?usp=sharing

---

## ⚙️ Methodology

### 1. Feature Extraction (GLCM)
Extracting texture-based features such as:
- Mean  
- Entropy  
- Energy  
- ASM (Angular Second Moment)  
- Homogeneity  

These features capture **texture irregularities** caused by tumor presence.

---

### 2. Data Preprocessing
- Standardization using `StandardScaler`
- Ensures:
  - Stable training process  
  - Balanced feature contribution  

---

### 3. Model Training

- Algorithm: **Random Forest Classifier**
- Number of Trees: **100**
- Reason:
  - Resistant to overfitting  
  - Performs well on tabular data  
  - Provides feature importance insights  

---

## 📊 Results & Evaluation

### ✅ Model Performance
- **Accuracy: 98.41%**
- Tested on **753 samples**

### 🎯 Feature Importance Insight
Top contributing features:
- Energy  
- ASM  
- Entropy  

📌 *Tumor presence significantly alters texture uniformity and randomness in MRI images.*

---

## 🛠️ Tech Stack

- **Python 3**
- **Scikit-Learn**
- **Pandas & NumPy**
- **Matplotlib & Seaborn**

---

## 📈 Workflow

```mermaid
graph TD
A[Dataset MRI] --> B[Feature Extraction GLCM]
B --> C[Preprocessing StandardScaler]
C --> D[Train Random Forest]
D --> E[Evaluation]
E --> F[Prediction: Tumor / Non-Tumor]
