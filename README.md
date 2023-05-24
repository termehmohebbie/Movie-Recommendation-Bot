# Movie Recommendation Chatbot

This Movie Recommendation Chatbot is a Python-based application that provides personalized movie recommendations based on user input. The chatbot utilizes a dataset of movies, applies machine learning techniques for analysis, and recommends similar movies to the user.

## Dataset

The dataset used for this project contains information about movies, including their titles, genres, overview, popularity, production countries, vote average, vote count, and ratings. The dataset is in CSV format and is named `combined_df_clean.csv`.

## Methodology

The chatbot employs the following methodology to recommend similar movies:

1. Data Preprocessing:
   - The movie dataset is loaded into a Pandas DataFrame.
   - Text preprocessing techniques are applied to the 'overview' column, including tokenization, lowercasing, removal of stopwords and punctuation, and lemmatization.
   - The 'genres' column is processed by extracting genre names from the list of dictionaries and transforming them into a single string.
   - The processed text data is stored in new columns for analysis.

2. Feature Extraction:
   - The TF-IDF vectorization technique is used to convert the processed 'overview' and 'genres' columns into numerical representations.
   - The vectorized data is combined with other relevant columns, including 'adult', 'original_language', 'popularity', 'production_countries', 'vote_average', 'vote_count', 'rating', and 'cluster_label', to form the feature matrix for analysis.

3. Clustering:
   - The K-means clustering algorithm is applied to group similar movies based on their features.
   - The optimal number of clusters is determined using techniques such as the elbow method or silhouette score.

4. Similarity Calculation:
   - For each user input, the chatbot identifies the movie's ID from the dataset using the movie title provided.
   - The movie's features are extracted from the dataset, and its cluster label is determined.
   - Movies in the same cluster as the input movie are considered similar.
   - Cosine similarity is calculated between the input movie and other movies in the same cluster to determine their similarity scores.

5. Movie Recommendation:
   - The top N movies with the highest similarity scores are recommended as similar movies to the user.
   - The recommended movies are displayed to the user as a list.
