# Research Scope

## Core Objective

Build a reproducible research protocol for reliable spatiotemporal forecasting under dynamic distribution shift, with calibration, uncertainty quantification, and risk-aware decision-making as the main evaluation axes.

## Why This Project Matters

Forecasting systems used in environmental contexts can fail under shift even when clean-split predictive error looks acceptable. The project tests whether reliability, uncertainty, and decision quality remain stable when data are corrupted or temporally shifted.

## Research Reboot Principle

Do not treat the old thesis as a finished research artifact.

Do not inherit old assumptions by default.

Do not migrate code before conceptual relearning.

Do not use old results as new-project evidence.

Redesign split, normalization, metrics, corruption protocol,
UQ evaluation, and decision task independently.

Compare with the prior prototype only after the new baseline protocol exists.

## Research Questions

* How do spatiotemporal forecasting models fail under noise, spike anomalies, missingness, and temporal distribution shift?
* Do MC Dropout, Deep Ensembles, and Split Conformal Prediction retain their reliability ranking under distribution shift?
* Does the model with the lowest predictive error also minimize downstream allocation cost?
* Can uncertainty estimates support selective prediction, conservative allocation, human review, and alert escalation?
* Does prediction-reconstruction multi-task learning improve latent representation stability under shift, and is representation stability associated with calibration or decision stability?

## MVP Boundaries

Dataset:

* KnowAir PM2.5 only

Baselines:

* Persistence
* Historical Average
* Vanilla STGCN
* DCRNN
* Robust-STGCN only after the baseline pipeline is reliable

UQ:

* MC Dropout
* Deep Ensemble
* Split Conformal Prediction

Shift:

* Gaussian noise
* spike anomalies
* missingness
* temporal shift

Decision layer:

* Mean Policy
* Risk-Averse Policy
* Upper-Quantile Policy
* simplified abstention and human-review policy

Metrics:

* MAE
* RMSE
* MAPE
* coverage
* coverage gap
* interval width
* sharpness
* CRPS
* WIS or Winkler Score
* quantile calibration error
* coverage rate
* selective risk
* risk–coverage curve
* AURC
* review rate
* average decision cost
* under-allocation cost
* over-allocation cost
* tail risk
* CVaR
* constraint violation rate
* runtime

## Extension Boundaries

* quantile regression
* Copula conformal prediction
* change-point adaptation
* station holdout
* extreme-event subset
* prediction-reconstruction multi-task learning
* representation-stability diagnostics
* traffic-dataset external validation

## Non-Goals

* no direct thesis-code dump
* no benchmark-only project
* no diffusion forecasting
* no foundation-model forecasting
* no complex transformer expansion
* no world model
* no agent project
* no full causal representation-learning implementation

## Expected Outputs

* reproducible baseline protocol
* documented shift stress tests
* UQ and calibration evaluation
* decision-reliability analysis
* advisor-ready evidence packet
* Week 7 representation-stability extension only if the MVP creates a concrete diagnostic question
