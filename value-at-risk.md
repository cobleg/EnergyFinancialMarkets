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

# Worked examples
## Worked example - estimating
In estimation, we make simplifying assumptions:
1. The variation is random which is captured by the Normal distribution.
2. Evolution of variation is purely random.

With these stringent (i.e. unlikely to be realistic) we can develop an `order-of-magnitude` estimate. 

Let's set a confidence interval of 95% since that implies a cut-off distance of 2 standard deviations less than the mean. This in turn implies a multiple of 1.645 of the actual distance between the standard deviation and the mean (assuming a [one-tailed test](https://stats.oarc.ucla.edu/other/mult-pkg/faq/general/faq-what-are-the-differences-between-one-tailed-and-two-tailed-tests/)).

In calendar year 2021, hourly wholesale spot electricity prices in South Australia averaged $54 per MWh with a standard deviation of $216 per MWh. This implies the cut-off value is:

$$ (54 - 216) \times 1.645  = -$266.49 $$
This is the VaR result assuming a holding period of just one hour. For 1 business day we need to adjust the value. There are 24 hours in the day, so the adjustment factor is:

$$ -266.49 \times \sqrt{24} = -266.49 \times 4.898979 = -$1,305.53 $$
However, there is a [[spot price floor]] imposed in the [[National Electricity Market]] [wholesale market price floor of -$1,000](https://aemo.com.au/-/media/Files/Electricity/NEM/National-Electricity-Market-Fact-Sheet.pdf) so this is the worst possible case, not the answer we calculated.


## Worked example - calculating using a PDF
The use of the 95% probability cut-off threshold was a little arbitrary. On occasion, risk managers may want to use a different cut-off threshold. This example shows how to calculate the value directly from the [Probability Density Function (PDF)](https://en.wikipedia.org/wiki/Probability_density_function). 

Hourly wholesale spot electricity prices in the Queensland region of the [[National Electricity Market]]  traded around an average of $83.70 per MWh and a standard deviation of $340 per MWh over calendar year 2021. Assume a Normal distribution for spot prices and a 1% cut-off probability level for VaR. 

**Q1. Calculate the cut-off price level.**

In Excel set up a table with the mean price, standard deviation, the cut-off probability and the cut-off price. Set the cut-off price at any plausible number. 

Use the NormDist function in Excel to calculate the probability of encountering a spot price that is at or below a probability of the cut-off price. 

Then use Solver to adjust the value of the cut-off price that matches the cut-off probability threshold. The derived cut-off price is -$707.26 per MWh. 

The negative price might be surprising and requires checking. However, wholesale electricity prices have fallen below zero across NEM regions on multiple occasions during calendar year 2021. 
![[VaR calculation in Excel 1.png]]

![[Excel Solver screenshot 1.png]]

![[VaR normal distribution 1.png]]


**Q2. Assume that an electricity supplier has a contract to sell 100 MW of electricity at $60 per MWh for one month. What is the VaR?**

The value-at-risk is: Contract Price less the Cut-off Price, which in this example is $$ $60 - -$707.26/MWh = $60/MWh + $707.26/MWh = $767.26/MWh $$
This suggests that in the worst-case scenario, the electricity supplier could realise a *gain* of $767.26 per MWh by keeping the $60 per MWh under contract and being paid to take electricity from the wholesale market. 

A more sensible consideration would be to calculate the cash flow at risk. Assume that it costs $35 per MWh to supply electricity. The net cash flow assuming the spot price is at or above $60 per MWh is equal to 

$$ $60/MWh - $35/MWh = $25/MWh $$
Now calculate the same cash flow at the worst case scenario. The electricity supplier would receive a cashflow equal to

$$ -$707/MWh - $35/MWh = -$742.26/MWh $$
That is, the electricity supplier is compelled to pay $742.26/MWh under the contract at the worst-case scenario. Assuming the electricity supplier is not a [[must-run generator]], it is better off by purchasing electricity to net off its obligation to supply from the wholesale market and receiving total cash flow of:

$$ $707.26/MWh + $60/MWh = $767.26/MWh $$ 

# References
Colleen Cassidy, Marianne Gizycki (1997). [Measuring Traded Market Risk: Value-At-Risk and Backtesting Techniques](https://www.rba.gov.au/publications/rdp/1997/pdf/rdp9708.pdf), Research Discussion Paper 9708, Reserve Bank of Australia

Johnathan Mun (2006). [*Modelling risk: applying Monte Carlo simulation, real options analysis, forecasting, and optimization techniques*](https://books.google.com.au/books?id=hBHBBwZx7YkC&printsec=frontcover#v=onepage&q&f=false), John Wiley & Sons; ISBN-13 978-0-471-78900-0

Simon Benninga (2014). [*Financial modeling*](https://www.academia.edu/37352998/Simon_Benninga_Financial_Modeling_4th_edition) —Fourth edition, MIT Press; ISBN 978-0-262-02728-1