# Experiment Protocol

## Pre-Implementation Stage: Relearning and Independent Protocol Design

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Relearn model stack and design the protocol before reading prior implementation details | Prevent accidental inheritance of unverified assumptions | Primary-source notes, conceptual explanations, protocol decisions, critique map | Model relearning plan and independent project charter | Planned |

## Eight-Week Public Execution Protocol

This protocol aligns with `8-week-execution-plan.md` and records planned
public deliverables. No experimental result is claimed until a traceable
artifact exists.

### Week 1-2 - Baseline and Core Literature

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Read Quantifying UQ | Establish the UQ comparison target for spatiotemporal forecasting | 1-page note with assumptions, metrics, and reproduction scope | Paper note | Planned |
| Read CopulaCPTS | Establish the multi-step conformal calibration target | 1-page note with coverage, interval width, and horizon-specific evaluation ideas | Paper note | Planned |
| Establish project skeleton | Make the future implementation reproducible before experiments | README, environment plan, dataset loader plan | Project skeleton plan | Planned |
| Run STGCN/DCRNN baseline | Baseline error is required before UQ or shift claims | Split logic, seeds, metric definitions, MAE / RMSE outputs | Baseline table | Planned |

### Week 3-4 - UQ and Calibration Metrics

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Add MC Dropout | Evaluate approximate uncertainty under shared baseline conditions | Sampling protocol, interval outputs, coverage and width metrics | UQ comparison record | Planned |
| Add Deep Ensemble or Quantile Regression | Compare uncertainty families under the same task | Ensemble or quantile protocol, runtime notes, interval outputs | UQ comparison table | Planned |
| Implement calibration metrics | Reliability requires more than point error | ECE, reliability diagram, CRPS where feasible | Calibration report | Planned |
| Read robust conformal literature | Connect empirical calibration to robust reliability questions | Robust conformal note with perturbation and coverage questions | Robust conformal note | Planned |

### Week 5-6 - Dynamic Shift and Conformal Wrapper

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Implement conformal wrapper | Evaluate empirical coverage under a shared calibration split | Calibration split, nonconformity scores, empirical coverage | Conformal wrapper report | Planned |
| Add temporal shift / missingness / noise | Reliability must be tested under non-clean conditions | Shift definitions, severity levels, seeds, shifted outputs | Shift stress test | Planned |
| Study change-point conformal forecasting | Abrupt non-stationarity may require adaptation beyond static calibration | Change-point experiment design and adaptation criteria | Change-point design note | Planned |
| Run first dynamic-shift experiment | Measure whether coverage degrades before and after shift | Coverage degradation figure and limitations | Dynamic-shift result record | Planned |

### Week 7-8 - Decision Risk and Technical Report

| Task | Rationale | Evidence Required | Artifact | Status |
| ---- | --------- | ----------------- | -------- | ------ |
| Add risk-aware decision metric | Predictive reliability should connect to downstream decisions | Top-K allocation regret, selective risk, decision-cost definitions | Decision-risk module report | Planned |
| Study meta-evaluation and recourse verification | Evaluation metrics and actions should be stress-tested | Meta-evaluation note and decision-risk note | Evaluation and decision notes | Planned |
| Write technical report | Consolidate methods, experiments, limitations, and next steps | Traceable tables, figures, notes, and limitation log | 6-8 page report | Planned |
| Prepare public project summary | Summarize the objective project without private planning content | One-page objective summary | Public project summary | Planned |

## Evidence Rules

* Do not claim reproduction completion before code, logs, and figures exist.
* Do not report results without split, seed, metric, and dataset records.
* Do not expand later extensions before the baseline, UQ, calibration, shift,
  and decision-risk modules are traceable.
