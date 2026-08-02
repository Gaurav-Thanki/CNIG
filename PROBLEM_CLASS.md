# The Problem Class CNIG Addresses

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Recognition Signature

CNIG addresses:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* individual components satisfy, or are materially consistent with, their local specifications;
* local configurations, permissions, policies, and transitions may be valid;
* no single local defect sufficiently explains the complete system-level condition;
* but the composition makes a globally unintended or inadmissible State reachable.

The defining distinction is:

> Local correctness does not establish global Admissibility.

CNIG therefore asks:

> What did the composition make reachable?

and:

> Did the resulting State remain admissible under the constraints governing the complete composition?

---

## 2. The Structural Condition

The CNIG problem class exists where the material system-level condition depends on relationships between components rather than on one component alone.

Relevant relationships may include:

* service interaction;
* delegation;
* inheritance;
* identity mapping;
* shared state;
* workflow sequencing;
* downstream execution;
* resource dependency;
* cross-domain integration;
* changed topology;
* accumulated transitions;
* authority composition;
* constraint interaction.

The decisive condition is not merely that several components are present.

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

## 3. Local Correctness

Within the recognition signature, **component-correct** means that local correctness is materially relevant to the problem being examined.

Local correctness may concern:

* component behaviour;
* configuration;
* local authorization;
* local transition validity;
* interface conformance;
* policy evaluation;
* workflow-stage acceptance;
* local resource effects.

In a completed retrospective analysis, local correctness should be supported by evidence.

During an initial or prospective analysis, it may remain:

* established;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

CNIG must not infer local correctness merely because:

* no error was reported;
* monitoring remained green;
* execution completed;
* a policy existed;
* a reviewer found no defect;
* the system remained available.

Where a direct component defect sufficiently explains the material outcome, that explanation should remain primary.

CNIG is not a mechanism for relabelling ordinary local failure as compositional failure.

---

## 4. Composition-Inadmissibility

A composition-inadmissible condition exists where:

1. a State or Transition Path is structurally reachable through the effective composition;
2. the State or path conflicts with the supported constraints governing the complete composition;
3. the material conflict cannot be explained adequately within one local component boundary.

The condition should identify:

* the bounded system;
* the relevant Source State;
* participating components;
* the complete Transition Path;
* material Intermediate States;
* the Target State;
* the structural relationship that made the State reachable;
* applicable Governing Constraints;
* supported Governing Intent;
* the resulting Admissibility Condition.

A State being:

* unexpected;
* undocumented;
* unanticipated;
* undesirable;
* unfamiliar;
* difficult to explain

does not independently establish inadmissibility.

Inadmissibility requires a supported governing basis.

---

## 5. Reachability Is Not Admissibility

A State may be:

* reachable and admissible;
* reachable but inadmissible;
* reachable with Admissibility unresolved;
* represented but unreachable;
* absent from the Structural Model but structurally reachable.

CNIG does not treat every expansion of Reachable State Space as failure.

A newly reachable State may be:

* intended;
* represented;
* authorized;
* governed;
* admissible.

The problem class becomes material where composition creates or exposes a reachable State whose relationship to Governing Intent requires system-level evaluation.

---

## 6. The Minimum CNIG Question

The minimum CNIG question is:

> What State, authority, capability, resource effect, or Transition Path exists only because these elements are composed?

The necessary second question is:

> Does that composed condition remain admissible?

These questions move analysis beyond isolated component boundaries without presuming that the composition has failed.

---

## 7. Applicability Conditions

CNIG may be materially applicable where several of the following are supported:

* several components, services, domains, identities, tools, or agents participate in the material outcome;
* local correctness is supported or materially relevant;
* no single local defect sufficiently explains the complete condition;
* the effective composition differs materially from the represented Structural Model;
* composition introduces or removes a Transition Path;
* composition changes Effective Authority or Effective Capability;
* an unchanged local permission acquires broader downstream effects;
* several locally valid transitions accumulate into an unevaluated Target State;
* separate governance regimes apply to a shared or Joint State;
* declared governance does not constrain the complete composition as intended;
* a State has no available continuation that preserves Admissibility;
* the central question concerns why the system structure permits a result rather than only why one component acted.

CNIG applicability may remain PROVISIONAL while evidence is incomplete.

---

## 8. Conditions That Are Not Required

CNIG does not require that:

* the behaviour has already occurred;
* the behaviour is reproducible;
* the behaviour is fully observable;
* every standard diagnostic method has been exhausted;
* every component has been formally proven correct;
* the architecture review passed;
* the configuration is known to be perfect;
* a production incident exists;
* a canonical Failure Mode has already been identified.

CNIG may be used prospectively before a State is executed.

It may also be used retrospectively where execution evidence reveals a material structural relationship or Transition Path.

---

## 9. Prospective Application

Prospective CNIG analysis asks what the current or proposed composition may make reachable.

It may examine:

* a planned integration;
* a proposed authority relationship;
* a new workflow stage;
* a service dependency;
* a cross-domain mapping;
* a topology change;
* a new agent-to-tool path;
* a migration;
* a failover design;
* a policy interaction;
* a proposed Target State.

Prospective analysis does not prove that a State will occur.

It identifies structural possibility and evaluates the represented Admissibility conditions.

---

## 10. Retrospective Application

Retrospective CNIG analysis begins from evidence of:

* an executed Transition Path;
* a reached Target State;
* an authority path;
* a resource effect;
* a topology change;
* an unavailable continuation;
* a Joint State;
* a system-level outcome.

Execution evidence may establish that a State was reachable.

It does not independently establish:

* local correctness;
* structural causation;
* Governing Intent;
* Target-State Admissibility;
* a canonical Failure Mode.

Those conclusions require separate evidence.

---

## 11. Simpler Sufficient Explanations

CNIG should not displace a simpler sufficient explanation.

Examples include:

* a direct software defect;
* an explicit misconfiguration;
* an incorrect permission assignment;
* malformed input;
* hardware failure;
* resource exhaustion;
* an unavailable dependency;
* message loss;
* an explicit policy violation;
* compromised credentials;
* a direct unauthorized action;
* a known operational mistake;
* intended probabilistic behaviour;
* ordinary variation within represented bounds.

A local explanation and a compositional condition may coexist.

The analysis should determine whether composition remains necessary to explain the material system-level result.

---

## 12. Relationship to Observability

Observability may provide evidence concerning:

* States;
* transitions;
* topology;
* authority use;
* resource effects;
* execution order;
* temporal phase;
* system outcomes.

CNIG does not replace observability.

Observability also does not automatically provide:

* the complete Reachable State Space;
* every alternate Transition Path;
* Governing Intent;
* Target-State Admissibility;
* complete authority lineage;
* complete Structural Model coverage.

The relationship depends on the scope and quality of the observability system.

CNIG should not claim that observability is inherently incapable of supporting compositional analysis.

---

## 13. Relationship to Testing

Testing may evaluate:

* local component behaviour;
* interfaces;
* integration paths;
* system-level transitions;
* properties of composed systems;
* expected Target States;
* prohibited States.

CNIG does not assume that testing is limited to isolated components or pairwise interaction.

Testing may provide strong evidence about Reachability and execution behaviour.

Its conclusions remain bounded by:

* tested Source States;
* represented paths;
* test coverage;
* assumptions;
* environment;
* temporal conditions.

Passing tests do not establish the Admissibility of every structurally reachable State.

Failing tests do not automatically establish a CNIG condition.

---

## 14. Relationship to Formal Methods

Formal methods may represent and verify:

* component properties;
* transition systems;
* composed systems;
* invariants;
* Reachability;
* safety properties;
* temporal properties;
* authority relationships.

CNIG does not claim that formal verification is inherently limited to component boundaries.

A formal model may provide powerful evidence for CNIG analysis.

Its conclusions remain bounded by:

* model scope;
* assumptions;
* represented components;
* represented relationships;
* completeness of constraints;
* correspondence between the model and the effective system.

Formalization remains external to CNIG.

It does not alter the canonical framework.

---

## 15. Relationship to Policy and Enforcement Systems

Policy-as-code and other enforcement systems may:

* encode constraints;
* evaluate requests;
* block transitions;
* establish evidence;
* limit authority;
* constrain resource effects.

CNIG does not assume that such systems can govern only anticipated States.

Their effectiveness depends on:

* policy scope;
* represented relationships;
* enforcement coverage;
* authority;
* complete Transition Paths;
* downstream effects;
* Joint States;
* temporal alignment.

A policy being present does not establish that it governs the complete composition.

A policy system may nevertheless provide or implement effective compositional constraints.

That implementation remains outside CNIG.

---

## 16. Relationship to Architecture and Systems Engineering

Architecture and systems-engineering methods may represent:

* components;
* relationships;
* interfaces;
* authority;
* constraints;
* State transitions;
* dependencies;
* failure conditions;
* system-level properties.

CNIG does not claim that architecture methods are inherently unable to represent Reachability or composition.

CNIG contributes a bounded vocabulary and problem framing centred on:

* component-correct composition;
* Reachable State Space;
* Admissible System States;
* State Transition Validation;
* Execution vs Governance Separation;
* Privilege Surface;
* canonical Invariants;
* canonical Failure Modes.

It may be used alongside existing architecture and systems-engineering practices.

---

## 17. Domain Illustrations

The problem class may appear in many domains.

Illustrative possibilities include:

### Distributed systems

Locally valid service transitions may accumulate into a Joint State absent from one service’s model.

### Identity and access systems

Several bounded authority relationships may combine into broader Effective Authority or Effective Capability.

### Orchestration and workflow systems

Individually accepted stages may reach a Target State that no stage evaluates globally.

### AI and multi-agent systems

Agents, tools, identities, and services may compose into a resource-effect path broader than the initiating agent’s represented capability.

### Infrastructure and cloud systems

Topology, control planes, automation, identity, and resource relationships may create a management or recovery State not represented within one component boundary.

These are hypothetical structural possibilities.

Domain membership does not establish CNIG applicability or a Failure Mode.

---

## 18. What CNIG Does Not Address by Itself

The following are not CNIG conditions by themselves:

* observer disagreement;
* fragmented evidence;
* inconsistent narratives;
* semantic incoherence;
* incomplete reconstruction;
* loss of unified understanding;
* LLM reasoning error;
* uncertainty about what happened;
* different observers describing the same State differently.

Those conditions may affect the quality of evidence.

They become relevant to CNIG only where evidence establishes an actual structural difference involving:

* identity;
* authority;
* constraints;
* State;
* temporal phase;
* Transition Path;
* Reachability;
* Admissibility.

The actual system condition—not the observer’s difficulty reconstructing it—is CNIG’s analytical object.

---

## 19. Failure Mode Boundary

CNIG applicability does not require that a canonical Failure Mode be established.

A system may be within the CNIG problem class while:

* no Failure Mode is yet supported;
* several Failure Modes remain PROVISIONAL;
* evidence supports competing classifications;
* the relevant condition is best recorded as UNRESOLVED.

Failure Mode attribution must follow the complete canonical definitions in:

`04_FAILURE_MODES.md`

The problem class must not be reduced to a keyword match against a Failure Mode name.

---

## 20. Applicability Result

A disciplined applicability assessment should conclude with one of:

* **CNIG materially applicable**
* **CNIG provisionally applicable**
* **CNIG not required by current evidence**
* **Applicability CONFLICTING**
* **Applicability UNRESOLVED**

The conclusion should state:

* the bounded system;
* why composition is or is not necessary;
* the status of local correctness;
* the relevant Reachability question;
* the relevant Admissibility question;
* simpler explanations considered;
* material evidence still required.

---

## 21. Non-Operational Boundary

Identifying a system as CNIG-relevant does not authorize:

* a configuration change;
* a policy change;
* an identity change;
* an access change;
* remediation;
* deployment;
* production approval;
* enforcement;
* autonomous action.

CNIG provides structural analysis.

Authority and action remain external.

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

---

## 22. Canonical Problem Statement

The canonical problem statement is:

> CNIG addresses component-correct, composition-inadmissible systems: systems in which each component satisfies its local specification, yet their composition makes a globally unintended or inadmissible State reachable without requiring a component fault, explicit policy violation, or conventional misconfiguration.

This statement identifies the problem class.

It does not assert that:

* every component is formally proven correct;
* every unintended State is inadmissible;
* every complex-system outcome belongs to CNIG;
* conventional tools are incapable of compositional analysis;
* CNIG replaces existing systems disciplines.

---

## 23. Closing Principle

The shortest reliable recognition rule is:

> Do not stop at whether each component worked.

Ask:

> What did their composition make possible?

Then determine:

> Whether the resulting State remained admissible.
