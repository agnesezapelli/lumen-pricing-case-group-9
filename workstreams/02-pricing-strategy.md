# Workstream 2 — Pricing Strategy

## Key finding

The evidence supports **€2.19 per 330ml can as LUMEN’s recommended German launch price**. It is the best-supported compromise between customer acceptance, attractive contribution economics, and credible premium positioning; €1.79 is more accessible but weakens the premium and financial case, while €2.59 maximizes margin per accepted unit but creates a substantial adoption risk.

## Evidence from the data

### Competitive price position

The case places competitors in four broad bands: PulsUp mass market at €1.0–€1.3, Mate Libre heritage/niche at €1.4–€1.8, VoltFit premium performance at €2.1–€2.7, and Root & Rise boutique adaptogenic at €2.5–€3.1. The channel-level competitor file shows similar ranges: PulsUp €0.96–€1.28, Mate Libre €1.37–€1.83, VoltFit €2.10–€2.72, and Root & Rise €2.54–€3.11 across formats and channels.

At €2.19, LUMEN would sit within the premium-performance band and below the boutique-adaptogenic band. This is consistent with the brief’s desired positioning near VoltFit and Root & Rise without placing LUMEN at the very top of the market on launch.

**Sources:** `LUMEN_Case_Brief.md`; `data/competitor_prices_by_channel.csv`.

### Tested price points

The repository tests three prices. Estimated acceptance is 61.7% at €1.79, 51.7% at €2.19, and 26.7% at €2.59. Acceptance therefore falls by 10 percentage points from €1.79 to €2.19 and by a further 25 percentage points from €2.19 to €2.59.

Contribution per unit and contribution margin move in the opposite direction:

| Price | Acceptance | Contribution range | Contribution-margin range |
|---:|---:|---:|---:|
| €1.79 | 61.7% | €0.40–€0.81 | 39.2%–56.7% |
| €2.19 | 51.7% | €0.63–€1.16 | 50.3%–65.1% |
| €2.59 | 26.7% | €0.86–€1.54 | 58.0%–71.4% |

The acceptance percentage is reported identically across the three channels in `price_test_results.csv`; the data therefore supports channel-specific contribution comparisons, but not channel-specific acceptance differences.

**Source:** `data/price_test_results.csv`.

### Customer price sensitivity

Across the 300 price-sensitivity respondents, the median thresholds are €0.91 for “too cheap,” €1.44 for “cheap,” €2.21 for “expensive,” and €2.82 for “too expensive.” The recommended €2.19 price is almost exactly at the overall median “expensive” threshold and below the median “too expensive” threshold.

The segment medians show why one price cannot optimize every customer: Urban Wellness Professionals have a median “expensive” threshold of €2.79 and “too expensive” threshold of €3.50, while Students & Budget-Conscious consumers have corresponding thresholds of €1.71 and €2.21. Fitness & Gym-Goers sit between these groups at €2.52 and €3.09.

**Source:** `data/price_sensitivity_survey.csv`.

### Unit cost and channel contribution

The cost breakdown gives total COGS of €0.62 per 330ml can, including ingredients, packaging, production, freight, and Germany import-duty/compliance allowance. At the illustrative €2.19 retail price, channel economics estimate contribution of €1.16 for DTC Online, €0.63 for Retail/Grocery, and €1.13 for Gym & Office.

Retail/Grocery contribution is lower because retailer margin and distributor deductions reduce the net price to LUMEN. DTC Online has payment-processing and fulfillment costs, while Gym & Office has a different deduction structure.

**Sources:** `data/cost_breakdown.csv`; `data/channel_economics.csv`.

### Price sensitivity and target customers

The broader customer survey identifies Urban Wellness Professionals as the least price-sensitive segment, with average price sensitivity of 3.63/10, and the highest average LUMEN purchase intent at 9.12/10. Fitness & Gym-Goers have average price sensitivity of 5.44/10 and purchase intent of 7.97/10. Students & Budget-Conscious consumers are more price-sensitive at 7.93/10 and have lower purchase intent at 5.50/10.

Qualitative quotes support a premium price for clean ingredients and adaptogenic benefits among Urban Wellness Professionals, but warn that students reject €2.50 and that Fitness & Gym-Goers will not pay more merely for attractive packaging.

**Sources:** `data/customer_survey.csv`; `data/customer_quotes.csv`.

## Recommended price

### Recommended launch price: €2.19 per 330ml can

€2.19 is recommended because:

1. It retains an estimated 51.7% acceptance—materially above the 26.7% estimated at €2.59.
2. It generates materially stronger contribution and margin than €1.79 across every listed channel.
3. It places LUMEN in the premium-performance competitive band without demanding the most aggressive premium.
4. It is close to the overall median price-sensitivity “expensive” threshold but below the median “too expensive” threshold.
5. It fits the strongest initial customer groups better than €1.79 while remaining less adoption-constrained than €2.59.

The price should be treated as the central launch hypothesis, not a guaranteed optimal price. The scenario simulator should still display €1.79 and €2.59 as sensitivity cases.

**Sources:** `data/price_test_results.csv`; `data/price_sensitivity_survey.csv`; `data/competitor_prices_by_channel.csv`; `data/customer_survey.csv`; `data/customer_quotes.csv`.

## Premium-positioning rationale

€2.19 is high enough to signal a premium-performance proposition relative to PulsUp and Mate Libre, but it remains below the upper boutique-adaptogenic range represented by Root & Rise. It therefore supports a “clean, functional, credible premium” position rather than a luxury or highly exclusive position.

The price should be supported by evidence of natural caffeine, adaptogen functionality, and good taste. The customer quotes indicate that clean ingredients and adaptogens can justify paying more for Urban Wellness Professionals, while Fitness & Gym-Goers require demonstrated performance and taste. Pricing alone cannot create premium positioning.

**Sources:** `LUMEN_Case_Brief.md`; `data/competitor_prices_by_channel.csv`; `data/customer_quotes.csv`.

## Assumptions and risks

### Facts directly supported by the repository

- €1.79, €2.19, and €2.59 are the tested candidate prices.
- Acceptance declines as price rises in the supplied price-test results.
- Contribution per unit and contribution margin increase as price rises.
- Unit COGS is €0.62 per can.
- Channel deductions materially change LUMEN’s net price and contribution.
- Competitor pricing places €2.19 near premium-performance competitors.
- The price-sensitivity survey contains approximately 300 respondents and provides four thresholds per respondent.

**Sources:** `data/price_test_results.csv`; `data/cost_breakdown.csv`; `data/channel_economics.csv`; `data/competitor_prices_by_channel.csv`; `data/README_data.md`.

### Assumptions used for this recommendation

- Survey acceptance is directionally useful for Germany’s initial price decision.
- The price-test contribution figures are sufficiently comparable across channels for scenario analysis.
- LUMEN can substantiate its clean-label, natural-caffeine, adaptogen, and taste claims.
- A balanced price is preferable for a first launch because German sales history does not exist.

### Risks and missing information

- There is no German sales data, so actual conversion, repeat purchase, and volume response are uncertain.
- The price-test acceptance measure is survey-derived and not a controlled German market launch.
- Acceptance is not differentiated by channel in the supplied price-test file.
- The data does not quantify how price changes affect brand perception or long-term willingness to pay.
- The data does not provide retailer listing fees, promotional funding, minimum order quantities, or city-specific channel terms.
- The price-sensitivity survey has fewer observations in some segments than the customer survey, and its thresholds are not necessarily purchase probabilities.
- Contribution per unit does not include marketing CAC; price profitability must ultimately be evaluated together with acquisition cost, volume, and LTV.
- The premium recommendation could underperform if taste, availability, or functional credibility is weak.

## Sources / datasets used

- `LUMEN_Case_Brief.md`
- `README.md`
- `data/README_data.md`
- `data/competitor_prices_by_channel.csv`
- `data/competitor_price_history.csv`
- `data/price_sensitivity_survey.csv`
- `data/price_test_results.csv`
- `data/cost_breakdown.csv`
- `data/channel_economics.csv`
- `data/customer_survey.csv`
- `data/customer_quotes.csv`

`marketing_funnel_monthly.csv`, `historical_sales_weekly.csv`, `market_context.csv`, and `seasonality_and_weather.csv` were not used for the core price recommendation because they address acquisition, existing-market sales, market sizing, and timing rather than directly estimating German willingness to pay or price/channel contribution. They should be combined with this recommendation in later workstreams.
