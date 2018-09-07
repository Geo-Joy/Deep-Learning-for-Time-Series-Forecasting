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
- m parameter influences the P , D, and Q parameters.

For example:
- m of 12 for monthly data suggests a yearly seasonal cycle.
- P = 1 would make use of the first seasonally offset observation in the model, e.g. t − (m × 1) or t − 12.
- P = 2, would use the last two seasonally offset observations t − (m × 1), t − (m × 2).
- D of 1 would calculate a first order seasonal difference.
- Q = 1 would use a first order errors in the model

## Exponential Smoothing Methods
- Exponential smoothing is a time series forecasting method for univariate data\
- Prediction is a weighted sum of past observations
- Exponential smoothing methods may be considered as peers and an alternative to the popular Box-Jenkins ARIMA class of methods
- Sometimes referred to as ETS models, referring to the explicit modeling of Error, Trend and Seasonality

### Single Exponential Smoothing
- SES for short, also called Simple Exponential Smoothing, is a time series forecasting method for univariate data without a trend or seasonality.
- It requires a single parameter, called alpha (a or α), also called the smoothing factor or smoothing coefficient
- Alpha is often set to a value between 0 and 1
- Alpha value close to 1 indicates fast learning (that is, only the most recent values influence the forecasts)
- Alpha value close to 0 indicates slow learning (past observations have a large influence on forecasts)

 - **Alpha (α):** Smoothing factor for the level.
 
### Double Exponential Smoothing
- Explicitly adds support for trends in the univariate time series
- An additional smoothing factor is added to control the decay of the influence of the change in trend called beta (b or β)
- supports trends that change in different ways: an additive and a multiplicative
- Double Exponential Smoothing with an additive trend is classically referred to as Holt’s linear trend model (Charles Holt)

- **Additive Trend:** Double Exponential Smoothing with a linear trend.
- **Multiplicative Trend:** Double Exponential Smoothing with an exponential trend.

For longer range (multi-step) forecasts, the trend may continue on unrealistically. As such, it can be useful to dampen the trend over time. Dampening means reducing the size of the trend over future time steps down to a straight line (no trend).

- **Additive Dampening:** Dampen a trend linearly.
- **Multiplicative Dampening:** Dampen the trend exponentially.

#### Hyperparameters:
- **Alpha (α):** Smoothing factor for the level.
- **Beta (β):** Smoothing factor for the trend.
- **Trend Type:** Additive or multiplicative.
- **Dampen Type:** Additive or multiplicative.
- **Phi (φ):** Damping coefficient.

### Triple Exponential Smoothing
- Triple Exponential Smoothing is an extension of Exponential Smoothing that explicitly adds support for seasonality to the univariate time series. 
- This method is sometimes called Holt-Winters Exponential Smoothing, named for two contributors to the method: Charles Holt and Peter Winters.
- gamma (g or γ) that controls the influence on the seasonal component.

- **Additive Seasonality:** Triple Exponential Smoothing with a linear seasonality.
- **Multiplicative Seasonality:** Triple Exponential Smoothing with an exponential seasonality

- Triple exponential smoothing is the most advanced variation of exponential smoothing and through configuration, it can also develop double and single exponential smoothing models.

- Additionally, to ensure that the seasonality is modeled correctly, the number of time steps in a seasonal period (Period) must be specified. For example, if the series was monthly data and the seasonal period repeated each year, then the Period=12.

#### Hyperparameters:
- **Alpha (α):** Smoothing factor for the level.
- **Beta (β):** Smoothing factor for the trend.
- **Trend Type:** Additive or multiplicative.
- **Dampen Type:** Additive or multiplicative.
- **Phi (φ):** Damping coefficient.
- **Gamma (γ):** Smoothing factor for the seasonality.
- **Seasonality Type:** Additive or multiplicative.
- **Period:** Time steps in seasonal period.

### Further Reading
#### Simple Methods
- [Chapter 2, The forecaster’s toolbox, Forecasting: Principles and Practice, 2013.](https://amzn.to/2xlJsfV)
- [Forecasting, Wikipedia.](https://en.wikipedia.org/wiki/Forecasting)

#### Autoregressive Methods
- [Chapter 8, ARIMA models, Forecasting: Principles and Practice, 2013.](https://amzn.to/2xlJsfV)
- [Chapter 7, Non-stationary Models, Introductory Time Series with R, 2009.](https://amzn.to/2smB9LR)
- [Autoregressive integrated moving average on Wikipedia.](https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average)

#### Exponential Smoothing
- [Chapter 7, Exponential smoothing, Forecasting: Principles and Practice, 2013.](https://amzn.to/2xlJsfV)
- [Section 6.4. Introduction to Time Series Analysis, Engineering Statistics Handbook, 2012.](https://www.itl.nist.gov/div898/handbook/)
- [Practical Time Series Forecasting with R, 2016.](https://amzn.to/2LGKzKm)
- [Exponential smoothing, Wikipedia.](https://en.wikipedia.org/wiki/Exponential_smoothing)
 


