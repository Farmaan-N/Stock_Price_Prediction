# Stock Price Prediction using Polynomial Regression

## Overview

This project predicts the stock prices of a given company using **Polynomial Regression**. It fetches historical stock market data from **Yahoo Finance (yfinance)**, processes it, and trains a machine learning model to forecast future stock prices.

## Features

- **Automatic Data Fetching**: Retrieves stock market data from Yahoo Finance.
- **Preprocessing & Feature Engineering**: Adds a day count column for regression.
- **Machine Learning Model**: Uses **Polynomial Regression (degree=3)**.
- **Performance Metrics**: Evaluates the model using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.
- **Stock Price Prediction**: Predicts the closing price of the stock for the next 5 days.

## Technologies Used

- Python
- Yahoo Finance API (yfinance)
- Scikit-learn
- NumPy   
- Pandas
- Matplotlib
  

## Installation & Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/Farmaan-N/stock-price-prediction.git
   cd stock-price-prediction
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:

   ```bash
   python stock_price_prediction.py
   ```

## How It Works

1. **Fetch Data**: Automatically retrieves stock prices for `WIPRO.NS` (changeable in code).
2. **Preprocessing**:
   - Extracts `Open`, `High`, `Low`, `Volume`, and `Days` as features.
   - Sets `Close` price as the target variable.
3. **Train-Test Split**: Splits the dataset into **80% training** and **20% testing**.
4. **Model Development Process**:
   - Initially, a **Simple Linear Regression** model was used with only the closing price as the independent variable. However, due to stock price volatility, this resulted in an **underfitted model**.
   - Next, **Polynomial Features** were introduced in the regression model, with the degree adjusted to find the best fit. However, this led to high **Mean Absolute Error (MAE) and Mean Squared Error (MSE)**.
   - Finally, **multiple independent variables** (`Open`, `High`, `Low`, `Volume`, `Days`) were incorporated into the polynomial regression model, significantly improving accuracy and reducing errors.
5. **Evaluate Model**:
   - Calculates **MAE, MSE, RMSE**.
6. **Predict Future Prices**:
   - Forecasts the next **5 days' closing prices**.

## Example Output

```
Fetching data for WIPRO.NS from 2021-01-01 to 2025-03-21... Please wait.

Model Performance:
Mean Absolute Error (MAE): 3.25
Root Mean Squared Error (RMSE): 4.78

Predicted Stock Prices for Next 5 Days:
Day 1: 512.45
Day 2: 515.30
Day 3: 518.60
Day 4: 522.10
Day 5: 525.80
```

### Contributors

- **Farmaan Naser** ([@Farmaan-N](https://github.com/Farmaan-N))

