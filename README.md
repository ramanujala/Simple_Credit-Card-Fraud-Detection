# 🛡️ FraudShield Pro — Credit Card Fraud Detection & Analytics

**FraudShield Pro** is an end-to-end Machine Learning solution for detecting fraudulent credit card transactions in real-time. Built with **Scikit-Learn**, **Pandas**, **Plotly**, and **Streamlit**, it combines balanced ensemble learning with statistical anomaly profiling to deliver actionable insights and visual explanations for every transaction.

---

## 🌟 Highlights & Key Features

- **High Performance ML Engine**: Leverages a balanced `RandomForestClassifier` trained on severe class imbalance (0.17% fraud rate), achieving a **ROC-AUC score of 0.9836** and **0.83 Recall** on unseen test data.
- **Statistical Anomaly Explanation**: Computes feature Z-Scores against legitimate baseline distributions to highlight top outlying factors driving fraud predictions.
- **Interactive Streamlit Web Dashboard**:
  - **Transaction Predictor**: Test real-time prediction using sample test cases or manual custom inputs.
  - **Exploratory Data Analysis (EDA)**: Log-scale amount distributions, V17/V12 cluster separation, and interactive correlation heatmaps.
  - **Model Evaluation**: Confusion Matrix, Precision, Recall, Accuracy, and ROC-AUC metrics visualized.
- **Modern Neon Dark-Mode UI**: Designed with gradient titles, glassmorphism cards, and interactive Plotly visuals.

---

## 📁 Repository Structure

```text
fraud-detection/
│
├── train_model.py               # ML Training pipeline, evaluation, and asset generation
├── app.py                       # Interactive Streamlit Web Application
├── creditcard.csv               # Kaggle Credit Card Fraud Detection Dataset (284,807 rows)
├── fraud_model_assets.joblib    # Trained Random Forest model, scaler, and statistical profiles
├── sample_test_data.csv         # Sample test dataset for Streamlit UI dropdown selection
├── requirements.txt             # Python project dependencies
├── PROJECT_REPORT.md            # Detailed technical project report
└── README.md                    # Project documentation & overview
```

---

## ⚙️ Installation & Setup

### 1. Prerequisites
Ensure you have **Python 3.9+** installed on your system.

### 2. Clone Repository & Setup Virtual Environment
```bash
git clone https://github.com/ramanujala/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection

# Create virtual environment
python -m venv .venv

# Activate virtual environment (Windows PowerShell)
.\.venv\Scripts\Activate.ps1

# Install required packages
pip install -r requirements.txt
```

---

## 🚀 Usage Instructions

### Step 1: Train the Machine Learning Model
Train the Random Forest classifier and extract statistical feature profiles:
```powershell
.\.venv\Scripts\python.exe train_model.py
```
*Output*: Generates `fraud_model_assets.joblib` and `sample_test_data.csv`.

### Step 2: Launch the Web Dashboard
Start the interactive Streamlit application:
```powershell
.\.venv\Scripts\streamlit.exe run app.py
```
Open your web browser and navigate to `http://localhost:8501`.

---

## 📊 Model Evaluation Summary

| Metric | Score / Value |
| :--- | :--- |
| **ROC-AUC Score** | `0.9836` |
| **Recall (Fraud Class)** | `83.00%` |
| **Precision (Fraud Class)** | `78.00%` |
| **Accuracy** | `99.92%` |
| **Testing Set Size** | 50,100 transactions (50,000 Legit, 100 Fraud) |

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).