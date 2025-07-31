# Cryptocurrency Price Forecasting Engine

This repository contains the code for a deep learning model developed to predict Bitcoin (BTC/USD) price trends using historical market data. This project was created as part of a Kaggle competition and focuses on the end-to-end workflow of time-series forecasting in a volatile financial market.

## Project Summary

This project demonstrates a complete data science pipeline, including:
- An automated data ingestion process using the Binance API.
- Feature engineering of technical indicators to capture market dynamics.
- Development and tuning of an LSTM neural network designed for sequence prediction.
- A rigorous model validation strategy suited for financial time-series data to prevent lookahead bias.

## Dataset

The dataset, consisting of over 50,000 OHLCV (Open, High, Low, Close, Volume) data points, was sourced directly from the Binance API. The data ingestion script is included in this repository. No external data download is required to run this project.

## My Approach

1.  **Data Pipeline:** I engineered a data pipeline to automate the ingestion, cleaning, and feature engineering process, ensuring a reproducible and scalable workflow.

2.  **Model Selection:** I chose an **LSTM (Long Short-Term Memory) neural network** because of its proven effectiveness in capturing long-term dependencies and non-linear patterns in sequential data, which is a hallmark of financial time-series.

3.  **Validation Strategy:** To ensure the model's predictions were realistic and not overfitted, I implemented **rigorous walk-forward testing**. This method involves training the model on a historical period and testing it on the immediate future, which closely simulates a live trading environment and prevents data leakage from the future.

## Key Results

* The final model achieved a **Pearson Correlation Coefficient of 0.0934 with a p-value of less than 0.01**.
* This result indicates a **statistically significant predictive ability**, confirming that the model found a persistent, non-random signal in the highly volatile market data of 2023.

## Technologies Used

-   **Languages:** Python
-   **Libraries:** Pandas, Scikit-learn, XGBoost, Optuna

## How to Run This Project

1.  Clone the repository:
    ```bash
    git clone [Your Repository URL]
    ```
2.  Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
3.  Set up your Binance API key in the configuration file.
4.  Run the main data ingestion and training script:
    ```bash
    python main.py
    ```
