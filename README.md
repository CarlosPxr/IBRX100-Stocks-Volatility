# Stock Volatility Analysis
This script is designed to analyze the volatility of stocks listed in the Ibovespa index, utilizing data from Yahoo Finance. It retrieves the list of stocks from the Status Invest website, calculates their volatility over a specified window,
and outputs the most volatile stocks.

### Requirements
- Python 3.x
- cloudscraper library
- beautifulsoup4 library
- yfinance library
- pandas library

### Functionality
1. Disable Logging for yfinance:
The script disables logging for the yfinance library to avoid cluttered output.

2. Retrieve Ibovespa Stocks:
The obter_ativos_ibovespa function scrapes the Status Invest website to retrieve the current list of stocks in the Ibovespa index. The ticker symbols are adjusted to be compatible with Yahoo Finance by appending .SA.

3. Calculate Volatility:
The calcular_volatilidade function downloads the last 30 days of adjusted closing prices for a given ticker using yfinance, computes the daily returns, and then calculates the rolling standard deviation over the specified window to determine the volatility.

4. Manual Addition of Tickers:
Additional tickers can be manually added to the list.

5. Volatility Calculation and Ranking:
The script calculates the volatility for each stock and stores the results in a dictionary. The results are then converted to a DataFrame, sorted by volatility, and the top N most volatile stocks are selected and displayed.

### How to Use
Run the Script:
Simply execute the script to see the most volatile stocks from the Ibovespa index. The top 15 most volatile stocks will be printed.

### Customization
Window for Volatility Calculation:
You can change the window for the rolling standard deviation in the calcular_volatilidade function by modifying the window parameter.

### Number of Top Volatile Stocks:
Adjust the top_n variable to display a different number of top volatile stocks.

### Notes
Ensure you have a stable internet connection, as the script fetches data from online sources.
Be aware of the API rate limits imposed by Yahoo Finance.

### Author
Carlos Peixer
Feel free to contribute or report issues via the project's repository.
