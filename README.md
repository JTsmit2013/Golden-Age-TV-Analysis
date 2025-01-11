# Golden Age TV Basic Python Analysis

## Introduction
This project analyzes data from the entertainment industry, specifically focusing on the "Golden Age" of television, which began in 1999 with The Sopranos and continues to this day. The primary objective is to investigate how the number of votes a title receives impacts its IMDb rating. The hypothesis is that highly-rated shows released during this period also garner the most votes.

## Dataset
The dataset is stored in /datasets/movies_and_shows.csv and contains the following columns:

- **name:** Name of the actor or director.
- **character:** Character played (for actors).
- **role:** The person's contribution to the title (actor or director).
- **title:** Title of the movie or show.
- **type:** Type of media (movie or show).
- **release_year:** Year of release.
- **genres:** List of genres.
- **imdb_score:** IMDb rating.
- **imdb_votes:** Number of votes on IMDb.

## Stages
1. Data Overview
  - Load the dataset and display the first 10 rows.
  - Review column names, data types, and missing values.
  - Identify key characteristics of the dataset, such as numeric columns for analysis and categorical columns for grouping.
2. Data Preprocessing
  - Column Renaming:
      - Standardize column names by converting them to lowercase, removing whitespaces, and replacing numeric zeros (0) with the letter o.
  - Handling Missing Values:
      - Drop rows with missing imdb_score or imdb_votes to ensure accuracy in analysis.
  - Duplicate Removal:
      - Identify and remove duplicate rows to avoid skewed results.
  - Resolving Implicit Duplicates:
      - Harmonize inconsistent values in the type column (e.g., replacing variations like "tv show" and "shows" with "SHOW").
3. Data Analysis
  - Filtering Data:
      - Analyze shows and movies released in 1999 or later.
  - Grouping Scores:
      - Round IMDb scores to group ratings into buckets.
  - Outlier Identification:
      - Identify outliers among scores based on the number of votes and exclude titles with exceptionally low votes.
  - Validation of Hypothesis:
      - Calculate average votes for each score bucket and evaluate the hypothesis.

## Key Takeaways
1. Data Cleanup:

    - Column names have been standardized for easier processing.
    - Missing values and duplicates have been removed to improve data reliability.
2. Insights:
    - Grouping and filtering steps ensure that analysis is focused on relevant titles.
    - High vote counts may correlate with high ratings, particularly for titles released during the "Golden Age."

## How to Run
1. Clone this repository.
2. Ensure you have Python installed with the required libraries (pandas).
3. Place the dataset in the /datasets/ directory.
4. Run the provided Jupyter Notebook or Python scripts for analysis.

## Future Work
- Expand the analysis to include more genres or platforms.
- Investigate additional factors influencing ratings, such as release platform or budget.

