# Observation 007 — Each agent stayed within its local boundary. The system crossed a global boundary.

A multi-agent system contained several agents with separate responsibilities.

Each agent had its own:

* assigned role
* permitted tools
* accepted inputs
* local decision boundary
* action permissions
* completion conditions
* downstream recipients

Each agent operated as configured.

Each:

* accepted a locally valid task
* used only its assigned tools
* performed a permitted action
* returned the expected status
* satisfied its local completion conditions

No individual agent showed evidence of unauthorized execution or component failure.

---

But the combined agent sequence reached a system state that no individual agent had been assigned, authorized, or evaluated to produce in full.

One agent created an output or state change.

Another agent accepted that result as a valid precondition.

A later agent used an independently permitted tool.

Additional agents continued the sequence through locally accepted transitions.

The final outcome emerged from the complete interaction path.

No single agent necessarily performed the complete action.

No single local rule necessarily described the complete result.

---

## What changed

The local capabilities of the agents did not necessarily change.

Their actions became connected.

Across the complete interaction path:

* one agent’s output became another agent’s input
* one action changed the preconditions available to another agent
* delegated tasks crossed local responsibility boundaries
* shared state carried effects between agents
* tool results enabled later actions
* locally permitted capabilities combined into a broader system capability
* intermediate transitions accumulated toward a final state

The interaction topology made a system-level action path available that was not visible from any individual agent boundary.

---

## CNIG lens (informal)

Local agent compliance does not establish global admissibility.

A multi-agent system must be evaluated as a composition of:

* agent roles
* authority boundaries
* tool relationships
* delegated tasks
* shared state
* intermediate transitions
* resulting system states

The relevant question is not only whether every agent followed its instructions.

It is:

> What complete action paths and system states became reachable when those agents, tools, and authority relationships were composed?

---

## Primitives that feel relevant

### Reachable State Space

Agent interaction can make system states reachable that no individual agent could produce independently.

The reachable state space is shaped by:

* which agents can communicate
* which outputs can trigger later actions
* which tools each agent can invoke
* how shared state changes
* how tasks can be delegated
* which intermediate states satisfy later preconditions

The system’s effective possibility space therefore depends on the complete agent interaction topology, not only on the capability of each agent in isolation.

### State Transition Validation

Each agent may validate only its own local action.

The complete transition path must also account for:

* the originating system state
* the initiating authority
* each delegated task
* every intermediate state
* tool-mediated side effects
* changes to shared resources
* downstream preconditions
* the final target state
* the constraints and invariants that must remain preserved

Local acceptance of every agent action does not establish validity of the complete multi-agent transition sequence.

### Execution vs Governance Separation

Each agent may execute correctly while the composed agent system produces a state outside governing intent.

Instruction compliance, tool success, and local task completion are execution properties.

Whether the resulting system state was authorized and admissible is a governance property.

One does not establish the other.

### Privilege Surface

Privilege Surface is relevant where the composition of agents, tools, delegation paths, and shared resources creates an effective capability or authority path that was not available to any agent independently.

Communication between agents does not, by itself, establish Privilege Surface expansion.

The structural evidence must show that the composed relationships enable:

* an action
* access path
* authority path
* control path
* or effective capability

that was not represented within the intended authority structure.

---

## Potential failure modes

### Privilege Surface Expansion Failure

This Failure Mode may be relevant if evidence establishes that:

* agent and tool relationships created a new effective capability path
* no individual agent independently possessed the complete capability
* the composed authority path was absent from the intended structural model
* no explicit authorization decision introduced the complete path
* the resulting capability arose through composition rather than a direct permission change

### Implicit Reachability Expansion Failure

This Failure Mode may be relevant if:

* the multi-agent sequence made a previously unrepresented state reachable
* the state emerged through locally accepted transitions
* no individual agent explicitly introduced or governed the complete outcome
* the expansion was not deliberately acknowledged by the governing structure

Failure-mode attribution remains provisional until the relevant structural conditions are supported.

A multi-agent system does not exhibit a CNIG Failure Mode merely because several agents collaborate or produce a result no single agent could produce alone.

The resulting path may remain intended, represented, authorized, and admissible.

---

## Invariant feeling

The **Structural Invariant** may weaken when agent, tool, delegation, and shared-state relationships produce action paths outside the represented system structure.

The **Behavioral Invariant** may appear preserved within every agent while the composed system produces a global outcome outside the expected behavioural boundary.

The **Identity Invariant** may become relevant where initiating authority, delegated authority, or responsibility for an action is not preserved across the complete agent sequence.

The **Stability Invariant** may be affected when small changes in agent ordering, delegation, tool availability, or shared state produce disproportionately different system outcomes.

---

## Structural distinction

This observation is not about:

* whether an agent reasoned well
* whether generated content was correct
* whether observers interpreted agent outputs differently
* whether system understanding became fragmented
* whether reconstructive coherence weakened

It concerns the actual structural consequences of composing agents, tools, authority relationships, and state transitions.

The relevant condition is:

> Locally permitted agent actions compose into a system-level path or state that no local boundary represented in full.

The relevant questions are:

> What complete action path did the agent composition make reachable?

and:

> Was the resulting state represented, authorized, and admissible?

---

## Cross-link

Related to `OBS_005_service_coupling_drift.md`, `OBS_002_access_surface.md`, and `OBS_011_governance_constraint_displacement.md`.

`OBS_005` shows how changed relationships between correct services can alter the transition paths available to a distributed system.

`OBS_007` shows how agent, tool, delegation, and shared-state relationships can compose locally permitted actions into a broader system-level action path.

`OBS_002` shows how connectivity can create effective access paths without changing individual access rules.

`OBS_011` shows how declared governance may remain locally present while failing to constrain the complete reachable state space created through composition.
