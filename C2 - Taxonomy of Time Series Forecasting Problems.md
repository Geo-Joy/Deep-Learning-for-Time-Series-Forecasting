## Taxonomy of Time Series Forecasting Problems
- In this chapter you will discover a framework that you can use to quickly understand and frame your time series forecasting problem.

### After reading this tutorial, you will know:
- A structured way of thinking about time series forecasting problems.
- A framework to uncover the characteristics of a given time series forecasting problem.
- A suite of specific questions, the answers to which will help to define your forecasting
problem.

### Probable Questions before starting a Time Series Forcasting Problem
- What are the inputs and outputs for a forecast?
- What are the endogenous and exogenous variables?
- Are you working on a regression or classification predictive modeling problem?
- What are some alternate ways to frame your time series forecasting problem?
- Are the time series variables unstructured or structured?
- Are you working on a univariate or multivariate time series problem?
- Do you require a single-step or a multi-step forecast?
- Do you require a static or a dynamically updated model?
- Are your observations contiguous or discontiguous?

**Time series forecasting involves developing and using a predictive model on data where there is
an ordered relationship between observations**

### Inputs vs. Outputs
- Generally, a prediction problem involves using past observations to predict or forecast one or
more possible future observations.

- **Inputs:** Historical data provided to the model in order to make a single forecast.
- **Outputs:** Prediction or forecast for a future time step beyond the data provided as input.

- Defining the inputs and outputs of the model forces you to think
about what exactly is or may be required to make a forecast.
- you may not know whether one or multiple prior
time steps are required to make a forecast.

### Endogenous vs. Exogenous
- **Endogenous:** Input variables that are influenced by other variables in the system and
on which the output variable depends.
 - For example, the observation at time t is dependent
upon the observation at t − 1; t − 1 may depend on t − 2, and so on.
- **Exogenous:** Input variables that are not influenced by other variables in the system and
on which the output variable depends.

- Often, exogenous variables are ignored given the strong focus on the time series.

### Regression vs. Classification
- **Regression:** Forecast a numerical quantity. fFr example a price, a count, a volume, and so on.
- **Classification:** Classify as one of two or more labels. For example
hot, cold, up, down, and buy, sell are categories.

### Unstructured vs. Structured
- It is useful to plot each variable in a time series and inspect the plot looking for possible
patterns.
- Unstructured: No obvious systematic time-dependent pattern in a time series variable.
- Structured: Systematic time-dependent patterns in a time series variable (e.g. trend
and/or seasonality).

### Univariate vs. Multivariate
- Univariate: One variable measured over time.
- Multivariate: Multiple variables measured over time.

- you may have multiple variables as input to the model and only be
interested in predicting one of the variables as output. In this case, there is an assumption in
the model that the multiple input variables aid and are required in predicting the single output
variable.

### Single-step vs. Multi-step
- One-step: Forecast the next time step.
- Multi-step: Forecast more than one future time steps.

- The more time steps to be projected into the future, the more
challenging the problem given the compounding nature of the uncertainty on each forecasted
time step.

### Static vs. Dynamic
- Static. A forecast model is fit once and used to make predictions.
- Dynamic. A forecast model is fit on newly available data prior to each prediction.

### Contiguous vs. Discontiguous
- Contiguous. Observations are made uniform over time.
- Discontiguous. Observations are not uniform over time.

- The lack of uniformity of the observations may be caused by missing
or corrupt values.
- It may also be a feature of the problem where observations are only made
available sporadically or at increasingly or decreasingly spaced time intervals.
- In the case of
non-uniform observations, specific data formatting may be required when fitting some models
to make the observations uniform over time.

### Further Reading

- [Machine Learning Strategies for Time Series Forecasting, 2013.](http://link.springer.com/chapter/10.1007%2F978-3-642-36318-4_3)
- [Recursive and direct multi-step forecasting: the best of both worlds, 2012.](https://econpapers.repec.org/paper/mshebswps/2012-19.htm)



