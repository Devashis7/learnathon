# 🚗 AI-Powered Fraud Detection in Auto Insurance

This repository contains the full code, analysis, and results for our Learnathon project: an intelligent machine learning system to detect fraudulent auto insurance claims.

## 📌 Problem Statement

**AI-Powered Fraud Detection in Auto Insurance: Predictive Modeling for Smarter Claims Management**

Insurance fraud is a growing concern in the auto industry. The goal of this project is to build a predictive model that accurately classifies whether a given insurance claim is fraudulent, based on detailed policy, personal, and accident-related data.

---
## Team Name: Team(SC2)4_2
## 👥 Team Members

| Name                   | Roll No      |
|------------------      |-----------------|
| Devashis Kumar         | 22CSE209      |
| Akshay Kumar           | 22CSE217  |
| Rohit Kumar            | 22CSE163     |
| Nitesh Kumar Prasad    | 22CSE280     |

---

## 🧠 Project Workflow

### ✅ Data Preparation
- Merged multiple training files.
- Converted date fields and extracted derived features (`policy_age`, `claim_report_delay`).
- Removed data leakage columns (claim amount, registration, etc.).
- Handled missing values via category mapping and encoding.
- Used:
  - Ordinal Encoding (`Education`, `Accident_Severity`)
  - Frequency Encoding (`Occupation`, `Hobbies`)
  - Manual Mapping (`Accident_Type`, `Collision_Type`, `authorities_contacted`)
  - One-Hot Encoding (`Gender`, `Policy_State`, etc.)

### ⚖️ Class Imbalance
- Applied SMOTE to oversample minority class after splitting data.

### 🔍 Models Trained
We tested and evaluated over 10 models. Here are the top-performing ones:

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC | Train Time (s) |
|---------------------|----------|-----------|--------|----------|---------|----------------|
| **XGBoost**         | 1.000    | 1.000     | 1.000  | 1.000    | 1.000   | 1.12           |
| **Random Forest**   | 1.000    | 1.000     | 1.000  | 1.000    | 1.000   | 16.87          |
| **LightGBM**        | 1.000    | 1.000     | 1.000  | 1.000    | 1.000   | 1.49           |
| Decision Tree       | 0.9998   | 1.000     | 0.999  | 0.9997   | 0.9997  | 1.72           |
| Gradient Boosting   | 0.9048   | 0.7475    | 0.9427 | 0.8339   | 0.9829  | 29.41          |
| Logistic Regression | 0.6353   | 0.3795    | 0.6928 | 0.4904   | 0.6956  | 0.91           |

✅ **Best Model Selected**: `XGBoost`, due to perfect generalization + fastest runtime among top scorers.

---

## 📊 Evaluation Tools
- Confusion Matrix
- ROC Curve
- Classification Report
- F1-Score-based model ranking

---

## 🚀 Getting Started

### 🖥️ Requirements
This project was developed and tested in **Google Colab**. You’ll need:

- Python 3.11+
- scikit-learn
- imbalanced-learn
- xgboost
- lightgbm
- pandas, numpy, matplotlib

You can run the entire pipeline from our notebook:

▶ **[Colab Notebook Link](https://colab.research.google.com/drive/1DH9-ul9iyqKr_4XtrwyVhNWiwxnFkZ_W?usp=sharing)**

---
---

## 🎥 Project Demo Video

Watch the walkthrough of our complete approach and final model:

▶ [Demo Video Link (Google Drive)](https://drive.google.com/drive/folders/15KCW59jSZ4fBU5T9Ac32feJUR3bQE6qP?usp=drive_link)

---
## 🖼️ Final Presentation

The final results and project explanation are also included in this repo:

📂 `AI_Insurance_Fraud_Presentation.pptx`  
- Problem Statement  
- ML Pipeline  
- Evaluation  
- Key Insights  
- Learnings  

---

## 💡 Key Learnings

- How to spot and eliminate data leakage
- Feature engineering and encoding strategy for real-world tabular data
- Model selection and interpretation using precision, recall, F1, and ROC-AUC
- Handling class imbalance with SMOTE

---

## 📜 License

This project is for educational purposes only, under the Learnathon initiative. Not licensed for commercial use.

---

## 🙌 Acknowledgements

Thanks to the mentors and organizers of the Learnathon for providing guidance and this real-world ML challenge.
