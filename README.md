## Data Science Project : US E-commerce Sales and Profit Forecasting with SARIMA and FBProphet Overview
* Build a tool to forecast snd predict the trend and value of sales and profit of one of US E commerce.
* Dataset contains records of E commerce succesful sales from january 2015 to december 2015
* Feature Engineered date feature to date time type for easier to converto data to to time series.
* Data Exploration giving a better understanding which products sold the most, generates most profit and where the sales / pofit mostly comes from.
* Auto ARIMA and FBProphet as tool to forecast sales and profit of the dataset.

### Code and Resource Used
* **Packages** : pandas, numpy, matplotlib, seaborn, sci-kit learn, statsmodel, pmdarima, fbprphet.

### Data Cleaning
* I had to do a number of features cleaning as many features had _anomaly_ values. Features with _anomaly_ value to be cleaned include `Order Priority, Aging, Segment, Quantity, Region, Country, State, Shipping Cost`.
* Replaced _anomaly_ values with the most frequent occuring ones or with the median of respective faatures. Because some of those value are not interpretable, so it had to be removed fom dataset.
* Cross-checking to see if the data had already been cleaned.

### Feature Engineering
* Feature engineered `sales` and `profit` features as those 2 stil in object (string) type and had to transform them to numeric type.
* Feature engineered `date time` to extract which day of the week, weektype, which month, and which quarter of the year the month fall into, to get better insight to the dataset.
* Export the newly cleansed data to csv file.

### Exploratory Data Analysis Highlight
* Total Profit Product <br>

![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index6.png)

The left plot shows the top 20 products which are bought by the customers the most, / making much higher profit, where T-shirt, wacth, Running shoes, Jeans and Formal Shoes are amongst of the top 5. It is also understood that products which makes the most profit also fall into Fashion category as represented by the right plot. It is alligned with the previous plot.

* Total Profit Country / Region <br>

![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index7.png)

The left plot shows the top 20 country generating higher profit for the ecommerce. Again, United States top the chart just as i explained in the previous plot where customers are dominantly live in the US, So it is natural that the States also generates more profit for the Ecommerce. In the second place it is Australia, followed France and Mexico and third and fourth. While the right plot shows Region which generates higher profit for the ecomerce. Central and East are amongst the top, it is understood, because the two are parts of The United States.

* Profit and Sales Over the year of 2015 <br>

![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index.png)

### Stationary Time Series Checking
![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index10.png)

* DIckey Fuller Test Result
> Test Statistics                -18.936836 <br>
> p-value                          0.000000 <br>
> No. of lags used                 0.000000 <br>
> Number of observations used    364.000000 <br>

Result shows that our profit time seriers is stationary, indicated by the p value of less than 0.05 and a minus (-) value of test statistic.

### Log transformation Time Series

![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index8.png)

This is done to eliminate the trend of time series, while its is stationary, so trend component is basically non existent. However, this is to further flaten the standard deviation.

### AUTO ARIMA 
* Modeling <br>
![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index1.png)

Plot interpretation:
* Standardized residual: The residual errors fluctuate around a mean of zero and have a uniform variance.
* Histogram: The density plot suggest normal distribution with mean.
* Theoretical Quantiles: Mostly the dots fall perfectly in line with the red line. Any significant deviations would imply the distribution is skewed.
* Correlogram: The Correlogram, (or ACF plot) shows the residual errors are not autocorrelated (independences).

The model is good to forecast the serires.

* Forecasting <br>
![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index5.png)

### FBProphet
* Forecast <br>
![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index3.png)

* Components <br>
![alt text](https://github.com/ELSady/Bootcamp-Final-Project-US-E-commerce-Sales-and-Profit-Forecasting/blob/main/index4.png)

* FBProphet Forecast Components highlight:
* Theres an increasing trend when it comes to profit and sales for the next few months.
* Weekly seasonal, on average, sunday and wednesday are the days when profit and sales are all tme high during the week, but the opposite is true for thursday, friday and saturday.
