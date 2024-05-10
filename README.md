# StockHistoryRU
StockHistoryRU is a powerful and easy-to-use Python package designed to fetch historical stock data for any Russian company. Whether you're a financial analyst, a data scientist, or a casual investor, StockHistoryRU provides you with the tools you need to access and analyze historical stock data.

# Key Features

- **Comprehensive Coverage:** Covers all publicly traded companies in the Russian stock market, ensuring you have access to the data you need.

- **Flexible Date Range:** You can fetch historical data for any time period you want. Whether you need data from the last month or the last decade, StockHistoryRU has you covered.

- **Ease of Use:** Designed to be user-friendly. With just a few lines of code, you can fetch and analyze historical stock data.

- **Data Accuracy:** Fetches data directly from reliable sources, ensuring the accuracy and reliability of the data.

# Usage

**Example:** You can use code from **usage_of_stockhistoryru.ipynb**.

## Import Module
```python
import stockhistoryru as sh
```

## Getting All Available Russian Companies
```python
stocks_list = sh.get_all_stocks_list()
```

**Output:** The function returns a DataFrame with all Russian companies that trade on the stock market (or have ever traded)

![image](https://github.com/VladekQ/StockHistoryRU/assets/72941961/9271c1e4-a975-4ce2-9ed8-4d4144d61c24)

## Obtaining historical data on the stock prices of one company
```python
gazp_stocks = sh.get_stocks_history(
    start_date='2020-05-01',
    end_date='2024-05-07',
    symbol='GAZP'
)
```

**Output:** The function returns a DataFrame with historical data on stock prices of one company

![image](https://github.com/VladekQ/StockHistoryRU/assets/72941961/8b22cafe-5bc4-4843-b61c-369be3fef4d9)

## Obtaining historical data on the stock prices of multiple companies
```python
stocks = sh.get_stocks_list_history(
    start_date='2020-05-01',
    end_date='2024-05-07',
    symbols=['ROSN', 'GAZP']
)
```

**Output:** The function returns a dictionary with DataFrames with historical data on stock prices of multiple companies

![image](https://github.com/VladekQ/StockHistoryRU/assets/72941961/056c876f-c8ae-4203-b8e9-0e5c3d5df996)

![image](https://github.com/VladekQ/StockHistoryRU/assets/72941961/f4a651dc-373f-451e-91d4-6cae176db4df)


