# Bicycle-rental-prediction

---

# 🚲 Bicycle Rental Demand Prediction

Predicting daily bike rentals using weather and calendar data with machine learning.

---

## 📌 Project Overview

This project tackles a classic regression problem: **predicting the number of bicycles rented per day** using historical data and weather information. It demonstrates how to clean, explore, and model real-world time-based data using Python and scikit-learn.

By progressively improving the model — including crafting a custom `last_week` feature — I achieved a **reduction in RMSE from ~2186 to ~926**, showing the impact of thoughtful feature engineering.

---

## 🧠 What I Learned

- How to explore time-series data visually and statistically  
- How weather conditions like temperature, humidity, and visibility affect demand  
- How to use linear regression with multiple features  
- How to split time-based datasets for training and validation  
- How to evaluate model performance with **RMSE (Root Mean Squared Error)**

---

## 📊 Dataset

Sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset) — the `day.csv` file contains:

- Daily rental counts (`cnt`)
- Weather conditions (`temp`, `atemp`, `hum`, `windspeed`, `weathersit`)
- Calendar info (`weekday`, `holiday`, `workingday`, `mnth`, `yr`)

---

## 🔧 Tools & Libraries

- `pandas` for data manipulation  
- `matplotlib` for visualization  
- `scikit-learn` for modeling  
- `numpy` for math  
- Linear regression (single and multiple input features)

---

## 🛠️ Feature Engineering

I created a **`last_week`** feature that represents the average rentals from 7 days prior. This helped the model capture **seasonal trends and demand lag** — a move that significantly improved prediction accuracy.

---

## 📈 Results

| Model Version              | Features Used                                                | RMSE   |
|---------------------------|--------------------------------------------------------------|--------|
| Basic Linear Regression   | `atemp`                                                      | ~2186  |
| Multi-feature Regression  | `atemp`, `workingday`, `hum`, `weathersit`, `windspeed`      | ~1220  |
| + Lag Feature (`last_week`) | All above + `last_week`                                    | **~926** ✅ |

---

## 📷 Sample Visuals

![Prediction vs Actual](images/prediction_vs_actual.png)  
*Note: Add visuals from your notebook for impact.*

---

## 💬 How to Run

1. Clone this repo  
2. Install dependencies  
   ```bash
   pip install pandas matplotlib scikit-learn numpy
   ```
3. Run the Jupyter notebook `bicycle_rentals.ipynb`  
4. Review charts and model metrics

---

## 🙋🏾‍♂️ About Me

I'm ABIODUN, a data science enthusiast building smart solutions with Python. Let's connect on [LinkedIn](www.linkedin.com/in/abiodun-oguntola-811748224)!

---

