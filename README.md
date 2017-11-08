# ARIMA and LSTM Time Series Models for Google Trends
### Overview
This project sought to compare Autoregressive Integrated Moving Average (ARIMA) and Long Short-Term Memory (LSTM) models for various time series data. I created generalized functions that could quickly test, iterate, and optimize ARIMA and LSTM models for a given time series input. The general models were used to forecast various trends, including:
- S&P 500 historical data
- "LeBron James" Google Trends
- "Coldbrew" Google Trends
- "Kentucky Derby" Google Trends
- "Gilmore Girls" Google Trends
- "Olympics" Google Trends
- "Zika Virus" Google Trends

I chose these various trends based on their unique shapes to test a variety of seasonality changes, increasing values over time, and sharp disparities. Each section contains a plot of the original data, followed by out-of-sample testing results. 

Further, I included results that used gaussian filtering to smooth the original dataset, followed by modeling of the smoothed dataset. The smoothed modeling results were compared to the original series data to determine whether the filtering improved performance of the models.

### Key Questions Explore
Given a wide range of time series data sets,
- Which model performed better at prediction out-of-sample data: ARIMA or LSTM?
- Does gaussian filtering improve the model results on the original, un-filtered dataset? 

### Key Findings
- The ARIMA model gave lower root mean squared errors (RMSEs) in 5/7 of the studied time series compared to the LSTM model. In many cases, the models gave similar errors, but on the whole, ARIMA provided higher-quality results, though it struggled to converge on a few series.
- Gaussian filtering the dataset prior to creating the model gave lower errors in every case, even when comparing the model results to the original, unfiltered data. On average, the Gaussian filtered predictions reduced the RMSE by close to 100%.


- Average RMSEs for unfiltered data, ARIMA: 21.69 & LSTM: 23.54
- Average RMSEs for Gaussian filtered data, ARIMA: 10.98 & LSTM: 12.22


### Techniques used
- time series analysis and forecasting
- pandas and numpy for datetime, data preparation
- statsmodel and keras for ARIMA and LSTM modeling
