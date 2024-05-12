# Book Recommender
A collaborative filtering model that can be used to recommend books based on a reader's ratings. This model is designed to be run with AWS' Sagemaker.

## Data Sources
The collaborative fitering model is trained on the Goodreads data from Kaggle.  
(source: https://www.kaggle.com/datasets/bahramjannesarr/goodreads-book-datasets-10m/data)

The source includes two types of data:
1. Book meta data (filename: book*.csv): Includes metadata elements including no of pages, publisher, language as well as distribution of ratings.
2. User ratings data (filename: user_rating_*.csv) : Ratings at a user id - book name level.

## Notebooks
Currently, the following functionality can be supported based on the code in the notebooks:
1. data_prep.ipynb: Convert the raw data into a form that can be used to train the model. Also includes some basic data cleaning.
2. collab_filtering.ipynb: Trains a fast ai/ pytorch based CF model. This model can later be scored to :
   * given a book, return the 5 most similar books
   * given a user's ratings, recoomend n number of books (yet to be implemented)
