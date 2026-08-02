# CNIG Overview

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. What CNIG Is

Constraint-Native Infrastructure Governance (CNIG) is a bounded conceptual framework for reasoning about:

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

It provides a bounded structural vocabulary for reasoning about the conditions that make system behaviour possible.

---

## 2. Recognition Signature

CNIG addresses:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* individual components satisfy, or are materially consistent with, their local specifications;
* local configurations, permissions, policies, and transitions may be valid;
* no single local defect sufficiently explains the complete system-level condition;
* but the composition makes a globally unintended or inadmissible State reachable.

The defining distinction is:

> Local correctness does not establish global Admissibility.

The minimum CNIG questions are:

> What did the composition make reachable?

and:

> Did the resulting State remain admissible under the constraints governing the complete composition?

---

## 3. Local Correctness

The phrase **component-correct** identifies the distinctive CNIG problem class.

It does not mean that local correctness may be assumed without evidence.

Local correctness may concern:

* component behaviour;
* configuration;
* interface conformance;
* local authorization;
* local transition validity;
* policy evaluation;
* workflow-stage acceptance;
* local resource effects.

In a completed retrospective analysis, local correctness should be supported.

During prospective or initial analysis, it may remain:

* established;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

Local correctness must not be inferred solely because:

* no error was reported;
* monitoring remained green;
* execution completed;
* a policy existed;
* a reviewer found no obvious defect;
* the system remained available.

Where a direct local defect sufficiently explains the material outcome, that explanation should remain primary.

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

Composition may occur through:

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
* accumulated transitions;
* feedback;
* temporal coordination.

The presence of several components is not sufficient for CNIG applicability.

The composition must materially affect one or more of:

* Reachable State Space;
* Transition Paths;
* Effective Authority;
* Effective Capability;
* Governing Constraints;
* Privilege Surface;
* valid continuation;
* Target-State Admissibility.

---

## 5. State, Transition, and Transition Path

A **State** is a structural configuration of the system within a bounded analysis.

A State may include:

* component configuration;
* versions;
* identities;
* roles;
* permissions;
* authority relationships;
* resources;
* topology;
* dependencies;
* shared state;
* active Governing Constraints;
* temporal phase;
* Effective Authority;
* Effective Capability.

A **Transition** is a structural change from one State to another.

A **Transition Path** is the complete sequence of transitions and Intermediate States connecting a Source State to a Target State.

```text
Source State
    ↓
Transition
    ↓
Intermediate State
    ↓
Transition
    ↓
Target State
```

Every local transition may be valid while the complete path reaches an inadmissible Target State.

CNIG therefore distinguishes:

* local transition validity;
* complete Transition-Path validity;
* Target-State Admissibility.

---

## 6. Reachability

**Reachable State Space** is:

> the complete set of system States that can emerge through component composition.

Reachability concerns structural possibility.

A State may become reachable through:

* direct transitions;
* accumulated transitions;
* service interaction;
* delegation;
* inheritance;
* identity mapping;
* shared-state change;
* changed topology;
* cross-domain integration;
* alternate authority paths;
* Intermediate States;
* downstream capability.

Reachability does not establish that a State is:

* intended;
* represented;
* governed;
* authorized at the global level;
* admissible.

An inadmissible State may still be structurally reachable.

---

## 7. Admissibility

An **Admissible System State** is:

> a reachable State that remains structurally coherent under the constraints governing the composition.

Admissibility may depend on:

* Governing Constraints;
* Governing Intent;
* authority boundaries;
* resource boundaries;
* separation requirements;
* prohibited relationships;
* transition conditions;
* Target-State requirements;
* valid-continuation requirements;
* relevant Invariant-preservation requirements.

A State may be:

* reachable and admissible;
* reachable but inadmissible;
* reachable with Admissibility PROVISIONAL;
* reachable with Admissibility CONFLICTING;
* reachable with Admissibility UNRESOLVED;
* represented but unreachable;
* absent from the Structural Model but structurally reachable.

A State being unexpected, undocumented, unfamiliar, or undesirable does not independently establish inadmissibility.

Inadmissibility requires a supported governing basis.

---

## 8. Reachability Is Not Admissibility

The distinction between Reachability and Admissibility is central to CNIG.

A new reachable State may be:

* intended;
* represented;
* authorized;
* governed;
* admissible.

Reachability expansion is not automatically a failure.

Likewise, absence from a Structural Model does not automatically establish:

* impossibility;
* inadmissibility;
* a canonical Failure Mode.

The analysis must determine:

1. what State or path became reachable;
2. how the composition made it reachable;
3. which Governing Constraints apply;
4. whether the resulting State remains admissible.

---

## 9. The Six Canonical Primitives

CNIG uses six canonical Primitives in the following order.

### 1. Reachable State Space

The complete set of system States that can emerge through component composition.

It concerns structural possibility, not only observed execution history.

### 2. Admissible System State

A reachable State that remains structurally coherent under the constraints governing the composition.

Local correctness does not establish Admissibility.

### 3. Constraint-Native Governance

The implicit or explicit structural constraints that shape:

* system relationships;
* interaction boundaries;
* authority;
* Transition Paths;
* Reachability;
* permissible configurations.

These constraints describe governing structure.

They are not necessarily runtime enforcement mechanisms.

### 4. State Transition Validation

A conceptual reasoning construct for evaluating whether movement between system States:

* preserves structural coherence;
* remains under valid authority;
* respects applicable Governing Constraints;
* preserves relevant Invariants;
* reaches an admissible Target State.

It considers the complete Transition Path.

It is not an execution-time validator.

### 5. Execution vs Governance Separation

The analytical distinction between:

* whether components and local transitions execute correctly;
* whether the complete composition and resulting Target State remain within Governing Intent.

Execution success does not establish governance validity.

### 6. Privilege Surface

The effective Interaction Topology through which composition expands or constrains:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect;
* action paths.

Generic connectivity does not by itself constitute Privilege Surface.

A relationship is material to Privilege Surface only where it affects effective:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

---

## 10. Effective Authority and Effective Capability

### Effective Authority

The complete authority available through the composed relationship structure.

It may include:

* direct assignment;
* inheritance;
* nested membership;
* delegation;
* identity mapping;
* service-held authority;
* token exchange;
* alternative authorization paths;
* transitive relationships.

### Effective Capability

The complete action or system effect reachable through a permission, service, tool, agent, or Transition Path.

Effective Capability may exceed the apparent scope of:

* the initiating permission;
* the initiating identity;
* one service contract;
* one local authorization decision.

Privilege Surface describes the effective topology through which these conditions arise.

---

## 11. The Four Canonical Invariants

CNIG uses four canonical Invariants in the following order.

### 1. Identity Invariant

Preservation of:

* principal identity;
* resource identity;
* Authority Lineage;
* responsibility;
* delegated authority;
* attributable action.

### 2. Stability Invariant

Bounded system deviation under structural variation.

The Invariant may weaken where small compositional changes produce disproportionately large system effects.

### 3. Behavioral Invariant

Preservation of the expected relationship between local component behaviour and the behaviour of the complete composition.

### 4. Structural Invariant

Preservation of coherent and intended relationships between:

* components;
* constraints;
* boundaries;
* authority paths;
* resources;
* transitions;
* Source States;
* Intermediate States;
* Target States;
* reachable and admissible States.

Invariants describe structural properties expected to remain preserved.

They do not:

* create States;
* remove States;
* filter the State space;
* execute transitions;
* authorize States;
* independently establish Admissibility;
* automatically establish a Failure Mode.

---

## 12. Admissibility Is Not Stability

Admissibility and Stability must remain separate.

### Admissibility

Concerns whether a reachable State remains coherent under Governing Constraints.

### Stability

Concerns whether system deviation remains bounded under structural variation.

A State may be admissible while the system remains sensitive to:

* topology changes;
* timing;
* concurrency;
* dependency changes;
* authority changes;
* future transitions.

An Admissible System State must not be defined automatically as a stable State.

---

## 13. The Ten Canonical Failure Modes

CNIG defines ten canonical Failure Modes in the following order:

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

Failure Modes describe evidence-supported structural conditions.

They are not:

* monitoring alerts;
* incident severities;
* operational labels;
* symptoms;
* implementation patterns;
* automatic diagnoses;
* observer-centred coherence conditions.

---

## 14. Failure Mode Discipline

A Failure Mode is not established merely because:

* a system is complex;
* an outcome is unexpected;
* a State is newly reachable;
* governance is imperfect;
* connectivity increased;
* execution varies;
* evidence is fragmented;
* observers disagree;
* an observation resembles an example file;
* a Failure Mode name resembles the symptom.

Failure Mode attribution requires evidence of:

1. the observed system effect;
2. the relevant Source State;
3. the complete Transition Path;
4. the Target State;
5. the Structural Cause;
6. the applicable Governing Constraints;
7. the Admissibility Condition;
8. the complete defining conditions of the proposed Failure Mode.

Where evidence is insufficient, preserve:

* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED;
* NOT SUPPORTED.

CNIG applicability does not require that a Failure Mode be established.

---

## 15. Diagnostic States

CNIG analysis should distinguish conclusion status explicitly.

### OBSERVED

Directly supported by available evidence.

### INFERRED

Derived from supported structural relationships.

### CANONICAL

Defined by the governing CNIG framework files.

### PROVISIONAL

Plausible, but one or more required conditions remain unsupported.

### CONFLICTING

Available evidence or canonical sources support incompatible conclusions.

### UNRESOLVED

The available evidence does not support a reliable determination.

UNRESOLVED is a valid analytical result.

---

## 16. Prospective and Retrospective Use

The phrase **prior to execution** describes CNIG’s analytical orientation.

CNIG reasons about structural possibility independently of whether every State has already been executed or observed.

This does not limit CNIG to design-time analysis.

### Prospective use

CNIG may examine:

* a proposed integration;
* a new authority relationship;
* a workflow change;
* a topology change;
* a migration;
* a failover design;
* a cross-domain mapping;
* a new agent-to-tool path;
* a proposed Target State.

Prospective analysis identifies structural possibility.

It does not prove that a State will occur.

### Retrospective use

Execution evidence may establish:

* that a State was reachable;
* that a Transition Path existed;
* that authority was effective;
* that an Intermediate State enabled a later transition;
* that a resource effect occurred.

Execution can reveal Reachability.

Execution does not independently establish:

* local correctness;
* structural causation;
* Governing Intent;
* Admissibility;
* a canonical Failure Mode.

---

## 17. Relationship to Evidence

CNIG does not generate evidence.

Evidence may come from:

* configuration records;
* identity and role records;
* permission records;
* policies;
* authority and delegation records;
* system diagrams;
* dependency maps;
* execution logs;
* State-transition history;
* resource-change history;
* version records;
* timing and propagation records;
* approval records;
* observed system outcomes;
* governing documentation.

Every practical CNIG analysis remains bounded by:

* scope;
* available evidence;
* assumptions;
* included components;
* represented relationships;
* time or phase;
* model completeness.

A complete-looking diagram or model is not proof that the effective system has been represented completely.

---

## 18. What CNIG Is Not

CNIG is not:

* a runtime system;
* a software architecture;
* a policy engine;
* an enforcement mechanism;
* a monitoring framework;
* an incident-management taxonomy;
* a compliance framework;
* a deployment framework;
* a certification mechanism;
* an executable specification;
* a formal verification system;
* a production decision authority;
* an autonomous controller;
* a theory of observer disagreement;
* a framework for semantic or reconstructive coherence.

CNIG does not:

* execute actions;
* approve transitions;
* reject transitions;
* enforce constraints;
* block system changes;
* prescribe remediation;
* control system behaviour;
* guarantee outcomes.

---

## 19. Observer Boundary

CNIG concerns actual system:

* States;
* relationships;
* constraints;
* identity;
* authority;
* capability;
* topology;
* Transition Paths;
* Reachability;
* Admissibility.

The following are not CNIG conditions by themselves:

* observer disagreement;
* fragmented evidence;
* inconsistent narratives;
* semantic incoherence;
* incomplete reconstruction;
* loss of unified understanding;
* evaluator disagreement;
* LLM reasoning error.

Those conditions may affect evidence quality.

They become relevant to CNIG only where evidence establishes an actual structural difference involving:

* identity;
* authority;
* constraints;
* State;
* temporal phase;
* Transition Path;
* Reachability;
* Admissibility.

The condition in the system—not the observer’s difficulty reconstructing it—is CNIG’s analytical object.

---

## 20. Relationship to Existing Disciplines

CNIG may be used alongside:

* systems architecture;
* distributed-systems analysis;
* formal methods;
* verification;
* testing;
* observability;
* policy-as-code;
* security engineering;
* identity governance;
* systems safety;
* incident analysis;
* governance engineering.

These disciplines may provide:

* evidence;
* Structural Models;
* constraints;
* execution records;
* authority records;
* topology;
* dependency maps;
* transition histories;
* system-level properties.

CNIG does not replace or rank above them.

It provides a distinct structural framework for reasoning about composition-induced Reachability and Admissibility.

---

## 21. Contribution Boundary

CNIG does not claim to originate the individual concepts of:

* Reachability;
* Admissibility;
* composition;
* invariants;
* governance;
* authority;
* local and global system reasoning.

Its contribution is their bounded integration for a specific problem class:

> systems in which locally correct components compose into a globally unintended or inadmissible reachable State.

CNIG provides:

* a defined problem class;
* six canonical Primitives;
* four canonical Invariants;
* ten canonical Failure Modes;
* a structural distinction between execution correctness and governance validity;
* a bounded, non-operational basis for evidence-grounded diagnostic analysis.

---

## 22. Non-Operational and External-Application Boundary

CNIG is conceptual and non-operational.

Observation files may illustrate its concepts.

External applications may reference or apply them, but any implementation remains outside CNIG and does not alter the canonical framework.

An external implementation must not be represented as:

* CNIG itself;
* the canonical implementation of CNIG;
* an official CNIG runtime;
* a canonical CNIG decision engine;
* proof that CNIG guarantees correctness;
* authority to redefine a Primitive, Invariant, or Failure Mode;
* authority to approve, reject, or execute system changes;
* evidence that CNIG itself enforces governance.

Applying CNIG concepts externally creates an external application.

It does not make the conceptual framework operational.

---

## 23. Repository Navigation

### Recognition and entry surfaces

* `README.md` — primary repository recognition surface
* `START_HERE.md` — reader entry point and navigation
* `CNIG_OVERVIEW.md` — non-authoritative framework overview
* `00_CANONICAL_IDENTITY.md` — canonical identity and attribution
* `01_ORIENTATION_LAYER.md` — initial applicability orientation
* `PROBLEM_CLASS.md` — definitive problem-class boundary

### Canonical ontology

* `02_CONCEPTUAL_CORE.md` — canonical conceptual core
* `03_PRIMITIVES.md` — six canonical Primitives
* `04_FAILURE_MODES.md` — ten canonical Failure Modes
* `GLOSSARY.md` — canonical terminology and four Invariants

### Analytical and representational layers

* `05_CHECKLISTS.md` — analytical checklists
* `06_DECISION_TEMPLATES.md` — analytical decision-record templates
* `07_STATE_MODEL.md` — conceptual State and Transition model
* `08_ARCHITECTURE_PATTERNS.md` — non-canonical structural composition patterns
* `09_DOMAIN_INSTANCES.md` — non-canonical domain illustrations

### Limits and interpretation

* `10_SYSTEM_LIMITS.md` — applicability, evidence, modelling, attribution, and implementation limits
* `11_INTERPRETATION_GUIDE.md` — ontology and interpretation boundaries
* `12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md` — external diagnostic methodology

### Conceptual assets

* `ASSETS-STATE-SPACE-DIAGRAM.md`
* `ASSETS-INVARIANT-FILTER.md`

The second filename is retained for repository continuity, but the asset defines an Invariant evaluation overlay. Invariants do not filter, create, remove, or authorize States.

### Observation files

`OBS_*` files provide non-canonical illustrative structural cases.

They may illustrate canonical concepts.

They do not override or redefine them.

---

## 24. Authority Boundary

Repository files do not carry equal definitional authority.

The following are navigation or overview surfaces and do not independently redefine CNIG:

* `README.md`
* `START_HERE.md`
* `CNIG_OVERVIEW.md`
* `01_ORIENTATION_LAYER.md`

Where definitions conflict, use the following order:

1. `00_CANONICAL_IDENTITY.md`
2. `PROBLEM_CLASS.md`
3. `02_CONCEPTUAL_CORE.md`
4. `03_PRIMITIVES.md`
5. `04_FAILURE_MODES.md`
6. `GLOSSARY.md`
7. `10_SYSTEM_LIMITS.md`
8. `11_INTERPRETATION_GUIDE.md`
9. `12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`
10. analytical and representational layers
11. conceptual assets
12. observation files

The analytical and representational layers include:

* `05_CHECKLISTS.md`
* `06_DECISION_TEMPLATES.md`
* `07_STATE_MODEL.md`
* `08_ARCHITECTURE_PATTERNS.md`
* `09_DOMAIN_INSTANCES.md`

A lower-authority layer may:

* illustrate;
* organize;
* contextualize;
* represent;
* or apply

a canonical concept.

It may not silently:

* rename it;
* broaden it;
* narrow it;
* merge it;
* reorder it;
* replace it;
* import another framework’s ontology into it.

---

## 25. Framework Stability

CNIG remains coherent when:

* the problem class remains bounded;
* the composed system remains the primary analytical object;
* Reachability remains distinct from Admissibility;
* Admissibility remains distinct from Stability;
* local correctness remains distinct from global Admissibility;
* a State remains distinct from a Transition;
* local transition validity remains distinct from complete Transition-Path validity;
* Privilege Surface remains limited to topology affecting effective interaction, access, authority, capability, control, or resource effect;
* Invariants remain distinct from Primitives and Failure Modes;
* Failure Mode attribution remains evidence-dependent;
* observer understanding remains distinct from actual system structure;
* implementation and action remain external.

CNIG degrades when:

* it becomes a universal label for complex-system problems;
* Failure Modes are assigned through keyword similarity;
* generic connectivity becomes Privilege Surface;
* every new reachable State becomes a Failure Mode;
* observer-centred coherence replaces system structure;
* external implementations are treated as canonical CNIG;
* canonical concepts are silently renamed, merged, broadened, or reordered.

---

## 26. Closing Principle

A system may be composed entirely of locally correct parts while still making a globally unintended or inadmissible State reachable.

The question is not only what the system executed.

The question is what its composition made possible.
