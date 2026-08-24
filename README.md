# Bike Sharing Demand Prediction

## Project Overview

This project uses the UCI Bike Sharing Dataset to predict the total number of bike rentals (`cnt`) using machine learning regression models.

The project focuses on understanding how temporal, environmental, and weather-related factors are associated with bike rental demand and building a predictive model based on these features.

## Dataset

The project uses the hourly bike sharing dataset containing 17,379 observations.

The target variable is:

* `cnt` — total number of bike rentals

The dataset includes temporal features such as hour, month, weekday, and year, as well as weather and environmental features such as temperature, humidity, and windspeed.

## Project Workflow

1. Problem Definition
2. Data Loading
3. Dataset Understanding
4. Exploratory Data Analysis
5. Feature Selection
6. Feature Engineering
7. Preprocessing
8. Train/Test Split
9. Baseline Model
10. Regression Models
11. Cross-Validation
12. Hyperparameter Tuning
13. Feature Importance
14. Final Model Selection
15. Business Insights

## Models

The following regression models were evaluated:

* Baseline
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor

Random Forest and Gradient Boosting were also tuned using GridSearchCV.

## Model Performance

| Model                   |    MAE |   RMSE |     R² |
| ----------------------- | -----: | -----: | -----: |
| Baseline                | 140.08 | 178.03 | -0.001 |
| Decision Tree           |  40.06 |  66.29 |  0.861 |
| Random Forest           |  29.80 |  47.87 |  0.928 |
| Gradient Boosting       |  58.00 |  79.90 |  0.798 |
| Tuned Random Forest     |  29.57 |  47.45 |  0.929 |
| Tuned Gradient Boosting |  46.85 |  66.37 |  0.861 |

## Final Model

The Tuned Random Forest model was selected as the final model.

### Final Test Performance

* **MAE:** 29.57
* **RMSE:** 47.45
* **R²:** 0.929

The tuned Random Forest achieved the strongest overall performance on the final test set.

## Key Insights

### Time and Working Day

Hour was the most important predictive feature. Rental demand varies substantially throughout the day, and demand patterns differ between working and non-working days.

### Season and Weather

Bike rental demand varies across seasons. In the analyzed data, demand was highest in Season 3 and lowest in Season 1. Poorer weather conditions were also associated with lower average rental demand.

### Temperature and Humidity

Temperature showed a generally positive but non-linear relationship with rental demand. Humidity had a less straightforward relationship but still contributed to the final model's predictions.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
Bike Sharing Demand Prediction/
│
├── datasets/
│   └── hour.csv
│
├── notebooks/
│   └── bike_sharing_demand_prediction.ipynb
│
├── README.md
└── .gitignore
```
