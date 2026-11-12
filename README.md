# How fast are European companies adopting AI, and what holds them back?

*Team project · Ironhack Data Analytics Bootcamp · Python, pandas, REST API, Matplotlib*

## At a glance

| | |
|---|---|
| **Business question** | Which European countries lead in company AI adoption, how fast is it growing, and what stops companies from using it? |
| **Data** | Eurostat *Enterprise AI adoption* (`isoc_eb_ai`), pulled live from the Eurostat REST API · companies with 10+ employees · 2021–2025 · 30+ European countries |
| **Main result** | The average adoption rate across countries **almost tripled**, from **7.0% (2021) to 19.3% (2025)** |
| **Biggest barrier** | **Lack of expertise**: about **70%** of companies that considered AI but didn't adopt it named it as a reason |

## Key findings

- **Adoption is speeding up.** The average share of companies using AI went from 7.0% in 2021 to 7.8% in 2023, 13.4% in 2024 and 19.3% in 2025. Most of the growth happened in the last two years.
- **The Nordics and Benelux lead.** Denmark (42.0%), Finland (37.8%) and Sweden (35.0%) top the 2025 ranking. **The Netherlands ranks 6th** (33.2%), ahead of Germany (26.0%).
- **Skills, not money, are the main barrier.** Among companies that considered AI but don't use it, the most common reasons are lack of expertise (~70%), legal uncertainty (~50%) and privacy concerns (~49%). High cost comes last (~41%).

## What this means for a business

- **Training and hiring beat budget.** The main reason companies hold back is a lack of people who know how to use AI, so upskilling staff is likely to unlock more adoption than extra spending.
- **Clear rules and privacy guidance matter.** Legal uncertainty and privacy are the next two barriers, so compliance and data-protection support are part of any AI rollout.
- **Benchmark against peers.** A Dutch company can compare itself with the national average (33%) and with the leading countries to judge whether it is falling behind.

## How it was built

1. **Collect:** wrote a reusable Python function that queries the Eurostat REST API for 7 indicators (adoption, use in marketing, and 5 barriers).
2. **Wrangle:** merged the indicators into one tidy table of 132 rows (country × year × 10 columns), checked missing values (barrier questions are not asked every year) and sorted it for analysis.
3. **Analyse:** ranked countries, tracked the yearly trend and compared barriers.
4. **Share:** presented the results to the class as a team.

## Files

| File | What it does |
|---|---|
| `dataset.ipynb` | API calls, merging, cleaning and the analysis above |
| `AI-Jobplacement.ipynb` | Charts for the presentation |

## Notes and limits

- Averages are simple averages across countries, not weighted by the number of companies.
- Barrier questions are only asked of companies that **considered** AI but did not adopt it, and not in every year.
- The data shows links and trends, not causes.

## Team

Team project with Pumikako, Stefano Marchiori and Lervin de la Rosa.

**Data source:** Eurostat, *Artificial intelligence by size class of enterprise* (`isoc_eb_ai`).
