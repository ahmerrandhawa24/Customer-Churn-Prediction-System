# Customer Churn Prediction

## Overview
This project predicts customer churn for a telecom company using the Telco Customer Churn dataset.  
Customer churn is when a customer leaves a company’s service. Predicting churn helps companies proactively retain high-risk customers and reduce revenue loss.

This project demonstrates a full **end-to-end machine learning workflow**, including:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model training and evaluation
- Feature importance analysis

All experiments were conducted in Python using **pandas, NumPy, scikit-learn, XGBoost, and LightGBM**.

---

## Dataset

We used the **Telco Customer Churn dataset**, which contains 7,043 customers with the following types of features:

- Customer demographics (gender, senior citizen, partner, dependents)
- Service subscription details (phone, internet, online security, tech support, streaming)
- Account information (tenure, contract type, payment method, monthly charges, total charges)
- Churn status (target variable: Yes/No)

Dataset source: [Kaggle – Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)

---

## Steps Performed

### 1. Data Cleaning
- Removed missing values and corrected data types
- Converted categorical variables into numerical using **one-hot encoding**
- Removed irrelevant columns (like `customerID`) for modeling

### 2. Exploratory Data Analysis (EDA)
- Examined churn distribution
- Analyzed relationships between key features and churn
- Created plots for `tenure`, `monthly charges`, and `contract type`

### 3. Feature Engineering
- Created derived features where necessary
- Scaled numerical features for models that require it
- Encoded categorical features

### 4. Model Training
We trained and evaluated the following models:

1. **Logistic Regression**
2. **Random Forest**
3. **XGBoost**
4. **LightGBM**

Train-test split: 80% training, 20% testing.  
Evaluation metrics:

- Accuracy
- ROC-AUC
- Precision, Recall, F1-score for churn

**Results:**

| Model                  | Accuracy | ROC-AUC | Precision (Churn) | Recall (Churn) | F1 (Churn) |
|------------------------|----------|---------|------------------|----------------|------------|
| Logistic Regression    | 0.7989   | 0.8337  | 0.6417           | 0.5508         | 0.5928     |
| Random Forest          | 0.7896   | 0.8192  | 0.6283           | 0.5107         | 0.5634     |
| XGBoost                | 0.7846   | 0.8322  | 0.6079           | 0.5348         | 0.5690     |
| LightGBM               | 0.7726   | 0.8191  | 0.5804           | 0.5214         | 0.5493     |

> Logistic Regression performed the best in terms of overall accuracy and ROC-AUC.

### 5. Feature Importance
- Identified the most important factors contributing to churn:
  - `Contract type`  
  - `Monthly Charges`  
  - `Tenure`  
  - `Tech Support`  
  - `Online Security`
- This information is useful for business decisions to reduce churn.

### 6. Churn Probability
- Instead of predicting only Yes/No, we also obtained **churn probabilities** for each customer.
- Example: `Customer churn probability: 0.71` → 71% chance to leave.

---

## Libraries Used
- pandas
- numpy
- scikit-learn
- xgboost
- lightgbm
- matplotlib / seaborn (for EDA)

---

## Usage
1. Clone the repository  
2. Open the Jupyter/Colab notebook  
3. Run each cell in order:  
   - Data cleaning & preprocessing  
   - EDA  
   - Feature engineering  
   - Model training & evaluation  
   - Feature importance analysis  
   - Churn probability calculation  

> No API or external input is required. The predictions are based on the existing dataset.

---

## Conclusion
This project demonstrates a complete workflow for **predicting customer churn**:

- Helps companies identify at-risk customers
- Shows which features influence churn the most
- Provides probability-based predictions for better decision-making

This project is **industry-relevant**, as customer churn is a major business problem in telecom and subscription-based services.

---

## Author
**Ahmer Randhawa**  
Artificial Intelligence Enthusiast & Data Science Learner
