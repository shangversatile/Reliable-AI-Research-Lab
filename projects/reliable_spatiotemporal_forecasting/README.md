# Reliable Spatiotemporal Forecasting

## Project Title

Reliable Spatiotemporal Forecasting under Dynamic Distribution Shift:
Calibration, Uncertainty Quantification and Risk-Aware Decision-Making

## Objective

Build a reproducible prototype for spatiotemporal forecasting reliability
under dynamic distribution shift, combining baseline forecasting,
uncertainty quantification, conformal calibration, shift stress testing,
and risk-aware decision evaluation.

## Current Phase

Research-protocol initialization.

No prior prototype code has been migrated.

No experimental results are claimed.

## Core Modules

1. Forecasting baseline: DCRNN or STGCN with traffic / PM2.5-style data and MAE / RMSE tables.
2. Uncertainty quantification: MC Dropout, Deep Ensemble or Quantile Regression, coverage, interval width, and CRPS where feasible.
3. Conformal calibration: split conformal wrapper, multi-step coverage, coverage degradation under shift, and change-point experiment.
4. Dynamic distribution shift: synthetic change point, temporal shift, missingness, noise, and spike corruption.
5. Risk-aware decision evaluation: Top-K allocation regret, selective risk, abstention or review-rate option, and decision-cost comparison.
6. Technical reporting: paper notes, experiment tables, reliability figures, a 6-8 page technical report, and a 1-page public project summary.

## Documentation

* `reports/project-charter.md`
* `reports/prior-prototype-reassessment.md`
* `reports/model-relearning-plan.md`
* `reports/innovation-and-critique-map.md`
* `reports/experiment-protocol.md`
* `reports/8-week-execution-plan.md`
* `reports/planned-code-structure.md`
* `templates/experiment-record-template.md`
