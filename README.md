
# Time Series Analysis of Basic Forcasting Technique

Time Series Analysis of Basic Forecasting Technique

The most interesting applications: -

Economic forecasting: -

Economic forecasting is the process of attempting to predict the future condition of the economy using a combination of widely followed indicators.

Sales forecasting: -

Sales forecasting is the process of estimating future sales.

Inventory Planning: -

Inventory planning includes creating forecasts to determine how much inventory should be on hand to meet consumer demand.

Workforce Planning: -

Workforce planning is the process of forecasting workforce supply and demand.

differences between Regression analysis and time series analysis.

As you already know In both Regression and Time series analysis we predict Continuous variables.
## Installation

-Pandas for analyzing data
- Numpy for math operations
- matplotlib. pyplot for data visualization
- seaborn for statistical graphics
- 'fivethirtyeight' for background
- warnings for awareness of the possible danger
warnings.filterwarnings('ignore')
## Contributing


Understand the difference between these two techniques.

Regression Analysis: -
Regression is a statistical method used for determining the relationship between the dependent variable and independent variables and predicting the continuous dependent variable.

Time series Analysis: -
Time series is simply a series of data points that has a time component involved in it.
-- It means every data point present in the dataset is associated directly with the date and time component.

The similarity between regression and time-series data is that the dependent variable or the target variable in both cases is of continuous type.

And the major difference between regression and time series is that the regression technique is used to find patterns in the data and use those patterns to predict the dependent variable.

On the other hand, a time series is used to identify trends in the data and then forecast future events.

And as you have so many variables to predict the price of the product, you would go with the 
regression technique.

Regression techniques help you to find the pattern in the data and predict the price of the new product based on the patterns present in the training data.

In Time series analysis we forecast the future sales, demand, temperature, number of customers/passengers, etc. based on the time.

Regression is about predicting the dependent variable based on the training dataset while time series is about forecasting future events based on past data.

Forecasting is the process of making predictions of the future, based on past, the present data and by analysis of trends.

There are two types of forecasting: -
Quantitative forecasting.

Qualitative forecasting.

Quantitative forecasting is based on past data which uses numerical measures and prior effects to predict future events.

This kind of forecasting is data-driven and hence has lesser bias.

Qualitative forecasting is done when you do not have much past data to perform any kind of statistical analysis on the data required for forecasting. 

As of now you know that you can not use any tools and techniques to perform qualitative forecasting The method used for performing qualitative forecasting is the Delphi method.

The Delphi method involves the subject matter experts, where these subject matter experts come together and discuss the subject to make significant decisions that are used for performing forecasting.

So, now you understand that whenever you have data you go for quantitative forecasting whereas 
If in any case, you do not have enough data, choose to go for qualitative forecasting.

A Time series data has 4 Major components.

Time series data have components because They can be decomposed into different factors which can be used to understand the Patterns from Time series data easily.

Different components in a time series include: -
- Level.
- Trend.
- Seasonality.
- Cyclicity.
- Noise.
Level: -
The level is the baseline for the entire time series. The level is the average of the time series and the baseline to which we add different other components. 

Trend: -
The trend is the indication of whether the time series has moved higher or lower over the long term. The graph shows the increasing trend over the time interval.

Seasonality: -
Seasonality is the pattern in time series that repeats after a fixed given interval of time.
The graph clearly shows the seasonality after every fixed interval of time.

Cyclicity: -
Cyclicity is the pattern in time series that repeats itself after some time but in the case of cyclicity, the interval of time is not fixed.

- One particular pattern may repeat after two months and then after about 6 months. 
- The graph shows the patterns but you can observe that the patterns repeat themselves after a random 
interval of time. 

Noise: -
Noise is the random variation in the time series. You cannot use noise to forecast the future.

Noise is just random fluctuations in your data and does not have any pattern.

Outliers are those values that can be very much extreme, and while preparing a Predictive Model.

If you feed a Data set having such outliers, then your Predictive model will get highly confused and will start producing biased results.

After knowing all these facts It becomes important for you to Handle these Outliers.

For Handling these outliers, first of all, you will need to detect them, for which you can use the Box Plot.

A boxplot is a standardized way of displaying the distribution of data.

Any data points which are less than Q1-1.5IQR or greater than Q3+1.5IQR are considered to be outliers.
## Documentation

Check for the outliers in your customer's dataset 
using a box plot: -

See that there are a few outliers in the dataset. And you must treat these outliers by capping their values because of the different ways of handling outliers and “capping outliers” is one of them.

There can be a situation that for some particular time there was more number of customers who visited the shop.

So, capping outliers turns out to be the best alternative as you can keep those observations in your analysis as well as get rid of outliers.

Some values are greater than 700 which seems to be outliers. So you will need to cap all such values to avoid overfitting in your Predictive Model.

Capping outliers is one of the methods of handling outliers which helps to replace the outliers with a maximum value that you can accept as a normal value.

Again plot the box plot to see how your box plot looks after the capping of all the outliers present in the data.

decompose the time series data into its various components. 
- The time series data contains some kind of pattern in them. 
- Decomposing a time series data into its different components helps to find their underlying pattern. 

This also improves the understanding of time series data. There are two ways of decomposing 

time series data: -
Additional Seasonal decomposition Multiplicative Seasonal decomposition Additional Seasonal 

decomposition: -
Additive Seasonal decomposition is when you add the individual components to get the time series data. 
Level+trend+seasonality+cyclicity+noise

Multiplicative seasonal decomposition: -
Multiplicative Seasonal decomposition is when you multiply the individual components to get the 

time series data. Example: - Leveltrendseasonalitycyclicitynoise

Prefer Additive Seasonal when the magnitude of the seasonal fluctuations does not vary with the level of the time series. 

Whereas you prefer using Multiplicative seasonal decomposition when the variation in the seasonal pattern appears to be directly proportional to the level of the time series data.

Check the Line plot of the Time series data and analyze whether it requires an additive seasonal decomposition or a multiplicative seasonal decomposition.

Notice the line plot carefully you can see that the seasonal components are growing as the level of time is increasing.

And Obviously for this case, prefer Multiplicative seasonal decomposition.
Try out Additive seasonal decomposition also, to 

understand how it is implemented in Python.
For time series decomposition, use the statsmodels package. Then, import the “TSA” module from the statsmodels package. 

After that import, the seasonal_decompose function and specify it as additive Write the code required for decomposing our time series data using additive seasonal decomposition.

Take a closer look and observe the different components of time series data.
- Represents the original data on which you want to perform decomposition.
- Represents the trend.
- Represents the seasonality.
- Represents the residual.

Residual is the leftover part after extracting trend and seasonality from the time series. There is an increasing trend in the time series. There is a fixed pattern for seasonality.

In residual, there is still some pattern in the data from 1949 to 1953 and after 1958. This means you can still do better using another decomposition method.
Try out the multiplicative seasonal decomposition. 

For the data set Multiplicative seasonal decomposition will be more suitable as the seasonal components in the time series grow directly proportional to the level of time.

You only change the model to be used and the rest of the things will remain the same.

Run the program and look at the output generated by the Multiplicative seasonal decomposition.

Observe that the trends show the increasing nature of the time series.

Seasonality captures the overall pattern of the time series data.

But this time there is no specific pattern in the residual part which means everything is captured by the trend and seasonality components of the time series data.

Go with Multiplicative seasonal decomposition because It is capturing most of the patterns from the time series data.

Different types of validation techniques: -
One-step validation Multi-Step validation First explores the one-step validation method used for splitting time series data.

In one-step validation: -
The test data is exactly after the train data. Have 10 data points, keep the first 6 data points as the train data and the rest of the 4 data points as the test data. 

The data points are taken one-by-one starting from the left. With 6 data points as the training data, forecast the 7th data point, and then with 7 data points as train data, forecast the 8th data point. Continue this until you forecast all 4 data points. 

Multi-step validation: -

Multi-step validation is similar to the one-step validation method. 

There is a difference that in the multi-step validation technique does not consider the exact next point after training data points. 
- Leave some data points in between to forecast well in the future. Try this in the jupyter notebook.
- Already treated all the missing values and outliers present in the time series. Also have decomposed the time series data into different components.

Going to split the data into training data and testing data.
- Keep the first 115 rows of the dataset as the training data and the remaining rows as the test data.
- Split the data into train data and test data successfully.
## Conclusion

Whenever the magnitude of the seasonal pattern in the data is not directly proportional to the series, prefer additive seasonal decomposition. Whereas, the magnitude of the seasonal pattern in the data is directly proportional to the series, preferring multiplicative seasonal decomposition.
