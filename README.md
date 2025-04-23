# Golden Age TV: Basic Python Analysis (Season 1)
_A data-driven dive into how IMDb votes relate to TV ratings since the rise of prestige television_

## 🎬 Introduction

This project explores trends in television ratings during the "Golden Age" of TV, beginning with *The Sopranos* in 1999. The primary objective is to examine whether the number of IMDb votes a title receives influences its rating. The hypothesis: critically acclaimed shows from this era also attract the highest audience engagement in the form of votes.

## 📁 Dataset

The dataset is located at `/datasets/movies_and_shows.csv` and includes the following columns:

| Column         | Description                                     |
|----------------|-------------------------------------------------|
| `name`         | Name of the actor or director                   |
| `character`    | Character played (for actors)                   |
| `role`         | Contribution type (actor or director)           |
| `title`        | Title of the movie or show                      |
| `type`         | Type of media (`movie` or `show`)               |
| `release_year` | Year the title was released                     |
| `genres`       | List of genres                                  |
| `imdb_score`   | IMDb rating                                     |
| `imdb_votes`   | Number of votes on IMDb                         |

> **Note:** The dataset is not included in this repository. 

## 🔍 Project Stages

### 1. 🧐 Data Overview
- [x] Load dataset and preview first 10 rows
- [x] Inspect column names, data types, and missing values
- [x] Identify numerical and categorical features

### 2. 🧹 Data Preprocessing
- [x] Standardize column names (lowercase, no spaces)
- [x] Drop rows with missing `imdb_score` or `imdb_votes`
- [x] Remove exact and implicit duplicates (e.g., unify inconsistent `type` values)

### 3. 📊 Data Analysis
- [x] Filter titles released in 1999 or later
- [x] Round IMDb scores into buckets for comparison
- [x] Exclude outliers with extremely low vote counts
- [x] Calculate average votes per score group to evaluate hypothesis

## 📝 Key Takeaways

### ✅ Data Cleanup
- Cleaned and standardized column names
- Removed incomplete and duplicate records to ensure accuracy

### 📈 Insights
- Grouping and filtering revealed relevant titles from the Golden Age era
- There is an observable correlation between higher ratings and larger vote counts

## ⚙️ How to Run

```bash
 1. Clone this repository
git clone https://github.com/yourusername/golden-age-tv.git
cd golden-age-tv

 2. (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows use: venv\Scripts\activate

 3. Install required libraries
pip install pandas

 4. Ensure the dataset is placed in the correct location:
    ./datasets/movies_and_shows.csv

 5. Run the analysis
    (either in Jupyter Notebook or as a script if provided)
jupyter notebook Golden_Age_TV_Analysis.ipynb

```


## 🚀 Future Work
- Expand analysis to include more genres or platforms (e.g., Netflix, HBO, AMC)
- Explore other influencing factors like production budget, awards, or critical reviews

