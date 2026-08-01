# Observation 009 — Nothing failed. The reachable state space changed.

All system components remained healthy.

No alerts triggered.

No errors appeared.

No individual transition was identified as invalid.

---

But over time, the composed system began permitting behaviour that had not previously been reachable.

The change was gradual.

Additional relationships, dependencies, configuration interactions, and locally accepted transitions accumulated across the system.

No single event fully explained the resulting state.

---

## What changed

The components did not necessarily change.

The composition did.

As interaction relationships accumulated, the system’s reachable state space changed.

A state that was previously unavailable, excluded, or structurally unrepresented became reachable through the combined effect of otherwise valid system relationships.

---

## CNIG lens (informal)

A structural failure does not always appear as an error.

It may appear as a change in what the composed system can reach.

The absence of component failure does not establish that the reachable state space has remained stable.

---

## Primitives that feel relevant

### Reachable State Space

System composition may expand or alter the set of reachable states without a single explicit transition introducing the complete change.

The effect may emerge through the accumulation of several locally valid relationships.

### Admissible System State

A newly reachable state is not automatically admissible.

The resulting state must still be evaluated against the constraints governing the composed system.

### State Transition Validation

Individual transitions may remain locally valid while their accumulated effect changes the global system state.

Transition validity therefore includes the structural consequences of a sequence, not only the validity of each isolated step.

---

## Potential failure mode

**Implicit Reachability Expansion Failure**

The composed system makes a state reachable that was not represented in the original structural model or explicitly introduced through a deliberate governing decision.

The expansion may occur gradually through accumulated relationships rather than through one identifiable change.

Failure-mode attribution remains provisional unless the evidence establishes that:

* the state was previously outside the represented reachable space
* composition introduced the new path
* no isolated component fault or ordinary misconfiguration explains the outcome
* the expansion was not explicitly acknowledged by the governing structure

---

## Invariant feeling

The **Stability Invariant** may appear preserved within each component while the system-level possibility space changes over time.

The **Structural Invariant** may weaken when accumulated relationships alter how components can combine, even though the components themselves remain unchanged.

The **Behavioral Invariant** may also become inconsistent when the same locally valid components produce newly reachable global outcomes under the changed composition.

---

## Structural distinction

This observation is not about different observers understanding the same system differently.

It concerns an actual change in system structure and the states that structure makes reachable.

The relevant question is not whether the system appears different.

It is whether the composition now permits a state that was previously unavailable, excluded, or unrepresented.

---

## Cross-link

Related to `OBS_003_pipeline_drift.md` and `OBS_011_governance_constraint_displacement.md`.

`OBS_003` shows how locally valid pipeline stages can produce a different outcome when executed as a composed chain.

`OBS_009` shows how accumulated structural relationships can gradually alter the reachable state space without a single visible failure event.

`OBS_011` shows how declared governance may remain present while no longer constraining the expanded reachable state space.
