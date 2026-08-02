# CNIG Structural Composition Patterns

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer describes recurring structural patterns that may appear in composed systems examined through CNIG.

The patterns help organize evidence concerning:

* component relationships;
* coupling;
* Governing Constraints;
* Reachable State Space;
* authority and capability;
* Transition Paths;
* Invariant preservation;
* Target-State Admissibility.

They are descriptive analytical groupings.

They are not additional:

* Primitives;
* Invariants;
* Failure Modes;
* system types;
* architecture requirements;
* implementation patterns.

The patterns do not extend or redefine the canonical CNIG ontology.

---

## 2. Nature of the Patterns

CNIG structural composition patterns describe recurring arrangements or changes in actual system structure.

They may concern:

* relationships;
* dependencies;
* topology;
* constraints;
* authority paths;
* Effective Capability;
* Source States;
* Intermediate States;
* Target States;
* Transition Paths;
* Reachability;
* Admissibility.

The patterns are:

* contextual;
* evidence-dependent;
* non-exhaustive;
* many-to-many;
* potentially overlapping;
* non-canonical as taxonomy.

A system may exhibit:

* one pattern;
* several patterns;
* no pattern defined in this file;
* a pattern without any CNIG Failure Mode;
* a Failure Mode without a clearly named pattern from this file.

Pattern recognition does not establish causal attribution.

---

## 3. Pattern Identification Rule

A pattern should be recorded only where the available evidence identifies:

1. the bounded system;
2. the relevant components or domains;
3. the material structural relationship;
4. the Source State or comparison basis;
5. the Transition Path or structural change involved;
6. the resulting effect on Reachability, authority, capability, constraints, or Admissibility;
7. the status of the evidence.

Use the diagnostic states:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

Similarity to an example is not sufficient.

---

# Pattern 1 — Emergent Coupling

## 4. Definition

The **Emergent Coupling Pattern** occurs where:

> component composition creates a material dependency or structural relationship that is not represented adequately within the participating components’ local models.

The coupling may arise through:

* shared state;
* downstream service effects;
* resource dependency;
* identity mapping;
* delegated authority;
* workflow sequencing;
* retry or queue behaviour;
* common control planes;
* feedback paths;
* cross-domain integration;
* temporal coordination.

The defining condition is not merely that components interact.

The relationship must materially affect:

* Transition Paths;
* Reachability;
* authority;
* Effective Capability;
* resource effects;
* Governing Constraints;
* Target-State Admissibility.

---

## 5. Emergent Coupling Questions

* Which relationship exists only because the components are composed?
* Is the relationship represented in the Structural Model?
* Does one component’s output alter another component’s future preconditions?
* Does shared state create a dependency absent from local specifications?
* Does downstream execution introduce authority or capability?
* Does the relationship create another reachable State or path?
* Does the relationship affect applicable Governing Constraints?
* Is the coupling intended and governed?

An undeclared relationship is not automatically inadmissible.

Its structural effect and governing boundary must be established.

---

## 6. Possible Relationships

Emergent Coupling may provide evidence relevant to:

* Governance Capture;
* Implicit Reachability Expansion Failure;
* Privilege Surface Expansion Failure;
* Stochastic Drift;
* Phase Desynchronization;
* Structural Invariant weakening;
* Behavioral Invariant weakening.

None of these mappings is automatic.

---

# Pattern 2 — Constraint Amplification

## 7. Definition

The **Constraint Amplification Pattern** occurs where:

> constraints that are individually bounded combine across composition to produce a materially greater restriction or structural effect.

Constraint amplification may arise through:

* overlapping exclusions;
* inherited restrictions;
* cross-domain policy interaction;
* prerequisite chains;
* dependency constraints;
* separation requirements;
* authority conditions;
* recovery conditions;
* ordering constraints;
* temporal conditions.

Amplification may affect:

* available Transition Paths;
* reachable States;
* recovery States;
* valid continuation;
* authority;
* resource access;
* Target-State Admissibility.

---

## 8. Constraint Amplification Questions

* Which constraints participate?
* Where does each constraint originate?
* What boundary does each constraint govern?
* What effect does each have independently?
* What additional effect arises only when they are combined?
* Does the combination remove an intended State or transition?
* Is the amplified restriction within Governing Intent?
* Are recovery or continuation States still available?
* Does the combination remain represented in the Structural Model?

Constraint amplification is not inherently a failure.

The amplified effect may be:

* intended;
* required;
* admissible;
* excessive;
* unresolved.

---

## 9. Possible Relationships

Constraint Amplification may provide evidence relevant to:

* Invariant Overconstraint;
* Null State Boundary Violation;
* Constitutional Fragmentation;
* Stability Invariant weakening;
* Behavioral Invariant weakening.

Invariant Overconstraint requires evidence that intended valid States or transitions are removed beyond Governing Intent.

Null State Boundary Violation requires evidence that the system has reached a State with no admissible continuation.

---

# Pattern 3 — Unrepresented Reachability Expansion

## 10. Definition

The existing pattern name **Hidden Reachability Expansion Pattern** refers more precisely to:

> composition creating a reachable State or Transition Path that is absent from the represented Structural Model.

The word **hidden** does not mean necessarily:

* impossible to observe;
* intentionally concealed;
* unknown to every participant;
* semantically misunderstood.

The relevant condition is structural non-representation.

A State or path may become reachable through:

* delegation;
* inheritance;
* alternate authority;
* Intermediate States;
* changed topology;
* downstream service capability;
* cross-domain mapping;
* shared resources;
* accumulated local transitions.

---

## 11. Reachability Expansion Questions

* What State or Transition Path became reachable?
* From which Source State?
* Through which complete path?
* Which Intermediate State enabled it?
* Was the State represented in the Structural Model?
* Was the expansion deliberately acknowledged?
* Which Governing Constraints apply?
* Is the resulting State admissible?
* Does the path affect Effective Authority or Effective Capability?

A reachable but unrepresented State is not automatically inadmissible.

The State may still be:

* intended;
* authorized;
* governed;
* admissible.

---

## 12. Possible Relationships

Unrepresented Reachability Expansion may provide evidence relevant to:

* Implicit Reachability Expansion Failure;
* Privilege Surface Expansion Failure;
* Governance Capture;
* Structural Invariant weakening;
* Behavioral Invariant weakening.

Implicit Reachability Expansion Failure requires more than expansion.

The new State or path must also:

* be absent from the represented Structural Model;
* lack deliberate acknowledgement;
* conflict with Governing Intent.

---

# Pattern 4 — Fragmented Governance

## 13. Definition

The **Fragmented Governance Pattern** occurs where:

> several governance regimes apply to connected components, domains, or States, but their combined effect on the composition is incomplete, incompatible, or unresolved.

The relevant objects are actual:

* policies;
* authority structures;
* governance boundaries;
* constraints;
* jurisdictions;
* transition rules;
* resource rules;
* Admissibility conditions.

The pattern does not concern fragmented observer interpretations.

---

## 14. Fragmented Governance Questions

* Which governance regimes apply?
* Is each locally coherent?
* Which shared or Joint States fall between them?
* Do they apply compatible Admissibility conditions?
* Is one regime authoritative for the complete composition?
* Are authority and responsibility continuous across boundaries?
* Are there conflicting permitted and prohibited conditions?
* Does any regime govern the complete Transition Path?
* Are downstream effects governed?
* Is the resulting Target State covered coherently?

The existence of several governance regimes does not establish fragmentation.

They may compose coherently through an explicit global rule.

---

## 15. Possible Relationships

Fragmented Governance may provide evidence relevant to:

* Constitutional Fragmentation;
* Governance Capture;
* Reference Drift;
* Phase Desynchronization;
* Structural Invariant weakening;
* Identity Invariant weakening.

Constitutional Fragmentation requires evidence that locally coherent governance regimes fail to compose into a coherent Admissibility structure for shared or Joint States.

---

# Pattern 5 — Interaction Topology Change

## 16. Definition

The existing pattern name **Interaction Topology Drift Pattern** refers to:

> a material change in the relationship topology through which components, identities, services, agents, tools, or resources interact.

The term **drift** should not be used merely because the topology changed over time.

The analysis should identify the actual structural change.

Relevant changes may include:

* a new service path;
* removed isolation;
* changed delegation;
* inherited authority;
* a new agent-to-tool path;
* altered group nesting;
* a cross-domain mapping;
* changed resource membership;
* a new control path;
* a downstream service gaining effect over another resource.

---

## 17. Topology Change Questions

* What relationship was added, removed, or altered?
* Which Source State and later State are being compared?
* What caused the topology change?
* Does it alter Reachability?
* Does it alter Effective Authority?
* Does it alter Effective Capability?
* Does it alter control or resource effect?
* Is the change represented?
* Is the change governed?
* Does it affect Target-State Admissibility?

Generic connectivity change is not automatically material to Privilege Surface.

The topology must affect effective:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

---

## 18. Possible Relationships

Interaction Topology Change may provide evidence relevant to:

* Privilege Surface Expansion Failure;
* Implicit Reachability Expansion Failure;
* Governance Capture;
* Phase Desynchronization;
* Stability Invariant weakening;
* Structural Invariant weakening;
* Behavioral Invariant weakening.

The topology change itself is not a Failure Mode.

---

# Pattern 6 — Local Stability, Global Instability

## 19. Definition

The existing pattern name **Stability Under Composition Illusion Pattern** refers to the condition where:

> local evidence of component stability is treated incorrectly as sufficient evidence of global compositional Stability.

The word **illusion** is shorthand for an unsupported inference.

It is not a separate observer-centred CNIG object.

A system may show:

* stable components;
* repeatable local transitions;
* successful local tests;
* unchanged local configurations;
* bounded local effects;

while the composition produces:

* disproportionate global effects;
* divergent Target States;
* sensitivity to topology;
* sensitivity to timing or ordering;
* broad authority changes;
* unstable continuation paths.

---

## 20. Stability Questions

* What local conditions are supported as stable?
* What global condition is being inferred from them?
* Are the compared Source States materially equivalent?
* Did topology change?
* Did authority change?
* Did temporal phase change?
* Did ordering or concurrency change?
* Did a small structural variation produce a disproportionate result?
* Did the result remain within intended bounds?
* Is the divergence explained by intended probabilistic behaviour?

Local Stability does not establish global Stability.

Global variation also does not automatically establish Stochastic Drift.

---

## 21. Possible Relationships

Local Stability with Global Instability may provide evidence relevant to:

* Stochastic Drift;
* Phase Desynchronization;
* Implicit Reachability Expansion Failure;
* Stability Invariant weakening;
* Behavioral Invariant weakening;
* Structural Invariant weakening.

Stochastic Drift requires materially equivalent Source States and transition conditions, with material system-level divergence emerging through composition.

---

# Cross-Pattern Analysis

## 22. Pattern Overlap

Patterns may overlap within one Transition Path.

For example:

```text id="3ah1m0"
Unrepresented service dependency
        ↓
Emergent Coupling
        ↓
Interaction Topology Change
        ↓
Additional Effective Capability
        ↓
Unrepresented Reachability Expansion
        ↓
Target-State Admissibility evaluation
```

This sequence does not establish a Failure Mode automatically.

It identifies structural relationships requiring evaluation.

---

## 23. Pattern Relationships Are Many-to-Many

A pattern may:

* support several Failure Mode candidates;
* support no Failure Mode;
* weaken several Invariants;
* be an intended and admissible property;
* be contradicted by later evidence.

A Failure Mode may also arise through structural relationships not named as patterns in this file.

Do not use deterministic mappings such as:

```text id="fq7lkj"
Pattern A = Failure Mode B
```

The correct relationship is:

```text id="m3jgkc"
Pattern evidence
        ↓
Primitive evaluation
        ↓
Invariant evaluation
        ↓
Reachability and Admissibility analysis
        ↓
Failure Mode attribution, where complete
canonical conditions are supported
```

---

## 24. Patterns and Primitives

Patterns may be analysed through several Primitives.

### Reachable State Space

Which States or Transition Paths does the pattern create or remove?

### Admissible System State

Do the resulting States remain coherent under Governing Constraints?

### Constraint-Native Governance

Which constraints shape the pattern, and do they remain effective?

### State Transition Validation

How does the pattern affect the complete Transition Path?

### Execution vs Governance Separation

Can local execution remain correct while the pattern creates a globally inadmissible result?

### Privilege Surface

Does the pattern alter effective authority, capability, control, access, interaction, or resource effect?

No pattern is itself a Primitive.

---

## 25. Patterns and Invariants

A pattern may provide evidence relevant to one or more Invariants.

Possible assessments include:

* preserved;
* conditionally preserved;
* weakened;
* not materially implicated;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

A pattern does not automatically weaken an Invariant.

Invariant evaluation requires evidence about the actual system property expected to remain preserved.

---

## 26. Patterns and Failure Modes

Failure Modes are canonical structural conditions.

Patterns are non-canonical descriptive groupings.

Patterns must not:

* replace Failure Mode definitions;
* serve as automatic precursors;
* be treated as lower-severity Failure Modes;
* be assigned one-to-one to Failure Modes;
* broaden Failure Mode conditions.

A pattern may be present while the resulting State remains admissible.

A Failure Mode may be supported only where the complete canonical conditions in:

`04_FAILURE_MODES.md`

are established.

---

# Evidence and Boundary Rules

## 27. Evidence Record

A pattern assessment should record:

* bounded system;
* Source State;
* material components;
* structural relationship;
* Transition Path;
* Target State;
* Reachability effect;
* authority or capability effect;
* Governing Constraints;
* Admissibility status;
* relevant Invariants;
* supporting evidence;
* competing explanations;
* diagnostic state;
* unresolved conditions.

---

## 28. Pattern Status

Use one of:

* **OBSERVED**
* **INFERRED**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**
* **NOT SUPPORTED**

Do not use:

* present;
* confirmed;
* causal;

without identifying the evidential basis and bounded scope.

---

## 29. Observer Boundary

The patterns concern actual system structure.

They do not classify, by themselves:

* fragmented evidence;
* observer disagreement;
* inconsistent narratives;
* semantic incoherence;
* reconstructive-coherence loss;
* incomplete understanding;
* LLM reasoning error.

Those conditions may affect the evidence available for identifying a pattern.

They do not constitute a structural pattern unless evidence establishes an actual system condition involving:

* relationships;
* constraints;
* authority;
* capability;
* State;
* Transition Path;
* Reachability;
* Admissibility.

---

# Non-Operational Boundary

## 30. Non-Prescriptive Rule

The patterns do not prescribe:

* system architecture;
* component selection;
* implementation design;
* deployment topology;
* policy content;
* remediation;
* runtime validation;
* production decisions;
* autonomous action.

They do not establish that a system should:

* adopt a pattern;
* avoid a pattern;
* remove a relationship;
* block a transition;
* change a constraint.

Those conclusions require an external engineering or governance process.

---

## 31. External Application Boundary

External applications may reference these patterns as analytical labels.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external application must not treat the patterns as:

* mandatory architecture classes;
* executable detection rules;
* canonical software modules;
* automated approval conditions;
* proof of a Failure Mode;
* authority to redefine CNIG concepts.

---

## 32. Non-Exhaustiveness Rule

The six patterns in this file are illustrative and non-exhaustive.

Their presence does not imply that every CNIG-relevant composition can be classified through them.

Additional structural arrangements may be described externally where they:

* preserve canonical CNIG terminology;
* do not redefine Primitives, Invariants, or Failure Modes;
* are identified explicitly as non-canonical;
* remain evidence-grounded;
* preserve the non-operational boundary.

Such descriptions do not become canonical CNIG patterns merely by being published or repeated.

---

## 33. Stability Rule

The pattern layer remains coherent when:

* patterns describe actual structural relationships;
* patterns remain non-canonical and non-exhaustive;
* pattern identification remains evidence-dependent;
* Reachability remains distinct from Admissibility;
* topology change remains distinct from Privilege Surface expansion;
* local Stability remains distinct from global Stability;
* patterns remain distinct from Primitives, Invariants, and Failure Modes;
* pattern-to-Failure-Mode relationships remain many-to-many;
* observer understanding remains distinct from system structure;
* implementation and action remain external.

The pattern layer degrades when:

* patterns become architecture blueprints;
* pattern names become automatic diagnoses;
* every topology change becomes Privilege Surface Expansion Failure;
* every unrepresented State becomes Implicit Reachability Expansion Failure;
* every multi-policy system becomes Constitutional Fragmentation;
* local stability is treated as proof of global Stability;
* patterns are treated as canonical system types;
* pattern recognition is used as operational authority.

---

## 34. Transition to Domain Instances

The next layer provides non-canonical domain illustrations of how CNIG structural conditions may appear across different system contexts.

See:

`09_DOMAIN_INSTANCES.md`
