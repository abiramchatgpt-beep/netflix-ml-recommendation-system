# Task 3 — Netflix Audience Rating Classification

Predicts a Netflix title's audience rating category (TV-MA, PG-13, TV-14,
etc.) using content attributes — type, country, genre, release year,
duration, and director presence.

## Approach

- Dropped rating classes with fewer than 10 titles (too rare to learn from)
- Trained and compared a Decision Tree and a Random Forest
- Tuned the Random Forest with GridSearchCV (n_estimators, max_depth,
  min_samples_leaf)
- Achieved ~49% accuracy across 11 rating classes (vs ~9% random baseline)

## Tech stack

Python, pandas, scikit-learn (DecisionTreeClassifier, RandomForestClassifier,
GridSearchCV)
