# 🚲 Seoul Bike Sharing Demand Prediction

## 📌 Project Overview

This project focuses on predicting the **number of rented bikes** in Seoul based on different environmental, weather, seasonal, and time-related factors.

The project uses the **Seoul Bike Sharing Demand Dataset** and applies data preprocessing, feature encoding, feature selection, scaling, and machine learning regression algorithms.

## 🎯 Objective

To build a machine learning model that can predict the **Rented Bike Count** using factors such as:

* Temperature
* Humidity
* Wind Speed
* Visibility
* Dew Point Temperature
* Solar Radiation
* Rainfall
* Snowfall
* Hour
* Season
* Holiday
* Functioning Day

## 📊 Dataset

**Dataset:** Seoul Bike Sharing Demand

* **Rows:** 8,760
* **Columns:** 14
* **Target Variable:** `Rented Bike Count`
* **Problem Type:** Regression

### Dataset Features

| Feature                   | Description                             |
| ------------------------- | --------------------------------------- |
| Date                      | Date of observation                     |
| Rented Bike Count         | Number of rented bikes                  |
| Hour                      | Hour of the day                         |
| Temperature(°C)           | Temperature                             |
| Humidity(%)               | Humidity percentage                     |
| Wind speed (m/s)          | Wind speed                              |
| Visibility (10m)          | Visibility                              |
| Dew point temperature(°C) | Dew point temperature                   |
| Solar Radiation (MJ/m2)   | Solar radiation                         |
| Rainfall(mm)              | Rainfall                                |
| Snowfall (cm)             | Snowfall                                |
| Seasons                   | Season of the year                      |
| Holiday                   | Holiday status                          |
| Functioning Day           | Whether the bike system was functioning |

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 🔄 Project Workflow

1. Data Collection
2. Data Loading
3. Data Exploration
4. Data Preprocessing
5. Categorical Feature Encoding
6. Feature Selection
7. Data Transformation
8. Feature Scaling
9. Train-Test Split
10. Model Training
11. Model Evaluation
12. Model Comparison

## ⚙️ Data Preprocessing

The dataset was loaded using Pandas and explored to understand its structure.

Categorical variables were converted into numerical features using **One-Hot Encoding**.

Feature selection was performed using:

```python
SelectKBest
```

with:

```python
f_regression
```

The top **25 features** were selected for model training.

The selected features were then standardized using:

```python
StandardScaler
```

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

## 🤖 Machine Learning Models

The following regression algorithms were implemented:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. AdaBoost Regressor
5. Gradient Boosting Regressor

## 📈 Model Performance

| Model             |        MAE |          MSE | R² Score |
| ----------------- | ---------: | -----------: | -------: |
| Linear Regression |     287.64 |    139192.63 |     0.66 |
| Decision Tree     |     195.26 |    102577.70 |     0.75 |
| **Random Forest** | **154.60** | **59679.77** | **0.85** |
| AdaBoost          |     344.18 |    189086.01 |     0.54 |
| Gradient Boosting |     203.53 |     81255.23 |     0.80 |

## 🏆 Best Model

The **Random Forest Regressor** achieved the best performance among the tested models.

### Random Forest Results

* **MAE:** 154.60
* **MSE:** 59,679.77
* **R² Score:** 0.85

An R² score of **0.85** indicates that the Random Forest model explains a large proportion of the variation in bike rental demand in the test data.

## 🔍 Feature Selection

Feature importance scores were calculated using `SelectKBest` with `f_regression`.

Some of the higher-scoring features included:

* Temperature
* Seasons
* Dew Point Temperature
* Solar Radiation
* Hour
* Functioning Day
* Humidity
* Visibility
* Wind Speed

## 📁 Project Structure

```text
Seoul-Bike-Sharing-Demand/
│
├── bike.csv
├── seou_bike_project.ipynb
├── README.md
└── requirements.txt


## 💡 Conclusion

This project demonstrates how machine learning can be used to predict bike rental demand using weather, time, and seasonal information.

Among the five regression models tested, **Random Forest Regressor performed the best with an R² score of 0.85**, making it the most suitable model among the models evaluated in this project.
