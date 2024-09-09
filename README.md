# Books Recommendation System

## Description

This project implements a book recommendation system using two approaches:
1. **Popularity-Based Recommendation System**: Recommends books based on their popularity.
2. **Collaborative Filtering-Based Recommendation System**: Recommends books based on user ratings and similarities between books.

## Features

- **Popularity-Based Recommendations**: Recommends books that have a high number of ratings and high average ratings.
- **Collaborative Filtering-Based Recommendations**: Uses cosine similarity to recommend books similar to a given book based on user ratings.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Mahad-Saffi/Books-Recommendation-System.git
    ```

## Usage

1. **Popularity-Based Recommendation System**:
    - The system merges the `books` and `ratings` datasets.
    - It calculates the number of ratings and the average rating for each book.
    - Books with a number of ratings above a specified threshold are considered.
    - The books are sorted based on their average rating in descending order.

2. **Collaborative Filtering-Based Recommendation System**:
    - Identifies reliable users who have given a significant number of ratings.
    - Filters books based on the number of ratings they have received.
    - Creates a pivot table representing the ratings given by reliable users for each book.
    - Calculates cosine similarity between books based on user ratings.
    - Recommends books similar to a given book based on cosine similarity scores.

## Example

To recommend books similar to "A Case of Need":

```python
recommended_books = RecommendBooks("A Case of Need")
for book in recommended_books:
    print(book)
```

## Acknowledgements
 - The Datasets used in this project are sourced from [Book Recommendation System By Möbius](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
