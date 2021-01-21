# IMDb Movie Revenue Predictions ![ImdbIcon](images/imdbheader.jpg)

## Problem Statement
Discover the most valuable features in predicting a movies revenue, and/or total score.

## Table of contents

| File Name                      | Description of Notebook                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_Cleaning.ipynb](IMDb_Cleaning.ipynb)  | Merging and cleaning data process. Final cleaned dataset exported. |
| [IMDb_EDA.ipynb](IMDb_EDA.ipynb) | Exploratory data analysis of clean movie dataframe. |
| [IMDb_LinearRegressionTotalScore.ipynb](models/IMDb_LinearRegressionTotalScore.ipynb) | Linear Regression Model - Predicting Total Score |
| [IMDb_LinearRegressionRevenue.ipynb](models/IMDb_LinearRegressionRevenue.ipynb) | Linear Regression Model - Predicting Revenue |
| [IMDb_RandomForestRegressionTotalScore.ipynb](models/IMDb_RandomForestRegressionTotalScore.ipynb) | Random Forests Regression Model - Predicting Total Score |
| [IMDb_RandomForestRegressionRevenue.ipynb](models/IMDb_RandomForestRegressionRevenue.ipynb) | Random Forests Regression Model - Predicting Revenue |
| [IMDb_XGBoostTotalScore.ipynb](models/IMDb_XGBoostTotalScore.ipynb) | XGBoost Regression Model - Predicting Total Score |
| [IMDb_XGBoostRevenue.ipynb](models/IMDb_XGBoostRevenue.ipynb) | XGBoost Regression Model - Predicting Revenue|

| Data Set | Description of Dataset|
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_movies.csv](data/IMDb_movies.csv)  | Kaggle dataset containing movie title, year released, genres, etc. |
| [IMDb_names.csv](data/IMDb_names.csv)  | Kaggle dataset actors, actresses, and directors names and information. |
| [IMDb_ratings.csv](data/IMDb_ratings.csv)  | Kaggle dataset containing IMDb movie ratings for each title. |
| [IMDb_title_principals.csv](data/IMDb_title_principals.csv)  | Kaggle dataset containing actors, actresses, and director roles. |
| [tmdb_movies_data.csv](data/tmdb_movies.csv)  | Kaggle dataset containing revenue and budget. |
| [final_df.csv](data/final_df.csv)  | Final dataset used for modeling. |

## Workflow
1. Data Cleaning

2. Exploratory Data Analysis (EDA)

3. Preprocessing and Modeling

4. Evaluation

5. Conclusions and Recommendations

## Summary of Analysis
In process..

![TotalScoreHistplot](https://git.generalassemb.ly/nolanarendt/Submissions/blob/main/Projects/capstone_project-master/images/total_score_histplot.png)

![DirectorTotalScore_budgets](https://git.generalassemb.ly/nolanarendt/Submissions/blob/main/Projects/capstone_project-master/images/directortotalscore_budget.png)

![RevenueByRating](https://git.generalassemb.ly/nolanarendt/Submissions/blob/main/Projects/capstone_project-master/images/revenue_totalscore.png)

## Conclusions & Recommendations

## Sources Used
  1. Kaggle IMDb movies extensive dataset
    - https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+title_principals.csv
    
  2. TMDb Movies Dataset
    - https://www.kaggle.com/juzershakir/tmdb-movies-dataset
