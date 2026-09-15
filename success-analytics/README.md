# Task 6 — Netflix Content Success Analytics Engine

An end-to-end pipeline that analyzes content patterns and generates
automated business insights about what drives TV show renewal.

## Scope note

This dataset has no view counts, ratings, or popularity scores — there's
no direct "success" metric to predict. The one genuinely meaningful
proxy available is TV show season count: Netflix only renews shows
people actually watch, so more seasons is a real (if imperfect) signal
of success. This engine is scoped to TV shows only for that reason.

## Approach

- Feature engineering: primary genre, primary country, rating, release
  year, genre count, director presence
- Trained and compared 3 models: Linear Regression, Random Forest,
  Gradient Boosting
- Best model (Gradient Boosting) achieved R² = 0.09 — modest, and
  honestly reported: this dataset's metadata alone only partially
  explains renewal outcomes, since it lacks viewership/budget/critical
  reception data
- Generated automated insights: feature importance ranking, top genres
  and countries by average season count
- Visual report: feature importance chart + top-genres chart

## Caveat worth noting

`release_year` ranks as the top predictor, but this is partly a
survivorship effect — older shows have simply had more time to
accumulate seasons — not necessarily a signal that older shows are
better received.

## Tech stack

Python, pandas, scikit-learn (LinearRegression, RandomForestRegressor,
GradientBoostingRegressor), matplotlib
