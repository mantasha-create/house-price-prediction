# House Price Prediction Using Machine Learning

## Overview
#### This project aims to predict house prices using machine learning techniques, leveraging the Boston House Price Dataset. The problem is a regression task since the target variable, median house price (MEDV), is a continuous value.

## Dataset Information
Source: The dataset is from the UCI Machine Learning Repository.
Size: 506 rows and 14 columns.
Features:
Input Features (13): CRIM, ZN, INDUS, CHAS, NOX, RM, AGE, DIS, RAD, TAX, PTRATIO, B, LSTAT.
Target Variable (1): MEDV (Median value of owner-occupied homes in $1000s).
Key Attributes:
Positive relationships (e.g., RM positively correlates with MEDV).
Negative relationships (e.g., LSTAT negatively correlates with MEDV).

## Workflow
Data Preprocessing:

Checked for missing values (house_price_dataset.isnull().sum()).
No missing values detected in the dataset, ensuring its readiness for analysis.
Data Analysis:

Conducted a correlation analysis with a heatmap to understand the relationships among features.

### Key observations:
RM (average number of rooms) has a strong positive correlation with MEDV.
LSTAT (% lower status population) shows a strong negative correlation with MEDV.

### Data Splitting:

Input features (X) and target variable (Y) separated.
Split dataset into training (80%) and testing (20%) subsets using train_test_split.

### Model Training:
Used XGBoost Regressor as the machine learning model.
The model was trained using the training dataset (X_train, Y_train).

### Model Evaluation:
Predictions were made on both training and testing datasets.
Metrics used:
Mean Absolute Error (MAE).
Mean Squared Error (MSE).
Root Mean Squared Error (RMSE).
Observations from predictions:
High accuracy on the training data, indicating the model effectively learns the patterns.
Results on test data indicate the model's potential generalization performance.

### Predictions:
The model performed well on both training and testing datasets.
Some overfitting may be present due to differences in errors between training and test data.
Key Factors Influencing House Prices:
RM (Average Rooms): Positively correlated with house prices. Larger houses tend to cost more.
LSTAT (% Lower Status Population): Negatively correlated with house prices. Areas with a higher proportion of lower-status populations tend to have lower house prices.


### Conclusion
The XGBoost Regressor proved to be an effective algorithm for predicting Boston house prices, offering reliable predictions based on input features. The model can be further fine-tuned to reduce overfitting and improve its generalization performance.
