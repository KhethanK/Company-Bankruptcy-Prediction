# Company-Bankruptcy-Prediction
# 📉 Bankruptcy Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![ROC-AUC](https://img.shields.io/badge/ROC--AUC-0.78-brightgreen)
![Model](https://img.shields.io/badge/Model-Logistic%20Regression-blue)
![Status](https://img.shields.io/badge/Status-Production--Ready-success)
![Last Commit](https://img.shields.io/github/last-commit/your-username/bankruptcy-prediction)

<!-- Enable after adding GitHub Actions -->
<!--
![CI](https://github.com/your-username/bankruptcy-prediction/actions/workflows/ci.yml/badge.svg)
-->

---

## 🔍 Project Overview
This project develops a machine learning pipeline to predict **corporate bankruptcy risk** using financial indicators. The solution is designed to handle **class imbalance**, improve **risk detection**, and provide **reliable classification performance** for financial decision-making.

---

## 🎯 Business Objective
- Identify high-risk companies before financial failure  
- Support data-driven risk assessment  
- Improve detection of minority class (bankrupt firms)  

---

## 📊 Dataset Description

The dataset consists of financial ratios derived from company financial statements.

### Key Characteristics:
- **Problem Type**: Binary Classification  
- **Target Variable**: Bankruptcy (0 = No, 1 = Yes)  
- **Challenge**: Highly imbalanced dataset  

### 📌 Data Schema

| Feature | Description |
|--------|------------|
| ROA(C) before interest and depreciation | Profitability indicator |
| Operating Gross Margin | Operational efficiency |
| Current Ratio | Liquidity measure |
| Debt Ratio | Financial leverage |
| Net Worth/Assets | Financial stability |
| Total Asset Growth Rate | Growth metric |
| Liability-Assets Flag | Risk signal |
| Bankrupt? | Target variable |

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Missing value handling  
- Outlier detection using **IQR method**  
- Feature scaling and normalization  

### 2. Exploratory Data Analysis
- Distribution analysis  
- Correlation heatmaps  
- Class imbalance visualization  

### 3. Feature Engineering
- Removal of redundant features  
- Selection based on correlation and importance  

### 4. Handling Class Imbalance
- Applied **SMOTE (Synthetic Minority Oversampling Technique)**  
- Improved minority class representation  

### 5. Model Development
The following models were trained and evaluated:
- Logistic Regression  
- Random Forest  
- XGBoost  
- CatBoost  

---

## 📊 Model Performance

### ROC Curve Analysis

![ROC Curve](images/roc_curve.png)

### 📈 ROC-AUC Scores

| Model                | ROC-AUC |
|---------------------|--------|
| Logistic Regression | 0.7833 |
| CatBoost            | 0.7669 |
| Random Forest       | 0.7372 |
| XGBoost             | 0.7312 |

---

## 🔍 Key Insights
- **Logistic Regression achieved the highest ROC-AUC (0.78)**, indicating strong classification capability  
- Ensemble models (CatBoost, Random Forest, XGBoost) delivered competitive performance  
- Handling class imbalance significantly improved detection of bankrupt companies  
- Financial ratios are strong predictors of bankruptcy risk  

---

## 📌 Evaluation Strategy
Given class imbalance, performance was evaluated using:
- **ROC-AUC (Primary Metric)**  
- Precision  
- Recall  
- F1-Score  

> Accuracy was not used as a primary metric due to imbalance bias.

---

## 🏗️ Project Structure

bankruptcy-prediction/

│  
├── data/  
│   └── bankruptcy.csv  

│  
├── notebooks/  
│   └── bankruptcy_analysis.ipynb  

│  
├── images/  
│   └── roc_curve.png  

│  
├── models/  
│   └── trained_model.pkl  

│  
├── src/  
│   ├── preprocessing.py  
│   ├── training.py  
│   └── evaluation.py  

│  
├── requirements.txt  
├── README.md  
└── LICENSE  

---

## 🛠️ Tech Stack
- **Language**: Python  
- **Libraries**:  
  - Pandas, NumPy  
  - Scikit-learn  
  - XGBoost, CatBoost  
  - Imbalanced-learn (SMOTE)  
  - Matplotlib, Seaborn

## 📦 Installation

```bash
git clone https://github.com/your-username/bankruptcy-prediction.git
cd bankruptcy-prediction
pip install -r requirements.txt

jupyter notebook notebooks/bankruptcy_analysis.ipynb

---

## 📈 Future Improvements

- **Advanced Hyperparameter Optimization**  
  Implement automated tuning using **Optuna** or **GridSearchCV** to enhance model performance and generalization.

- **Model Explainability & Interpretability**  
  Integrate **SHAP** and **LIME** to provide transparent, feature-level insights into model predictions for better trust and decision-making.

- **Production Deployment**  
  Deploy the trained model using **Flask** or **FastAPI** to enable scalable, real-time inference through REST APIs.

- **Real-Time Risk Scoring System**  
  Build an end-to-end pipeline for continuous financial data ingestion and **real-time bankruptcy risk prediction**.

- **Model Monitoring & Drift Detection (Advanced)**  
  Implement monitoring to track performance degradation and detect **data drift** in production environments.

- **End-to-End MLOps Pipeline (Advanced)**  
  Incorporate CI/CD, versioning (MLflow), and automated retraining workflows for production-grade reliability.

---

## 🤝 Contribution

Contributions are welcome. Feel free to fork the repo and submit a pull request.

---

## 📬 Contact

For queries or collaboration:

* LinkedIn: https://www.linkedin.com/in/khethan-kalluru-7723aa376/
* Email: khethankalluru05@gmail.com

---

## ⭐ If you found this useful

Give this repo a star ⭐ — it helps visibility!
