Volatility defines the riskiness of an asset. That is, the degree of likely and possible variation in price or value over time.

The frequency of observation (how often the price of an asset is measured) will affect the volatility measurement.

A higher frequency data sample (e.g. daily returns) will have a lower volatility than a lower frequency data sample (e.g. monthly returns).

Conversion between the two frequencies is sometimes necessary. For example, the daily returns data for a given asset may need to be used to estimate the volatility of the same asset over a month.

## Theoretical basis for the rule  

Any random variable that is the sum of independent and identically distributed random variables will have a variance that scales linearly with the number of random variables in the sum.

Define $T$ as the number of time steps in a sample. That is, $T$ is the last observation in the sample.

Let $X_t$ denote the value of a random variable at a time occurring between $t=1$ and $t=T$ such that $0 < t \le T$. That is, $t=(1,2,3,...,T)$.

Define $Y_T$ as the sum of the series of random variable observations measured at regular time intervals, that is

$Y_T=X_1+X_2+X_3+…+X_T$

where $X_T \sim N(\mu,\sigma^2)$, _i.i.d._

By definition, the variance of $Y_T$ is

$V[Y_T] = \Sigma_{t=1}^{T} V[X_t] = V\Sigma_{t=1}^{T} [X_t] = T V[X_t] = T\sigma^2$

Given the definition of [[volatility]], the [[volatility]] of the aggregate variable $Y_T$ is the square root of this variance, that is $vol = \sqrt{T}\sigma$.

When $Y_T$ represents a lower frequency sum of the same random variable, then it follows that the lower frequency volatility can be estimated by using the square root of time rule.


## References
[Square Root of Time Rule](Square%20Root%20of%20Time%20Rule.md)
