# Inclusion & Accessibility

## Co-design requirement

The project specification calls for direct participation from people with lived experience of stroke and prosthetic use. This must become auditable project practice rather than a narrative statement.

For each design cycle record:

- participant profile at an appropriate level of aggregation;
- accessibility barriers identified;
- proposed change;
- prototype tested;
- result;
- unresolved issue;
- decision owner.

## Accessibility modes

### Motor

- reduced precision requirement;
- target enlargement;
- adjustable dwell times;
- reduced repetition intensity;
- alternative controller/hand input.

### Cognitive

- one-action-at-a-time navigation;
- consistent layouts;
- adjustable instruction pacing;
- optional voice guidance;
- reduced distractors.

### Visual

- adjustable contrast;
- scalable UI;
- reduced visual motion;
- configurable visual effects;
- clear target affordances.

### Auditory

- captions/subtitles;
- independent volume controls;
- non-audio alternatives for essential cues.

### Communication

- pictogram-based instructions;
- plain-language copy;
- localization-ready text assets;
- assistive communication compatibility where technically feasible.

## XR comfort and safety

Users should be able to pause or terminate a session immediately. Avoid unnecessary camera motion, acceleration, flashing effects, and forced orientation changes. Comfort settings must be applied consistently across scenes.

The project should not claim that accessibility settings "eliminate" a seizure risk. Risk mitigation is a design and clinical safety process and requires validation with the intended population.

## Offline-first principle

The rehabilitation session should remain functional without continuous internet connectivity where technically and clinically appropriate. Synchronization should be opportunistic and should never be required for immediate session safety.

## Accessibility acceptance tests

Every release should test at minimum:

1. reduced-motion mode;
2. captions and audio alternatives;
3. large-target mode;
4. alternative input mode;
5. interruption/pause flow;
6. sensor-loss fallback;
7. localization expansion;
8. session completion without cloud connectivity.
