# Task 3 - Forest Cover Type Classification

In this task I predicted which of 7 types of forest cover grows on a patch of land, using features like elevation, slope, distance to water and roads, wilderness area and soil type.

Dataset: Covertype from the UCI Machine Learning Repository
https://archive.ics.uci.edu/dataset/31/covertype

The notebook loads the UCI file covtype.data. The file has no column names, so they are added in the code.

Libraries used: pandas, numpy, matplotlib, scikit-learn, xgboost

## What I did

- Loaded the data and checked it (581,012 rows, 54 features, no missing values or duplicates)
- Checked the one-hot encoded wilderness area and soil type columns
- Plotted the number of patches per tree type and the elevation of each tree type
- Split the data into 80% training and 20% testing (stratified)
- Trained a Random Forest and evaluated it with a classification report and a confusion matrix
- Plotted the feature importance
- Bonus: trained XGBoost and compared it with Random Forest

## Results

- Random Forest: accuracy 95.3%, macro F1 0.924
- XGBoost: accuracy 96.6%, macro F1 0.941

XGBoost was better, especially for the rare tree types. Aspen recall went from 0.77 with Random Forest to 0.88 with XGBoost.

Most mistakes were between trees that grow in similar places, for example Aspen being predicted as Lodgepole Pine.

Elevation was the most important feature, followed by the distances to roads, fire points and water.

## How to run

Download covtype.data from the UCI link above, put it in the same folder as the notebook (or upload it in Colab) and run all the cells. Training takes a few minutes.
