# House_Price_Prediction_MachineLearning

## Description
This project aims to build and compare multiple machine learning models to accurately predict house prices based on various features such as area, number of bedrooms and bathrooms, presence of amenities (e.g., guestroom, basement, hot water heating), location preferences, and furnishing status.


## Data Overview

- The dataset used for this project contains 545 records with 13 input features and 1 target variable — price. The features include both numerical (e.g., area, parking, number of stories) and categorical variables (e.g., furnishing status, presence of main road, air conditioning). These features are key indicators that influence real estate pricing.
- The target variable is price, and the features include:
> - Numerical: area, bedrooms, bathrooms, stories, parking
> - Categorical/Binary: mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishingstatus
-  Shape of Dataset is 545 x 13
 > <img width="1345" height="482" alt="image" src="https://github.com/user-attachments/assets/b84b168e-5bec-4cac-9f10-199549cae77d" />
##

## Data Preprocessing:

- **Data Cleaning :** Verified dataset integrity; handled any inconsistencies or missing values.

- **Feature Engineering :** Converted binary categorical features to 0/1; applied Label Encoding and pandas Dummies for multi-class variables like furnishingstatus.

- **Scaling :** Normalized numerical variables to ensure uniform contribution to the models.

- **Train-Test Split :** The dataset was split into training (80%) and testing (20%) sets to evaluate model generalization.

## Model Development & Algorithms Used:

**Several supervised regression models were trained and evaluated:**

- Linear Regression

- Decision Tree Regressor

- Random Forest Regressor

- KNeighbors Regressor

- XGBoost Regressor

- Support Vector Regressor (SVR)

Each model was trained using the processed data and optimized using hyperparameter tuning where applicable.

##

## Model Evaluation Metrics:

To ensure fair comparison and performance benchmarking, the following metrics were used:

- Mean Absolute Error (MAE)

- Root Mean Squared Error (RMSE)

- R² Score (Coefficient of Determination)

These metrics helped assess not just accuracy but also the robustness and error magnitude of predictions.

##

## Results & Insights:

  | ML Model                | R² Score   | MAE            | RMSE           |
  | ----------------------- | ---------- | -------------- | -------------- |
  | KNeighbors Regressor    | 0.5426     | 789,178.10     | 1,035,400.80   |
  | **Linear Regression**   | **0.6505** | 689,643.54     | **905,095.30** |
  | Random Forest Regressor | 0.6415     | 672,877.84     | 916,710.12     |
  | Decision Tree           | 0.1083     | 1,047,370.18   | 1,445,717.06   |
  | XGBoost Regressor       | 0.6503     | **649,028.78** | 905,366.44     |
  | SVR Regressor           | -0.0014    | 1,200,219.37   | 1,532,105.77   |


- **Best R² Score:** Linear Regression (0.6505) – explains the most variance in the data.

- **Lowest MAE:** XGBoost Regressor (649,028.78) – most accurate on average.

- **Lowest RMSE:** Linear Regression (905,095.30) – smallest average squared error.
##

***Linear Regression*** is the best overall model based on:

- Highest R² Score

- Lowest RMSE
- 2nd lowest MAE (just behind XGBoost)

If your priority is overall balanced accuracy and consistency, go with Linear Regression.
However, if minimizing average absolute error (MAE) is your top concern, XGBoost is very close in performance and slightly better on that metric.

##

## Key insights:

- Properties with features like **air conditioning**, **proximity to main roads**, more **bathrooms**, and preferred **locations** tended to have higher **prices**.

- Categorical features such as **furnishing status** and presence of **basement/guestroom** had significant influence on the model’s predictions.

##

## Conclusion:

This project showcases the use of machine learning in solving real-world regression problems in real estate. By comparing various algorithms, it demonstrates the trade-offs between model interpretability and predictive power. The final model can be deployed to assist stakeholders in estimating property prices more reliably than traditional heuristics.
