## Data Science Project : US E-commerce Sales and Profit Forecasting with SARIMA and FBProphet Overview
* Build a tool to forecast snd predict the trend and value of sales and profit of one of US E commerce.
* Dataset contains records of E commerce succesful sales from january 2015 to december 2015
* Feature Engineered date feature to date time type for easier to converto data to to time series.
* Data Exploration giving a better understanding which products sold the most, generates most profit and where the sales / pofit mostly comes from.
* Auto ARIMA and FBProphet as tool to forecast sales and profit of the dataset.

### Code and Resource Used
* **Packages** : pandas, numpy, matplotlib, seaborn, sci-kit learn, statsmodel, pmdarima, fbprphet.

### Data Cleaning
* I had to do a number of features cleaning as many features had _anomaly_ values. Had to replace those values to their appropiate value and types. Features with _anomaly_ value to be cleaned include 'Order Priority','Aging','Segment','Quantity','Region','Country','State','Shipping Cost'.
