# Promise of Deep Learning for Time Series Forecasting
- Deep learning neural networks are able to automatically learn arbitrary complex mappings from
inputs to outputs

## After reading this tutorial, you will know:
- The focus and implicit, if not explicit, limitations on classical time series forecasting
methods.
- The general capabilities of Multilayer Perceptrons and how they may be harnessed for
time series forecasting.
- The added capabilities of feature learning and native support for sequences provided by
Convolutional Neural Networks and Recurrent Neural Networks.

#### Time Series Forecasting
- Time series forecasting is difficult :P
- These problems add the complexity of order or temporal dependence between observations
- Specialized handling of the data is required when fitting and evaluating models
- Traditionally, time series forecasting has been dominated by linear methods like ARIMA

##### Limitations of Time Series Forecasting
- Focus on complete data: missing or corrupt data is generally unsupported.
- Focus on linear relationships: assuming a linear relationship excludes more complex
joint distributions.
- Focus on fixed temporal dependence: the relationship between observations at
different times, and in turn the number of lag observations provided as input, must be
diagnosed and specified.
- Focus on univariate data: many real-world problems have multiple input variables.
- Focus on one-step forecasts: many real-world problems require forecasts with a long
time horizon.

#### Summary
- Machine learning methods can be effective on more complex time series forecasting problems
with multiple input variables, complex nonlinear relationships, and missing data. 
- In order to perform well, these methods often require hand-engineered features prepared by either domain
experts or practitioners with a background in signal processing.


#### Convolutional Neural Networks for Time Series
[Representation learning or Feature Learning](https://g.co/kgs/cVrnNt)
transform or distortion invariance = Features are extracted by CNN regardless of how they occur in the data

- Type of neural network that was designed to efficiently handle image data
- Operate directly on raw data, such as raw pixel values, instead of domain-specific or handcrafted features derived from the raw data
- The ability of CNNs to learn and automatically extract features from raw input data can be applied to time series forecasting problems
- A sequence of observations can be treated like a one-dimensional image that a CNN model can read and distill into the most salient elements.

#### Recurrent Neural Networks for Time Series
- Recurrent neural networks like the Long Short-Term Memory network or LSTM add the explicit
handling of order between observations when learning a mapping function from inputs to outputs,
not offered by MLPs or CNNs.
- Native Support for Sequences. Recurrent neural networks directly add support for
input sequence data.
- recurrent neural networks can also automatically learn the temporal dependence from the data
- In the simplest case, the network is shown one observation at a time from a sequence and
can learn what observations it has seen previously are relevant and how they are relevant to
forecasting
- The model both learns a mapping from inputs to outputs and learns what context
from the input sequence is useful for the mapping, and can dynamically change this context as
needed.

### Promise of Deep Learning
- Neural networks learn arbitrary mapping functions.
- Neural networks may not require a scaled or stationary time series as input
- Neural networks support multivariate inputs.
- Neural networks support multi-step outputs.
- Convolutional neural networks support efficient feature learning.
- LSTM networks support efficient learning of temporal dependencies.
- Hybrid models efficiently combine the diverse capabilities of different architectures.

### Further Reading
- [Deep Learning for Time-Series Analysis, 2017.](https://arxiv.org/abs/1701.01887)
- [Neural Networks for Time Series Processing, 1996.](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5697)
- [Sequence to Sequence Learning with Neural Networks, 2014.](https://arxiv.org/abs/1409.3215)
- [Applying LSTM to Time Series Predictable through Time-Window Approaches, 2001.](https://link.springer.com/chapter/10.1007/3-540-44668-0_93)
- [Long Short Term Memory Networks for Anomaly Detection in Time Series, 2015.](https://www.elen.ucl.ac.be/Proceedings/esann/esannpdf/es2015-56.pdf)
- [Convolutional Networks for Images, Speech, and Time-Series, 1998.](https://dl.acm.org/citation.cfm?id=303704)
- [Deep Convolutional Neural Networks On Multichannel Time Series For Human Activity
Recognition, 2015.](https://dl.acm.org/citation.cfm?id=2832806)

