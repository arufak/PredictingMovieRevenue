# 🎥 Movie Revenue Prediction

This project aims to predict the revenue of movies using a variety of machine learning models and a dataset derived from the TMDB Movie Database. The goal is to help movie producers make informed decisions about how well a movie might perform before release, allowing them to adjust strategies, such as release dates or marketing efforts, accordingly.

## 📖 Overview

The movie industry generates over $100 billion annually, yet more than 80% of films fail to make a profit. Understanding the factors that drive movie profitability can help studios and producers make better business decisions. Our machine learning models analyze various predictors to estimate a movie's potential revenue prior to its release.

## 📊 Dataset

We used the TMDB Movie Dataset, which includes information on approximately 700,000 movies. Key features of the dataset include:
- Movie titles
- Genres
- Release dates
- Cast and crew details
- Budget and revenue

We performed several cleaning steps to focus on predicting a movie's revenue using features available before a movie's release.

## 🧹 Data Preprocessing

Several preprocessing steps were taken to ensure the dataset was suitable for modeling:
1. Dropped irrelevant columns such as movie posters and reviews.
2. Removed invalid movie entries with no budget or revenue data.
3. Created dummy variables for genres and release seasons.
4. Calculated new features such as actor and director's past success.
5. Fetched additional data using the TMDB API, including director information and movie age ratings.

## 📈 Features

Some of the engineered features include:
- **Main Actor’s Previous Success**: A predictor based on the ratio of an actor's prior movies' successes.
- **Director’s Previous Success**: Similar to actor success, calculated using the director's past movie revenues.
- **Release Season**: The season in which the movie was released (spring, summer, fall, winter).
- **Competitors**: Number of movies released in the same genre and season.

## 🤖 Models

We experimented with various machine learning models to predict movie revenue:
1. **Linear Regression, LASSO, and Ridge**: These models provided a baseline but showed signs of overfitting.
2. **K-Nearest Neighbors (KNN)**: Tuned using cross-validation, but performance was limited.
3. **Decision Trees**: Used with a max depth of 3, but still suffered from high test MSE.
4. **Boosted Decision Trees**: Our best-performing model, tuned using GridSearch with different depths and learning rates.
5. **Bagging and Random Forest**: Attempted to reduce overfitting and improve prediction accuracy.
6. **Neural Networks**: Tested models with different activation functions (Tanh and ReLU) but were not fully tuned.

### 🏆 Best Model Performance
- **Boosted Decision Tree**: Test MSE: 1.15e+16
- **Random Forest**: Test MSE: 1.18e+16

## ⚠️ Challenges

We encountered several challenges during the project:
- Lack of critical predictors like marketing spend or distribution methods.
- Computational limits when running models with large datasets.
- Skewed budget data, leading to difficulty in accurate predictions.
- Presence of extreme outliers in revenue data.

## 📝 Conclusion

Our analysis highlighted the difficulty of accurately predicting movie revenue with the available dataset. Key takeaways include the importance of budget, runtime, and the previous success of actors and directors. However, due to the dataset's limitations, further data on marketing, distribution, and platform-specific factors is required to improve predictions.

## 🚀 Future Work

- Integrate additional predictors, such as marketing budget, streaming platform, and distribution companies.
- Tune the neural network models further for better accuracy.
- Explore more advanced ensemble techniques to improve predictions.

## 👩‍💻 Authors

- Arufa Khanom  
- Zachary Formes  
- Ana Ramirez

