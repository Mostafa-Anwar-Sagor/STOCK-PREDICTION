# Stock Price Prediction Using LSTM

This project implements a deep learning model to predict stock prices using historical data. By leveraging Long Short-Term Memory (LSTM) networks, the model learns temporal patterns from historical stock prices and forecasts future values. This repository contains the complete code, data preprocessing, model training, and evaluation steps for predicting AAPL (Apple Inc.) stock prices.

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

The goal of this project is to predict the closing price of Apple Inc. (AAPL) stock using an LSTM neural network. Historical data is downloaded from Yahoo Finance and preprocessed into sequences that enable the LSTM to learn time-series patterns. The model is evaluated using common regression metrics, and its performance is visually displayed with a plot comparing actual versus predicted prices.

## Methodology

1. **Data Collection:**  
   - Historical AAPL stock prices are downloaded via the [yfinance](https://pypi.org/project/yfinance/) Python package. Data spans from January 1, 2012 to January 1, 2024.

2. **Data Preprocessing:**  
   - Only the 'Close' price is used.
   - Data is normalized to a 0–1 range using `MinMaxScaler`.
   - Sequences (90 days per sample) are created for training the LSTM model.

3. **Model Architecture:**  
   - The model consists of two LSTM layers with dropout regularization followed by Dense layers.
   - The model is trained with the Adam optimizer and uses early stopping to prevent overfitting.

4. **Evaluation:**  
   - The model is evaluated using:
     - **Mean Absolute Error (MAE)**
     - **Root Mean Squared Error (RMSE)**
     - **R² Score**
   - Example performance metrics:
     - **MAE:** 4.41
     - **RMSE:** 5.63
     - **R² Score:** 0.8940

## Installation

Clone this repository and install the required dependencies.

```bash
git clone https://github.com/Mostafa-Anwar-Sagor/STOCK-PREDICTION.git
cd STOCK-PREDICTION
pip install yfinance scikit-learn tensorflow matplotlib

Usage
You can run the code using a Jupyter Notebook or as a standalone Python script.

Jupyter Notebook:
Open the provided notebook (e.g., Stock_Price_Prediction.ipynb) and run the cells in order.

Python Script:
Simply run the main Python file:

bash
Copy
python main.py
The main tasks performed by the code are:

Data download and normalization.

Sequence creation from normalized data.

Building and training the LSTM model.

Evaluating performance and plotting actual vs. predicted prices.

Performance Evaluation
After training, the model achieved the following metrics on the test set:

Mean Absolute Error (MAE): 4.41

Root Mean Squared Error (RMSE): 5.63

R² Score: 0.8940

These results indicate that about 89.4% of the variance in the actual stock prices is explained by the model, with average prediction errors around $4.41.

Results
A performance plot is generated to visually compare actual vs. predicted prices.


Note: Replace ./path_to_your_plot_image.png with the actual path to your saved plot image if you include it.

Future Enhancements
To further improve the model, consider:

Expanding features: Incorporate additional technical indicators (e.g., volume, RSI, MACD, Bollinger Bands).

Advanced model architectures: Experiment with hybrid models (e.g., CNN + LSTM, Transformer-based methods).

Hyperparameter tuning: Optimize model parameters using grid search or Bayesian optimization.

Data augmentation: Use a larger historical dataset or multi-stock datasets.

License
This project is open-source and available under the MIT License.

Contact
If you are interested in collaborating or have any questions about this project, please connect with me:

GitHub: Mostafa-Anwar-Sagor/STOCK-PREDICTION

LinkedIn: Mostafa Anwar

Feel free to reach out for collaborations or further discussion on stock price prediction and deep learning techniques.
