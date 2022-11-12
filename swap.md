# Overview
A swap is a [[forward-contract]] with fixed volumes. In the electricity industry, fixed-volume forward contracts are known as `contracts-for-difference`, otherwise known as swaps.

A swap is a financial agreement where the seller agrees to pay the buyer an amount equal to the difference between the spot price at a predetermined market interval and a predetermined fixed price multiplied by a predetermined quantity. This results in the swap of a floating revenue stream for a fixed revenue stream.

$$ Swap(P,X,S)=(S-P)X $$
where:
$P$ is the uncertain future spot price at a given date and time
$X$ is the quantity, typically measured in units of MWh
$S$ is the fixed swap price

A swap implies a two-way cashflow. If the spot price is less than the fixed price, the swap buyer pays the swap seller the difference. If the spot price is more than the fixed price, the swap seller pays the swap buyer the difference.

# Types of swaps
## Flat swap
Covers the market intervals across the day for a fixed period of time, e.g. a month, quarter, or year.

## Peak swap
Cover the peak demand market interval periods in each day for a fixed period of time, e.g. a month, quarter, or year.

## Off-peak swap
Cover the market intervals outside the peak demand period for a fixed period of time, e.g. a month, quarter, or year.

## Sculptured swap
A swap in which the volume varies in a prescribed pattern over a specified time period e.g. a day. 

**Source**
Darryl R. Biggar, Mohammad Reza Hesamzadeh (2014). Managing Intertemporal Price Risks (Chapter 13), in [*The Economics of Electricity Markets*](https://onlinelibrary.wiley.com/doi/book/10.1002/9781118775745), John Wiley & Sons, Print ISBN:9781118775752 |Online ISBN:9781118775745 |DOI:10.1002/9781118775745