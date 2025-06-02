# Customer Churn Prediction Project

## Project Overview

Customer churn prediction is a critical task for businesses to identify customers who are likely to stop using their services. This project implements a machine learning pipeline to predict customer churn using real-world data. The goal is to enable companies to proactively engage at-risk customers and reduce churn, thereby improving customer retention and revenue.

---

## Dataset Description

The dataset used in this project contains detailed information about customers, including demographic details, account information, service usage metrics, and billing/payment data. The data is divided into training and testing subsets to build and validate the predictive model.

Typical features include:

- Customer demographics: Age, Gender, Geography
- Account details: Tenure, Contract type, Monthly charges, Total charges
- Service usage: Number of products/services subscribed, usage frequency
- Payment details: Payment method, billing frequency

---

## Data Preprocessing

Key preprocessing steps undertaken:

- Handling missing values and outliers
- Encoding categorical variables using One-Hot Encoding and Label Encoding where appropriate
- Feature scaling using StandardScaler/MinMaxScaler to normalize numerical features
- Feature engineering to create meaningful aggregated metrics and interaction terms
- Splitting data into training and testing sets with stratification to preserve class distribution

---

## Exploratory Data Analysis (EDA)

Performed EDA to understand data distribution and feature relationships:

- Visualized churn rate across different customer segments using bar plots and pie charts
- Analyzed correlation between features and target variable (churn)
- Identified important features using feature importance scores from tree-based models
- Checked class imbalance and employed techniques if necessary (e.g., SMOTE, undersampling)

---

## Modelling Approach

- Utilized **XGBoost** classifier for its efficiency and accuracy on tabular data.
- Hyperparameter tuning performed using GridSearchCV/RandomizedSearchCV to optimize model parameters.
- Evaluated model performance using multiple metrics:
  - Accuracy
  - Precision, Recall, F1-score
  - ROC-AUC score for classification threshold analysis

---

## Model Explainability

To build trust and transparency, this project integrates **LIME (Local Interpretable Model-Agnostic Explanations)**:

- Explains individual predictions by approximating the model locally with an interpretable model
- Helps identify the key features influencing the churn prediction for each customer instance
- Facilitates business stakeholders to understand actionable factors behind customer churn

---

## Results

- Achieved an accuracy of **XX%** (replace with your actual result).
- ROC-AUC score of **XX** indicating strong discriminative ability.
- LIME explanations showed features such as contract type, monthly charges, and tenure were significant drivers of churn predictions.

---

## Sample Output

### 📌 Confusion Matrix
![Confusion Matrix](images/confusion_matrix.png)

### 📌 ROC Curve
![ROC Curve](images/roc_curve.png)

### 📌 LIME Explanation
![LIME Explanation](images/lime_explanation.png)

---

## Technologies Used

- Python 3.x
- pandas, numpy
- scikit-learn
- XGBoost
- LIME
- matplotlib, seaborn for visualization
- Jupyter Notebook

## How to Use

- Clone this repository:
   ```bash
   git clone https://github.com/your-username/customer-churn-prediction.git
   cd customer-churn-prediction
- pip install -r requirements.txt
