# Observation 002 — No permission changed. A new effective access path emerged.

A composed system contained several services, identity boundaries, and protected resources.

Each component had valid access controls.

The:

* user permissions
* service permissions
* network rules
* application roles
* API authorizations
* resource policies
* trust relationships
* delegation boundaries

were each correct within their local scope.

No individual rule explicitly granted the complete access path.

No direct permission change occurred.

---

But after systems were connected, a principal or service could affect a resource that it could not reach through any one declared relationship independently.

One component accepted the initiating identity or request.

Another component possessed authority over a downstream service.

That service could act on an additional resource.

Each interaction was locally permitted.

Together, the relationships formed an effective access path across several system boundaries.

Access did not expand within one rule.

It expanded through the composition of paths.

---

## What changed

The individual permissions did not necessarily change.

The relationship topology did.

Across the complete composition:

* one authenticated session became valid input to another service
* one service acted with its own downstream authority
* one trusted system accepted assertions from another
* a permitted API call triggered a more privileged internal action
* delegated access crossed a resource boundary
* an intermediary transformed or relayed an authorized request
* multiple limited capabilities combined into a broader effective capability
* an alternative path bypassed the boundary represented by the direct access model

The complete path enabled an action or resource effect not represented by any one permission record.

---

## CNIG lens (informal)

Declared permissions describe local authorization decisions.

They do not necessarily describe every effective path created when systems, services, identities, and resources are connected.

The relevant structural question is not only:

> What does each component permit directly?

It is also:

> What actions and resource states become reachable through the complete chain of permitted relationships?

---

## Primitives that feel relevant

### Privilege Surface

Privilege Surface describes the emergent interaction topology created through system composition.

In an access context, the surface includes paths between:

* principals
* identities
* services
* APIs
* delegation relationships
* trust boundaries
* tools
* protected resources
* control mechanisms

A Privilege Surface exists where the composed relationships enable effective access, authority, capability, or control.

Connectivity alone does not establish Privilege Surface expansion.

The structural evidence must show that the connection enables an action or resource effect that was unavailable through the previously represented authority structure.

### Reachable State Space

A new access path can make additional actions or resource states reachable.

The resulting reachability may depend on:

* transitive service calls
* delegated authority
* trust inheritance
* identity mapping
* request forwarding
* downstream service permissions
* shared credentials or tokens
* alternate authorization paths

The reachable state belongs to the complete composition, not to any one access rule independently.

### State Transition Validation

Each component may validate only its local part of an access sequence.

The complete path may include:

* authentication
* identity mapping
* token or claim acceptance
* delegation
* service invocation
* downstream authorization
* resource modification

Every transition may be locally accepted while the complete sequence produces an authority path or target state absent from the represented access model.

Local authorization of every step does not establish admissibility of the complete access path.

### Execution vs Governance Separation

Every authentication, authorization, and service component may execute correctly.

That is execution correctness.

Whether their composition creates an intended and admissible access path is a governance question.

A system can enforce every local access rule correctly while permitting a global action that no individual rule appears to grant.

---

## Potential failure mode

**Privilege Surface Expansion Failure** may be relevant if evidence establishes that:

* system composition created a new effective access or capability path
* the complete path was absent from the intended structural model
* no direct permission or authorization decision introduced it
* the path arose through several locally permitted relationships
* the resulting action or resource state was outside governing intent

Failure-mode attribution remains provisional until those conditions are supported.

A new connection does not constitute a CNIG Failure Mode merely because it creates another route between components.

The path may be explicitly represented, deliberately authorized, appropriately constrained, and admissible.

---

## Invariant feeling

The **Structural Invariant** may weaken when relationships between identity, service, and resource boundaries create access paths absent from the represented system structure.

The **Behavioral Invariant** may appear preserved within every authorization component while the composed system permits a different global action.

The **Identity Invariant** may become relevant where the identity or authority attributed to the initiating principal is not preserved across delegation, mapping, or service-mediated execution.

The principal may initiate the path, while the resulting action is performed under authority that the original access model did not associate with that principal.

---

## Structural distinction

This observation is not about:

* network connectivity by itself
* a direct permission misconfiguration
* an unauthorized component action
* different observers interpreting the same access policy differently

It concerns an actual effective path created through the composition of locally permitted relationships.

It is distinct from identity aggregation.

The relevant condition is:

> No individual rule grants the complete capability, but the composed system relationships make the capability reachable.

The relevant questions are:

> What complete access path did the composition create?

and:

> Was that path represented, authorized, constrained, and admissible?

---

## Cross-link

Related to `OBS_001_identity_surface.md`, `OBS_004_identity_aggregation.md`, `OBS_005_service_coupling_drift.md`, and `OBS_007_multi_agent_drift.md`.

`OBS_001` shows how a stable principal can acquire a different effective authority state across composed identity and infrastructure systems.

`OBS_002` shows how locally permitted relationships can compose into a new effective access or capability path without a direct permission change.

`OBS_004` shows how groups, roles, policies, and inherited permissions combine into an aggregated authority state within an identity structure.

`OBS_005` shows how changed service relationships alter the transition paths available to a distributed system.

`OBS_007` shows how agents, tools, delegation, and shared state can compose local permissions into a broader system-level action path.
