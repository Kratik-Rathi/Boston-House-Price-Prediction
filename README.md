# Boston House Price Analysis & Prediction

This repository provides a comprehensive analysis of the Boston Housing Price dataset and implements various machine learning models to predict housing prices. The project highlights key insights from the data and evaluates the performance of different predictive models.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset Information](#dataset-information)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Modeling Techniques](#modeling-techniques)
- [Results](#results)
- [Future Work](#future-work)

---

## Project Overview

The primary goal of this project is to predict the median value of owner-occupied homes in the Boston area based on various features. Through exploratory data analysis, model training, and evaluation, we derive insights into the factors affecting housing prices and assess the performance of different regression techniques.

## Dataset Information

The Boston Housing dataset includes 506 observations with the following features:

| Feature  | Description |
|----------|-------------|
| **CRIM** | Per capita crime rate by town |
| **ZN**   | Proportion of residential land zoned for lots over 25,000 sq. ft. |
| **INDUS**| Proportion of non-retail business acres per town |
| **CHAS** | Charles River dummy variable (1 if tract bounds river; 0 otherwise) |
| **NOX**  | Nitric oxides concentration (parts per 10 million) |
| **RM**   | Average number of rooms per dwelling |
| **AGE**  | Proportion of owner-occupied units built prior to 1940 |
| **DIS**  | Weighted distances to five Boston employment centers |
| **RAD**  | Index of accessibility to radial highways |
| **TAX**  | Full-value property-tax rate per $10,000 |
| **PTRATIO** | Pupil-teacher ratio by town |
| **B**    | 1000(Bk - 0.63)^2, where Bk is the proportion of Black residents |
| **LSTAT**| % lower status of the population |
| **MEDV** | Median value of owner-occupied homes in $1000s (target variable) |

## Exploratory Data Analysis (EDA)

Key findings from the EDA:
- **RM** (number of rooms) shows a strong positive correlation with **MEDV** (correlation = 0.695).
- **LSTAT** (lower status population) is negatively correlated with **MEDV** (correlation = -0.738).
- **TAX** and **RAD** have a high positive correlation (correlation = 0.910), indicating potential multicollinearity.
- Outliers and skewed distributions are observed in features like **CRIM** and **LSTAT**.

## Feature Engineering

- **Normalization/Standardization**: Applied to features to improve model performance.
- **Polynomial Features**: Added quadratic terms to enhance model complexity.

## Modeling Techniques

The following models were implemented and evaluated:

### 1. **Linear Regression**
   - **Training Loss**: 22.35
   - **Validation Loss**: 22.31

### 2. **Ridge Regression**
   - **Optimal Regularization Parameter (α)**: 1
   - Improved generalization compared to Linear Regression.

### 3. **Lasso Regression**
   - Effective for feature selection by shrinking less important feature coefficients to zero.
   - **Best α**: 0.01
   - Mean RMSE: 3.72

### 4. **Polynomial Regression (Degree 2)**
   - Captures non-linear relationships.
   - Ridge with **α = 10**: **Lowest Mean RMSE = 3.55**

### 5. **Stochastic Gradient Descent (SGD) Regression**
   - Iterative optimization for large datasets.
   - Converged Training Loss: 22.35 (after 1500 iterations).

## Results

| Model                       | Training Loss | Validation Loss | Best RMSE |
|-----------------------------|---------------|-----------------|-----------|
| **Linear Regression**       | 22.35         | 22.31           | 4.25      |
| **Ridge Regression**        | 21.87         | 21.45           | 3.95      |
| **Lasso Regression**        | 22.15         | 21.88           | 3.72      |
| **Polynomial Ridge (α=10)** | 18.55         | 17.95           | 3.55      |

---

## Future Work

- **Model Improvements**:
  - Implement ensemble models like Random Forests, Gradient Boosting, and XGBoost.
- **Feature Engineering**:
  - Incorporate interaction terms and non-linear transformations.
- **Outlier Handling**:
  - Use robust regression techniques or advanced outlier detection methods.
- **Hyperparameter Tuning**:
  - Perform a comprehensive grid search for optimal parameters.

---
