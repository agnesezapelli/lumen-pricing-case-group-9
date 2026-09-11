# Workstream 5 — Consulting Story and Quality Control

## Executive recommendation

LUMEN should enter Germany with a focused, testable launch scenario rather than a national volume forecast:

| Decision | Recommendation | Evidence status |
|---|---|---|
| City | Berlin first; Hamburg and Munich as follow-on tests | Berlin’s 18% illustrative city share, 9% illustrative CAGR, 81 survey respondents, and largest primary-target count; city economics remain unknown |
| Primary target | Urban Wellness Professionals | Highest average purchase intent (9.12/10), lowest average price sensitivity (3.63/10), and strongest DTC preference |
| Secondary target | Fitness & Gym-Goers | 7.97/10 average intent, Gym & Office preference, and 77% VoltFit awareness |
| Price | €2.19 per 330ml can | Supported price-test point with 51.7% estimated acceptance and balanced contribution/premium positioning |
| Sales channels | DTC-led, Gym & Office-supported, selective Retail/Grocery | DTC and Gym & Office provide €1.16 and €1.13 contribution per unit at €2.19; Retail/Grocery provides reach but €0.63 contribution |
| Marketing priority | Referral / Subscription first; controlled Influencer / Content and Retail Sampling tests | Historical benchmark CAC of €28.14 for Referral / Subscription versus €60.13 for Retail Sampling |
| Main risk | Actual German conversion, repeat purchase, and channel scalability may differ from the evidence | No German sales or customer-level attribution exists |
| Main assumption | German survey and existing-market benchmarks are directionally transferable to a pilot | Must be validated through a measured launch test |

## The consulting story

LUMEN’s decision is not simply whether Germany is attractive; it is how to enter while reconciling premium brand-building with fast, credible financial learning. Germany is described as a €9.1bn 2026 functional-beverage market with approximately 7% category CAGR, and the relevant 2026 subcategories are Energy / focus (€2.548bn) and Plant-based / adaptogenic (€2.184bn). These figures establish category attractiveness, not LUMEN’s forecast share.

The best initial customer evidence points to Urban Wellness Professionals: they combine the highest purchase intent, lowest price sensitivity, highest beverage spend, highest purchase frequency, and strong DTC preference in the German survey. Fitness & Gym-Goers are a sensible second audience because their intent is strong, Gym & Office is their leading preferred channel, and their qualitative feedback supports switching if LUMEN proves performance and taste.

Berlin is the most defensible first city because it has the largest illustrative city market share, an illustrative 9% regional CAGR, the largest survey sample, and the largest number of Urban Wellness Professionals in the survey. Hamburg is a strong wellness-oriented follow-on test and Munich is a strong fitness-oriented test, but neither city has enough evidence to establish superior profitability.

€2.19 is the balanced price hypothesis. €1.79 has higher estimated acceptance (61.7%) but lower contribution and weaker premium signaling; €2.59 has higher contribution and margin but acceptance falls to 26.7%. At €2.19, acceptance is estimated at 51.7%, and the price sits in the premium-performance competitive range while remaining below the upper boutique-adaptogenic range.

The channel answer should separate reach from economics. DTC Online and Gym & Office produce the strongest listed contribution at €2.19, while Retail/Grocery represented 50.0% of historical units in LUMEN’s Netherlands, Denmark, and Sweden sales. Therefore, LUMEN should use DTC as the economic and relationship anchor, Gym & Office for targeted performance-led trial, and selective Retail/Grocery for reach. Referral / Subscription is the most efficient historical acquisition benchmark, while Retail Sampling may be useful for trial but has the highest CAC and should be tested rather than scaled automatically.

This balances the CMO and CFO perspectives: premium price and focused audiences support brand credibility and willingness to pay; DTC/Gym contribution and efficient acquisition support financial discipline; selective retail prevents the company from sacrificing contribution before German demand is proven.

**Sources:** `LUMEN_Case_Brief.md`; `data/market_context.csv`; `data/customer_survey.csv`; `data/customer_quotes.csv`; `data/price_test_results.csv`; `data/price_sensitivity_survey.csv`; `data/competitor_prices_by_channel.csv`; `data/channel_economics.csv`; `data/historical_sales_weekly.csv`; `data/marketing_funnel_monthly.csv`; Workstreams 1–3; `dashboard/`.

## Evidence consistency audit

### Prices and acceptance

- Dashboard options are restricted to €1.79, €2.19, and €2.59, matching `price_test_results.csv`.
- Acceptance is 61.7%, 51.7%, and 26.7%, respectively, matching the source dataset.
- Acceptance is not differentiated by channel because the source file reports the same acceptance percentage for each channel at a given price.

### Contribution and margin

At €2.19, the source values are DTC Online €1.16 contribution and 65.1% margin, Retail/Grocery €0.63 and 50.3%, and Gym & Office €1.13 and 64.6%. The dashboard calculates weighted contribution as the channel-mix-weighted contribution per unit and weighted margin as weighted contribution divided by weighted net price. These are derived unit economics, not total German profit.

### CAC, LTV, and payback

The dashboard uses historical benchmark values from `marketing_funnel_monthly.csv`: Referral / Subscription CAC €28.14 and LTV:CAC 2.89; Influencer / Content €37.53 and 2.69; Paid Social €45.79 and 2.89; Retail Sampling €60.13 and 2.90. The dashboard labels these as benchmarks and does not claim a German payback period. This is correct because the repository contains no LTV timing, repeat-purchase intervals, or customer-level attribution.

### Segments, cities, and competitors

The dashboard’s segment and city values match the aggregate calculations documented in Workstream 1 and the underlying `customer_survey.csv` and `market_context.csv`. Berlin is highlighted as the default city, Urban Wellness Professionals as the default segment, and €2.19 as the default price. Competitor bands are drawn from `competitor_prices_by_channel.csv` and the case brief.

### Issue corrected

The original dashboard recommendation sentence always described DTC Online as the economic anchor, even when a user set the DTC mix to zero. `dashboard/app.js` now derives the channel wording from the selected mix and warns when the mix does not total 100%, making the recommendation text consistent with the inputs.

## Data privacy and data quality review

- `data/customer_survey.csv` contains names and email-style fields. The dashboard does not load or expose these fields; it uses aggregate segment and city values only.
- `data/customer_quotes.csv` contains no names or contact details. Only selected business-relevant, privacy-safe quotes are shown.
- `historical_sales_weekly.csv` contains duplicate rows and an unusual spike week, as noted in `data/README_data.md`; historical benchmarks must be quality-controlled before forecasting.
- The repository describes the data as synthetic or illustrative in several places. Survey intent, market shares, regional CAGR, estimated LTV, and price-test acceptance should therefore be treated as directional evidence.
- No external API, customer-level database, or raw survey endpoint is used by the dashboard.

## Facts, calculations, assumptions, and unknowns

### Fully supported facts

- The three tested prices and their acceptance/contribution values.
- Channel net prices and contribution economics.
- Customer-segment survey indicators and preferred channels.
- Illustrative city market shares and regional CAGR values.
- Historical existing-market sales channel shares.
- Historical marketing CAC and estimated LTV values.

### Calculated or derived metrics

- Weighted channel-mix net price.
- Weighted contribution per unit.
- Weighted contribution margin.
- Historical CAC derived as spend divided by acquired customers.
- LTV:CAC derived as estimated LTV divided by CAC.
- Aggregate segment and city averages.

### Assumptions

- German survey responses are directionally useful for pilot targeting.
- Existing-market channel mix is directionally useful for identifying scale potential.
- Historical marketing CAC/LTV benchmarks may inform initial tests.
- Referral / Subscription can support a DTC-led strategy, and sampling can support physical-channel trial.
- The provisional 40% DTC / 25% Gym & Office / 35% Retail/Grocery mix is a scenario input, not a forecast.

### Unknowns

- German sales volume, revenue, market share, repeat purchase, retention, and city-level profitability.
- German channel capacity, retailer terms, listing fees, trade spend, and distribution costs.
- Customer-level marketing attribution and time-to-payback.
- Causal price elasticity, taste acceptance, and the effect of promotions on long-term demand.

## Submission-readiness assessment

The project is **analytically ready for review, but not fully submission-ready until the branch is pushed, the pull request is reviewed and merged, and the dashboard is tested in a normal browser after deployment**. The management recommendation is coherent across Workstreams 1–4, the unsupported financial claims have been removed or labeled, and the key dashboard inconsistency has been corrected.

Remaining risks before submission are remote branch synchronization, final browser/deployment QA, validation of dashboard calculations with a stakeholder, and confirmation that the team has merged all approved workstream branches into the final graded branch.
