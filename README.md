# Movie_Recomdation_System

![img1](https://github.com/user-attachments/assets/ebcfa395-b407-4e66-b500-eedfe7f03e1e)

## Overview:
This report outlines the development of a Movie Recommendation System utilizing user-based collaborative filtering and item-based similarity calculations using Pearson correlation. The system aims to predict movie recommendations based on user input, leveraging a dataset comprising user ratings and movie metadata.

## Objectives:
The main objectives of this project are:
  1. To implement a collaborative filtering technique that recommends movies based on user preferences.
  2. To calculate item-based similarity using Pearson correlation.
  3. To provide a user-friendly interface that allows users to obtain movie recommendations based on the movies they have watched.

## Data Collection:
The project utilizes two primary datasets:
* Ratings Dataset: Contains user ratings for movies, including user IDs, movie IDs, and ratings.
* Movies Metadata Dataset: Contains metadata for movies, including movie IDs, titles, and genres.

Link : https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/

## Data Cleaning and Transformation:
The following steps were taken to clean and prepare the datasets for analysis:

1. **Loading the Datasets:** The datasets were loaded into a data processing tool.
2. **Selecting Relevant Columns:** From the movies metadata, only essential columns (movie ID, title, and genres) were retained. The timestamp column from the ratings dataset was dropped for simplicity.
3. **Handling Missing Values:** The datasets were checked for any missing values to ensure data integrity and completeness.
4. **Column Renaming and Type Consistency:** The `id` column in the movies dataset was renamed to `movieId` to align with the ratings dataset, and both datasets had their `movieId` columns converted to a consistent data type.
5. **Duplicate Checks:** The movies dataset was scanned for duplicate entries to maintain a clean and accurate dataset.
6. **Merging Datasets:** The cleaned ratings and movies datasets were merged on the movieId column, creating a comprehensive dataset for further analysis.

## Calculate Item-Based Similarity Using Pearson Correlation:
### User-Movie Ratings Matrix
A user-movie ratings matrix was created, representing users as rows and movies as columns, with ratings as the values. Missing ratings were filled with zeros to facilitate similarity calculations.
### Similarity Calculation
An item similarity matrix was computed using Pearson correlation to quantify the similarity between movies based on user ratings. This matrix serves as the foundation for generating movie recommendations.

## Recommendation Engine:
The recommendation system is designed to provide personalized movie recommendations based on user input. The main functionalities include:
1. **Retrieving Movie ID:** The system checks if the user-input movie title exists in the dataset and retrieves the corresponding movie ID.
2.**Checking Similarity:** The system ensures that the retrieved movie ID exists in the item similarity matrix before proceeding.
3. **Calculating Similar Movies:** Using the item similarity matrix, the system identifies movies that are similar to the input movie, sorting them by their similarity scores.
4. **Visualizing Similarity Scores:** The correlation scores for the recommended movies are visualized through a bar plot, enhancing user understanding of the recommendations.
5. **Returning Recommendations:** The system generates and presents a list of recommended movie titles to the user.

## User Interaction:
The system prompts users to input the title of a movie they have watched. If the movie exists in the dataset, the system generates a list of recommended movies. In cases where the movie title is not found, the user is advised to check the title and try again.

## Conclusion:
The Movie Recommendation System successfully implements user-based collaborative filtering and item-based similarity calculations using Pearson correlation. It provides personalized movie recommendations based on user input while also visualizing the correlation scores for clarity.
