## Review of Simple and Classical Forecasting Methods

Machine learning and deep learning methods can achieve impressive results on challenging time series forecasting problems. Nevertheless, there are many forecasting problems where classical methods such as SARIMA and exponential smoothing readily outperform more sophisticated methods. Therefore, it is important to both understand how classical time series forecasting methods work and to evaluate them prior to exploring more advanced methods. In this tutorial, you will discover naive and classical methods for time series forecasting.

### After reading this lesson, you will know:
- How to develop simple forecasts for time series forecasting problems that provide a baseline for estimating model skill.
- How to develop autoregressive models for time series forecasting.
- How to develop exponential smoothing methods for time series forecasting.

### Forecast Performance Baseline
- A baseline in forecast performance provides a point of comparison.
- If a model achieves performance at or below the baseline, the technique should be fixed or abandoned.
- The goal is to get a baseline performance on your time series forecast problem as quickly as possible so that you can get to work better understanding the dataset and developing more advanced models.

Three properties of a good technique for making a naive forecast are:
- Simple: A method that requires little or no training or intelligence.
- Fast: A method that is fast to implement and computationally trivial to make a prediction.
- Repeatable: A method that is [deterministic](https://g.co/kgs/2LmQcr), meaning that it produces an expected output given the same input.


## Autoregressive Methods
Autoregressive Integrated Moving Average, or ARIMA, is one of the most widely used forecasting methods for univariate time series data forecasting.
- Can handle data with a trend
- Does not support time series with a seasonal component

An extension to ARIMA that supports the direct modeling of the seasonal component of the series is called SARIMA

### Autoregressive Integrated Moving Average Model
- Is a class of statistical models for analyzing and forecasting time series data

- **AR:** Autoregression. A model that uses the dependent relationship between an observation and some number of lagged observations.
- **I:** Integrated. The use of differencing of raw observations (e.g. subtracting an observation from an observation at the previous time step) in order to make the time series stationary.
- **MA:** Moving Average. A model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations.
> ARIMA(p,d,q)

### Seasonal ARIMA
- It is an extension of ARIMA that explicitly supports univariate time series data with a seasonal component
- Configuring a SARIMA requires selecting hyperparameters for both the trend and seasonal elements of the series.

#### Trend Elements
- **p:** Trend autoregression order.
- **d:** Trend difference order.
- **q:** Trend moving average order.

#### Seasonal Elements
- **P:** Seasonal autoregressive order.
- **D:** Seasonal difference order.
- **Q:** Seasonal moving average order.
- **m:** The number of time steps for a single seasonal period.
> SARIMA(p,d,q)(P,D,Q)m





