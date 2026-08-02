# CNIG State and Transition Model

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer defines how CNIG conceptually represents:

* system States;
* Source States;
* Intermediate States;
* Target States;
* Joint States;
* Transitions;
* complete Transition Paths;
* Reachable State Space;
* Admissible System States;
* authority and capability changes;
* temporal phase;
* valid continuation.

The model supports reasoning about structural possibility and Admissibility under composition.

It may be used:

* prospectively, to examine States and Transition Paths that may become reachable;
* retrospectively, to analyse evidence of States and transitions that occurred.

This is a conceptual model.

It is not:

* a runtime state machine;
* an orchestration engine;
* an executable transition calculus;
* a workflow specification;
* a simulation;
* a model checker;
* a deterministic validator;
* a production-control mechanism.

---

## 2. Nature of the State Model

The CNIG State and Transition Model is:

* a bounded representation of relevant system structure;
* a way to distinguish States from Transitions;
* a way to connect Source States to Target States;
* a way to expose material Intermediate States;
* a way to reason about composition-induced Reachability;
* a way to evaluate Target-State Admissibility;
* a way to trace Effective Authority and Effective Capability across a path.

It does not claim that every real system can be represented completely.

Any practical model remains bounded by:

* system scope;
* evidence;
* assumptions;
* time or phase;
* included components;
* represented relationships;
* identified constraints;
* model completeness.

---

## 3. System State

A **State** is:

> a structural configuration of the system at a relevant point within the bounded analysis.

A State may include:

* component configuration;
* component versions;
* identities;
* roles;
* permissions;
* authority relationships;
* delegated authority;
* resources;
* resource membership;
* topology;
* dependencies;
* shared state;
* active Governing Constraints;
* governance boundaries;
* temporal phase;
* available Transition Paths;
* Effective Authority;
* Effective Capability.

A State is not limited to a runtime snapshot.

It may be:

* represented prospectively;
* inferred from structural relationships;
* established through execution evidence;
* partially known;
* conflicting;
* unresolved.

---

## 4. State Identity

Two States should not be treated as equivalent merely because they share:

* the same component names;
* the same visible configuration;
* the same policy text;
* the same user identity;
* the same intended workflow;
* the same observed output.

Material State differences may exist in:

* authority;
* delegation;
* resource membership;
* topology;
* dependency versions;
* temporal phase;
* shared state;
* active constraints;
* service-held capability;
* prior Intermediate States;
* available continuation paths.

State equivalence is a claim requiring support.

This is especially important when evaluating:

* Stochastic Drift;
* Phase Desynchronization;
* alternate Transition Paths;
* repeated execution;
* apparently identical outcomes.

---

# State Roles

## 5. Source State

A **Source State** is:

> the structural configuration from which a transition or Transition Path begins.

The Source State establishes the conditions under which later Reachability is evaluated.

A Source State should identify, where material:

* participating components;
* active versions;
* configuration;
* identity mappings;
* authority;
* permissions;
* resources;
* topology;
* dependencies;
* active Governing Constraints;
* temporal phase;
* earlier transitions whose effects remain present.

A Source State may be:

* established;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

Local correctness must not be inferred solely from the absence of a reported error.

---

## 6. Intermediate State

An **Intermediate State** is:

> a structural configuration reached after the Source State and before the final Target State.

An Intermediate State may materially change:

* transition preconditions;
* authority;
* Effective Capability;
* resource membership;
* shared state;
* topology;
* applicable Governing Constraints;
* available continuation paths;
* later Reachability;
* Target-State Admissibility.

An Intermediate State must not be omitted merely because:

* it was short-lived;
* no component exposed it directly;
* each local stage succeeded;
* the final outcome received more operational attention.

A short-lived Intermediate State may be the condition that makes a later Target State reachable.

---

## 7. Target State

A **Target State** is:

> the structural configuration reached at the end of the Transition Path under analysis.

The Target State should be evaluated separately for:

* Reachability;
* representation in the Structural Model;
* governing constraint coverage;
* authority;
* Effective Capability;
* Invariant preservation;
* Admissibility;
* available continuation.

A Target State being reached establishes that it was reachable under the actual path.

It does not establish that it was:

* intended;
* represented;
* governed;
* admissible;
* stable;
* safe;
* approved.

---

## 8. Joint State

A **Joint State** is:

> a State whose material properties arise from the combined condition of several components, domains, resources, authorities, or governance regimes.

A Joint State may not be represented completely within any one participating component.

Examples include States produced through:

* cross-domain identity mapping;
* shared resources;
* distributed workflows;
* service chains;
* multi-agent interaction;
* separately governed systems;
* accumulated authority;
* cross-system synchronization.

A Joint State is not inherently inadmissible.

Its Admissibility depends on the constraints governing the complete composition.

---

## 9. Contextual Nature of State Roles

Source State, Intermediate State, and Target State are contextual roles.

The same structural State may be:

* a Target State in one bounded analysis;
* a Source State in a later analysis;
* an Intermediate State in a longer Transition Path.

The role depends on:

* the bounded question;
* the selected path;
* the analytical scope;
* the material outcome.

The underlying State and its analytical role must remain distinct.

---

# Reachability and Admissibility

## 10. Reachable State

A **Reachable State** is:

> a State that can emerge from the relevant Source State through an available Transition Path under the effective composition.

A reachable State may emerge through:

* direct execution;
* accumulated local transitions;
* delegation;
* inheritance;
* identity mapping;
* shared-state change;
* service interaction;
* workflow progression;
* changed topology;
* cross-domain integration;
* alternate authority paths;
* downstream capability;
* feedback;
* temporal conditions.

A reachable State is not necessarily:

* valid;
* intended;
* represented;
* authorized at the global level;
* admissible.

The phrase **valid composition** must not be used as a prerequisite for Reachability.

An inadmissible State may still be structurally reachable.

---

## 11. Admissible State

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

Admissibility does not mean simply:

* executable;
* permitted locally;
* stable;
* healthy;
* available;
* successful;
* expected.

It is a distinct structural determination.

---

## 12. Inadmissible State

An **inadmissible State** is:

> a reachable State that conflicts with the supported constraints governing the complete composition.

A State should be classified as inadmissible only where the analysis identifies:

* the relevant State;
* the applicable Governing Constraints;
* the supported Governing Intent;
* the material structural conflict;
* the evidence supporting that conflict.

The term **invalid State** should not be used as a generic substitute.

“Invalid” may ambiguously refer to:

* component validation failure;
* malformed input;
* policy rejection;
* unreachable configuration;
* runtime error;
* structural inadmissibility.

CNIG should use the more precise term required by the evidence.

---

## 13. Unresolved Admissibility

A reachable State may have unresolved Admissibility where:

* Governing Intent is unsupported;
* constraints conflict;
* the relevant boundary is unclear;
* the Source State is incomplete;
* the Transition Path is only partially known;
* authority cannot be traced;
* the Target State is incompletely represented;
* evidence belongs to different temporal phases.

Use:

* **Admissibility PROVISIONAL**
* **Admissibility CONFLICTING**
* **Admissibility UNRESOLVED**

Do not force a binary admissible/inadmissible conclusion where the structural basis is insufficient.

---

## 14. Admissibility Is Not Stability

Admissibility and Stability must remain distinct.

### Admissibility

Concerns whether a reachable State remains coherent under Governing Constraints.

### Stability

Concerns whether system deviation remains bounded under structural variation.

A State may be admissible at a particular point while the system remains sensitive to:

* small topology changes;
* timing;
* concurrency;
* dependency changes;
* future transitions;
* authority changes.

An Admissible System State must not be defined automatically as a stable State.

Stability requires separate evaluation through the Stability Invariant.

---

# Transitions

## 15. Transition

A **Transition** is:

> a structural change from one State to another.

A Transition may change:

* component configuration;
* identity;
* authority;
* permissions;
* resource membership;
* topology;
* dependencies;
* shared state;
* Governing Constraints;
* temporal phase;
* Effective Capability;
* available continuation paths.

A Transition is not itself a State.

The former category **Transitional State** should not be used to describe movement.

Where a structural configuration exists between two transitions, it is an Intermediate State.

---

## 16. Possible and Observed Transitions

A Transition may be:

* structurally possible but not observed;
* represented in the Structural Model;
* inferred from supported relationships;
* observed through execution evidence;
* executed successfully;
* attempted but not completed;
* locally rejected;
* unresolved.

CNIG does not claim that transitions are never executed.

Actual systems execute actions that may produce structural transitions.

The conceptual model represents those transitions without becoming an execution mechanism.

---

## 17. Transition Preconditions

A Transition may depend on:

* a particular Source State;
* identity;
* authority;
* permission;
* resource condition;
* dependency availability;
* prior Intermediate State;
* temporal phase;
* topology;
* governing approval;
* external event;
* service-held capability.

A transition being available in one State does not establish that it is available in another.

Transition availability must be evaluated against the material Source State.

---

## 18. Transition Effect

A Transition may have effects beyond the component that performs it.

Relevant effects may include:

* a new reachable State;
* changed authority;
* expanded Effective Capability;
* altered resource membership;
* changed topology;
* a new downstream path;
* weakened constraint authority;
* removal of a valid continuation;
* activation of a later transition.

The local output of a transition may therefore be insufficient to represent its complete system-level effect.

---

## 19. Transition Path

A **Transition Path** is:

> the complete sequence of transitions and Intermediate States connecting a Source State to a Target State.

```text
Source State S0
      ↓
Transition T1
      ↓
Intermediate State S1
      ↓
Transition T2
      ↓
Intermediate State S2
      ↓
Transition T3
      ↓
Target State S3
```

A Transition Path may cross:

* component boundaries;
* identity boundaries;
* authority boundaries;
* policy boundaries;
* governance domains;
* resource boundaries;
* temporal phases;
* trust boundaries.

The complete path—not only the initiating action—must be considered when evaluating Admissibility.

---

## 20. Alternate Transition Paths

The same Target State may be reachable through several paths.

Different paths may involve:

* different authority;
* different Intermediate States;
* different constraints;
* different services;
* different temporal phases;
* different resource effects;
* different Invariant consequences.

A Target State being admissible through one path does not automatically establish that every path to it is admissible.

Likewise, one inadmissible path does not automatically establish that the Target State is inadmissible under every possible composition.

The bounded path and Governing Constraints must be explicit.

---

## 21. Local Transition Validity

**Local transition validity** concerns whether one component or stage accepts and completes its own transition according to local conditions.

Local validity may establish that:

* input conditions were satisfied;
* permission was accepted;
* the component acted according to specification;
* the local output was produced;
* the local contract was satisfied.

It does not establish:

* complete Transition-Path validity;
* preservation of Governing Intent;
* Target-State Admissibility;
* absence of authority expansion;
* preservation of all Invariants.

---

## 22. Complete Transition-Path Validity

**Complete Transition-Path validity** concerns whether the accumulated sequence:

* remains under valid authority;
* preserves relevant Governing Constraints;
* preserves applicable Invariants;
* represents material resource effects;
* accounts for Intermediate States;
* reaches an admissible Target State.

Every local transition may be valid while the complete path remains inadmissible.

This is a central CNIG distinction.

---

## 23. State Transition Validation

**State Transition Validation** is the conceptual evaluation of whether movement through a Transition Path preserves structural coherence and Admissibility.

It may evaluate:

* Source State;
* transition preconditions;
* initiating authority;
* Intermediate States;
* authority changes;
* Effective Capability changes;
* resource effects;
* applicable Governing Constraints;
* Invariant preservation;
* Target State;
* valid continuation.

State Transition Validation is not:

* a runtime validator;
* an API routine;
* a pipeline gate;
* a workflow engine;
* an automated approval mechanism;
* a production control.

---

# Authority, Capability, and Topology

## 24. Authority Across State Transitions

Authority may change during a Transition Path.

Relevant changes include:

* direct assignment;
* inheritance;
* nested membership;
* delegation;
* token exchange;
* service-held authority;
* identity mapping;
* transitive authority;
* cross-domain authority recognition.

The authority that initiates a path may differ from the authority that produces the final resource effect.

Authority Lineage should therefore be traced across all material States and transitions.

---

## 25. Effective Capability Across State Transitions

Effective Capability is the complete action or system effect available through the composed path.

A local permission may lead to broader capability through:

* downstream service authority;
* tool access;
* agent delegation;
* workflow continuation;
* resource relationships;
* cross-domain mappings;
* alternate paths.

The State model should represent capability changes where they materially affect:

* Reachability;
* Privilege Surface;
* Governing Constraints;
* Target-State Admissibility.

---

## 26. Privilege Surface

Privilege Surface is the effective Interaction Topology through which composition expands or constrains:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect;
* action paths.

Within the State model, Privilege Surface may change when:

* a State adds a new authority relationship;
* an Intermediate State enables a downstream service;
* a transition grants inherited or delegated capability;
* topology exposes another protected resource;
* a cross-domain mapping creates another action path.

Generic connectivity is not sufficient.

The topology must materially affect effective authority, capability, control, access, interaction, or resource effect.

---

# Constraints and Invariants

## 27. Governing Constraints in a State

A State may contain or be subject to Governing Constraints concerning:

* authority;
* permitted relationships;
* prohibited relationships;
* separation requirements;
* resource scope;
* transition conditions;
* Target-State requirements;
* valid continuation;
* temporal phase;
* capability boundaries.

The model should distinguish:

* declared constraints;
* represented constraints;
* implemented constraints;
* effective constraints.

The presence of a declared rule does not establish that it constrains every path or State in the complete composition.

---

## 28. Constraint Changes Across a Path

A Governing Constraint may:

* remain unchanged and effective;
* remain declared but lose effective authority;
* change scope;
* apply only in one domain;
* conflict with another governance regime;
* become stale relative to the system phase;
* fail to cover a Joint State;
* remove an intended continuation.

Constraint changes may therefore affect both:

* Reachability;
* Admissibility.

---

## 29. Invariant Evaluation

The four CNIG Invariants are:

1. Identity Invariant
2. Stability Invariant
3. Behavioral Invariant
4. Structural Invariant

Invariant evaluation asks whether relevant system properties remain preserved across:

* Source State;
* Intermediate States;
* Transition Path;
* Target State.

Invariants do not:

* create States;
* remove States;
* execute transitions;
* filter the State space;
* independently establish Admissibility;
* automatically establish a Failure Mode.

An Invariant may be assessed as:

* preserved;
* conditionally preserved;
* weakened;
* not materially implicated;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

---

# Temporal Structure

## 30. Temporal Phase

Time may be a material property of actual system structure.

A **temporal phase** may include:

* active configuration generation;
* policy version;
* identity propagation state;
* replicated-resource state;
* deployment phase;
* transition ordering;
* lease or token validity;
* control-plane convergence;
* governance effective period.

Temporal phase is not merely an interpretive perspective.

A system State at one phase may differ materially from a visually similar State at another phase.

---

## 31. Phase Alignment

A Transition should be evaluated against the structural conditions effective during that transition.

Relevant questions include:

* Which State existed when the transition began?
* Which policy version applied?
* Had authority changes propagated?
* Had topology converged?
* Which resource version was active?
* Did governance and execution refer to the same phase?
* Did an Intermediate State belong to another phase?

Delayed observer awareness does not itself create Phase Desynchronization.

Phase Desynchronization requires an actual temporal mismatch in system State, authority, topology, constraints, or governance conditions that changes Reachability or Admissibility.

---

## 32. Concurrency and Ordering

Concurrent or differently ordered transitions may create different Intermediate States or Target States.

The model should consider, where material:

* transition order;
* concurrency;
* retries;
* queues;
* asynchronous propagation;
* race conditions;
* delayed constraint application;
* replicated State.

Different outcomes under apparently similar conditions do not establish Stochastic Drift until material State and phase differences are evaluated.

---

# Reachability Change

## 33. Reachability Expansion

Reachable State Space may expand when composition introduces:

* a new relationship;
* an alternate Transition Path;
* delegated authority;
* inherited capability;
* a new Intermediate State;
* downstream service effects;
* changed topology;
* cross-domain integration;
* changed resource membership.

Reachability expansion is not automatically a failure.

The new State or path may be:

* intended;
* represented;
* governed;
* admissible.

Implicit Reachability Expansion Failure requires its complete canonical defining conditions.

---

## 34. Reachability Contraction

Practical Reachability may contract when composition:

* removes authority;
* compounds constraints;
* removes a dependency;
* eliminates a transition;
* removes a recovery path;
* creates incompatible preconditions;
* disconnects State spaces.

Contraction may be:

* intended;
* required;
* admissible;
* excessive;
* unresolved.

Reachability contraction does not automatically establish Invariant Overconstraint or Null State Boundary Violation.

---

## 35. No Admissible Continuation

A State may be reached from which:

* executable transitions remain;
* but no available transition preserves Admissibility.

This condition is distinct from:

* ordinary unavailability;
* stopped execution;
* a component crash;
* an unreachable desired State;
* temporary resource exhaustion.

Null State Boundary Violation may be relevant only where its full canonical conditions are supported.

A State with no admissible continuation should not be classified automatically without evidence concerning:

* available outgoing transitions;
* Governing Constraints;
* valid-continuation requirements;
* Target-State conditions.

---

# Evidence and Model Limits

## 36. Relationship to Evidence

The State model does not generate evidence.

Evidence may establish:

* a State;
* a transition;
* an Intermediate State;
* authority use;
* a resource effect;
* topology;
* temporal phase;
* a Target State;
* a valid continuation.

Material conclusions should distinguish:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

A visually complete diagram is not proof that the real system has been modelled completely.

---

## 37. Bounded-Model Rule

Every practical CNIG State model is bounded by:

* a selected Source State;
* included components;
* represented relationships;
* identified authority;
* included resources;
* time window;
* temporal phase;
* available evidence;
* assumptions;
* the analytical question.

The model should identify:

* what is included;
* what is excluded;
* what is assumed;
* what is supported;
* what remains unresolved.

A bounded model must not be presented as the complete real-world Reachable State Space unless that claim is independently supported.

---

## 38. Unknown and Unrepresented States

The model must distinguish between:

* a State known to be reachable;
* a State inferred to be reachable;
* a State represented as reachable;
* a State reached through evidence;
* a State not yet evaluated;
* a State supported as unreachable;
* a State absent from the model.

Absence from the Structural Model does not prove:

* impossibility;
* inadmissibility;
* non-existence.

Likewise, representation in the model does not prove:

* actual Reachability;
* effective authority;
* Admissibility.

---

## 39. Observer Boundary

The State model concerns actual system structure.

It does not classify, by themselves:

* observer disagreement;
* fragmented evidence;
* conflicting narratives;
* incomplete understanding;
* semantic incoherence;
* reconstructive-coherence loss;
* LLM reasoning error.

Those conditions may limit confidence in the represented model.

They do not themselves change actual:

* State;
* authority;
* topology;
* Transition Paths;
* Reachability;
* Admissibility.

Where the evidence is insufficient, the model should preserve an UNRESOLVED conclusion.

---

# Canonical Relationships

## 40. Relationship to the Six Primitives

### Reachable State Space

Defines the complete structural possibility space generated by composition.

### Admissible System State

Identifies reachable States that remain coherent under Governing Constraints.

### Constraint-Native Governance

Shapes:

* relationships;
* authority;
* available Transition Paths;
* Reachability;
* Admissibility.

### State Transition Validation

Evaluates the complete path from Source State to Target State.

### Execution vs Governance Separation

Prevents successful local execution from being treated as proof of Target-State Admissibility.

### Privilege Surface

Describes topology that changes effective authority, capability, access, control, interaction, or resource effect.

All six Primitives are materially represented in the State model.

---

## 41. Relationship to Failure Modes

The State model may provide evidence relevant to Failure Mode attribution.

For example:

* unrepresented Reachability expansion may support analysis of Implicit Reachability Expansion Failure;
* changed effective capability may support analysis of Privilege Surface Expansion Failure;
* temporal mismatch may support analysis of Phase Desynchronization;
* incompatible governing conditions for a Joint State may support analysis of Constitutional Fragmentation;
* absence of admissible continuation may support analysis of Null State Boundary Violation.

These relationships are not automatic classifications.

A Failure Mode requires evidence of its complete canonical conditions.

---

## 42. State Model Relationship

The conceptual relationship may be represented as:

```text
Bounded Source State
        ↓
Available Transition Paths
        ↓
Intermediate States
        ↓
Target State
        ↓
Reachability Finding
        ↓
Governing Constraints
        +
Invariant Evaluation
        ↓
Admissibility Finding
        ↓
Failure Mode Attribution,
where supported
```

This representation is conceptual.

It is not an executable workflow.

---

# Non-Operational Boundary

## 43. Non-Execution Rule

The State model does not:

* execute transitions;
* approve transitions;
* block transitions;
* enforce constraints;
* calculate production permission;
* control system behaviour;
* remediate States;
* guarantee outcomes.

It represents and analyses structural relationships.

---

## 44. External Representation

External applications may represent CNIG State concepts through:

* diagrams;
* schemas;
* evidence graphs;
* formal models;
* software abstractions;
* databases;
* analytical tools.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external representation must not be treated as:

* CNIG itself;
* the canonical executable State model;
* proof of complete Reachability;
* proof of Admissibility;
* authority to redefine State, Transition, or a Primitive;
* authority to approve or execute system changes.

---

## 45. Stability Rule

The State model remains coherent when:

* a State remains distinct from a Transition;
* Source, Intermediate, and Target roles remain explicit;
* Reachability remains distinct from Admissibility;
* Admissibility remains distinct from Stability;
* local transition validity remains distinct from complete Transition-Path validity;
* actual transitions may be represented without making CNIG operational;
* temporal phase remains an actual system property;
* authority and capability changes remain traceable;
* uncertainty remains explicit;
* Failure Mode attribution remains evidence-dependent;
* observer understanding remains distinct from system structure;
* implementation remains external.

The State model degrades when:

* reachable States are presumed valid or admissible;
* transitions are treated as States;
* execution evidence is excluded from structural analysis;
* “invalid” replaces precise classification;
* time becomes an observer-centred concept;
* local success is treated as complete-path validity;
* generic connectivity becomes Privilege Surface;
* the model is presented as an execution engine;
* external implementations redefine canonical concepts.

---

## 46. Transition to Architecture Patterns

The next layer describes recurring structural patterns that may appear across composed systems.

See:

`08_ARCHITECTURE_PATTERNS.md`
