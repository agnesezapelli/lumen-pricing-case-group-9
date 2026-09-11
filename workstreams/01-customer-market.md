# Workstream 1 — Customer and Market Analysis

## Scope

This workstream identifies LUMEN’s most attractive German target customers and launch-city priority using the German market context, customer survey, price-sensitivity survey, qualitative quotes, and competitor evidence.

## Key findings

### Germany is an attractive category, with direct relevance to LUMEN

The case describes a German functional-beverage market of approximately €9.1 billion in 2026, with category CAGR of about 7% through 2033. The 2026 market-context data estimates €2.548 billion for Energy / focus and €2.184 billion for Plant-based / adaptogenic—both relevant to LUMEN’s natural green-tea caffeine and adaptogen proposition.

**Sources:** `LUMEN_Case_Brief.md`; `data/market_context.csv`.

**Assumption / risk:** These are category-level figures, not LUMEN’s addressable market or forecast share. The market-context notes describe the regional allocation as illustrative and cite external market research without providing its full methodology.

### Urban Wellness Professionals are the primary target

Urban Wellness Professionals have the strongest customer indicators in `customer_survey.csv`: average LUMEN purchase intent of 9.12/10, the lowest average price sensitivity of 3.63/10, average monthly beverage spend of €21.73, and average purchase frequency of 7.56 per month. DTC Online is their most common preferred channel, with 60 of 112 respondents selecting it. Their highest recorded competitor awareness is Root & Rise at 65%, consistent with LUMEN’s opportunity to compete in a premium/adaptogenic space.

The qualitative evidence supports this direction: these customers say they will pay more for clean ingredients and are motivated by the adaptogen angle. However, one quote identifies taste as a major risk, describing wellness drinks that taste like medicine.

**Sources:** `data/customer_survey.csv`; `data/customer_quotes.csv`; `LUMEN_Case_Brief.md`.

**Assumption / risk:** Purchase intent is survey-based and may not translate into actual trial, conversion, or repeat purchase. Taste acceptance is not measured in the supplied data.

### Fitness & Gym-Goers are the strongest secondary target

Fitness & Gym-Goers have average LUMEN purchase intent of 7.97/10 and average price sensitivity of 5.44/10. Gym & Office is their most common preferred channel, with 37 of 83 respondents selecting it. Awareness of VoltFit, the premium-performance competitor, is 77% in this segment.

The quotes indicate a credible switching opportunity if LUMEN performs like VoltFit and tastes better. They also show a distribution barrier: gyms already sell several energy drinks, so LUMEN needs a clear reason to earn shelf space.

**Sources:** `data/customer_survey.csv`; `data/customer_quotes.csv`; `LUMEN_Case_Brief.md`.

**Assumption / risk:** Interest does not prove that gyms will list LUMEN or that consumers will repurchase. No gym-level sell-through, listing-fee, or distribution-access data is provided.

### Students & Budget-Conscious consumers should not be the initial core audience

Students & Budget-Conscious consumers have the lowest average purchase intent at 5.50/10 and the highest average price sensitivity at 7.93/10. Their preferred channel is mainly Retail/Grocery, with 73 of 135 respondents selecting it. Their quotes emphasize promotions, affordability, and buying only when a usual alternative is unavailable.

On-the-go Commuters are a possible later expansion segment: their average purchase intent is 6.71/10 and 54 of 90 respondents prefer Retail/Grocery. Their qualitative evidence emphasizes convenience, habit, kiosk availability, and taste rather than a strong LUMEN-specific reason to switch.

**Sources:** `data/customer_survey.csv`; `data/customer_quotes.csv`.

**Assumption / risk:** These segments could still generate volume, but the available evidence does not show that they will support premium pricing or strong early repeat purchase.

## City analysis

### Berlin is the recommended primary launch city

Berlin has the largest explicit city market share in `market_context.csv` at 18% and an illustrative regional CAGR of 9%. It is also the largest city sample in `customer_survey.csv`, with 81 respondents and average LUMEN purchase intent of 7.40/10. Berlin contains 27 Urban Wellness Professionals—the largest city count for the primary target—and 14 Fitness & Gym-Goers.

Berlin therefore offers the best combined starting hypothesis across market scale, illustrative growth, sample size, and target-segment presence.

**Sources:** `data/market_context.csv`; `data/customer_survey.csv`.

**Assumption / risk:** The city market shares and regional CAGR values are explicitly illustrative. Berlin’s survey results are directional and do not establish city-level profitability, conversion, or repeat purchase.

### Hamburg and Munich are the strongest follow-on tests

Hamburg has the highest overall city purchase intent in the survey at 7.52/10 and particularly strong Urban Wellness Professionals intent at 9.6/10. Munich has the highest Fitness & Gym-Goers intent at 8.7/10. Both Berlin and Munich have an illustrative regional CAGR of 9%, compared with 7% for Hamburg, Cologne, Frankfurt, and Other Germany.

**Sources:** `data/customer_survey.csv`; `data/market_context.csv`.

**Assumption / risk:** The city samples are uneven—Berlin has 81 respondents, Hamburg 48, and Munich 57—so small differences in average intent should not be treated as statistically conclusive. No city-specific CAC, retailer access, distribution cost, or competitor-sales data is available.

## Recommendation

Use a phased launch priority:

1. **Berlin:** primary launch city.
2. **Hamburg:** follow-on or wellness-focused test city because of its strongest overall city intent and high Urban Wellness Professionals intent.
3. **Munich:** targeted premium-performance test city for Fitness & Gym-Goers.

Make **Urban Wellness Professionals** the primary audience, with messaging around clean ingredients, natural energy, and credible functional benefits. Use **Fitness & Gym-Goers** as the secondary audience, supported by Gym & Office partnerships and sampling that proves performance and taste.

Do not make Students & Budget-Conscious consumers the initial core audience. Treat On-the-go Commuters as a later expansion opportunity once LUMEN has strong convenience-store, kiosk, or other grab-and-go availability.

## Implications for the scenario simulator

The initial default scenario should be:

- City: Berlin
- Primary segment: Urban Wellness Professionals
- Secondary segment: Fitness & Gym-Goers
- Expansion tests: Hamburg for wellness professionals; Munich for fitness-oriented consumers

The simulator should show city and segment composition, not just rank cities by average purchase intent. It should expose uncertainty around survey-to-purchase conversion, repeat purchase, taste acceptance, channel access, and city economics rather than presenting the recommendation as a proven forecast.

## Sources used

- `README.md`
- `LUMEN_Case_Brief.md`
- `data/README_data.md`
- `data/market_context.csv`
- `data/customer_survey.csv`
- `data/customer_quotes.csv`
- `data/price_sensitivity_survey.csv` (available for follow-up price-by-segment analysis; this workstream does not infer unsupported segment-specific price thresholds)
- `data/competitor_prices_by_channel.csv`
- `data/competitor_price_history.csv`
- `AGENTS.md` (repository workflow requirements only)
