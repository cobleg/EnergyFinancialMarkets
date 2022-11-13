## Short answer questions
#### 1.1 Coal plants in the NEM (6 Marks total)

The retirement of coal-fired power stations will likely change electricity spot price outcomes in the NEM.     

1.  Using credible reference material, establish the number of coal-fired generators in the NEM, noting announced closure dates, their respective capacity (MW), and their size relative to the total generation capacity by year. Present your findings in a chart or table. **(4 marks)**
    #### References
    [@OpenNEMFacilitiesNEM]
    “OpenNEM Facilities: NEM.” n.d. Accessed November 12, 2022. [https://opennem.org.au](https://opennem.org.au).

2.  What are the main factors determining the profitability of coal-fired generation? What impact will retirement of coal-fired generation have on the profitability of the remaining coal-fired generation plant. **(2 marks)**

	 **Key points**
	- New facility investment in renewable electricity generation is growing faster than retirement of old facilities
	- Demand growth is slowing, in part due to distributed energy resources at load sites reducing grid-sourced electricity demand
	- Resulting in increased competition when solar and wind energy is abundant.
	- Coal fuelled generation facilities are not designed for intermittent use, resulting (or risking) increased fuel consumed for given electrical power output. 
	- Aging facility typically incur higher maintenance costs
	- Increasing CO2-e would incur high LGC certificate obligations and LGC prices have been trending higher.
	- Relatively high prices for coal internationally could squeeze domestic coal consumers on the buy side.
	- Remaining coal fuelled generators could benefit from reduced competition from retiring coal fuelled generators. However, this would be impacted by the other factors listed above.
	 **References**
[@edistristanFastErosionCoal2021]
Edis, Tristan, and Johanna Bowyer. 2021. “Fast Erosion of Coal Plant Profits in the National Electricity Market.” GreenMarkets.com.au. [http://greenmarkets.com.au/images/uploads/Coal-Plant-Profitability-Is-Eroding_February-2021.pdf](http://greenmarkets.com.au/images/uploads/Coal-Plant-Profitability-Is-Eroding_February-2021.pdf).
	
#### 1.2 Market risk in the NEM (9 marks total)  

Spark Energy has 1,500 MW of coal and gas-powered generation in QLD. It also has a simple hedge portfolio of 1,000 MW in flat swaps with an average strike price of $60/MWh for the next 12 months (8,760hrs). Spark Energy’s risk manager wishes to calculate the VaR associated with its hedge portfolio for a holding period equal to the time between risk committee meetings (one month).  

1.  Using market research to establish realistic volatility parameters, determine a simple VaR for the existing hedge portfolio **(4 marks)**  
	**Key points**
	[Value-at-Risk](value-at-risk.md) = FV x HPV x z
		FV = face value of contracts
		HPV = holding period volatility = $\sqrt{h/T} \times \sigma$ where $h$ is holding period, $T$ is the total number of intervals in a year and $\sigma$ is the annualised volatility. 
		z = the 95% confidence interval
		Using reasonable assumptions (normalised historical volatility over 2021-22 for NSW and normal distribution) HPV = $\sqrt{1/12} \times 0.44 \times 1.645$
		Face value of contracts (FV) = (1,500 MW - 1,000 MW) x $60/MWh (Price) X 12 months
	

2.  Spark Energy’s risk manager does not feel that VaR gives the full picture of Spark Energy’s exposure to electricity price risk. The risk manager is considering using simple sensitivity analysis with parallel shifts in electricity spot and forward prices. What advantages and disadvantages does this sensitivity analysis have relative to the previous VaR analysis? **(2 marks)**
	**Key points**
	- Parallel shifts in the spot price reflect an instantaneous shift in the entire risk profile (measured by the average dispersion of the spot price). One advantage is the realistic reflection of an unplanned loss of a significant generation or load facility.
	- Use of forward prices captures the market's risk bias, which may efficiently reflect all relevant information about future risk.
	- Parallel shift in the forward curve would capture an instantaneous change in future risk profile. One advantage is the shift in the market's assessement of future risk.
	- One disadvantage is that the parallel shift may not reflect an accurate measure of the change in credible (or likely) risk. The key is the magnitude of the shift - how is that determined?
	- Another disadvantage is that the parallel shift might not be readily understood or accepted by senior management. This may require discussion and agreement for something that is an ad-hoc, one-off issue. 
1.  What other ’at risk’ metrics might be useful to Spark Energy’s risk manager in addition to VaR and what are their advantages? **(3 marks)** 
	**Key points**
	- [Cash flow at risk](cashflow-at-risk.md), which focuses on the cashflow rather than the mark-to-market valuation. Cash is likely to be more important to Spark Energy.
	- [Conditional VaR](https://www.investopedia.com/terms/c/conditional_value_at_risk.asp#:~:text=Conditional%20Value%20at%20Risk%20(CVaR)%2C%20also%20known%20as%20the,risk%20an%20investment%20portfolio%20has.) (aka Expected Tail Loss) which measures the expected loss in a tail risk event. This is helpful in providing insight into distress event management and provides a focus on proactive measurement. Also, likely to use obervable metrics to anticipate shifts or changing shape of the risk profile.
	- [Alpha](https://www.investopedia.com/terms/r/riskmeasures.asp), which measures the risk relative to the market. This can help identify any asset specific risks that could affect risk management strategies.
	- [Beta](https://www.investopedia.com/terms/r/riskmeasures.asp#Beta), which measures the systematic risk of loss, which could be used to rank various assets used to manage risk.	- 
    

#### 1.3 Spot price risk in the NEM (6 marks total)

Five-minute settlement was introduced on 1 October 2021.  

1.  Identify two of the anticipated benefits of the change. **(2 marks)**
    - Removes a mismatch between settlemtent and dispatch
    - Improve price signals
    - Improve bidding incentives among large generators, who may have had an incentive to:
	    - Bid extreme high prices in the first five minutes and then bid extremely low for the remainder of the 30 minute interval. This may have been done to exploit market power during specific market conditions, e.g. temporary loss of an interconnector.
	    - Conduct strategic late rebidding with withdrawal of generation capacity to influence the spot price.
	- Encourage investment in fast response generation and demand side response. This would help improve system security [@FiveMinuteSettlement] 
		“Five Minute Settlement.” n.d. AEMC. Accessed November 13, 2022. [https://www.aemc.gov.au/rule-changes/five-minute-settlement](https://www.aemc.gov.au/rule-changes/five-minute-settlement).

2.  Using actual 5-minute spot price data for VIC, produce summary statistics (average, standard deviation, etc.) for the historical spot price distribution, dividing your data into the following two time periods: (i) 12am on 1 October 2020 to 11.55pm on 31 March 2021, and (ii) 12am on 1 October 2021 to 11.55pm on 31 March 2022. Explain any discernible differences in spot price outcomes between the two periods. Data can be sourced from AEMO (https://aemo.com.au/energy-systems/electricity/national-electricity-market-nem/data-nem/aggregated-data). **(4 marks)**  

	**Notes**
	- Five minute data not available until 1 October 2021. Need to use 30 minutes and aggregate the second data sample to 30 minutes.

#### 1.4 Setting portfolio limits for Diverse Energy  (6 marks total) 

Ahead of the commissioning of AMBER1, Diverse recruited Ms Bec Sharp, an experienced risk manager in the Australian energy sector. Bec Sharp’s immediate role is to establish a governance framework and trading infrastructure for managing the market risk exposures of Diverse Energy and its AMBER1 generation portfolio.

Bec Sharp is conscious that her budget for establishing trading infrastructure and placing human resources in risk and analytical roles is limited. Her experience with acquiring sophisticated energy risk systems is that they are expensive and have a long lead time before they can be successfully delivered into production. She is also aware that skilled human resources will be required to ensure that the inputs and risk parameters of these systems undergo calibration and recalibration.

As a result, she has decided to propose _N-1_ volume limits as the methodology for AMBER1’s electricity trading portfolio limits.

1.  Using the limited data available to Bec, calculate and propose an _N-1_ volume limit for Diverse Energy’s electricity hedging portfolio limit. **(2 marks)** 
	**Notes**
	- Diverse Energy case study is the course notes, Topic 2, Lesson 2.5
	- Debt to equity ratio: 60:40
	- Number of units: 4
	- 
	
1.  Identify two reasons influencing Bec’s decision to select _N-1_ as her preferred initial approach. (2 marks)
2.  Identify the issues with volume limit use, with specific reference to the business plan and market risks of Diverse Energy. (2 marks)