# Automated Dataset Analysis

# Dataset Analysis Summary

## Overview of the Dataset

The dataset consists of a collection of 10,000 entries related to books, comprising 23 columns with various attributes. The data appear to include key information such as book IDs, authors, reviews, ratings, and publication details. Each column's data type is diverse, including both numerical (e.g., ratings counts, average ratings) and categorical (e.g., authors, language codes) types. Notably, the dataset contains no missing values, ensuring that all entries are complete for analysis.

### Summary of Key Attributes:

- **Identifiers**: ID fields (e.g., `book_id`, `goodreads_book_id`, `best_book_id`, `work_id`) are formatted as float numbers to uniquely identify each book.
- **Book Metadata**:
  - **Authors**: Categorical data represent book authors.
  - **Titles**: Original titles and translations, both included in the dataset.
  - **ISBNs**: Uniquely identify books, with both ISBN and ISBN13 included.
  - **Publication Year**: Indicates the year the book was originally published, with a range of publication years observed.
  
- **Ratings and Reviews**:
  - **Average Rating**: Ranges from 2.47 to 4.82, indicating overall positive sentiment towards the books.
  - **Ratings Count**: The number of reviews and ratings per book averages over 54,000, suggesting considerable engagement with the titles.

### Column Data Types

- Numerical: `float64` for numeric identifiers, ratings, and counts; `object` for categorical data such as titles and authors.

## Key Findings

### Descriptive Statistics
- The average rating of books is approximately 4.00, with a standard deviation of 0.25. This indicates that most books are well-received, suggesting high quality across the dataset.
- The `original_publication_year` ranges from -1750 to 2017, with a mean year around 1982. This indicates that the dataset captures a wide range of book publications, from historical to contemporary literature.
- There is significant variation in `ratings_count`, showing engagement levels varying across books: while mean ratings suggest popularity, the maximum count (over 4.78 million) implies some books have amassed a considerable following.

### Clustering Analysis
- The clustering analysis reveals three distinct clusters based on the inertia value of **94,298.16**

## Summary of Dataset
```
{'total_rows': 10000, 'total_columns': 23, 'column_types': {'book_id': 'float64', 'goodreads_book_id': 'float64', 'best_book_id': 'float64', 'work_id': 'float64', 'books_count': 'float64', 'isbn': 'object', 'isbn13': 'float64', 'authors': 'object', 'original_publication_year': 'float64', 'original_title': 'object', 'title': 'object', 'language_code': 'object', 'average_rating': 'float64', 'ratings_count': 'float64', 'work_ratings_count': 'float64', 'work_text_reviews_count': 'float64', 'ratings_1': 'float64', 'ratings_2': 'float64', 'ratings_3': 'float64', 'ratings_4': 'float64', 'ratings_5': 'float64', 'image_url': 'object', 'small_image_url': 'object'}, 'missing_values': {'book_id': 0, 'goodreads_book_id': 0, 'best_book_id': 0, 'work_id': 0, 'books_count': 0, 'isbn': 0, 'isbn13': 0, 'authors': 0, 'original_publication_year': 0, 'original_title': 0, 'title': 0, 'language_code': 0, 'average_rating': 0, 'ratings_count': 0, 'work_ratings_count': 0, 'work_text_reviews_count': 0, 'ratings_1': 0, 'ratings_2': 0, 'ratings_3': 0, 'ratings_4': 0, 'ratings_5': 0, 'image_url': 0, 'small_image_url': 0}, 'numeric_summary': {'book_id': {'count': 10000.0, 'mean': 5000.5, 'std': 2886.8956799071675, 'min': 1.0, '25%': 2500.75, '50%': 5000.5, '75%': 7500.25, 'max': 10000.0}, 'goodreads_book_id': {'count': 10000.0, 'mean': 5264696.5132, 'std': 7575461.863589611, 'min': 1.0, '25%': 46275.75, '50%': 394965.5, '75%': 9382225.25, 'max': 33288638.0}, 'best_book_id': {'count': 10000.0, 'mean': 5471213.5801, 'std': 7827329.890719961, 'min': 1.0, '25%': 47911.75, '50%': 425123.5, '75%': 9636112.5, 'max': 35534230.0}, 'work_id': {'count': 10000.0, 'mean': 8646183.4246, 'std': 11751060.824080039, 'min': 87.0, '25%': 1008841.0, '50%': 2719524.5, '75%': 14517748.25, 'max': 56399597.0}, 'books_count': {'count': 10000.0, 'mean': 75.7127, 'std': 170.47072765025834, 'min': 1.0, '25%': 23.0, '50%': 40.0, '75%': 67.0, 'max': 3455.0}, 'isbn13': {'count': 10000.0, 'mean': 9756530621824.22, 'std': 429753045646.84436, 'min': 195170342.0, '25%': 9780330413197.5, '50%': 9780451528640.0, '75%': 9780807760637.5, 'max': 9790007672390.0}, 'original_publication_year': {'count': 10000.0, 'mean': 1982.0339, 'std': 152.41969074566023, 'min': -1750.0, '25%': 1990.0, '50%': 2004.0, '75%': 2011.0, 'max': 2017.0}, 'average_rating': {'count': 10000.0, 'mean': 4.002191000000001, 'std': 0.25442748053872905, 'min': 2.47, '25%': 3.85, '50%': 4.02, '75%': 4.18, 'max': 4.82}, 'ratings_count': {'count': 10000.0, 'mean': 54001.2351, 'std': 157369.95643554674, 'min': 2716.0, '25%': 13568.75, '50%': 21155.5, '75%': 41053.5, 'max': 4780653.0}, 'work_ratings_count': {'count': 10000.0, 'mean': 59687.3216, 'std': 167803.7852374182, 'min': 5510.0, '25%': 15438.75, '50%': 23832.5, '75%': 45915.0, 'max': 4942365.0}, 'work_text_reviews_count': {'count': 10000.0, 'mean': 2919.9553, 'std': 6124.378131569911, 'min': 3.0, '25%': 694.0, '50%': 1402.0, '75%': 2744.25, 'max': 155254.0}, 'ratings_1': {'count': 10000.0, 'mean': 1345.0406, 'std': 6635.626262783459, 'min': 11.0, '25%': 196.0, '50%': 391.0, '75%': 885.0, 'max': 456191.0}, 'ratings_2': {'count': 10000.0, 'mean': 3110.885, 'std': 9717.123578396993, 'min': 30.0, '25%': 656.0, '50%': 1163.0, '75%': 2353.25, 'max': 436802.0}, 'ratings_3': {'count': 10000.0, 'mean': 11475.8938, 'std': 28546.449183182456, 'min': 323.0, '25%': 3112.0, '50%': 4894.0, '75%': 9287.0, 'max': 793319.0}, 'ratings_4': {'count': 10000.0, 'mean': 19965.6966, 'std': 51447.35838380058, 'min': 750.0, '25%': 5405.75, '50%': 8269.5, '75%': 16023.5, 'max': 1481305.0}, 'ratings_5': {'count': 10000.0, 'mean': 23789.8056, 'std': 79768.88561077163, 'min': 754.0, '25%': 5334.0, '50%': 8836.0, '75%': 17304.5, 'max': 3011543.0}}}
```

## Clustering Analysis Results
```
{'inertia': 94298.16420923788, 'cluster_centers': [[0.19107257470099037, 1.5173153404883848, 1.4949433846839424, 1.4174677191722305, -0.25181053045874513, -0.09776414830605418, 0.19916566338164787, -0.03772053327748799, -0.13569191983594156, -0.12315099289382045, 0.14568699104847335, -0.07612007636653811, -0.11142547688526719, -0.14299738699530323, -0.12317134820991314, -0.10854426579153323], [-0.0468256908135604, -0.5187785107810665, -0.5114347235915099, -0.48557737669212314, 0.05564296077329143, 0.03310788265092409, -0.0654603218275349, 0.011051686800375935, -0.048143594161841295, -0.05335632457394288, -0.12581534534016062, -0.04515066055658332, -0.04842077368526793, -0.04406547681624733, -0.052952852971735374, -0.05266567720127041], [-1.717024219269797, -0.42167667930326547, -0.3880038886848189, -0.3096378273955798, 2.8084731310341438, 0.055786178325734535, -0.2923540791056933, 0.17641339258450525, 8.539159846488445, 8.618849552806484, 6.794325015988141, 6.421834697813655, 7.811234126235178, 8.3990753482812, 8.583198142190179, 8.103577022632027]]}
```

