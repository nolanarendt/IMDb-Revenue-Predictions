# IMDb Movie Revenue Predictions ![ImdbIcon](images/imdbheader.jpg)

## Background & Problem Statement
"To make a film is easy; to make a good film is war. To make a very good film is a miracle.", Alejandro Gonazlez Inarritu. For the movie industry, I aim to predict not only how well a movie will do, but also how much revenue a movie will make. Movies are released each day across the globe, but have you ever wondered how different casts would do in another movie, or genre? 

To help resolve the uncertainty in producing films, I aim to identify key features that will have high predictive value in both total score and revenue. One of my main goals for this project is to create actor, actress, and directors score for each movie, that are the average score of each movie they have been in prior. A barrier that I face with my data is that not every movie has actors or actresses, so for those I will repeat the score of actors or actresses and place that value in my data so that I do not remove any films. Another conflict that I ran into is that when I merged budgets and revenues for my original dataset, I lost around 10,000 rows of data, and thus, I decideded to create two seperate dataframes for predicting two different values. Each dataframe will be cleaned similarlly, but one dataset for IMDb_Score will be without budget and revenue, and the dataset for predicting revenue will be much smaller than the IMDb_Score dataset.

## Table of Contents

| File Name                      | Description of Notebook                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_CleaningTotalScore.ipynb](code/IMDb_CleaningTotalScore.ipynb)  | Merging and cleaning total score dataset. Final cleaned dataset exported containing 4,156 movies and 53,173 different actors, actresses, and directors. |
| [IMDb_CleaningRevenue.ipynb](code/IMDb_CleaningRevenue.ipynb)  | Merging and cleaning revenue dataset. Final cleaned dataset exported containing 1,843 movies 11,321 different actors, actresses, and directors. |
| [IMDb_EDA.ipynb](code/IMDb_EDA.ipynb) | Exploratory data analysis of both movie score and revenue dataframes. |
| [IMDb_LinearRegressionTotalScore.ipynb](models/IMDb_LinearRegressionTotalScore.ipynb) | Linear Regression Model - Predicting IMDb Movie Score |
| [IMDb_LinearRegressionRevenue.ipynb](models/IMDb_LinearRegressionRevenue.ipynb) | Linear Regression Model - Predicting Movie Revenue |
| [IMDb_RandomForestRegressionTotalScore.ipynb](models/IMDb_RandomForestsRegressionTotalScore.ipynb) | Random Forests Regression Model - Predicting IMDb Movie Score |
| [IMDb_RandomForestRegressionRevenue.ipynb](models/IMDb_RandomForestsRegressionRevenue.ipynb) | Random Forests Regression Model - Predicting Movie Revenue |
| [IMDb_XGBoostRegressionTotalScore.ipynb](models/IMDb_XGBoostRegressionTotalScore.ipynb) | XGBoost Regression Model - Predicting IMDb Movie Score |
| [IMDb_XGBoostRegressionRevenue.ipynb](models/IMDb_XGBoostRegressionRevenue.ipynb) | XGBoost Regression Model - Predicting Movie Revenue|
| [IMDb_ExtraTreesRegressionTotalScore.ipynb](models/IMDb_ExtraTreesRegressionTotalScore.ipynb) | Extra Trees Regression Model - Predicting IMDb Movie Score|
| [IMDb_ExtraTreesRegressionRevenue.ipynb](models/IMDb_ExtraTreesRegressionRevenue.ipynb) | Extra Trees Regression Model - Predicting Movie Revenue|

| Data Set | Description of Dataset|
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [IMDb_movies.csv](data/IMDb_movies.csv)  | Kaggle dataset containing movie title, year released, genres, etc. |
| [IMDb_names.csv](data/IMDb_names.csv)  | Kaggle dataset actors, actresses, and directors names and information. |
| [IMDb_ratings.csv](data/IMDb_ratings.csv)  | Kaggle dataset containing IMDb movie ratings for each title. |
| [IMDb_title_principals.csv](data/IMDb_title_principals.csv)  | Kaggle dataset containing actors, actresses, and director roles. |
| [tmdb_movies_data.csv](data/tmdb_movies_data.csv)  | Kaggle dataset containing revenue and budget. |
| [totalscore_df.csv](data/totalscore_df.csv)  | Final movie score dataset used for modeling. |
| [revenue_df.csv](data/revenue_df.csv)  | Final revenue dataset used for modeling. |

## Workflow
1. Data Cleaning

2. Exploratory Data Analysis (EDA)

3. Preprocessing and Modeling

4. Evaluation

5. Conclusions and Recommendations

## Summary of Analysis

From the data that was gathered from Kaggle and IMDb, I initially noticed that a majority of the datasets had numerous columns with a majority null values. To solve this, I merged the four datasets, identified columns with either the majority (95-100%) filled in values, and only kept those columns to serve as features in my prediction models. As a result, I decided that rather than using so few columns, this would give me an opportunity to feature engineer some columns and see how correlated they were. I decided to seperate actors, actresses, and directors into their own dataframes and give them each an average score, which was an average score of each movie they had been apart of. 

Initially, I was stuck on the idea that predicting a movies IMDb score would be interesting, but quickly switched to predicting both IMDb score and revenue, as revenue is probably most important to a company. In this project, I used four different regression models, ExtraTrees, Random Forests, Linear Regression, and XGBoost. I use each of the four models to predict both IMDb_Score and revenue, and then compare the two as show in visualizations below. For predicting IMDb_Score, my linear regression model worked with best, with a training score of 0.76, and a testing score of 0.767. The baseline was around 0.98 (error in predictions), to 0.49 with only a select amount of features.

In predicting revenue, I chose the ExtraTrees regression model as my best performing model. The training score came in around 0.82, and testing score around 0.76, a little overfit, but much less overfit than my other three regression models. The baseline before modeling was around $187 million, and was cut down to $71 million, and decrease in $116 million dollars. Going forward, I think that most of my attention will be focused on reducing revenue even smaller, although my dataset being so small is a barrier that I will have to resolve. Another block I noticed is that my data has less than four movies that grossed over one billion dollars, and as time goes on, I believe my data will become more accurate.

The Average IMDb_Score in Dataset

![TotalScoreHistplot](https://github.com/nolanarendt/capstone-dsi/blob/main/images/total_score_histplot.png)

The two plots below show the similarity between budgets and revenues in films. Budget and revenue are highly correlated by genre, and as seen, I believe that movies with higher budgets tend to make a larger revenue.

![AvgBudget_Genres](https://github.com/nolanarendt/capstone-dsi/blob/main/images/avgbudget_genres.png)

![AvgRevenue_Genres](https://github.com/nolanarendt/capstone-dsi/blob/main/images/avgrevenue_genres.png)

This visualization highlights the correlation between IMDb score and a movies revenue. The scores are rounded, but this highlights how movies that score a nine and above bring in more than double that of a movie that scores a seven or below.

![RevenueByRating](https://github.com/nolanarendt/capstone-dsi/blob/main/images/revenue_totalscore.png)

An interesting visualization that I thought was interesting when reflecting back on average revenues was that we see the genres with the highest average revenue all have a plot sentiment closer to zero.

![Plot_Sentiment](https://github.com/nolanarendt/capstone-dsi/blob/main/images/avgplotsentiment_genres.png)


## Conclusions & Recommendations

I believe that the lack of data was a huge barrier in making my model accurate, as my revenue dataframe contained less than 2000 rows of data. While I was able to more than 52,000 individuals (actors, actresses, and directors) in my dataframe, I believe that the lack of individual movies is something that I will attempt to resolve in the next steps of making more accurate predictions for both IMDb score and revenue.

Among the next steps include adding in more roles rather than just the three I have. I attempted to use more roles such as writer and producer, but found that my dataset got even smaller with each role that was added, and this may be resolved by scraping IMDb myself with the help of libraries such as BeautifulSoup. More developments in the future also include a fully functioning Heroku Application that will allow users to input different actors/actresses into films together and predict how well the movie would do, as well as predict how movies that have not yet been released will do if given budget.


## Sources Used
  1. Kaggle IMDb movies extensive dataset
    - https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+title_principals.csv
    
  2. TMDb Movies Dataset
    - https://www.kaggle.com/juzershakir/tmdb-movies-dataset
