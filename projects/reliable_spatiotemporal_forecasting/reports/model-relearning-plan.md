# Model Relearning Plan

## Purpose

Rebuild understanding before implementation.

| Module | Core Questions | Primary-Source Reading Needed | Derivation or Explanation Required | Minimal Verification Task | Status |
| ------ | -------------- | ----------------------------- | ---------------------------------- | ------------------------- | ------ |
| forecasting task definition | What is predicted, at what horizon, and under what data assumptions? | Required before implementation | Formal task statement and target definition | Write task definition and expected inputs/outputs | Planned |
| chronological split and normalization | How are temporal order and training-only statistics preserved? | Required before implementation | Split rationale and leakage analysis | Specify train, validation, calibration, and test protocol | Planned |
| graph construction | What graph is used and why is it meaningful? | Required before implementation | Graph assumption explanation | Define graph candidates and sensitivity checks | Planned |
| graph convolution foundations | What operation is being applied over graph structure? | Required before implementation | Derive or explain graph convolution mechanism | Explain how graph convolution uses adjacency information | Planned |
| STGCN | What assumptions does STGCN make about space and time? | Required before implementation | Architecture explanation and failure modes | Reproduce architecture diagram and baseline role | Planned |
| DCRNN | What diffusion and recurrence assumptions are used? | Required before implementation | Architecture explanation and multi-step behavior | Explain teacher forcing or rollout decisions | Planned |
| multi-step forecasting | How do errors and uncertainty propagate across horizons? | Required before implementation | Multi-step evaluation protocol | Define horizon-specific metrics | Planned |
| aleatoric versus epistemic uncertainty | What uncertainty sources are being represented? | Required before UQ implementation | Conceptual distinction and examples | Map each UQ method to uncertainty type assumptions | Planned |
| MC Dropout | What approximation is being used and when can it fail? | Required before UQ implementation | Bayesian approximation explanation | Define inference-time sampling protocol | Planned |
| Deep Ensemble | What diversity source supports uncertainty estimation? | Required before UQ implementation | Ensemble training and aggregation explanation | Define seed and aggregation protocol | Planned |
| Split Conformal Prediction | What coverage guarantee is targeted? | Required before UQ implementation | Conformal calibration explanation | Define calibration split and score function | Planned |
| exchangeability | Why does exchangeability matter for coverage? | Required before conformal evaluation | Assumption and failure analysis | Identify where temporal data may violate exchangeability | Planned |
| adaptive conformal inference | How can coverage adapt under shift? | Required before extension | Adaptation mechanism explanation | Define extension trigger after MVP results | Planned |
| probabilistic metrics | Which metrics evaluate distributional forecasts? | Required before evaluation | Metric definitions and limitations | Define CRPS, WIS, calibration, and interval metrics | Planned |
| selective prediction | When should the model abstain or request review? | Required before decision evaluation | Risk–coverage explanation | Define thresholding and review policy | Planned |
| decision-cost design | What cost function reflects downstream decisions? | Required before decision evaluation | Cost components and assumptions | Define under-allocation, over-allocation, and constraint costs | Planned |
| tail risk and CVaR | How are severe failures measured? | Required before decision evaluation | Tail-risk and CVaR explanation | Define tail threshold and aggregation method | Planned |
| representation-stability extension | What representation-level hypothesis is being tested? | Required only after MVP failure evidence | Diagnostic hypothesis and method rationale | Write activation condition and required model outputs | Planned |
