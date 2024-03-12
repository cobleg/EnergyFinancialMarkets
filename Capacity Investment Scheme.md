# Definition
> The Capacity Investment Scheme (CIS) is a national framework and an Australian Government initiative to encourage new investment in renewable capacity, such as wind and solar, and clean dispatchable capacity.

[Implementation Design Paper - Capacity Investment Scheme](Implementation%20Design%20Paper%20-%20Capacity%20Investment%20Scheme.md) 
# Objective
The objective is to:
- Deliver an additional 32 GW of new capacity by 2030
- Supporting electricity generation growth and reliability in Australia's rapidly changing electricity markets as aging thermal power stations exit.
- Support the delivery of the Australian Government's 82% renewable electricity by 2030 target.
# Design principles
The design principles guiding the CIS are:
- **Maintaining momentum** by accelerating the investment timeline for projects already in the advanced planning stage to deliver new $CO_2$-e emissions-free electricity supply capacity.
- **Stimulate investment** by providing long-term certainty for financiers through a combination of long-term financial underwriting offered to Projects and a clear, transparent tender process used to set key commercial terms in the CIS agreement (CISA).
- **Complementing existing market operations** by avoiding imposing operational conditions that may conflict with existing operating rules. The CISA can be integrated into a portfolio of [[swap]] contracts and [[tolling agreements]]. 
- **Tender product adaptability** which will select projects that support energy system reliability and lower electricity prices.
- **Supporting local communities and first nations people**
Source: [Implementation Design Paper | Capacity Investment Scheme](Implementation%20Design%20Paper%20-%20Capacity%20Investment%20Scheme.md) 

In short, the CIS design aims to reduce risks for proponents of renewable energy and clean dispatchable projects while preserving existing electricity market signals.

# CISA products
There are two defined products:
- **Clean Dispatchable CISA** applies to a *clean dispatchable generator* (e.g. battery and pumped hydro) at a registered capacity for 2 or more hours. The contract term is 15 years. 
- **Generation CISA** applies to generators (i.e. solar and wind power stations)

Eligible projects (i.e. facilities) have the following properties:
- Registered or intended to be registered with the Australian Electricity Market Operator (AEMO) as a generator.
- Are facilities that *do not* emit $CO_2$-e gases. That is the project has a fuel source that is not included in [[Scope 1 emissions]].
- Are commercially defined as defined in the section: [Key commercial terms](#Key%20commercial%20terms) 
- Have a minimum capacity of 30 MW
- Can sustain continuous operation for a duration of at least 4 hours
- For storage-only projects, the project is capable of charging only from the grid
- The project can demonstrate that it contributes to system reliability (this excludes stand-alone wind or solar PV projects from being eligible for the CIS)
- There is evidence of secure access to land, a planning pathway with relevant planning approvals, and a viable grid connection
- The project has adopted established, proven technologies where delivery risk and the project's commissioning dates are reasonably assessable.

Projects that already receive revenue support from either the Commonwealth, State or Territory Governments, that operate similarly to the CIS as a periodic or ongoing payment, will be ineligible for CIS tenders. However, the receipt of [large-scale-generation-certificates](large-scale-generation-certificates.md) (LGCs), [ARENA](https://arena.gov.au/about/) or [Clean Energy Finance Corporation](https://www.cefc.com.au/) grants will not affect eligibility.

Source: 
[Federal Government's new $10 billion Capacity Investment Scheme](Federal%20Government's%20new%20$10%20billion%20Capacity%20Investment%20Scheme.md) 

# Payment mechanisms
## Generation CISA
The Generation CISA will provide revenue underwriting for net revenue per MWh of generation sent out by a facility. This contract structure is shown below:
![Generation CISA](images/Generation%20CISA.png)

Source: [Implementation Design Paper - Capacity Investment Scheme](Implementation%20Design%20Paper%20-%20Capacity%20Investment%20Scheme.md) 

## Clean Dispatchable CISA
The Clean Dispatch CISA is similar in design
![Clean Dispatchable CISA revenue underwriting design instrument](images/Clean%20Dispatchable%20CISA%20revenue%20underwriting%20design%20instrument.png)
# Key commercial terms
The following are the defined commercial terms:
- **Ownership structure**: A project must be owned by a [[SPV]] that has all the assets required to undertake the project. The [[SPV]] must  be:
	- the Project Operator for the CISA
	- a registered [[NEM]] participant and receive all financial value associated with the Project.
	The Project Operator must:
		- be the counterparty to all revenue contracts (e.g. for a [[PPA]] )
		- must not carry on any other business other than the Project.
- **Project characteristics**: are required (e.g. nameplate capacity).
- **Support term**: spans up to maximum of 15 years.
- **Payment mechanism**: 
	- Quarterly payments for the first three quarters of the financial year. An annual reconciliation payment (Annual Adjustment Payment) will be made, subject to an annual cap.
	- Payments made according to the Project's revenue for each period, compared to its revenue floor and ceiling.
	- The underwriting mechanism is based on a project's net revenue, which is the sum of all revenue for the project minus costs from:
		- For storage projects, costs in relation to the import of electricity from the network.
		- Costs for Ancillary Services Network Support Services, or System Support Services.
		- Other costs incurred under the National Electricity Rules (excluding fines or penalties)
		- Any payments under and Eligible Wholesale Contract (excluding liquidated damages, warranty payments, or non-performance payments).
- **Contracted Percentage**: up to a maximum of the Project's capacity.
- **Escalation**: The Floor Price and Sharing/Ceiling Price will be bid ($/MWh) for each supported year. Escalation is allowed as a bid negotiation point.
- **Performance pay requirements**: the Project Operator must:
	- Operate the project following best industry practice, including maximising availability of the Project and revenues for the Project.
	- Respond to price signals in the electricity market.
	For the Generation CISA, the performance criteria are:
	- **Minimum dispatch**: Satisfy the performance pay requirement of being dispatched for at least 75% of [[P90]] operational demand each year).
	For the Clean Dispatchable CISA, the performance criteria are:
	- **Performance Event**: the project must bid at least 50% of its contracted capacity during an actual Lack of Reserve (LoR) 3 event.
	- **Storage capacity**: the project must have a tested storage capacity of at least the CISA schedule capacity.
	- **Availability**: the project must be available at least 90% during the support year.
# Discussion
The intent of the CIS is to simulate additional investment in electricity supply infrastructure that will accelerate the [[Energy Transition]] in Australia.

The scheme favors dispatchable or firm capacity. Also, there is a focus on least-cost procurement via an implied enhanced [contestability](https://www.investopedia.com/terms/c/contestablemarket.asp) between eligible projects via a competitive tender.

The underlying [[swap]] structure is intended to reassign financial risk associated with operating the project (facility). The risk of revenue under-recovery is assumed by the Australian Government while the risk of revenue over-recovery is assumed by the [[SPV]] as Project Owner. The effect is to reduce the uncertainty of future revenue variability and thus enhance the [[financeability]] of the projects. 

The underlying assumption is that all investment grade projects will be financed, constructed and become operational at an earlier date than would otherwise occur. 

Taking this rather indirect approach contrasts with an alternative in which the Australian Government directly builds and owns its own facilities. The assumed benefits are:
- Incurring less than 100% of the cost of each facility.
- Avoidance of 'picking winners' in relation to choosing between specific projects.
- Remaining technology agnostic by defining the properties of the desired operational outcomes (e.g. supply of clean, reliable power) rather than defining the technological inputs (e.g. wind, solar, battery storage, nuclear etc).
- Does not interfere with (or crowd out) other investments in power infrastructure.

One caveat is that the introduction could introduce a 'moral hazard' issue given that the scheme explicitly transfers the risk of revenue under-recovery to Australian taxpayers. The design of the scheme imposes a variety of constraints for known moral hazard issues, but may not prevent some yet-to-be discovered loophole from being exploited. 


#CIS
#CISA 