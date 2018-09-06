## How to Transform Time Series to a Supervised Learning Problem

In this section, you will discover how you can re-frame your time series problem as a supervised learning problem for machine learning.

### After reading this lesson, you will know:
- What supervised learning is and how it is the foundation for all predictive modeling machine learning algorithms.
- The sliding window method for framing a time series dataset and how to use it.
- How to use the sliding window for multivariate data and multi-step forecasting.

### Supervised Machine Learning
- It is called supervised learning because the process of an algorithm learning from the training dataset can be thought of as a teacher supervising the learning process.

Supervised learning is where you have input variables (X) and an output variable (y) and you use an algorithm to learn the mapping function from the input to the output.
> Y = f (X)
The goal is to approximate the real underlying mapping so well that when you have new input data (X), you can predict the output variables (y) for that data.
Supervised learning problems can be further grouped into regression and classification problems.
- Classification: A classification problem is when the output variable is a category, such as red and blue or disease and no disease.
- Regression: A regression problem is when the output variable is a real value, such as dollars or weight. The contrived example above is a regression problem.

### Sliding Window
- The use of prior time steps to predict the next time step is called the sliding window method. 
- For short, it may be called the window method in some literature.
- In statistics and time series analysis, this is called a lag or lag method.
- The number of previous time steps is called the window width or size of the lag.

### Sliding Window With Multiple Variates
- Univariate Time Series: These are datasets where only a single variable is observed at each time, such as temperature each hour. The example in the previous section is a univariate time series dataset.
- Multivariate Time Series: These are datasets where two or more variables are observed at each time.

### Sliding Window With Multiple Steps
- One-step Forecast: This is where the next time step (t+1) is predicted.
- Multi-step Forecast: This is where two or more future time steps are to be predicted.

### Further Reading
- [Multivariate Time Series Analysis: With R and Financial Applications, 2013.](https://amzn.to/2KD4rw7)
- [Machine Learning for Sequential Data: A Review, 2002.](https://link.springer.com/chapter/10.1007/3-540-70659-3_2)
- [Machine Learning Strategies for Time Series Forecasting, 2013.](https://link.springer.com/chapter/10.1007/978-3-642-36318-4_3)







