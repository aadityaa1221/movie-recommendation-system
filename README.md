Content-Based Movie Recommendation System

Overview

This project is about a movie recommendation system that is based on the content of the movies. It uses Python to suggest movies to users by looking at how similar the moviesre in terms of things like genres, keywords, cast and crew.

This system does not look at what movies a user has watched. Instead it looks at the information about the movies themselves. Finds the ones that are most similar. It uses a way of looking at the words in the movie information called a Bag-of-Words approach and a measure called Cosine Similarity to find the closest matches.

Dataset

The project uses a dataset called the TMDB 5000 Movies and Credits dataset.

* tmdb_5000_movies.csv: This file has information about the movies, like genres, keywords and budget.

* tmdb_5000_credits.csv: This file has information about the cast and crew of the movies.

Methodology & Mathematical Intuition

The system follows a step-by-step process to turn the text information about the movies into numbers that can be used by a computer.

1. Data Preprocessing & Feature Engineering

First the system combines the two datasets into one. Then it extracts the information from the text like the names of the genres, keywords, cast and crew. It also removes any spaces from the names so that the computer can tell them apart.

Next it puts all the extracted information together into one list of tags for each movie.

2. Text Normalization

The system then uses an algorithm to reduce the words to their simplest form so that words like "action" and "actions" are treated the same. This helps the computer find the matches.

3. Vectorization (Bag of Words)

The system then turns the text information into numbers using a tool called CountVectorizer. It only looks at the 5,000 common words and ignores common words like "the" and "and".

Each movie is now represented as a list of numbers which's like a special code that the computer can understand.

4. Similarity Calculation

The system then calculates how similar each movie is to every movie using a measure called Cosine Similarity. This measure looks at the angle between the two lists of numbers. Gives a score between 0 and 1.

The score is calculated using a formula:

Similarity(A,B) = cos(θ) = (A ⋅ B) / (∥A∥ ∥B∥)

Where A and B are the lists of numbers for two movies. A score of 1 means the movies are identical and a score of 0 means they are completely different.

Tech. Libraries Utilized

This project uses the following tools:

* Python 3.x: This is the programming language used.

* Pandas & NumPy: These libraries are used to manipulate and clean the data.

* NLTK (Natural Language Toolkit): This library is used for text normalization.

* Scikit-Learn: This library is used for turning the text into numbers and calculating the similarity, between movies.
