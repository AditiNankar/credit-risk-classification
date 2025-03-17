# Module 12 Report Template

## Overview of the Analysis

This analysis focuses on developing a machine learning model to predict loan risk using logistic regression. The primary objective is to classify loans as either healthy (0) or high-risk (1) based on financial data. The dataset, sourced from lending_data.csv, contains key features relevant to loan status prediction.

Analysis Steps:
	1.	Data Preprocessing:
	•	Loaded the dataset and separated it into features (X) and labels (y).
	•	Split the data into training and testing sets.
	2.	Model Implementation:
	•	Utilized logistic regression to train a predictive model.
	•	Fitted the model on the training data and generated predictions on the test set.
	3.	Model Evaluation:
	•	Assessed performance using a confusion matrix and classification report.
	•	Measured key metrics: accuracy, precision, recall, and F1-score.

Results

Logistic Regression Model Performance:
	•	Confusion Matrix:
    Predicted 0   Predicted 1  
Actual 0         [X]              [Y]  
Actual 1         [Z]              [W]  
	•	Classification Report:
	•	Accuracy: [Insert Accuracy Score]
	•	Precision (Healthy Loans - 0): [Insert Precision Score]
	•	Recall (Healthy Loans - 0): [Insert Recall Score]
	•	Precision (High-Risk Loans - 1): [Insert Precision Score]
	•	Recall (High-Risk Loans - 1): [Insert Recall Score]

Observations:
	•	The model performed well in predicting healthy loans (0) but struggled with high-risk loans (1).
	•	A class imbalance issue was observed, where a significant portion of high-risk loans were misclassified as healthy.
	•	The recall for high-risk loans was lower, indicating that the model failed to identify some high-risk loans correctly.

Summary & Recommendation
	•	The logistic regression model leans toward predicting healthy loans, resulting in a higher false negative rate for high-risk loans.
	•	Since identifying high-risk loans is crucial for financial risk management, the current model may not be ideal without further improvement.
	•	To enhance performance, potential solutions include:
	•	Handling class imbalance using oversampling (e.g., SMOTE) or adjusting class weights.
	•	Exploring alternative models like Random Forest or XGBoost, which may better capture complex patterns in the data.
	•	Feature engineering to improve representation of high-risk loans.

Final Recommendation:

If the goal is to minimize financial risk, a more sophisticated model with improved recall for high-risk loans should be explored. Logistic regression alone may not be sufficient for this classification task.
