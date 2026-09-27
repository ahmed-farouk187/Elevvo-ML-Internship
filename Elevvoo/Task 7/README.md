# Task 7 - Sales Forecasting

In this task I forecasted the weekly sales of 45 Walmart stores using time-based features and regression models.

Dataset: Walmart Sales Forecast from Kaggle (Aslan Ahmedov)
https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast

Files used: train.csv, features.csv and stores.csv

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the three files and checked the data
- Added up all departments to get the total weekly sales of each store, and joined the store information and weekly features (temperature, fuel price, CPI, unemployment)
- Plotted total sales over time, sales in holiday weeks and sales by store type
- Created time-based features: year, month, week number, last week's sales (Lag_1), sales in the same week last year (Lag_52) and a 4-week rolling average
- Split the data by date: trained on data up to March 2012 and tested on April to October 2012
- Trained Linear Regression and Random Forest and compared them with a naive forecast (last week's sales)
- Plotted actual vs predicted sales over time and the feature importance

## Results

- Naive forecast: MAE $58,628, MAPE 5.55%
- Linear Regression: MAE $54,186, MAPE 5.92%
- Random Forest: MAE $44,961, MAPE 4.34%

Random Forest was the best model. The most important feature was the sales in the same week last year. Both models missed the sales spikes around Easter and the 4th of July, because those holidays are not marked in the data.

## How to run

Download train.csv, features.csv and stores.csv from the Kaggle link above, put them in the same folder as the notebook (or upload them in Colab), and run all the cells.
