# 🏠 House Prices - Advanced Regression Techniques (Kaggle Competition)

**Author:** Pablo Arango-Gomez  
**Competition:** Kaggle - House Prices: Advanced Regression Techniques  
**Score Achieved:** 0.16375  

---

## Overview

This project is a solution to the **House Prices - Advanced Regression Techniques** Kaggle competition. The goal was to develop a machine learning model to predict house sale prices based on various features. This solution uses **data preprocessing**, **feature engineering**, and **Linear Regression modeling** to produce competitive predictions.

---

## Key Features

- **Comprehensive Data Cleaning & Null Handling**:
  - Automatic filling of missing numeric values using column means.
  - Data filtering to retain only numeric columns for regression modeling.

- **Feature Engineering**:
  - Custom feature creation (e.g., `Age` feature computed as `YrSold - YearBuilt`).
  - Transformation of skewed data using log and square root to normalize distributions (e.g., `GrLivArea`, `TotalBsmtSF`, `1stFlrSF`).

- **Logarithmic Transformation of Target Variable**:
  - Applied `np.log()` to `SalePrice` to reduce skew and improve linear modeling.

- **Correlation Analysis & Feature Selection**:
  - Generation of correlation matrix to identify top features influencing house prices.
  - Visualization of feature-to-price relationships using scatter plots.

- **Model Training & Prediction**:
  - Trained **Linear Regression** model using selected top features.
  - Final predictions transformed back using `np.exp()` for submission.

---

## Technologies & Libraries

- **Python**
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical computations
- **Matplotlib** — Data visualization
- **Scikit-learn** — Machine learning model (Linear Regression)
- **Jupyter Notebook** — Development environment

---

## Process & Methodology

### 1. Data Preprocessing
- Removed non-numeric columns to simplify modeling.
- Filled missing numeric values with the column's mean to avoid data loss.

### 2. Feature Engineering
- Created new `Age` feature: `YrSold - YearBuilt`.
- Log-transformed `SalePrice` into `LogPrice` for normal distribution.

### 3. Addressing Skewed Features
- Applied `np.log()` and `np.sqrt()` to skewed variables identified through histograms.

### 4. Correlation Analysis
- Identified top correlated features with `SalePrice` for model training:
  - `OverallQual`, `GrLivArea`, `GarageCars`, `GarageArea`, `1stFlrSF`, `FullBath`, `TotalBsmtSF`, `TotRmsAbvGrd`, `YearBuilt`.

### 5. Model Training
- Fitted a Linear Regression model on the cleaned and engineered dataset.
- Generated predictions and reversed log transformation for final sale price output.

---
