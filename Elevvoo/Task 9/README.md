# Task 9 - Industrial Predictive Maintenance

In this task I built a classifier that predicts machine failures from sensor readings. The main goal was to keep false alarms as low as possible, because a false alarm stops production for nothing.

Dataset: AI4I 2020 Predictive Maintenance Dataset by Stephan Matzka
https://www.kaggle.com/datasets/stephanmatzka/predictive-maintenance-dataset-ai4i-2020
(also on UCI: https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset)

Libraries used: pandas, numpy, matplotlib, scikit-learn, xgboost

## What I did

- Loaded the data and checked it (10,000 rows, no missing values or duplicates, only 3.4% failures)
- Removed the ID columns and the five failure type columns (TWF, HDF, PWF, OSF, RNF) because they would leak the answer
- Created three new features: temperature difference, power and tool wear x torque
- Split the data into 80% training and 20% testing (stratified)
- Trained Random Forest and XGBoost and compared them using precision, recall and the False Discovery Rate (FDR)
- Tuned the decision threshold to reduce false alarms
- Bonus: checked which sensor is most related to failure using feature importance and correlation

## Results

With the default threshold (0.5):

- Random Forest: FDR 0.034 (2 false alarms), recall 0.824
- XGBoost: FDR 0.070 (4 false alarms), recall 0.779

With the threshold raised to 0.7, the Random Forest raised only 1 false alarm (FDR 0.019) with 99.1% accuracy, but missed a few more failures.

The engineered features Wear_x_torque and Power were the most important. Torque was the sensor most correlated with failure.

## How to run

Download ai4i2020.csv from the link above, put it in the same folder as the notebook (or upload it in Colab), and run all the cells.
