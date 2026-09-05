# Research

This directory contains research-facing specifications, synthetic-data experiments, and eventually approved study artifacts.

## Separation of concerns

- `docs/` defines intended product, impact, governance, and safety behavior.
- `research/` contains experimental methods and analyses.
- `prototype/` contains executable product work.

## Reproducibility requirements

Every experiment should record:

- hypothesis;
- dataset origin;
- preprocessing;
- train/validation/test separation;
- software version;
- model/policy version;
- random seed where applicable;
- metrics;
- failure cases;
- limitations.

No patient-identifiable information belongs in the public repository.
