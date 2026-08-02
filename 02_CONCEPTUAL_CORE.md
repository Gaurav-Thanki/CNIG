# CNIG Conceptual Core

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Core Definition

Constraint-Native Infrastructure Governance (CNIG) is a conceptual framework for reasoning about:

> admissible system states within Reachable State Space under composition constraints prior to execution.

CNIG examines how the structure of a composed system determines:

* what States can become reachable;
* which reachable States remain admissible;
* how locally valid transitions combine into system-level outcomes;
* how component relationships alter Effective Authority and Effective Capability;
* whether Governing Constraints remain effective across composition;
* whether relevant structural Invariants remain preserved.

Its primary analytical object is:

> the composed system and the States made structurally reachable through its relationships.

CNIG does not define system behaviour.

It provides a bounded vocabulary and structural framework for reasoning about the conditions that make system behaviour possible.

---

## 2. The Problem Class

CNIG addresses:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* individual components satisfy their local specifications;
* local configurations, permissions, policies, or transitions may be valid;
* no single component fault explains the complete outcome;
* but the composition makes a globally unintended or inadmissible State reachable.

The distinctive CNIG condition is not simply that:

* the system is distributed;
* the system is complex;
* components interact;
* an outcome is unexpected;
* or a failure is difficult to diagnose.

The distinctive condition is:

> local correctness exists or is materially relevant, but does not establish the Admissibility of the resulting composed State.

CNIG therefore distinguishes between:

* component correctness;
* Transition-Path validity;
* structural Reachability;
* and global Admissibility.

---

## 3. Primary Structural Question

Conventional component analysis commonly begins with:

> Is this component correct?

CNIG introduces an additional system-level question:

> What system States become reachable when these components interact?

That question must be followed by:

> Which of those reachable States remain admissible under the constraints governing the complete composition?

The two questions are distinct.

A State may be:

* reachable and admissible;
* reachable but inadmissible;
* represented but unreachable;
* reachable but absent from the represented Structural Model;
* unresolved because the applicable Governing Constraints are incomplete or conflicting.

Reachability does not imply Admissibility.

---

## 4. Composition

Within CNIG, **Composition** is the structural combination of:

* components;
* relationships;
* identities;
* authority;
* permissions;
* constraints;
* resources;
* transitions;
* services;
* tools;
* agents;
* workflows;
* infrastructure boundaries;
* governance domains.

Composition includes more than physical or logical connection.

A component may participate in the composed system through:

* direct invocation;
* delegation;
* inheritance;
* identity mapping;
* shared state;
* resource dependency;
* policy interaction;
* workflow sequencing;
* downstream service execution;
* cross-domain integration;
* feedback;
* accumulated transitions.

Properties that hold within individual component boundaries do not automatically remain preserved across the complete composition.

---

## 5. Source State, Transition Path, and Target State

CNIG analyses system movement through structural States.

### Source State

The structural configuration from which a transition or transition sequence begins.

A Source State may include:

* component versions;
* configuration;
* identity relationships;
* authority;
* permissions;
* resource membership;
* topology;
* dependencies;
* active constraints;
* temporal phase;
* governing boundaries.

### Intermediate State

A State reached between the Source State and the final Target State.

An Intermediate State may:

* change later transition preconditions;
* introduce authority;
* alter shared resources;
* activate a dependency;
* expose a downstream capability;
* expand later Reachability;
* weaken a Governing Constraint;
* make another transition possible.

### Transition Path

The complete sequence connecting the Source State to the Target State.

A Transition Path may contain several locally accepted transitions.

### Target State

The resulting structural configuration reached through the complete Transition Path.

Every local transition may be valid while the complete path reaches an inadmissible Target State.

CNIG therefore distinguishes:

* local transition validity;
* complete Transition-Path validity;
* Target-State Admissibility.

---

## 6. Reachable State Space

**Reachable State Space** is the complete set of system States that can emerge through component composition.

It concerns structural possibility.

Reachability may arise through:

* direct transitions;
* accumulated transitions;
* alternative paths;
* inherited relationships;
* delegated authority;
* changed topology;
* service-mediated effects;
* cross-domain mappings;
* shared resources;
* Intermediate States;
* downstream capability.

Reachable State Space is not limited to:

* States already observed;
* States documented in an architecture;
* States one component can produce independently;
* States that were deliberately intended.

A State may be structurally reachable while remaining absent from the represented Structural Model.

---

## 7. Admissible System State

An **Admissible System State** is a reachable State that remains structurally coherent under the constraints governing the composition.

Admissibility may depend on:

* authority boundaries;
* separation requirements;
* prohibited relationships;
* Target-State conditions;
* resource boundaries;
* valid-continuation requirements;
* transition conditions;
* relevant Invariant-preservation requirements;
* Governing Intent.

Admissibility is not established merely by:

* successful execution;
* component health;
* policy presence;
* authentication success;
* authorization success;
* local validation;
* absence of an alert;
* continued system operation.

Admissibility requires a supported structural basis.

It is not an observer preference or narrative judgement.

---

## 8. Constraint-Native Governance

**Constraint-Native Governance** describes the implicit or explicit structural constraints that shape:

* component relationships;
* system boundaries;
* authority;
* Transition Paths;
* Reachability;
* permissible configurations;
* Admissibility.

These constraints may be represented through:

* policy;
* architecture;
* authority definitions;
* separation rules;
* resource boundaries;
* trust conditions;
* transition requirements;
* exclusions;
* governing agreements.

Constraint-Native Governance is not necessarily implemented as a runtime enforcement mechanism.

A Governing Constraint may remain:

* documented;
* configured;
* named;
* formally present;

while losing effective constraint authority over the complete composition.

CNIG therefore distinguishes between:

* declared governance;
* implemented governance;
* effective governing structure;
* observed execution;
* resulting system State.

---

## 9. Execution vs Governance Separation

CNIG distinguishes two independent analytical properties.

### Execution correctness

Whether a component, action, service, tool, or local transition behaves according to its specification or local acceptance conditions.

### Governance validity

Whether the complete composition and resulting Target State remain within Governing Intent.

A system may exhibit:

* correct execution and admissible outcome;
* correct execution and inadmissible outcome;
* incorrect execution and inadmissible outcome;
* incorrect execution whose effects remain locally bounded.

Execution success does not establish governance validity.

Governance declarations do not establish that their constraints remain effective across the composition.

---

## 10. Relationship to Execution Evidence

The phrase **prior to execution** describes CNIG’s analytical orientation.

CNIG reasons about structural possibility independently of whether every State has already been executed or observed.

It does not mean that CNIG can only be used before runtime.

Observed execution may provide evidence that:

* a State was reachable;
* a Transition Path existed;
* an authority path was effective;
* a resource was affected;
* a Governing Constraint did not shape the complete outcome;
* an Intermediate State enabled a later transition.

CNIG may therefore be applied:

* prospectively, to reason about structural possibility;
* retrospectively, to analyse evidence of an executed Transition Path.

Execution can reveal the Reachable State Space.

Execution does not define Admissibility.

---

## 11. State Transition Validation

**State Transition Validation** is a conceptual reasoning construct for evaluating whether movement between system States:

* preserves relevant structural relationships;
* remains under valid authority;
* respects Governing Constraints;
* preserves applicable Invariants;
* reaches an admissible Target State.

It is not:

* an execution-time validator;
* an API validation routine;
* a pipeline gate;
* a policy engine;
* a software service;
* a production decision mechanism.

A local system may validate one transition correctly while no component validates the complete Transition Path or Target State.

---

## 12. Privilege Surface

**Privilege Surface** is the effective Interaction Topology through which composition expands or constrains:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect;
* action paths.

Privilege Surface may include relationships between:

* principals;
* roles;
* identities;
* services;
* agents;
* tools;
* APIs;
* delegated authority;
* downstream services;
* protected resources.

Generic connectivity is not automatically Privilege Surface.

A relationship belongs to the Privilege Surface where it materially affects effective:

* authority;
* capability;
* access;
* control;
* or resource effect.

Privilege Surface is a structural concept.

It is not an access-control product or security mechanism.

---

## 13. Invariants

CNIG uses four canonical Invariants:

1. Identity Invariant
2. Stability Invariant
3. Behavioral Invariant
4. Structural Invariant

Invariants describe system properties expected to remain preserved across composition and transition.

They are not:

* observer interpretations;
* semantic-coherence measures;
* runtime checks;
* enforcement rules;
* automatic pass-or-fail controls.

An Invariant may remain preserved locally while weakening across the complete composition.

Invariant weakening may contribute evidence to an Admissibility assessment.

It does not automatically establish a Failure Mode.

Canonical Invariant definitions are governed by:

`GLOSSARY.md`

---

## 14. Failure Modes

CNIG uses ten canonical Failure Modes:

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

Failure Modes describe evidence-supported structural conditions in which composition produces or exposes inadmissibility.

They are not:

* incidents;
* alerts;
* symptoms;
* severities;
* root-cause labels;
* automatic diagnoses;
* observer-centred coherence conditions.

A Failure Mode may be attributed only after its canonical defining conditions are supported.

Canonical Failure Mode definitions are governed by:

`04_FAILURE_MODES.md`

---

## 15. Structural Model

A **Structural Model** is the represented account of the system’s relevant:

* components;
* relationships;
* boundaries;
* constraints;
* authority paths;
* Source States;
* Intermediate States;
* Target States;
* Transition Paths;
* reachable States;
* Admissibility conditions.

The represented Structural Model may differ from the effective composition.

For example:

* a relationship may exist but remain undocumented;
* an authority path may emerge through delegation;
* an Intermediate State may enable an unrepresented transition;
* a permission may acquire wider downstream effects;
* separate domains may jointly reach a State neither models completely.

CNIG reasons about the effective structure.

The Structural Model is evidence about that structure, not an automatic guarantee of completeness.

---

## 16. Actual Structure vs Observer Understanding

CNIG concerns actual system:

* States;
* relationships;
* constraints;
* mappings;
* authority;
* Transition Paths;
* Reachability;
* Admissibility.

CNIG does not classify, by themselves:

* observer disagreement;
* fragmented evidence;
* inconsistent narratives;
* incomplete understanding;
* semantic incoherence;
* reconstructive-coherence loss;
* LLM reasoning error;
* difficulty combining distributed observations.

Those conditions may affect evidence quality.

They become relevant to CNIG only where evidence establishes an actual structural condition, such as:

* non-equivalent identity mappings;
* different effective structural referents;
* incompatible Governing Constraints;
* different system phases;
* changed authority paths;
* changed Transition Paths;
* altered Reachability;
* altered Admissibility.

The system condition—not disagreement about it—is CNIG’s analytical object.

---

## 17. Relationship to Existing Disciplines

CNIG may be used alongside:

* systems architecture;
* distributed-systems analysis;
* formal methods;
* verification;
* observability;
* policy-as-code;
* security engineering;
* identity governance;
* systems safety;
* incident analysis;
* governance engineering.

These disciplines may provide:

* evidence;
* execution history;
* state representations;
* constraints;
* authority records;
* topology;
* dependency maps;
* Transition Paths.

CNIG does not replace them.

It does not operate as a secondary or superior layer over them.

It provides a distinct structural framework for examining composition-induced Reachability and Admissibility.

---

## 18. Non-Operational Boundary

CNIG is not:

* executable;
* a runtime system;
* a policy engine;
* an enforcement mechanism;
* a deployment architecture;
* a formal proof system;
* a production validator;
* a remediation system;
* an autonomous controller;
* a decision authority.

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external implementation must not be treated as:

* CNIG itself;
* the canonical implementation of CNIG;
* proof that CNIG guarantees correctness;
* authority to redefine a Primitive, Invariant, or Failure Mode;
* evidence that CNIG executes or enforces governance.

---

## 19. Canonical Relationships

The core CNIG relationship can be represented as:

```text
System Composition
        ↓
Available Transition Paths
        ↓
Reachable State Space
        ↓
Target State
        ↓
Governing Constraints + Invariant Evaluation
        ↓
Admissibility Assessment
        ↓
Evidence-dependent Failure Mode Attribution,
where supported
```

The concepts must remain distinct.

In particular:

* local correctness is not global Admissibility;
* Reachability is not Admissibility;
* Admissibility is not Stability;
* connectivity is not Privilege Surface;
* Invariant weakening is not automatically a Failure Mode;
* execution success is not governance validity;
* an unrepresented State is not automatically inadmissible;
* observer disagreement is not Reference Drift;
* delayed awareness is not Phase Desynchronization.

---

## 20. Stability Rule

CNIG remains conceptually stable when:

* its problem class remains bounded;
* its analytical object remains the composed system;
* Reachability remains distinct from Admissibility;
* local correctness remains distinct from global Admissibility;
* system structure remains distinct from observer understanding;
* Primitives, Invariants, and Failure Modes remain separate;
* Failure Mode attribution remains evidence-dependent;
* implementation remains external;
* adjacent ontologies remain separate.

CNIG degrades when:

* every complex-system problem is classified through it;
* terms become generic metaphors;
* Failure Modes are assigned through keyword similarity;
* observer-centred coherence replaces system structure;
* external implementations are treated as canonical CNIG;
* canonical concepts are silently renamed, merged, broadened, or reordered.

---

## 21. Transition to Primitives

The next canonical layer defines the six CNIG Primitives in detail.

See:

`03_PRIMITIVES.md`
