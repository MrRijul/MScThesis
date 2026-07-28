# The Silent Asset

## Franchise Deposits and Cross-Sectional Bank Equity Returns in the Euro Area

This repository contains the empirical analysis for my 2026 MSc dissertation, supervised by Prof. Carla Soares.

## Repository structure

```text
.
├── README.md
├── requirements.txt
├── notebooks/
│   └── 01_empirical_analysis.ipynb # Code and Logic
├── data/
│   └── README.md
├── docs/
│   └── Main Defense Slides.pdf # Contains easy to read slide deck to get quick overview.
```

## Research question

Are banks with stronger franchise-deposit exposure priced differently when the euro-area yield curve steepens rather than flattens, and does this relationship depend on deposit composition, the macro-financial regime and asset-side repricing capacity?

## Sample

- 36 listed euro-area banks
- April 2011 to December 2024
- 165 monthly periods
- 5,318 bank-month observations in the main sample
- 3,386 observations in the deposit-composition subsample

## Main findings

1. High-customer-deposit banks earn a relative equity premium during yield-curve steepening, although the broad result weakens under the fullest macro-financial controls.
2. Deposit composition matters: savings-deposit heavy banks are penalised during steepening.
3. The relationship is regime-dependent and becomes more visible after the 2022 rate normalisation.
4. The strongest premium is concentrated among banks combining high deposit exposure with high loan exposure.

## Methods

- Python panel-data pipeline
- Bank and month fixed effects
- Bank-clustered covariance estimation
- 999-draw wild-cluster bootstrap inference
- Wald coefficient tests
- 60-month rolling regressions
- High-/low-stress regime analysis
- Alternative yield-curve definitions
- Winsorisation and continuous specifications
- Leave-one-bank-out and leave-one-country-out stability checks

## Data availability

The underlying bank-level data are derived from licensed Refinitiv Datastream/Worldscope and BvD OSIRIS sources and therefore cannot be redistributed publicly.

The notebook is published with selected outputs for transparency. Authorised users can reproduce the analysis by placing `final_panel.csv` inside `data/processed/`.

## Local setup

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/01_empirical_analysis.ipynb` and run the notebook after placing the authorised dataset in `data/processed/`.

## Author

Rijul Sharma
