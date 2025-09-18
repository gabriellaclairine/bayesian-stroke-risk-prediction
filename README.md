# Bayesian Stroke Risk Prediction

This project develops a **Bayesian Logistic Regression** model to predict the risk of **stroke** using healthcare data.  
The dataset used is the **Healthcare Stroke Prediction Dataset** with 5,110 observations.

## 📌 Objectives
- Identify significant factors (age, hypertension, heart disease, average glucose level, etc.) contributing to stroke risk.
- Compare the performance of two Bayesian models with different priors.
- Evaluate models using **WAIC** and **DIC**.

## 📂 Dataset
- **File**: `healthcare-dataset-stroke-data.csv`
- **Main features**:
  - Demographics: gender, age, marital status, residence type, work type
  - Health conditions: hypertension, heart disease, BMI, average glucose level
  - Lifestyle: smoking status
  - Label: `stroke` (0 = no stroke, 1 = stroke)

## ⚙️ Methodology
- **Preprocessing**: missing value imputation (BMI), categorical encoding, numerical scaling.
- **Model**: Bayesian Logistic Regression built with the `rjags` package.
- **Evaluation**: WAIC, DIC, and MCMC diagnostics (trace plots, autocorrelation, Gelman-Rubin, Geweke).

## 📊 Key Findings
- Most significant predictors: **age**, **hypertension**, and **average glucose level**.
- Model 2 (with more informative priors) achieved **WAIC = 1624.9** and **DIC = 1610**, slightly better than Model 1.
