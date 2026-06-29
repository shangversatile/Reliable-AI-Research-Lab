# Research Scope

## Core Objective

Build a reproducible research protocol for reliable spatiotemporal
forecasting under dynamic distribution shift, with calibration,
uncertainty quantification, conformal reliability, shift stress testing,
and risk-aware decision-making as the main evaluation axes.

## Why This Project Matters

Forecasting systems used in environmental contexts can fail under shift
even when clean-split predictive error looks acceptable. The project tests
whether reliability, uncertainty, and decision quality remain stable when
data are corrupted, temporally shifted, or affected by changing regimes.

## Project Core Modules

### Forecasting Baseline

* DCRNN or STGCN
* traffic / PM2.5-style dataset
* MAE / RMSE baseline table

### Uncertainty Quantification

* MC Dropout
* Deep Ensemble or Quantile Regression
* interval width
* coverage
* CRPS where feasible

### Conformal Calibration

* split conformal / conformal wrapper
* multi-step coverage
* coverage degradation under shift
* change-point experiment

### Dynamic Distribution Shift

* synthetic change point
* temporal shift
* missingness
* noise / spike corruption

### Risk-Aware Decision Evaluation

* Top-K allocation regret
* selective risk
* abstention or review-rate option
* decision-cost comparison

### Technical Reporting

* paper notes
* experiment tables
* reliability figures
* 6-8 page technical report
* 1-page public project summary

## Research Reboot Principle

Do not treat the prior prototype as a finished research artifact.

Do not inherit old assumptions by default.

Do not migrate code before conceptual relearning.

Do not use old results as new-project evidence.

Redesign split, normalization, metrics, corruption protocol,
UQ evaluation, and decision task independently.

Compare with the prior prototype only after the new baseline protocol exists.

## Research Questions

* How do spatiotemporal forecasting models fail under noise, spike anomalies, missingness, and temporal distribution shift?
* Do MC Dropout, Deep Ensembles, Quantile Regression, and Split Conformal Prediction retain their reliability ranking under distribution shift?
* Does the model with the lowest predictive error also minimize downstream allocation cost?
* Can uncertainty estimates support selective prediction, conservative allocation, human review, and alert escalation?
* Does prediction-reconstruction multi-task learning improve latent representation stability under shift, and is representation stability associated with calibration or decision stability?

## MVP Boundaries

Dataset:

* A PM2.5 forecasting dataset selected through the dataset-selection gate
* Original KnowAir and KnowAir-V2 remain candidates until evidence review is complete
* No MVP dataset is locked before schema, missingness, reproducibility, licensing, and implementation-cost review

Baselines:

* Persistence
* Historical Average
* Vanilla STGCN
* DCRNN
* Robust-STGCN only after the baseline pipeline is reliable

UQ:

* MC Dropout
* Deep Ensemble
* Quantile Regression as a comparison target where feasible
* Split Conformal Prediction

Shift:

* synthetic change point
* Gaussian noise
* spike anomalies
* missingness
* temporal shift

Decision layer:

* Mean Policy
* Risk-Averse Policy
* Upper-Quantile Policy
* simplified abstention and human-review policy
* Top-K allocation regret

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
* risk-coverage curve
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

* copula conformal prediction
* change-point adaptation
* station holdout
* extreme-event subset
* prediction-reconstruction multi-task learning
* representation-stability diagnostics
* traffic-dataset external validation
* latent causal mechanism shift
* climate generative forecasting
* forecast-to-control
* AI systems / inference reliability as a separate side line
* LLM / RAG / agent reliability as a separate line

## Public Literature Roadmap

Reproduction priority:

* Quantifying Uncertainty in Deep Spatiotemporal Forecasting
* DCRNN or STGCN baseline
* Copula Conformal Prediction for Multi-Step Time-Series Forecasting
* Conformal Prediction for Time Series with Change Points / CPTC

Deep reading priority:

* Provably Robust Conformal Prediction with Improved Efficiency
* Evaluating Neuron Explanations
* Prediction without Preclusion
* U-Cast

Later extensions:

* SPACY
* Koopman Neural Forecaster
* Spherical DYffusion
* Zephyrus
* forecast-to-control literature
* causal data audit literature
* LLM / RAG / agent reliability literature as a separate line
* AI systems literature as a separate line

## Non-Goals

* no direct prototype-code dump
* no benchmark-only project
* no diffusion forecasting in the MVP
* no foundation-model forecasting in the MVP
* no complex transformer expansion in the MVP
* no world model
* no agent project in the MVP
* no full causal representation-learning implementation in the MVP

## Expected Outputs

* reproducible baseline protocol
* documented shift stress tests
* UQ and calibration evaluation
* conformal wrapper evaluation
* decision-reliability analysis
* paper notes
* experiment tables
* reliability figures
* 6-8 page technical report
* 1-page public project summary
* Week 7 representation-stability extension only if the MVP creates a concrete diagnostic question
