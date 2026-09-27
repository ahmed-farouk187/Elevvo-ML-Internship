# Task 5 - Movie Recommendation System

In this task I built a movie recommendation system that recommends movies to a user based on what similar users liked (user-based collaborative filtering).

Dataset: MovieLens small dataset (ml-latest-small) from GroupLens, downloaded from Kaggle
https://www.kaggle.com/datasets/abhikjha/movielens-100k

Files used: ratings.csv and movies.csv

Libraries used: pandas, numpy, matplotlib, scikit-learn

## What I did

- Loaded the ratings and movie titles and checked the data (100,836 ratings, 610 users, 9,724 movies, no missing values)
- Plotted the distribution of ratings and checked how many movies each user rated
- Hid 20% of each user's ratings to use for testing
- Built a user-item matrix (users as rows, movies as columns)
- Computed cosine similarity between users
- Recommended the top 10 unseen movies for a user using their 30 most similar users
- Evaluated the recommendations with precision@10 and compared them with recommending the most popular movies
- Bonus: tried matrix factorisation with SVD (20 factors)

## Results

Precision@10 (599 users evaluated):

- Most popular movies: 0.122
- User-based collaborative filtering: 0.194
- SVD: 0.197

Both personalised methods did much better than the most popular baseline, and SVD was slightly better than user-based filtering.

## How to run

Download ratings.csv and movies.csv from the Kaggle link above, put them in the same folder as the notebook (or upload them in Colab), and run all the cells.
