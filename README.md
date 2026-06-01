# eth-volatility-forecasting
Rolling GARCH(1,1) volatility forecasts for ETH-USDT, evaluated against options implied volatility.

## Overview
This project fits a GARCH(1,1) model on ETH-USDT returns data from Binance, with pre and post-fit diagnostic tests. The model is then refit on a rolling basis and evaluated out of sample against implied volatility as derived from end of hour ETH-USDT options contract summaries on Binance.

## Viewing the Notebook
If viewing the Volatility_Project.ipynb notebook in github does not work, please try either:
1) pasting the notebook URL at [nbviewer.org](https://nbviewer.org)
2) opening the notebook in [Google Colab](https://colab.research.google.com/github/HerbieDB/eth-volatility-forecasting/blob/main/Volatility_Project.ipynb) (Note: do not click "Run all" as the file will not run. All outputs are already in the file)
