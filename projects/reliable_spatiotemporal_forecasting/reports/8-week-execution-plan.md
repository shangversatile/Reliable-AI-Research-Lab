# Eight-Week Execution Plan

## Project Core

Project title:

Reliable Spatiotemporal Forecasting under Dynamic Distribution Shift

Objective:

Build a reproducible prototype for spatiotemporal forecasting reliability
under dynamic distribution shift, combining baseline forecasting,
uncertainty quantification, conformal calibration, shift stress testing,
and risk-aware decision evaluation.

## Core Modules

### 1. Forecasting Baseline

* DCRNN or STGCN
* traffic / PM2.5-style dataset
* MAE / RMSE baseline table

### 2. Uncertainty Quantification

* MC Dropout
* Deep Ensemble or Quantile Regression
* interval width
* coverage
* CRPS where feasible

### 3. Conformal Calibration

* split conformal / conformal wrapper
* multi-step coverage
* coverage degradation under shift
* change-point experiment

### 4. Dynamic Distribution Shift

* synthetic change point
* temporal shift
* missingness
* noise / spike corruption

### 5. Risk-Aware Decision Evaluation

* Top-K allocation regret
* selective risk
* abstention or review-rate option
* decision-cost comparison

### 6. Technical Reporting

* paper notes
* experiment tables
* reliability figures
* 6-8 page technical report
* 1-page public project summary

## Eight-Week Execution Plan

### Week 1-2 - Baseline and Core Literature

| Task | Deliverable |
| ---- | ----------- |
| Read Quantifying UQ | 1-page paper note |
| Read CopulaCPTS | 1-page paper note |
| Establish project skeleton | README + environment plan + dataset loader plan |
| Run STGCN/DCRNN baseline | MAE / RMSE table |

### Week 3-4 - UQ and Calibration Metrics

| Task | Deliverable |
| ---- | ----------- |
| Add MC Dropout | coverage / interval width |
| Add Deep Ensemble or Quantile Regression | UQ comparison |
| Implement calibration metrics | ECE / reliability diagram / CRPS |
| Read robust conformal literature | robust conformal note |

### Week 5-6 - Dynamic Shift and Conformal Wrapper

| Task | Deliverable |
| ---- | ----------- |
| Implement conformal wrapper | empirical coverage |
| Add temporal shift / missingness / noise | shift stress test |
| Study change-point conformal forecasting | change-point experiment design |
| Run first dynamic-shift experiment | coverage degradation figure |

### Week 7-8 - Decision Risk and Technical Report

| Task | Deliverable |
| ---- | ----------- |
| Add risk-aware decision metric | Top-K allocation regret / selective risk |
| Study meta-evaluation and recourse verification | evaluation and decision-risk notes |
| Write technical report | 6-8 page report |
| Prepare public project summary | 1-page objective summary |

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

## Public Tone Requirements

Use objective academic language and objective terms:

* related literature
* research alignment
* technical milestone
* experiment module
* benchmark component
* public deliverable
* later extension

Keep non-technical planning details outside public project documents.
