## How to Develop a Skillful Forecasting Model
*“Here is a dataset, now develop a forecast.”*

### After reading this tutorial, you will know:
- A systematic four-step process that you can use to work through any time series forecasting problem.
- A list of models to evaluate and the order in which to evaluate them.
- A methodology that allows the choice of a final model to be defensible with empirical evidence, rather than whim or fashion.

### The Situation
You are handed data and told to develop a forecast model. What do you do? This is a common situation; far more common than most people think.
- Perhaps you are sent a CSV file.
- Perhaps you are given access to a database.
- Perhaps you are starting a competition.

The problem can be reasonably well defined:
- You have or can access historical time series data.
- You know or can find out what needs to be forecasted.
- You know or can find out how what is most important in evaluating a candidate model.

So how do you tackle this problem? Unless you have been through this trial by fire, you will struggle.
- You may struggle because you are new to the fields of machine learning and time series.
- You may struggle even if you have machine learning experience because time series data is different.
- You may struggle even if you have a background in time series forecasting because machine learning methods may outperform the classical approaches on your data.


### Step 1: Define Problem
1. Inputs vs. Outputs: What are the inputs and outputs for a forecast?
2. Endogenous vs. Exogenous: What are the endogenous and exogenous variables?
3. Unstructured vs. Structured: Are the time series variables unstructured or structured?
4. Regression vs. Classification: Are you working on a regression or classification predictive modeling problem? What are some alternate ways to frame your time series forecasting problem?
5. Univariate vs. Multivariate: Are you working on a univariate or multivariate time series problem?
6. Single-step vs. Multi-step: Do you require a single-step or a multi-step forecast?
7. Static vs. Dynamic: Do you require a static or a dynamically updated model?
8. Contiguous vs. Discontiguous: Are your observations contiguous or discontiguous?

Some useful tools to help get answers include:
- Data visualizations (e.g. line plots, etc.).
- Statistical analysis (e.g. ACF/PACF plots, etc.).
- Domain experts.
- Project stakeholders.

### Step 2: Design Test Harness
Design a test harness that you can use to evaluate candidate models.
Below is a common time series forecasting model evaluation scheme
1. Split the dataset into a train and test set.
2. Fit a candidate approach on the training dataset.3.6.
3. Make predictions on the test set directly or using walk-forward validation.
4. Calculate a metric that compares the predictions to the expected values.

### Step 3: Test Models
1. Baseline. Simple forecasting methods such as persistence and averages.
2. Autoregression. The Box-Jenkins process and methods such as SARIMA.
3. Exponential Smoothing. Single, double and triple exponential smoothing methods.
4. Linear Machine Learning. Linear regression methods and variants such as regularization.
5. Nonlinear Machine Learning. kNN, decision trees, support vector regression and more.
6. Ensemble Machine Learning. Random forest, gradient boosting, stacking and more.
7. Deep Learning. MLPs, CNNs, LSTMs, and Hybrid models.

The more time and resources that you have, the more configurations that you can evaluate. For example, with more time and resources, you could:
- Search model configurations at a finer resolution around a configuration known to already perform well.
- Search more model hyperparameter configurations.
- Use analysis to set better bounds on model hyperparameters to be searched.
- Use domain knowledge to better prepare data or engineer input features.
- Explore different potentially more complex methods.
- Explore ensembles of well performing base models.

Some data preparation schemes to consider include:
- Differencing to remove a trend.
- Seasonal differencing to remove seasonality.
- Standardize to center.
- Normalize to rescale.
- Power Transform to make normal.

This large amount of systematic searching can be slow to execute. Some ideas to speed up the evaluation of models include:
- Use multiple machines in parallel via cloud hardware (such as Amazon EC2).
- Reduce the size of the train or test dataset to make the evaluation process faster.
- Use a more coarse grid of hyperparameters and circle back if you have time later.
- Perhaps do not refit a model for each step in walk-forward validation.

### Step 4: Finalize Model
- At the end of the previous time step, you know whether your time series is predictable. If it is predictable, you will have a list of the top 5 to 10 candidate models that are skillful on the
problem. You can pick one or multiple models and finalize them. This involves training a new final model on all available historical data (train and test).
- Make a prediction for the future.
- Save the model to file for later use in making predictions.
- Incorporate the model into software for making predictions.

You can always circle back to the previous step and see if you can further improve upon the final model. This may be required periodically if the data changes significantly over time.


### Further Reading
- [Forecasting: principles and practice, 2013.](http://amzn.to/2lln93c)
- [Practical Time Series Forecasting with R: A Hands-On Guide, 2016.](http://amzn.to/2k3QpuV)
- [Statistical and Machine Learning forecasting methods: Concerns and ways forward, 2018.](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0194889)
