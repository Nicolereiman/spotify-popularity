# spotify-popularity
# 🎵 Predicting Spotify Song Popularity with Machine Learning

This project explores how machine learning can be used to predict the popularity of songs on Spotify based on their audio characteristics and metadata.  
It was developed as part of an advanced analytics course, but more importantly, it reflects my passion for applying data science to real-world challenges in music and culture.

## 💼 Real-World Motivation

Streaming platforms like Spotify rely on understanding user behavior and content dynamics to recommend, promote, and monetize music effectively.  
Being able to **predict the popularity of a track before it becomes a hit** allows platforms, labels, and independent artists to make smarter decisions about marketing, playlist placement, and production investment.

This project simulates exactly that challenge — predicting a song’s popularity (a continuous variable from 0 to 100) using features like `danceability`, `tempo`, `energy`, `valence`, and others extracted from Spotify metadata.

## 🧠 Problem Framing

- **Type:** Regression  
- **Target Variable:** `popularity` (0–100)  
- **Dataset Source:** Kaggle – 129,000+ songs with audio features  
- **Business Objective:** Identify high-potential tracks for investment and visibility on the platform

## 📊 Workflow Summary

### 1. Exploratory Data Analysis (EDA)

- Checked for missing values and outliers  
- Reviewed distributions of numerical and categorical features  
- Top artists, feature correlations, and range insights

### 2. Feature Engineering

- Used `langdetect` to infer the language of each track  
- Replaced artist names with a count of featured artists  
- Encoded language frequency numerically to avoid model bias

### 3. Pipeline & Preprocessing

A Scikit-learn pipeline was used to streamline transformations and model training:

- Scaling numerical variables with `StandardScaler`  
- Encoding language frequency  
- Fitting multiple regression models

### 4. Model Selection & Evaluation

Models evaluated via cross-validation using **R²** and **MSE**:
- XGBoost  
- Random Forest  
- LASSO  
- KNN  
- **HistGradientBoosting** (best performance)

✅ **Best model**: HistGradientBoosting  
- **MSE**: 151.83  
- **R² (test set)**: 0.6817

### 5. Hyperparameter Tuning

- Grid Search  
- Random Search  
- Hyperopt  
- Scikit-Optimize  
→ Best results achieved with **Scikit-Optimize**

### 6. Interpretability with SHAP

- Used SHAP values to explain model predictions  
- Identified most influential features:
  - `year`
  - `instrumentalness`
  - `loudness`

## 📌 Key Insights

- More recent songs tend to have higher popularity  
- Tracks with moderate instrumentalness and dynamic range score better  
- Model performs well but has natural limitations due to unpredictable factors like virality or artist fame

## 🚀 Why This Project Matters to Me

As someone passionate about **music, data, and storytelling**, this project represents the intersection of my interests. I believe in using data not just to analyze trends, but to **unlock creativity and cultural discovery**.

I’d love to contribute to platforms like Spotify, where music meets data at scale — and where projects like this can have a real impact on both creators and listeners.

## 🛠️ Tech Stack

- Python  
- Pandas  
- Scikit-learn  
- XGBoost  
- SHAP  
- langdetect  
- Hyperopt, Scikit-Optimize  
- Matplotlib, Seaborn

## 📁 Files

## 📁 Project Files

This repository includes all core components of the analysis, from data exploration to modeling and presentation:

| File                           | Description |
|--------------------------------|-------------|
| **`Spotify_EDA.ipynb`**        | Exploratory Data Analysis notebook: distributions, outliers, unique values, and correlations. |
| **`FeatureEngineering.ipynb`** | Feature engineering steps including language detection, artist count, and frequency encoding. |
| **`FinalModel.ipynb`**         | Regression model training and evaluation (XGBoost, Lasso, Random Forest, etc.) with final performance metrics. |
| **`Spotify_Popularity.pdf`** | Visual summary of the full project: objectives, methods, results, SHAP analysis, and key conclusions. |

> **Note:** The dataset was sourced from [Kaggle](https://www.kaggle.com/) and is not included in this repository due to size restrictions.

## 🙋‍♀️ About Me

I'm Nicole, a data scientist based in Buenos Aires. I bring together experience in **audience analytics**, **data journalism**, and **machine learning**, with a strong focus on **human-centered insights**. I’m excited about roles where I can connect data with culture — and help build meaningful digital experiences.

📫 [LinkedIn](https://www.linkedin.com/in/nicole-reiman-32877b245/) | [GitHub](https://github.com/Nicolereiman) 
