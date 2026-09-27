# Task 4 - Loan Approval Prediction

In this task I built classification models to predict whether a loan application will be approved or rejected.

Dataset: Loan-Approval-Prediction-Dataset from Kaggle
https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the data and removed the extra spaces in the column names and text values
- Checked the data (4,269 rows, no missing values or duplicates)
- Found 28 negative residential asset values, treated them as missing and filled them with the median
- Plotted the CIBIL score for approved and rejected loans, and the rejection rate by education and self-employment
- Encoded the text columns as 0 and 1 (Rejected = 1)
- Split the data into 80% training and 20% testing (stratified)
- Trained Logistic Regression and a Decision Tree and compared them using precision, recall, F1 and confusion matrices

## Results

The data is imbalanced (62% approved, 38% rejected), so I looked at precision, recall and F1 for the Rejected class.

- Logistic Regression: precision 0.919, recall 0.876, F1 0.897
- Decision Tree: precision 0.972, recall 0.950, F1 0.961

The Decision Tree was better. It wrongly approved 16 loans that should have been rejected, compared to 40 for Logistic Regression.

The CIBIL score was the most important factor: almost all applications with a score below about 550 were rejected. Education and self-employment made almost no difference.

## How to run

Download loan_approval_dataset.csv from Kaggle, put it in the same folder as the notebook (or upload it in Colab), and run all the cells.
