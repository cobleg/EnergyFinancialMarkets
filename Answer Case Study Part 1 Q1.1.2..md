
| Item                       | Value            | Units of Measurement |
| -------------------------- | ---------------- | -------------------- |
| Company name               | Mcap Pty Ltd     |                      |
| Number of generating units | 3                |                      |
| Capacity per generator     | 250              | MW                   |
| Swap position              | short            |                      |
| Swaps capacity             | 750              | MW                   |
| Swap strike price          | 90               | $/MWh                |
| Date of high price event   | 1 September 2024 |                      |
| Trading interval duration  | 5                | minutes              |
| Spot price maximum         | 16,600           | $/MWh                |
| Number of minutes per hour | 60               | minutes              |
## Generation revenue
This is calculated by
$$
Units \times Capacity \times SpotPrice \times \frac{TradingInterval}{Minutes Per Hour}

$$
$$
2 \times 250 \times 16,600 \times \frac{5}{60}
$$

$$

\$         691,667
$$
## Swap revenue
This is calculated by
$$
-(SpotPrice - StrikePrice) \times Q_{MW} \times \frac{TradingInterval}{Minutes Per Hour}

$$
$$
-(16,600-90) \times 750 \times \frac{5}{60}
$$

$$

$      1,031,875
$$
## Net position
The net position is the sum of the generation and swap revenue, which yields $-\$340,208$
