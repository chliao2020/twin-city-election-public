# Twin City Election Public Forecasts

This repository is a public archive of the latest forecast outputs for the 2026 Taipei and New Taipei mayoral elections. It is not a full application or model codebase; it is the reporting layer: a set of generated charts, plain-language summaries, and social-ready updates produced by a forecasting workflow.

The goal is simple: to make the model output transparent, easy to inspect, and easy to share. If you are browsing the repository, you should be able to understand what the model is saying at a glance, how the forecast evolved over time, and when it was published.

## What is happening here

The outputs in this repo are generated from a hierarchical Bayesian state-space forecasting model that blends polling data, smooths undecided voters, and estimates candidate win probabilities with uncertainty bands. The model also examines retrospective fit and cross-city relationships between Taipei and New Taipei, which helps stabilize the estimates when the two political markets are strongly linked.

In other words: this is a compact public record of election forecasting results, not a campaign database or a software product with operational features.

## What to look at first

Start with the plain-language forecast summary:

- `results/Taipei_NewTaipei_fb_post.txt` — the latest social-post style update with candidate percentages, uncertainty ranges, and a short explanation of the model

Then open the visual outputs:

- `results/Taipei_forecast_dashboard.png` — Taipei forecast dashboard
- `results/NewTaipei_forecast_dashboard.png` — New Taipei forecast dashboard
- `results/Taipei_Retrospective_vs_Actual_Polls.png` — Taipei retrospective check against poll history and actual results
- `results/NewTaipei_Retrospective_vs_Actual_Polls.png` — New Taipei retrospective check against poll history and actual results

Finally, check the publication timestamp:

- `results/published_at_utc.txt` — the UTC timestamp for the latest forecast release

## How to read the outputs

1. Read the text summary first. It gives the most concise interpretation of the latest forecast.
2. Open the forecast dashboards for the city-level visuals and the model estimates.
3. Review the retrospective plots to understand the model's historical fit and stability.
4. Use the timestamp file to understand when the output was generated relative to the election timeline.

## Why this repo exists

This repository serves as a transparent, shareable archive of model outputs. It is designed for readers who want to:

- see the latest forecast without digging through code
- inspect how the model behaves over time
- understand the difference between a current estimate and a historical validation snapshot
- share the results in a clean, readable format

## Caveat

These are forecasting outputs for public interest and exploratory analysis. They are not official election results, and they should be read as a snapshot of a probabilistic model at a specific time.

## Repository structure

```text
.
├── .gitkeep
└── results/
    ├── Taipei_forecast_dashboard.png
    ├── NewTaipei_forecast_dashboard.png
    ├── Taipei_Retrospective_vs_Actual_Polls.png
    ├── NewTaipei_Retrospective_vs_Actual_Polls.png
    ├── Taipei_NewTaipei_fb_post.txt
    └── published_at_utc.txt
```

If you are visiting this repo for the first time, the best path is: open the text summary, inspect the dashboards, and then review the retrospective validation charts to get a feel for how the forecasting system behaves over time.
