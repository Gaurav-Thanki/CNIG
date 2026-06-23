# Observation 003 — Pipelines behave differently when composed

A pipeline system was consistent.

Each stage was correct:
- build
- test
- validate
- deploy

---

But when executed as a full chain across environments, outcomes changed.

Not because any stage failed.

But because composition changed behavior.

---

## What changed

Each part stayed correct.

The whole behaved differently.

---

## CNIG lens (informal)

Execution correctness does not guarantee compositional correctness.

---

## Primitive that feels relevant

Execution vs Governance Separation

Local correctness does not fully describe global outcome.

---

## Invariant feeling

Stability weakens across boundaries between environments.

---

## Cross-link

Related to OBS_002_access_surface.md
