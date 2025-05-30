🎯 Project Objective
The aim of this project is to build a predictive model that identifies customers at risk of churning. 

📝 Background
In the highly competitive telecommunications sector, retaining existing customers is more cost-effective than acquiring new ones. This project leverages machine learning techniques to analyze customer data and predict potential churners. The IBM Telco Customer Churn dataset serves as the foundation for this analysis.
GitHub

📂 Dataset Overview
The dataset comprises various customer attributes:

Demographics: Gender, Senior Citizen status

Account Information: Tenure, Contract Type, Payment Method

Service Usage: Internet Service Type, Phone Service, Additional Features

Billing Details: Monthly Charges, Total Charges

The dataset exhibits class imbalance:
No Churn: 73.46%
Churn: 26.54%
Class Weighting: Applied to penalize misclassification of minority class.

🤖 Machine Learning Models
Four models were developed and evaluated:

Logistic Regression

Random Forest

XGBoost

LightGBM

Each model was trained using both class weighting and SMOTE techniques to handle class imbalance.

📊 Model Performance Comparison
Model	Technique	Accuracy	Precision	Recall	F1 Score	ROC AUC	Cross-Val ROC AUC
Logistic Regression	Class Weight	0.7587	0.5282	0.8284	0.6451	0.8650	0.8426
Logistic Regression	SMOTE	0.7892	0.6484	0.4450	0.5278	0.7927	0.9327
Random Forest	Class Weight	0.7921	0.6460	0.4745	0.5471	0.8369	0.8266
XGBoost	Class Weight	0.7991	0.6415	0.5469	0.5904	0.8375	0.8138
LightGBM	Class Weight	0.7743	0.5516	0.7882	0.6490	0.8554	0.8308
LightGBM	SMOTE	0.8105	0.6506	0.6139	0.6317	0.8548	0.9377

The LightGBM model with SMOTE outperformed others across multiple metrics.

🔍 Feature Importance (LightGBM)
Top 15 features influencing churn prediction:

Monthly Charges

Total Charges

Total Charges per Tenure

Tenure

Monthly Charges per Tenure

Electronic Check Payment Method

Gender

No Online Backup

Credit Card (Automatic) Payment Method

Bank Transfer (Automatic) Payment Method

No Tech Support

No Online Security

One-Year Contract

Partner Status

Paperless Billing

📈 Key Insights
Financial Factors: Monthly and total charges, along with tenure, are significant churn predictors.

Payment Methods: Customers using electronic checks show higher churn rates.

Service Engagement: Lack of services like Online Backup, Tech Support, and Online Security correlates with increased churn.

Contract Type: One-year contracts are associated with higher retention.

<img src="path/to/image" alt="Alt text" width="400"/>

