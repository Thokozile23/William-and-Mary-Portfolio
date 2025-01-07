**Project Overview**

In our Stochastic modelling-driven stock pitch presentation, we analyzed Ford's investment projections over the next 10 years. Using R, we built a simulation model to evaluate potential outcomes under three scenarios: Bear Case, Base Case, and Bull Case. The simulations incorporated macroeconomic factors, including rising interest rates, recession expectations, and the intense competition within the electric vehicle market.The aim of the project was to determine whether investing in Ford would be a safe and profitable decision.

**Model Selection**

While model fitting, we used the forecasting models learned in class and fitted them to the training data. We used TSLM, TSLM2, ETS, and ARIMA.
TSLM is a linear regression model that allows you to look at trends and seasonality. We are able to see if there are periods where there are more/less sales, or higher/lower stock prices during the set period.
TSLM2, in our case allows us to see a time-based trend. the I(trend()^2) allows for flexibility in modeling the trend. It
**Ford Stock Final Presentation**
accounts for the possibility that the relationship between the variable and time may not be linear.
ETS captures error, trend, and seasonality. It is useful when you want to model time series data with explicit attention to trend and seasonality but without external predictors.
ARIMA looks at how past values and data can influence future ones (autocorrelation). It is useful for making accurate forecasts when the data shows patterns of autocorrelation but may not have strong seasonality.


![Alt Text](https://github.com/Thokozile23/William-and-Mary-Portfolio/blob/3756aa5b00e29685f8867fea7c5cdda1c6a0b549/ford%20graph1.png)

This graph shows the 5 month forecast for Ford's stock price using an ETS model. The confidence intervals are represented by shaded regions. The historical stock prices are plotted from 2014 to 2024, showing a significant spike around 2020, followed by a stabilization period. The forecast shows a prediction with uncertainty as represented by the widening bands, illustrating potential variability in the stock price over the forecast period.



![Alt Text](https://github.com/Thokozile23/William-and-Mary-Portfolio/blob/67cb16b665faf1aa0036afa1497ce81ef6bdbf19/ford%20graph2.png)
This graph also represents a 5-month forecast of Ford vehicle sales using an ETS model. The plot displays the number of vehicles sold over time, with a forecast for the upcoming months. The solid line shows the historical data from 2014-2024, which shows a pattern and variability over time. Once again, around 2020, we see a dip in sales, followed lower variability, then by a sharp increase near 2025.

**Expected Outcome**

Based on our analysis, we anticipate the Base Case scenario to unfold, where there is no significant growth in Ford’s stock due to mounting macroeconomic pressures and market competition.

**Recommendation**

Our findings suggest that our team should not invest in Ford’s stock. The Base Case simulations revealed that 50% of the outcomes resulted in a final investment value of $1,886.07, which is less than the total contributions, signaling a lack of favorable returns

