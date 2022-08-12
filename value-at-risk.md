# Overview
Value-at-Risk (VaR) measures the capital reserves at risk given a defined holding period and at a specified probability of loss. In other words, VaR is the worst expected loss under *normal market conditions* over a specified time interval at a given level of confidence.

This metric was developed by J.P. Morgan in the 1990s as part of its [RiskMetrics](https://en.wikipedia.org/wiki/RiskMetrics) methodology.

VaR is focused on quantifying the risk of financial loss at the end of a holding period (e.g. 1 month). 

Advantages of VaR include simple to calculate and understand. Some disadvantages are that it is subject to change (which can be unpredictable) and requires a judgement of what *normal market* conditions look like in terms of a proabability distribution. Also, it implies an assumption of a stable probability distribution over the holding period (i.e. a constant mean and standard deviation). 
# Calculating VaR
VaR is calculated via this procedure:
1. Define the holding period, e.g. 1 month or 1 year
2. Create a probability density function (can be a simple histogram of historical returns or asset prices)
3. Determine the downside cut-off probability as a quantile (e.g. 1 %). The question is, what is the value of the asset at the cut-off period. The VaR is the difference between the current value and the value at the 1% cutoff.



# Worked example


# References
Johnathan Mun (2006). [*Modelling risk: applying Monte Carlo simulation, real options analysis, forecasting, and optimization techniques*](https://books.google.com.au/books?id=hBHBBwZx7YkC&printsec=frontcover#v=onepage&q&f=false), John Wiley & Sons; ISBN-13 978-0-471-78900-0

Simon Benninga (2014). [*Financial modeling*](https://www.academia.edu/37352998/Simon_Benninga_Financial_Modeling_4th_edition) —Fourth edition, MIT Press; ISBN 978-0-262-02728-1