# 🏦 Credit Risk Classification

## 📘 Overview

This project uses machine learning to assess the **credit risk** of borrowers using historical loan data. The goal is to build and evaluate a **logistic regression model** that predicts whether a loan is likely to be healthy or at high risk of default.

Peer-to-peer lending platforms can use this type of model to make informed lending decisions, minimize default rates, and improve profitability by identifying risky borrowers ahead of time.

---

## 🔍 Data Source

The dataset, `lending_data.csv`, contains anonymized records of lending activity. Each record includes financial attributes of the borrower along with a **binary target column (`loan_status`)**:
- `0` → Healthy Loan  
- `1` → High-Risk Loan

---

## ✅ Steps Performed

### 1. Data Preparation
- Loaded `lending_data.csv` into a Pandas DataFrame
- Defined `X` (features) and `y` (labels)
- Split data into training and testing sets using `train_test_split`

### 2. Model Building
- Trained a **logistic regression** model using `LogisticRegression` from scikit-learn
- Generated predictions on the testing set

### 3. Model Evaluation
- Evaluated the model using:
  - **Confusion Matrix**
  - **Classification Report** (Precision, Recall, F1-Score)
  - **Accuracy Score**

---

## 📊 Model Performance

- **Accuracy Score**: `0.93`
- **Precision Score**:
  - Class 0 (Healthy Loans): `1.00`
  - Class 1 (High-Risk Loans): `0.84`
- **Recall Score**:
  - Class 0: `0.99`
  - Class 1: `0.94`

---

## 🧠 Summary & Recommendation

### Summary:
- The model performs **very well** in identifying healthy loans (class 0), with high precision and recall.
- It shows **moderate performance** for detecting high-risk loans (class 1), with good precision (few false positives), but lower recall (some high-risk loans are missed).

### Recommendation:
While the model is suitable for identifying healthy loans, the **low recall for high-risk loans** presents a concern. In finance, failing to catch risky loans could result in losses. Therefore, we **do not fully recommend** this model for production use without:
- Further tuning (e.g., adjusting class weights or threshold)
- Experimenting with more advanced models like Random Forest, XGBoost, or SMOTE for imbalanced data

---

## 👩‍💻 Author

Aditi Nankar
