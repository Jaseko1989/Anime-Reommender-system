# Anime Recommender System

## Project Overview
This project is an end-to-end implementation of an anime recommender system. The goal is to predict user ratings for unseen anime titles based on historical preferences. The project includes data loading, preprocessing, model training, evaluation, and final deployment.

## Dataset
The dataset includes the following files:
- `anime.csv`: Contains information about anime titles.
- `train.csv`: Contains user ratings for anime titles.
- `test.csv`: Contains user and anime pairs for which ratings need to be predicted.
- `submission.csv`: Illustrates the expected format for the final predictions.

## Detailed File Descriptions
### `anime.csv`
- `anime_id`: Unique ID identifying an anime.
- `name`: Full name of the anime.
- `genre`: Comma-separated list of genres for this anime.
- `type`: Movie, TV, OVA, etc.
- `episodes`: Number of episodes in the series (1 if a movie).
- `rating`: Average rating out of 10 for this anime.
- `members`: Number of community members in this anime's group.

### `train.csv`
- `user_id`: Randomly generated user ID.
- `anime_id`: The anime that this user has rated.
- `rating`: Rating out of 10 this user has assigned (or -1 if the user watched it but didn't assign a rating).

### `test.csv`
- `user_id`: Randomly generated user ID.
- `anime_id`: The anime that this user has rated.

### `submission.csv`
- `ID`: A concatenation of `user_id` and `anime_id` given in the test file (using an `_` character).
- `rating`: The predicted rating for a given user-anime pair.

## Project Workflow
1. **Data Loading**: Load the provided datasets.
2. **Data Preprocessing**: Handle missing values, encode categorical features, and vectorize descriptions.
3. **Model Training**: Build collaborative filtering (using SVD) and content-based filtering models.
4. **Model Evaluation**: Evaluate the collaborative filtering model using RMSE.
5. **Generating Predictions**: Generate rating predictions for the test set.
6. **Deployment**: Deploy the model using Flask to expose a recommendation API.
# Project Files
'anime_recommender.ipynb': Jupyter notebook containing the full implementation.
'anime.csv': Dataset file with anime information.
'train.csv': Dataset file with user ratings.
'test.csv': Dataset file for generating predictions.
'submission.csv': Example submission format.
# Conclusion
This project demonstrates an end-to-end workflow for building, evaluating, and deploying a recommender system for anime titles. By leveraging both collaborative filtering and content-based filtering techniques, we aim to provide accurate and personalized recommendations for users.



