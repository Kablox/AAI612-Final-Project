# Seeing the Market: Predicting Stock Price Direction from Chart Images

Final project for AAI612: Deep Learning & its Applications.

Every 20 trading days of a stock are drawn as a small black and white price chart, and a ConvNet predicts if the price will be higher or lower 5 trading days later. The ConvNet is compared with simple baselines, an LSTM that reads the same data as numbers, and a frozen pretrained ResNet50. The chart format follows Jiang, Kelly and Xiu, "(Re-)Imag(in)ing Price Trends", The Journal of Finance, 2023.

## Run it

Open the notebook in Google Colab with a GPU runtime (Runtime > Change runtime type > T4 GPU) and run all cells:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Kablox/AAI612-Final-Project/blob/main/AAI612_FinalProject.ipynb)

The notebook loads the dataset directly from this repository, so nothing has to be uploaded.

## Dataset

`data/stock_prices.csv` has the daily prices of 50 large US companies from 2009-12-01 to 2024-12-31 (3,796 trading days each, 189,800 rows).

| Column | Meaning |
|---|---|
| Date | Trading day |
| Ticker | Stock symbol |
| Open, High, Low, Close | Daily prices in USD, adjusted for stock splits and dividends |
| Volume | Number of shares traded |

Source: Yahoo Finance, downloaded once with the [yfinance](https://github.com/ranaroussi/yfinance) library (`auto_adjust=True`).

## Files

| File | What it is |
|---|---|
| `AAI612_FinalProject.ipynb` | The project notebook |
| `data/stock_prices.csv` | The dataset |
