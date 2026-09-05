# Risk Register

| ID | Risk | Probability | Impact | Mitigation | Gate |
|---|---|---:|---:|---|---|
| R1 | Project remains conceptual | High | High | Deliver runnable Unity vertical slice | Prototype review |
| R2 | Scope too broad for funding | High | High | Prioritize one core rehabilitation loop | Milestone planning |
| R3 | Sensor integration unstable | Medium | High | Hardware abstraction + fallback input | Integration test |
| R4 | Adaptive model behaves unpredictably | Medium | Critical | Rule-based baseline + hard bounds + rollback | Safety review |
| R5 | Clinical claims exceed evidence | Medium | Critical | Claims register + research sign-off | External review |
| R6 | Privacy architecture inadequate | Medium | Critical | Threat model + data minimization + security review | Data-governance gate |
| R7 | XR discomfort | Medium | High | Comfort settings + device profiling + user testing | UX gate |
| R8 | Accessibility fails for intended users | Medium | High | Co-design + acceptance testing | Accessibility gate |
| R9 | Regulatory pathway misunderstood | Medium | Critical | Qualified regulatory assessment | Deployment gate |
| R10 | Global deployment assumptions unrealistic | High | Medium | Pilot one or two representative contexts first | Expansion gate |
| R11 | Clinical recruitment slower than planned | Medium | High | Staged pilot + contingency recruitment plan | Study gate |
| R12 | AI model lacks generalization | Medium | High | Held-out evaluation + subgroup analysis + baseline comparison | ML gate |

## Go/no-go gates

### Gate A — Prototype

Proceed only when the core task loop is runnable, repeatable, interruptible, and documented.

### Gate B — Integrated prototype

Proceed only when telemetry, accessibility, adaptation, and sensor abstraction operate together without unsafe failure behavior.

### Gate C — Human research

Proceed only after required ethics/governance approvals and participant-safety procedures are in place.

### Gate D — Clinical validation

Proceed only under an approved protocol with qualified clinical oversight and predefined endpoints.

### Gate E — Deployment

Proceed only after the intended-use statement, regulatory pathway, privacy/security controls, support model, and release documentation are complete.
