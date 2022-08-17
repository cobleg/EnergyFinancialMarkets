# Overview
A `cap` is a financial agreement in which one party agrees to pay the difference between the spot price at a pre-determined market interval and a given strike price multiplied by a predetermined quantity. Another name for a cap is a *[call option](https://corporatefinanceinstitute.com/resources/knowledge/trading-investing/call-option/)*.

The payment from the cap seller to the cap buyer is defined as:

$$ Cap(P,X,S,P_c) = \begin{cases} (P-S)X-P_cX & P \ge S \\
-P_cX & P < S
\end{cases} $$
where
$P$ is the uncertain spot price
$S$ is the strike price
$X$ is the quantity multiplier, e.g. MWh
$P_c$ is the cap premium

In words, this equation says that the cap buyer will receive a payment from the cap seller less the cap premium originally paid in the event that the price exceeds the strike price. The payment received will also be in proportion to the quantity multiplier. 

The term `cap` refers to the buyer's perspective since by buying this contract, the buyer is capping the uncertain spot price. This is achieved by passing on the liability of paying the difference between a high spot price and the strike price to a third party (i.e. the cap seller).

The cap seller gains when the high price event fails to be realised. A smart cap seller will ensure that the probability of a high price event (i.e. higher than the strike price) occuring is low.

A `cap` is a type of [[hedge]] instrument equivalent to one part of a [[swap]]. 

# Worked example


**Source**
Darryl R. Biggar, Mohammad Reza Hesamzadeh (2014). Managing Intertemporal Price Risks (Chapter 13), in [*The Economics of Electricity Markets*](https://onlinelibrary.wiley.com/doi/book/10.1002/9781118775745), John Wiley & Sons, Print ISBN:9781118775752 |Online ISBN:9781118775745 |DOI:10.1002/9781118775745