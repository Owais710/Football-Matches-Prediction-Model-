# ⚽ Football Scoreline Predictor (Premier League)

A machine learning–based football match scoreline prediction system built using historical Premier League data and deployed with Streamlit.

The model predicts expected goals scored and conceded and simulates realistic match scorelines using Poisson distribution.

---

## 📓 Model Training Notebook

The complete data preprocessing, feature engineering, model training, and evaluation pipeline is available in the Jupyter notebook:

This notebook includes:
- Data cleaning & preprocessing
- Feature engineering (xG, xGA, possession, venue, teams)
- Label encoding
- Model training for:
  - Goals For (GF)
  - Goals Against (GA)
- Model saving using `joblib`

---

## 🧠 Model Explanation

- Two regression models are trained:
  - **GF model** → predicts goals scored
  - **GA model** → predicts goals conceded
- Predicted values are treated as Poisson parameters (λ)
- Final match score is sampled from a Poisson distribution

This approach produces realistic football scorelines rather than deterministic outputs.

---

## 🖥 Streamlit Interface

Users can:
- Select teams and match venue
- Input match statistics
- Generate predicted scorelines
- View expected goals (λ values)

---

## 🛠 Tech Stack

- Python 3
- Pandas & NumPy
- Scikit-learn
- Streamlit
- Joblib

---


