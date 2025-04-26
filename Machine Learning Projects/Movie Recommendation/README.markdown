# Movie Recommendation System using Python and Machine Learning

## Overview
This project builds a movie recommendation system using Python and machine learning techniques. It provides personalized movie suggestions based on a user’s preferences by analyzing movie metadata such as cast, crew, keywords, and genres. The system employs a content-based filtering approach to recommend movies similar to a given title.

## Purpose
The purpose of this project is to create a recommendation engine that suggests movies to users based on metadata similarities. It mimics the functionality of recommendation systems used by platforms like Netflix or Amazon, helping users discover movies they might enjoy.

## Dataset
- The dataset comprises two CSV files: `credits.csv` and `movies.csv`.
- `credits.csv` includes metadata such as cast and crew details.
- `movies.csv` contains information like movie ID, title, budget, and genres.
- Key features used for recommendations: `cast`, `crew`, `keywords`, and `genres`.
- Download the dataset from [this link](#) (replace with the actual link if available).

## Tools and Libraries
To run this project, you’ll need the following:
- **Python 3.x**: The core programming language.
- **Pandas 1.2.4**: For data manipulation and analysis.
- **Scikit-learn 0.24.1**: For vectorization and similarity computation.

Install the required libraries with this command:
```bash
pip install pandas scikit-learn
```

## Steps to Build the Movie Recommendation System

### 1. Exploratory Data Analysis (EDA)
- **Load the Data**: Import `credits.csv` and `movies.csv` using Pandas.
- **Merge DataFrames**: Combine the datasets on the `id` column to form a unified DataFrame.
- **Select Columns**: Use relevant columns: `id`, `title`, `cast`, `crew`, `keywords`, and `genres`.

### 2. Build the Recommendation System
- **Preprocess Metadata**:
  - Convert stringified lists in `cast`, `crew`, `keywords`, and `genres` to Python lists using `literal_eval`.
  - Extract the director’s name from the `crew` column.
  - Limit `cast`, `keywords`, and `genres` to the top 3 elements.
  - Clean data by converting text to lowercase and removing spaces (e.g., "Johnny Depp" becomes "johnnydepp").
- **Create a "Soup"**:
  - Combine `keywords`, `cast`, `director`, and `genres` into a single string (the "soup") for each movie.
- **Vectorize the Text**:
  - Use `CountVectorizer` to transform the "soup" into a numerical matrix, excluding English stopwords.
- **Calculate Similarity**:
  - Compute cosine similarity scores between movies based on the vectorized data.
- **Map Titles to Indices**:
  - Create a reverse mapping of movie titles to their DataFrame indices for efficient lookup.

### 3. Get Recommendations
- **Recommendation Function**:
  - The `get_recommendations` function accepts a movie title and cosine similarity matrix as inputs.
  - It retrieves the movie’s index, computes similarity scores with all other movies, sorts them, and returns the top 10 similar movie titles (excluding the input movie).

## How to Use the Code
1. **Download the Dataset**: Place `credits.csv` and `movies.csv` in your project directory.
2. **Install Libraries**: Run the installation command provided above.
3. **Run the Script**: Execute the Python script to process the data and build the recommendation system.
4. **Get Recommendations**: Call the `get_recommendations` function with a movie title.

### Example
```python
print(get_recommendations("The Dark Knight Rises", cosine_sim2))
```
Possible output:
- The Dark Knight
- Batman Begins
- The Prestige
- Inception
- (and other similar movies)

## Summary
This project offers a practical introduction to building a content-based movie recommendation system. By leveraging movie metadata and machine learning, it delivers tailored suggestions, serving as an excellent foundation for exploring recommendation engines.