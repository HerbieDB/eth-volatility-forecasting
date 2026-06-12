# eth-volatility-forecasting
Rolling GARCH(1,1) volatility forecasts for ETH/USDT, evaluated against implied volatility derived from Binance ETH/USDT options.

## Overview
This project tests whether Chi & Hao's (2021) finding, that GARCH forecasts outperform options-derived implied volatility (IV) for ETH/USDT, extends to a later sample period (May 2023 to October 2023). I fit a GARCH(1,1) model to ETH/USDT returns with pre- and post-fit diagnostics, refitting on a daily rolling basis and evaluating out of sample against IV derived from end-of-hour options summaries. The evaluation extends the paper's methodology with a robust loss function (QLIKE) and formal significance testing with a Diebold-Mariano test.

## Key Findings
- Neither GARCH nor IV shows material forecasting power over the primary forecast window (Mincer-Zarnowitz adjusted R² near 0 for both)
- IV significantly outperforms GARCH on QLIKE (DM = 3.56, p < 0.01), contrasting Chi & Hao's result - though this may be due to the smoothness of the long-dated IV series in a period of relatively low volatility, rather than superior forecasting
- A sensitivity test over a more volatile 365-day window results in improved forecasting power (adjusted R² of 0.29, in line with Chi & Hao's 0.32), suggesting the primary forecast window results are regime-dependent.

## Viewing the Notebook
If viewing the Volatility_Project.ipynb notebook in github does not work, please try either:
1) pasting the notebook URL at [nbviewer.org](https://nbviewer.org)
2) opening the notebook in [Google Colab](https://colab.research.google.com/github/HerbieDB/eth-volatility-forecasting/blob/main/Volatility_Project.ipynb) (Note: do not click "Run all" as the file will not run without the required data files. All outputs are already in the file)
