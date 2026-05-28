# OnlineRetailSARIMAFitting
## Project Overview
This project extends the previous ARIMA forecasting model by introducing SARIMA to evaluate whether seasonal components improve weekly revenue forecasting.

Multiple seasonal periods were tested and compared against the ARIMA baseline using both MAE and RMSE metrics.
## Previous Work
- ARIMA: https://github.com/NewLifeStyle101/OnlineRetailARIMAFitting
- EDA: https://github.com/NewLifeStyle101/OnlineRetailEDA
## Dataset
- Name: Online Retail Dataset
- Source: UCI Machine Learning Repository
- Time Period: December 2010 until December 2011
- Link: https://archive.ics.uci.edu/dataset/352/online+retail
### Description:
- **InvoiceNo** - 6 digit transaction identifier. Transactions beginning with a c indicate a cancellation
- **StockCode** - 5 digit unique product identifier 
- **Description** - Product name
- **Quantity** - Number of units purchased
- **InvoiceDate** - Transaction timestamp
- **UnitPrice**  - Price per product unit
- **CustomerID** - 5 digit unique customer identifier 
- **Country** - Customer country of residence
### Feature Engineering:
Revenue = Quantity x UnitPrice
## Methodology
### Revenue Aggregation
Weekly aggregation was used on the transactional data to create a time-series suitable for forecasting.
### Transformations
Log transformation and first-order differencing were applied to stabilize the variance and to achieve stationarity.
### SARIMA
Multiple seasonal periods (4, 8, 12 weeks) have been evaluated using SARIMA models and compared to the ARIMA baseline using MAE and RMSE metric.
## Models Tested
- SARIMA (0,1,1)(1,0,0,4)
- SARIMA (0,1,1)(1,0,0,8)
- SARIMA (0,1,1)(1,0,0,12)
## Results
| Models | Seasonal Period | MAE | RMSE|
|--------|-----------------|-----|-----|
|ARIMA| None| 0.170 | 0.236|          
|SARIMA| 4| 0.171 | 0.240|
| **SARIMA**| 8| **0.159** | **0.216**|
|SARIMA| 12| 0.178 | 0.232|
- Seasonality has not been detected within the dataset
- SARIMA (0,1,1)(1,0,0,8) has beaten the previous ARIMA baseline based on both the RMSE and MAE scores
## Key Insights
## Limitations
## Future Work
## Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels


