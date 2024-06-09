![Gas markets Australia - liquidity ratio](images/Gas%20markets%20Australia%20-%20liquidity%20ratio.png)

The [[liquidity]] ratio is defined as the volume of futures contracts over physical delivery. [[Liquidity]] is a measure of market efficiency with higher liquidity implying easier trading conditions in which the act of buying and selling a commodity yields lower price change.

The [[liquidity]] ratio is a measure of trading intensity. There are two calculations with different interpretations:

1. **[[Liquidity]] ratio in the period**. That is, volume traded in futures contracts across all maturities in a given period (e.g. a year) over the underlying physically delivered for that period. In this interpretation, the liquidity ratio indicates the relative liquidity of trading between future periods relative to current demand. A low ratio (less than one) could indicate that the futures market is not very liquid with most buyers wanting physical delivery and secure deliveries via 'off-screen' trading. 
2. **[[Liquidity]] ratio for the period**. That is, volume traded across all futures contract maturities within a given period of physical delivery. This interpretation provides an indication of the relative liquidity of future contract periods to the current period. A low ratio (less than one) could indicate 'price discovery' activities occurring in the futures market without full commitment to physical delivery ahead of time.

The [[liquidity]] ratios shown in the table above show both interpretations.
- [[Liquidity]] ratio (all contracts traded in year). The liquidity ratio are less than one, which indicates that futures trading has a lower volume than physical delivery. The decrease in the ratio from 2021 to 2022 reflects reduced demand as gas prices were expected to decline following a large upward price spike during 2022.
- [[Liquidity]] ratio (all contracts for year). While still less than one, the liquidity ratio increased substantially in 2022. This likely reflects the need to lock-in the price ahead of time given the gas price shock. Also note the reduced underlying demand for gas in 2022 compared to 2021. 

## How the liquidity ratio is calculated
There are several steps to calculating the liquidity ratio in this case:
- Obtain gas futures contract data and create an analytical data set
- Obtain data for the physical delivery market, aka spot market
- Calculate the conditional sum for each maturity date:
	- across maturity dates for each period (e.g. a year)
	- within each maturity date over time.

### Analytical data sets
![ASX cash futures contracts](ASX%20cash%20futures%20contracts.png)
The gas futures data is shown in the image above. The Code provides information identifying the trading hub (i.e. Victoria or Wallumbilla), time to maturity (i.e. month, quarter or year) and maturity year (e.g. 2020, 2021, 2022). The quantity represented by each contract is calculated and presented in petajoule quantities.
![ASX gas futures codes](ASX%20gas%20futures%20codes.png)

The physical delivery data is obtained from reports published by the Australian Energy Regulator (see example below).
![AER Gas production Table 5.2](AER%20Gas%20production%20Table%205.2.png)
The futures contracts are summed across the gas trading hubs to align with the Eastern Australia total shown in the gas production table.

The conditional sums for each year are calculated in Excel: 
- All contracts traded in year according to`=SUMIFS(Table1[Quantity (PJ)],Table1[Year],2021)`. Note that the year column is obtained from the trading date.
- All contracts for year according to `=SUMIFS(Table1[Quantity (PJ)],Table1[Contract maturity period],2021)`. Note that the contract maturity period column is obtained from the ASX gas futures code.

The liquidity ratios are calculated according to
$$
LR_{\text{in year}} = \frac{Q_{\text{traded in year}}}{Q_{\text{produced, year}}}
$$

and

$$
LR_{\text{for year}} = \frac{Q_{\text{maturity year}}}{Q_{\text{produced, year}}}
$$
## References
[State of the energy market 2022 - Australian Energy Regulator (AER)](State%20of%20the%20energy%20market%202022%20-%20Australian%20Energy%20Regulator%20(AER).md)
[State of the energy market 2023 - Australian Energy Regulator (AER)](State%20of%20the%20energy%20market%202023%20-%20Australian%20Energy%20Regulator%20(AER).md)
[Australian and New Zealand Natural Gas Futures - Contract Specifications](Australian%20and%20New%20Zealand%20Natural%20Gas%20Futures%20-%20Contract%20Specifications.md)
