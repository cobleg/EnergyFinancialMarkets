To calculate the price of the electricity retail contract that Johnnie offered, adopt the futures contract based on the wholesale electricity forward curve and account for the additional retail margin. 
### Methodology to Calculate the Price

1. **Identify the Wholesale Electricity Forward Curve**:
   - Obtain the current wholesale market electricity forward curve, which provides the expected prices for electricity for future periods.

2. **Determine the Load Profile**:
   - Estimate the customer's electricity consumption pattern over the contract period.
   - Consider factors like peak and off-peak demand, seasonal variations, and overall consumption volume.

3. **Calculate the Average Wholesale Price**:
   - Using the load profile, calculate a weighted average price based on the forward curve prices.
   - Weight each period's price by the proportion of total consumption expected in that period.

$$
   \text{Average Wholesale Price} = \frac{\sum (\text{Forward Price}_i \times \text{Consumption}_i)}{\sum \text{Consumption}_i}
$$

4. **Add the Retail Margin**:
   - Apply the 5% retail margin to the average wholesale price to determine the final retail price offered to the customer.

$$  
   \text{Retail Price} = \text{Average Wholesale Price} \times (1 + \text{Retail Margin})
 $$

### Key Factors Impacting the Price

1. **Wholesale Market Prices**
   - The primary factor is the current and expected future wholesale market prices as reflected in the forward curve.
   - Market prices are influenced by supply and demand dynamics, fuel costs, regulatory changes, and macroeconomic factors.

2. **Customer's Load Profile**
   - The pattern and timing of the customer's electricity usage impact the average price calculation.
   - Peak vs. off-peak consumption and seasonal variations need to be accurately forecasted.

3. **Market Volatility**
   - Fluctuations in the wholesale market prices can significantly impact the cost base.
   - Hedging strategies need to account for potential price volatility.

4. **Regulatory Environment**
   - Changes in regulations, such as carbon pricing or renewable energy mandates, can affect wholesale prices.
   - Regulatory risks need to be factored into the pricing model.

5. **Retail Margin**
   - The 5% retail margin is added to cover operational costs, risk premiums, and profit.
   - The margin should reflect the company’s risk tolerance and market competition.

6. **Hedging Costs**
   - The cost of entering into futures contracts or other hedging instruments should be included.
   - Hedging helps mitigate price risk but incurs costs that need to be accounted for in the pricing model.

### Example Calculation

Assume the following simplified data:

- Monthly forward prices for the next two years: $\$80, \$85, \$90, ...$ (average of $\$85/\text{MWh}$).
- Customer’s monthly consumption is constant at 1,000 MWh.

1. **Calculate Average Wholesale Price**
$$ 
   \text{Average Wholesale Price} = \frac{\sum (\text{Forward Price}_i \times \text{Consumption}_i)}{\sum \text{Consumption}_i}
$$
   Given consumption is constant and forward prices average to $85:
   $$
   \text{Average Wholesale Price} = $85/\text{MWh}
$$   

2. **Add Retail Margin**
  $$
   \text{Retail Price} = $85 \times (1 + 0.05) = $85 \times 1.05 = $89.25/\text{MWh}
$$

Thus, the final retail price offered to the customer is $89.25/MWh, ensuring the retail margin is included and reflecting the average cost based on the wholesale forward curve.