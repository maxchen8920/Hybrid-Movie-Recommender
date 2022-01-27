# Hybrid-Movie-Recommender

## Introduction
This movie recommender combines both collaborative filtering (user ratings) and content-based filtering (genres and tags) to produce a recommendation of 10 similar movies.
The dataset is the [MovieLens](https://grouplens.org/datasets/movielens/) ml-latest-small dataset with "100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users".

For collaborative filtering, I performed item-based collaborative filtering by applying Truncated SVD on an item-to-user rating matrix. This utilises past user ratings on movies to determine what other movies were rated highly by users who also rated a specific movie similarly.

For content-based filtering, I used cosine similarity to find similar movies based on their user-defined genres and tags.

This hybrid recommender combines the recommendations, and with a higher weighting on ratings and equal weightings for genres and tags.

## Results
As shown in the Jupyter notebook, the results appear to be good. The recommendations are very similar to the results when typing "similar movies to Toy Story" and "similar movies to The Usual Suspects" in the Google search engine, despite the notebook's use of a smaller and older dataset.

## Files
`recommendation.ipynb` - hybrid recommender system that can be run through 'get_hybrid_recommendations(movieId)'. <br>
`movies.csv` - dataset of 9000+ movies, with their IDs, titles and genres . <br>
`ratings.csv` - dataset of users and their ratings for movies. <br>
`tags.csv` - dataset of movies and their tags added by users.
