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
## Output

                            OLS Regression Results                            
==============================================================================
Dep. Variable:                 Height   R-squared:                       0.736
Model:                            OLS   Adj. R-squared:                  0.670
Method:                 Least Squares   F-statistic:                     12.5
Date:                YYYY-MM-DD HH:MM   Prob (F-statistic):           0.0023
==============================================================================
                 coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------
const        156.4700      5.340     29.280      0.000     145.460     167.480
Weight        17.2982      4.890      3.536      0.002       7.400      27.196
==============================================================================
