# Observation 005 — Services remained correct. Interaction topology changed.

A distributed system contained multiple independently operated services.

Each service:

* passed its health checks
* respected its declared interface
* returned valid responses
* processed locally valid inputs
* remained within its expected operating conditions

No individual service showed evidence of failure.

---

But as the system expanded, its global behaviour changed.

Additional:

* service dependencies
* event subscriptions
* retry paths
* queue relationships
* replicas
* orchestration paths
* shared state interactions
* indirect call sequences

changed how the services could affect one another.

The services remained locally correct.

The interaction topology connecting them did not remain the same.

---

## What changed

The internal logic of each service did not necessarily change.

The number, direction, ordering, and recurrence of interactions changed.

A service output could now:

* trigger additional services
* return through an indirect dependency path
* participate in a feedback loop
* alter shared state used by another service
* be retried through a different route
* influence a later transition that the originating service did not represent

These relationships created system-level consequences not visible from any one service boundary.

---

## CNIG lens (informal)

Component correctness does not establish stability of the composition in which those components operate.

When interaction topology changes, the reachable state space of the composed system may also change.

The relevant structural question is not only whether every service behaves correctly.

It is:

> What states become reachable through the complete set of relationships between those services?

---

## Primitives that feel relevant

### Reachable State Space

Changes in service relationships can introduce new paths through the system.

Those paths may make new intermediate or final states reachable even when no service changes its own implementation.

Reachability therefore depends on the interaction topology of the composition, not only on the capabilities of individual services.

### State Transition Validation

A service may validate its own local transition without representing the cumulative transition path created across several services.

Evaluation of the composed system includes:

* the originating state
* the sequence of service interactions
* indirect dependencies
* feedback paths
* shared-state effects
* the resulting target state
* the constraints and invariants that must remain preserved

Local acceptance by each service does not establish validity of the complete system-level transition.

### Execution vs Governance Separation

Every service may execute correctly while their interaction structure permits a result outside governing intent.

Service health and interface correctness are execution properties.

The admissibility of the resulting system state is a governance property.

One does not establish the other.

### Privilege Surface

Privilege Surface is relevant only where new service relationships create or expand effective capability, access, authority, or control pathways.

Generic service coupling does not, by itself, establish Privilege Surface expansion.

The structural evidence must show that the changed topology enables an interaction or capability that was not previously available through the declared authority structure.

---

## Potential failure mode

**Implicit Reachability Expansion Failure** may be relevant if evidence establishes that:

* changed service relationships introduced a new system path
* the path made a previously unrepresented state reachable
* the state was not deliberately introduced into the governing model
* no isolated service fault or ordinary misconfiguration explains the outcome
* the expansion arose from composition rather than from a single service capability

Failure-mode attribution remains provisional until those conditions are supported.

If the changed topology produces only intended and admissible states, the observation does not establish a CNIG Failure Mode merely because the system has become more interconnected.

---

## Invariant feeling

The **Structural Invariant** may weaken when the relationships between services no longer preserve the boundaries or effects represented in the original composition.

The **Behavioral Invariant** may appear preserved within each service while the composed system produces different global behaviour through new interaction paths.

The **Stability Invariant** may be affected when small changes in service relationships, ordering, retries, or shared-state dependencies produce disproportionately different system outcomes.

---

## Structural distinction

This observation is not about observers reconstructing different accounts of the same distributed system.

It concerns an actual change in the system’s interaction topology.

It is also not evidence that service coupling is inherently inadmissible.

The relevant condition is:

> Locally correct services become connected through relationships that alter the states or transition paths available to the composed system.

The relevant question is:

> What did the changed interaction topology make reachable, and did those states remain admissible?

---

## Cross-link

Related to `OBS_007_multi_agent_drift.md` and `OBS_009_silent_drift.md`.

`OBS_005` shows how changed relationships between correct services can alter the transition paths and states available to a distributed system.

`OBS_007` examines the corresponding problem where autonomous agents interact and create system-level behaviour not contained in any one agent’s local specification.

`OBS_009` shows how accumulated structural relationships can gradually alter the reachable state space without a single identifiable component failure.
