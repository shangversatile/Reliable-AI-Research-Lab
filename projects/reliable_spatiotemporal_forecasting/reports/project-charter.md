# Project Charter

## Project Motivation

The project studies whether spatiotemporal forecasting models remain reliable when environmental data experience noise, anomalies, missingness, and temporal distribution shift.

## Research Reboot Positioning

The project inherits a problem family, not a codebase.

Prior thesis observations are hypotheses, not evidence.

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

RQ5 belongs to the Week 7 extension.

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

H4 belongs to the Week 7 extension.

## Dataset

KnowAir PM2.5 only for the MVP.

## Chronological Split

* Train: 60%
* Validation: 10%
* Calibration: 10%
* Test: 20%
* preserve temporal order
* do not use random splitting
* normalization statistics must be fitted on training data only

## Models

Persistence, Historical Average, Vanilla STGCN, DCRNN, and Robust-STGCN only after the baseline pipeline is reliable.

## Shift Definitions

Gaussian noise, spike anomalies, missingness, and temporal shift.

## UQ Methods

MC Dropout, Deep Ensemble, and Split Conformal Prediction.

## Evaluation Metrics

MAE, RMSE, MAPE, coverage, coverage gap, interval width, sharpness, CRPS, WIS or Winkler Score, quantile calibration error, coverage rate, selective risk, risk–coverage curve, AURC, review rate, average decision cost, under-allocation cost, over-allocation cost, tail risk, CVaR, constraint violation rate, and runtime.

## Decision Task

Compare Mean Policy, Risk-Averse Policy, Upper-Quantile Policy, and simplified abstention or human-review policy under clean and shifted conditions.

## MVP Scope

Reproducible baselines, UQ and calibration, shift stress testing, and decision reliability for KnowAir PM2.5.

## Stretch Goals

Quantile regression, copula conformal prediction, change-point adaptation, station holdout, extreme-event subset, prediction-reconstruction multi-task learning, representation-stability diagnostics, and traffic-dataset external validation.

## Stop Conditions

Stop or rescope if split logic cannot be verified, metrics cannot be reproduced, corruption protocols are ambiguous, or baseline results cannot be traced to fixed seeds and configuration records.

## Deliverables

* prior-prototype reassessment table
* model relearning record
* innovation and critique map
* reproducible baseline protocol
* baseline metrics table
* UQ and calibration report
* shift stress-test report
* decision-reliability report
* failure analysis
* six core figures
* one-page project summary
* research-style short report
* advisor-specific summaries
* advisor-alignment evidence packet
* Week 7 representation-stability extension only if justified by MVP evidence
