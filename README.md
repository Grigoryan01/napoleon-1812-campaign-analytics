# 1812: Napoleon's Invasion of Russia — Power BI Analytics

A Power BI dashboard analyzing troop strength, attrition, and casualties during
Napoleon's 1812 campaign in Russia, comparing the Grande Armée and the Russian
Imperial Army month by month and battle by battle.

## What's in this dashboard

- **French Army page** — Grande Armée strength decline (line chart), stage-by-stage
  losses (waterfall), cumulative attrition (funnel), and losses by cause (donut).
- **Russian Army page** — Russian strength over time (area chart), reinforcements vs.
  losses per stage (clustered column), attrition rate trend (line chart), and
  remaining vs. lost headcount (clustered bar).
- **Comparison page** — both armies plotted together (combo chart), side-by-side
  attrition percentages (multi-row card), and a battle-by-battle casualty
  exchange (scatter/bubble chart).

## Data sources

Figures are order-of-magnitude estimates compiled from:
- Carl von Clausewitz, *The Campaign of 1812 in Russia*
- George Nafziger, *Napoleon's Invasion of Russia*
- Adam Zamoyski, *Moscow 1812: Napoleon's Fatal March*
- Richard Riehn, *1812: Napoleon's Russian Campaign*
- Dominic Lieven, *Russia Against Napoleon*
- Alexander Mikaberidze, *The Battle of Borodino*
- Wikipedia infoboxes (Borodino, Smolensk, Tarutino, Krasnoi, Berezina, Maloyaroslavets)

Russian-side figures are less precisely documented in the historiography than
French ones (fewer surviving muster rolls, multiple field armies merging over
the campaign, militia not always counted) — treat both sides as illustrative
estimates for comparison, not audited counts.

## Files

| File | Description |
|---|---|
| `1812.pbix` | Power BI report — all pages, visuals, and DAX measures |
| `1812_campaign_data.xlsx` | Source data (6 tables: strength timelines, battle casualties, loss causes) |

## Key measures (DAX)

- `French Attrition Percent` / `Russian Attrition Percent` — share of starting
  strength lost by campaign's end
- `French Cumulative Losses` / `Russian Cumulative Losses` — running total of
  losses by stage, for waterfall/trend visuals
- `Russian Reinforcements` — the one metric with no French equivalent: the
  Grande Armée received no meaningful reinforcement during the campaign,
  while the Russian army partially rebuilt at Tarutino

## Requirements

- Power BI Desktop (2023 or later recommended) to open `1812.pbix`

## License

Historical data compiled from public-domain and secondary sources for
educational/analytical purposes. No proprietary data included.
