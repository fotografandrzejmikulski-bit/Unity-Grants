# A.U.R.A. — Adaptive User Recovery Assistant

## Purpose

A.U.R.A. is the proposed adaptation layer for NeuroAdapt AI. Its job is to personalize task parameters from observable session performance while respecting hard safety and clinician-configured bounds.

**Important:** the initial implementation should be deterministic and interpretable. Machine-learning or reinforcement-learning components should be introduced only after a rule-based baseline is measurable and reproducible.

## Inputs

Normalized session signals may include:

- movement accuracy;
- movement smoothness;
- task completion time;
- reaction time;
- repetition count;
- error rate;
- interaction modality;
- user-selected difficulty;
- optional fatigue proxies when a validated sensor pathway exists.

Raw biomedical signals should not be sent into the adaptation policy without an explicit preprocessing and validation layer.

## Outputs

A.U.R.A. may adjust bounded task parameters:

- target size;
- movement tolerance;
- pacing;
- number of repetitions;
- distractor complexity;
- rest interval;
- interaction assistance.

## Policy hierarchy

```text
Safety constraints
       ↓
Clinician / protocol bounds
       ↓
Accessibility constraints
       ↓
Personalization policy
       ↓
Task parameters
```

A lower layer must never override a higher-priority constraint.

## Rule-based baseline

Example policy:

```text
IF completion_rate < lower_bound
    reduce difficulty one step
ELSE IF completion_rate > upper_bound
    increase difficulty one step
ELSE
    maintain difficulty

IF fatigue_flag = true
    reduce intensity and offer rest
```

All adaptations must be logged with:

- previous parameter state;
- new parameter state;
- triggering measurements;
- policy version;
- timestamp/session identifier.

## Future ML pathway

A future policy can be evaluated against the rule-based baseline using offline replay or synthetic environments before clinical use. Candidate methods include contextual bandits or reinforcement-learning policies, but any learned policy must remain constrained by the same safety and accessibility layer.

Minimum ML evaluation:

- held-out evaluation data;
- predefined success criteria;
- calibration/error analysis;
- subgroup analysis where sample size allows;
- robustness to missing/noisy sensor data;
- reproducible model versioning;
- rollback to a validated baseline.

## Prohibited behavior

A.U.R.A. must not infer a diagnosis from session data, alter medication, recommend emergency treatment, or present a probabilistic prediction as a clinician-approved prognosis.

## Synthetic-data testing

Before any patient data are used for model development, synthetic sessions should exercise edge cases:

- high error / low speed;
- high error / high speed;
- low error / high fatigue proxy;
- disconnected sensor;
- missing observations;
- abrupt hardware changes;
- accessibility mode changes.

The test harness should verify that outputs always remain within declared bounds.
