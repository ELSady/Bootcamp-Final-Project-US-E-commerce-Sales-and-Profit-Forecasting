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
* Feature engineered sales and profit features as those 2 stil in object (string) type and transform them to numeric type.
* Feature engineered date time to extract which day of the week, weektype, which month, and which quarter of the year the month fall into, to get better insight to the dataset.
* Export the newly cleansed data to csv file.
*
### Exploratory Data Analysis Highlight
* Customer and Segment Distribution <br>

The first plot shows the country with most the customers, here there are United States followed by Australia and the France. For united State, it is understood why many customer come from the country, becuse the Ecommerce where the dataset is from is US based ecommerce. So then, it is natural the majority comes from the United States. While the second plot shows the customer segmentation, it is dominantly consumer who bought from the ecommerce followed by corporate and then home office in third.

* Product Distribution <br>

It is clear as a day, the products bought the most by the customers falls in to the fashion category. THe demand for those product are relatively high compared to others.

* Total Profit Product <br>

The left plot shows the top 20 products which are bought by the customers the most, / making much higher profit, where T-shirt, wacth, Running shoes, Jeans and Formal Shoes are amongst of the top 5. It is also understood that products which makes the most profit also fall into Fashion category as represented by the right plot. It is alligned with the previous plot.

* Total Profit Country / Region <br>

The left plot shows the top 20 country generating higher profit for the ecommerce. Again, United States top the chart just as i explained in the previous plot where customers are dominantly live in the US, So it is natural that the States also generates more profit for the Ecommerce. In the second place it is Australia, followed France and Mexico and third and fourth. While the right plot shows Region which generates higher profit for the ecomerce. Central and East are amongst the top, it is understood, because the two are parts of The United States.

### Modeling
