# 🚗 Used Car Analysis: Linear Regression, Logistic Regression & Time Series

A student machine learning project exploring **Linear Regression**, **Logistic Regression**, and **Time Series Forecasting** on the CarDekho dataset.

---

## 📁 Project Structure

```
car-price-prediction/
│
├── car_price_prediction.ipynb         # Single Jupyter Notebook containing the full project
│
├── data/
│   └── raw/
│       ├── car data.csv               # Primary dataset (301 rows)
│       ├── CAR DETAILS FROM CAR DEKHO.csv
│       ├── Car details v3.csv
│       └── car details v4.csv
│
├── requirements.txt                   # Project dependencies (including statsmodels)
└── README.md                          # Project documentation
```

---

## 🎓 College Project Outline

The notebook [`car_price_prediction.ipynb`](file:///C:/Users/samar/.gemini/antigravity/scratch/car-price-prediction/car_price_prediction.ipynb) is organized into standard academic sections:

### 1. Data Inspection & Cleaning
- Loading `car data.csv`.
- Inspecting data types, summary statistics (`describe()`), and null values.

### 2. Exploratory Data Analysis (EDA)
- Distribution histogram of `Selling_Price`.
- Scatter plot of showroom `Present_Price` vs `Selling_Price`.
- Count plots for `Fuel_Type`, `Seller_Type`, and `Transmission`.

### 3. Feature Engineering
- Calculating car age: `Car_Age = 2024 - Year`.
- Categorical one-hot encoding (`pd.get_dummies()`).
- Correlation heatmap.

### 4. Model 1: Linear Regression (Price Prediction)
- Predicts continuous resale price in Lakhs INR.
- Explains intercept and feature coefficients.
- **Metrics:** $R^2 = 84.90\%$, $\text{MAE} = 1.22\text{ Lakhs}$, $\text{RMSE} = 1.87\text{ Lakhs}$.
- Actual vs. Predicted price scatter plot.

### 5. Model 2: Logistic Regression (Budget vs High-Price Classification)
- Predicts whether a car sells for above or below median price (₹3.60 Lakhs).
- Standardizes features using `StandardScaler`.
- **Metrics:** $\text{Accuracy} = 95.08\%$, Precision / Recall / F1 = $0.95$.
- Confusion Matrix heatmap.

### 6. Model 3: Time Series Analysis & Forecasting
- Aggregates average selling prices across years (2003–2018).
- Calculates a **3-Year Simple Moving Average (SMA)** to smooth trend noise.
- Forecasts future average prices (2019 to 2023) using **Linear Trend Modeling** and **Holt's Exponential Smoothing**.
- Time series line plots showing historical trends alongside future projections.

### 7. Sample Vehicle Prediction
- Evaluates a sample car (2018 Petrol Manual Swift) across both models.

---

## 🚀 How to Run

1. Open PowerShell in this project folder:
   ```powershell
   cd "C:\Users\samar\.gemini\antigravity\scratch\car-price-prediction"
   ```

2. Start Jupyter Notebook:
   ```powershell
   .\.venv\Scripts\jupyter notebook car_price_prediction.ipynb
   ```
