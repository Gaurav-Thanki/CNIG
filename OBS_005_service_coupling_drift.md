# Observation 005 — Services remain correct, system drifts

A distributed system had correct services.

Each service:
- passed health checks
- responded correctly
- behaved consistently

---

But at scale, the system began behaving differently.

Not failing.

Just drifting in behavior.

---

## What changed

No service changed.

Only interactions changed.

---

## CNIG lens (informal)

Interaction structure dominates component correctness.

---

## Primitive that feels relevant

Privilege Surface

Interaction paths create new effective behavior surfaces.

---

## Invariant feeling

Structural Invariant holds locally, weakens globally.

---

## Cross-link

Related to OBS_003_pipeline_drift.md
