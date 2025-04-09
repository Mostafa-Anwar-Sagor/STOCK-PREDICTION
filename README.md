# Stock Price Prediction Using LSTM

This project implements a deep learning model to predict stock prices using historical data. By leveraging Long Short-Term Memory (LSTM) networks, the model learns temporal patterns in historical AAPL stock prices and forecasts future values.

## Table of Contents

- [Overview](#overview)
- [Methodology](#methodology)
- [Installation](#installation)
- [Usage](#usage)
- [Performance Evaluation](#performance-evaluation)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Contact](#contact)

## Overview

The goal of this project is to predict the closing price of Apple Inc. (AAPL) stock using historical data from Yahoo Finance. The data is normalized and structured into sequences for an LSTM model to learn time-series patterns and forecast future closing prices.

## Methodology

1. **Data Collection:**  
   Historical AAPL stock prices are downloaded using the [yfinance](https://pypi.org/project/yfinance/) package. Data is collected for the period from January 1, 2012 to January 1, 2024.

2. **Data Preprocessing:**  
   - Only the 'Close' price is used.
   - The data is normalized between 0 and 1 using `MinMaxScaler`.
   - Rolling sequences of 90 days are generated to capture historical trends for the LSTM model.

3. **Model Architecture:**  
   A deep learning model is built using two LSTM layers with dropout regularization followed by dense layers. The model is trained using the Adam optimizer with a learning rate of 0.0003 and early stopping to prevent overfitting.

4. **Evaluation:**  
   Model performance is evaluated using regression metrics:
   - **Mean Absolute Error (MAE)**
   - **Root Mean Squared Error (RMSE)**
   - **R² Score**

## Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/Mostafa-Anwar-Sagor/STOCK-PREDICTION.git
cd STOCK-PREDICTION
pip install yfinance scikit-learn tensorflow matplotlib
