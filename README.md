# 🌧️ Rain Prediction Using Machine Learning

This project aims to predict whether it will rain tomorrow using historical weather data. It involves data preprocessing, feature engineering, model training, and evaluation using various machine learning algorithms.

## 📁 Dataset

- **Source**: [weatherAUS.csv](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package)
- **Target Variable**: `RainTomorrow` (Yes/No)

## 📊 Features Used

The dataset includes features like:
- Temperature (MinTemp, MaxTemp)
- Rainfall
- Wind speed and direction
- Humidity, Pressure
- Sunshine, Cloud cover
- Binary rain today flag (`RainToday`)

Categorical variables like wind direction and `RainToday` are one-hot encoded.

## 🛠️ Preprocessing Steps

- **Missing Value Handling**: Dropped rows with missing values after encoding.
- **Categorical Encoding**: One-hot encoding on wind direction and rain indicators.
- **Outlier Treatment**: IQR-based capping on numerical columns.
- **Class Imbalance**: SMOTE used to balance the binary target class.

## 🤖 Models Trained

The following models were trained and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors
- Support Vector Machine (LinearSVC)
- XGBoost
- LightGBM
- CatBoost

Each model was evaluated using metrics like:
- Accuracy
- F1 Score
- Precision & Recall
- Jaccard Index
- Log Loss

## 📈 Evaluation Metrics

Models are compared using a variety of classification metrics to ensure robust evaluation, especially given the class imbalance.

## 🔧 Requirements

Install dependencies using pip:

```bash
pip install pandas scikit-learn matplotlib seaborn xgboost lightgbm catboost imbalanced-learn
