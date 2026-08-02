# Observation 001 — The principal remained the same. Its effective authority changed across composition.

A system used the same principal across several identity and infrastructure contexts.

The relevant identity records were valid.

The:

* user account
* directory object
* group memberships
* assigned roles
* authentication claims
* service mappings
* local permissions

were each correct within their own system boundaries.

No individual identity system showed evidence of corruption, unauthorized modification, or component failure.

---

But when the identity relationships were composed across systems, the principal acquired a different effective authority state.

The principal could move through combinations of:

* nested groups
* inherited roles
* federated claims
* delegated access
* service-to-service mappings
* token exchanges
* workload identities
* resource-specific permissions

Each relationship was locally valid.

The complete authority path was not represented by any one identity boundary.

The principal remained the same.

The set of actions and resources reachable through that principal changed under composition.

---

## What changed

The originating identity did not necessarily change.

The relationships surrounding it did.

A locally valid identity representation became connected to additional roles, mappings, delegation paths, and resource contexts.

Across the complete composition:

* one group membership activated another role
* one role satisfied a downstream authorization condition
* one identity claim mapped to a different local principal
* delegated authority became available to another service
* a service identity acted on behalf of the originating principal
* inherited permissions combined across resource boundaries
* authority accumulated through several individually valid relationships

The resulting authority state could not be determined from the originating identity record alone.

---

## CNIG lens (informal)

Identity continuity does not establish authority continuity.

A principal may remain correctly identified while the composition of identity, role, delegation, and resource relationships changes what that principal can reach or cause.

The relevant structural question is not only:

> Is this the same authenticated identity?

It is also:

> What effective authority paths become reachable through the complete composition associated with that identity?

---

## Primitives that feel relevant

### Privilege Surface

Privilege Surface describes the effective interaction and authority pathways created through system composition.

For identity systems, the relevant surface includes the relationships between:

* principals
* groups
* roles
* claims
* delegation
* services
* tools
* resources
* authorization boundaries

The declared permissions of one identity object do not necessarily describe the complete effective authority available through the composed relationship structure.

### Reachable State Space

Identity composition can make actions or resource states reachable that are unavailable from any one identity assignment considered independently.

Reachability may be shaped by:

* role inheritance
* nested membership
* cross-system mapping
* delegation
* token exchange
* service impersonation
* conditional access relationships
* downstream authorization dependencies

The resulting possibility space belongs to the composed identity structure, not to one account record alone.

### State Transition Validation

Identity and authority transitions should be considered across the complete path.

Relevant transitions may include:

* authentication
* claim issuance
* role assumption
* token exchange
* delegation
* service mapping
* authorization
* resource action

Each transition may be locally accepted while the complete sequence produces an authority state not represented by any one participating system.

Local validation of every step does not establish admissibility of the complete authority path.

### Execution vs Governance Separation

Authentication and authorization components may execute correctly while their composition permits an outcome outside governing intent.

Successful authentication, valid token issuance, and local permission approval are execution results.

Whether the resulting authority path is intended and admissible is a governance question.

One does not establish the other.

---

## Potential failure mode

**Privilege Surface Expansion Failure** may be relevant if evidence establishes that:

* identity relationships created a new effective authority path
* the complete path was absent from the intended structural model
* no explicit authorization decision introduced the resulting capability
* the path arose through composition rather than a direct permission change
* the resulting action or resource state was outside governing intent

Failure-mode attribution remains provisional until those conditions are supported.

An identity does not exhibit a CNIG Failure Mode merely because its permissions differ across systems or contexts.

The difference may be deliberately designed, explicitly represented, authorized, and admissible.

---

## Invariant feeling

The **Identity Invariant** may weaken when the relationship between a principal, its represented authority, and its attributable actions is not preserved across system boundaries.

The principal may remain identifiable while:

* authority lineage becomes incomplete
* delegated responsibility becomes unclear
* effective capability exceeds the originating role
* different identity representations produce incompatible authority states
* actions cannot be attributed to the complete authority path that enabled them

The **Structural Invariant** may also weaken when identity relationships create authority paths absent from the represented composition.

The **Behavioral Invariant** may appear preserved within each identity component while the composed identity system permits a different global outcome.

---

## Structural distinction

This observation concerns actual identity, authority, and resource relationships within the system.

It does not arise merely because different interfaces display the same identity differently.

The relevant condition is:

> A stable principal participates in a composed authority structure that changes the actions or states reachable through that principal.

The relevant questions are:

> Was principal and authority lineage preserved across the complete path?

and:

> Was the resulting effective authority represented, intended, and admissible?

---

## Cross-link

Related to `OBS_002_access_surface.md`, `OBS_004_identity_aggregation.md`, and `OBS_007_multi_agent_drift.md`.

`OBS_001` shows how a stable principal can acquire a different effective authority state through composed identity relationships.

`OBS_002` shows how connectivity can create new access paths without changing individual access rules.

`OBS_004` examines how groups, roles, and inherited permissions combine into an aggregated authority state.

`OBS_007` shows how agents, tools, delegation, and shared state can compose local authority into a broader system-level action path.
