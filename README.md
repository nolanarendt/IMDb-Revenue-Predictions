# IMDb Movie Revenue Predictions ![ImdbIcon](images/imdbheader.jpg)

## Problem Statement
Discover the most valuable features in predicting a movies revenue, and/or total score. Identify how valuable total score is when predicting revenue, and how impactful revenue is in predicting a movies total score.

## Table of contents

| File Name                      | Description of Notebook                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_CleaningTotalScore.ipynb](code/IMDb_CleaningTotalScore.ipynb)  | Merging and cleaning total score dataset. Final cleaned dataset exported. |
| [IMDb_CleaningRevenue.ipynb](code/IMDb_CleaningRevenue.ipynb)  | Merging and cleaning revenue dataset. Final cleaned dataset exported. |
| [IMDb_EDA.ipynb](code/IMDb_EDA.ipynb) | Exploratory data analysis of clean movie dataframe. |
| [IMDb_LinearRegressionTotalScore.ipynb](models/IMDb_LinearRegressionTotalScore.ipynb) | Linear Regression Model - Predicting Total Score |
| [IMDb_LinearRegressionRevenue.ipynb](models/IMDb_LinearRegressionRevenue.ipynb) | Linear Regression Model - Predicting Revenue |
| [IMDb_RandomForestRegressionTotalScore.ipynb](models/IMDb_RandomForestsRegressionTotalScore.ipynb) | Random Forests Regression Model - Predicting Total Score |
| [IMDb_RandomForestRegressionRevenue.ipynb](models/IMDb_RandomForestsRegressionRevenue.ipynb) | Random Forests Regression Model - Predicting Revenue |
| [IMDb_XGBoostRegressionTotalScore.ipynb](models/IMDb_XGBoostRegressionTotalScore.ipynb) | XGBoost Regression Model - Predicting Total Score |
| [IMDb_XGBoostRegressionRevenue.ipynb](models/IMDb_XGBoostRegressionRevenue.ipynb) | XGBoost Regression Model - Predicting Revenue|
| [IMDb_ExtraTreesRegressionTotalScore.ipynb](models/IMDb_ExtraTreesRegressionTotalScore.ipynb) | Extra Trees Regression Model - Predicting Total Score|
| [IMDb_ExtraTreesRegressionRevenue.ipynb](models/IMDb_ExtraTreesRegressionRevenue.ipynb) | Extra Trees Regression Model - Predicting Revenue|

| Data Set | Description of Dataset|
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_movies.csv](data/IMDb_movies.csv)  | Kaggle dataset containing movie title, year released, genres, etc. |
| [IMDb_names.csv](data/IMDb_names.csv)  | Kaggle dataset actors, actresses, and directors names and information. |
| [IMDb_ratings.csv](data/IMDb_ratings.csv)  | Kaggle dataset containing IMDb movie ratings for each title. |
| [IMDb_title_principals.csv](data/IMDb_title_principals.csv)  | Kaggle dataset containing actors, actresses, and director roles. |
| [tmdb_movies_data.csv](data/tmdb_movies.csv)  | Kaggle dataset containing revenue and budget. |
| [totalscore_df.csv](data/totalscore_df.csv)  | Final total score dataset used for modeling. |
| [revenue_df.csv](data/revenue_df.csv)  | Final revenue dataset used for modeling. |

## Workflow
1. Data Cleaning

2. Exploratory Data Analysis (EDA)

3. Preprocessing and Modeling

4. Evaluation

5. Conclusions and Recommendations

## Summary of Analysis
In process..

![TotalScoreHistplot](https://github.com/nolanarendt/capstone-dsi/blob/main/images/total_score_histplot.png)

![DirectorTotalScore_budgets](https://github.com/nolanarendt/capstone-dsi/blob/main/images/directortotalscore_budget.png)

![RevenueByRating](https://github.com/nolanarendt/capstone-dsi/blob/main/images/revenue_totalscore.png)

## Conclusions & Recommendations

## Sources Used
  1. Kaggle IMDb movies extensive dataset
    - https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+title_principals.csv
    
  2. TMDb Movies Dataset
    - https://www.kaggle.com/juzershakir/tmdb-movies-dataset
