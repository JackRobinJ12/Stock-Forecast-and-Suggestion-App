Stock Forecast and Suggestion App

Overview

The Stock Forecast and Suggestion App is a Streamlit-based application that allows users to visualize historical stock data, predict future trends using the Prophet model, and receive stock suggestions based on moving averages. The app also compares selected stocks against the S&P 500 benchmark to help users make informed investment decisions.

Features

Stock Selection: Users can select from a predefined list of stocks for forecasting.

Interactive Data Visualization: Displays historical stock prices and forecasts using Plotly.

Stock Price Prediction: Uses Facebook's Prophet model to predict future stock prices.

S&P 500 Benchmark Comparison: Plots selected stock prices against the S&P 500 ETF (SPY).

Stock Suggestion Module: Identifies stocks that are trending upwards based on moving averages.

User Customization: Users can select the number of years for forecasting (1 to 4 years).

Installation

To run the app, install the required dependencies:

pip install streamlit prophet yfinance plotly pandas

Usage

Run the Streamlit app using:

streamlit run app.py

How It Works

Loading Stock Data: The app fetches stock data from Yahoo Finance.

Data Visualization: Displays raw stock data and an interactive price chart.

Forecasting with Prophet: Trains a Prophet model and generates future predictions.

Benchmark Comparison: Compares the selected stock's performance with the S&P 500.

Stock Suggestions: Identifies stocks trending above their 30-day moving average.

Technologies Used

Python: Main programming language.

Streamlit: For building the interactive web app.

Prophet: For time series forecasting.

Yahoo Finance (yfinance): For retrieving stock market data.

Plotly: For creating interactive visualizations.

Pandas: For data manipulation.

Stock Prediction Model

The app utilizes Facebook's Prophet model, which is a robust time series forecasting tool. It automatically detects trends and seasonality in stock prices to generate future predictions.

Stock Suggestion Algorithm

The app fetches the last 60 days of stock data and calculates the 30-day moving average. If the latest stock closing price is higher than its moving average, the stock is suggested as trending upwards.

Notes

The app retries fetching stock data up to 3 times in case of failures.

A small delay is added between API calls to prevent rate limiting.

If no data is available for a stock, a warning is displayed.

Future Enhancements

Allow users to enter custom stock symbols.

Implement additional forecasting models for comparison.

Provide real-time stock alerts and notifications.

License

This project is for educational purposes. Feel free to modify and enhance it!

Author

Jack Robin J


