# Linear and Multiple Regression Analysis

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This repository provides a practical implementation and exploration of linear and regularized regression models. The project demonstrates how to build, train, and evaluate Simple Linear Regression, Multiple Linear Regression, and advanced regularized models like **Ridge**, **Lasso**, and **ElasticNet**.

The primary goal is to predict a continuous target variable based on one or more independent features. We leverage **`scikit-learn` Pipelines** to create a robust and reproducible workflow, and analyze the relationships between variables through statistical modeling and visualization.

## 📋 Table of Contents
- [Concepts Covered](#-concepts-covered)
- [Dataset](#-dataset)
- [Visualizations](#-visualizations)
- [Methodology](#-methodology)
- [Model Evaluation & Comparison](#-model-evaluation--comparison)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [License](#-license)

## ✨ Concepts Covered
- **Simple Linear Regression (OLS):** Modeling the relationship between a single independent variable and a dependent variable.
- **Multiple Linear Regression:** Extending linear regression to model the relationship with two or more independent variables.
- **Regularized Regression:** Using advanced models to prevent overfitting and improve generalization on unseen data.
  - **Ridge (L2 Regularization):** Adds a penalty proportional to the square of the magnitude of coefficients. Effective at handling multicollinearity.
  - **Lasso (L1 Regularization):** Adds a penalty proportional to the absolute value of coefficients. Can shrink unimportant feature coefficients to exactly zero, performing automatic feature selection.
  - **ElasticNet:** A hybrid model that combines both L1 and L2 penalties, offering a balance between Ridge and Lasso.
- **Scikit-Learn Pipelines:** Streamlining preprocessing (e.g., feature scaling) and modeling into a single, robust workflow to prevent data leakage.
- **Data Preprocessing & Splitting:** Preparing the dataset and splitting it into training and testing sets.
- **Model Training & Prediction:** Fitting models to training data and making predictions on test data.
- **Data Visualization:** Using `matplotlib` and `seaborn` for insightful plots to understand data and model performance.

## 💾 Dataset
This project uses the classic **"Advertising" dataset**, which contains information on product sales figures based on advertising spend in different media channels.
-   **Features (Independent Variables):** `TV`, `Radio`, `Newspaper` advertising spend.
-   **Target (Dependent Variable):** `Sales`.

The analysis explores how these features contribute to the final sales predictions and which models provide the most accurate results.

## 📊 Visualizations
Visualizations are key to understanding the data's underlying structure and the performance of our models.

### Scatter Plot
A simple scatter plot helps visualize the relationship between a single feature and the target variable. It's the first step in determining if a linear relationship might exist.

![Scatter Plot of Feature vs Target](assets/scatter_plot.png)

### Regression Plot
Seaborn's `regplot` combines a scatter plot with a fitted OLS regression line and a 95% confidence interval. This provides a clear view of the linear relationship.

![Regression Plot](assets/regplot.png)

### Pairplot
For multiple linear regression, a `pairplot` is incredibly useful. It creates a grid of scatter plots for each pair of variables, allowing for a quick overview of pairwise relationships and the distribution of each variable.

![Pairplot of all variables](assets/pairplot.png)

### Residuals Plot
A residuals plot is a crucial diagnostic tool. It plots the difference between the actual values and the predicted values (the residuals) against the predicted values. A good model will have residuals randomly scattered around zero with no clear pattern.

![Residuals Plot](assets/residuals_plot.png)

## ⚙️ Methodology
The project follows these key steps:
1.  **Data Loading and Inspection:** Load the dataset using Pandas and perform an initial analysis (`.info()`, `.describe()`, `.head()`).
2.  **Exploratory Data Analysis (EDA):** Create visualizations (like those above) to understand variable distributions and relationships.
3.  **Feature Selection:** Choose the independent variables (X) and the dependent variable (y).
4.  **Train-Test Split:** Divide the data into training and testing sets to evaluate the model on unseen data.
5.  **Model Building with Pipelines:** A `scikit-learn` **Pipeline** is constructed to chain preprocessing steps (e.g., `StandardScaler`) with a regression model. This ensures that scaling is only learned from the training data, preventing data leakage.
6.  **Model Instantiation and Training:** Create and train pipelines for various regression models:
    -   `LinearRegression` (as a baseline)
    -   `Ridge`
    -   `Lasso`
    -   `ElasticNet`
7.  **Prediction:** Use the trained pipelines to make predictions on the test set.
8.  **Evaluation and Comparison:** Assess and compare the performance of each model using key regression metrics.

## 📈 Model Evaluation & Comparison
The performance of each trained model is evaluated using standard regression metrics. This allows for a direct comparison to determine which model generalizes best to the test data.

- **Mean Absolute Error (MAE):** The average of the absolute differences between predicted and actual values. It's easy to interpret as it's in the same units as the target variable.
- **Mean Squared Error (MSE):** The average of the squared differences between predicted and actual values. It penalizes larger errors more heavily.
- **Root Mean Squared Error (RMSE):** The square root of the MSE. It's also in the same units as the target variable and is a popular metric.
- **R-squared (R²):** The coefficient of determination. It represents the proportion of the variance in the dependent variable that is predictable from the independent variables. A value closer to 1 indicates a better fit.

By comparing these metrics across the Linear, Ridge, Lasso, and ElasticNet models, we can select the one that offers the best predictive performance for this dataset.

## 🚀 Getting Started
Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites
You will need Python 3.x and Pip installed on your system.

### Installation
1.  Clone the repository to your local machine:
    ```sh
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  (Recommended) Create and activate a virtual environment to keep dependencies isolated:
    ```sh
    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # For Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  Install the required packages from `requirements.txt`:
    ```sh
    pip install -r requirements.txt
    ```
    If you do not have a `requirements.txt` file, you can create one with the following content:
    ```txt
    # requirements.txt
    pandas
    numpy
    scikit-learn
    matplotlib
    seaborn
    jupyterlab
    ```

## 💻 Usage
The core analysis and model implementation are contained within a Jupyter Notebook (`.ipynb`). To run the project:

1.  Make sure your virtual environment is activated and you have installed the required packages.
2.  Start Jupyter Lab:
    ```sh
    jupyter lab
    ```
3.  Open the main notebook file and run the cells sequentially to see the data loading, EDA, model training, and evaluation steps.

## ⚖️ License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.
