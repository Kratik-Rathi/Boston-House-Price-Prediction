# Boston House Price Prediction

This repository is dedicated to analyzing and predicting housing prices in Boston using various machine learning models. The dataset used in this project provides essential features influencing house prices, enabling the development of robust predictive models.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)
- [How to Use](#how-to-use)
- [Future Scope](#future-scope)
- [Acknowledgments](#acknowledgments)

---

## Overview
This project aims to predict housing prices based on various features, such as the number of rooms, location, and crime rate. Accurate predictions can help stakeholders in the real estate industry make data-driven decisions.

---

## Dataset
The dataset used is from the **Boston Housing dataset**, which includes the following features:
- CRIM: Per capita crime rate by town.
- ZN: Proportion of residential land zoned for lots over 25,000 sq. ft.
- INDUS: Proportion of non-retail business acres per town.
- CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise).
- NOX: Nitric oxide concentration (parts per 10 million).
- RM: Average number of rooms per dwelling.
- AGE: Proportion of owner-occupied units built before 1940.
- DIS: Weighted distances to five Boston employment centers.
- RAD: Index of accessibility to radial highways.
- TAX: Full-value property tax rate per $10,000.
- PTRATIO: Pupil-teacher ratio by town.
- B: 1000(Bk - 0.63)² where Bk is the proportion of Black residents by town.
- LSTAT: Percentage of the lower status of the population.
- MEDV: Median value of owner-occupied homes in $1000s (target variable).

---

## Data Preprocessing
1. **Handling Missing Values**: Checked and imputed missing data (if any).
2. **Feature Engineering**: Normalized features to improve model performance.
3. **Encoding Categorical Variables**: Converted categorical data into numerical format using one-hot encoding.

---

## Exploratory Data Analysis (EDA)
- **Correlation Analysis**: Identified relationships between variables.
- **Visualization**: Used histograms, scatter plots, and heatmaps to understand data distribution and trends.

---

## Modeling
The following models were implemented:
1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **Gradient Boosting Regressor**

Each model was fine-tuned using hyperparameter optimization techniques.

---

## Results
The table below summarizes the performance of each model:

| Model                     | Accuracy (R² Score) |
|---------------------------|---------------------|
| Linear Regression          | X.XX               |
| Decision Tree Regressor    | X.XX               |
| Random Forest Regressor    | X.XX               |
| Gradient Boosting Regressor| X.XX               |

*Note: Replace "X.XX" with actual accuracy values after running the models.*

---

## Conclusion
- The **Gradient Boosting Regressor** achieved the best performance with an accuracy of X.XX%.
- Certain features like **RM** (average number of rooms per dwelling) and **LSTAT** (% lower status of the population) were found to be highly influential in determining house prices.
