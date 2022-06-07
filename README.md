# ProfitRUs

# Presentation
[ProfitRUs](https://public.tableau.com/app/profile/aman.s.gill/viz/ProfitRus/ProfitRus?publish=yes)

# Project Background

Performance of the Stock market is a complex subject but it is also based on basic math. With the help of a strong algorithm and machine learning, we want to compute mathematical data to provide a benchmark for stock investment.

# Project Goal
We are trying to create an algorithm that will signal a Buy, Sell or Hold (Step 1). Additionally we will create a ML Model that will make predictions for a stock ticker and then evaluate it against historical data (Step 2). 

# Contributors
- Aman Gill
        - Step 2 and Presentation
- Andrey Kotovets
        - Step 2 and Presentation
- Puneeth Nimmagadda
        - Step 1 and Presentation
        - Postgress SQL

# Data Collection

Data will be collected for a particular stock from available python libraries (example Yahoo Finance). We are going to collect the following attributes: 
- Open price
- Close price
- volume
- High for a calendar day
- Low for a calendar day
- MACD
- RSI
- TSI

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
- Download data from yahoo_finance and finta - one ticker based on user input.
- Export to a CSV file.
## Calculate new fields
-   SMA 20 & 50
-   Volume Avg 10
## ML
- User prophet to predict timeseries for next 10 business days in 2022.
- use a combination of regressors to create diff prediction models.
- compare with actual stock price in those 10 business days (we are using 2021 data to predict first 10 days in 2022).
## Calculate Predictors (Buy/Sell/Hold)
-   Based on SMA and Volume.
        We created an algoritham that produces a buy/sell/hold signal using a combination of SMA values and volume.

# Final Summary
ProfitRus is a product that suits any investment style (including short vs long). The only input that is needed is the stock ticker and the timeframe, based on which it produces meaningful graphical representation of where the stock might be headed. 
The functionality of the product can be improved by adding more regressors, thus making predictions more accurate.
