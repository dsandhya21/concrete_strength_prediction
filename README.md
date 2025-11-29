# Concrete-compressive-strength

# Concrete Compressive Strength — ML Prediction Project  

## 📄 Overview  
This project implements a full machine-learning workflow to predict **concrete compressive strength (MPa)** from mixture proportions (cement, water, aggregates, admixtures) and curing age. The objective was to compare multiple regression models, identify the best-performing algorithm, and understand which input features most strongly affect strength — providing insight useful for concrete mix design.

## 📁 Repository Contents  
- `ConcreteCompressiveStrengthPrediction.ipynb` — Jupyter notebook containing EDA, preprocessing, model training & evaluation, plots and analyses.  
- `images/` — folder containing plots used in this README (`corr.png`, `feat_imp.png`, `comparision.png`).  
- `README.md` — this documentation.  

## 🧰 Data Description  
**Dataset:** UCI Concrete Compressive Strength Dataset (1030 samples, 8 inputs + 1 target)  
**Input features:** Cement, Blast Furnace Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate (all in kg/m³), and Age (days)  
**Target:** Concrete Compressive Strength (MPa)  
**Source:** UCI ML Repository — https://archive.ics.uci.edu/ml/datasets/Concrete+Compressive+Strength  

## 🔧 Methodology  
1. **Exploratory Data Analysis (EDA):** Computed correlations, visualized distributions to inspect relationships between mixture inputs, age, and strength.  
2. **Preprocessing:** Applied feature scaling (standardization) for linear models; performed train/test split (e.g., 80% train / 20% test).  
3. **Models trained:** Linear Regression, Lasso, Ridge, Decision Tree Regressor, Random Forest Regressor.  
4. **Evaluation metrics:** MAE, MSE, RMSE, R² on test data. Also compared models via bar charts.  
5. **Feature-importance and interpretation:** Used Random Forest and Decision Tree to extract importance scores; interpreted results in the context of concrete mix design (e.g., water-to-cement ratio, cement content, curing age).

## 📊 Key Results & Findings  
- **Best model:** Random Forest — Test RMSE ≈ **5.08 MPa** (much lower than linear models ~10 MPa), R² ≈ *give your value*.  
- **Importance ranking (top 3):** Cement > Age (curing) > Water. Aggregates and mineral admixtures had lower influence.  
- **Engineering implication:** To maximize compressive strength, mix design should prioritize cement content and proper curing age, while controlling water content.  

## 📈 Visualizations  

**Correlation Heatmap (feature vs strength correlations):**  
![Correlation Heatmap](images/corr.png)

**Model Performance Comparison (RMSE across algorithms):**  
![Model Comparison](images/comparision.png)

**Feature Importance (Random Forest & Decision Tree):**  
![Feature Importance](images/feat_imp.png)

## 🎯 Reproducibility & Setup  
- **Notebook link:** [ConcreteCompressiveStrengthPrediction.ipynb](./ConcreteCompressiveStrengthPrediction.ipynb)  
- **Environment:** Python 3.x; libraries: pandas, numpy, scikit-learn, matplotlib, seaborn (see notebook for exact versions)  
- **Random seed:** 42 (ensures consistent train/test split and reproducible results)  

## 📝 Notes
- This project was carried out to understand how machine learning can improve concrete mix performance prediction.
- The dataset used for training and evaluation is from the UCI Machine Learning Repository.


