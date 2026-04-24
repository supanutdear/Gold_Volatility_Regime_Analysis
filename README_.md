# Gold Volatility and the Breakdown of the Real Yield Relationship Under Trump Regime II

A quantitative technical white paper analyzing structural volatility regime change in gold markets using GARCH-VaR framework, Kupiec POF test, and Christoffersen Independence test.

## Overview

This analysis examines whether gold volatility has structurally changed since Trump Regime II began in January 2025, and whether the traditional inverse relationship between gold and real yields remains reliable as a risk management heuristic.

Built by a gold trader managing daily XAU/USD hedging exposure as a systematic quantitative analysis of an observed market shift.

## Research Questions

1. Has the volatility of gold structurally changed since Trump Regime II began in January 2025?
2. Is the long-held belief that gold moves inversely to real yields still reliable in the current regime?

## Key Findings

- **Alpha increased 502%** — the market now prices new information into volatility more than six times more aggressively
- **Half-life of shocks dropped from 12 days to 2.4 days** — markets absorb and reset within days, not weeks
- **Out-of-sample breach rate: 5.88% vs 5.00% target** — pre-2025 models underestimate current risk
- **Real yield correlation weakened from −0.48 to −0.14** — inverse relationship now active on only 61% of trading days versus 82% historically
- **Peak volatility exceeded the COVID-19 spike by nearly 2.8×**

## Methodology

| Component | Detail |
|-----------|--------|
| Calibration Period | 20 Jan 2017 – 19 Jan 2025 (2,085 trading days) |
| Evaluation Period | 20 Jan 2025 – 16 Apr 2026 (323 trading days) |
| Volatility Model | GARCH(1,1) via Maximum Likelihood Estimation |
| Risk Metrics | VaR 95% and CVaR (Expected Shortfall) |
| Validation | Kupiec POF test + Christoffersen Independence test |
| Data Sources | Gold Futures (GC=F) from Yahoo Finance; 10-Year Real Yield (DFII10) from FRED |

## Files

| File | Description |
|------|-------------|
| `Gold_Volatility_Regime_Analysis.ipynb` | Full analysis notebook with code, outputs, and visualizations |
| `Gold_Volatility_Regime_Analysis.pdf` | Technical white paper with narrative analysis and findings |

## Run in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/supanutdear/Gold-Volatility-GARCH-VaR/blob/main/Gold_Volatility_Regime_Analysis.ipynb)

## Reproducibility

The notebook uses a locked end date (`TODAY = '2026-04-17'`) to ensure any reader can run it and obtain identical results. All data is fetched live from Yahoo Finance and FRED.

### Requirements

```
pandas
numpy
yfinance
pandas_datareader
matplotlib
seaborn
scipy
statsmodels
arch
```

### How to Run

Open the notebook in Jupyter or Google Colab and run cells sequentially. All sections must execute in order since later sections depend on variables from earlier ones.

## Scope and Limitations

- **Regime boundaries** are defined by U.S. presidential inauguration dates as the primary hypothesis driver, not by formal statistical structural break tests (Chow, Bai-Perron) — reserved for future work
- **Sample size** for Trump Regime II is limited (323 days), so parameter estimates carry higher uncertainty than the in-sample period
- **Framework** is practitioner-oriented, prioritizing actionable risk management insights over exhaustive academic formalism

## About the Author

Built by a gold trader managing approximately 20M USD/day in XAU/USD and USD/THB hedging exposure. Code implementation was AI-assisted; all analytical design decisions, methodology choices, and interpretations are the author's own.

## License

MIT License — free to use and adapt for your own analysis.
