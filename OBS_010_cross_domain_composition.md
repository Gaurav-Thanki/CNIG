# Observation 010 — Each system remained locally admissible. Their integration created an unevaluated joint state.

Two independently governed systems were integrated.

For example:

* an identity system and a workflow system
* a cloud platform and an on-premises control plane
* an orchestration system and a protected resource domain
* a business application and an external automation service
* two infrastructure environments with separate governance boundaries

Each system had its own:

* state model
* authority structure
* constraints
* validation rules
* operational boundary
* admissibility conditions
* governing intent

Each system behaved correctly within its own boundary.

No individual system showed evidence of component failure or local constraint violation.

---

But after integration, the systems could jointly reach a state that neither local governance boundary represented in full.

One system produced a valid output.

The other accepted that output as a valid input or precondition.

A locally permitted transition in one domain activated a locally permitted transition in the other.

Each system continued to satisfy its own rules.

The combined state depended on both systems.

Neither system independently evaluated whether that joint state remained admissible.

---

## What changed

The internal rules of the individual systems did not necessarily change.

The relationship between their state spaces did.

Integration introduced:

* shared transition paths
* cross-domain preconditions
* identity or authority mappings
* translated state representations
* delegated operations
* synchronized resources
* data-triggered actions
* dependencies across governance boundaries
* effects that returned from one domain into the other

The interface connected two locally governed possibility spaces.

That connection created system states whose admissibility could not be established from either local constraint set alone.

---

## CNIG lens (informal)

Local admissibility does not establish compositional admissibility across governance boundaries.

Each system may correctly validate:

* its own source state
* its own transition
* its own authority conditions
* its own target state

while the integrated composition reaches a joint state outside the governing intent of the wider system.

The relevant question is not only:

> Did each system remain valid within its own boundary?

It is also:

> What joint states became reachable through the interface, and which constraints govern those states?

---

## Primitives that feel relevant

### Reachable State Space

Integration connects the reachable state spaces of independently governed systems.

A state in one domain may become:

* an input
* precondition
* authority signal
* trigger
* resource dependency
* or transition enabler

for another domain.

This can make joint states reachable that are absent from either system’s local model.

The resulting possibility space belongs to the composition, not to either system independently.

### Admissible System State

A joint state is not admissible merely because each contributing local state is admissible within its own domain.

Compositional admissibility must account for:

* cross-domain constraints
* combined authority
* shared resources
* transition effects
* boundary assumptions
* exclusions
* dependency conditions
* wider governing intent

Local admissibility is necessary within each domain.

It is not sufficient for the integrated system.

### State Transition Validation

Each domain may validate only the transitions it owns.

The complete cross-domain path may include:

* a source state in the first system
* an output or state change
* interface translation
* identity or authority mapping
* acceptance by the second system
* a downstream transition
* effects returned to the first system
* a resulting joint state

Local validation of every individual transition does not establish validity of the complete cross-domain transition path.

### Constraint-Native Governance

Each system may contain valid structural constraints.

The integration must also represent the constraints governing the relationship between those systems.

A boundary contract that defines only:

* data format
* protocol
* authentication
* transport
* execution sequence

does not necessarily define the admissibility conditions of the combined state space.

Governance must account for what the integration makes structurally possible.

### Execution vs Governance Separation

Both systems may execute correctly.

The interface may also function exactly as designed.

Those are execution results.

Whether the resulting joint state remains within governing intent is a separate governance question.

Successful integration does not establish compositional admissibility.

---

## Potential failure modes

### Implicit Reachability Expansion Failure

This Failure Mode may be relevant if evidence establishes that:

* integration made a new joint state reachable
* the state was absent from both represented local models
* no explicit governance decision acknowledged the expanded possibility space
* the state arose through locally valid cross-domain transitions
* the resulting state was outside governing intent

### Constitutional Fragmentation

This Failure Mode may be relevant if:

* each domain retains its own admissibility logic
* those local constraint sets do not establish one coherent rule for the joint state
* a state can remain locally admissible in both domains while violating the governing requirements of the composition
* no system boundary owns or resolves the combined constraint condition

Failure-mode attribution remains provisional until the relevant structural evidence is established.

Cross-domain integration does not constitute a CNIG Failure Mode merely because it introduces new joint states.

Those states may be deliberately represented, explicitly governed, validated, and admissible.

---

## Invariant feeling

The **Structural Invariant** may weaken where the integration creates relationships or joint states absent from the represented composition.

The **Behavioral Invariant** may appear preserved within both systems while the integrated system produces a different global outcome.

The **Identity Invariant** may become relevant where principals, authority, responsibility, or resource identity are not preserved across cross-domain mappings.

The **Stability Invariant** may be affected where a small change in one domain creates a disproportionate or unexpected state change in the other.

---

## Structural distinction

This observation is not about:

* ordinary communication between services
* source-state differences between equivalent environments
* aggregation of assignments within one identity system
* different observers interpreting the integration differently
* generic complexity caused by connecting systems

It concerns a specific structural condition:

> Independently governed systems compose into a joint state that neither local governance boundary represents or evaluates in full.

It is distinct from `OBS_005_service_coupling_drift.md`.

`OBS_005` concerns changes in interaction topology among services within a distributed composition.

`OBS_010` concerns the connection of separately governed state spaces and the absence or insufficiency of joint admissibility constraints at their boundary.

The relevant questions are:

> What joint states did the integration make reachable?

> Which constraints govern those states?

and:

> Where is compositional admissibility evaluated?

---

## Cross-link

Related to `OBS_001_identity_surface.md`, `OBS_005_service_coupling_drift.md`, `OBS_009_silent_drift.md`, and `OBS_011_governance_constraint_displacement.md`.

`OBS_001` shows how identity and authority can change structurally across composed system boundaries.

`OBS_005` shows how changed relationships between services alter available transition paths within a distributed system.

`OBS_009` shows how accumulated relationships can gradually alter the reachable state space without a single identifiable transition failure.

`OBS_010` shows how separately governed systems can create an unevaluated joint state when their state spaces are connected.

`OBS_011` shows how declared governance may remain locally present while failing to constrain the complete reachable state space of the composition.
