# Dataset Selection Review

## Purpose

Choose the MVP dataset only after comparing the prior prototype dataset
with currently available alternatives.

## Research Reboot Rule

Do not use the original KnowAir dataset only because it appeared
in the prior prototype.

## Candidates

| Dataset | Role | Questions to Verify | Decision Status |
| ------- | ---- | ------------------- | --------------- |
| Original KnowAir | Historical comparison candidate | schema, time span, stations, variables, missingness, preprocessing, licensing, reproducibility | Pending review |
| KnowAir-V2 | Preferred new-project candidate for review | schema, time span, stations, variables, missingness, preprocessing, licensing, compatibility with MVP scope | Pending review |
| Traffic dataset | Week 8 external validation | domain transfer value, comparability, implementation cost | Deferred |
| AirQualityBench | Post-MVP frontier watchlist | structured missingness, deployment realism, scale, compatibility with project goals | Deferred |

## Decision Questions

* Does KnowAir-V2 materially improve data quality without making the MVP too large?
* Can the project preserve a clean chronological train, validation, calibration, and test split?
* Are missingness and imputation rules documented?
* Are graph-construction assumptions scientifically meaningful?
* Can the selected dataset support PM2.5 reliability analysis rather than benchmark-only modeling?
* Should the original KnowAir remain only as a historical comparison?
* Is AirQualityBench better treated as a later external stress-test benchmark?

## Required Evidence Before Decision

* verified dataset documentation
* schema comparison
* temporal coverage comparison
* station and feature comparison
* missingness and imputation notes
* licensing and access notes
* implementation cost estimate
* MVP-scope decision

## Current Status

Pending evidence review. No dataset is locked yet.
