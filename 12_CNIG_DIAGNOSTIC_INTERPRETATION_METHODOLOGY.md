# CNIG Diagnostic Interpretation Methodology

## Constraint-Native Infrastructure Governance (CNIG)

**Canonical attribution:** Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Document

This document defines the diagnostic methodology used to interpret system behaviour through the Constraint-Native Infrastructure Governance (CNIG) framework.

It provides a structured method for mapping observed system behaviour to:

* CNIG Primitives
* CNIG Invariants
* CNIG Failure Modes
* system boundaries and transitions
* compositional effects across system structures
* structural relationships evidenced across observations

The objective is not to describe systems only in operational or component-level terms.

The objective is to examine how system composition makes observable behaviour possible and whether the resulting system state remains structurally admissible.

This document establishes the vocabulary, analytical sequence, and scope boundaries required for consistent CNIG analysis across observations.

It does not replace the canonical definitions contained elsewhere in the CNIG repository.

---

## 2. Diagnostic Principle

CNIG diagnostics begin from the following analytical principle:

> Within the problem domain examined by CNIG, structural inadmissibility may emerge before observable execution failure.

CNIG does not assume that every system failure is structural.

CNIG also does not assume that local components are always correct.

Instead, CNIG examines whether elements that are locally valid, individually functional, or procedurally compliant can produce an unintended or inadmissible system state when composed.

The diagnostic focus therefore includes:

* interaction structure
* reachable-state expansion or contraction
* privilege-surface changes
* state-transition validity
* invariant deformation under composition
* divergence between governance intent and execution behaviour
* emergent effects that cannot be attributed to one component in isolation

The foundational CNIG distinction is:

> Local correctness does not guarantee global admissibility.

---

## 3. CNIG Ontology Reference Set

This section provides a stable reference index for the vocabulary used across CNIG observation analysis.

The names below are canonical references.

Their complete definitions remain in the relevant CNIG conceptual-core, primitive, invariant, failure-mode, state-model, glossary, and interpretation documents.

This methodology must not silently redefine, merge, rename, flatten, substitute, or expand these terms.

---

### 3.1 Primitives

CNIG Primitives define the structural basis of analysis.

1. **Reachable State Space**
2. **Admissible System State**
3. **Execution vs Governance Separation**
4. **Privilege Surface**
5. **State Transition Validation**
6. **Constraint-Native Governance**

Primitives identify the structural axes through which system composition is examined.

They are not incident categories, component types, implementation mechanisms, or remediation controls.

---

### 3.2 Invariants

CNIG Invariants define the conditions expected to remain stable across system composition and state transition.

1. **Identity Invariant**
2. **Stability Invariant**
3. **Behavioral Invariant**
4. **Structural Invariant**

An invariant may remain valid locally while becoming inconsistent, weakened, overconstrained, or structurally divergent at a broader compositional level.

Invariants must therefore be evaluated across relevant system boundaries, not only within individual components.

---

### 3.3 Failure Modes

CNIG Failure Modes define classes of compositional breakdown.

1. **Reference Drift**
2. **Privilege Surface Expansion Failure**
3. **Constitutional Fragmentation**
4. **Invariant Overconstraint**
5. **Recursive Governance Instability**
6. **Implicit Reachability Expansion Failure**
7. **Stochastic Drift**
8. **Phase Desynchronization**
9. **Null State Boundary Violation**
10. **Governance Capture**

Failure Modes are not synonymous with:

* component errors
* alerts
* incidents
* implementation defects
* product failures
* isolated operational events

They describe how structural consistency, admissibility, governance, privilege, transition validity, or invariant preservation can break under composition.

---

## 4. Observation Analysis Model

Each `OBS_*` entry represents an observational trace of system behaviour under composition.

An observation is not automatically:

* an incident
* a root cause
* a component failure
* a fixed taxonomy node
* proof of a particular Failure Mode
* an operational remediation case

An observation provides evidence that may be analysed through:

* **Primitives** — which CNIG structural axes are involved
* **Invariants** — which stability conditions are affected
* **Failure Modes** — which compositional breakdown class may apply
* **System boundaries** — where constraint scope, authority, identity, privilege, or governance changes
* **State transitions** — how the system moves between states
* **Structural relationships** — shared entities, constraints, dependencies, transitions, or effects evidenced across observations

Observations may be:

* repeatable
* situational
* partial
* context-dependent
* incomplete
* provisional

Repeatability, causation, and Failure Mode attribution must not be presumed without supporting evidence.

---

## 5. Diagnostic Evaluation Sequence

The following sequence defines the standard CNIG diagnostic path.

The sequence is ordered, but analysis may return to an earlier stage when new evidence changes the structural assessment.

---

### Step 1 — Observation Decomposition

Decompose the observation into:

* local component state
* evidence of local correctness or failure
* relevant system entities
* applicable constraints
* relevant system boundaries
* compositional relationships
* observed state transitions
* emergent system effects
* unresolved evidence gaps

The analysis must distinguish between:

* what was directly observed
* what is inferred from the evidence
* what is defined canonically by CNIG
* what remains unresolved

Local correctness is neither presumed nor excluded.

The governing question is:

> Can locally valid or apparently correct elements produce structurally divergent behaviour when composed?

---

### Step 2 — Constraint and Transition Boundary Identification

Identify the system boundaries across which any of the following changes:

* constraint applicability
* authority scope
* identity scope
* privilege scope
* governance jurisdiction
* enforcement responsibility
* state ownership
* transition validity
* policy applicability
* execution control

Relevant boundaries may include:

* identity boundaries
* administrative boundaries
* trust boundaries
* privilege boundaries
* policy-to-enforcement boundaries
* control-plane and data-plane boundaries
* local-state and global-state boundaries
* governance and execution boundaries
* temporal or phase boundaries
* state-transition boundaries

A boundary is not automatically a failure point.

It is a location where constraints, authority, privilege, governance, or state-transition validity may need to be re-evaluated.

---

### Step 3 — Primitive Alignment

Identify the CNIG Primitives relevant to the observed system structure.

Primitive alignment is many-to-many and evidence-dependent.

Illustrative starting associations include:

* identity behaviour may involve **Reachable State Space**, **Privilege Surface**, or **State Transition Validation**
* access behaviour may involve **Privilege Surface**, **Admissible System State**, or **Constraint-Native Governance**
* execution divergence may involve **Execution vs Governance Separation**
* unintended state expansion may involve **Reachable State Space**
* transition ambiguity may involve **State Transition Validation**
* system-wide governance drift may involve **Constraint-Native Governance**

These associations are not fixed classifications.

An observation may involve multiple Primitives, and a Primitive may be relevant to multiple observations.

Primitive alignment must be justified through the represented system structure.

---

### Step 4 — Invariant Evaluation

Evaluate how each relevant invariant behaves under composition.

Possible states include:

* locally stable
* globally stable
* locally stable but globally inconsistent
* conditionally stable
* weakened across a system boundary
* overconstrained
* structurally divergent under aggregation
* violated during a state transition
* unresolved due to insufficient evidence

The evaluation must identify:

* where the invariant appears stable
* where its conditions change
* which boundaries affect it
* which transitions affect it
* whether local preservation produces global deformation
* whether the resulting state remains admissible

Invariant evaluation must not be reduced to component health.

A component may remain healthy while the composed invariant fails.

---

### Step 5 — Reachability and Admissibility Evaluation

Determine whether the observed composition:

* expands reachable states
* contracts reachable states
* creates implicit transitions
* removes valid continuation states
* exposes previously inaccessible privilege paths
* enables states outside intended governance boundaries
* produces reachable but structurally inadmissible states
* prevents intended admissible states from remaining reachable
* creates states whose admissibility cannot be established

Reachability and admissibility must remain distinct.

A state may be:

* reachable and admissible
* reachable but inadmissible
* admissible in principle but unreachable
* neither reachable nor admissible
* unresolved because applicable constraints are incomplete or conflicting

The existence of a state does not establish its admissibility.

The absence of an observed failure does not establish that the state is admissible.

---

### Step 6 — State Transition Evaluation

Identify the transition or sequence of transitions that produced, enabled, or exposed the observed state.

Evaluate:

* the source state
* the target state
* the transition authority
* the applicable constraints
* the validation point
* the affected entities
* the privilege surface before and after transition
* the invariants expected to remain stable
* the resulting reachable-state changes
* whether the transition was explicitly governed
* whether the resulting state was validated

A transition may be individually valid while contributing to a globally inadmissible system state.

State Transition Validation must therefore examine both:

* local transition validity
* compositional effect on the resulting system state

---

### Step 7 — Governance and Execution Comparison

Compare:

* declared governance
* intended governance
* implemented governance
* enforced constraints
* observed execution behaviour
* resulting system state

The purpose is to determine whether governance and execution remain aligned under composition.

Divergence may occur when:

* policy scope changes across implementation boundaries
* execution permits states governance did not intend
* governance assumes constraints that are not enforced
* distributed authorities apply incompatible constraints
* execution remains locally compliant while the global state becomes inadmissible
* governance validates actions but not the resulting composed state
* authority exists to execute a transition but not to authorize its global consequences

Governance intent must not be inferred from execution alone.

Observed execution must not be treated as approved governance merely because it occurred.

---

### Step 8 — Failure Mode Attribution

A Failure Mode may be attributed only when the available structural evidence supports its canonical definition.

Attribution must identify:

* the relevant observation
* the implicated Primitives
* the affected Invariants
* the relevant system boundary
* the relevant state transition
* the reachable-state effect
* the admissibility effect
* the governance or privilege effect
* the evidence supporting attribution
* competing structural explanations
* unresolved evidence
* whether the attribution is provisional or established

Failure Modes must not be assigned through:

* keyword matching
* one-to-one lookup
* superficial symptom similarity
* component-error classification
* unsupported causal assumption

Different Failure Modes have different structural conditions.

For example:

* **Implicit Reachability Expansion Failure** concerns unintended expansion of reachable states
* **Invariant Overconstraint** may reduce valid behaviour or eliminate admissible continuation
* **Phase Desynchronization** concerns structural or temporal misalignment between system states or governing processes
* **Recursive Governance Instability** concerns governance processes that recursively destabilize their own evaluation or enforcement
* **Null State Boundary Violation** concerns invalid movement into, through, or beyond a state where required structural continuity is absent

Failure Mode attribution is evidence-dependent and may remain provisional.

---

### Step 9 — Cross-Observation Structural Correlation

When multiple observations are present, determine whether they evidence shared:

* system entities
* constraints
* state transitions
* privilege paths
* governance boundaries
* invariant effects
* reachable-state changes
* admissibility failures
* structural dependencies

Cross-observation analysis must ask whether combined evidence exposes compositional behaviour that is not visible from an observation in isolation.

Relevant questions include:

* Do identity and access observations expose a shared privilege or reachability boundary?
* Do multiple observations involve the same governing constraint?
* Does execution behaviour reveal separation from declared governance?
* Do separate state transitions contribute to the same inadmissible state?
* Do multiple observations expose deformation of the same invariant?
* Does one observation provide missing structural evidence for another?
* Do apparently independent observations share a dependency or authority boundary?
* Do combined observations expose a reachable state, invariant deformation, or governance divergence that is not visible locally?

Shared entities, sequence, dependency, or affected state do not by themselves establish causation.

Structural relationships must be supported by evidence.

---

### Step 10 — Diagnostic State Assignment

Each material diagnostic conclusion should be assigned a state.

Recommended states include:

* **OBSERVED** — directly supported by available evidence
* **INFERRED** — derived from supported structural relationships
* **CANONICAL** — defined by the CNIG framework
* **PROVISIONAL** — plausible but awaiting further evidence
* **CONFLICTING** — contradicted by another observation or canonical source
* **UNRESOLVED** — insufficient evidence for reliable attribution

Unsupported conclusions must remain unresolved.

Recency, repetition, confidence, or fluent explanation does not make a conclusion canonical.

---

## 6. Observation Registry Mapping Principle

Each `OBS_*` entry may be represented as a structural node in an evolving CNIG compositional graph.

The graph represents the system structures evidenced by the observations.

It does not treat observations themselves as interacting system components.

The following rules apply:

* OBS entries are not permanently hard-classified nodes
* Primitive mappings are contextual
* Invariant relationships are many-to-many
* Failure Mode attribution may change when new structural evidence appears
* graph relationships must be supported by structural evidence
* graph edges must identify the represented relationship
* shared sequence or dependency does not by itself establish a causal transition
* new observations may revise earlier structural assessments
* revisions must preserve provenance and supersession

Relevant graph relationships may include:

* shared system entity
* shared constraint
* shared invariant
* shared authority
* shared privilege path
* shared state transition
* dependency relationship
* governance relationship
* reachable-state relationship
* admissibility relationship

Earlier assessments must not be silently overwritten.

Where an assessment changes, the revision should identify:

* the previous assessment
* the new evidence
* the reason for revision
* the affected structural relationships
* the current authoritative state

---

## 7. Cross-Observation Structural Rule

Cross-observation analysis must evaluate system composition rather than merely count similar observations.

The objective is to determine whether separate observations expose a common structural condition.

Relevant questions include:

* Do multiple observations involve the same reachable-state expansion?
* Do identity and access observations expose a shared privilege boundary?
* Do separate transitions affect the same invariant?
* Does observed execution diverge from the same governing constraint?
* Do multiple local states contribute to one globally inadmissible state?
* Does one observation identify a dependency required to explain another?
* Does a repeated structural pattern indicate a shared constraint or transition?
* Do combined observations expose a compositional effect that no observation establishes independently?

Cross-observation evidence may strengthen, weaken, or contradict a structural assessment.

It must not automatically establish a Failure Mode or causal chain.

---

## 8. Diagnostic Grouping Lenses

The following lenses may be used to organize observations for CNIG analysis.

They are diagnostic groupings.

They are not additional CNIG Primitives, Invariants, or Failure Modes.

They are non-exhaustive and may overlap.

---

### 8.1 Local Stability with Global Drift

Individual components remain locally valid or functional, but composition changes global behaviour, reachability, or admissibility.

Potentially associated Failure Modes include:

* Stochastic Drift
* Implicit Reachability Expansion Failure
* Privilege Surface Expansion Failure
* Invariant Overconstraint

The applicable mapping depends on structural evidence.

---

### 8.2 Constraint Boundary Failure

Constraint applicability, authority, privilege, identity scope, timing, or reference changes across a system boundary in a way that affects structural admissibility.

Potentially associated Failure Modes include:

* Reference Drift
* Phase Desynchronization
* Constitutional Fragmentation
* Governance Capture

A boundary change alone does not establish failure.

The analysis must show how the change affects:

* constraint enforcement
* reachable states
* privilege
* governance
* transition validity
* invariant preservation
* system admissibility

---

### 8.3 Compositional Instability

System-wide instability emerges from:

* interaction topology
* recursive governance
* conflicting authorities
* incompatible constraints
* missing structural continuation
* invalid state transitions
* incompatible local states
* ungoverned reachable-state expansion

Potentially associated Failure Modes include:

* Constitutional Fragmentation
* Recursive Governance Instability
* Governance Capture
* Null State Boundary Violation

Compositional instability must not be reduced to an individual component defect unless evidence establishes that cause.

---

## 9. CNIG Interpretation Integrity

A valid CNIG analysis must preserve:

* canonical names
* canonical definitions
* the distinction between Primitives, Invariants, and Failure Modes
* the distinction between reachability and admissibility
* the distinction between local correctness and global admissibility
* the distinction between governance intent and observed execution
* the distinction between transition validity and resulting-state admissibility
* many-to-many mappings
* evidence-supported structural relationships
* provenance and supersession
* the non-operational boundary
* unresolved state where evidence is insufficient

A CNIG analysis is invalid if it:

* treats CNIG as conventional incident management
* reduces Failure Modes to component errors
* treats observations as fixed taxonomy classes
* converts illustrative mappings into universal rules
* assumes correlation establishes causation
* merges Primitives, Invariants, and Failure Modes
* invents operational mechanisms not defined by CNIG
* treats observed state as approved governance
* treats reachability as proof of admissibility
* silently replaces canonical terminology
* presents provisional attribution as established fact
* imports constructs or analytical objects from another framework

The objective is not exact textual repetition.

The objective is preservation of CNIG’s canonical identity, structural relationships, scope, and analytical direction.

---

## 10. Framework Boundary

This methodology applies only to CNIG.

It must not import, merge with, or reinterpret CNIG through constructs belonging to another framework.

CNIG analysis remains centred on:

* system structure
* reachable states
* admissible states
* invariants
* privilege surfaces
* state transitions
* governance
* compositional failure modes

Cross-framework comparison, where required, must be:

* explicit
* separately scoped
* non-substitutive
* terminology-preserving
* attribution-preserving

No external framework construct becomes part of CNIG merely because a conceptual relationship can be identified.

Framework adjacency must not become ontology merger.

---

## 11. Non-Operational Boundary

This document does not define:

* remediation procedures
* configuration changes
* implementation guidance
* runtime enforcement mechanisms
* autonomous actions
* product architecture
* operational control systems
* diagnostic commands
* vendor-specific troubleshooting
* guaranteed causal attribution

It defines CNIG diagnostic interpretation only.

CNIG may inform operational reasoning, but this document does not authorize or specify an operational derivative.

---

## 12. Stability Principle

The diagnostic methodology remains coherent when:

* observations are treated as structural evidence
* Primitives define structural axes
* Invariants define stability conditions
* Failure Modes define compositional breakdown classes
* relationships remain evidence-dependent
* reachability remains distinct from admissibility
* local correctness remains distinct from global structural validity
* governance remains distinct from execution
* transition validity remains distinct from resulting-state admissibility
* unresolved evidence remains explicitly unresolved
* revisions preserve provenance and supersession
* CNIG remains separate from adjacent frameworks

The methodology degrades when:

* observations are treated as isolated incidents
* component health is equated with system admissibility
* mappings become rigid or one-to-one
* framework terms are silently substituted
* correlation is converted into causation
* later assessments erase earlier provenance
* operational assumptions are imported into the non-operational framework
* local correctness is used to infer global correctness
* reachability is used to infer admissibility
* adjacent framework concepts are imported into CNIG

---

## 13. Closing Principle

CNIG diagnostics do not stop at describing what happened.

They examine:

> **how structure made what happened possible**
