# ProfitsRUS

# Project Background

Performance of the Stock market is based on both human sentiments and basic math. With the help of a strong algorithm and machine learning we want to combine and predict human sentiment as well as compute mathematical data to provide a benchmark for stock investment. 

# Project Goal
We are trying to create an algorithm that will signal a Buy, Sell or Hold (Step 1). Additionally we will create a ML Model that will make predictions for a set of stock tickers and then evaluate it against historical data (Step 2). 

# Contributors
- Puneeth Nimmagadda
        - Step 1 and Presentation
- Aman Gill
        - Step 2 and Presentation
- Andrey Kotovets
        - Step 2 and Presentation

# Data Collection

Data will be collected for a set number of stocks from an API service (example Yahoo Finance). At a minimum, We are going to collect the following:
- Price-to-Earnings Ratio
- Price-to-Book Ratio
- Debt-to-Equity Ratio
- Free Cash Flow
- PEG Ratio
- Payout ratio
- Beta
- Return on equity (ROE)
- Free cash flow

# Data Cleaning

We are not expecting data to be readily useful and it will need to be cleaned. A few examples are:
- Date Formats: Date should be in 'YYYY-MM-DD' format
- Number: Any numbers stored as text are not ready for calculations.
- Nulls: We need to drop or analyse rows that have nulls.
- Invalid or Corrupt data: We do not want our models to use invalid data and hence those rows will be dropped as well.
- Outliers: We will need to analyse and review how outliers are impacting our core data.

# Modules/Libraries

It is hard to predict what challenges we will face during our analysis and thus, we cannot rule out any python library that help us achieve our goal. But based on our high level project details, we are planning on using the following libraries:
- numpy
- pandas
- matplotlib
- Scipy
- yfinance
- math
- finta
- prophet
- mplfinance
- SQl
- postgres
- pgadmin

# High level data flow
## Download Data
- Download data from yahoo_finance and finta - one ticker based on user input (MSFT)
    -  RSI, MACD
- Save as CSV
## Calculate new fields
-   SMA 20 & 50
-   Volume Avg 10
## ML
- User prophet to predict timeseries for next 10 business days
- use a combination of regressors to create diff prediction models
- compare with actual stock price in those 10 business days (we are using 2021 data to predict first 10 days in 2022)
## Calculate Predictors (Buy/Sell/Hold)
-   Based on SMA and Volume

# Final Summary

