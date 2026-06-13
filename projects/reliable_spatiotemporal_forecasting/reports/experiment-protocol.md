# Experiment Protocol

## Pre-Implementation Stage: Relearning and Independent Protocol Design

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Relearn model stack and design the protocol before reading prior implementation details | Prevent accidental inheritance of unverified assumptions | Primary-source notes, conceptual explanations, protocol decisions, critique map | Model relearning plan and independent project charter | Planned |

## Week 1: Reproducible Baselines

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Establish clean baselines on the PM2.5 dataset selected through the dataset-selection gate | Baselines are required before UQ or shift claims | Split logic, seeds, metric definitions, baseline outputs | Baseline report | Planned |

## Week 2: UQ and Calibration

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Add MC Dropout, Deep Ensemble, and Split Conformal Prediction | UQ methods need shared evaluation before shift testing | Calibration protocol, interval outputs, coverage metrics | UQ report | Planned |

## Week 3: Shift Stress Testing

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Apply Gaussian noise, spike anomalies, missingness, and temporal shift | Reliability must be evaluated under dynamic distribution shift | Shift definitions, seeds, shifted outputs, failure cases | Shift stress-test report | Planned |

## Week 4: Decision Reliability

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Compare mean, risk-averse, upper-quantile, and review policies | Predictive accuracy may not match downstream decision quality | Cost definitions, decision logs, tail-risk metrics | Decision reliability report | Planned |

## Week 5: Multi-Step Dependency Extension

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Test whether multi-step dependencies alter reliability conclusions | Forecast horizon may change calibration and decision behavior | Horizon-specific metrics and comparison tables | Multi-step extension note | Planned |

## Week 6: Change-Point Adaptation

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Evaluate whether change-point adaptation helps under temporal shift | Temporal regimes may require adaptation beyond static calibration | Change-point rule, adaptation logs, before-after metrics | Change-point extension note | Planned |

## Week 7: Representation Stability

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Compare prediction-only and prediction-reconstruction latent behavior | Representation diagnostics should explain concrete MVP failures | Latent outputs, diagnostic question, calibration and decision links | Representation stability note | Planned |

## Week 8: External Validation and Research Communication

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Prepare external validation plan and research communication materials | External communication needs reproducible evidence rather than broad claims | Project summary, evidence tables, limitation log | Research communication packet | Planned |
