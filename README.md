# Fraud Detection Using Machine Learning

## Overview

This project is a proof-of-concept system developed for a bank that aims to detect fraudulent transactions using machine learning techniques. The goal is to accurately predict whether a given transaction is fraudulent based on a provided dataset.

## Problem Statement

Financial fraud is a significant issue in the banking industry, costing institutions billions of dollars each year. The bank provided a dataset (`bs140513_032310.csv`, available on [Kaggle](https://www.kaggle.com/code/kartik2112/fraud-detection-banksim/input) containing information about approximately 600,000 transactions. The challenge is to develop a machine learning model that can predict whether a transaction is fraudulent with high accuracy, while maintaining a balance between detecting frauds and minimizing false positives for legitimate transactions.

## Project Structure

### 1. Data Preprocessing
   - **Data Cleaning**: Removed unnecessary columns and handled missing values.
   - **Feature Engineering**: Created new features like transaction frequency and average transaction amount per merchant.
   - **Label Encoding**: Converted categorical variables into numerical values.
   - **Class Imbalance Handling**: Used SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset.

### 2. Model Training
   - Trained multiple machine learning models including:
     - **Random Forest**
     - **XGBoost**
     - **Logistic Regression**
     - **K-Nearest Neighbors**
     - **Decision Tree**
     - **Naive Bayes**

### 3. Hyperparameter Tuning
   - Applied `GridSearchCV` to fine-tune model parameters for optimal performance.

### 4. Ensemble Learning
   - Combined the best-performing models using a `Voting Classifier` to create an ensemble model for improved robustness and accuracy.

### 5. Model Evaluation
   - Assessed model performance on both validation and test datasets using:
     - **Accuracy**
     - **F1-Score**
     - **Precision**
     - **Recall**
     - **Confusion Matrices**

## Dataset

The dataset used in this project contains the following features:

1. **customer**: Customer ID
2. **age**: Age of the customer
3. **gender**: Gender of the customer
4. **merchant**: ID of the merchant
5. **category**: Category of the transaction
6. **amount**: Amount of the transaction
7. **zipcodeOri**: Zipcode of the origin (removed during preprocessing)
8. **zipMerchant**: Zipcode of the merchant (removed during preprocessing)
9. **step**: Time step of the transaction
10. **fraud**: Binary label indicating if the transaction is fraudulent (`1`) or not (`0`)

## Results

The ensemble model demonstrated strong performance across both genuine and fraudulent transactions.

## Conclusion

This project demonstrates that machine learning can effectively be used to detect fraudulent transactions in financial datasets. By leveraging ensemble learning techniques, we were able to create a model that balances accuracy with precision and recall, making it a reliable tool for fraud detection in a banking environment.
