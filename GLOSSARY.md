# CNIG Glossary

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose

This glossary defines the canonical vocabulary used within Constraint-Native Infrastructure Governance.

Terms are organized into:

* framework terms
* canonical Primitives
* canonical Invariants
* canonical Failure Modes
* descriptive architecture patterns
* diagnostic-status terms

These definitions describe system structure, reachability, admissibility, authority, transitions, and compositional behaviour.

They are not:

* implementation requirements
* runtime objects
* enforcement controls
* monitoring signals
* incident labels
* observer-centred coherence concepts

Where another repository file uses a term inconsistently with this glossary, the relevant canonical framework layer governs:

* `02_CONCEPTUAL_CORE.md` for framework definition
* `03_PRIMITIVES.md` for Primitives
* `04_FAILURE_MODES.md` for Failure Modes
* this glossary for canonical terminology and Invariants

---

# Framework Terms

## Constraint-Native Infrastructure Governance

**Constraint-Native Infrastructure Governance (CNIG)** is a conceptual framework for reasoning about admissible system states within reachable state space under composition constraints prior to execution.

CNIG examines how the structure of a composed system determines:

* what states become reachable
* which reachable states remain admissible
* how locally valid transitions combine
* how authority and capability paths emerge
* whether governing constraints remain effective across composition

Its primary object of analysis is the composed system and the states made structurally reachable through component relationships.

CNIG is not itself a methodology.

A methodology may be used to apply CNIG, but the framework remains a bounded conceptual ontology.

---

## Component-Correct, Composition-Inadmissible System

A system in which:

* individual components satisfy their local specifications
* local configurations, permissions, transitions, or policies may be valid
* no single component fault explains the outcome
* but component composition makes a globally unintended or inadmissible state reachable

This is the distinctive problem class addressed by CNIG.

Component correctness does not establish compositional admissibility.

---

## Composition

The structural combination of multiple components, relationships, constraints, authority paths, and transitions into a system-level whole.

Composition includes more than physical or logical connection.

It may include:

* service interaction
* identity mapping
* role inheritance
* delegation
* shared state
* orchestration
* cross-domain integration
* workflow sequencing
* dependency relationships
* tool-mediated action
* policy interaction

Properties that hold for individual components do not automatically hold for their composition.

---

## Composition Constraint

A structural condition that shapes:

* how components can interact
* which transitions are available
* what authority or capability paths exist
* which target states can be reached
* which reachable states remain admissible

Composition Constraints operate at the level of system relationships and governing boundaries.

They are distinct from one component’s execution logic.

---

## Governing Constraint

An implicit or explicit condition that defines or limits intended system structure, authority, transition paths, or admissible states.

A Governing Constraint may concern:

* identity
* authority
* resource boundaries
* permitted relationships
* transition conditions
* exclusions
* separation requirements
* stability requirements
* target-state conditions

A constraint may remain declared while losing effective influence over the composed system.

---

## Governing Intent

The intended structural boundary within which the composed system is expected to operate.

Governing Intent includes the expected relationship between:

* components
* authority
* constraints
* transition paths
* reachable states
* admissible states
* intended capability
* prohibited outcomes

Governing Intent is not inferred solely from successful execution or the existence of local rules.

It must be supported by the relevant structural or authoritative evidence.

---

## Reachability

The property of a system state, action, capability, or transition path being accessible through the current composition.

Reachability describes structural possibility.

A state may be reachable through:

* direct transition
* accumulated transitions
* transitive relationships
* delegation
* inheritance
* integration
* changed interaction topology
* shared state
* downstream effects

Reachability does not determine admissibility.

---

## Admissibility

The property of a reachable system state or transition path remaining structurally coherent under the constraints governing the composition.

A state may be reachable without being admissible.

Admissibility depends on:

* governing constraints
* authority boundaries
* transition conditions
* invariant preservation
* intended system structure
* combined state relationships

Admissibility is not established merely by:

* successful execution
* local validation
* component health
* policy presence
* permission approval
* absence of an error

---

## Structural Model

The represented account of the system’s relevant:

* components
* relationships
* boundaries
* constraints
* authority paths
* source states
* transitions
* target states
* reachable states
* admissibility conditions

A Structural Model need not be executable or formally encoded.

A state or path may be structurally reachable while absent from the represented Structural Model.

---

## Source State

The system configuration from which a transition or transition sequence begins.

A Source State may include:

* component configuration
* identity and authority relationships
* dependency state
* shared resources
* active constraints
* version state
* topology
* temporal phase

Apparently equivalent executions may produce different outcomes where their Source States are not structurally equivalent.

---

## Intermediate State

A system state reached between the originating Source State and the final Target State.

Intermediate States may:

* alter later preconditions
* introduce authority
* change shared resources
* activate dependencies
* expand future reachability
* weaken constraints
* make later states possible

Local validation of individual Intermediate States does not establish admissibility of the complete transition path.

---

## Target State

The resulting system configuration reached through a transition or transition sequence.

A Target State may be:

* reachable and admissible
* reachable but inadmissible
* represented but not evaluated
* absent from the represented Structural Model

Execution success does not establish Target State admissibility.

---

## Joint State

A system state whose defining conditions depend on two or more separately governed systems or domains.

A Joint State cannot be fully described or evaluated from either local domain independently.

Each contributing local state may be admissible while the Joint State is not.

---

## Transition Path

The complete sequence of relationships and state changes connecting a Source State to a Target State.

A Transition Path may include:

* local actions
* service calls
* identity mappings
* delegated authority
* intermediate states
* tool execution
* shared-state changes
* cross-domain effects
* downstream transitions

The validity of every local step does not establish admissibility of the complete Transition Path.

---

## Interaction Topology

The structure of relationships through which system components can affect one another.

Interaction Topology includes:

* direction
* ordering
* recurrence
* dependency
* feedback
* delegation
* authority
* shared state
* invocation paths
* resource effects

Changes in Interaction Topology may change the Reachable State Space without modifying individual components.

---

## Effective Authority

The complete authority available to a principal, service, agent, or component through the composed relationship structure.

Effective Authority may differ from one declared assignment because it can include:

* inheritance
* nested membership
* delegation
* downstream service authority
* token exchange
* identity mapping
* alternative authorization paths
* tool relationships
* transitive capability

Effective Authority is a structural result of composition.

---

## Effective Capability

The complete action or system effect that can be produced through a principal, permission, service, tool, agent, or transition path.

Effective Capability includes downstream and transitive effects.

It may exceed the apparent scope of the initiating permission or component without any direct rule change.

---

## Authority Lineage

The traceable structural relationship between:

* the initiating principal
* assigned authority
* delegated authority
* intermediate actors
* tool or service execution
* resulting actions
* affected resources

Authority Lineage is preserved where responsibility and effective authority remain attributable across the complete action path.

---

## Structural Evidence

Evidence concerning actual system:

* states
* configurations
* relationships
* constraints
* authority paths
* transitions
* resource effects
* topology
* governing boundaries

Structural Evidence is distinct from an unsupported interpretation or narrative about the system.

---

# Canonical Primitives

## Reachable State Space

The complete set of system states that can emerge through the composition of components.

Reachable State Space represents structural possibility, not only observed execution history.

It may expand when:

* new relationships are introduced
* previously separate domains are connected
* authority paths combine
* transitions accumulate
* service topology changes
* permissions gain broader downstream effects
* intermediate states enable additional transitions

Reachable State Space does not determine which states are admissible.

---

## Admissible System State

A state within the Reachable State Space that remains structurally coherent under the constraints governing the composition.

An Admissible System State preserves the relevant:

* authority boundaries
* structural relationships
* transition conditions
* exclusions
* governing constraints
* Invariants
* intended capability boundaries

Local correctness of the components producing the state does not establish its admissibility.

---

## Constraint-Native Governance

The implicit or explicit structural constraints that shape:

* system relationships
* interaction boundaries
* authority
* reachable states
* transition paths
* permissible configurations

Constraint-Native Governance describes governing structure.

It is not necessarily enforced by a runtime mechanism.

Its effectiveness is determined by whether the constraints continue to shape the complete composition, not merely whether their declarations remain present.

---

## State Transition Validation

A conceptual reasoning construct describing whether movement from one system state to another preserves structural coherence and remains within the admissible state space.

State Transition Validation considers:

* Source State
* Intermediate States
* Transition Path
* authority changes
* affected resources
* constraint preservation
* Target State
* resulting reachability

It is not an execution-time validator or software component.

---

## Execution vs Governance Separation

The analytical distinction between:

### Execution correctness

Whether a component, action, tool, service, or transition behaves according to its local specification.

### Governance validity

Whether the composed system and resulting state remain within governing constraints and Governing Intent.

These are independent properties.

A system can execute successfully while reaching an inadmissible state.

---

## Privilege Surface

The effective interaction topology through which composition expands or constrains:

* access
* authority
* capability
* control
* resource effect
* action pathways

Privilege Surface may include relationships between:

* principals
* identities
* roles
* services
* APIs
* agents
* tools
* resources
* delegation paths
* control mechanisms

Generic connectivity does not by itself establish Privilege Surface expansion.

The topology must alter effective interaction, access, authority, capability, or control.

Privilege Surface is not a security product or access-control mechanism.

---

# Canonical Invariants

## Nature of Invariants

CNIG Invariants describe structural properties expected to remain preserved across system composition and transition.

They are analytical reference concepts.

They are not:

* runtime checks
* enforcement rules
* implementation requirements
* observer interpretations
* semantic-coherence measures

An Invariant weakens when the corresponding system property is no longer preserved across the composition.

---

## Identity Invariant

Preservation of identity, authority lineage, responsibility, and attributable action across representations, transitions, and system boundaries.

The Identity Invariant may weaken where:

* one principal maps to non-equivalent effective identities
* authority lineage becomes incomplete
* delegated responsibility cannot be traced
* actions are performed under authority not represented for the initiator
* resource or principal identity changes across mappings
* equivalent identities acquire materially different authority through structural position

The Identity Invariant concerns actual system identity and authority relationships.

It is not about observers describing the same identity differently.

---

## Stability Invariant

Bounded deviation in system behaviour and state under structural variation.

The Stability Invariant may weaken where:

* small topology changes produce disproportionately large outcomes
* minor dependency changes alter the Target State materially
* ordering, concurrency, or timing produces unbounded divergence
* equivalent conditions do not preserve expected system bounds
* a small authority or resource change expands capability significantly

Stability does not require identical outcomes in every system.

It requires system deviation to remain within intended structural and behavioural boundaries.

---

## Behavioral Invariant

Preservation of the expected relationship between local component behaviour and the behaviour of the complete composition.

The Behavioral Invariant may weaken where:

* locally correct components produce an unintended global outcome
* the same valid operation produces a materially broader effect
* equivalent transition conditions produce divergent results
* system behaviour changes through relationship changes rather than component changes
* a composed chain produces effects outside its represented behavioural boundary

Behavioral Invariant concerns actual system behaviour.

It is not a measure of agreement between descriptions of that behaviour.

---

## Structural Invariant

Preservation of coherent and intended relationships between:

* components
* constraints
* system boundaries
* authority paths
* resources
* transitions
* source and target states
* reachable and admissible states

The Structural Invariant may weaken where:

* relationships create unrepresented states
* boundaries no longer preserve their intended effect
* constraint regimes become incompatible
* topology introduces unintended transition paths
* a shared reference resolves to non-equivalent structural objects
* the represented system structure no longer describes the effective composition

---

# Canonical Failure Modes

## Nature of Failure Modes

CNIG Failure Modes describe evidence-supported structural conditions in which composition produces or exposes inadmissibility.

They are not:

* incidents
* alerts
* metrics
* root-cause declarations
* monitoring categories
* observer disagreements
* automatic classifications

The complete definitions and distinctions are canonical in:

`04_FAILURE_MODES.md`

The definitions below are concise glossary forms.

---

## Governance Capture

A condition in which declared governing constraints remain present, but interaction structures weaken, bypass, displace, or neutralize their effective authority over the composed system.

**Distinctive condition:**

> Governance remains declared, but no longer effectively constrains the complete Reachable State Space.

---

## Reference Drift

A condition in which a shared structural reference resolves to non-equivalent effective objects, states, constraints, boundaries, resources, identities, or authority conditions across components or domains.

**Distinctive condition:**

> A reference remains apparently shared while its effective structural referent diverges across the composition.

Reference Drift concerns actual structural non-equivalence.

It is not observer disagreement.

---

## Constitutional Fragmentation

A condition in which locally coherent governance regimes fail to compose into one coherent admissibility structure for shared or Joint States.

**Distinctive condition:**

> Different system regions remain locally governed but no unified constraint structure determines global admissibility.

Constitutional Fragmentation concerns incompatible effective constraint regimes, not different narratives about governance.

---

## Invariant Overconstraint

A condition in which composed constraints restrict the admissible state space beyond Governing Intent.

Intended valid states or transitions become unavailable because the combined restrictive effect exceeds the intended boundary.

**Distinctive condition:**

> Constraint composition eliminates states or transitions that Governing Intent requires to remain admissible.

---

## Recursive Governance Instability

A condition in which determining admissibility depends on another governance determination that ultimately depends on the original determination.

No stable, non-circular basis exists for resolving governance validity.

**Distinctive condition:**

> Governance validity depends on itself through a composed dependency cycle.

---

## Implicit Reachability Expansion Failure

A condition in which composition makes new states or Transition Paths reachable without those possibilities being represented and deliberately acknowledged in the governing Structural Model.

**Distinctive condition:**

> Composition expands the Reachable State Space beyond the represented Structural Model.

A new state is not a failure where it is represented, intended, governed, and admissible.

---

## Stochastic Drift

A condition in which structurally equivalent Source States and transition inputs produce materially divergent system-level outcomes because variability emerges through composition.

**Distinctive condition:**

> Equivalent structural conditions produce divergent global outcomes through compositional variability.

Stochastic Drift must be distinguished from:

* different Source States
* different versions
* incomplete evidence
* intended probabilistic behaviour
* Phase Desynchronization

---

## Phase Desynchronization

A condition in which a transition and the structural state, constraint set, authority condition, or governance model applicable to that transition belong to different effective temporal phases.

**Distinctive condition:**

> The transition and the conditions governing it are temporally misaligned in a way that alters reachability, authority, or admissibility.

Phase Desynchronization concerns actual system phase mismatch, not delayed interpretation by an observer.

---

## Privilege Surface Expansion Failure

A condition in which composition creates or enlarges an effective interaction, access, authority, capability, or control path beyond intended structural boundaries.

**Distinctive condition:**

> Composition creates an effective capability path absent from the intended authority structure.

Connectivity alone does not establish this Failure Mode.

---

## Null State Boundary Violation

A condition in which the composed system reaches a state from which no admissible continuation exists under the governing constraints.

Technically executable transitions may remain, but none preserves admissibility.

**Distinctive condition:**

> The system reaches a state with no admissible outgoing transition.

---

# Architecture Patterns

## Nature of Architecture Patterns

Architecture Patterns describe recurring structural arrangements or behaviours visible under CNIG analysis.

They are descriptive.

They are not:

* design prescriptions
* implementation templates
* reference architectures
* mandatory controls
* Failure Modes by themselves

A pattern may exist without producing an inadmissible state.

---

## Emergent Coupling Pattern

A pattern in which independently correct components acquire undeclared or insufficiently represented dependencies through composition.

The coupling arises from Interaction Topology rather than one explicit component design.

Emergent Coupling may alter:

* transition ordering
* shared state
* downstream effects
* failure propagation
* reachability

It becomes a CNIG failure condition only where the resulting state or path conflicts with Governing Intent.

---

## Constraint Amplification Pattern

A pattern in which local constraints combine to produce a disproportionately larger system-level restriction.

Constraint Amplification may:

* eliminate valid transition paths
* restrict intended capability
* prevent required recovery states
* narrow the admissible state space

Where the restriction exceeds Governing Intent, the pattern may support Invariant Overconstraint.

---

## Hidden Reachability Expansion Pattern

A pattern in which composition introduces reachable states or Transition Paths absent from component-level analysis or the represented Structural Model.

The pattern may arise through:

* new relationships
* inheritance
* delegation
* accumulation
* integration
* intermediate states
* topology changes

Where the expansion is unacknowledged and outside Governing Intent, it may support Implicit Reachability Expansion Failure.

---

## Fragmented Governance Pattern

A pattern in which different regions of a composed system apply separate effective constraint regimes to connected or shared states.

The pattern may include:

* separate local admissibility rules
* absent ownership of a Joint State
* incompatible cross-domain constraints
* unresolved governance boundaries

Where no coherent combined admissibility structure exists, the pattern may support Constitutional Fragmentation.

Fragmented Governance concerns actual constraint structure.

It is not a condition of observers holding different interpretations.

---

## Interaction Topology Drift Pattern

A pattern in which system behaviour changes because relationships between components change while the components themselves remain materially unchanged.

Topology Drift may involve:

* additional dependencies
* different call paths
* retries
* queues
* feedback loops
* changed resource relationships
* altered delegation
* orchestration changes

The pattern may change the Reachable State Space without a component modification.

---

## Stability Under Composition Illusion Pattern

A pattern in which component-level tests and health indicators remain stable while the complete composition exhibits instability or inadmissibility.

The apparent stability results from evaluating components independently rather than evaluating:

* Transition Paths
* Joint States
* topology
* cumulative effects
* authority composition
* Target State admissibility

The pattern does not imply that component-level validation is incorrect.

It indicates that its scope is insufficient to establish global admissibility.

---

## Authority Aggregation Pattern

A pattern in which several valid identity, role, policy, delegation, or resource relationships combine into an Effective Authority state not visible in any one assignment.

The pattern may include:

* nested groups
* inherited roles
* overlapping policies
* conditional grants
* alternative authorization paths
* transitive delegation

Where the resulting authority path is outside the intended model, the pattern may support Privilege Surface Expansion Failure.

---

## Downstream Capability Expansion Pattern

A pattern in which an existing permission or authorized operation retains the same entry boundary while acquiring a broader system-level effect through changed downstream composition.

The permission does not change.

Its Effective Capability does.

This pattern is distinct from a new access path.

---

## Cross-Domain Joint-State Pattern

A pattern in which separately governed systems become connected and jointly reach a state that neither local governance boundary represents or evaluates in full.

Each local state may remain admissible.

The Joint State may still require independent compositional evaluation.

---

## Transition-Chain Accumulation Pattern

A pattern in which individually valid transitions accumulate into a system-level Target State that no individual stage evaluates in full.

The pattern may occur in:

* pipelines
* workflows
* orchestration
* service chains
* agents
* approval systems

The relevant object is the complete Transition Path.

---

# Diagnostic Terms

## Observation

A recorded system condition, behaviour, state change, relationship, or outcome used as potential evidence in CNIG analysis.

An Observation does not automatically establish:

* structural cause
* inadmissibility
* an affected Invariant
* a Failure Mode

Observation files in the repository are illustrative and non-canonical.

---

## Observed

A diagnostic status indicating that the relevant condition is directly supported by available evidence.

Examples may include:

* a state was reached
* a relationship exists
* a permission remained unchanged
* a transition completed
* a resource was affected

Observed status does not by itself establish structural cause or Failure Mode classification.

---

## Inferred

A diagnostic status indicating that a conclusion follows from available evidence but has not been directly observed in full.

An Inference must identify:

* the evidence consumed
* the reasoning relationship
* unresolved alternatives
* the uncertainty remaining

---

## Canonical

A diagnostic or documentary status indicating that a definition, name, relationship, or ordering is established by the governing CNIG framework files.

Canonical status applies to framework content.

It does not make an unverified system claim factual.

---

## Provisional

A diagnostic status indicating that a structural classification is plausible but one or more required conditions remain unsupported.

Failure Mode attribution should remain Provisional until its defining structural conditions are established.

---

## Conflicting

A diagnostic status indicating that available evidence supports materially incompatible accounts of the relevant system state, relationship, or transition.

Conflicting evidence must not be silently merged.

This status concerns evidence quality.

It is not itself a CNIG Failure Mode.

---

## Unresolved

A diagnostic status indicating that available evidence is insufficient to determine the relevant:

* state
* relationship
* transition
* authority path
* structural cause
* admissibility condition
* Failure Mode

Unresolved is a valid analytical result.

CNIG does not require a classification where the evidence does not support one.

---

## Structural Cause

The composition relationship or transition condition that made the observed outcome structurally reachable.

A Structural Cause is distinct from:

* the observed outcome
* a component symptom
* an unsupported explanation
* a Failure Mode label

---

## Admissibility Condition

The structural basis for determining whether a reachable state or path remains within Governing Intent.

An Admissibility Condition may include:

* required constraints
* prohibited relationships
* authority boundaries
* target-state requirements
* separation rules
* valid continuation requirements
* Invariant preservation

A Failure Mode cannot be established solely from surprise or undesired outcome.

The relevant Admissibility Condition must be identified.

---

## Failure-Mode Attribution

The evidence-supported assignment of a canonical CNIG Failure Mode to an observed structural condition.

Failure-Mode Attribution should identify:

* observed outcome
* Structural Cause
* affected state or Transition Path
* governing constraints
* Admissibility Condition
* canonical Failure Mode conditions
* unresolved evidence

Attribution is not automatic.

---

# Framework Boundary Terms

## Observer Disagreement

A condition in which different people, tools, models, or interfaces describe the same system differently.

Observer Disagreement is not itself a CNIG Failure Mode.

It becomes relevant to CNIG only where evidence establishes an actual structural difference, such as:

* non-equivalent mappings
* different effective constraints
* different Source States
* different authority paths
* different temporal phases

---

## Evidence Fragmentation

A condition in which relevant information is distributed, incomplete, inaccessible, or difficult to combine.

Evidence Fragmentation may limit diagnostic certainty.

It does not establish a structural CNIG condition by itself.

---

## Semantic Coherence

The consistency with which meaning can be preserved or reconstructed across information fragments or representations.

Semantic Coherence is not a CNIG analytical object.

CNIG concerns actual system structure, reachability, transitions, constraints, authority paths, and admissibility.

---

## Reconstructive Coherence

The ability of an observer or system to reconstruct a coherent account from fragmented information.

Reconstructive Coherence is outside CNIG’s ontology.

It must not be substituted for:

* Structural Invariant
* Reference Drift
* Constitutional Fragmentation
* Identity Invariant
* Phase Desynchronization

---

## Interpretation

The act of applying CNIG concepts to evidence.

Interpretation is a diagnostic activity performed through an external methodology.

It is not the system object being governed by CNIG.

Where older CNIG text uses “interpretation” to describe actual system behaviour, it should be read or revised in terms of:

* structural representation
* constraint application
* state identity
* authority mapping
* governing scope
* system phase
* effective system relationship

---

# Canonical Distinctions

## Reachable vs Admissible

* **Reachable:** the composition can enter or produce the state.
* **Admissible:** the state remains structurally coherent under governing constraints.

A state can be reachable but inadmissible.

---

## Local Correctness vs Global Admissibility

* **Local correctness:** a component satisfies its specification or local validation conditions.
* **Global admissibility:** the complete composed state remains within Governing Intent.

Local correctness does not establish global admissibility.

---

## Permission vs Effective Capability

* **Permission:** a declared authorization to perform an operation.
* **Effective Capability:** the complete system effect reachable through that operation and its downstream composition.

An unchanged permission may acquire broader Effective Capability.

---

## Identity vs Effective Authority

* **Identity:** the represented principal or system entity.
* **Effective Authority:** the complete authority available through composed identity, role, delegation, service, and resource relationships.

A stable identity may participate in a changed Effective Authority state.

---

## Connectivity vs Privilege Surface

* **Connectivity:** the existence of a communication or relationship path.
* **Privilege Surface:** topology that changes effective interaction, access, authority, capability, or control.

Connectivity alone does not establish Privilege Surface expansion.

---

## Local Transition Validity vs Complete Transition-Path Admissibility

* **Local transition validity:** one transition satisfies its local conditions.
* **Complete Transition-Path admissibility:** the accumulated sequence preserves governing constraints and reaches an admissible Target State.

Every local transition may be valid while the complete path is not.

---

## Structural Representation vs Observer Interpretation

* **Structural Representation:** how the system encodes or instantiates identities, constraints, states, mappings, boundaries, and authority.
* **Observer Interpretation:** how an external observer understands or describes the system.

CNIG analyses Structural Representation and actual system structure.

It does not classify Observer Interpretation by itself.

---

## Reference Drift vs Observer Disagreement

* **Reference Drift:** one shared reference resolves to non-equivalent effective structural referents.
* **Observer Disagreement:** observers describe the reference differently.

Only the first is a CNIG Failure Mode.

---

## Constitutional Fragmentation vs Fragmented Understanding

* **Constitutional Fragmentation:** incompatible effective governance regimes fail to define global admissibility.
* **Fragmented Understanding:** knowledge of the system is incomplete or distributed.

Only the first is a CNIG Failure Mode.

---

## Phase Desynchronization vs Delayed Awareness

* **Phase Desynchronization:** the transition and governing structural conditions belong to different effective system phases.
* **Delayed Awareness:** an observer learns of the transition later.

Only the first is a CNIG Failure Mode.

---

# Canonical Reference

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

Canonical framework navigation:

* `00_CANONICAL_IDENTITY.md`
* `PROBLEM_CLASS.md`
* `02_CONCEPTUAL_CORE.md`
* `03_PRIMITIVES.md`
* `04_FAILURE_MODES.md`
* `GLOSSARY.md`
* `11_INTERPRETATION_GUIDE.md`
* `12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

The canonical names and ordering of the six Primitives, four Invariants, and ten Failure Modes must remain stable.

Observation files may illustrate these concepts. External applications may reference or apply them, but any implementation remains outside CNIG and does not alter the canonical framework.

They may not silently rename, broaden, merge, or replace them.
