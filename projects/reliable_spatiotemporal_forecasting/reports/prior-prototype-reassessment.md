# Prior Prototype Reassessment

## Principle

The earlier prototype is a prior prototype,
not the implementation foundation of the new research project.

Preserve promising questions and historical observations,
not accidental script structure or unverified assumptions.

## Allowed Uses of the Prior Prototype

* historical context
* source of candidate research questions
* comparison point after independent reimplementation
* source of audit warnings
* selective adaptation only after tests

## Prohibited Uses

* direct code dump
* default inheritance of split logic
* default inheritance of normalization logic
* default inheritance of metrics
* default inheritance of corruption severity
* treating old results as current evidence
* assuming prediction-reconstruction or Robust-STGCN is already justified

## Reassessment Modes

* Reference only
* Relearn from primary source
* Reimplement from first principles
* Compare with prior prototype
* Selective adaptation after tests
* Retire

| Prior Asset or Idea | Historical Role | What Must Be Relearned | Critical Questions | Default Reassessment Mode | Allowed Use After Audit | Status |
| ------------------- | --------------- | ---------------------- | ------------------ | ------------------------- | ----------------------- | ------ |
| KnowAir loader | Prior data access prototype | Dataset schema, temporal ordering, missingness handling, and leakage risks | Does the loader preserve the intended chronological protocol and avoid hidden preprocessing assumptions? | Relearn from primary source | Reference for audit warnings only until independently reimplemented | Planned |
| chronological split | Prior split idea | Temporal validation design, calibration split, test split, and leakage controls | Does the split support UQ calibration and decision evaluation without random leakage? | Reimplement from first principles | Compare with prior prototype after new protocol exists | Planned |
| normalization | Prior preprocessing idea | Training-only statistics, station-level behavior, and shift interaction | Were statistics fitted only on training data, and do they remain valid under shift testing? | Reimplement from first principles | Compare with prior prototype after leakage checks | Planned |
| graph builder | Prior graph construction prototype | Spatial graph assumptions, distance or correlation choices, and sensitivity | Is the graph scientifically meaningful and reproducible across stations? | Relearn from primary source | Selective adaptation after tests | Planned |
| STGCN | Prior baseline family | Model architecture, assumptions, receptive field, and training protocol | What does STGCN contribute beyond simpler baselines under the new protocol? | Relearn from primary source | Reimplement independently before comparison | Planned |
| DCRNN | Prior baseline family | Diffusion assumptions, recurrent dynamics, and multi-step behavior | When is DCRNN a fair baseline for environmental forecasting? | Relearn from primary source | Reimplement independently before comparison | Planned |
| Robust-STGCN | Prior robustness idea | Operational definition of robustness and relationship to reliability metrics | Does robustness mean more than lower average error under synthetic corruption? | Relearn from primary source | Selective adaptation only after falsification tests | Planned |
| corruption protocol | Prior stress-test idea | Corruption types, severity, seeds, and operational realism | Are corruptions realistic, reproducible, and aligned with reliability questions? | Reimplement from first principles | Compare with prior prototype after new stress tests exist | Planned |
| MC Dropout | Prior UQ candidate | Bayesian approximation assumptions and calibration behavior | Does uncertainty remain informative under shift or become overconfident? | Relearn from primary source | Reimplement independently before comparison | Planned |
| prediction-reconstruction objective | Prior multi-task idea | Representation hypothesis, loss interaction, and diagnostic target | Does reconstruction improve useful representations or only act as generic regularization? | Relearn from primary source | Candidate intervention after MVP failure analysis | Planned |
| allocation policy | Prior decision layer idea | Decision objective, constraints, cost function, and uncertainty interface | Is the policy compatible with calibrated uncertainty and tail-risk metrics? | Reimplement from first principles | Compare after independent decision task is defined | Planned |
| lambda ablation | Prior risk-aversion experiment | Risk preference meaning, sensitivity, and interpretability | Is lambda connected to an interpretable decision preference? | Reference only | Use only as historical warning or comparison | Planned |
| old result tables | Prior empirical record | Experimental setup, seeds, metrics, and reproducibility trace | Are old results reproducible and comparable to the new protocol? | Compare with prior prototype | Historical comparison only, not current evidence | Planned |
