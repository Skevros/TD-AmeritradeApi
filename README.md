# TD-Ameritrade-Bot

Project Scope: The objective of this project is to develop a TD Ameritrade trading bot capable of executing simulated trades using real historical data obtained through API requests. The bot will calculate the following indicators based on the retrieved historical candles/data:

- Simple Moving Average (SMA)
- Exponential Moving Average (EMA)
- Relative Strength Index (RSI)

Then the trading strategies (1-4) selected will be used to perform a simulated trade, which then shows the gain/loss of the trade strategy.

<b><i><u>NOTE:</b></i></u> In order to fetch actual candles/data from TD Ameritrade, the user will need to enter their API key + access token (mines is for my personal use :P) in the 'config.json' file.</br></br>
TD Ameritrade API setup link to create API key + access token: https://developer.tdameritrade.com/content/getting-started

Replace the following key/value pairs with your API key + access token values:</br>

<b><i>"apiKey": "enter your tdameritrade api key",</b></i></br>
<b><i>"accessToken": "enter your tdameritrade access token"</b></i>

If an API key or access token is not provided, the request to retrieve data from TD Ameritrade will fail, resulting in a 500 status code. In such a scenario, the program will default to using the included dummy/test data (TSLA-10day-5min.json) for mock testing purposes.

To run the program, execute the main.py file. Upon running the program, the user will be prompted to input a stock ticker symbol. Subsequently, a menu for trade strategy selection will be displayed. Once the user makes a selection, the calculated EMA/RSI indicator values will be presented, along with simulated trade transactions. Finally, the net gain/loss will be displayed based on the simulated trades.

<pre>
+-----------------------------------------------+
|               Trading Strategies              |
+-----------------------------------------------+
|                                               |
Baseline: Trade when RSI reaches the level of 50.
EMA only: Trade using the EMA indicator exclusively.
RSI only: Trade based on the most recent RSI level.
EMA + RSI: Trade using both the EMA and RSI levels.       
|                                               |
+-----------------------------------------------+
|           Select a trading strategy           |
+-----------------------------------------------+

