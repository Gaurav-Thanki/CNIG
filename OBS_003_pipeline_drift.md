# Observation 003 — Each stage was valid. The chain reached an unvalidated state.

A delivery pipeline contained several stages:

* build
* test
* validate
* approve
* deploy

Each stage behaved correctly.

Each stage:

* accepted the expected input
* performed its declared action
* produced the expected output
* returned a successful status
* satisfied its local validation conditions

No individual stage reported a failure.

---

But when the stages executed as a complete chain, the pipeline reached a final system state that no individual stage had represented or evaluated.

The build was valid.

The tests passed.

Validation completed.

Approval was granted.

Deployment succeeded.

The complete resulting state had not been assessed by any one stage.

---

## What changed

The correctness of the individual stages did not necessarily change.

Their outputs became the inputs, conditions, and structural context of later stages.

Across the complete chain, the pipeline accumulated:

* artifacts
* configuration state
* dependency state
* identity and authority context
* approval scope
* environment relationships
* effects from prior transitions

Each stage validated its local transition.

No stage necessarily validated the structural consequence of the complete transition sequence.

The chain therefore produced a system-level result that could not be inferred from stage-level success alone.

---

## CNIG lens (informal)

A sequence of locally valid transitions does not automatically preserve global admissibility.

Pipeline success establishes that the declared stages completed.

It does not establish that the complete transition path remained within the intended admissible state space.

The relevant question is not only whether every stage succeeded.

It is whether the composition of those successful stages produced an admissible target state.

---

## Primitives that feel relevant

### State Transition Validation

A transition sequence must be considered as more than a collection of individually accepted steps.

Evaluation includes:

* the initial source state
* each intermediate state
* the relationships introduced between stages
* the cumulative effects of prior transitions
* the final target state
* the constraints and invariants that must remain preserved

Local transition acceptance does not establish validity of the complete transition path.

### Execution vs Governance Separation

Every pipeline stage may execute correctly while the chain produces a state outside governing intent.

Stage completion is an execution property.

Target-state admissibility is a governance property.

One does not establish the other.

### Admissible System State

The final state must be evaluated independently of whether the stages that produced it succeeded.

A successfully reached state may still be structurally inconsistent with the constraints governing the composed system.

### Reachable State Space

Pipeline composition can make states reachable that were not visible when stages were considered independently.

The full chain may therefore expose structural possibilities absent from stage-level analysis.

---

## Potential failure mode

**Implicit Reachability Expansion Failure** may be relevant if evidence establishes that:

* the complete chain made a new state reachable
* the state was absent from the represented structural model
* no individual stage explicitly introduced or governed the complete outcome
* the expansion resulted from stage composition rather than an isolated fault
* the new state was not deliberately acknowledged by the governing structure

Failure-mode attribution remains provisional until those conditions are supported.

If the final state was represented, intended, and admissible, the observation does not establish a CNIG Failure Mode merely because no individual stage evaluated it alone.

---

## Invariant feeling

The **Behavioral Invariant** may appear preserved within every stage while the complete chain produces an unintended system-level outcome.

The **Structural Invariant** may weaken where relationships between stage outputs, intermediate states, and later transitions create effects not represented in the pipeline’s local validation boundaries.

The **Stability Invariant** may also be affected if minor changes in stage order, dependency state, or intermediate conditions produce disproportionately different target states.

---

## Structural distinction

This observation is not about different observers interpreting the same pipeline differently.

It concerns the actual structural consequence of composing valid stages into a complete transition chain.

It is also distinct from source-state divergence.

The relevant condition here is:

> Individually valid stages produce an unvalidated system-level result through their composition.

The relevant question is:

> What final state did the complete chain make reachable, and was that state admissible?

---

## Cross-link

Related to `OBS_006_ci_cd_divergence.md` and `OBS_009_silent_drift.md`.

`OBS_003` shows how individually valid stages can produce an unvalidated result when composed into one complete transition chain.

`OBS_006` shows how the same complete transition chain can produce different results when applied to different composed source states.

`OBS_009` shows how accumulated structural relationships can gradually alter the reachable state space without a single identifiable transition failure.
