# Oil & Gas Stock Pitch: Aker BP (Ticker: AKRBF)

## Objective:
- Identify relevant KPIs and drivers
- Identify potential alternative data sources to approximate KPIs and drivers
- Develop proof-of-concept
- Summarize process, assumptions, relevancy and potential investment strategy

### Company Overview:
Aker BP ASA is a Norwegian oil exploration and development company focused on the production of oil and gas on the Norwegian Continental Shelf.
As of October 2023, the company operates 6 assets in the NCS (Alvheim, Ivar Aasen, Skarv, Edvard Grieg, Ula and Valhall) and is in a strategic partnership with Equinor Energy AS over the management of the largest field in the NCS (Johan Sverdrup).

### Reported KPIs:
- Production Volume: net petroleum production (mboepd), production cost (USD/boe), net liquid volumes sold (mboepd), net natural gas volumes sold (mboepd)
  - Alternative Data Sources: real-time satellite imagery of assets, real-time weather tracking, number of operational sites, number of newly active wells, number of wells in exploratory phase, number of abandoned sites, production volume per active rig
- Operating Costs: capital expenditure (capex), exploration expenditure (expex), abandonment expenditure (abex)
  - Alternative Data Sources: real-time satellite imagery of oil and gas fields, number of new wells drilled, success rate of exploratory wells

### Industry Drivers:
- Expectations of future oil and gas prices
- Increased crude oil demand → higher prices → increased drilling activity
- The number of wells planned
- The number of active drilling rigs and rig utilization rates (i.e. the # of active drilling rigs used by an oil company as a % of its total fleet)
-   Generally, there is a positive relationship between RUR and company revenues
- Rig selection (onshore vs. offshore)
  - Supply of offshore rigs is inelastic given the higher costs compared to onshore rigs

### Competitive Landscape
- Compared to a selection of industry peers (i.e. EQT, MRO, TPL, CTRA, OVV), AKRBF leads across a number of profitability metrics in FY2022:
  - Gross Profit Margin: 93.69%
  - EBITDA Margin: 91.13%
  - Levered FCF Margin: 40.07%
  - Return on Total Capital: 38.67%
  
### Risks & Confounding Variables
- Impact of geopolitical conflicts on OPEC+ production and global oil prices
- U.S. approaching critical levels of its Strategic Petroleum Reserve (SPR)
- Growing adoption of electric vehicles amongst Norwegian consumers
- M&A activity within the oil & gas industry (e.g. Chevron-Hess)

## Why does this matter?
Real-time satellite and weather data feeds can help assess whether under normal weather and drilling conditions, the company’s output guidance is achievable. For example, leveraging Sentinel-2 satellite images of Aker BP’s offshore rig in Valhall, we can approximate how many barrels of oil equivalents (in million Sm3) the site produces each quarter based on the number of ships that arrive at the rig on a weekly or monthly basis. We can then conduct this analysis at scale by tracking satellite imagery of all Aker BP drilling sites and aggregating the # of ship sightings on a quarterly basis to determine whether or not AKRBF will meet its net production volume figures (mboepd). 

Some other important data points include the number of operational drilling rigs, the number of newly active wells, the number of wells in exploration and the number of abandoned sites. If we have both the number of active drilling rigs and total production volumes at Aker BP sites over time, we can then compute a sales/production per active rig metric which can serve as a benchmark for how much AKRBF should be producing on a monthly and/or quarterly basis given our knowledge of the number of operational sites. 

Similarly, the number of newly discovered wells and the number of abandoned sites can feed directly into an investor’s model inputs - specifically, capital and exploratory/abandonment expenditures. See below for a chart which plots AKER BP’s total annual investments (NOK) in its fields through 2021 - from here, we can use historical investments as an input to build forecasts which predict capex line items and assess whether or not the company will be profitable in a given quarter.

Outside of supply metrics, it is important to account for local and global demand for Aker BP oil and natural gas products. For example, there has been a gradual uptick in total road traffic data (in million km) in Norway from 2015 onwards. Similarly, the seasonally-adjusted proportion of wallet spend at the pump (as measured by the Norwegian household consumption index) has gradually declined - apart from a sharp spike in late 2022 - since first being tracked two years ago. Understanding the macroeconomic dynamics that underpin Norwegian oil consumption is important to determine whether oil demand is robust enough to sustain Aker BP’s guidance for net liquid and natural gas volumes sold (mboepd).

So why does this matter? The key is whether the real-time satellite/weather imagery and other sources of alternative data imply whether AKRBF will beat or fall short enough of quarterly guidance such that they have to adjust their full-year guidance, which would cause the stock to fluctuate greatly and affect earnings per share (EPS). Conversely, even if the company meets and/or beats output targets in unfavorable drilling/market conditions that then implies that there was an incremental capex spend (either in the form of newly active sites or exploratory wells) which summarily affects free cash flow (FCF). In other words, performance against guidance will either impact EPS or FCF which ultimately impacts valuation (i.e. what multiples of earnings or FCF the ticker should trade at). Taking into account all of these alternative data sources as approximations for company reported KPIs, if the investor has enough conviction around risks of big beats/misses, then the potential recommendation would be to either shift directional views on AKRBF or to leverage options to hedge any tail risk.

## Assumptions
Throughout my analysis, I made a number of assumptions about oil field productions, revenues and capital expenditures in the instances where a field was co-owned by 2 or more operators. 

The Norwegian Petroleum Directorate regularly updates its database with the percentages of ownership for each drilling operator at a given field. For example, in October 2004, Aker BP had 80% ownership of the Alvheim field while ConocoPhillips Skandinavia owned the remaining 20%. As such, in order to compute Aker BP’s total net oil equivalent production (in million Sm3), I multiplied the total net production per site by Aker BP’s company share percentage. Similarly, I multiplied total investment (in NOK) per site by Aker BP’s company share of the site to compute Aker BP’s total investment in that site. Lastly, I applied the same computation to calculate Aker BP’s total reserves at each operational site.
Across the different Norwegian petroleum databases, there was no standard approach to classifying whether a site was in an exploratory or abandoned phase. As such, I mapped all sites on the Norwegian Petroleum Directorate with an activity status of “Production likely, but unclarified” as “Exploratory” and those with “Production not evaluated” as “Abandoned”.  

Lastly, I retrieved Norway’s household consumption index from Statistics Norway to measure the percentage of their wallets that Norwegian consumers have spent at the pump over time. There are two caveats associated with this index:
  - Firstly, these are seasonally-adjusted figures which have been normalized such that reported figures in 2005 are the baseline (i.e. 100). Therefore, we can interpret that any increase represents a higher proportion of wallet spend for a given expense category.
  - Secondly, consumer spending at the pump fell under the “Purchases of vehicles and petrol” category, therefore, any overall changes in trends may not be directly attributable to petrol spending alone.

## Next Steps:

1. Conduct deeper dive into weather pattern data in Norwegian Continental Shelf from MET Norway
2. Incorporate Q3 earnings results (October 27th, 2023)
3. Run backtests of approximations against previously reported earnings figures
