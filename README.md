# Detrending-a-time-series-using-log-t

Here I have data which had just 21 points. I detrended the time series by subtracting 'log(t)'. Then I fit a pure random walk(ARIMA(0,1,0)) on the remaining part.

Following are the steps:

1) Run a linear regression of Y_t (data) on log(t)
2) Subtract the log(t) (along with the slope coefficient) from log(t). This will leave error term from time series data.
3) Fit ARIMA(p,d,q) on error term.
4) Predicted Y_t= estimated intercept term from 1) + estimated coeff from 1) * log(t) + error term from 3)
