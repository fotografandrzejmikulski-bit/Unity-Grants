# NeuroAdapt AI

## Immersive Neuromotor Rehabilitation & Prosthetic Adaptation

**Grant track:** Unity for Humanity / social-impact RT3D  
**Status:** Early-stage production / evidence-ready project foundation  
**Primary domains:** neurorehabilitation, prosthetic adaptation, XR, accessibility, adaptive interaction

> **Evidence policy:** This repository distinguishes implemented, prototyped, and planned capabilities. It does not present clinical outcomes, partnerships, certifications, or technical integrations as completed unless they are supported by repository evidence.

## Why this project exists

NeuroAdapt AI is a proposed Unity-based RT3D rehabilitation environment for people recovering from neurological injury and for people adapting to upper-limb prostheses. The design combines immersive interaction, adaptive task difficulty, accessible interfaces, and measurable rehabilitation workflows.

The project brief identifies two principal use cases:

1. neuromotor training after stroke;
2. adaptation and training for people using prosthetic limbs, including mirror-therapy-inspired workflows for phantom-limb pain management.

The project brief also proposes an adaptive AI layer named **A.U.R.A. — Adaptive User Recovery Assistant**.

## Current repository status

This repository is currently a **grant-facing project foundation**, not a claim of completed clinical software.

| Capability | Repository status | Evidence required before claiming completion |
|---|---|---|
| Unity RT3D application | Planned/prototyping foundation | Unity project and runnable build |
| XR interaction | Architecture defined | Device test report |
| Hand tracking | Architecture defined | Supported-device integration demo |
| EMG integration | Planned | Sensor SDK adapter + validation |
| A.U.R.A. adaptive difficulty | Design specification | Reproducible prototype |
| ML/RL personalization | Research/prototype stage | Model, evaluation protocol, benchmark |
| Clinical telemetry | Design stage | Data dictionary + privacy/security implementation |
| Clinical efficacy | Not established | Ethics-approved study + statistical analysis |
| Medical-device certification | Not established | Formal regulatory pathway and documentation |

## Project architecture

```text
+-----------------------------+
|        Unity XR Client      |
|-----------------------------|
| Accessibility / UX          |
| Rehabilitation Tasks        |
| Interaction Layer            |
| Session Controller           |
+--------------+--------------+
               |
        normalized signals
               v
+-----------------------------+
|     A.U.R.A. Adaptation     |
|-----------------------------|
| Fatigue / performance state |
| Difficulty policy            |
| Safety constraints           |
| Personalization              |
+--------------+--------------+
               |
               +--------------------+
               |                    |
               v                    v
      +----------------+   +----------------+
      | Local metrics  |   | Optional sync  |
      | / session data |   | / research API |
      +----------------+   +----------------+
```

## Design principles

### Patient-first interaction
Tasks should minimize cognitive overhead and make the next therapeutic action obvious.

### Adaptive difficulty, not adaptive medical judgment
A.U.R.A. may adjust task parameters such as target size, movement tolerance, repetition, pacing, or environmental complexity. It must not independently diagnose, prescribe treatment, or override clinician-defined safety constraints.

### Accessibility by default
The architecture anticipates configurable interaction modes including hand tracking, controller input, gaze-based navigation where supported, voice guidance, pictograms, reduced visual stimulation, and low-bandwidth/offline operation.

### Evidence before claims
Clinical benefit, pain reduction, adherence improvements, demographic reach, and certification are outcome claims. They belong in research documentation only after appropriate evidence exists.

## Impact framework

The project brief targets the following UN Sustainable Development Goals:

- **SDG 3 — Good Health and Well-Being**
- **SDG 10 — Reduced Inequalities**
- **SDG 9 — Industry, Innovation and Infrastructure**

Proposed outcome measures include motor-performance measures, session adherence, patient-reported outcomes, usability, and accessibility metrics. Specific clinical targets are treated as **study hypotheses**, not guaranteed results.

## Safety and medical governance

NeuroAdapt AI is intended as a research and development project. Any clinical deployment requires appropriate clinical governance, informed consent, ethics review where applicable, data protection controls, adverse-event procedures, and a determination of the applicable medical-device regulatory pathway.

The repository intentionally avoids asserting that encryption or software architecture alone establishes HIPAA or GDPR compliance. Compliance is a system-, organizational-, contractual-, and jurisdiction-specific matter.

## Grant alignment

Unity's current public FAQ states that Unity for Humanity supports impact-driven RT3D projects that are in production beyond conceptualization with a prototype or demo, and evaluates applications across **Vision, Impact, Inclusion, and Viability**, each weighted at 25%. citehttps://unity.com/humanity

The 2026 call allocated $600,000 across multiple projects and had a February 20, 2026 deadline. Applications are currently closed; Unity states that applications will open again in 2027. citehttps://unity.com/blog/unity-for-humanity-2026-grant-now-open citehttps://unity.com/humanity

## Repository roadmap

- [ ] Unity application prototype
- [ ] Interaction abstraction layer
- [ ] Accessibility settings
- [ ] Rehabilitation task framework
- [ ] A.U.R.A. rule-based baseline
- [ ] Synthetic-data evaluation harness
- [ ] EMG adapter interface
- [ ] Research telemetry schema
- [ ] Privacy and threat model
- [ ] Usability testing protocol
- [ ] Clinical study protocol draft
- [ ] Grant pitch deck
- [ ] Demonstration video

## Directory structure

```text
.
├── README.md
├── docs/
│   ├── GRANT_STRATEGY.md
│   ├── PROJECT_SPECIFICATION.md
│   ├── AURA_SPEC.md
│   ├── IMPACT_AND_KPI_FRAMEWORK.md
│   ├── INCLUSION_AND_ACCESSIBILITY.md
│   ├── CLINICAL_RESEARCH_FRAMEWORK.md
│   ├── DATA_PRIVACY_AND_SECURITY.md
│   ├── RISK_REGISTER.md
│   ├── ROADMAP.md
│   └── EVIDENCE_STATUS.md
├── research/
│   └── README.md
├── prototype/
│   └── README.md
└── .github/
    └── ISSUE_TEMPLATE/
        └── evidence-gap.md
```

## Licensing and contribution

Until the legal entity, ownership model, and clinical/research partnerships are finalized, repository contributions should be treated as project-development artifacts rather than evidence of institutional endorsement.
