# xg-model-premier-league
Custom Expected Goals (xG) model built on StatsBomb open data (Premier League 2015/16) — Logistic Regression vs. XGBoost, benchmarked against StatsBomb’s own xG.

# Premier League Expected Goals (xG) Model

A from-scratch Expected Goals model built on StatsBomb's open shot event data for the 2015/16 Premier League season, comparing Logistic Regression and XGBoost.

## What I did:
- Parsed raw shot event data (location, body part, technique, shot type,  pressure, one-on-ones, aerial duels)
- Calculated distance-to-goal and shot-angle features from shot coordinates
- Trained and tuned Logistic Regression and XGBoost classifiers with  GridSearchCV (5-fold CV, log-loss scoring)
- Benchmarked predictions against StatsBomb's own published xG values
- Visualized shot maps on a pitch (mplsoccer) and team-level xG performance  (goals scored vs. xG, over/underperformance)

## Stack Python · pandas · scikit-learn · XGBoost · mplsoccer · statsbombpy

## Results:
- Logistic Regression and XGBoost performed comparably (log-loss ≈ 0.266–0.268)
   — a good reminder that a well-featured linear model can hold its own against a gradient booster on tabular shot data
- Predicted xG correlates strongly with StatsBomb's own published xG  (r ≈ 0.84), validating that the feature set captures real shot quality
- Team-level xG differential highlighted Manchester City, West Ham, and  Spurs as the biggest overperformers of goals vs. xG that season

## Motivation:
Built as part of my path toward football performance analysis — I wanted to understand what actually goes into an xG model rather than treating it as a black box, and to see how close a self-built model gets to StatsBomb's own.

## Data Shot event data from [StatsBomb's open data]
