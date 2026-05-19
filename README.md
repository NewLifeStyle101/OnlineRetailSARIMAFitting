# OnlineRetailSARIMAFitting
## Project Overview
This project extends the previous ARIMA forecasting model by introducing SARIMA to evaluate wether seasonal components improve weekly revenue forecasting.

Multiple seasonal periods were tested and compared against the ARIMA baseline using both MAE and RMSE metrics
## Previous Work
- ARIMA: https://github.com/NewLifeStyle101/OnlineRetailARIMAFitting
- EDA: https://github.com/NewLifeStyle101/OnlineRetailEDA
## Dataset
- Name: Online Retail Dataset
- Source: UCI Machine Learning Repository
- Time Period: December 2010 until December 2011
- Link: https://archive.ics.uci.edu/dataset/352/online+retail
### Description:
- InvoiceNo which is a 6 digit number assigned to each transaction if it starts with a c it represents a cancellation
- StockCode a 5 digit number unique to each distinct product
- Description which is the product name
- Quantity represents the quantity sold per invoice
- InvoiceDate is the day and time when each transaction has been generated
- UnitPrice is the price of the product per unit
- CustomerID is a 5 number unique identifier assigned to each customer
- Country is the name of the country the customer resides
### Feature Engineering:
Revenue = Quantity x UnitPrice
## Methodology
### Revenue Aggregation
Weekly aggregation was used on the transactional data to create a time-series suitable for forecasting
### Transformations
Log transformation and first-order differencing were applied to stabilize the variance and to achieve a stationary time series
### SARIMA
Multiple seasonal periods (4, 8, 12 weeks) have been evaluated using SARIMA models and comparing them to the ARIMA baseline using MAE and RMSE metric.
## Models Tested
- SARIMA (0,1,1)(1,0,0,4)
- SARIMA (0,1,1)(1,0,0,8)
- SARIMA (0,1,1)(1,0,0,12)
## Results
## Key Insights
## Limitations
## Future Work
## Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels


