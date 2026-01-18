# Regression-Analysis-to-Predict-House-Prices-Python
Predict house prices using simple linear regression (Python, scikit-learn)
# Task 1: Regression Analysis (Level 2 - Intermediate)

## Internship Project

This project is part of my internship tasks. The objective is to perform **simple linear regression** to predict house prices (`MEDV`) based on the average number of rooms (`RM`) using the **House Prediction dataset**.

---

## Dataset

**File:** `House prediction dataset.csv`  
**Description:**  
- 14 numeric features per house  
- Last column `MEDV` is the **median house price**, which is the target variable.  

**Columns:**

| Column | Description |
|--------|-------------|
| CRIM | Crime rate per town |
| ZN | Residential land zoned for lots >25,000 sq.ft. |
| INDUS | Proportion of non-retail business acres |
| CHAS | Charles River dummy variable (1 if tract bounds river, 0 otherwise) |
| NOX | Nitric oxide concentration |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built prior to 1940 |
| DIS | Weighted distances to employment centers |
| RAD | Index of accessibility to radial highways |
| TAX | Full-value property-tax rate |
| PTRATIO | Student–teacher ratio by town |
| B | Neighborhood index (1000(Bk − 0.63)^2) |
| LSTAT | % lower status of the population |
| MEDV | Median value of owner-occupied homes (target) |

---

## Objective

- Perform **simple linear regression** using `RM` → `MEDV`.  
- Evaluate model performance with:
  - **R-squared (R²)**  
  - **Mean Squared Error (MSE)**  
- Interpret coefficients and visualize predictions.

---

## Methodology

1. Load dataset using `pandas` and assign column names.  
2. Select predictor (`RM`) and target (`MEDV`).  
3. Split dataset into **training (80%)** and **testing (20%)** sets.  
4. Fit a **linear regression model** using `scikit-learn`.  
5. Predict house prices on the test set.  
6. Evaluate model performance (R², MSE).  
7. Interpret coefficients:
   - **Slope:** price increase per additional room  
   - **Intercept:** predicted price when rooms = 0  
8. Visualize results with a scatter plot and regression line.  
9. Compare actual vs predicted prices in a table.

---

## Results

- **R-squared (R²):** 0.371 → 37% of variance in house price explained by number of rooms.  
- **Mean Squared Error (MSE):** 46.14  
- **Slope (RM):** 9.35 → each additional room increases predicted price by ~9.35k.  
- **Intercept:** -36.25 → predicted price when RM = 0 (theoretical).  

**Regression Plot:**

## Regression Plot

![Simple Linear Regression](https://raw.githubusercontent.com/Chisom-Okoli/Regression-Analysis-to-Predict-House-Prices-Python/main/Simple%20linear%20regression.png)



**Sample Actual vs Predicted Prices:**

| Actual | Predicted |
|--------|-----------|
| 24.0   | 23.5      |
| 21.6   | 20.8      |
| 34.7   | 32.9      |
| 33.4   | 31.5      |
| 36.2   | 35.0      |

## Interpretation of Results

The analysis indicates a positive relationship between the average number of rooms and house price. This means that, in general, houses with more rooms tend to have higher prices.

However, the model explains only 37% of the variation in house prices, which suggests that room count alone is not sufficient to accurately predict property value. Other factors such as location, crime rate, proximity to employment centers, and neighborhood characteristics likely play a significant role in determining house prices.
