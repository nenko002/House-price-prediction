# House-price-prediction

An end-to-end machine learning workflow for the Kaggle “House Prices – Advanced Regression Techniques” competition. This repository now contains the full pipeline—from raw data to final submission.

---

## ✅ Progress

1. **Exploratory Data Analysis (EDA)**  
   – Inspected shapes, missing values, and SalePrice distribution  
   – Identified top raw predictors (OverallQual, GrLivArea, GarageCars, etc.)  

2. **Data Preprocessing**  
   – Imputed missing values (“None” for absent categories, medians for numeric gaps)  
   – Engineered features (total square footage, age, bathroom counts, binary flags)  
   – Encoded ordinal & nominal variables; aligned train/test feature sets  

3. **Modeling & Evaluation**  
   – Trained and tuned 5 algorithms (Ridge, Lasso, Random Forest, Gradient Boosting, XGBoost) via 5-fold CV  
   – Validation RMSEs (log-target):  
     - Ridge: 0.1295  Lasso: 0.1273  Random Forest: 0.1453  
     - **Gradient Boosting: 0.1226**  XGBoost: 0.1401  

4. **Feature Importance & Interpretation**  
   – Plotted top-20 importances for tree-based models  
   – Confirmed quality, size, and functional features drive price  

5. **Conclusion & Submission**  
   – Selected Gradient Boosting (learning_rate=0.05, n_estimators=200) as final model  
   – Predicted sale prices range \$54 190 to \$728 217  
   – Generated `submission.csv` ready for Kaggle

---

## 📂 What’s Included

- **Notebook**  
  – `notebooks/house-price-ml-pipeline.ipynb`: complete code covering Steps 1–5

- **Data**  
  – `dataset/train.csv` & `dataset/test.csv` (raw CSVs; listed in `.gitignore` to avoid versioning)

- **Environment**  
  – `requirements.txt`: Python dependencies  

---

## 🚀 Getting Started

1. **Clone this repo**  
   ```bash
   git clone https://github.com/nenko002/House-price-prediction.git
   cd House-price-prediction
   
2. **Install dependencies**

pip install -r requirements.txt
Download the raw data

Web UI:
Go to https://kaggle.com/competitions/home-data-for-ml-course/data
Download & unzip into dataset/

jupyter notebook notebooks/house-price-ml-pipeline.ipynb
