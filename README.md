# Forecasting Net Pophet

MercadoLibre is the most popular e-commerce site in Latin America with over 200 million users. As a growth analyst, you have been tasked with analyzing the company's financial and user data in clever ways to make the company grow. You want to find out if the ability to predict search traffic can translate into the ability to successfully trade the stock. To achieve this goal, you have been given the following instructions divided into four steps and an optional fifth step.

#### Step 1: Find Unusual Patterns in Hourly Google Search Traffic
You need to find out if there is any relationship between Google search traffic for the company and any financial events at the company. To accomplish this task, follow these steps:

Read the search data into a DataFrame and slice the data to just the month of May 2020, and then use hvPlot to visualize the results. Do any unusual patterns exist?
Calculate the total search traffic for the month and compare the value to the monthly median across all months. Did the Google search traffic increase during the month that MercadoLibre released its financial results?

#### Step 2: Mine the Search Traffic Data for Seasonality
You want to mine the search traffic data for predictable seasonal patterns of interest in the company to enable Marketing to focus their marketing efforts around the times that have the most traffic. Here are the steps to follow:

Group the hourly search data to plot the average traffic by the day of the week.
Using hvPlot, visualize this traffic as a heatmap, referencing the index.hour as the x-axis and the index.dayofweek as the y-axis. Does any day-of-week effect that you observe concentrate in just a few hours of that day?
Group the search data by the week of the year. Does the search traffic tend to increase during the winter holiday period?

#### Step 3: Relate the Search Traffic to Stock Price Patterns
You want to find out if there is any relationship between the search data and the company stock price. Here are the steps to follow:

Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.
Slice the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then use hvPlot to plot the data. Do both time series indicate a common trend that’s consistent with this narrative?
Create a new column in the DataFrame named “Lagged Search Trends” that offsets the search traffic by one hour. Create two additional columns: “Stock Volatility,” which holds an exponentially weighted four-hour rolling average of the company’s stock volatility, and “Hourly Stock Return,” which holds the percent change of the company's stock price on an hourly basis.
Review the time series correlation, and then answer the following question: Does a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?

#### Step 4: Create a Time Series Model with Prophet
You need to produce a time series model that analyzes and forecasts patterns in the hourly search data. Here are the steps to follow:

Set up the Google search data for a Prophet forecasting model.
After estimating the model, plot the forecast. How's the near-term forecast for the popularity of MercadoLibre?
Plot the individual time series components of the model to answer the following questions:
What time of day exhibits the greatest popularity?
Which day of the week gets the most search traffic?
What's the lowest point for search traffic in the calendar year?
