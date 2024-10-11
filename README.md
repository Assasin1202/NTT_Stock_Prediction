# Stock Price Prediction Model

## Overview

This project focuses on predicting stock prices using time-series data from NTT. The model development process includes exploratory data analysis (EDA), feature engineering, and training multiple machine learning models to evaluate their accuracy in real-world stock price prediction scenarios.

The project is divided into two approaches: one using an unscaled version of the dataset, and the other using a MinMax-scaled version. The models used for prediction include ARIMA, LSTM, and GRU, with additional features such as moving averages, lags, and volatility being engineered to enhance prediction accuracy.

## Features

- **Two Versions of the Dataset**:
  - **Unscaled Dataset**: Original stock price data
  - **MinMax-Scaled Dataset**: Scaled data using MinMaxScaler for better model performance
  
- **Feature Engineering**:
  - **Moving Averages**: Capture long-term trends
  - **Lags**: Incorporate previous time steps into the model for better short-term prediction
  - **Volatility**: Measure fluctuations in stock prices to account for market variability

- **Prediction Models**:
  - **ARIMA (AutoRegressive Integrated Moving Average)**: A traditional statistical method for time-series forecasting.
  - **LSTM (Long Short-Term Memory)**: A type of recurrent neural network well-suited for sequential data like stock prices.
  - **GRU (Gated Recurrent Units)**: A simpler recurrent neural network than LSTM, often achieving similar performance with less computational cost.

## Project Structure

## Project Structure

```bash
stock-price-prediction/
│
├── data/ 
│   ├── stock_data_preprocessed_unscaled.csv
│   ├── stock_data_preprocessed.csv
│   └── stock_price.csv
│
├── notebooks/
│   ├── EDA_feature_engineering.ipynb
│   ├── Model_scaled_data.ipynb
│   ├── Model_unscaled_data.ipynb
│   └── plots.ipynb
│
├── README.md
└── requirements.txt
```

## How to Run the Project

Clone the repository:

```bash
git clone https://github.com/yourusername/stock-price-prediction.git
```

Navigate to the project directory:

```bash
cd stock-price-prediction
```

Install the necessary dependencies:

```bash
pip install -r requirements.txt
```

Run the Jupyter notebooks to:
- Perform exploratory data analysis and feature engineering
- Train and evaluate the models

Start Jupyter:

```bash
jupyter notebook
```

Open the relevant notebooks under the `notebooks/` directory to view the step-by-step implementation.

## Results

The model performance is evaluated using various metrics including RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), and MAPE (Mean Absolute Percentage Error).

- **ARIMA** provides baseline predictions with limited accuracy for non-linear patterns.
- **LSTM and GRU** models outperform ARIMA in terms of capturing non-linear trends in stock price data.
- Results from both the scaled and unscaled datasets show that scaling improves the performance of deep learning models.

- The link for the presentation can be found here:
https://www.canva.com/design/DAGS4k45F9k/sLX9xIfUP7UEQ4Csbzz2Rw/view?utm_content=DAGS4k45F9k&utm_campaign=designshare&utm_medium=link&utm_source=editor

### Evaluation Metrics

- **RMSE**: Measures the square root of the average squared errors between the predicted and actual values.
- **MAE**: Represents the average magnitude of errors in a set of predictions, without considering their direction.
- **MAPE**: Provides a normalized metric showing the average percentage error between predicted and actual values.

The evaluation results and comparison between models are included in the `notebook/plots.ipynb` file.

## Conclusion

This project showcases how both statistical methods (ARIMA) and deep learning techniques (LSTM, GRU) can be applied to stock price prediction, with a focus on time-series data. The deep learning models, particularly LSTM and GRU, show better results in capturing stock price trends when using scaled data. ARIMA model also gives very good predictions for our time series data. Further enhancements can be made by experimenting with hyperparameters and exploring additional features for improving model accuracy.