# March Madness XGBoost Model


## Introduction

March Madness is one of the most popular sporting spectacles in the world, drawing in millions of viewers and generating some of the greatest stories in sports. Upsets are commonplace in March, and while favorites tend to do well, **nobody** knows when the next underdog might break out and beat the 1-seed.

Or do they? Every year, as March approaches, so too does a huge uptick in betting, bracket-making, and general attempts to predict the outcome of every single game. A significant part of this involves data science; especially in the last few years, the number of statistics and probabilities floating around relating to the tournament has increased exponentially. With this said, I - being an avid college basketball fan (Go Heels!) - wanted to make my own model and see just how well I could predict one of the most unpredictable tournament in sports.

To do so, I created a model to predict teams' scores using XGBoost and historical data ranging from 2003-2023. Given these scores, the model is able to select the team that is predicted to progress and eventually win the whole tournament.


## Research and Data

I've done research on March Madness before; specifically, my friend and I researched the probability of upsets in the NCAA Men's Basketball Tournament, and we presented our research at UNC and at Carnegie Mellon. For that research, we independently collected several statistics online and put them together, and created a logistic regression model that could predict the winner for each game in the tournament (0 represented a win for the "better" seed and 1 represented a win for the "worse seed", or the underdog).

With this approach in mind, I wanted to consider a different approach for this new model. Instead of predicting the outcome of the game as a win or a loss, I wanted to predict the score for each game (especially as this would also help me assess how close the model expected games to be). As for the data, I utilized a dataset containing historical data of NCAA men's basketball games ranging as far back as 1985 (although I only analyzed games from 2003 and later). The dataset was made publicly available by Kaggle and much of the actual historical data was provided by Kenneth Massey, so credit goes out to both Kaggle and Kenneth Massey for this data.

For this model, I decided to use regular season data to predict scores in each tournament game. In the future, I plan to use data from the actual tournaments as well, along with ratings provided by both Massey and other sources.


## Notable Predictions

Here's some of the games that the model predicted correctly (as of 3/28):

* GCU (12) vs. St. Mary's (5) :white_check_mark:
* Oakland (14) vs. Kentucky (3) :white_check_mark:
* NC State (11) vs. Texas Tech (6) :white_check_mark:
* James Madison (12) vs. Wisconsin (5) :white_check_mark:
* Michigan State (9) vs. Mississippi State (8) :white_check_mark:

**Current Overall Accuracy Rate: 58.33%**