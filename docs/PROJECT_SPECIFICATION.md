# Project Specification

## Product definition

**Working title:** NeuroAdapt AI  
**Core platform:** Unity RT3D  
**Target form factors:** Standalone XR first; extensible to additional input/display modes.

## Primary users

### User group A — stroke recovery
People undergoing supervised or home-based neuromotor rehabilitation after stroke, subject to clinician-defined suitability and safety criteria.

### User group B — prosthetic adaptation
People learning to control and incorporate an upper-limb prosthesis into functional movement and task performance.

## Product boundaries

NeuroAdapt AI is a rehabilitation-support system. It should provide:

- repeatable motor tasks;
- configurable difficulty;
- objective task telemetry;
- accessibility options;
- session summaries;
- clinician/research export pathways where governance permits.

It should not independently:

- diagnose disease;
- determine medical eligibility;
- change a prescribed treatment plan;
- make emergency clinical decisions;
- claim efficacy without validated evidence.

## Core loop

```text
Calibration → Baseline task → Adaptive task selection → User performs task
       ↑                                      ↓
       └──── Safety / fatigue / accessibility constraints ← Metrics
```

## Functional modules

1. **Session Manager** — starts, pauses, resumes, and closes therapy sessions.
2. **Input Abstraction** — presents a normalized interaction stream regardless of whether input originates from controllers, hand tracking, gaze, or an external sensor adapter.
3. **Task Engine** — defines therapeutic tasks independently of rendering.
4. **Difficulty Controller** — applies bounded difficulty changes.
5. **Accessibility Layer** — applies user preferences and clinically permitted interaction alternatives.
6. **Telemetry Layer** — captures only the minimum data required for product/research objectives.
7. **Local Data Store** — supports offline-first operation.
8. **Sync Gateway** — optional, policy-controlled synchronization when connectivity and authorization exist.

## Non-functional requirements

### Performance

The target should be defined per device tier rather than relying on a single universal frame-rate claim. For comfort-sensitive XR builds, performance budgets must be validated on the actual target hardware.

### Reliability

The session must fail safely when optional sensors disconnect. The core application should never treat missing sensor data as a successful therapeutic signal.

### Privacy

Collect the minimum necessary data, separate identity from research/session identifiers, encrypt data in transit and at rest where applicable, and document retention/deletion procedures.

### Accessibility

Accessibility features must be testable individually and in combination. Examples include larger targets, slower pacing, reduced visual motion, simplified navigation, voice guidance, alternative input, and adjustable audio/visual stimulation.

## Technical maturity levels

- **M0 — concept:** no executable artifact.
- **M1 — interaction prototype:** core interaction can be demonstrated.
- **M2 — integrated prototype:** task, adaptation, telemetry, and accessibility work together.
- **M3 — pilot-ready:** reproducible build plus test protocols and governance artifacts.
- **M4 — validated deployment:** evidence supports the intended use and the applicable regulatory pathway has been addressed.

The repository currently documents the target architecture; it must not imply M3/M4 status until those artifacts actually exist.
