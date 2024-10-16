# Forecast-Stock-Price-Using-SARIMA 

## Introduction

This repository contains the implementation of an Apple stock price prediction model using the **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** technique. Stock price prediction has been a critical area of interest in finance and machine learning. SARIMA is widely used for time series forecasting, and in this project, it is applied to predict Apple Inc. (AAPL) stock prices.

## Methods Used

### 1. **Data Preprocessing**
   The dataset used is Apple stock price data from the file `apple.csv`. The preprocessing step involves:
   - Parsing the date column.
   - Handling missing values.
   - Visualizing the stock price data to observe trends and seasonality.

### 2. **Stationarity Check**
   To apply the SARIMA model, the stock price data needs to be stationary. The Augmented Dickey-Fuller (ADF) test was used to determine whether the series is stationary. In case of non-stationarity, differencing is applied to remove trends and seasonality.

### 3. **SARIMA Model**
   SARIMA is an extension of ARIMA that supports univariate time series data with a seasonal component. The model is represented as:
   - **SARIMA(p, d, q)(P, D, Q, s)** where:
     - `p`: Number of lag observations (AR term)
     - `d`: Degree of differencing
     - `q`: Size of the moving average window (MA term)
     - `P`, `D`, `Q`: Seasonal components
     - `s`: Seasonality period

   After determining stationarity, SARIMA parameters are selected, and the model is trained on the Apple stock dataset.

### 4. **Model Evaluation**
   The model is evaluated using forecasting error metrics such as:
   - Mean Absolute Error (MAE)
   - Root Mean Squared Error (RMSE)
   - Mean Absolute Percentage Error (MAPE)

   These metrics provide insight into the accuracy of the predictions.

## Data Source

The stock price data for Apple Inc. is available in the `apple.csv` file included in this repository. It contains historical stock prices, including:
   - Date
   - Open price
   - High price
   - Low price
   - Close price
   - Volume
   
The dataset is available for public use and sourced from financial APIs or data providers.

## Summary and Learnings

- **SARIMA Model Performance:** SARIMA is an effective method for time series forecasting, especially when the data shows clear seasonality. For Apple stock prices, the model captured both trend and seasonal components accurately.
  
- **Data Stationarity:** Ensuring data stationarity is a key requirement for applying SARIMA models. Differencing techniques and ADF tests were used effectively to achieve stationarity in the Apple stock data.

- **Challenges:** One challenge is optimizing the model's parameters (p, d, q, P, D, Q, s), which requires extensive tuning and validation. However, with careful selection, SARIMA provides reliable predictions.

- **Applications:** This model can be used for short-term forecasting of Apple stock prices, which is useful for investors, analysts, and finance professionals.

## Requirements

To run the notebook, the following libraries are required:
```bash
pip install pandas numpy statsmodels matplotlib

