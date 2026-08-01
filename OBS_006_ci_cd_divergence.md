# Observation 006 — The pipeline was identical. The source states were not.

A CI/CD pipeline was executed across multiple environments.

The same:

* build stages
* test stages
* validation stages
* deployment sequence
* automation logic

were used in each environment.

Every pipeline stage completed successfully.

No stage reported an execution failure.

---

But the resulting system states differed.

One environment reached the intended target state.

Another environment reached a different state despite following the same transition sequence.

The pipeline was identical.

The composed source environments were not.

---

## What changed

The execution path did not necessarily change.

The state from which execution began did.

Each environment contained its own combination of:

* existing configuration
* deployed dependencies
* identity and authority relationships
* policy scope
* infrastructure state
* service versions
* external integrations
* prior transitions

The same pipeline therefore operated against different composed system states.

An identical sequence of locally valid actions produced different global consequences.

---

## CNIG lens (informal)

A transition cannot be evaluated independently of the state from which it begins and the composition within which it occurs.

Identical execution does not guarantee identical reachability or admissibility when source states, constraints, dependencies, or system boundaries differ.

Pipeline success confirms that the declared stages completed.

It does not confirm that every resulting system state is equivalent or admissible.

---

## Primitives that feel relevant

### State Transition Validation

Transition validity depends on more than whether an action completed successfully.

It also depends on:

* the source state
* the applicable constraints
* the target state
* the affected system relationships
* the resulting reachable-state changes
* whether required invariants remain preserved

The same transition sequence may be valid from one source state and structurally divergent from another.

### Execution vs Governance Separation

Pipeline execution can remain locally correct while the resulting system state differs from governing intent.

A successful deployment is an execution result.

It is not, by itself, evidence that the resulting composed state is admissible.

### Admissible System State

Each resulting environment state must be evaluated against the constraints governing that environment and the wider system composition.

Two successfully deployed states are not necessarily structurally equivalent.

One may remain admissible while another does not.

---

## Potential structural conditions

This observation does not automatically establish a CNIG Failure Mode.

The structural cause must first be identified.

Depending on the available evidence, the divergence may involve:

* a source-state difference that changes transition validity
* an unrepresented dependency
* a constraint that applies differently across environments
* a reachable-state expansion in one environment
* a missing admissibility evaluation after deployment
* a temporal or version misalignment between related system states

Failure-mode attribution should remain unresolved until the relevant structural condition is established.

---

## Invariant feeling

The **Behavioral Invariant** may appear stable at the pipeline level because the same stages perform the same declared actions.

At the composed-system level, behaviour may diverge because those actions operate on different source states.

The **Structural Invariant** may weaken where environment-specific relationships, dependencies, or constraints change the effect of the same transition sequence.

The **Stability Invariant** may also be affected when small differences in source composition produce disproportionately different target states.

---

## Structural distinction

This observation is not about the same execution being understood differently.

It concerns the same execution sequence acting on structurally different system states.

The relevant question is not only:

> Did the pipeline complete successfully?

It is also:

> From what composed state did the transition begin, and what system state did it make reachable?

---

## Cross-link

Related to `OBS_003_pipeline_drift.md` and `OBS_009_silent_drift.md`.

`OBS_003` shows how individually valid pipeline stages can produce a different outcome when composed into a complete execution chain.

`OBS_006` shows how the same complete execution chain can produce different outcomes when applied to different composed source states.

`OBS_009` shows how accumulated structural relationships can gradually alter the reachable state space even when no individual transition is identified as invalid.
