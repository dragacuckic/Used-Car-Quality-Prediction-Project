Project Overview

This project aims to develop a predictive model to assist Carvana, an online used car retailer, in making informed purchasing decisions at auctions.
The primary objective is to minimize the risk of acquiring faulty vehicles by predicting the quality of used cars based on historical data.
By implementing this model, Carvana can ensure that they are offering the best possible options to their customers, reducing potential costs associated with faulty vehicle acquisitions.

Dataset
Source: The dataset was sourced from Kaggle.
Size: The dataset contains 72,983 instances and 32 independent variables.
Target Variable: The output variable is binary, where 0 indicates a good purchase, and 1 indicates a bad purchase.
Imbalance: The data is highly imbalanced, with 64,007 instances labeled as good purchases and 8,976 instances as bad purchases.
Data Preprocessing
Handling Missing Data:

Missing values were handled using imputation techniques. The most frequent values were used to fill missing categorical data, while the median was used for numerical data.
Data Transformation:

String data was converted to numerical values using one-hot encoding.
Temporal features such as years were transformed into timestamps and further broken down into "Years," "Months," and "Quarters."
Feature Engineering:

A new feature, AcquisitionToRetailPriceRatio, was created to represent the ratio between the average retail price and the auction purchase price.
Cars were categorized by age and condition, enhancing the model's ability to predict quality.
Visualization
Various visualizations were created to gain better insights into the data, including:

Average Vehicle Acquisition Price
Distribution of Vehicle Prices
Machine Learning Models
Three machine learning algorithms were applied to the processed data:

k-Nearest Neighbors (k-NN):

Precision: 80%
Recall: 86%
F1-Score: 82%
Accuracy: 86%
Naive Bayes:

Precision: 92%
Recall: 86%
F1-Score: 88%
Accuracy: 86%
Random Forest:

Precision: 89%
Recall: 89%
F1-Score: 85%
Accuracy: 89%
Based on the evaluation metrics, Random Forest proved to be the most effective algorithm for this dataset.

Data Normalization
To improve the model's performance, data normalization was applied using the MinMaxScaler, which scaled the data to a range of 0 to 1. This step was crucial for algorithms like k-NN, which rely on distance calculations.

Feature Selection
Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) were used to reduce the dimensionality of the data while preserving the most critical features for model performance.

Testing on New Data
The models were tested on new data to evaluate their generalization ability. Random Forest continued to outperform the other algorithms, maintaining high precision, recall, and accuracy.
