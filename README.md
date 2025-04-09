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
   A deep learning model is built using two LSTM layers with dropout regularization followed by dense layers to forecast the next closing price. Early stopping is employed to prevent overfitting.

4. **Evaluation:**  
   Model performance is measured using:
   - **Mean Absolute Error (MAE)**
   - **Root Mean Squared Error (RMSE)**
   - **R² Score**


Performance Evaluation
After training, the model achieved the following performance metrics on the test set:

Mean Absolute Error (MAE): 4.41

Root Mean Squared Error (RMSE): 5.63

R² Score: 0.8940

These metrics indicate that on average, the predictions deviate from the actual closing price by $4.41, and about 89.4% of the variance in the actual stock prices is explained by the model.

Results
Below is an example performance plot comparing the actual closing prices with the predicted prices:



Future Enhancements
To further improve the model's accuracy and robustness, future enhancements may include:

Feature Expansion:
Incorporate additional features such as trading volume and technical indicators (RSI, MACD, Bollinger Bands).

Advanced Architectures:
Experiment with hybrid models (e.g., combining CNNs with LSTMs or using Transformer-based techniques).

Hyperparameter Tuning:
Optimize the sequence length, the number of layers, dropout rates, and the learning rate using grid search or Bayesian optimization.

Data Augmentation:
Utilize a larger historical dataset or combine data from multiple stocks for training.

License
This project is open-source and available under the MIT License.

Contact
If you are interested in collaborating or have any questions about this project, please feel free to connect with me:

GitHub: Mostafa-Anwar-Sagor/STOCK-PREDICTION

LinkedIn: Mostafa Anwar





