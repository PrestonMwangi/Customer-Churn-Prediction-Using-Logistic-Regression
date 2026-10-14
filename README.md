# Telco Customer Churn Prediction Using Logistic Regression

## Project Overview

Customer churn is a major challenge for telecommunications companies. When customers discontinue their subscriptions, businesses lose recurring revenue and may incur additional costs to acquire replacement customers.

This project uses **Logistic Regression, a supervised machine learning classification algorithm**, to predict whether a telecommunications customer is likely to leave the company.

The objective is to identify customers at risk of churning so that the business can prioritize retention campaigns, investigate customer dissatisfaction, and make better data-driven decisions.

## Business Problem

Telecommunications companies need to identify customers who are likely to discontinue their services before they leave.

Rather than treating every customer equally, a predictive model can help a retention team focus its efforts on customers who are more likely to churn.

**Key business question:**

Which customers are most likely to churn, and how can the company use these predictions to improve customer retention?

## Project Objectives

- Explore customer demographics, subscription services, contract types, and billing information.
- Clean and prepare the dataset for machine learning.
- Train a Logistic Regression model to predict customer churn.
- Evaluate the model using classification metrics.
- Examine the trade-off between identifying churners and incorrectly flagging customers who would stay.
- Demonstrate how predictive analytics can support customer retention strategies.

## Dataset

The project uses the Telco Customer Churn dataset, stored as:

`WA_Fn-UseC_-Telco-Customer-Churn.csv`

The dataset contains customer information, including:

- **Demographics:** Gender, senior citizen status, partner, and dependents.
- **Services:** Phone service, internet service, online security, and streaming services.
- **Account information:** Tenure, contract type, payment method, and paperless billing.
- **Billing:** Monthly charges, total charges, and related customer account information.
- **Target variable:** `Churn`, indicating whether a customer left the company.

The target variable is encoded as:

- `Yes` → `1` (customer churned)
- `No` → `0` (customer stayed)

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Data Loading and Exploration

Loaded the dataset using Pandas and examined its structure, data types, missing values, and distribution of the target variable.

Exploratory data analysis helps establish the characteristics of customers who churn and identify patterns that may be useful for prediction.

### 2. Data Cleaning

The preprocessing workflow included:

- Removing `customerID` because it is an identifier rather than a useful predictive feature.
- Converting `TotalCharges` to a numeric data type.
- Handling blank or invalid `TotalCharges` values by removing affected records.
- Preparing categorical and numerical features for model training.

### 3. Feature Engineering and Encoding

Categorical variables were converted into numerical representations using one-hot encoding.

The target variable, `Churn`, was mapped to binary values, making the problem suitable for binary classification.

### 4. Train-Test Split

The dataset was divided into training and testing sets using an 80/20 split.

A stratified split was applied to preserve the approximate churn-to-non-churn distribution in both sets.

The split used `random_state=42` for reproducibility.

### 5. Feature Scaling

Feature standardization was applied to prepare numerical features for Logistic Regression.

The scaler was fitted on the training data and then applied to the test data to avoid information leakage.

These recommendations are potential applications of the model; their actual impact would need to be tested using business data.


## Limitations

- Logistic Regression may not capture complex nonlinear relationships between customer characteristics and churn.
- Predictions depend on the quality and representativeness of the dataset.
- The classification threshold involves a trade-off between recall and precision.
- Predicting churn does not establish why a customer leaves or prove that a retention offer will change their decision.
- Model performance should be monitored over time as customer behavior and business conditions change.

## Future Improvements

Potential extensions include:

- Comparing Logistic Regression with Decision Trees, Random Forest, and Gradient Boosting.
- Evaluating the model using a confusion matrix and ROC curve.
- Calculating ROC-AUC from the model's predicted probabilities.
- Tuning the classification threshold using retention costs and expected business value.
- Building an interactive Streamlit application to score customer churn risk.
- Deploying the model with a clear interface for exploring customer-level predictions.

## Conclusion

This project demonstrates how machine learning can support customer retention by identifying telecommunications customers who are more likely to churn.

The model achieved a reported churn recall of 0.76 at a threshold of 0.30, showing its potential to identify a substantial proportion of customers who leave. Its precision of 0.51 also highlights the need to balance customer coverage against the cost of unnecessary retention interventions.

The central lesson is that a useful classification model should not be judged by accuracy alone. Its threshold, evaluation metrics, and business application should align with the decisions the organization needs to make.

## Author

**Timothy Kamau**

Data Analytics | Python | SQL | Business Intelligence | Machine Learning

This project demonstrates practical application of data preparation, classification, model evaluation, and business-focused analytical thinking.
