# OLS Regression Analysis with Statsmodels

This repository contains a simple example of how to perform Ordinary Least Squares (OLS) linear regression using the `statsmodels` library in Python.

---

## Overview

We use a dataset with features such as `Weight` (independent variable) and `Height` (dependent variable) to build a linear regression model and analyze its performance.

---

## Code Explanation

1. **Data Preparation:**

```python
import statsmodels.api as sm

# Add constant term to the independent variables matrix
X_train_const = sm.add_constant(X_train)
X_test_const = sm.add_constant(X_test)

```
R-squared (R²): Represents the proportion of variance explained by the model.

Coefficients: Slopes for each independent variable.

p-values: Statistical significance of coefficients.

F-statistic: Overall model significance.
