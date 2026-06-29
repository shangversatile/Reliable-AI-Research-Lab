# Reliable-AI-Research-Lab

## Purpose

A research repository for reliable and trustworthy AI systems.

The repository focuses on building reproducible evaluation protocols,
identifying failure modes, and studying how uncertainty estimates
should influence downstream decisions.

## Active Flagship Project

Reliable Spatiotemporal Forecasting under Dynamic Distribution Shift:
Calibration, Uncertainty Quantification, and Risk-Aware Decision-Making

## Project Core

Objective:

Build a reproducible prototype for spatiotemporal forecasting reliability
under dynamic distribution shift, combining baseline forecasting,
uncertainty quantification, conformal calibration, shift stress testing,
and risk-aware decision evaluation.

Core public modules:

* forecasting baseline with DCRNN or STGCN
* uncertainty quantification with MC Dropout and ensemble or quantile methods
* conformal calibration for multi-step and shifted settings
* dynamic distribution shift stress tests
* risk-aware decision evaluation
* technical reporting through notes, tables, figures, and a short report

The active 8-week execution roadmap is maintained in
`projects/reliable_spatiotemporal_forecasting/reports/8-week-execution-plan.md`.

## Research Approach

The flagship project follows a research-reboot approach.

Earlier prototypes are treated as historical reference points
rather than implementation foundations.

The project relearns the model stack,
critically reassesses assumptions,
designs an independent evaluation protocol,
and reimplements trustworthy baselines before considering
selective adaptation of prior ideas.

## Current Status

* literature curriculum initialized
* research questions and falsifiable hypotheses defined
* dataset-selection review in progress
* model relearning stage in progress
* 8-week public roadmap defined
* no claimed experimental results yet

## Relationship to Other Repositories

* `Paper-Reading-Notes` supplies verified literature maps,
  critical reading records, and research questions.
* `ML-DL-NLP-Lab` is a separately maintained foundations repository.
* `Representation-Analysis-Lab` will activate only after the flagship MVP
  exposes a concrete representation-level diagnostic question.
