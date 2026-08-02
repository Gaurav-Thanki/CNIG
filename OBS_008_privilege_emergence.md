# Observation 008 — The permission stayed the same. Its reachable effect expanded.

A principal or service had permission to perform a defined operation.

The relevant:

* identity
* role
* permission
* policy
* authorization condition
* invocation path
* approval requirement

remained unchanged.

The same authorization check continued to succeed.

No additional role was assigned.

No new direct access rule was introduced.

---

But exercising the permitted operation began producing a broader system-level effect.

The operation could now:

* affect additional resources
* trigger additional services
* activate a wider workflow
* modify shared state used by other systems
* invoke downstream authority
* reach additional target environments
* initiate transitions outside its original represented scope

The initiating permission had not changed.

The composition behind the permitted operation had.

---

## What changed

The access decision did not necessarily change.

The system relationships activated after that decision did.

A permission that originally enabled one bounded operation became connected to additional:

* downstream services
* resource collections
* orchestration stages
* delegated capabilities
* automation paths
* shared-state relationships
* control-plane operations
* transitive side effects

The same locally permitted action therefore produced a broader effective capability.

The permission remained stable.

The set of system states reachable by exercising it expanded.

---

## CNIG lens (informal)

Permission scope cannot always be determined from the authorization rule alone.

The effective capability associated with a permission also depends on the system relationships and transitions activated after authorization succeeds.

The relevant structural question is not only:

> Is this principal permitted to invoke the operation?

It is also:

> What complete system effect becomes reachable when that permitted operation executes through the current composition?

---

## Primitives that feel relevant

### Privilege Surface

Privilege Surface describes effective interaction, authority, capability, and control pathways created through composition.

A permission may appear unchanged at its local authorization boundary while its effective privilege expands because the operation now connects to:

* additional resources
* more authoritative services
* broader workflows
* delegated operations
* new control paths
* wider downstream effects

The effective privilege associated with an operation therefore includes the complete capability path activated behind the permission boundary.

The declared permission does not necessarily describe the complete effect available through that path.

### Reachable State Space

The same authorized operation may make additional system states reachable after downstream composition changes.

Those states may become reachable through:

* expanded resource membership
* new service dependencies
* additional workflow stages
* delegated execution
* orchestration changes
* broader shared-state effects
* newly connected control relationships

The reachable state space can therefore expand without a change to the permission that initiates the transition.

### State Transition Validation

Authorization validates whether an initiating action is locally permitted.

It does not necessarily validate every transition and side effect that follows.

Evaluation of the complete path includes:

* the initiating state
* the authorized operation
* downstream service calls
* delegated authority
* affected resources
* intermediate states
* transitive side effects
* the final target state
* the constraints and invariants that must remain preserved

A locally valid authorization decision does not establish admissibility of the complete transition path activated by that decision.

### Execution vs Governance Separation

The authorization component may correctly approve the operation.

Every downstream service may also execute correctly.

Those are execution properties.

Whether the complete resulting capability and target state remain within governing intent is a governance question.

Correct enforcement of an unchanged permission does not establish that its current system-level effect remains admissible.

---

## Potential failure mode

**Privilege Surface Expansion Failure** may be relevant if evidence establishes that:

* an existing permission now activates a broader effective capability
* the expansion resulted from downstream composition rather than a direct permission change
* the complete capability path was absent from the intended structural model
* no explicit authorization or governance decision acknowledged the broader effect
* the resulting action or system state was outside governing intent

Failure-mode attribution remains provisional until those conditions are supported.

A permitted operation does not exhibit a CNIG Failure Mode merely because its downstream implementation changes or affects several components.

The broader effect may be deliberately designed, explicitly represented, properly authorized, constrained, and admissible.

---

## Invariant feeling

The **Behavioral Invariant** may weaken when the same authorized operation produces a materially broader system-level result after composition changes.

The **Structural Invariant** may weaken when downstream relationships extend the operation beyond the boundaries represented by its permission or original design.

The **Stability Invariant** may be affected when a small change in resource membership, orchestration, dependency structure, or downstream authority produces a disproportionately larger operational effect.

The **Identity Invariant** becomes relevant only where the authority attributed to the initiating principal is not preserved through delegated or service-mediated execution.

---

## Structural distinction

This observation is not about:

* a new direct permission
* a new access route to a protected resource
* several identity assignments aggregating into broader authority
* an authorization component incorrectly approving an action
* different observers interpreting the same permission differently

The access boundary may remain unchanged.

The distinctive condition is:

> The system-level capability available through an existing permission expands because the composition activated behind that permission changes.

The relevant questions are:

> What complete effect does the permitted operation now make reachable?

and:

> Is that expanded effect represented, authorized, constrained, and admissible?

---

## Cross-link

Related to `OBS_002_access_surface.md`, `OBS_004_identity_aggregation.md`, and `OBS_005_service_coupling_drift.md`.

`OBS_002` shows how locally permitted relationships can form a new effective access path without a direct permission change.

`OBS_004` shows how valid identity assignments combine into an aggregated authority state.

`OBS_005` shows how changed service relationships alter the transition paths and states available to a distributed system.

`OBS_008` shows how an existing permission can retain the same entry boundary while acquiring a broader effective capability through changes in downstream composition.
