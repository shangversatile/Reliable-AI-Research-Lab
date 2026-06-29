# Project Charter

## Project Motivation

The project studies whether spatiotemporal forecasting models remain reliable
when environmental data experience noise, anomalies, missingness, temporal
shift, and changing regimes.

## Project Objective

Build a reproducible prototype for spatiotemporal forecasting reliability
under dynamic distribution shift, combining baseline forecasting,
uncertainty quantification, conformal calibration, shift stress testing,
and risk-aware decision evaluation.

## Research Reboot Positioning

The project inherits a problem family, not a codebase.

Prior prototype observations are hypotheses, not evidence.

Baselines will be relearned and independently implemented.

Innovation should emerge from falsification, failure analysis,
and explicit research gaps.

## Core Research Questions

RQ1:
How do models fail under controlled corruption and temporal shift?

RQ2:
Do uncertainty methods retain their reliability ranking under shift?

RQ3:
Does the model with the lowest predictive error also minimize downstream allocation cost?

RQ4:
Can uncertainty estimates support selective prediction, conservative allocation, human review, and alert escalation?

RQ5:
Does prediction-reconstruction multi-task learning improve latent representation stability under shift?

RQ1-RQ4 belong to the MVP.

RQ5 belongs to a gated extension.

## Falsifiable Hypotheses

H1:
Point-prediction ranking and reliability ranking may diverge under shift.

H2:
UQ methods that work under near-IID conditions may degrade under shift.

H3:
Uncertainty-aware allocation may reduce tail risk while increasing average resource cost.

H4:
Prediction-reconstruction learning may improve representation stability without necessarily improving calibration.

H1-H3 belong to the MVP.

H4 belongs to a gated extension.

## Core Modules

### Forecasting Baseline

DCRNN or STGCN on traffic / PM2.5-style data with MAE / RMSE baseline tables.

### Uncertainty Quantification

MC Dropout, Deep Ensemble or Quantile Regression, interval width, coverage,
and CRPS where feasible.

### Conformal Calibration

Split conformal / conformal wrapper, multi-step coverage, coverage degradation
under shift, and change-point experiment.

### Dynamic Distribution Shift

Synthetic change point, temporal shift, missingness, noise, and spike corruption.

### Risk-Aware Decision Evaluation

Top-K allocation regret, selective risk, abstention or review-rate option,
and decision-cost comparison.

### Technical Reporting

Paper notes, experiment tables, reliability figures, a 6-8 page technical
report, and a 1-page public project summary.

## Dataset

The MVP will use a PM2.5 forecasting dataset selected through
the dataset-selection gate.

Original KnowAir and KnowAir-V2 remain candidates until
schema, missingness, reproducibility, licensing,
and implementation-cost evidence are reviewed.

No MVP dataset is locked yet.

## Chronological Split

* Train: 60%
* Validation: 10%
* Calibration: 10%
* Test: 20%
* preserve temporal order
* do not use random splitting
* normalization statistics must be fitted on training data only

## Models

Persistence, Historical Average, Vanilla STGCN, DCRNN, and Robust-STGCN only
after the baseline pipeline is reliable.

## Shift Definitions

Synthetic change point, Gaussian noise, spike anomalies, missingness, and temporal shift.

## UQ and Calibration Methods

MC Dropout, Deep Ensemble, Quantile Regression where feasible, Split Conformal
Prediction, multi-step conformal calibration, and change-point-aware conformal
forecasting.

## Evaluation Metrics

MAE, RMSE, MAPE, coverage, coverage gap, interval width, sharpness, CRPS,
WIS or Winkler Score, quantile calibration error, coverage rate, selective risk,
risk-coverage curve, AURC, review rate, average decision cost,
under-allocation cost, over-allocation cost, tail risk, CVaR,
constraint violation rate, Top-K allocation regret, and runtime.

## Decision Task

Compare Mean Policy, Risk-Averse Policy, Upper-Quantile Policy, Top-K allocation,
and simplified abstention or human-review policy under clean and shifted conditions.

## Public Literature Roadmap

### Reproduction Priority

* Quantifying Uncertainty in Deep Spatiotemporal Forecasting
* DCRNN or STGCN baseline
* Copula Conformal Prediction for Multi-Step Time-Series Forecasting
* Conformal Prediction for Time Series with Change Points / CPTC

### Deep Reading Priority

* Provably Robust Conformal Prediction with Improved Efficiency
* Evaluating Neuron Explanations
* Prediction without Preclusion
* U-Cast

### Later Extensions

* SPACY
* Koopman Neural Forecaster
* Spherical DYffusion
* Zephyrus
* forecast-to-control literature
* causal data audit literature
* LLM / RAG / agent reliability literature as separate line
* AI systems literature as separate line

## MVP Scope

Reproducible baselines, UQ and calibration, shift stress testing,
and decision reliability for the PM2.5 dataset selected through
the dataset-selection gate.

## Stretch Goals

Copula conformal prediction, change-point adaptation, station holdout,
extreme-event subset, prediction-reconstruction multi-task learning,
representation-stability diagnostics, traffic-dataset external validation,
latent causal mechanism shift, climate forecasting extension, and
forecast-to-control extension.

## Stop Conditions

Stop or rescope if split logic cannot be verified, metrics cannot be reproduced,
corruption protocols are ambiguous, or baseline results cannot be traced to fixed
seeds and configuration records.

## Deliverables

* prior-prototype reassessment table
* model relearning record
* innovation and critique map
* reproducible baseline protocol
* baseline metrics table
* UQ and calibration report
* conformal wrapper report
* shift stress-test report
* decision-reliability report
* failure analysis
* reliability figures
* paper notes
* experiment tables
* 6-8 page technical report
* 1-page public project summary
* gated representation-stability extension only if justified by MVP evidence
