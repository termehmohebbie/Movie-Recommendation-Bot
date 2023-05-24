# Movie Recommendation Chatbot

The Movie Recommendation Chatbot is a Python-based application that provides personalized movie recommendations based on user input. It utilizes a dataset of movies obtained from the Kaggle platform. The dataset, titled "The Movies Dataset," is created by Rounak Banik and can be found at the following link: [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset).

## Dataset Overview

The Movies Dataset is a comprehensive collection of movie-related information, including details about movies, ratings, genres, production companies, and more. The dataset is sourced from various data providers and encompasses a wide range of movies from different genres, languages, and release years.

The dataset consists of multiple CSV files, providing information about movies, credits, ratings, and keywords. It includes attributes such as movie titles, genres, production countries, original language, overviews, popularity, vote average, vote count, and ratings.

## Methodology

The Movie Recommendation Chatbot employs the following methodology to provide movie recommendations:

1. Data Preprocessing: The dataset is preprocessed to extract relevant features and clean the data. Text columns, such as overviews and genres, undergo preprocessing steps such as tokenization, lowercasing, removal of stopwords and punctuation, and lemmatization.

2. Feature Extraction: The preprocessed text data is transformed into numerical representations using the TF-IDF (Term Frequency-Inverse Document Frequency) technique. This allows the chatbot to perform similarity calculations based on the movie features.

3. Clustering: The K-means clustering algorithm is applied to group similar movies based on their features. The optimal number of clusters is determined using techniques such as the elbow method or silhouette score. Each movie is assigned a cluster label.

4. Similarity Calculation: Cosine similarity is used to calculate similarity scores between the user's input movie and other movies in the same cluster. The higher the similarity score, the more similar the movies are considered to be.

5. Recommendation Generation: The chatbot recommends the top N movies with the highest similarity scores as similar movies to the user. The recommended movies are displayed based on the user's input movie.
