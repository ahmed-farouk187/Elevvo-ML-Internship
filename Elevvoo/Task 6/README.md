# Task 6 - Music Genre Classification

In this task I classified songs into 10 music genres using audio features extracted from the songs (tabular approach).

Dataset: GTZAN Dataset - Music Genre Classification from Kaggle (Andrada Olteanu)
https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification

File used: features_30_sec.csv (1,000 songs of 30 seconds, 100 per genre, 57 audio features)

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the audio features and checked the data (no missing values or duplicates, 100 songs per genre)
- Removed the filename and length columns and encoded the genres as numbers
- Split the data into 80% training and 20% testing (stratified) and scaled the features
- Trained and compared Random Forest, SVM and KNN
- Looked at the results per genre and the confusion matrix of the best model

## Results

- SVM: accuracy 76.5%, macro F1 0.764
- Random Forest: accuracy 71.0%, macro F1 0.702
- KNN: accuracy 67.0%, macro F1 0.669

SVM was the best model. Metal and country were the easiest genres to predict, and disco was the hardest. Most mistakes were between genres that sound similar, like metal and blues or pop and reggae.

## How to run

Download features_30_sec.csv from the Kaggle link above (it is in the Data folder), put it in the same folder as the notebook (or upload it in Colab), and run all the cells.
