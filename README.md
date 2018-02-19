# Irish Wind Data 

In this Notebook, we follow Tilmanm  Gneiting experiment as presented in his paper: [Nonseparable, stationary Covariance Functions for Space-Time Data](http://www.jstor.org/stable/3085674).

The Irish wind data consist of daily averages of wind speeds at 12 synoptic meteorological stations in Ireland during the period 1961-1978. Gneiting in his experiment used data from 11 stations, he excluded data from Roslare station. We follow his experiment, by first loading the data into the data frame. We do a square root transformation of the data to make the marginal distributions approximately normal. We then proceed to calculate empirical correlation and plot empirical space-time correlation graphs as in Figure 5 in Gneiting paper. We then fit the data to proposed covariance model and compare results with the results presented in Gneiting paper. In our analysis, we got slightly different results in comparison to Gneting analysis.

In our analysis, we got slightly different results in comparison to Gneting analysis.

Covariance function as presented in paper:

\begin{equation} C(\mathbf{h},t)=\frac{0.968 \exp(-0.00134 ||\mathbf{h}||)}{0.901 t^{1.544} +1}  \end{equation}

Our result:

\begin{equation} C(\mathbf{h},t)=\frac{0.978 \exp(-0.0012 ||\mathbf{h}||)}{0.901 t^{1.589} +1}  \end{equation}


The difference is probably due to a different method of fitting the covariance functions and different results in the average for time lags.
