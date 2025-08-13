# Credit Scoring Model

The goal of this project is to build a predictive model for a bank to improve lending decisions and, by extension, enhance corporate financial performance. This model utilizes several machine learning classifiers to assess creditworthiness based on customer data.

## Problem Statement

Banks and financial institutions face the constant challenge of accurately predicting loan repayment. Inaccurate assessments can lead to financial losses from defaults or missed opportunities with reliable borrowers. The objective of this project is to develop a more effective and data-driven approach to credit scoring that goes beyond traditional methods.

## Solution Overview

This project provides a solution by leveraging machine learning to predict the likelihood of a client defaulting. The project's methodology is as follows:

* **Data Cleaning and Preprocessing**: The initial data was thoroughly cleaned and preprocessed. Missing values were handled, and categorical features were encoded to a numerical format suitable for machine learning algorithms.
* **Feature Engineering**: To improve the model's predictive power, new features were created from the raw data. These include INCOME_PER_FAMILY (income per family member) and EMPLOYMENT_TO_AGE_RATIO (ratio of years employed to age), which provide a richer understanding of a client's financial situation.
* **Target Variable Definition**: The target variable (TARGET) was carefully defined. A client was labeled as "good" (0) only if they had no credit or their payments were always on time. Clients with any history of overdue payments were labeled as "bad" (1).
* **Data Scaling**: To balance the influence of different features, numerical data was scaled. This process, known as Standard Scaling, transforms features like AMT_INCOME_TOTAL and CNT_FAM_MEMBERS to have a mean of 0 and a standard deviation of 1. This prevents features with large values from dominating the model's training process.
* **Model Training and Evaluation**: Several classifiers were trained and evaluated to identify the best-performing model. The following models were used:
    * Logistic Regression: A baseline model for binary classification.
    * Random Forest Classifier: An ensemble model known for its high accuracy.
    * Gradient Boosting Classifier: An advanced ensemble method that builds models sequentially to correct errors.

## Key Findings and Results

After training and evaluation, the Random Forest Classifier showed the best overall performance, particularly in distinguishing between good and bad clients, as indicated by its high ROC-AUC score.

* **Random Forest Classifier**:
    * Accuracy: 0.8276
    * ROC-AUC: 0.7670
* **Gradient Boosting Classifier**:
    * Accuracy: 0.8781
    * ROC-AUC: 0.6236
* **Logistic Regression**:
    * Accuracy: 0.4841
    * ROC-AUC: 0.5017

The Random Forest model's strong performance makes it the recommended choice for this credit scoring task.

## Author

Sergey Nikitin
