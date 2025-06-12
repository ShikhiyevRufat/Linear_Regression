# Linear and Multiple Regression Analysis

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This repository provides a practical implementation and exploration of linear regression models. The project demonstrates how to build, train, and evaluate both Simple Linear Regression (using Ordinary Least Squares) and Multiple Linear Regression models.

The primary goal is to predict a continuous target variable based on one or more independent features, and to analyze the relationships between these variables through statistical modeling and visualization.

## 📋 Table of Contents
- [Concepts Covered](#-concepts-covered)
- [Dataset](#-dataset)
- [Visualizations](#-visualizations)
- [Methodology](#-methodology)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Model Evaluation](#-model-evaluation)
- [License](#-license)

## ✨ Concepts Covered
- **Simple Linear Regression (OLS):** Modeling the relationship between a single independent variable and a dependent variable.
- **Multiple Linear Regression:** Extending linear regression to model the relationship with two or more independent variables.
- **Data Preprocessing & Splitting:** Using `scikit-learn` to split the dataset into training and testing sets.
- **Model Training:** Fitting the regression models to the training data.
- **Model Prediction:** Making predictions on the test data.
- **Data Visualization:** Using `matplotlib` and `seaborn` for insightful plots to understand data and model performance.

## 💾 Dataset
This project uses a dataset to predict a target variable (e.g., `Sales`) based on one or more feature variables (e.g., `TV Advertising Spend`, `Radio Advertising Spend`). The analysis explores how these features contribute to the final prediction.

*(You can add more specific details about your dataset here. For example: "The dataset used is the 'Advertising' dataset, which contains information on sales figures based on advertising spend in different media.")*

## 📊 Visualizations
Visualizations are key to understanding the data's underlying structure and the performance of our models.

### Scatter Plot
A simple scatter plot helps visualize the relationship between a single feature and the target variable. It's the first step in determining if a linear relationship might exist.

![Scatter Plot of Feature vs Target](assets/scatter_plot.png)

### Regression Plot
Seaborn's `regplot` combines a scatter plot with a fitted OLS regression line and a 95% confidence interval. This provides a clear view of the linear relationship.

![Regression Plot](assets/regplot.png)

### Pairplot
For multiple linear regression, a `pairplot` is incredibly useful. It creates a grid of scatter plots for each pair of variables in the dataset, allowing for a quick overview of pairwise relationships and the distribution of each variable.

![Pairplot of all variables](assets/pairplot.png)

### Residuals Plot
A residuals plot is a crucial diagnostic tool. It plots the difference between the actual values and the predicted values (the residuals) against the predicted values. A good model will have residuals randomly scattered around zero.

![Residuals Plot](assets/residuals_plot.png)

## ⚙️ Methodology
The project follows these key steps:
1.  **Data Loading and Inspection:** Load the dataset using Pandas and perform an initial analysis (`.info()`, `.describe()`, `.head()`).
2.  **Exploratory Data Analysis (EDA):** Create visualizations (like those above) to understand variable distributions and relationships.
3.  **Feature Selection:** Choose the independent variables (X) and the dependent variable (y).
4.  **Train-Test Split:** Divide the data into training and testing sets to evaluate the model on unseen data.
5.  **Model Instantiation and Training:** Create an instance of the `LinearRegression` model from `scikit-learn` and fit it to the training data using the `.fit()` method.
6.  **Prediction:** Use the trained model to make predictions on the test set with the `.predict()` method.
7.  **Evaluation:** Assess the model's performance using key regression metrics.

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

2.  (Recommended) Create and activate a virtual environment:
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

If you don't have a `requirements.txt` file, you can create one with the following content:
```txt
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyterlab
