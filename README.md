# Risk Model Validation

At each month-end, the Valuation Product Control Group (VPC) performs an independent fair valuation of all portfolios within Trading Products. This process results in independent price verification adjustments (IPV) and valuation adjustments (VA). IPV reflect the valuation difference between the line of business (LOB) view of valuation and the independent VPC view. VA’s are adjustments used to achieve fair value and include Close-Out, Uncertainty, Liquidity, Model Risk, and Administrative.

Value at Risk (VaR) is computed using risk sensitivities from the official risk systems. Given that the IPV and VA are applied outside the system, consideration must be paid to what impact these adjustments may have, if any, to these risk sensitivities. For example, a large IPV may signal a material difference between the market data in the source system and the independent market data. The source system data is used to compute the risk sensitivities for VaR. Differences in these market data may result in changes in risk sensitivities, particularly for portfolios that exhibit non-linearity, where the risk sensitivity itself changes with changes in market data.

In this note, a control process will be outlined with the following steps:

§  Monthly IPV and VA review
§  Assessment of potential impact of IPV and VA on risk sensitivities
§  Implementation and maintenance of required Proxy Trades
§  Sign Off and Record Keeping


VPC holds a month-end meeting to review all IPV/VA with representatives from the line of business (LOB), Capital Markets Finance, Chief Accountant’s Group, and Risk Oversight. A report is distributed outlining the IPV and VA balances and month over month changes. Detailed reports for each LOB are also available

VPC will identify material IPV and VA balance for each portfolio (as defined by a unique limit letter) that have a potential impact on VaR. Materiality will be set at total IPV adjustment or total VA greater than $1MM per portfolio. Note that individual rather than net IPV and VA balances should be reviewed as there may be offsetting effects within a portfolio.

The origin of IPV balances can generally be ascribed to two principle effects. The first effect originates from a difference between the existing source system market data and the independent VPC market data. The second effect originates from constraints in the source system valuation functionality. These constraints are typically addressed through out-of-system calculations performed by VPC.

Differences in market data can change the risk sensitivities, particularly for the non-linear books. For exotic derivative desks and options desks, calculating new risk sensitivities using VPC market data is an important consideration given the inherent non-linearity existing in these portfolios. For more linear books, the effect of market data differences on risk sensitivities will not be as pronounced. VPC/Risk Oversight will compute new risk sensitivities for material IPV balances.

In certain cases, fair valuation of financial instruments may require capabilities that are not present in the source system valuation models or valuation environment. In these cases, VPC will use existing vetted models outside the source systems to compute fair value. For material IPV adjustments, the factor(s) will be assessed with respect to the implications on risk sensitivities.

Where IPV/VA adjustments have been deemed material and therefore new risk sensitivities are required, VPC and Risk Oversight will work to compute these sensitivities. With respect to material IPV balances originating from market data differences, this will generally involve using the existing source system to compute risk sensitivities with VPC data. For source system functionality constraints, this will involve using the valuation platform used by VPC to compute the risk sensitivities. Given that risk sensitivities are computed by perturbing market data, this can be achieved by performing repeated valuations using the platform. For material VA balances, new risk sensitivities will be obtained from either the source system or the VPC valuation platform, whichever is appropriate.

Once new risk sensitivities are computed for a given portfolio, these will be compared to existing risk sensitivities used to compute the original LOB level VaR figure. Where risk sensitivity differences exist with magnitude greater than 10%, Risk Oversight will work with the Risk Methodologies group using their vetted VaR prototype to compute potential VaR impact at the portfolio and top of the house level. The prototype allows for this kind of assessment in an expedient manner without having to enhance the risk files in the official VaR process. If the VaR change at the LOB node level is greater than a threshold of 15% and/or the impact at the top of the house is greater than 5%, the immediate implementation of a proxy trade will be initiated.

For example, there are more than 1,500 different types of bonds. The differences are specified by calculation type. Each calc type defines a method used to determine the accrued interest, price, yield of the bond based on specified market conventions and security structures. Model validation needs to be very careful. See https://finpricing.com/lib/FiBond.html

