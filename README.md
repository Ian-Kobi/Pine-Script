## Pine-Script

These are all indicators coded in Pine Script. 
In order for these scripts to run, they must be copied and pasted into TradingView.com's native IDE, Pine Editor.

### Money Flow
This indicator tracks money flowing in and out of a security. Best used wtih Tick Data.

### Money Flow MTF 20 Min
This indicator attempts to "slightly" fix the problem of using Money Flow with traditional time-series data. It takes a time series
(in this stock data that is in increments of 20 mins) and slices the data up into an average of the sum of it's parts. This gives a more 
accurate representation of the money flow in real-time during that 20 minute time period.

To specifically describe the problem (and thus the solution here), if a stock closes lower in the span of 20 minutes then all of the money flow 
is marked as negative. But what if the stock had money flowing in for 19 minutes straight before it was hit with a ladder attack, other
spoofing, or plain retail panic selling? The original Money Flow indicator does not take this into account. By slicing up the total 20 minutes
into a sum of its parts, then we get a more accurate picture, albeit not a perfect one. For perfect accuracy, use tick data!

### Integrated Fractal Statistic

This is a synthesis of my knowledge in the various domains of Data Science, Chaos Theory, Fractal Geometry, Statistics, and practical 
trading experience. This indicator is an extension of statistical data analysis methods. However, standard statistical analysis methods 
assume stationary data and constant randomness. This is not true. Stock market time-series data is non-stationary and is selectively random 
as shown using fractal geometry methods. This Integrated Fractal Statistic Indicator provides two different means by which the state of 
randomness of the current data can be gauged. By monitoring the state of randomness of the data, we can then verify or invalidate the accuracy 
of our statistical indicators. 

This indicator plots an exponential linear regression using the R-squared method for fitted linear regression. Then to check the accuracy of our
regression, uses fractal geometry to calculate the fractal dimension of the time-series. It also uses Detrended Fluctuation Analysis to measure
the current state of randomness for our time-series. These can both then be used to determine the level of confidence we can have when deciding 
whether to follow our statistical forecasting.
