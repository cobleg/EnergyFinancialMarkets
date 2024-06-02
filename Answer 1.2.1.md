Value-at-Risk (VaR) determines the expected maximum loss. A confidence interval of 95% implies a risk tolerance of 5% for the loss side. If the normal distribution applies, this suggests a `z-score` $z = 1.645$. 

The sample data is daily data for futures series `BQH2025` spans February 2023 to February 2024, inclusive. 
![BQH2025 sample data](BQH2025%20sample%20data.png)

Choosing the `settle` series, calculate the natural logarithmic ratio:
$$ 
r_t = ln(\frac{r_t}{r_{t-1}})
$$
The resulting returns histogram is as shown in the chart:
![BQH2025 histogram](BQH2025%20histogram.png)

The sample mean settle price is $110.93 / MWh. 

The standard deviation summary statistics for the returns are $\mu = -0.03\%$, $\sigma = 1.37\%$. The VaR cut-off (lower) is $\mu + \sigma z = 0 - 1.37\% \times 1.645 = -2.28\%$. The upper cut-off statistic is $2.23\%$. 

The holding period is 30 days, so the cut-off statistic needs to be scaled to monthly. This requires multiplying by the square root 30 days. This is $-2.28\% \times \sqrt{30} = -7.54\%$; $2.23 \% \times \sqrt{30} = 7.48\%$.

The swap strike price is $130/MWh$ and the total swap hours for 1 megawatt (MW) over 30 days is $30 \times 24 = 720$ hours.  

The swap formula is $(S-P)X$ where
$S$ is the strike price
$P$ is the spot price
$X$ is the quantity

The current spot price is $104.86, so the lowest expected price over 30 days is $(1-7.48\%)\times \$104.86 =\$102.47$.
Assuming the maximum expected loss for 1 MW yields

$$
(\$102.47-\$130) \times 720 = -$18,101.80
$$
Since Spark Energy holds 1,000 MW in flat swaps, this is multiplied by 1,000 to yield

$$
-$18,101 \times 1,000 = -$18,100,800
$$

