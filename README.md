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

- Gradient Boosting Regressor

- XGBoost Regressor

- Support Vector Regressor (SVR)

Each model was trained using the processed data and optimized using hyperparameter tuning where applicable.

##

## Model Evaluation Metrics:

To ensure fair comparison and performance benchmarking, the following metrics were used:

- Mean Absolute Error (MAE)

- Mean Squared Error (MSE)

- Root Mean Squared Error (RMSE)

- R² Score (Coefficient of Determination)

These metrics helped assess not just accuracy but also the robustness and error magnitude of predictions.

##

## Results & Insights:

Among all the models tested, ensemble methods like Random Forest and XGBoost showed superior performance, capturing non-linear relationships and interactions between variables effectively. Linear models, while interpretable, underperformed on accuracy due to the complexity of the dataset.

##

## Key insights:

- Properties with features like **air conditioning**, **proximity to main roads**, more **bathrooms**, and preferred **locations** tended to have higher **prices**.

- Categorical features such as **furnishing status** and presence of **basement/guestroom** had significant influence on the model’s predictions.

##

## Conclusion:

This project showcases the use of machine learning in solving real-world regression problems in real estate. By comparing various algorithms, it demonstrates the trade-offs between model interpretability and predictive power. The final model can be deployed to assist stakeholders in estimating property prices more reliably than traditional heuristics.
