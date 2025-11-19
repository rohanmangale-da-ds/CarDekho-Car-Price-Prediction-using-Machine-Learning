# CarDekho-Car-Price-Prediction-using-Machine-Learning

<img width="1536" height="1024" alt="ChatGPT Image Nov 18, 2025, 09_26_55 PM" src="https://github.com/user-attachments/assets/35141c59-7dac-4422-9470-c9dae6aec078" />

A complete end-to-end Machine Learning project to predict used-car selling prices using the CarDekho dataset. This project includes data cleaning, EDA, feature engineering, model building, hyperparameter tuning, model comparison, and business insights.


1. Project Overview

This project builds a machine learning system to estimate the selling price of used cars based on car characteristics such as manufacturing year, engine power, mileage, kilometers driven, and ownership details.
Multiple ML models were trained and compared to identify the most accurate, generalizable model for real-world price estimation.

2. Dataset Summary

The dataset contains structured car attributes, including:

year, selling_price, km_driven

fuel, seller_type, transmission, owner

mileage, engine, max_power, seats

Issues identified:
✔ Missing values in mileage, engine, power, seats
✔ Mixed units in numeric columns
✔ Many categorical variables requiring encoding

3. Data Cleaning & Preprocessing

Key steps:

Removed duplicates

Standardized numeric columns (converted strings → numeric)

Cleaned units from mileage, engine, max_power

Handled missing values using KNN Imputer

One-hot encoded categorical variables (drop_first=True to avoid dummy trap)

Feature engineering: created car age from the year column

Train–test split (80/20)

4. Models Trained

The following algorithms were evaluated:

Linear Regression

Lasso Regression

Random Forest Regressor

Gradient Boosting Regressor

KNN Regressor

Bagging Regressor

5. Model Performance
Model	Train R²	Test R²	MSE	MAE
Linear Regression	65.58	54.47	9.98e10	172232
Lasso	65.58	54.47	9.98e10	172230
Gradient Boosting	93.69	90.53	2.07e10	89545
Random Forest	98.47	91.89	1.77e10	74455
KNN	91.14	84.09	3.49e10	94257
Bagging	98.19	90.54	2.07e10	77722
Best Model: Random Forest Regressor

Highest Test R² (91.89%)

Lowest MSE & MAE

Strong generalization, least overfitting

6. Visual Insights
🔹 Predicted vs Actual Plots

All models were visualized with scatter plots against the perfect prediction line (y = x).
Random Forest showed the tightest clustering around the line → high prediction accuracy.

🔹 Feature Importance (Random Forest)

Top contributing features:

Max Power

Year (Car Age)

Kilometers Driven

Engine Capacity

Mileage

Categorical features (fuel, owner, seller_type) had very low influence.

7. Key Insights

Performance features drive price: max_power, engine size, car age strongly determine resale value.

Usage matters: Cars with lower km_driven command higher prices.

Fuel, owner type, seller type affect price minimally.

Random Forest is the most reliable algorithm for this type of structured pricing data.
