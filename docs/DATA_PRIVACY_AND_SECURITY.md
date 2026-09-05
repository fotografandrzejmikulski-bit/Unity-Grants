# Data Privacy & Security

## Scope

NeuroAdapt AI may process interaction and, in some configurations, biomedical sensor data. Such data can be sensitive and must be governed according to the actual deployment, jurisdiction, controller/processor roles, contracts, and applicable law.

## Data minimization

Default telemetry should contain only:

- pseudonymous session identifier;
- application/build version;
- task identifier;
- event type;
- event timestamp;
- task-performance fields required by the research/product objective.

Identity data and research/session data should be logically separated.

## Security architecture

```text
Device
  │
  ├── local encrypted storage (where required)
  │
  └── authenticated sync
          │
          v
     API gateway
          │
          ├── authorization
          ├── validation
          ├── audit logging
          └── rate limiting
          │
          v
     research/product datastore
```

## Threat model

Primary threats include:

- unauthorized access to sensitive records;
- accidental collection of unnecessary identifiers;
- compromised device;
- malicious or altered telemetry;
- insecure synchronization;
- over-retention;
- re-identification from supposedly anonymous datasets.

## Controls

Recommended controls include:

- least-privilege access;
- authenticated APIs;
- encryption in transit;
- encryption at rest where appropriate;
- key rotation and secret management;
- audit trails;
- environment separation;
- dependency and vulnerability scanning;
- retention/deletion policies;
- incident-response procedures;
- periodic access review.

## HIPAA / GDPR wording

The project should not state that a standalone Unity application is "HIPAA compliant" or "GDPR compliant" as a universal property. HIPAA applicability depends on covered entities/business associates and context. GDPR obligations depend on roles, processing activities, jurisdictions, legal basis, data categories, and organizational controls.

External grant materials should therefore use wording such as:

> "The system will be engineered to support applicable privacy and security obligations in the deployment jurisdictions, subject to formal legal, clinical, and organizational review."

## Data lifecycle

```text
Collection → Validation → Pseudonymization → Controlled storage
       → Authorized analysis → Retention limit → Secure deletion
```

## AI-specific governance

AI training data must have documented provenance, permitted use, quality controls, versioning, and leakage prevention. Patient data must not be silently repurposed for model development outside the approved research/data-governance scope.
