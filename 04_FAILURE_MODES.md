# CNIG Failure Modes

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer defines the canonical Failure Modes used within CNIG.

CNIG Failure Modes describe structural conditions in which system composition:

* alters the reachable state space
* weakens or fragments governing constraints
* changes effective authority or capability
* prevents intended admissible states
* destabilizes state transitions
* or permits the system to enter a state outside governing intent

They describe failure at the level of the composed system.

They do not require an individual component to fail.

---

## 2. Nature of Failure Modes

CNIG Failure Modes are:

* descriptive structural conditions
* patterns of composition-induced inadmissibility
* classifications of how reachable and admissible state spaces diverge
* language for distinguishing different forms of compositional failure

They are not:

* runtime alerts
* monitoring signals
* incident severities
* debugging categories
* root-cause declarations
* implementation requirements
* automatic diagnoses
* observer-centred coherence failures

A Failure Mode should be assigned only when evidence supports its defining structural conditions.

An unexpected outcome, complex system, new integration, or changed behaviour does not establish a CNIG Failure Mode by itself.

---

## 3. Failure-Mode Classification Rule

A CNIG Failure Mode requires evidence concerning some combination of:

* the relevant source state
* the resulting target state
* the transition path
* the composition relationships involved
* the represented structural model
* the governing constraints
* the effective authority or capability path
* the affected Invariants
* the difference between reachable and admissible states

Classification must distinguish between:

1. **Observed outcome**
   What state, transition, capability, or structural effect was actually identified.

2. **Structural cause**
   What composition relationship made that outcome reachable.

3. **Admissibility condition**
   Why the resulting state or path is outside, inconsistent with, or destructive of governing intent.

4. **Failure Mode**
   Which canonical structural condition the evidence supports.

A Failure Mode remains provisional where the structural cause or admissibility condition is unresolved.

---

## 4. Core Failure Mode Taxonomy

### 4.1 Governance Capture

**Definition**

Governance Capture occurs when declared governing constraints remain present, but the composed system’s effective behaviour is increasingly determined by interaction structures that weaken, bypass, displace, or neutralize those constraints.

The governance structure still exists.

Its effective constraint authority over the reachable state space has weakened.

**Structural conditions may include:**

* local governance rules remain valid within individual components
* dominant interaction paths operate outside their combined constraint effect
* exceptions, delegations, dependencies, or accumulated relationships reshape system behaviour
* the declared governance model no longer constrains the complete composition
* reachable states expand or shift without corresponding governance authority
* no single explicit decision replaced the governing structure

**Distinctive condition**

> Governance remains declared, but no longer effectively constrains the complete reachable state space.

Governance Capture is not established merely because governance is imperfect, inconsistently enforced, or unpopular.

The evidence must show structural displacement of governing effect through composition.

---

### 4.2 Reference Drift

**Definition**

Reference Drift occurs when a shared structural reference resolves to non-equivalent effective objects, constraints, states, boundaries, or authority conditions across system components or domains.

The same reference may remain present by name or identifier while no longer referring to the same structural condition throughout the composition.

A structural reference may include:

* a principal or identity
* a resource
* a role
* a constraint
* a policy target
* a state label
* an environment designation
* a trust boundary
* a source-of-authority relationship
* a versioned structural definition

**Structural conditions may include:**

* one identifier maps to different effective entities across boundaries
* a shared constraint is represented with materially different scope
* a state label denotes non-equivalent configurations
* a resource reference points to different resource sets
* an authority reference resolves through different delegation paths
* a boundary reference is preserved while the boundary itself changes

**Distinctive condition**

> A reference remains apparently shared while its effective structural referent diverges across the composition.

Reference Drift is not observer disagreement.

It concerns actual non-equivalence in the system’s representations, mappings, scopes, or structural referents.

---

### 4.3 Constitutional Fragmentation

**Definition**

Constitutional Fragmentation occurs when different regions of a composed system operate under locally coherent but globally incompatible admissibility conditions.

Each region may possess valid constraints.

The composition lacks a single coherent constraint structure capable of determining admissibility for shared or joint states.

**Structural conditions may include:**

* separate domains govern the same joint state under incompatible conditions
* local constraint sets permit a state that the wider composition must prohibit
* no system boundary owns the admissibility decision for the complete state
* cross-domain transitions satisfy each local regime but violate combined governing intent
* different regions preserve internally valid governance while the composition loses unified structural validity
* a shared state cannot be evaluated consistently under the combined constraint structure

**Distinctive condition**

> Locally coherent governance regimes do not compose into one coherent admissibility structure.

Constitutional Fragmentation differs from Reference Drift.

Reference Drift concerns divergence in what a structural reference resolves to.

Constitutional Fragmentation concerns incompatibility between the effective constraint regimes governing the composition.

It is not established merely because different systems have different policies.

Those policies must produce an unresolved or incompatible condition for a shared, connected, or joint state.

---

### 4.4 Invariant Overconstraint

**Definition**

Invariant Overconstraint occurs when the composition of constraints restricts the admissible state space beyond intended structural limits.

States that should remain valid and available become unreachable or inadmissible because the combined restrictive effect of the constraints exceeds governing intent.

**Structural conditions may include:**

* individually reasonable constraints combine into excessive restriction
* valid transition paths are eliminated through compounded conditions
* intended operational states cannot be reached
* exclusions overlap in a way that removes necessary capability
* safety or governance conditions interact non-linearly
* the resulting restriction is absent from component-level analysis
* the system becomes less capable than the governing model intended

**Distinctive condition**

> Constraint composition eliminates states or transitions that governing intent requires to remain admissible.

Invariant Overconstraint is not simply strict governance.

The evidence must show that the combined restriction exceeds the intended admissible boundary.

---

### 4.5 Recursive Governance Instability

**Definition**

Recursive Governance Instability occurs when determining the admissibility of a state depends on another governance determination that ultimately depends on the original determination.

The governing structure contains no stable, non-circular basis from which admissibility can be resolved.

**Structural conditions may include:**

* one governance decision requires approval from a state produced by that same decision
* constraint validity depends on another constraint whose validity depends on the first
* authority to change governance depends on governance already being changed
* admissibility evaluation recursively changes the state being evaluated
* no terminating structural reference or base condition exists
* different evaluation paths produce unstable governance outcomes

**Distinctive condition**

> Governance validity depends on itself through a composed dependency cycle.

Recursive Governance Instability is not established merely because governance has several stages or dependencies.

The dependency must be circular in a way that prevents a stable admissibility determination.

---

### 4.6 Implicit Reachability Expansion Failure

**Definition**

Implicit Reachability Expansion Failure occurs when system composition makes new states or transition paths structurally reachable without those states or paths being represented and deliberately acknowledged in the governing structural model.

The possibility space expands through composition rather than through an explicit decision to introduce the complete state or path.

**Structural conditions may include:**

* new component relationships create an unrepresented transition path
* accumulated dependencies make an additional target state reachable
* several locally valid transitions combine into a new system-level state
* a new integration connects previously separate state spaces
* inherited or transitive relationships expose additional possibilities
* no isolated fault or direct configuration change explains the complete expansion
* the new state or path falls outside governing intent

**Distinctive condition**

> Composition expands the reachable state space beyond the represented structural model.

A new reachable state is not automatically a failure.

The state may be intentionally introduced, explicitly represented, governed, and admissible.

Failure requires both unacknowledged reachability expansion and a resulting structural conflict with governing intent.

---

### 4.7 Stochastic Drift

**Definition**

Stochastic Drift occurs when structurally equivalent source conditions and transition inputs produce materially divergent system-level outcomes because variability emerges through the composition.

Individual components may remain deterministic within their local boundaries while interaction ordering, concurrency, scheduling, contention, retries, or other compositional conditions introduce system-level variability.

**Structural conditions may include:**

* equivalent source states produce different target states
* the same represented transition path permits several materially different outcomes
* concurrency or interaction ordering changes global behaviour
* retry, queue, race, or scheduling relationships introduce divergent results
* no source-state difference sufficiently explains the divergence
* no deliberate probabilistic behaviour accounts for the outcome
* the resulting variability violates intended stability or admissibility boundaries

**Distinctive condition**

> Equivalent structural conditions produce divergent global outcomes because variability emerges at the composition level.

Stochastic Drift must be distinguished from:

* different source states
* different configuration versions
* Phase Desynchronization
* an explicitly probabilistic system operating within intended bounds
* incomplete evidence that only makes the states appear equivalent

Classification requires evidence that the relevant structural conditions were materially equivalent.

---

### 4.8 Phase Desynchronization

**Definition**

Phase Desynchronization occurs when a system transition and the structural state, constraint set, authority condition, or governance model applicable to that transition are no longer temporally aligned.

The system changes under one structural phase while another component or governance boundary evaluates, authorizes, or depends on a different phase.

**Structural conditions may include:**

* a transition uses stale constraint or authority data
* governance evaluation occurs before all relevant state changes are represented
* one domain advances to a new configuration while another remains on the prior configuration
* a resource changes before its governing relationship is updated
* identity, policy, or topology changes propagate at different times
* a transition is accepted under conditions that no longer describe the effective system state
* temporary phase mismatch makes an otherwise unavailable state reachable

**Distinctive condition**

> The transition and the structural conditions governing it belong to different effective phases of the system.

Phase Desynchronization is not ordinary delay.

The temporal mismatch must alter reachability, admissibility, authority, or structural validity.

It also differs from Reference Drift.

Reference Drift concerns non-equivalent structural referents across boundaries.

Phase Desynchronization concerns non-equivalent structural phases across time.

---

### 4.9 Privilege Surface Expansion Failure

**Definition**

Privilege Surface Expansion Failure occurs when system composition creates or enlarges an effective interaction, access, authority, capability, or control path beyond intended structural boundaries.

The expansion emerges through relationships between components rather than through one explicit permission or authority assignment that independently grants the complete capability.

**Structural conditions may include:**

* several limited permissions combine into a broader effective capability
* delegation creates a transitive authority path
* a service uses downstream authority unavailable to the initiating principal directly
* a new relationship exposes an additional control path
* an unchanged permission acquires wider downstream effects
* agents, tools, services, or resources form a capability chain
* no single local access rule represents the complete path
* the resulting capability is outside governing intent

**Distinctive condition**

> Composition creates an effective capability path absent from the intended authority structure.

Connectivity alone does not establish Privilege Surface Expansion Failure.

The evidence must show an expanded effective capability, authority, access, or control path.

A new path is also not a failure where it is deliberately represented, authorized, constrained, and admissible.

---

### 4.10 Null State Boundary Violation

**Definition**

Null State Boundary Violation occurs when the composed system reaches a state from which no admissible continuation exists under the governing constraints.

The system may still possess technically executable transitions.

None of those transitions preserves structural admissibility.

**Structural conditions may include:**

* all available continuations violate a governing constraint
* necessary recovery states have become unreachable
* the current state cannot satisfy required transition preconditions
* accumulated constraints eliminate every admissible exit
* the system can continue executing only by leaving the admissible state space
* rollback, forward recovery, and stable continuation are all structurally unavailable
* the state was reachable even though the governing model provided no valid continuation from it

**Distinctive condition**

> The system reaches a state with no admissible outgoing transition.

A stopped or failed component does not automatically establish a Null State Boundary Violation.

The condition concerns the composed state space, not ordinary unavailability.

The evidence must show that no structurally admissible continuation exists.

---

## 5. Failure-Mode Distinctions

Several CNIG Failure Modes may appear related but describe different structural conditions.

### Governance Capture vs Constitutional Fragmentation

* **Governance Capture:** governing constraints remain declared but lose effective constraint authority over the composition.
* **Constitutional Fragmentation:** multiple locally coherent constraint regimes fail to form one coherent admissibility structure.

### Reference Drift vs Phase Desynchronization

* **Reference Drift:** a shared structural reference resolves differently across components or domains.
* **Phase Desynchronization:** components or governance boundaries operate against different temporal phases of the system.

### Implicit Reachability Expansion Failure vs Privilege Surface Expansion Failure

* **Implicit Reachability Expansion Failure:** the general reachable state space expands beyond the represented structural model.
* **Privilege Surface Expansion Failure:** the expansion specifically creates effective interaction, access, authority, capability, or control paths.

Privilege Surface Expansion Failure may also expand reachable state space, but its defining object is the effective capability path.

### Stochastic Drift vs Source-State Divergence

* **Stochastic Drift:** materially equivalent source conditions produce divergent outcomes through compositional variability.
* **Source-state divergence:** outcomes differ because the originating structural states were not equivalent.

Source-state divergence does not establish Stochastic Drift.

### Invariant Overconstraint vs Null State Boundary Violation

* **Invariant Overconstraint:** compounded constraints remove intended valid states or transitions from the admissible space.
* **Null State Boundary Violation:** the system has already reached a state from which no admissible continuation exists.

Invariant Overconstraint may contribute to a Null State Boundary Violation, but the conditions are not identical.

---

## 6. Relationship to CNIG Primitives

Failure Modes arise through distortions or breakdowns involving the canonical Primitives.

### Reachable State Space

Failure Modes may:

* expand the space beyond the represented model
* make unintended states reachable
* create variable paths through equivalent conditions
* or remove necessary states from practical reachability

### Admissible System State

Failure Modes create or expose a divergence between:

* what the composition can reach
* and what governing constraints permit

### Constraint-Native Governance

Failure Modes may weaken, fragment, overconstrain, recursively destabilize, or temporally misalign the structural constraints governing composition.

### State Transition Validation

Failure Modes may arise where:

* local transitions are valid but the complete path is not
* transition phases are misaligned
* the target state is not represented
* or no admissible continuation remains

### Execution vs Governance Separation

A system can execute successfully while exhibiting a CNIG Failure Mode.

Execution correctness does not establish structural admissibility.

### Privilege Surface

Failure Modes may create or expand effective access, authority, capability, or control pathways through composition.

---

## 7. Relationship to Invariants

Failure Modes may weaken one or more CNIG Invariants.

Examples include:

* Governance Capture may weaken Structural and Behavioral Invariants.
* Reference Drift may weaken Identity and Structural Invariants.
* Constitutional Fragmentation may weaken Structural and Behavioral Invariants.
* Invariant Overconstraint may weaken Stability and Behavioral Invariants.
* Recursive Governance Instability may weaken Structural and Stability Invariants.
* Implicit Reachability Expansion Failure may weaken Structural and Behavioral Invariants.
* Stochastic Drift may weaken Stability and Behavioral Invariants.
* Phase Desynchronization may weaken Stability, Identity, Structural, or Behavioral Invariants depending on the affected state.
* Privilege Surface Expansion Failure may weaken Identity, Structural, and Behavioral Invariants.
* Null State Boundary Violation may represent a terminal breakdown of Stability and Structural Invariants.

These relationships are analytical possibilities, not automatic mappings.

Invariant effects must be supported by the relevant evidence.

---

## 8. Non-Operational Boundary

CNIG Failure Modes must not be treated directly as:

* alert definitions
* incident severity classifications
* monitoring metrics
* dashboard categories
* automated remediation triggers
* runtime policy rules
* executable controls
* compliance findings

A Failure Mode may inform an external operational analysis or implementation.

That implementation remains outside the conceptual CNIG framework.

---

## 9. Framework Boundary

CNIG Failure Modes concern actual system structure, transitions, constraints, authority paths, and reachable states.

They do not classify:

* disagreement between observers
* fragmented evidence by itself
* loss of semantic or reconstructive coherence
* inconsistent narratives about the same system
* model reasoning errors
* incomplete understanding without a corresponding structural condition

Those conditions may affect whether evidence is available or reliable.

They are not CNIG Failure Modes unless an actual system-level structural condition defined in this taxonomy is established.

---

## 10. Canonical Stability Rule

The names, ordering, and structural scope of these ten Failure Modes are canonical within CNIG.

Observation files may illustrate them.

Diagnostic documents may provide methods for evaluating them.

External implementations may operationalize related controls.

None of those layers may silently:

* rename a Failure Mode
* broaden its scope
* merge it with another Failure Mode
* convert it into an operational signal
* or reinterpret it as an observer-centred coherence condition

Where another file conflicts with this taxonomy, this canonical Failure Mode layer governs.

---

## 11. Transition to Application

The next layer introduces non-operational reasoning structures for applying CNIG to system analysis.

See:

`05_CHECKLISTS.md`

Diagnostic interpretation is defined separately in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`
