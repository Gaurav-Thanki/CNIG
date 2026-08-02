# Constraint-Native Infrastructure Governance (CNIG)

**Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki**

A conceptual framework for reasoning about admissible system states within Reachable State Space under composition constraints prior to execution.

---

## 1. Recognition Signature

CNIG addresses:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* components satisfy their local specifications;
* local configurations, permissions, policies, and transitions may be valid;
* no single component fault explains the complete outcome;
* but the composition makes a globally unintended or inadmissible State reachable.

The defining CNIG distinction is:

> Local correctness does not establish global admissibility.

The primary question is not only:

> Is each component correct?

It is:

> What system States become reachable when correct components interact, and which of those States remain admissible?

---

## 2. Core Definition

Constraint-Native Infrastructure Governance is a bounded conceptual framework concerned with how system composition shapes:

* Reachable State Space
* Admissible System States
* Transition Paths
* Governing Constraints
* Effective Authority
* Effective Capability
* Privilege Surface
* preservation of structural Invariants

CNIG reasons at the level of the composed system.

Its primary analytical object is the actual system structure and the States made reachable through component relationships.

CNIG does not treat observer understanding, evidence reconstruction, semantic coherence, or narrative agreement as substitutes for system structure.

---

## 3. The Problem CNIG Addresses

Distributed and interconnected systems are commonly evaluated through local boundaries.

A component may confirm that:

* its input is valid;
* its action is permitted;
* its configuration is correct;
* its transition completed;
* its output satisfies its local contract;
* its health checks remain successful.

The global outcome may still depend on relationships that no component represents or evaluates in full.

For example:

* valid identity assignments may aggregate into broader Effective Authority;
* an unchanged permission may acquire wider downstream capability;
* individually valid pipeline stages may reach an unevaluated Target State;
* correct services may create new Transition Paths through topology changes;
* separately governed systems may reach a Joint State neither governs completely;
* declared governance may remain visible while losing effective constraint authority.

CNIG addresses this structural distance between:

* local component correctness;
* system-level Reachability;
* and global Admissibility.

---

## 4. Reachability and Admissibility

### Reachability

Reachability concerns what the current composition makes structurally possible.

A State may become reachable through:

* direct transitions
* accumulated transitions
* service interaction
* inheritance
* delegation
* identity mapping
* shared state
* workflow progression
* cross-domain integration
* changed Interaction Topology
* downstream effects

Reachability does not establish that the State was intended, represented, or admissible.

### Admissibility

Admissibility concerns whether a reachable State remains structurally coherent under the constraints governing the composition.

A State may be:

* reachable and admissible;
* reachable but inadmissible;
* represented but unreachable;
* reachable but absent from the represented Structural Model;
* unresolved because governing conditions are incomplete or conflicting.

The gap between Reachability and Admissibility is central to CNIG.

---

## 5. Canonical Primitives

CNIG uses six canonical Primitives in the following order.

### 1. Reachable State Space

The complete set of system States that can emerge through component composition.

It describes structural possibility, not only observed execution history.

### 2. Admissible System State

A reachable State that remains structurally coherent under the constraints governing the composition.

Local correctness does not establish Admissibility.

### 3. Constraint-Native Governance

The implicit or explicit structural constraints that shape:

* system relationships
* authority
* Transition Paths
* interaction boundaries
* Reachability
* permissible configurations

These constraints describe governing structure.

They are not necessarily runtime enforcement mechanisms.

### 4. State Transition Validation

A conceptual reasoning construct for evaluating whether movement between system States preserves structural coherence and remains within the admissible State space.

It considers the complete Transition Path, not only one locally accepted step.

### 5. Execution vs Governance Separation

The analytical distinction between:

* whether components and transitions execute correctly;
* whether the resulting composed State remains within Governing Intent.

Execution success does not establish governance validity.

### 6. Privilege Surface

The effective Interaction Topology through which composition expands or constrains:

* interaction
* access
* authority
* capability
* control
* resource effect
* action paths

Generic connectivity does not by itself constitute Privilege Surface.

The relationship must materially affect effective capability or authority.

---

## 6. Canonical Invariants

CNIG uses four canonical Invariants.

Invariants describe structural properties expected to remain preserved across composition and transition.

They are not:

* observer interpretations
* semantic-coherence measures
* enforcement rules
* runtime checks
* automatic pass-or-fail controls

### Identity Invariant

Preservation of:

* principal identity
* resource identity
* Authority Lineage
* responsibility
* delegated authority
* attributable action

### Stability Invariant

Bounded system deviation under structural variation.

The Invariant may weaken where small compositional changes produce disproportionately large system effects.

### Behavioral Invariant

Preservation of the expected relationship between local component behaviour and the behaviour of the complete composition.

### Structural Invariant

Preservation of coherent and intended relationships between:

* components
* constraints
* boundaries
* authority paths
* resources
* transitions
* Source States
* Intermediate States
* Target States
* reachable and admissible States

---

## 7. Canonical Failure Modes

CNIG defines ten canonical Failure Modes in the following order.

### 1. Governance Capture

Declared governing constraints remain present but lose effective constraint authority over the complete Reachable State Space.

### 2. Reference Drift

A shared structural reference resolves to non-equivalent effective objects, States, constraints, identities, boundaries, resources, or authority conditions across the composition.

Reference Drift concerns actual structural non-equivalence.

It is not observer disagreement.

### 3. Constitutional Fragmentation

Locally coherent governance regimes fail to compose into one coherent Admissibility structure for shared or Joint States.

### 4. Invariant Overconstraint

Composed constraints restrict the admissible State space beyond Governing Intent, eliminating States or transitions intended to remain valid.

### 5. Recursive Governance Instability

Governance validity depends on another governance determination that ultimately depends on the original determination.

No stable, non-circular basis resolves Admissibility.

### 6. Implicit Reachability Expansion Failure

Composition expands Reachable State Space beyond the represented Structural Model without deliberate acknowledgement, and the resulting State or path conflicts with Governing Intent.

### 7. Stochastic Drift

Materially equivalent Source States and transition conditions produce divergent system-level outcomes because variability emerges through composition.

### 8. Phase Desynchronization

A transition and the structural State, authority, constraints, topology, or governance conditions applicable to it belong to different effective temporal phases.

Delayed observer awareness is not Phase Desynchronization.

### 9. Privilege Surface Expansion Failure

Composition creates or enlarges an effective interaction, access, authority, capability, or control path beyond intended structural boundaries.

### 10. Null State Boundary Violation

The composed system reaches a State from which no admissible outgoing transition exists.

Technically executable transitions may remain, but none preserves Admissibility.

---

## 8. Failure-Mode Discipline

A CNIG Failure Mode is not established merely because:

* a system is complex;
* an outcome is unexpected;
* a new State is reachable;
* governance is imperfect;
* execution varies;
* evidence is fragmented;
* observers disagree;
* an observation resembles an example file.

Failure Mode attribution requires evidence of:

1. the observed system effect;
2. the relevant Source State;
3. the complete Transition Path;
4. the composition relationship that made the outcome reachable;
5. the applicable Governing Constraints;
6. the Admissibility Condition;
7. the defining conditions of the proposed Failure Mode.

Where evidence is insufficient, the correct result is:

* **PROVISIONAL**
* **CONFLICTING**
* or **UNRESOLVED**

---

## 9. What CNIG Is Not

CNIG is not:

* a runtime system
* a software architecture
* a policy engine
* an enforcement mechanism
* a monitoring framework
* an incident-management taxonomy
* a compliance framework
* a deployment framework
* a certification mechanism
* an executable specification
* a formal verification system
* a production decision authority
* an autonomous controller
* a theory of observer disagreement
* a framework for semantic or reconstructive coherence

CNIG does not execute, approve, enforce, remediate, or guarantee system changes.

---

## 10. Non-Operational Boundary

CNIG is conceptual and non-operational.

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external implementation must not be represented as:

* CNIG itself;
* the canonical implementation of CNIG;
* proof that CNIG guarantees correctness;
* authority to redefine a Primitive, Invariant, or Failure Mode;
* evidence that CNIG executes or enforces governance.

Observation files may illustrate CNIG concepts.

They do not authorize operational action.

---

## 11. Framework Boundary

CNIG concerns actual system:

* structure
* relationships
* constraints
* identity
* authority
* capability
* Source States
* Intermediate States
* Target States
* Transition Paths
* Reachability
* Admissibility

The following conditions are not CNIG Failure Modes by themselves:

* fragmented evidence
* observer disagreement
* conflicting narratives
* incomplete understanding
* semantic inconsistency
* loss of reconstructive coherence
* LLM reasoning failure
* difficulty combining distributed observations

Those conditions may affect evidence quality.

They become relevant to CNIG only where evidence establishes an actual structural difference in the system, such as:

* non-equivalent identity mappings;
* different effective authority;
* different structural referents;
* incompatible governing constraints;
* different temporal phases;
* different Source States;
* changed Transition Paths;
* changed Reachability or Admissibility.

The condition in the system—not the observer’s difficulty understanding it—is CNIG’s analytical object.

---

## 12. Relationship to Existing Disciplines

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
* governance engineering

These disciplines may provide:

* evidence
* system models
* constraints
* execution records
* authority records
* topology
* dependency maps
* transition histories

CNIG does not replace them.

It provides a distinct structural framework for reasoning about composition-induced Reachability and Admissibility.

It does not operate “above” those disciplines or govern their correctness.

---

## 13. Contribution Boundary

CNIG does not claim to originate the individual concepts of:

* Reachability
* Admissibility
* composition
* invariants
* governance
* authority
* local and global system reasoning

Its contribution is their bounded integration for a specific problem class:

> systems in which locally correct components compose into a globally unintended or inadmissible reachable State.

CNIG provides:

* a defined problem class;
* a canonical set of Primitives;
* a canonical set of Invariants;
* a canonical Failure Mode taxonomy;
* a structural distinction between execution correctness and governance validity;
* a non-operational methodology for evidence-grounded diagnostic interpretation.

---

## 14. How to Read This Repository

Use the following canonical sequence.

### Framework identity

`00_CANONICAL_IDENTITY.md`

Defines the canonical framework name, authorship, and attribution.

### Orientation

`START_HERE.md`

Provides the reader entry point and repository navigation.

### Problem class

`PROBLEM_CLASS.md`

Defines the precise condition CNIG addresses and where it should not be applied.

### Conceptual core

`02_CONCEPTUAL_CORE.md`

Defines the canonical framework scope and primary structural distinction.

### Primitives

`03_PRIMITIVES.md`

Defines the six canonical Primitives.

### Failure Modes

`04_FAILURE_MODES.md`

Defines the ten canonical Failure Modes and their distinctions.

### System limits

`10_SYSTEM_LIMITS.md`

Defines the limits of applicability, evidence, modelling, attribution, and implementation claims.

### Interpretation boundary

`11_INTERPRETATION_GUIDE.md`

Defines how CNIG concepts should be read without ontology drift.

### Diagnostic methodology

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

Defines the external methodology used to analyse observational evidence through CNIG.

CNIG itself remains a conceptual framework, not a methodology.

### Glossary

`GLOSSARY.md`

Defines canonical terminology and the four Invariants.

### Conceptual assets

* `ASSETS-STATE-SPACE-DIAGRAM.md`
* `ASSETS-INVARIANT-FILTER.md`

These illustrate canonical distinctions without creating new ontology.

### Observations

`OBS_*` files provide non-canonical illustrative structural cases.

They may contribute evidence patterns and graph relationships.

They do not override canonical definitions.

---

## 15. Canonical Authority Rule

CNIG files do not carry equal definitional authority.

Where files conflict, use the following order:

1. `00_CANONICAL_IDENTITY.md`
2. `PROBLEM_CLASS.md`
3. `02_CONCEPTUAL_CORE.md`
4. `03_PRIMITIVES.md`
5. `04_FAILURE_MODES.md`
6. `GLOSSARY.md`
7. `10_SYSTEM_LIMITS.md`
8. `11_INTERPRETATION_GUIDE.md`
9. `12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`
10. conceptual assets
11. observation files

Observation wording must not redefine the canonical framework.

External applications must not redefine it either.

---

## 16. Minimal Recognition Test

A problem may warrant CNIG analysis where all of the following are materially relevant:

* several components or domains participate in the outcome;
* local correctness alone does not explain the result;
* composition changes Reachability, authority, capability, constraints, or Transition Paths;
* a Target State may be outside Governing Intent;
* the structural cause cannot be reduced adequately to one component boundary.

The minimum CNIG question is:

> What did the composition make reachable?

The necessary second question is:

> Did the resulting State remain admissible?

---

## 17. Canonical Attribution

Use the following exact attribution:

> **Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki**

The canonical names and ordering of the six Primitives, four Invariants, and ten Failure Modes must remain stable.

Repository examples, external analysis, and external applications may reference these concepts.

They may not silently rename, broaden, merge, substitute, or replace them.

---

## 18. Closing Principle

A system may be composed entirely of locally correct parts while still making a globally unintended or inadmissible State reachable.

The question is not only what the system executed.

The question is what its composition made possible.
