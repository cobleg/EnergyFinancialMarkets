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

## Issues with using this rule in the real world
According to [On time-scaling of risk and the square–root–of–time rule](inbox/On%20time-scaling%20of%20risk%20and%20the%20square–root–of–time%20rule.md), the:

- **Square-Root-of-Time Rule**: is used for estimating quantiles of return distributions, such as value-at-risk (VaR). The authors argue that this rule leads to a systematic underestimation of risk, especially when returns follow a jump diffusion process.
    
- **Underestimation of Risk**: The underestimation worsens with longer time horizons, higher jump intensity, and higher confidence levels. The rule is not robust for modeling systemic risk.
    
- **Alternative Methods**: The authors propose that for accurate risk assessment, alternative methods need to be applied carefully, considering the potential biases of the square-root-of-time rule. They provide approximations for correcting the rule and stress the importance of not relying solely on this rule for longer horizons or systemic risk modeling.
    
- **Systemic Risk and VaR Estimation**: The main themes revolve around the analysis of systemic risk, Value-at-Risk (VaR) estimation, and the impact of systemic events on financial portfolios. 
    
Specific scenarios that highlight the issues with using the square-root-of-time rule:

1. **Partial Wealth Wipeout**: in a scenario where only part of the wealth is wiped out in a systemic event, the square-root-of-time rule still leads to a downward bias in quantile forecasts. This is because the portfolio return almost surely cannot recover losses greater than the Value-at-Risk (VaR) over the specified scaling horizon.
    
2. **Positive Drift**: the drift (the expected return in a risk-neutral world) is positive. Some practitioners recognize that the presence of a positive drift term leads to an overestimation of risk. However, even in this case, jumps (sudden drastic changes in value) lessen, and in most practical situations, this overestimation lead to a situation where financial institutions are potentially ill-prepared and/or under-capitalized.
    

## References
[Square Root of Time Rule](Square%20Root%20of%20Time%20Rule.md)
[On time-scaling of risk and the square–root–of–time rule](inbox/On%20time-scaling%20of%20risk%20and%20the%20square–root–of–time%20rule.md)
