# Car Price Prediction

## Project Overview

This project demonstrates machine learning techniques to predict used car prices using real-world car listings data. Accurate car price prediction helps buyers and sellers make informed decisions in online marketplaces.

We implement and compare three regression models—Linear Regression, Ridge Regression (L2 regularization), and Lasso Regression (L1 regularization)—for continuous price prediction.

## Dataset

- *Source:* Real-world car listings dataset with 9,374 entries and 30+ features per listing.
- *Features:* Includes numerical features (Year, Mileage, Engine specs, Ratings) and categorical features (Make, Model, Transmission, Drivetrain, FuelType, State, etc.).
- *Target:*  
  - Continuous price (in USD) for regression models.  
- *Preprocessing:*  
  - Cleaned and converted price column from string to numeric.  
  - Consolidated categorical variables and reduced cardinality (e.g., grouping rare car models).  
  - Extracted engine displacement and cylinders from engine descriptions.  
  - One-hot encoding applied for categorical features.  
  - Standard scaling applied to numeric features.

## Methodology

- Data split into 80% training and 20% test sets.
- Three regression models trained and evaluated using R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).
- Multinomial Logistic Regression trained on price buckets and evaluated using accuracy, precision, recall, and F1-score.
- Exploratory data analysis guided feature selection and engineering.

## Results

- Regression models achieved approximately 72–73% explained variance (R²) with average MAE around $4,200.
- Regularization (L1 and L2) did not significantly improve performance over the baseline linear regression.
- Key predictors include Year, Mileage, Make/Model, and Engine characteristics.

## Future Work

- Incorporate advanced models such as Random Forests or Gradient Boosted Trees for non-linear relationships.
- Enrich dataset with vehicle condition, trim levels, and market factors.
- Perform hyperparameter tuning for better generalization.
- Deploy models in a web application for real-time price estimation.

## Requirements

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn

Install dependencies via:

```bash
pip install -r requirements.txt
