\setcounter{page}{1}
\pagenumbering{arabic}
\doublespacing
\setlength{\parindent}{0.5in}

# The ARIMA model {#sec:intro}

The ARIMA model consists of three different models combined into one and can be used to make predictions.

## AR component

The AR part of ARIMA stands for "Auto-Regression". Values from previous time stamps are used to predict the value for the next time stamp. The parameter **p** determines how many past values are used. Thus, the formula for the AR model can look like this [@hyndman_rj_83_2018]:

$$y_{t} = c + \phi_{1} y_{t-1} + \phi_{2} y_{t-2} + ⋯ + \phi_{p} y_{t-p} + \varepsilon_{t}$$ {#eq:my_equation}

The component _c_ is a constant and can be used to shift the outcome of the prediction. If not desired, it can be set to 0 and be left out.

The component $\varepsilon_{t}$ is white noise.

## I component

The I part stands for "Integrated" and is described by the integration of the differentiation terms of the time series to establish data stationarity.
The paramter **d** indicates how often this operation is performed. 
If the time series is not stationary i.e. its statistical properties such as mean and variance vary over time, they must be stabilized by differentiation to allow stable prediction.

This part can be described with the formula [@schaffer_interrupted_2021]:

$$y'_{t} = y_{t} - y_{t-1}$$ {#eq:my_equation}


## MA component

The MA part stands for "Moving Average". Previous forecast errors are used to predict the next value. The parameter **q** determines how many past forecast errors are used. Thus, the formula for the MA model can look like this [@hyndman_rj_84_2018]: 

$$y_{t} = c + \varepsilon_{t} + \theta_{1} \varepsilon_{t-1} + \theta_{2} \varepsilon_{t-2} + ⋯ + \theta_{q} \varepsilon_{t-q}$$ {#eq:my_equation}

As in the AR model, the component _c_ is a constant to shift the outcome and the component $\varepsilon_{t}$ is white noise.


## Determing the parameters

There are various ways to determine the parameters. One way would be to use random numbers in a certain range. In the following, one mathematical approach for each paramter will be described.

### Parameters  $\phi_{1},...,\phi_{p}, \theta_{1},...,\theta_{q}$

The parameters **$\phi_{1},...,\phi_{p}, \theta_{1},...,\theta_{q}$** can be determined by using maximum likelihood estimation (MLE). This method tries to find the parameter values that minimize the distance between the observed values and the predicted values.

### Parameter p

To choose a suitable value for the parameter **p** it is possible to choose the most significant lags in the partial autocorrelation function plot. This function is estimated by the partial correlation of values after controlling for the effects of other variables [@zvornicanin_choosing_2023].

### Parameter d

The paramter **d** is the value at which the time series becomes stationary and the ACF plot and PACF plot of the differentiated time series no longer show significant autocorrelations.It can be determined by checking test statistics such as the ADF test (Augmented Dickey-Fuller Test). When the value returned from that test is greater than 0.5 the time series is non-stationary and more differenciating is needed.

### Parameter q

Similar to the parameter p, the parameter **q** can be chosen by the most significant lags in the autocorrelation function plot. This plot shows the correlation of the values in a time series [@zvornicanin_choosing_2023].

