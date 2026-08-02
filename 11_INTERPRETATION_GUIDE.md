# CNIG Interpretation Guide

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer defines how CNIG concepts should be read, applied, distinguished, and referenced consistently.

It protects the framework from:

* ontology expansion
* terminology drift
* unsupported Failure Mode attribution
* reduction into implementation logic
* confusion between local correctness and global admissibility
* confusion between system structure and observer understanding
* collapse into adjacent frameworks or disciplines

This document is not:

* a system-design manual
* an implementation guide
* an engineering methodology
* an operational procedure
* a diagnostic workflow
* a replacement for canonical definitions

The diagnostic methodology used to apply CNIG to observational evidence is defined separately in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

CNIG itself remains a conceptual framework, not a methodology.

---

## 2. Meaning of Interpretation

Within this repository, **interpretation** means:

> applying CNIG’s canonical concepts to evidence about an actual system.

Interpretation is an external analytical activity.

It may involve determining:

* what system state was present
* what transition occurred
* what relationships formed the composition
* what states became reachable
* what constraints applied
* whether the resulting state remained admissible
* which Invariants were affected
* whether a canonical Failure Mode is supported

Interpretation is not the primary object governed by CNIG.

CNIG does not analyse:

* how an observer reconstructs fragmented information
* whether narratives remain semantically coherent
* whether different observers agree
* whether an LLM understands the system correctly
* whether evidence can be recomposed into one account

Those conditions are outside CNIG unless they establish evidence of an actual difference in system structure, state, authority, constraint application, transition path, or admissibility.

---

## 3. Primary Reading Principle

CNIG should be read as a bounded structural framework concerned with:

> what states become reachable through system composition, and which of those states remain admissible under governing constraints.

Its primary analytical object is the composed system.

Relevant system objects include:

* components
* relationships
* constraints
* identities
* authority paths
* permissions
* capabilities
* source states
* intermediate states
* target states
* transition paths
* system boundaries
* reachable states
* admissible states

CNIG is not primarily concerned with the correctness of a description of the system.

It is concerned with the structure and consequences of the system itself.

---

## 4. Core Problem Recognition

CNIG is most relevant where evidence supports the following pattern:

* components are locally valid or correct
* local rules may be enforced correctly
* transitions may succeed
* no single component fault explains the result
* but the composition makes an unintended or inadmissible state reachable

This is the CNIG problem class:

> **Component-correct, composition-inadmissible systems.**

The presence of complexity, integration, unexpected behaviour, or multiple components is not sufficient.

The analysis must establish a meaningful distinction between:

* local correctness
* structural reachability
* and global admissibility

---

## 5. Applicability Test

Before applying CNIG, determine whether the problem materially involves composition.

CNIG may be applicable where the outcome depends on:

* several locally valid components
* accumulated state transitions
* interaction topology
* authority aggregation
* delegation
* inherited relationships
* cross-domain integration
* shared resources
* service-mediated effects
* downstream capability
* governing constraints that span component boundaries

The minimum applicability question is:

> Does the outcome depend on relationships between components in a way that cannot be explained adequately from one component boundary alone?

If the answer is no, CNIG may not be the appropriate framework.

---

## 6. Non-Applicability Conditions

CNIG should not be applied merely because:

* a component failed
* a configuration is directly incorrect
* a permission was explicitly misassigned
* a policy was plainly violated
* software contains a conventional defect
* an operator made a known error
* a system is complex
* information is incomplete
* observers disagree
* an explanation is difficult
* an outcome was unexpected

These conditions may coexist with a CNIG problem.

They do not establish one.

Where an ordinary component fault, direct misconfiguration, explicit policy violation, or conventional failure sufficiently explains the outcome, that explanation should not be displaced by a compositional classification without evidence.

---

## 7. Canonical Reading Hierarchy

CNIG files do not carry equal definitional authority.

Use the following hierarchy.

### 7.1 Canonical identity and attribution

`00_CANONICAL_IDENTITY.md`

This file governs:

* framework identity
* canonical name
* authorship
* attribution

### 7.2 Canonical problem class

`PROBLEM_CLASS.md`

This file governs:

* the condition CNIG addresses
* inclusion criteria
* exclusion criteria
* the distinction between local correctness and global inadmissibility

### 7.3 Canonical framework definition

`02_CONCEPTUAL_CORE.md`

This file governs:

* CNIG’s conceptual scope
* its primary structural distinction
* its relationship to execution and implementation

### 7.4 Canonical Primitives

`03_PRIMITIVES.md`

This file governs the names, scope, and ordering of the six Primitives:

1. Reachable State Space
2. Admissible System State
3. Constraint-Native Governance
4. State Transition Validation
5. Execution vs Governance Separation
6. Privilege Surface

### 7.5 Canonical Failure Modes

`04_FAILURE_MODES.md`

This file governs the names, scope, ordering, conditions, and distinctions of the ten Failure Modes:

1. Governance Capture
2. Reference Drift
3. Constitutional Fragmentation
4. Invariant Overconstraint
5. Recursive Governance Instability
6. Implicit Reachability Expansion Failure
7. Stochastic Drift
8. Phase Desynchronization
9. Privilege Surface Expansion Failure
10. Null State Boundary Violation

### 7.6 Canonical terminology and Invariants

`GLOSSARY.md`

This file governs:

* defined framework terminology
* the four Invariants
* concise canonical term definitions
* distinctions between structurally related concepts

The four Invariants are:

1. Identity Invariant
2. Stability Invariant
3. Behavioral Invariant
4. Structural Invariant

### 7.7 Interpretation boundary

`11_INTERPRETATION_GUIDE.md`

This file governs:

* how canonical concepts should be read
* how framework boundaries should be preserved
* how conflicts between layers should be resolved

### 7.8 Diagnostic application

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

This file governs the external methodology used to analyse observational evidence through CNIG.

It may apply canonical concepts.

It may not redefine them.

### 7.9 Illustrative observations

`OBS_*` files are illustrative and non-canonical.

They may:

* demonstrate structural conditions
* provide examples
* show relationships between concepts
* support diagnostic analysis

They may not redefine:

* CNIG
* a Primitive
* an Invariant
* a Failure Mode
* the framework boundary

Where an observation conflicts with a canonical layer, the canonical layer governs.

---

## 8. Vocabulary Consistency Rule

CNIG terminology must retain its canonical structural meaning.

Terms must not be silently:

* renamed
* merged
* broadened
* narrowed
* substituted
* converted into implementation objects
* imported into another ontology
* replaced by a similar term from another framework

A term appearing similar to a CNIG term is not automatically equivalent.

For example:

* connectivity is not automatically Privilege Surface
* a new state is not automatically Implicit Reachability Expansion Failure
* local policy differences are not automatically Constitutional Fragmentation
* delayed awareness is not Phase Desynchronization
* observer disagreement is not Reference Drift
* probabilistic output is not automatically Stochastic Drift
* strict constraints are not automatically Invariant Overconstraint
* system unavailability is not automatically Null State Boundary Violation

Canonical conditions must be established.

---

## 9. Reading the Primitives

Primitives are analytical reference concepts.

They are not:

* software components
* APIs
* services
* data structures
* enforcement mechanisms
* implementation requirements
* product features

### Reachable State Space

Read this as the complete structural possibility space created through composition.

Do not reduce it to:

* states already observed
* states documented in a design
* states one component can produce independently

### Admissible System State

Read this as a reachable state that remains coherent under governing constraints.

Do not equate admissibility with:

* execution success
* component health
* policy presence
* absence of an alert
* local permission approval

### Constraint-Native Governance

Read this as the governing structural constraints that shape the composition.

Do not assume that declared governance remains effective merely because its rules or vocabulary remain present.

### State Transition Validation

Read this as a conceptual evaluation of whether a complete transition preserves admissibility.

Do not reduce it to:

* input validation
* API validation
* pipeline-stage success
* one component’s transition check
* a runtime validation engine

### Execution vs Governance Separation

Read this as the distinction between:

* whether execution succeeds locally
* whether the resulting composed state remains within Governing Intent

Do not infer governance validity from execution success.

### Privilege Surface

Read this as the effective topology through which composition changes:

* interaction
* access
* authority
* capability
* control
* resource effect

Do not apply Privilege Surface to generic connectivity that does not alter effective capability or authority.

---

## 10. Reading the Invariants

Invariants describe structural properties expected to remain preserved across composition and transition.

They are not “interpretive stability” concepts.

They are not:

* observer viewpoints
* semantic-coherence measures
* runtime enforcement rules
* health checks
* automatic pass/fail controls

### Identity Invariant

Concerns preservation of:

* principal identity
* resource identity
* authority lineage
* responsibility
* attributable action

It does not concern whether observers describe an identity consistently.

### Stability Invariant

Concerns bounded system deviation under structural variation.

It does not require absolute determinism.

It concerns whether changes remain within intended structural and behavioural bounds.

### Behavioral Invariant

Concerns preservation of the expected relationship between local component behaviour and global composed behaviour.

It does not concern agreement between descriptions of system behaviour.

### Structural Invariant

Concerns preservation of coherent and intended relationships between components, boundaries, constraints, authority paths, transitions, and states.

It does not concern whether an observer can reconstruct those relationships coherently.

---

## 11. Reading the Failure Modes

Failure Modes are evidence-supported structural conditions.

They are not:

* symptoms
* keywords
* incidents
* alerts
* severities
* root causes
* generic risk categories
* automatic labels

A Failure Mode should be assigned only where evidence establishes:

1. the relevant observed state or effect;
2. the composition relationship that made it reachable;
3. the applicable Governing Constraint or Admissibility Condition;
4. why the resulting state or path is structurally problematic;
5. the canonical conditions of the proposed Failure Mode.

Where evidence is incomplete, classification should remain:

* PROVISIONAL
* CONFLICTING
* or UNRESOLVED

An unexpected result does not justify selecting the most linguistically similar Failure Mode.

---

## 12. State and Transition Reading Rule

Within CNIG:

### State

A State is a structural system configuration.

It may include:

* component configuration
* identity and authority
* relationships
* active constraints
* topology
* shared resources
* dependencies
* temporal phase

A State is not limited to a runtime snapshot.

### Transition

A Transition is movement from one structural configuration to another.

A complete Transition Path may contain:

* several local actions
* intermediate states
* delegated authority
* service calls
* shared-state changes
* downstream effects
* cross-domain transitions

A Transition is not merely an abstract metaphor.

Observed execution may provide evidence that a structural transition occurred.

### Transition admissibility

Every local transition may be valid while the complete Transition Path reaches an inadmissible Target State.

Analysis must therefore distinguish:

* local transition validity
* complete Transition-Path admissibility

---

## 13. Reachability Before Failure Classification

CNIG analysis should establish reachability before assigning a Failure Mode.

The analysis should identify:

* the Source State
* the relevant relationships
* the Transition Path
* Intermediate States
* the Target State
* changes to authority or capability
* the applicable Governing Constraints
* whether the Target State was represented
* whether it remained admissible

A state being possible, new, unexpected, or undocumented is not by itself a failure.

The relevant question is:

> Did composition make the state reachable in a way that conflicts with the governing structural model or Governing Intent?

---

## 14. Evidence Discipline

CNIG analysis must distinguish between:

* **OBSERVED** — directly supported by evidence
* **INFERRED** — derived from supported structural relationships
* **CANONICAL** — defined by the CNIG framework
* **PROVISIONAL** — plausible but not fully established
* **CONFLICTING** — contradicted by other evidence or canonical material
* **UNRESOLVED** — insufficient evidence

A fluent explanation is not evidence.

Repeated description is not proof.

Similarity to an observation file is not sufficient for classification.

Where the relevant system structure cannot be established, the analysis should remain unresolved rather than forcing a CNIG conclusion.

---

## 15. Framework Boundary

CNIG concerns actual system:

* structure
* relationships
* constraints
* transitions
* authority
* capability
* reachable states
* admissible states

CNIG does not classify the following by themselves:

* fragmented evidence
* inconsistent narratives
* semantic drift in human discussion
* observer disagreement
* loss of reconstructive coherence
* incomplete system understanding
* LLM reasoning failure
* conflicting descriptions

These conditions may affect evidence quality.

They do not become CNIG conditions unless they correspond to, reveal, or produce an actual structural difference in the system.

Examples include:

* one identity reference mapping to different effective principals
* one constraint having materially different effective scope
* two domains applying incompatible governing conditions to a Joint State
* a transition being evaluated against a stale system phase
* an authority path changing through composition

The structural condition—not disagreement about it—is the CNIG object.

---

## 16. Cross-Framework Separation

CNIG must remain independently bounded.

Concepts from another framework must not be imported into CNIG as substitutes for:

* Primitives
* Invariants
* Failure Modes
* system states
* structural evidence
* admissibility conditions

Cross-framework comparison may be appropriate where it is:

* explicit
* non-substitutive
* terminologically precise
* scoped to the distinct contribution of each framework

Compatibility does not imply equivalence.

Coexistence does not authorize ontology merging.

A framework that analyses observers, evidence reconstruction, semantic coherence, pressure signals, or cognitive fracture is not describing the same analytical object as CNIG merely because both concern complex systems.

CNIG remains concerned with structural reachability and admissibility.

---

## 17. Relationship to Engineering Disciplines

CNIG may be used alongside:

* systems architecture
* distributed-systems analysis
* formal methods
* verification
* observability
* policy-as-code
* security engineering
* identity governance
* systems safety
* incident analysis

These disciplines may provide:

* evidence
* state representations
* constraints
* execution records
* authority records
* dependency maps
* transition histories

CNIG does not replace them.

It does not become a “higher” layer that governs their correctness.

It provides a distinct structural framework for examining composition-induced reachability and admissibility.

---

## 18. Implementation Boundary

CNIG is not:

* executable
* a policy engine
* a production validator
* a deployment architecture
* an enforcement system
* a software specification
* a decision authority
* an autonomous control mechanism

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external implementation must not be treated as:

* the canonical form of CNIG
* proof that CNIG guarantees an outcome
* authority to redefine a Primitive, Invariant, or Failure Mode
* evidence that CNIG itself executes or enforces governance

---

## 19. Observation Reading Rule

Observation files should be read as:

* illustrative structural cases
* locally meaningful nodes
* evidence patterns
* examples of relationships between canonical concepts

They should not be read as:

* independent definitions
* exhaustive scenarios
* fixed one-to-one Failure Mode mappings
* mandatory diagnostic sequences
* universal claims

An observation may involve:

* several Primitives
* several Invariants
* more than one provisional Failure Mode
* no established Failure Mode
* unresolved structural evidence

Its role is to contribute a distinct structural example while converging toward the canonical framework.

---

## 20. Anti-Forcing Principle

CNIG should not be forced into:

* every engineering problem
* every unexpected system outcome
* every integration
* every access issue
* every probabilistic system
* every governance disagreement
* every distributed-system failure

CNIG is appropriate where compositional structure is materially necessary to explain the reachable or admissible system state.

Applying CNIG without that condition weakens the framework by turning bounded concepts into generic labels.

Selective non-application preserves analytical precision.

---

## 21. Stability Rule

CNIG remains stable when:

* its canonical terms retain fixed structural meaning
* local correctness remains distinct from global admissibility
* Reachability remains distinct from Admissibility
* Primitives remain distinct from Failure Modes
* Invariants remain structural properties
* observations remain illustrative
* Failure Modes remain evidence-dependent
* implementation remains external
* observer-centred coherence remains outside the ontology

CNIG degrades when:

* every system problem is classified through it
* terms become generic metaphors
* Failure Modes are assigned by keyword similarity
* observations redefine the canon
* structural conditions are replaced by narratives
* implementation objects are treated as canonical concepts
* adjacent ontologies are silently merged into it

---

## 22. Closing Principle

CNIG interpretation must always return to the same structural question:

> What did the composition make reachable, and did the resulting state remain admissible?

The purpose of interpretation is to apply the framework to evidence.

Interpretation itself is not the object of the framework.

---

## 23. Transition to Diagnostic Application

The next layer defines the external methodology used to analyse observational evidence through CNIG.

See:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`
