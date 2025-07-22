# 🏏 IPL First Innings Score Prediction Using Machine Learning

This project uses machine learning techniques to predict the first innings score of IPL cricket matches. By analyzing historical IPL data and engineering match-specific features, the model estimates the total runs a team might score in the first innings given team, venue, and match conditions.

---

## 📌 Overview

- **Goal:** Predict first-innings scores based on match conditions and historical data.
- **Dataset:** Historical IPL match data including teams, venue, overs, runs, and wickets.
- **ML Models Used:**
  - Linear Regression
  - Decision Tree Regression
  - Random Forest Regression
  - AdaBoost Regressor (with Linear Regression as base learner)

---

## 📊 Exploratory Data Analysis (EDA)

Performed initial analysis using:
- Descriptive statistics
- Team filtering (removing old/renamed teams)
- Over-based filtering (removed first 5 overs due to volatility)
- Venue standardization
- Time-based data transformations (datetime parsing)

---

## 🧹 Data Preprocessing

- Applied one-hot encoding to categorical variables: teams, venue.
- Removed irrelevant columns (e.g., player names).
- Created year-wise train/test splits.
- Reordered features for consistency and model training.

---

## 🤖 Model Training

All four models were trained and evaluated using the cleaned and preprocessed dataset.  
**Best Performance:**  
✅ **AdaBoost Regressor** achieved an **R² score of 0.86**, outperforming all other models in first-innings prediction.

---

## ⚙️ Score Prediction Functionality

A custom prediction function was built to:
- Accept live match inputs (batting team, bowling team, overs, runs, wickets, venue)
- Return an estimated score range using the Linear Regression model

---

## 🧪 Example Predictions

```python
predict_score('Chennai Super Kings', 'Mumbai Indians', 'Eden Gardens', current_score=50, overs=6, wickets=2)
