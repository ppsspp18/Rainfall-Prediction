# Rain Prediction Using Machine Learning

This project aims to predict whether it will rain tomorrow using historical weather data. It involves data preprocessing, feature engineering, model training, and evaluation using both traditional machine learning models and deep learning techniques including **LSTM** and **GRU****.

---

## 📊 Dataset

- **Source**: [weatherAUS.csv](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package)  
- **Target Variable**: `RainTomorrow` (Yes/No)

---

## 🔍 Features Used

The dataset includes features like:

- Temperature (`MinTemp`, `MaxTemp`)
- Rainfall
- Wind speed and direction
- Humidity, Pressure
- Sunshine, Cloud cover
- Binary rain today flag (`RainToday`)

Categorical variables like wind direction and `RainToday` are one-hot encoded.

---

## 🧹 Preprocessing Steps

- **Missing Value Handling**: Dropped rows with missing values after encoding.
- **Categorical Encoding**: One-hot encoding on wind direction and rain indicators.
- **Outlier Treatment**: IQR-based capping on numerical columns.
- **Feature Scaling**: Normalization applied to numerical columns.
- **Class Imbalance**: SMOTE used to balance the binary target class.
- **Dimensionality Reduction(rainfall_prediction_2)**: PCA used to reduce feature space before deep learning.

---

## 🤖 Models Trained

### Traditional Machine Learning Models

- Logistic Regression  
- Decision Tree  
- Random Forest  
- K-Nearest Neighbors  
- Support Vector Machine (LinearSVC)  
- Naive Bayes  
- XGBoost  
- LightGBM  
- CatBoost
- LWP (Learning with Prototypes)

### Deep Learning Models

- **LSTM (Long Short-Term Memory)**
- **GRU (Gated Recurrent Unit)**

> ✅ **Best Performance Achieved**  
> Using LSTM with PCA
> - **Accuracy**: **95%**  
> - **F1 Score**: **0.90**

---

## 📈 Evaluation Metrics

Each model was evaluated using:

- Accuracy  
- F1 Score  
- Precision & Recall  
- Jaccard Index  
- Log Loss  

These metrics ensure a comprehensive and fair comparison, especially in the presence of class imbalance.

---

## 📦 Requirements

Install dependencies using pip:

```bash
pip install pandas scikit-learn matplotlib seaborn xgboost lightgbm catboost imbalanced-learn tensorflow
