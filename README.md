# Credit-Card-Fraud-Prediction-System

Project Overview
This project is a machine learning system designed to detect fraudulent credit card transactions. By identifying anomalies or using supervised learning techniques, this system can effectively distinguish between legitimate and fraudulent transactions, helping financial institutions prevent losses.

Objectives
Detect Fraudulent Transactions: Utilize machine learning techniques to identify fraudulent transactions from anonymized credit card data.
Apply Supervised and Unsupervised Learning: Use algorithms like XGBoost for supervised learning and Isolation Forest for anomaly detection.

Optimize Model Performance: Tune hyperparameters to achieve high accuracy, precision, recall, and ROC-AUC scores.
Dataset
The dataset used in this project is the Credit Card Fraud Detection Dataset, which contains anonymized features for transactions, including:

Time: The time elapsed between the transaction and the first transaction.

Amount: The transaction amount.

Class: The target variable, where 1 indicates fraud and 0 indicates a legitimate transaction.
You can find the dataset on Kaggle at Credit Card Fraud Detection Dataset.

Project Workflow

1. Data Preprocessing
Handling Missing Values: Filled missing values with the mean of each column to ensure a complete dataset.
Scaling Features: Standardized Time and Amount columns to improve model performance.
Class Balancing: Used SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset, as fraud cases are rare.

2. Model Training and Tuning
Supervised Learning with XGBoost
GridSearchCV was used for hyperparameter tuning with parameters like:
n_estimators: Number of trees.
max_depth: Depth of each tree.
learning_rate: Learning rate for gradient boosting.
subsample and colsample_bytree: Fraction of samples and features used per tree.
Evaluation: Achieved high accuracy and ROC-AUC scores, with metrics indicating effective fraud detection.
Anomaly Detection with Isolation Forest
Applied Isolation Forest for unsupervised learning to detect outliers that could indicate fraud.
Evaluation: Isolation Forest underperformed compared to XGBoost due to dataset imbalance, indicating that supervised learning was more effective.

3. Model Evaluation
Confusion Matrix: Showed high accuracy in detecting both fraud and legitimate transactions with XGBoost.

ROC-AUC Score: Provided insight into model’s ability to distinguish between fraud and legitimate cases.

Precision-Recall Curve: Used to assess performance, particularly given the dataset’s imbalance.

Key Results
XGBoost achieved an accuracy of 99.87% and ROC-AUC score of 0.999, making it effective in fraud detection.
Isolation Forest was less effective, indicating supervised learning methods are preferable for this task.

Future Improvements

Explore additional unsupervised methods for fraud detection.
Experiment with ensemble methods combining XGBoost and anomaly detection for improved results.
Fine-tune the decision threshold to optimize for precision or recall, depending on specific needs.
