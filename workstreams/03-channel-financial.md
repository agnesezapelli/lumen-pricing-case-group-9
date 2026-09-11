# Workstream 3 — Channel and Financial Analysis

## Key finding

LUMEN should use a **DTC-led, Gym & Office-supported, selectively distributed Retail/Grocery launch**. DTC Online and Gym & Office provide the strongest unit contribution at the recommended €2.19 price, while Retail/Grocery provides the strongest historical sales scale but the weakest contribution per unit. Marketing should prioritize Referral / Subscription for efficient acquisition, use Influencer / Content as a supporting acquisition and brand channel, and use Retail Sampling selectively to create trial rather than treating it as the most efficient acquisition source.

An exact Germany channel percentage cannot be established from the repository because there is no German sales data, German channel CAC, channel-specific German conversion data, or channel capacity information.

## Evidence from the data

### LUMEN’s channel economics

At the illustrative €2.19 retail price, `channel_economics.csv` reports the following contribution economics:

| Sales channel | Net price to LUMEN | Unit contribution | Contribution margin |
|---|---:|---:|---:|
| DTC Online | €1.78 | €1.16 | 65.1% |
| Gym & Office | €1.75 | €1.13 | 64.6% |
| Retail/Grocery | €1.25 | €0.63 | 50.3% |

DTC Online and Gym & Office therefore generate approximately €0.53 more contribution per unit than Retail/Grocery at €2.19. Retail/Grocery’s lower economics reflect retailer margin and distributor deductions; DTC Online includes payment processing and fulfillment costs.

**Sources:** `data/channel_economics.csv`; `data/price_test_results.csv`.

### Existing-market sales scale

The 78-week historical dataset covers the Netherlands, Denmark, and Sweden—not Germany. Across those markets, Retail/Grocery represents approximately 50.0% of units, DTC Online 32.2%, and Gym & Office 17.8%. Average weekly units across the available country-channel rows are approximately 2,571 for Retail/Grocery, 1,641 for DTC Online, and 918 for Gym & Office.

This demonstrates that Retail/Grocery has historically delivered the most volume, but it does not demonstrate that the same mix or scale will occur in Germany.

**Source:** `data/historical_sales_weekly.csv`; the non-German limitation is stated in `data/README_data.md`.

### Marketing acquisition economics

Aggregated across the 18 months in `marketing_funnel_monthly.csv`, the acquisition channels show:

| Marketing channel | Spend | Customers acquired | CAC | Average estimated LTV | LTV:CAC |
|---|---:|---:|---:|---:|---:|
| Referral / Subscription | €322,241 | 11,452 | €28.14 | €81.39 | 2.89 |
| Influencer / Content | €84,733 | 2,258 | €37.53 | €100.82 | 2.69 |
| Paid Social | €43,589 | 952 | €45.79 | €132.13 | 2.89 |
| Retail Sampling | €726,327 | 12,080 | €60.13 | €174.17 | 2.90 |

Referral / Subscription has the lowest CAC and the highest number of acquired customers. Retail Sampling has the highest CAC and highest spend, but also the highest estimated LTV. Influencer / Content has the lowest aggregate LTV:CAC in this dataset, while Paid Social and Retail Sampling are close to the repository’s stated 3:1 target but do not exceed it.

**Sources:** `data/marketing_funnel_monthly.csv`; `LUMEN_Case_Brief.md`.

The marketing channels are not identical to the sales channels. Treating Referral / Subscription as a DTC proxy or Retail Sampling as a Retail/Grocery proxy is a planning assumption, not a directly measured relationship in the data.

### Acquisition, profitability, and payback trade-off

The data shows two different economic layers:

1. **Sales-channel contribution:** what LUMEN earns per unit after channel deductions, where DTC Online and Gym & Office are stronger than Retail/Grocery at €2.19.
2. **Marketing acquisition economics:** what it costs to acquire customers and their estimated LTV, where Referral / Subscription has the lowest CAC and Retail Sampling has the highest CAC but high estimated LTV.

The repository does not provide customers acquired by German sales channel, units per acquired customer, repeat-purchase timing, gross-profit-based LTV, or a defined payback period. Consequently, an exact contribution-after-CAC or months-to-payback calculation would require assumptions not supported by the repository.

**Sources:** `data/channel_economics.csv`; `data/marketing_funnel_monthly.csv`; `data/historical_sales_weekly.csv`; `data/README_data.md`.

## Recommended channel mix

### Strategic recommendation

- **DTC Online — prioritize:** Use as the economic and relationship anchor. It has €1.16 unit contribution at €2.19, the highest listed sales-channel contribution, and is the preferred channel for the strongest target segment, Urban Wellness Professionals. Use Referral / Subscription as the main acquisition lever where the mapping is operationally appropriate.
- **Gym & Office — build selectively:** Use for Fitness & Gym-Goers, performance credibility, and trial. It has €1.13 unit contribution at €2.19 and is the preferred channel for Fitness & Gym-Goers. Partnerships and sampling should prove incremental demand because the quotes warn that gyms already carry several energy drinks.
- **Retail/Grocery — use for targeted reach and scale:** Do not exclude it: it represented 50.0% of historical units in LUMEN’s existing markets. However, its €0.63 unit contribution at €2.19 is materially lower, so launch selectively in locations where availability and trial justify the economics rather than assuming national retail distribution from day one.

### Practical launch design

The evidence supports a **DTC-led and Gym & Office-supported pilot, with selective Retail/Grocery availability**. Retail Sampling should be used as a targeted trial mechanism near the selected retail or gym locations, not automatically scaled according to its historical spend.

If the simulator needs a numerical starting mix, a provisional **40% DTC Online / 25% Gym & Office / 35% Retail/Grocery** unit mix can be used only as an explicit scenario assumption. Those percentages are not observed German forecasts and should be editable, stress-tested, and clearly labeled.

**Sources:** `data/channel_economics.csv`; `data/historical_sales_weekly.csv`; `data/marketing_funnel_monthly.csv`; `data/customer_survey.csv`; `data/customer_quotes.csv`.

## ROI and payback logic

The simulator should calculate, for each editable price/channel/mix scenario:

- Units and revenue by sales channel.
- Net revenue to LUMEN by channel.
- Contribution per unit and total contribution.
- Marketing spend by acquisition channel.
- CAC, acquired customers, estimated LTV, and LTV:CAC.
- Contribution after marketing spend as a scenario metric.
- A payback proxy, clearly labeled as such, unless the team later adds a supported time-to-repurchase assumption.

The most defensible current conclusion is that Referral / Subscription is the first marketing channel to test for efficient acquisition because its observed CAC is €28.14, compared with €37.53 for Influencer / Content, €45.79 for Paid Social, and €60.13 for Retail Sampling. Retail Sampling may still be justified for launch trial because its estimated LTV is highest at €174.17, but its €60.13 CAC and high spend require controlled testing.

LTV:CAC should not be described as payback period. The supplied data gives cumulative estimated LTV and CAC, but not the timing of cash flows. The target LTV:CAC ratio of approximately 3:1 is a planning benchmark, not proof that the German launch will pay back within a particular number of months.

**Sources:** `data/marketing_funnel_monthly.csv`; `LUMEN_Case_Brief.md`.

## Assumptions and risks

### Facts directly supported by the repository

- DTC Online and Gym & Office have higher €2.19 unit contribution than Retail/Grocery.
- Retail/Grocery has the largest historical unit share in the Netherlands, Denmark, and Sweden.
- Referral / Subscription has the lowest observed marketing CAC in the 18-month funnel data.
- Retail Sampling has the highest observed marketing CAC, spend, and estimated LTV among the listed acquisition channels.
- There is no German sales data in the repository.

**Sources:** `data/channel_economics.csv`; `data/historical_sales_weekly.csv`; `data/marketing_funnel_monthly.csv`; `data/README_data.md`.

### Assumptions used for this recommendation

- Existing-market sales-channel patterns are directionally useful for identifying a retail-scale opportunity, but not for forecasting German volume.
- Referral / Subscription can be used to support DTC Online acquisition.
- Retail Sampling can support trial in or near Retail/Grocery and Gym & Office placements.
- A phased, selective retail launch is more appropriate than assuming national retail scale before German evidence exists.
- The provisional 40% / 25% / 35% mix is a scenario input, not a data-derived forecast.

### Risks and missing information

- No German channel demand, conversion, retention, or repeat-purchase data.
- No customer-level link between marketing source, sales channel, units purchased, and LTV.
- No time dimension for LTV, so actual payback period cannot be calculated.
- No German retailer terms, listing fees, distributor terms, trade promotion costs, or channel capacity.
- Historical sales contain duplicate rows and an unusual spike week, requiring quality controls before using them as a benchmark.
- Marketing channel results may reflect different scale and targeting decisions; observed CAC is not necessarily causal or transferable to Germany.
- The data does not establish whether DTC can scale to the required German volume or whether gyms can provide sufficient distribution.

## Sources / datasets used

- `LUMEN_Case_Brief.md`
- `data/README_data.md`
- `data/channel_economics.csv`
- `data/marketing_funnel_monthly.csv`
- `data/historical_sales_weekly.csv`
- `data/price_test_results.csv`
- `data/customer_survey.csv`
- `data/customer_quotes.csv`
- `data/cost_breakdown.csv`

`competitor_prices_by_channel.csv`, `competitor_price_history.csv`, `price_sensitivity_survey.csv`, `market_context.csv`, and `seasonality_and_weather.csv` were not used for the core channel-financial recommendation; they belong primarily to pricing, customer/market, or timing analysis and should be incorporated into the full simulator in later workstreams.
