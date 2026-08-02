# Observation 004 — Every assignment was valid. Aggregation produced an unrepresented authority state.

An identity system contained users, groups, roles, policies, and inherited permissions.

Each individual assignment was valid.

The:

* user accounts
* direct group memberships
* nested group memberships
* role assignments
* policy attachments
* inheritance relationships
* resource permissions
* conditional rules

were each correctly configured within their local boundaries.

No individual assignment exceeded its declared scope.

No identity object showed evidence of corruption, unauthorized modification, or component failure.

---

But when the complete identity structure was evaluated, the principal acquired an effective authority state that no individual assignment represented independently.

A direct group activated a nested group.

The nested group activated a role.

The role inherited another permission set.

A policy condition enabled access to an additional resource.

Each relationship was locally valid.

Their aggregation produced the complete authority state.

The resulting capability was not visible in any one assignment considered alone.

---

## What changed

The principal did not necessarily change.

The individual assignments did not necessarily change.

What changed was the authority produced by their aggregation.

Across the complete identity structure:

* direct permissions combined with inherited permissions
* nested membership extended role reach
* role relationships activated downstream policies
* resource-specific grants combined with broader assignments
* conditional rules changed which permissions became effective
* several limited assignments formed a broader authority path
* revocation or exclusion at one layer did not necessarily remove authority available through another path

The effective authority state was a structural result of the complete aggregation graph.

It could not be determined from one user, group, role, or policy record alone.

---

## CNIG lens (informal)

Declared identity assignments are local facts.

Effective authority is a compositional property.

A set of individually valid assignments may combine into an authority state that is broader, different, or less constrained than any assignment expresses independently.

The relevant question is not only:

> Is every identity assignment valid?

It is also:

> What complete authority state is produced when all membership, inheritance, policy, and resource relationships are aggregated?

---

## Primitives that feel relevant

### Privilege Surface

Privilege Surface describes the effective interaction and authority pathways created through composition.

Within an aggregated identity structure, the relevant surface includes:

* direct membership paths
* nested membership paths
* inherited roles
* policy relationships
* conditional grants
* delegation
* resource mappings
* alternative authorization paths

The declared scope of one assignment does not necessarily describe the complete capability available through the aggregated structure.

A permission removed from one path may remain reachable through another.

A limited role may combine with another assignment to enable a broader action.

Privilege must therefore be evaluated across the full relationship topology.

### Reachable State Space

Identity aggregation determines which actions and resource states become reachable through a principal.

The reachable state space may expand through:

* nested membership
* role inheritance
* overlapping assignments
* policy composition
* alternative authorization paths
* conditional activation
* cross-resource relationships

The resulting authority state belongs to the complete identity composition, not to any one assignment independently.

### Admissible System State

An effective authority state is not admissible merely because every contributing assignment is valid.

The aggregated result must remain consistent with:

* intended authority boundaries
* separation requirements
* exclusion constraints
* delegation limits
* resource boundaries
* governing intent

Local validity of the contributing assignments does not establish admissibility of the resulting authority state.

### Execution vs Governance Separation

The identity platform may correctly calculate and enforce every configured assignment.

That is execution correctness.

Whether the resulting aggregated authority state was intended and admissible is a governance question.

A system can enforce every rule correctly while the composition of those rules permits an unintended capability.

---

## Potential failure mode

**Privilege Surface Expansion Failure** may be relevant if evidence establishes that:

* valid identity relationships combined into a new effective authority path
* the complete path was absent from the intended structural model
* no explicit authorization decision introduced the resulting capability
* the capability arose through aggregation rather than a direct permission change
* the resulting action or resource state was outside governing intent

Failure-mode attribution remains provisional until those conditions are supported.

Aggregation does not constitute a CNIG Failure Mode merely because the effective authority exceeds one individual assignment.

The complete result may be deliberately designed, explicitly represented, authorized, and admissible.

---

## Invariant feeling

The **Identity Invariant** may weaken when the relationship between a principal, its declared assignments, and its effective authority is not preserved across the aggregation structure.

The principal may remain stable while:

* its authority lineage becomes incomplete
* effective capability cannot be traced to one represented path
* exclusion at one layer is bypassed by another valid path
* inherited authority exceeds the intended role boundary
* equivalent principals acquire materially different authority through structural position

The **Structural Invariant** may weaken when the aggregation graph produces authority relationships absent from the represented identity design.

The **Behavioral Invariant** may appear preserved within every identity component while the complete identity system permits a different global outcome.

---

## Structural distinction

This observation is not about different interfaces displaying different descriptions of the same identity.

It concerns the actual authority produced when identity relationships are aggregated.

It is distinct from the broader cross-system condition in `OBS_001_identity_surface.md`.

The relevant condition here is:

> Individually valid identity assignments combine into an effective authority state that no assignment represents independently.

The relevant questions are:

> What authority does the complete aggregation graph produce?

and:

> Is that resulting authority state represented, intended, and admissible?

---

## Cross-link

Related to `OBS_001_identity_surface.md`, `OBS_002_access_surface.md`, and `OBS_007_multi_agent_drift.md`.

`OBS_001` shows how a stable principal can acquire a different effective authority state across composed identity and infrastructure systems.

`OBS_004` shows how valid groups, roles, policies, and inherited permissions combine into an aggregated authority state within an identity structure.

`OBS_002` shows how connectivity can create effective access paths without changing individual access rules.

`OBS_007` shows how local agent and tool permissions can compose into a broader system-level action path.
