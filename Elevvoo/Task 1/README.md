# Task 1 - Student Score Prediction

In this task I built a linear regression model to predict students' exam scores based on how many hours they study.

Dataset: Student Performance Factors from Kaggle
https://www.kaggle.com/datasets/lainguyn123/student-performance-factors

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the data and checked its size, column types and statistics
- Cleaned the data (filled missing values in 3 columns and removed one row with a score of 101)
- Plotted the exam scores and the relationship between hours studied and score
- Split the data into 80% training and 20% testing
- Trained a linear regression model using hours studied
- Evaluated it with MAE, RMSE and R2 and plotted the predictions
- Bonus: tried polynomial regression and different feature combinations

## Results

Model: score = 0.286 * hours + 61.55

MAE = 2.42, RMSE = 3.16, R2 = 0.247

Polynomial regression didn't improve the results.

Adding more features helped a lot:

- Hours only: R2 = 0.247
- Adding attendance: R2 = 0.622
- Adding previous scores: R2 = 0.655
- Adding tutoring: R2 = 0.681
- Adding sleep: R2 = 0.681 (no change)

Attendance made the biggest difference, and sleep didn't help at all.

## How to run

Download the CSV from Kaggle, put it in the same folder as the notebook (or upload it in Colab), and run all the cells.
