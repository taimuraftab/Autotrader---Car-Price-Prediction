### **Project Overview**

This project focuses on building a regression model to predict the selling price of used cars using a dataset provided by AutoTrader. The dataset includes various characteristics of the vehicles, and the goal is to develop a model capable of accurately forecasting the price of a car based on these features. Different regression algorithms were employed to find the most suitable approach for this task. The project aims to showcase the application of these models and evaluate their performance in predicting car prices from historical data.

## Dataset

This project uses a dataset with 402,005 car adverts from AutoTrader, featuring 12 columns that describe various vehicle characteristics such as make, model, mileage, and year of registration. The target variable is the **price**, representing the selling price of the car.

The dataset includes missing values, which were handled during preprocessing, and has been anonymized to protect car owners' identities.

## Data Processing

The data preprocessing involved several steps to prepare the dataset for modeling:

- **Missing Values**: Missing values were handled logically, using the mean or based on the frequency distribution of the columns.
- **Feature Engineering**: A new feature, **age of car**, was created by subtracting the year of registration from the current year.
- **Scaling**: Numerical features were scaled using **StandardScaler** to ensure uniformity across features.
- **Outlier Removal**: Outliers were detected and removed using the **Interquartile Range (IQR)** method.

## Model Performance

Three different regression models were trained and evaluated for predicting the selling price of used cars:

- **K-Nearest Neighbors (KNN) Regressor**: After performing hyperparameter tuning, the best **n_neighbors** value was found to be **11**. The model's performance is as follows:
  - **MSE**: 12,896,982.38
  - **RMSE**: 3,591.24
  - **R²**: 0.81

- **Decision Tree Regressor**: The best **max_depth** parameter was found to be **15**. The performance of the Decision Tree model is:
  - **MSE**: 14,806,067.41
  - **RMSE**: 3,847.87
  - **R²**: 0.78

- **Linear Regression**: This model showed the following performance:
  - **MSE**: 18,666,028.06
  - **RMSE**: 4,320.42
  - **R²**: 0.73

The **KNN Regressor** achieved the best performance among the three models, with the highest **R²** and lowest **MSE** and **RMSE** values.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/taimuraftab/Autotrader---Car-Price-Prediction.git
