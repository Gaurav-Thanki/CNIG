# CNIG Domain Illustrations

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer provides non-canonical illustrations of how CNIG structural questions may arise across different system domains.

The illustrations show how the fixed CNIG ontology may be applied to domain-specific evidence concerning:

* system composition;
* Source States;
* Intermediate States;
* Target States;
* Transition Paths;
* Reachable State Space;
* Governing Constraints;
* Effective Authority;
* Effective Capability;
* Privilege Surface;
* Invariant preservation;
* Admissibility.

These illustrations do not establish that every system in a named domain exhibits a CNIG condition.

They are not:

* implementations;
* domain packs;
* architecture blueprints;
* control frameworks;
* engineering prescriptions;
* operational playbooks;
* automatic Failure Mode mappings.

---

## 2. Nature of Domain Illustrations

A domain illustration is:

> a bounded example of how domain-specific components and evidence may be represented through canonical CNIG concepts.

Domain illustrations are:

* explanatory;
* contextual;
* non-exhaustive;
* evidence-sensitive;
* many-to-many;
* non-canonical.

They may help identify useful questions.

They do not prove:

* local correctness;
* structural causation;
* Reachability expansion;
* inadmissibility;
* Invariant weakening;
* a canonical Failure Mode.

A real analysis must still establish the relevant system structure from evidence.

---

## 3. Domain-Invariance Rule

CNIG’s canonical ontology remains stable across domains.

The following do not change by domain:

### Six Primitives

1. Reachable State Space
2. Admissible System State
3. Constraint-Native Governance
4. State Transition Validation
5. Execution vs Governance Separation
6. Privilege Surface

### Four Invariants

1. Identity Invariant
2. Stability Invariant
3. Behavioral Invariant
4. Structural Invariant

### Ten Failure Modes

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

Domain-specific evidence, terminology, components, constraints, and system representations may differ.

Those differences do not authorize changes to canonical CNIG definitions.

The stable ontology is applied to different evidence.

CNIG is not rewritten around each domain.

---

## 4. Domain-Evidence Rule

A domain analysis should identify:

1. the bounded system;
2. the relevant Source State;
3. participating components or domains;
4. material relationships;
5. the complete Transition Path;
6. material Intermediate States;
7. the Target State;
8. Reachability changes;
9. applicable Governing Constraints;
10. the supported Governing Intent;
11. relevant authority or capability changes;
12. Invariant preservation or weakening;
13. the Admissibility finding;
14. any evidence-supported Failure Mode;
15. competing explanations;
16. unresolved evidence.

Without those elements, a domain illustration remains only a possible structural analogy.

---

# Domain 1 — Distributed Systems

## 5. Domain Composition

A distributed-system composition may include:

* services;
* APIs;
* message brokers;
* queues;
* caches;
* databases;
* replicated resources;
* control planes;
* service identities;
* schedulers;
* retry mechanisms;
* consistency mechanisms;
* orchestration layers.

The CNIG question is not merely whether the system is distributed.

It is whether relationships between locally valid components create a material system State or Transition Path that no component evaluates in full.

---

## 6. Possible Structural Conditions

Relevant structural conditions may include:

* one service’s output changing another service’s future transition preconditions;
* retries producing additional downstream resource effects;
* a queue preserving an action beyond the phase in which it was governed;
* replication creating non-equivalent effective Source States;
* individually valid service transitions accumulating into an unintended Target State;
* a dependency change introducing an alternate Transition Path;
* several locally coherent services reaching a Joint State absent from the Structural Model.

These conditions do not establish a CNIG Failure Mode automatically.

---

## 7. Distributed-System Questions

* What was the material Source State?
* Which services participated in the complete Transition Path?
* Which Intermediate States existed between the initiating request and final resource effect?
* Did retries, queues, or asynchronous propagation change later transition preconditions?
* Did the effective topology differ from the represented dependency model?
* Did service-held authority broaden the effect of the initiating action?
* Did execution occur under the same structural phase as the applicable governance conditions?
* What Target State became reachable?
* Which Governing Constraints applied to the complete path?
* Did the resulting State remain admissible?

---

## 8. Possible Canonical Relationships

Depending on evidence, a distributed-system condition may be relevant to:

* Phase Desynchronization;
* Stochastic Drift;
* Implicit Reachability Expansion Failure;
* Governance Capture;
* Constitutional Fragmentation;
* Stability Invariant weakening;
* Behavioral Invariant weakening;
* Structural Invariant weakening.

For example, divergent outcomes do not establish Stochastic Drift until materially equivalent Source States and transition conditions are supported.

Asynchronous execution does not establish Phase Desynchronization unless an actual phase mismatch alters Reachability or Admissibility.

---

## 9. Non-CNIG Alternatives

A distributed-system outcome may instead be explained sufficiently by:

* a software defect;
* message loss;
* malformed data;
* resource exhaustion;
* an incorrect retry policy;
* an unavailable dependency;
* a direct configuration error;
* a known consistency model;
* intended probabilistic behaviour.

CNIG should not displace those explanations without evidence that composition remains necessary to explain the material outcome.

---

# Domain 2 — Identity and Access Systems

## 10. Domain Composition

An identity and access composition may include:

* users;
* service principals;
* managed identities;
* roles;
* groups;
* nested groups;
* direct permissions;
* inherited permissions;
* delegated authority;
* token exchange;
* resource scopes;
* policy engines;
* identity providers;
* cross-domain mappings;
* service-held authority.

The relevant object is not only the declared permission.

It is the complete authority and capability made effective through the composed relationship structure.

---

## 11. Possible Structural Conditions

Relevant conditions may include:

* several limited assignments combining into broader Effective Authority;
* nested membership creating an authority path absent from one local view;
* an unchanged permission acquiring broader downstream capability;
* identity mapping creating non-equivalent effective principals;
* delegated authority obscuring Authority Lineage;
* a service acting with authority broader than the initiating identity;
* cross-domain identity recognition joining separately governed authority spaces;
* a role or group change creating another resource-effect path.

Permission aggregation does not automatically establish inadmissibility.

The resulting authority or capability must be evaluated against Governing Intent.

---

## 12. Identity-System Questions

* Which principal initiated the path?
* Which effective identity acted at each stage?
* Which roles, groups, inherited relationships, or delegated permissions contributed authority?
* Was Authority Lineage preserved?
* Which service-held authority participated?
* What Effective Authority existed through the complete composition?
* What Effective Capability became reachable?
* Which protected resources could be affected?
* Was the complete authority path represented?
* Was the authority path within the intended structural boundary?
* Did the Target State remain admissible?

---

## 13. Privilege Surface Boundary

In identity and access systems, Privilege Surface is not synonymous with:

* the number of permissions;
* the number of accounts;
* every authentication path;
* every network connection;
* every role relationship.

Privilege Surface concerns the effective Interaction Topology through which composition changes:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

A relationship must have a material effect on one or more of those properties.

---

## 14. Possible Canonical Relationships

Depending on evidence, an identity-system condition may be relevant to:

* Privilege Surface Expansion Failure;
* Reference Drift;
* Governance Capture;
* Constitutional Fragmentation;
* Implicit Reachability Expansion Failure;
* Identity Invariant weakening;
* Structural Invariant weakening;
* Behavioral Invariant weakening.

Observer disagreement about an identity does not establish Reference Drift.

The same structural reference must resolve to non-equivalent effective identities, authorities, scopes, or resources in the actual system.

---

## 15. Non-CNIG Alternatives

An identity outcome may instead be explained sufficiently by:

* a direct excessive permission;
* an incorrect group assignment;
* a known role misconfiguration;
* a disabled policy;
* an authentication defect;
* a compromised credential;
* an explicit unauthorized action;
* a conventional access-control error.

CNIG becomes material where the decisive authority or capability exists through composition rather than one direct local assignment alone.

---

# Domain 3 — Orchestration and Workflow Systems

## 16. Domain Composition

An orchestration or workflow composition may include:

* workflow stages;
* pipelines;
* schedulers;
* triggers;
* queues;
* approvals;
* service accounts;
* agents;
* tools;
* deployment systems;
* state stores;
* rollback paths;
* downstream resource operations.

Each stage may satisfy its own local acceptance conditions.

The complete path may still reach a Target State that no stage evaluates globally.

---

## 17. Possible Structural Conditions

Relevant conditions may include:

* one successful stage changing the preconditions of a later stage;
* an Intermediate State enabling downstream capability;
* locally valid approvals covering only part of the complete resource effect;
* a retry or resume path bypassing a previously applicable constraint;
* a pipeline reaching an unrepresented Target State;
* separate workflow owners governing different stages without governing the Joint State;
* rollback remaining technically available but no longer admissible;
* execution order altering the resulting Target State.

---

## 18. Workflow-System Questions

* What was the Source State before workflow initiation?
* Which stage initiated each transition?
* Which authority did each stage use?
* What Intermediate States were created?
* Did later stages operate with service-held or delegated authority?
* Did any stage validate the complete Transition Path?
* Which resources changed at each stage?
* Did retries, resumes, or alternate branches create additional paths?
* What final Target State was reached?
* Was the Target State represented before execution?
* Was the complete path within Governing Intent?
* Were admissible rollback or continuation paths available?

---

## 19. Execution vs Governance Separation

Workflow completion may establish that:

* each stage ran;
* local checks passed;
* authorization succeeded;
* expected outputs were produced.

It does not establish that:

* the complete Transition Path was governed;
* downstream effects were represented;
* authority remained within intended boundaries;
* the Target State was admissible;
* valid continuation remained available.

Workflow systems are therefore a direct context in which Execution vs Governance Separation may be material.

---

## 20. Possible Canonical Relationships

Depending on evidence, a workflow condition may be relevant to:

* Implicit Reachability Expansion Failure;
* Phase Desynchronization;
* Governance Capture;
* Null State Boundary Violation;
* Privilege Surface Expansion Failure;
* Behavioral Invariant weakening;
* Structural Invariant weakening;
* Stability Invariant weakening.

A failed workflow is not automatically a CNIG condition.

A successful workflow is not automatically admissible.

---

# Domain 4 — AI and Multi-Agent Systems

## 21. Domain Composition

An AI or multi-agent composition may include:

* language models;
* decision models;
* agents;
* sub-agents;
* tools;
* external services;
* memory stores;
* retrieval systems;
* planners;
* evaluators;
* approval interfaces;
* identity and permission systems;
* protected resources;
* human authorities.

CNIG does not evaluate whether a model’s internal reasoning is semantically coherent.

It examines the actual system structure through which model or agent outputs may create States, invoke tools, exercise authority, or affect resources.

---

## 22. System-State Boundary

The relevant CNIG object is not generic “behavioural space.”

The relevant objects include actual:

* tool-call paths;
* authority paths;
* resource effects;
* agent-to-agent delegation;
* identity mappings;
* memory changes;
* workflow transitions;
* system States;
* reachable Target States.

A model output becomes structurally relevant to CNIG where it participates in a path that changes actual system:

* State;
* authority;
* capability;
* control;
* resource effect;
* Reachability;
* Admissibility.

---

## 23. Possible Structural Conditions

Relevant conditions may include:

* one agent delegating to another agent with broader tool access;
* several individually bounded agents combining into broader Effective Capability;
* an evaluator validating an output without evaluating downstream resource effects;
* memory or retrieved context changing later transition preconditions;
* a planner introducing a tool path absent from the represented workflow;
* agent retries creating repeated or accumulated effects;
* an approval applying to the stated action but not its complete reachable consequences;
* separate agent policies failing to govern a Joint State;
* a tool executing with service-held authority not represented for the initiating agent.

---

## 24. AI-System Questions

* What bounded system includes the model, agents, tools, identities, and resources?
* Which principal or authority initiated the path?
* Which agent acted at each stage?
* Which tools were available?
* Which agent or tool possessed effective authority?
* Did delegation alter Effective Capability?
* What memory, retrieval result, or Intermediate State changed later preconditions?
* What resource effects became reachable?
* Was the complete tool and agent path represented?
* Which human or system authority governed the complete path?
* Did approval cover only the requested action or also its reachable consequences?
* Did the resulting Target State remain admissible?

---

## 25. Observer and Reasoning Boundary

The following are not CNIG conditions by themselves:

* model hallucination;
* inconsistent reasoning;
* fragmented context;
* semantic contradiction;
* observer disagreement;
* incomplete reconstruction;
* evaluator disagreement;
* low confidence.

Those conditions may affect evidence or system inputs.

They become relevant to CNIG only where they contribute to an actual structural condition, such as:

* a tool invocation;
* an authority change;
* a State transition;
* a resource effect;
* changed Reachability;
* changed Admissibility.

---

## 26. Possible Canonical Relationships

Depending on evidence, an AI or multi-agent condition may be relevant to:

* Privilege Surface Expansion Failure;
* Implicit Reachability Expansion Failure;
* Governance Capture;
* Constitutional Fragmentation;
* Stochastic Drift;
* Identity Invariant weakening;
* Behavioral Invariant weakening;
* Structural Invariant weakening.

Probabilistic model output alone does not establish Stochastic Drift.

The canonical conditions concerning materially equivalent Source States, transition conditions, compositional divergence, and intended bounds must still be supported.

---

# Domain 5 — Infrastructure and Cloud Systems

## 27. Domain Composition

An infrastructure or cloud composition may include:

* compute;
* storage;
* networks;
* identity systems;
* hypervisors;
* clusters;
* control planes;
* orchestration systems;
* backup systems;
* replication;
* monitoring;
* policy systems;
* management interfaces;
* cloud accounts or subscriptions;
* regions;
* shared services;
* infrastructure automation.

Infrastructure may be examined as a composed State system where relationships determine available transitions and resource effects.

---

## 28. Possible Structural Conditions

Relevant conditions may include:

* a topology change exposing a new management path;
* shared identity or role relationships broadening administrative capability;
* scaling changing resource membership and downstream effects;
* replication placing governance and resource State in different phases;
* a control plane retaining authority after the represented boundary changes;
* separate infrastructure domains sharing a resource neither governs completely;
* locally valid automation stages reaching an unintended infrastructure Target State;
* backup, recovery, or failover changes removing an admissible continuation;
* a configuration remaining unchanged while its Effective Capability changes through integration.

---

## 29. Infrastructure-System Questions

* What was the relevant infrastructure Source State?
* Which components and control planes participated?
* Which identities and service accounts held authority?
* Which topology and dependency relationships existed?
* Which automation or administrative Transition Path was available?
* Did scaling, replication, migration, or failover create Intermediate States?
* Did resource membership change?
* Did Effective Authority or Effective Capability change?
* Were management paths represented?
* Did Governing Constraints cover all participating domains?
* Which States became newly reachable?
* Did the resulting infrastructure State remain admissible?
* Did valid recovery or rollback States remain reachable?

---

## 30. Possible Canonical Relationships

Depending on evidence, an infrastructure condition may be relevant to:

* Privilege Surface Expansion Failure;
* Implicit Reachability Expansion Failure;
* Phase Desynchronization;
* Governance Capture;
* Constitutional Fragmentation;
* Invariant Overconstraint;
* Null State Boundary Violation;
* Stability Invariant weakening;
* Structural Invariant weakening.

Scaling alone does not establish structural instability.

Topology change alone does not establish Privilege Surface Expansion Failure.

Replication delay alone does not establish Phase Desynchronization.

The material effect on Reachability or Admissibility must be supported.

---

## 31. Non-CNIG Alternatives

An infrastructure outcome may instead be explained sufficiently by:

* hardware failure;
* capacity exhaustion;
* a direct network fault;
* a known software defect;
* an explicit configuration error;
* an unavailable dependency;
* failed storage;
* a direct operational mistake;
* ordinary replication delay within intended bounds.

CNIG becomes material where component composition remains necessary to explain the system-level State.

---

# Cross-Domain Composition

## 32. Cross-Domain Conditions

Many CNIG-relevant systems cross more than one domain.

For example:

```text id="cy0om8"
Human or system principal
        ↓
Identity and authority system
        ↓
Workflow or orchestration system
        ↓
Agent, service, or automation layer
        ↓
Infrastructure control plane
        ↓
Protected resource
```

The complete Transition Path may cross:

* identity boundaries;
* governance boundaries;
* service boundaries;
* resource boundaries;
* temporal phases;
* authority domains.

No single domain may represent the complete:

* authority path;
* Effective Capability;
* Target State;
* Admissibility condition.

---

## 33. Cross-Domain Questions

* Where does authority originate?
* Where does identity mapping occur?
* Which domain owns each transition?
* Which domain governs the Joint State?
* Where does one domain’s output become another domain’s precondition?
* Which Intermediate States cross domains?
* Does one domain introduce authority unavailable in another?
* Which constraints survive the boundary?
* Which constraints change scope?
* Does any governing structure evaluate the complete path?
* What final system State becomes reachable?
* Is that State admissible under the combined constraints?

Cross-domain composition does not automatically establish Constitutional Fragmentation.

The governance regimes may compose coherently.

---

# Canonical Relationship Discipline

## 34. Domain Illustrations and Primitives

Each domain may be evaluated through all six Primitives.

A domain must not be assigned permanently to one Primitive.

For example:

* identity systems are not reducible to Privilege Surface;
* workflow systems are not reducible to State Transition Validation;
* distributed systems are not reducible to Reachable State Space;
* AI systems are not reducible to Stochastic Drift;
* infrastructure systems are not reducible to Stability.

Primitive relationships remain many-to-many and evidence-dependent.

---

## 35. Domain Illustrations and Invariants

Each domain may implicate several Invariants.

Possible assessments remain:

* preserved;
* conditionally preserved;
* weakened;
* not materially implicated;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

A domain does not have a default weakened Invariant.

Invariant assessment concerns the actual system property expected to remain preserved.

---

## 36. Domain Illustrations and Failure Modes

No domain maps automatically to a Failure Mode.

The following mappings are invalid:

```text id="yk5w73"
Identity system = Privilege Surface Expansion Failure
Distributed system = Stochastic Drift
Multi-agent system = Governance Capture
Workflow system = Phase Desynchronization
Cloud system = Implicit Reachability Expansion Failure
```

A valid relationship is:

```text id="vgs5tj"
Domain evidence
        ↓
Bounded system representation
        ↓
Source State and Transition Path
        ↓
Primitive evaluation
        ↓
Invariant evaluation
        ↓
Reachability and Admissibility finding
        ↓
Failure Mode attribution,
where complete canonical conditions are supported
```

---

## 37. Evidence Status

A domain analysis should classify material conclusions as:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

The domain label itself is not evidence.

The fact that a system belongs to a complex or distributed domain does not establish a CNIG condition.

---

## 38. Illustrative Status

The examples in this file are hypothetical structural possibilities.

They do not assert that:

* a named product behaves in a particular way;
* a domain necessarily contains the described condition;
* a particular architecture is defective;
* a Failure Mode is widespread;
* any operational change is required.

A real case requires its own evidence.

---

# Framework and Implementation Boundaries

## 39. Observer Boundary

CNIG domain analysis concerns actual system:

* States;
* relationships;
* constraints;
* authority;
* capability;
* Transition Paths;
* Reachability;
* Admissibility.

It does not classify, by themselves:

* domain vocabulary differences;
* observer disagreement;
* incomplete documentation;
* fragmented evidence;
* semantic inconsistency;
* reconstructive-coherence loss;
* LLM reasoning error.

Those conditions may affect evidence quality.

They do not become CNIG structural conditions without evidence of an actual system difference.

---

## 40. Non-Prescriptive Rule

Domain illustrations do not prescribe:

* system architecture;
* product selection;
* identity design;
* workflow design;
* agent design;
* cloud topology;
* infrastructure configuration;
* security controls;
* remediation;
* deployment;
* production action.

They identify structural questions.

Engineering and governance decisions remain external.

---

## 41. External Application Boundary

External applications may reference CNIG concepts within a domain.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external domain application must not be represented as:

* CNIG itself;
* a canonical domain edition of CNIG;
* an official CNIG implementation;
* a mandatory CNIG architecture;
* a canonical domain pack;
* proof that CNIG guarantees correctness;
* authority to redefine a Primitive, Invariant, or Failure Mode;
* authority to approve or execute system changes.

---

## 42. Domain-Extension Rule

Additional domain illustrations may be created externally where they:

* preserve canonical terminology;
* maintain the fixed Primitive, Invariant, and Failure Mode sets;
* identify themselves as non-canonical;
* remain evidence-grounded;
* avoid automatic domain-to-Failure-Mode mappings;
* preserve the observer boundary;
* preserve the non-operational boundary;
* retain canonical attribution.

Publication or repetition does not make an external domain illustration canonical.

---

## 43. Stability Rule

The domain layer remains coherent when:

* canonical CNIG concepts remain unchanged across domains;
* domain-specific evidence remains explicit;
* domain illustrations remain non-canonical;
* Source States and Transition Paths remain material;
* Reachability remains distinct from Admissibility;
* system behaviour remains distinct from observer understanding;
* domain membership does not imply a Failure Mode;
* Privilege Surface remains bounded to effective authority, capability, control, access, interaction, or resource effect;
* uncertainty remains explicit;
* implementation remains external.

The domain layer degrades when:

* domains become separate CNIG ontologies;
* examples become universal domain claims;
* domain labels substitute for evidence;
* interpretations replace actual system structure;
* each domain is mapped to one Primitive or Failure Mode;
* behavioural space replaces system State;
* external domain implementations are treated as canonical CNIG;
* examples imply operational prescriptions.

---

## 44. Transition to System Limits

The next layer defines CNIG’s applicability, evidence, modelling, attribution, formalization, and implementation limits.

See:

`10_SYSTEM_LIMITS.md`
