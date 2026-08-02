# CNIG Overview

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. What CNIG Is

Constraint-Native Infrastructure Governance (CNIG) is a conceptual framework for reasoning about:

> admissible system states within reachable state space under composition constraints prior to execution.

CNIG examines how the structure of a composed system determines:

* what states can become reachable
* which reachable states remain admissible
* how valid local transitions combine into system-level outcomes
* how interaction topology changes effective capability
* whether governing constraints remain effective across composition

Its primary object of analysis is the **composed system and its structurally reachable states**.

CNIG is not itself a methodology.

A methodology may be used to apply CNIG, but the framework remains a bounded conceptual ontology consisting of Primitives, Invariants, Failure Modes, and structural relationships.

---

## 2. The Problem Class CNIG Addresses

CNIG becomes relevant when:

* components behave correctly according to their local specifications
* configurations and policies may be valid as written
* individual transitions may complete successfully
* no single component fault explains the outcome
* but the composition makes an unintended or inadmissible system state reachable

The distinctive condition is:

> **Component-correct, composition-inadmissible systems.**

In such systems, local correctness does not establish global admissibility.

A state may become reachable through the interaction of:

* services
* identities
* roles
* policies
* pipelines
* agents
* tools
* infrastructure boundaries
* delegated authority
* shared resources
* independently governed systems

without any one component independently introducing the complete result.

The central CNIG question is therefore not only:

> Is each component correct?

It is:

> What system states become reachable when these correct components interact, and which of those states remain admissible?

---

## 3. Reachability and Admissibility

CNIG distinguishes two structural conditions.

### Reachability

Reachability concerns what the composition makes possible.

A state may become reachable through:

* direct transitions
* accumulated transitions
* interaction paths
* inherited relationships
* delegation
* aggregation
* cross-system mappings
* downstream effects
* changes in system topology

Reachability does not establish that the state was intended or structurally acceptable.

### Admissibility

Admissibility concerns whether a reachable state remains structurally coherent under the constraints governing the composition.

A state may be:

* reachable and admissible
* reachable but inadmissible
* represented but unreachable
* absent from the represented state model yet structurally reachable

The gap between reachable and admissible states is central to CNIG.

Not every new state, interaction, or capability is a failure.

A structural failure condition arises only where the resulting state or path is inconsistent with governing constraints, intended structural boundaries, or admissibility conditions.

---

## 4. Why Local Correctness Is Insufficient

Components normally validate conditions within their own boundaries.

A component may confirm that:

* its input is valid
* its action is permitted
* its transition completed
* its output satisfies its local contract
* its health and configuration remain correct

But a composed outcome may depend on relationships that no component represents in full.

For example:

* several valid identity assignments may produce a broader effective authority state
* an unchanged permission may acquire a wider downstream effect
* valid pipeline stages may reach an unvalidated target state
* correct services may create new transition paths through changed topology
* separately governed systems may create a joint state neither evaluates
* declared governance may remain present while losing structural constraint effect

CNIG addresses the structural distance between local validation and global outcome.

---

## 5. Core Primitives

CNIG uses six canonical Primitives.

### Reachable State Space

The complete set of system states that can emerge through component composition.

It describes structural possibility, not only states already executed or observed.

### Admissible System State

The subset of reachable states that remains structurally coherent under the constraints governing the composition.

A reachable state is not necessarily admissible.

### Constraint-Native Governance

The implicit or explicit structural constraints that shape system relationships, interaction boundaries, and permissible configurations.

These constraints describe governing structure. They are not necessarily runtime enforcement mechanisms.

### State Transition Validation

A conceptual reasoning construct for evaluating whether movement between system states preserves structural coherence and remains within the admissible state space.

It is not an execution-time validator.

### Execution vs Governance Separation

The analytical distinction between:

* whether components and transitions execute correctly
* whether the resulting composed state remains within governing intent

Execution success does not establish governance validity.

### Privilege Surface

The emergent interaction topology created through composition.

It describes how relationships between components can expand or constrain effective interaction, access, authority, capability, or control pathways.

Privilege Surface is a structural concept, not an access-control product or security mechanism.

---

## 6. Invariants

CNIG uses four Invariants to describe properties that should remain preserved across system composition.

### Identity Invariant

Preservation of identity, authority lineage, responsibility, and attributable action across representations and system boundaries.

### Stability Invariant

Bounded system deviation under structural variation.

The invariant weakens where small compositional changes produce disproportionately large system effects.

### Behavioral Invariant

Preservation of the expected relationship between local component behaviour and the resulting behaviour of the composition.

### Structural Invariant

Preservation of coherent and intended relationships between components, constraints, boundaries, and system states.

Invariants are descriptive analytical concepts.

They are not runtime checks, enforcement rules, or implementation requirements.

---

## 7. Failure Modes

CNIG defines ten canonical compositional Failure Modes:

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

Failure Modes describe structural conditions that may arise under composition.

They are not:

* monitoring alerts
* incident severity levels
* operational labels
* automatic diagnoses
* implementation patterns

A Failure Mode should not be assigned merely because a system is complex, interconnected, dynamic, or producing an unexpected outcome.

The relevant structural conditions must first be established.

---

## 8. Relationship to Execution

CNIG reasons about structural possibility prior to and independently of whether a state has already been executed or observed.

This does not limit CNIG to design-time analysis.

Observed system behaviour may provide evidence that a state or transition path is reachable.

CNIG then asks:

* what composition made that state reachable
* whether the state was represented
* which constraints govern it
* whether the state remains admissible
* which Primitives, Invariants, or Failure Modes are implicated

Execution can reveal the reachable state space.

Execution success does not define admissibility.

---

## 9. How CNIG Is Applied

CNIG may be used to structure analysis of:

* distributed systems
* identity and authority composition
* service interaction topology
* CI/CD and orchestration chains
* multi-agent and tool-mediated systems
* cross-domain integrations
* policy and governance structures
* infrastructure dependency relationships
* privilege and capability expansion
* structural change over time

The observation files in this repository provide illustrative evidence patterns.

They are not independent definitions of CNIG and do not override the canonical framework files.

Diagnostic interpretation is described separately in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

That document defines a methodology for interpreting observational evidence through CNIG.

It does not redefine CNIG as a methodology.

---

## 10. What CNIG Is Not

CNIG is not:

* a runtime system
* a software architecture
* a policy engine
* an enforcement mechanism
* a compliance product
* a monitoring framework
* an incident-management taxonomy
* a deployment framework
* an executable specification
* a formal verification system
* a theory of observer disagreement
* a framework for reconstructive or semantic coherence

CNIG does not execute actions, enforce constraints, validate production transitions, or provide operational guarantees.

Any implementation that operationalizes CNIG concepts is an external projection or derivative, not the conceptual framework itself.

---

## 11. Framework Boundary

CNIG concerns actual system structure and the states made reachable through composition.

Its analytical objects include:

* components
* relationships
* constraints
* authority paths
* source states
* target states
* transitions
* reachable states
* admissible states
* governing boundaries

A condition does not become a CNIG problem merely because:

* different observers describe the system differently
* evidence is fragmented
* interpretations conflict
* system understanding is incomplete
* semantic coherence weakens
* a model reconstructs the system incorrectly

Those conditions are outside CNIG unless they provide evidence of, or produce, an actual structural change in the system’s reachable or admissible state space.

CNIG evaluates the structure itself, not the coherence with which an observer reconstructs it.

---

## 12. Relationship to Other Systems Disciplines

CNIG can coexist with:

* architecture analysis
* formal methods
* verification tools
* policy-as-code
* observability
* security engineering
* distributed-systems analysis
* identity governance
* systems safety
* operational diagnostics

It does not replace those disciplines.

They may provide:

* component specifications
* execution evidence
* constraint definitions
* state observations
* dependency information
* authority records
* transition history

CNIG uses such information to reason about structural reachability and admissibility under composition.

---

## 13. Canonical Navigation

Use the following files as the primary framework references:

* `00_CANONICAL_IDENTITY.md` — canonical identity and attribution
* `PROBLEM_CLASS.md` — the precise problem class CNIG addresses
* `02_CONCEPTUAL_CORE.md` — canonical framework definition
* `03_PRIMITIVES.md` — canonical Primitives
* `04_FAILURE_MODES.md` — canonical Failure Modes
* `GLOSSARY.md` — canonical terminology
* `11_INTERPRETATION_GUIDE.md` — interpretation boundaries
* `12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md` — diagnostic application methodology

Observation files are illustrative and non-canonical.

Where an observation appears inconsistent with a canonical definition, the canonical framework file governs.

---

## 14. Stability Statement

CNIG remains coherent when it is used to reason about:

* component-correct but composition-inadmissible systems
* reachable versus admissible states
* structural effects of interaction topology
* cumulative transition consequences
* authority and capability paths
* preservation of governing constraints
* local correctness versus global outcome

CNIG degrades when it is treated as:

* an implementation architecture
* an execution engine
* a universal theory of system failure
* an observer-centred coherence framework
* a substitute for evidence or domain expertise
* an automatic justification for assigning a Failure Mode

Its scope remains deliberately bounded.

---

## 15. Closing Principle

CNIG is defined by a structural distinction:

> A system may be composed entirely of locally correct parts while still making a globally unintended or inadmissible state reachable.

The question is not only what the system executed.

The question is what its composition made possible.
