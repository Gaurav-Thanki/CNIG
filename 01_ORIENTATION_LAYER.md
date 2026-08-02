# CNIG Orientation Layer

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer provides an initial orientation for determining whether a system question may warrant CNIG analysis.

It helps a reader identify:

* whether composition is materially relevant;
* whether local correctness is supported or remains unresolved;
* whether the composition changes Reachability, authority, capability, constraints, or valid continuation;
* whether a system-level Admissibility question exists;
* which canonical CNIG file should be consulted next.

This layer does not independently define:

* the CNIG problem class;
* the six Primitives;
* the four Invariants;
* the ten Failure Modes;
* diagnostic methodology;
* operational action.

Definitive applicability conditions are governed by:

`PROBLEM_CLASS.md`

The canonical conceptual definition is governed by:

`02_CONCEPTUAL_CORE.md`

---

## 2. Recognition Signature

The canonical CNIG recognition signature is:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* individual components satisfy, or are materially consistent with, their local specifications;
* local configurations, permissions, policies, or transitions may be valid;
* no single local defect sufficiently explains the complete system-level condition;
* but the composition makes a globally unintended or inadmissible State reachable.

The defining distinction is:

> Local correctness does not establish global Admissibility.

At orientation stage, local correctness may remain:

* established;
* PROVISIONAL;
* CONFLICTING;
* UNRESOLVED.

It must not be presumed merely because no local error is visible.

---

## 3. Minimum Orientation Questions

The shortest useful CNIG orientation consists of two questions:

> What State, authority, capability, resource effect, or Transition Path exists only because these elements are composed?

and:

> Does that composed condition remain admissible under the constraints governing the complete composition?

These questions do not presume failure.

A composition may create:

* intended Reachability;
* represented authority;
* governed capability;
* admissible Target States;
* valid continuation.

CNIG becomes materially relevant where the relationship between composition and Admissibility requires system-level evaluation.

---

## 4. Bounded-System Question

Before evaluating CNIG applicability, identify the bounded system.

Ask:

* What system or subsystem is being examined?
* Which components, services, domains, identities, tools, or agents are included?
* Which resources are included?
* Which governance domains are included?
* What Source State or proposed configuration anchors the analysis?
* What Target State or material system effect is being evaluated?
* What time, version, or temporal phase is relevant?
* Which relationships remain outside the current scope?

CNIG should not be applied to an undefined or unlimited system boundary.

---

## 5. Composition Question

Determine whether composition is necessary to explain the material condition.

Ask:

* Does the outcome depend on relationships between several components?
* Does one component’s output change another component’s transition preconditions?
* Does delegation or inheritance alter authority?
* Does shared state create an additional dependency?
* Does topology create an alternate Transition Path?
* Does downstream execution broaden Effective Capability?
* Do several local transitions accumulate into a Joint State?
* Do several governance regimes apply to the same State or path?
* Does the condition disappear when the components are considered separately?

The presence of several components is not sufficient.

The composition must have a material structural effect.

---

## 6. Material Structural Effects

A CNIG-relevant composition may affect one or more of:

* Reachable State Space;
* available Transition Paths;
* Source-State conditions;
* Intermediate States;
* Target States;
* Effective Authority;
* Effective Capability;
* Privilege Surface;
* Governing Constraints;
* Invariant preservation;
* valid continuation;
* Target-State Admissibility.

Generic complexity, connectivity, or interaction is not enough.

The material structural effect should be identified explicitly.

---

## 7. Local-Correctness Status

Determine what the evidence supports concerning local correctness.

Possible local-correctness evidence may include:

* component tests;
* interface conformance;
* configuration review;
* local policy evaluation;
* authorization results;
* transition records;
* component health;
* expected local outputs.

Classify local correctness as:

* **supported**
* **partially supported**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**
* **not supported**

Do not infer local correctness solely because:

* execution completed;
* monitoring remained green;
* no alert was generated;
* a policy existed;
* a reviewer found no obvious defect;
* the system remained available.

Where a direct local defect sufficiently explains the material outcome, that explanation should remain primary.

---

## 8. Simpler-Explanation Gate

Before proceeding with CNIG analysis, evaluate whether a simpler explanation is sufficient.

Possible explanations include:

* a direct software defect;
* an explicit misconfiguration;
* malformed input;
* hardware failure;
* an unavailable dependency;
* incorrect permission assignment;
* compromised credentials;
* resource exhaustion;
* a direct unauthorized action;
* an explicit policy violation;
* a known operational mistake;
* intended probabilistic behaviour;
* ordinary variation within represented bounds.

A local explanation and a compositional condition may coexist.

The orientation question is:

> Does composition remain necessary to explain the material system-level condition?

CNIG should not replace a sufficient conventional explanation merely because the system is complex.

---

## 9. Reachability Question

Ask what the composition makes structurally possible.

Relevant questions include:

* What States become reachable from the Source State?
* Which Transition Paths become available?
* Which Intermediate States enable later transitions?
* Does authority create an alternate path?
* Does service-held capability broaden the final effect?
* Does topology join previously separate State spaces?
* Does the composition remove a previously available State or continuation?
* Are any reachable States absent from the Structural Model?

Reachability does not establish:

* intention;
* authorization at the global level;
* representation;
* governance;
* Admissibility.

A new reachable State is not automatically a failure.

---

## 10. Admissibility Question

For each material reachable State or path, ask:

* Which Governing Constraints apply?
* What Governing Intent is supported?
* Which authority boundaries apply?
* Which resource boundaries apply?
* Which separation requirements apply?
* Which transition conditions apply?
* Which Target-State conditions apply?
* Which valid-continuation requirements apply?
* Which Invariant-preservation requirements are material?
* Does the composed State remain within those conditions?

Where the governing basis is incomplete or conflicting, preserve:

* **Admissibility PROVISIONAL**
* **Admissibility CONFLICTING**
* **Admissibility UNRESOLVED**

Unexpected or undocumented does not independently mean inadmissible.

---

## 11. Orientation Signals

The following conditions may justify further CNIG analysis:

* local correctness is materially relevant but does not explain the system-level result;
* an unchanged local permission acquires broader downstream capability;
* several bounded authority relationships combine into broader Effective Authority;
* a new Transition Path appears through composition;
* an Intermediate State enables a later unevaluated transition;
* several locally valid stages reach an unassessed Target State;
* separate governance regimes apply to a Joint State;
* declared governance does not constrain the complete path as intended;
* the composition removes every continuation that preserves Admissibility;
* the effective system structure differs materially from the represented Structural Model.

These are orientation signals.

They are not proof of:

* inadmissibility;
* Invariant weakening;
* structural causation;
* a canonical Failure Mode.

---

## 12. Conditions Not Required

CNIG orientation does not require that:

* the State has already occurred;
* the outcome is reproducible;
* the complete system is observable;
* monitoring appears healthy;
* every conventional diagnostic method has been exhausted;
* every component has been formally proven correct;
* a production incident exists;
* an architecture review has passed;
* a Failure Mode has already been selected.

CNIG may be applied prospectively or retrospectively.

---

## 13. Prospective Orientation

Prospective orientation considers a current or proposed composition before the material Target State has been observed.

Possible subjects include:

* a planned integration;
* a new service relationship;
* a proposed authority mapping;
* a workflow change;
* a topology change;
* a migration;
* a failover design;
* a new agent-to-tool path;
* a cross-domain connection;
* a policy interaction;
* a proposed Target State.

Prospective analysis identifies structural possibility.

It does not prove that a State will occur.

---

## 14. Retrospective Orientation

Retrospective orientation begins from execution or system evidence.

Relevant evidence may establish:

* an executed transition;
* an Intermediate State;
* a reached Target State;
* an authority path;
* a resource effect;
* a topology change;
* a temporal phase;
* an unavailable continuation;
* a Joint State.

Execution evidence may establish that a State was reachable.

It does not independently establish:

* local correctness;
* structural causation;
* Governing Intent;
* Target-State Admissibility;
* a canonical Failure Mode.

Observed execution is valid evidence input.

CNIG remains conceptual because it analyses that evidence without executing or controlling the system.

---

## 15. Relationship to Existing Disciplines

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
* transition records;
* authority records;
* topology;
* constraints;
* execution history;
* system-level properties.

CNIG does not replace or rank above them.

It is not a secondary interpretive overlay over those disciplines.

It provides a distinct structural framework centred on composition-induced Reachability and Admissibility.

---

## 16. Orientation vs Canonical Definition

This orientation layer may summarize canonical concepts for navigation.

It may not:

* redefine the problem class;
* rename a Primitive;
* alter Invariant meaning;
* broaden a Failure Mode;
* create new canonical terminology;
* replace evidence requirements;
* override higher-authority files.

Where this file conflicts with:

* `PROBLEM_CLASS.md`
* `02_CONCEPTUAL_CORE.md`
* `03_PRIMITIVES.md`
* `04_FAILURE_MODES.md`
* `GLOSSARY.md`

the relevant canonical file governs.

---

## 17. Orientation vs Diagnostic Methodology

Orientation answers:

> Is CNIG materially relevant to this bounded question?

Diagnostic methodology answers:

> How should the available evidence be analysed through CNIG?

The complete external methodology is defined in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

Orientation does not perform complete:

* Source-State establishment;
* Transition-Path reconstruction;
* Invariant assessment;
* Failure Mode attribution;
* cross-observation correlation;
* provenance management.

It determines whether those activities may be warranted.

---

## 18. Failure Mode Boundary

Do not select a Failure Mode during orientation merely because:

* a word resembles a Failure Mode name;
* the system is complex;
* the outcome is undesirable;
* a State is unrepresented;
* topology changed;
* evidence is fragmented;
* observers disagree;
* execution varied.

Failure Mode attribution requires:

* the relevant Source State;
* the complete Transition Path;
* the Target State;
* the Structural Cause;
* the applicable Governing Constraints;
* the Admissibility Condition;
* evidence of the complete canonical Failure Mode conditions.

A CNIG-relevant case may exist without any supported Failure Mode.

---

## 19. Observer Boundary

CNIG orientation concerns actual system:

* States;
* relationships;
* constraints;
* authority;
* capability;
* Transition Paths;
* Reachability;
* Admissibility.

The following are not CNIG activation conditions by themselves:

* observer disagreement;
* fragmented evidence;
* conflicting narratives;
* semantic inconsistency;
* incomplete reconstruction;
* loss of unified understanding;
* LLM reasoning error.

Those conditions may affect evidence quality.

They become relevant to CNIG only where evidence establishes an actual structural condition in the system.

---

## 20. Orientation Result

A disciplined orientation should conclude with one of:

* **CNIG materially applicable**
* **CNIG provisionally applicable**
* **CNIG not required by current evidence**
* **Applicability CONFLICTING**
* **Applicability UNRESOLVED**

The result should state:

* the bounded system;
* why composition is or is not necessary;
* the status of local correctness;
* the material structural effect;
* the Reachability question;
* the Admissibility question;
* simpler explanations considered;
* evidence still required.

The orientation result is not:

* an approval;
* a diagnosis;
* a risk-acceptance decision;
* an implementation instruction;
* an authorization for action.

---

## 21. Non-Operational Boundary

CNIG orientation does not:

* execute actions;
* approve transitions;
* reject transitions;
* enforce constraints;
* block system changes;
* prescribe remediation;
* authorize production activity;
* control system behaviour.

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external orientation tool must not be represented as:

* CNIG itself;
* a canonical CNIG detector;
* proof of Admissibility;
* proof of a Failure Mode;
* authority to approve or reject system changes.

---

## 22. Recommended Reading Path

After this orientation layer, use:

### Definitive problem-class boundary

`PROBLEM_CLASS.md`

### Canonical conceptual core

`02_CONCEPTUAL_CORE.md`

### Six canonical Primitives

`03_PRIMITIVES.md`

### Ten canonical Failure Modes

`04_FAILURE_MODES.md`

### Canonical terminology and Invariants

`GLOSSARY.md`

### Full diagnostic methodology

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

---

## 23. Closing Principle

CNIG orientation does not begin by asking which Failure Mode is present.

It begins by asking:

> What did the composition make structurally possible?

Then:

> Does the resulting State remain admissible?

Only after those questions are supported should deeper CNIG analysis proceed.
