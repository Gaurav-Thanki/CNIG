# CNIG Primitives

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer defines the six canonical Primitives used within Constraint-Native Infrastructure Governance.

The Primitives provide the minimum structural vocabulary required to reason about:

* system composition;
* Reachability;
* Admissibility;
* Governing Constraints;
* Transition Paths;
* execution correctness;
* governance validity;
* Effective Authority;
* Effective Capability.

They are canonical analytical concepts.

They are not:

* software components;
* runtime objects;
* APIs;
* services;
* implementation targets;
* enforcement mechanisms;
* operational controls;
* Failure Modes.

The canonical names and ordering of the six Primitives must remain stable.

---

## 2. Canonical Primitive Set

CNIG uses the following six Primitives in this order:

1. **Reachable State Space**
2. **Admissible System State**
3. **Constraint-Native Governance**
4. **State Transition Validation**
5. **Execution vs Governance Separation**
6. **Privilege Surface**

The ordering provides a conceptual progression:

* what the composition makes possible;
* which possible States remain admissible;
* what Governing Constraints shape the composition;
* whether movement between States preserves Admissibility;
* why execution success and governance validity must remain separate;
* how composition changes effective interaction, authority, and capability.

---

# Primitive 1 — Reachable State Space

## 3. Definition

**Reachable State Space** is:

> the complete set of system States that can emerge through component composition.

It represents structural possibility.

A State may become reachable through:

* direct transitions;
* accumulated transitions;
* component relationships;
* service interaction;
* delegation;
* inheritance;
* identity mapping;
* shared state;
* workflow progression;
* cross-domain integration;
* changed topology;
* Intermediate States;
* alternative authority paths;
* downstream capability.

Reachable State Space is not limited to:

* States already executed;
* States already observed;
* States documented in the Structural Model;
* States intended by the architecture;
* States one component can produce independently.

A State may be reachable without being:

* intended;
* represented;
* authorized;
* governed;
* admissible.

---

## 4. Relationship to Execution

Reachable State Space describes structural possibility independently of whether every State has already occurred.

However, execution evidence may establish that:

* a State was reachable;
* a Transition Path existed;
* an authority path was effective;
* an Intermediate State enabled a later transition;
* a resource effect was structurally possible.

Observed execution therefore provides evidence about Reachability.

Execution does not define the complete Reachable State Space.

It also does not establish Admissibility.

---

## 5. Representation Limit

The canonical definition concerns the complete theoretical set of structurally reachable States.

A practical analysis may identify only:

* States known to be reachable;
* States inferred to be reachable;
* States represented as reachable;
* States not yet evaluated;
* States supported as unreachable within a bounded model.

Failure to identify a Transition Path does not prove that no path exists unless the bounded model and method support that conclusion.

---

# Primitive 2 — Admissible System State

## 6. Definition

An **Admissible System State** is:

> a reachable State that remains structurally coherent under the constraints governing the composition.

Admissibility may depend on:

* authority boundaries;
* separation requirements;
* prohibited relationships;
* resource boundaries;
* transition conditions;
* Target-State requirements;
* valid-continuation requirements;
* Governing Intent;
* relevant Invariant-preservation requirements.

A State must first be reachable before it can be evaluated as an Admissible System State within that composition.

---

## 7. Reachability Is Not Admissibility

A State may be:

* reachable and admissible;
* reachable but inadmissible;
* reachable with Admissibility unresolved;
* represented but unreachable;
* absent from the represented Structural Model yet structurally reachable.

Admissibility is not established merely by:

* successful execution;
* local validation;
* component health;
* authentication success;
* authorization success;
* policy presence;
* absence of an alert;
* continued system operation.

A successful transition may still produce an inadmissible Target State.

---

## 8. Structural Basis

Admissibility requires a supported structural basis.

The analysis should identify:

* the relevant State;
* the applicable Governing Constraints;
* the authority conditions;
* the relevant boundaries;
* the Transition Path;
* the Target-State requirements;
* the Governing Intent;
* any material Invariant-preservation requirement.

An outcome being unexpected, undesirable, undocumented, or unusual does not independently establish inadmissibility.

Where the governing basis is incomplete or conflicting, Admissibility should remain:

* PROVISIONAL;
* CONFLICTING;
* or UNRESOLVED.

---

# Primitive 3 — Constraint-Native Governance

## 9. Definition

**Constraint-Native Governance** is:

> the implicit or explicit structural constraints that shape system relationships, interaction boundaries, authority, Transition Paths, Reachability, and permissible configurations.

These constraints may be represented through:

* policies;
* architecture;
* authority definitions;
* identity relationships;
* separation requirements;
* resource boundaries;
* exclusions;
* trust conditions;
* transition requirements;
* governing agreements;
* ownership boundaries;
* valid-continuation requirements.

Constraint-Native Governance describes governing structure.

It is not necessarily a runtime enforcement mechanism.

---

## 10. Declared and Effective Governance

CNIG distinguishes between:

* declared governance;
* represented governance;
* implemented governance;
* enforced constraints;
* effective governing structure;
* observed execution;
* resulting system State.

A Governing Constraint may remain:

* documented;
* configured;
* named;
* formally present;

while no longer constraining the complete composition as intended.

The existence of a rule does not establish that its effect extends across:

* every component;
* every boundary;
* every authority path;
* every Transition Path;
* every reachable Target State.

---

## 11. Governing Intent

**Governing Intent** is the intended structural boundary within which the composed system is expected to operate.

It may concern:

* permitted relationships;
* prohibited relationships;
* authority scope;
* resource scope;
* valid Transition Paths;
* required separation;
* expected Target States;
* unavailable States;
* recovery requirements;
* capability boundaries.

Governing Intent must be supported by relevant structural or authoritative evidence.

It must not be inferred solely from:

* observed execution;
* system history;
* local permission approval;
* absence of enforcement;
* continued operation.

---

# Primitive 4 — State Transition Validation

## 12. Definition

**State Transition Validation** is:

> a conceptual reasoning construct for evaluating whether movement from one system State to another preserves structural coherence and remains within the admissible State space.

It evaluates more than whether one local action succeeded.

The relevant analytical objects may include:

* Source State;
* initiating action or condition;
* Intermediate States;
* complete Transition Path;
* transition authority;
* authority changes;
* resource effects;
* constraint applicability;
* Invariant preservation;
* Target State;
* resulting Reachability;
* Target-State Admissibility.

---

## 13. Local and Complete Validation

CNIG distinguishes between:

### Local transition validity

Whether one component or stage accepts and completes its local transition.

### Complete Transition-Path validity

Whether the accumulated sequence of transitions preserves the relevant Governing Constraints across the composition.

### Target-State Admissibility

Whether the final composed State remains within Governing Intent.

Every local transition may be valid while:

* an Intermediate State introduces unintended authority;
* a downstream effect expands capability;
* the complete path crosses an unevaluated boundary;
* the Target State is absent from the Structural Model;
* the resulting State is inadmissible.

---

## 14. Conceptual Boundary

State Transition Validation is not:

* an execution-time validator;
* a software component;
* an API validation routine;
* a workflow engine;
* a policy engine;
* a pipeline gate;
* a deployment control;
* a production approval mechanism.

An external application may create its own validation process using related concepts.

That implementation remains outside CNIG.

---

# Primitive 5 — Execution vs Governance Separation

## 15. Definition

**Execution vs Governance Separation** is:

> the analytical distinction between whether a component or transition executes correctly and whether the resulting composed State remains within Governing Intent.

It separates two independent properties.

### Execution correctness

Whether a component, service, action, tool, agent, or local transition behaves according to its specification or local acceptance conditions.

### Governance validity

Whether the complete composition, Transition Path, and resulting Target State remain structurally admissible under the applicable Governing Constraints.

---

## 16. Possible Combinations

A system may exhibit:

| Execution condition | Governance condition    | Structural result                                       |
| ------------------- | ----------------------- | ------------------------------------------------------- |
| Correct             | Valid                   | Locally correct execution reaches an admissible State   |
| Correct             | Invalid                 | Locally correct execution reaches an inadmissible State |
| Incorrect           | Invalid                 | Component failure contributes to an inadmissible State  |
| Incorrect           | Not materially affected | A local failure remains structurally bounded            |

CNIG is particularly concerned with the second condition:

> execution succeeds locally while the composition reaches a globally unintended or inadmissible State.

---

## 17. Analytical Consequences

Execution success does not establish:

* Target-State Admissibility;
* preservation of Governing Intent;
* completeness of the Structural Model;
* absence of Reachability expansion;
* preservation of Invariants;
* absence of a Failure Mode.

Likewise, declared governance does not establish:

* effective constraint authority;
* actual enforcement;
* coverage of every Transition Path;
* governance of every Joint State;
* Admissibility of every reachable State.

---

# Primitive 6 — Privilege Surface

## 18. Definition

**Privilege Surface** is:

> the effective Interaction Topology through which composition expands or constrains interaction, access, authority, capability, control, resource effect, or action paths.

Privilege Surface may include relationships between:

* principals;
* identities;
* roles;
* groups;
* services;
* agents;
* tools;
* APIs;
* delegated authority;
* service-held authority;
* resources;
* control mechanisms;
* downstream systems.

Privilege Surface concerns effective capability produced through composition.

---

## 19. Connectivity Boundary

Generic connectivity is not automatically Privilege Surface.

A relationship belongs to the Privilege Surface only where it materially affects effective:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

For example, a communication path that carries information but cannot alter authority, capability, control, or protected resource effect may be relevant to system topology without being material to the Privilege Surface.

---

## 20. Effective Authority and Effective Capability

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

Privilege Surface describes the topology through which these effective conditions emerge.

---

## 21. Non-Security Reduction

Privilege Surface is relevant to security and identity systems, but it is not limited to conventional access control.

It may also concern:

* agent-to-tool capability;
* service-mediated resource effects;
* orchestration authority;
* workflow control;
* infrastructure administration;
* cross-domain action paths;
* authority over system transitions.

Privilege Surface is not:

* an access-control product;
* a permission database;
* a threat score;
* an attack-surface synonym;
* a runtime security mechanism.

---

# Primitive Relationships

## 22. Canonical Relationship Model

The six Primitives interact as follows:

```text
System Composition
        |
        v
Available Transition Paths
        |
        v
Reachable State Space
        |
        v
Target State
        |
        +----------------------------------+
        |                                  |
        v                                  v
Constraint-Native Governance       Privilege Surface
        |                           and effective
        |                           authority/capability
        +----------------+-----------------+
                         |
                         v
              State Transition Validation
                         |
                         v
             Admissible System State
                         ^
                         |
         Execution vs Governance Separation
         prevents local execution success from
         being treated as proof of Admissibility
```

This representation is conceptual.

It is not an executable flow.

---

## 23. Relationship Summary

### Reachable State Space

Defines the structural possibility space created through composition.

### Admissible System State

Identifies reachable States that remain coherent under Governing Constraints.

### Constraint-Native Governance

Shapes:

* available relationships;
* transition conditions;
* authority boundaries;
* Reachability;
* Admissibility.

### State Transition Validation

Evaluates whether the complete Transition Path preserves structural coherence and reaches an admissible Target State.

### Execution vs Governance Separation

Prevents local execution correctness from being treated as proof of global governance validity.

### Privilege Surface

Describes how Interaction Topology changes Effective Authority, Effective Capability, control, access, and resource effects.

---

## 24. Many-to-Many Relationships

The Primitives are related but must not be collapsed.

For example:

* Privilege Surface may change Reachable State Space;
* Constraint-Native Governance may constrain Privilege Surface;
* a Transition Path may expand Effective Capability;
* State Transition Validation may identify a reachable but inadmissible Target State;
* Execution vs Governance Separation may explain why every local stage succeeded despite global inadmissibility;
* an Admissible System State may depend on authority, topology, and valid continuation conditions.

No Primitive is a substitute for another.

---

# Ontology Boundaries

## 25. Primitives vs Invariants

Primitives define the structural axes of CNIG analysis.

Invariants describe properties expected to remain preserved across composition and transition.

Examples:

* Reachable State Space is a Primitive.
* Stability Invariant is an Invariant.
* Privilege Surface is a Primitive.
* Identity Invariant is an Invariant.

An Invariant may be evaluated through several Primitives.

A Primitive is not an Invariant.

Canonical Invariant definitions are governed by:

`GLOSSARY.md`

---

## 26. Primitives vs Failure Modes

Primitives describe the structure through which system composition is analysed.

Failure Modes describe evidence-supported conditions in which composition produces or exposes inadmissibility.

Examples:

* Reachable State Space is a Primitive.
* Implicit Reachability Expansion Failure is a Failure Mode.
* Privilege Surface is a Primitive.
* Privilege Surface Expansion Failure is a Failure Mode.

The existence of a Primitive does not establish its similarly named Failure Mode.

For example:

* every system has some Reachable State Space;
* not every expansion is Implicit Reachability Expansion Failure;
* a system may have a Privilege Surface without Privilege Surface Expansion Failure.

Canonical Failure Mode definitions are governed by:

`04_FAILURE_MODES.md`

---

## 27. Actual Structure vs Observer Understanding

The Primitives concern actual system:

* States;
* relationships;
* constraints;
* Transition Paths;
* authority;
* capability;
* Reachability;
* Admissibility.

They do not describe, by themselves:

* observer disagreement;
* fragmented evidence;
* semantic inconsistency;
* conflicting narratives;
* reconstructive-coherence loss;
* incomplete understanding;
* LLM reasoning failure.

Those conditions may affect the evidence available for applying the Primitives.

They do not redefine the Primitives or become their analytical object.

---

# Non-Operational Boundary

## 28. Non-Implementation Rule

The six Primitives must not be treated as:

* required software modules;
* product features;
* service names;
* API objects;
* database entities;
* mandatory workflow stages;
* production controls;
* automated decisions;
* runtime enforcement mechanisms.

External applications may reference or apply these concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

No implementation should be presented as:

* CNIG itself;
* the canonical implementation of a Primitive;
* proof that CNIG guarantees an outcome;
* authority to redefine a Primitive.

---

## 29. Representation Rule

Primitives may be represented externally through:

* diagrams;
* analytical models;
* schemas;
* formal methods;
* evidence graphs;
* documentation;
* software abstractions.

The representation is not identical to the Primitive.

Its validity remains bounded by:

* its scope;
* evidence;
* assumptions;
* model completeness;
* implementation choices.

---

## 30. Stability Rule

The Primitive layer remains stable when:

* the six canonical names and their ordering remain fixed;
* Reachability remains distinct from Admissibility;
* Constraint-Native Governance remains structural and non-operational;
* State Transition Validation remains conceptual;
* execution correctness remains distinct from governance validity;
* Privilege Surface remains limited to topology affecting effective interaction, authority, capability, control, or resource effect;
* Primitives remain distinct from Invariants and Failure Modes;
* system structure remains distinct from observer understanding;
* implementation remains external.

The Primitive layer degrades when:

* Primitives become generic metaphors;
* Privilege Surface becomes a synonym for all connectivity;
* Admissibility is inferred from execution success;
* State Transition Validation becomes a claimed runtime mechanism;
* Failure Modes are merged with their related Primitives;
* external implementation objects are treated as canonical CNIG concepts;
* adjacent ontologies are imported silently.

---

## 31. Transition to Failure Modes

The next canonical layer defines the ten CNIG Failure Modes and their structural distinctions.

See:

`04_FAILURE_MODES.md`
