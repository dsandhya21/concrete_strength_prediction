# Concrete-compressive-strength

# Concrete Compressive Strength — ML Prediction Project  

## 📄 Overview  
This project presents an end-to-end machine learning pipeline designed to predict **concrete compressive strength (MPa)** using mixture proportions (cement, water, aggregates, admixtures) and curing age.  
The workflow includes **exploratory data analysis (EDA), feature scaling, model development, and performance evaluation** using multiple regression algorithms such as Linear Regression, Lasso, Ridge, Decision Tree, and Random Forest.

The aim is to identify the most accurate prediction model and extract meaningful engineering insights.  
As part of the model comparison, **Random Forest achieved the best performance**, and the analysis highlighted key factors influencing concrete strength, including **cement content, water-to-cement behavior, and curing age**.

## 🧰 Data Description  
**Dataset:** UCI Concrete Compressive Strength Dataset (1030 samples, 8 input variables + 1 target)  
**Inputs:** Cement, Blast Furnace Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate (kg/m³), and Age (days)  
**Output:** Concrete Compressive Strength (MPa)  
**Source:** https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength  

## 🔧 Methodology  
1. **Exploratory Data Analysis (EDA):** Examined correlations, patterns, and distributions to understand relationships among features and strength.  
2. **Preprocessing:**  
   - Applied feature scaling for linear models  
   - Performed an 80/20 train–test split  
3. **Model Development:**  
   - Linear Regression  
   - Lasso Regression  
   - Ridge Regression  
   - Decision Tree Regressor  
   - Random Forest Regressor  
4. **Model Evaluation:**  
   Computed MAE, MSE, RMSE, and R².  
   Compared model performance using bar plots and metrics tables.  
5. **Feature Importance:**  
   Used Random Forest and Decision Tree to understand the contribution of each ingredient toward strength prediction.  

## 📊 Key Results & Findings  
- **Best-performing model:** Random Forest — RMSE ≈ **5.08 MPa** (significantly lower than linear models, which were around 10 MPa).  
- **Most influential features:** Cement, Age (curing), and Water.  
- **Insights:**  
  - Higher cement content and longer curing age improve strength.  
  - Increased water content generally reduces strength (aligning with water–cement ratio theory).  
- **Summary:** The Random Forest model consistently produced the most accurate predictions and captured the underlying nonlinear behavior of concrete materials.

## 📈 Visualizations  

**Correlation Heatmap:**  
Shows how mixture proportions and age correlate with strength.  
![Correlation Heatmap](images/corr.png)

**Model Performance Comparison (RMSE):**  
Visual comparison of all regression models.  
![Model Comparison](images/comparision.png)

**Feature Importance:**  
Importance scores derived from tree-based models.  
![Feature Importance](images/feat_imp.png)

## 🎯 Reproducibility & Setup  
- **Notebook:** [ConcreteCompressiveStrengthPrediction.ipynb](./ConcreteCompressiveStrengthPrediction.ipynb)  
- **Tools/Libraries:** Python 3.x, pandas, numpy, scikit-learn, matplotlib, seaborn  
- **Random seed:** 42  

## 📝 Notes
- This project was carried out to understand how machine learning can improve concrete mix performance prediction.
- The dataset used for training and evaluation is from the UCI Machine Learning Repository.


