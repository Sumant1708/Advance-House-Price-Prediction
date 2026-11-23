# Advanced House Price Prediction

A machine learning regression project based on Kaggle's **House Prices: Advanced Regression Techniques** competition. The objective is to predict residential property sale prices by analyzing numerical and categorical housing features.

## Project Overview

This project explores different regression techniques, statistical analysis, feature engineering, and model optimization to develop an effective house price prediction model.

The primary focus is on understanding how feature characteristics, multicollinearity, regularization, and hyperparameter tuning influence regression performance.

## Key Features

- **Exploratory Data Analysis:** Statistical analysis, correlation analysis, distribution visualization, and missing-value assessment.
- **Data Cleaning:** Missing-value imputation, removal of irrelevant features, and outlier treatment using the Interquartile Range (IQR) method.
- **Feature Engineering:** Log transformation of the target variable, categorical encoding, and numerical feature scaling.
- **Multicollinearity Analysis:** Correlation matrix and Variance Inflation Factor (VIF).
- **Model Development:** Implementation and comparison of multiple regression algorithms.
- **Hyperparameter Optimization:** GridSearchCV, RandomizedSearchCV, and cross-validation.

## Machine Learning Models

The following regression algorithms were implemented and evaluated:

| Model | Technique |
|---|---|
| Linear Regression | Baseline Regression |
| Ridge Regression | L2 Regularization |
| Lasso Regression | L1 Regularization |
| ElasticNet | Combined L1 and L2 Regularization |
| Decision Tree | Tree-based Regression |
| Random Forest | Ensemble Learning |
| Gradient Boosting | Boosting |
| XGBoost | Extreme Gradient Boosting |
| CatBoost | Gradient Boosting with Categorical Feature Support |

## Model Evaluation

Models were evaluated using the following metrics:

- **MAE (Mean Absolute Error):** Measures the average absolute prediction error.
- **MSE (Mean Squared Error):** Penalizes larger prediction errors more heavily.
- **RMSE (Root Mean Squared Error):** Measures prediction error while emphasizing larger deviations.
- **R² Score:** Measures the proportion of variance explained by the model.

Five-fold cross-validation was also used to assess model generalization.

## Hyperparameter Tuning

Hyperparameter optimization was performed using:

- GridSearchCV
- RandomizedSearchCV
- RidgeCV
- LassoCV
- ElasticNetCV

Learning curves were also analyzed to understand model performance across different training dataset sizes.

## Final Model

LassoCV was used for generating the final Kaggle test-set predictions and submission file.

The target variable was log-transformed during training, and predictions were converted back to the original price scale using `numpy.expm1()`.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- CatBoost
- Statsmodels
- KaggleHub
- Jupyter Notebook

## Dataset

**Kaggle Competition:** [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

The dataset contains residential property characteristics, including:
- Overall quality and condition
- Living area and lot dimensions
- Garage and basement features
- Year built and remodeled
- Neighborhood and building type
- Sale price (target variable)

## Project Structure

```text
Advanced-House-Price-Prediction/
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebook.ipynb
├── submission.csv
├── requirements.txt
└── README.md
```

## Installation and Usage

1. Clone the repository:

```bash
git clone https://github.com/Sumant1708/Advanced-House-Price-Prediction.git
```

2. Navigate to the project directory:

```bash
cd Advanced-House-Price-Prediction
```

3. Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn statsmodels xgboost catboost kagglehub python-dotenv jupyter
```

4. Launch Jupyter Notebook:

```bash
jupyter notebook
```

5. Open the notebook and execute the cells sequentially.

**Dataset Access:** The notebook attempts to download the competition dataset through KaggleHub. Alternatively, place `train.csv` inside the `data/` directory. Kaggle API access may require competition access and authentication.

## Project Objective

The project aims to strengthen practical understanding of regression modeling, feature engineering, regularization, statistical diagnostics, ensemble methods, and model selection through a real-world housing price prediction problem.
