# Impact & KPI Framework

## Evidence hierarchy

Clinical endpoints must be distinguished from product telemetry. A product metric is not automatically a clinical outcome.

### Tier 1 — engagement and usability

- session completion rate;
- sessions per week;
- dropout rate;
- time-on-task;
- System Usability Scale or another selected validated usability measure;
- accessibility feature usage.

### Tier 2 — task performance

- movement accuracy;
- completion time;
- trajectory/smoothness metrics;
- error rate;
- repetitions completed.

### Tier 3 — clinical outcomes

Selected in cooperation with qualified clinicians and the study protocol. Instruments should be validated for the relevant population and use case.

### Tier 4 — patient-reported outcomes

May include pain intensity, confidence, perceived exertion, quality-of-life measures, or other validated instruments. The exact instruments must be specified in the study protocol.

## Proposed KPI table

| Domain | KPI | Target status | Measurement | Evidence standard |
|---|---|---|---|---|
| Engagement | Sessions/week | Hypothesis | Application telemetry | Reproducible logs |
| Adherence | 12-week retention | Hypothesis | Session records | Predefined analysis |
| Task performance | Accuracy / completion time | Hypothesis | Task engine metrics | Validated metric definition |
| Accessibility | Successful completion by modality | Hypothesis | Modality-tagged sessions | Accessibility test protocol |
| Usability | Usability score | Hypothesis | Validated questionnaire | Research protocol |
| Pain | Change from baseline | Hypothesis | Validated patient-reported instrument | Clinical study |
| Motor function | Change from baseline | Hypothesis | Clinician-selected validated measure | Clinical study |

## Correct treatment of the draft's previous numeric claims

The source project draft proposed outcomes including 30% improvement, an average 4-point reduction in VAS pain, 75% adherence, and deployment to 50 Global South clinics. Those figures are retained as **proposed targets/hypotheses**, not established facts.

Before using any target in an external grant application, document:

1. baseline definition;
2. population and inclusion criteria;
3. sample-size rationale;
4. comparator or control condition where applicable;
5. measurement instrument;
6. statistical analysis plan;
7. missing-data handling;
8. clinically meaningful effect threshold;
9. study duration;
10. governance/ethics pathway.

## Telemetry principles

Telemetry should be event-based and purpose-limited. Recommended event families:

```text
session_started
session_paused
session_completed
trial_started
trial_completed
adaptation_applied
accessibility_changed
sensor_connected
sensor_disconnected
error_state
safety_stop
```

Each event should carry a pseudonymous session ID, application version, task ID, timestamp, and only the minimum contextual fields necessary for analysis.

## Impact dashboard

The future project dashboard should report:

- numerator and denominator for every rate;
- confidence intervals where appropriate;
- missing-data rate;
- subgroup results when statistically defensible;
- protocol deviations;
- software/model version.

Avoid presenting aggregate percentages without denominators.
