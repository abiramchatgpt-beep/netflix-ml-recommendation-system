# Task 5 — Netflix Trend Forecasting Model

Forecasts future Netflix content release volume based on historical
release-year patterns, using lag-based feature engineering to turn the
time series into a supervised regression problem.

## Approach

- Built yearly release counts (2000–2020), with lag features, a 3-year
  rolling average, and year-over-year growth
- Time-based train/test split (trained on earlier years, tested on the
  most recent ones — not a random split, to avoid leaking future data)
- Compared Linear Regression and Random Forest
- Generated 3-year-ahead forecasts

## Key finding

Both models perform poorly (negative R²) on the test years. The catalog
grew steeply and consistently from 2003–2016, then plateaued and
declined 2017–2020. Both models learned the steep growth phase and
extrapolated it into the plateau period, overshooting actual counts.
This is a clear example of a regime change breaking a trend-following
model — a genuine limitation worth discussing rather than hiding.

## Tech stack

Python, pandas, scikit-learn (LinearRegression, RandomForestRegressor)
