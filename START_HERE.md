# START HERE

**Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki**

CNIG is a conceptual framework for reasoning about admissible system states within Reachable State Space under composition constraints prior to execution.

It may also be applied retrospectively to execution evidence where observed behaviour reveals a structural State, relationship, or Transition Path.

---

## 1. What This Repository Defines

This repository defines the canonical public form of Constraint-Native Infrastructure Governance.

CNIG addresses:

> **Component-correct, composition-inadmissible systems.**

These are systems in which:

* individual components satisfy their local specifications;
* local configurations, permissions, policies, and transitions may be valid;
* no single component fault explains the complete outcome;
* but the composition makes a globally unintended or inadmissible State reachable.

The central distinction is:

> Local correctness does not establish global admissibility.

CNIG therefore asks:

> What did the composition make reachable?

and:

> Did the resulting State remain admissible under the constraints governing the complete composition?

---

## 2. What CNIG Examines

CNIG examines actual system:

* components
* relationships
* constraints
* identities
* authority paths
* permissions
* capabilities
* Source States
* Intermediate States
* Target States
* Transition Paths
* Reachable State Space
* Admissible System States
* governing boundaries

Its primary analytical object is the composed system and the States made structurally reachable through component relationships.

CNIG is not primarily concerned with:

* how observers understand the system;
* how evidence is reconstructed;
* whether narratives remain semantically coherent;
* whether different descriptions agree.

Those conditions may affect evidence quality.

They do not replace analysis of the actual system structure.

---

## 3. What CNIG Is Not

CNIG is not:

* a software product
* a runtime system
* a system architecture
* a policy engine
* an enforcement mechanism
* a monitoring framework
* an incident-management taxonomy
* a compliance framework
* a certification mechanism
* a deployment methodology
* an executable specification
* a formal verification system
* a production decision authority
* an autonomous controller

CNIG itself does not:

* execute actions;
* approve transitions;
* enforce constraints;
* remediate systems;
* guarantee outcomes.

It is a conceptual framework.

The methodology used to apply it to observational evidence is defined separately in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

---

## 4. When CNIG Is Relevant

CNIG may be relevant where:

* several components or domains participate in an outcome;
* components remain locally valid or correct;
* local transitions succeed;
* no direct component fault sufficiently explains the global result;
* composition changes Reachability, authority, capability, or constraint effect;
* a Target State may fall outside Governing Intent;
* the decisive structural cause cannot be located within one component boundary.

Examples include:

* valid identity assignments combining into broader Effective Authority;
* an unchanged permission acquiring wider downstream capability;
* individually valid pipeline stages reaching an unevaluated Target State;
* service topology creating new Transition Paths;
* separately governed systems reaching a Joint State neither governs completely;
* declared governance remaining present while losing effective constraint authority.

CNIG should not displace a simpler sufficient explanation.

Where a conventional defect, direct misconfiguration, explicit policy violation, or known component failure adequately explains the outcome, that explanation should remain primary unless additional evidence establishes a compositional condition.

---

## 5. Recognition Test

A problem may warrant CNIG analysis where the answer to all three questions is materially significant:

### 1. Is composition necessary to explain the outcome?

Does the outcome depend on relationships between components rather than one component alone?

### 2. Did composition alter structural possibility?

Did it change:

* Reachability;
* authority;
* Effective Capability;
* Transition Paths;
* constraint effect;
* or available continuation States?

### 3. Is there an Admissibility question?

Is there evidence that the resulting State or path may conflict with:

* Governing Constraints;
* authority boundaries;
* exclusions;
* separation requirements;
* Target State requirements;
* valid-continuation requirements;
* or Governing Intent?

Where these questions cannot be answered from the evidence, the result should remain PROVISIONAL or UNRESOLVED.

---

## 6. Minimal Entry Vocabulary

The following concepts provide the shortest useful entry into CNIG.

### Reachable State Space

The complete set of system States that can emerge through component composition.

It concerns structural possibility.

### Admissible System State

A reachable State that remains structurally coherent under the constraints governing the composition.

Reachability does not establish Admissibility.

### Constraint-Native Governance

The implicit or explicit structural constraints that shape:

* relationships;
* authority;
* interaction boundaries;
* Transition Paths;
* Reachability;
* permissible configurations.

### State Transition Validation

Conceptual evaluation of whether movement between system States preserves structural coherence and remains within the admissible State space.

### Execution vs Governance Separation

The distinction between:

* whether execution succeeds locally;
* whether the resulting composed State remains within Governing Intent.

### Privilege Surface

The effective Interaction Topology through which composition expands or constrains:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

Generic connectivity does not automatically constitute Privilege Surface.

---

## 7. Recommended Reading Path

The repository is accessible non-linearly, but canonical authority is not flat.

For a reliable first reading, use the following path.

### Step 1 — Recognition surface

`README.md`

Read this first for:

* the recognition signature;
* the core problem;
* the canonical vocabulary;
* the framework boundary;
* the repository map.

### Step 2 — Canonical identity

`00_CANONICAL_IDENTITY.md`

Use this for:

* framework identity;
* exact name;
* authorship;
* canonical attribution.

### Step 3 — Problem class

`PROBLEM_CLASS.md`

Use this to determine:

* what condition CNIG addresses;
* when CNIG is applicable;
* when another explanation is more appropriate;
* how local correctness differs from global Admissibility.

### Step 4 — Conceptual core

`02_CONCEPTUAL_CORE.md`

Use this for:

* the canonical framework definition;
* the primary structural distinction;
* the relationship between composition, Reachability, and Admissibility;
* the non-operational boundary.

### Step 5 — Primitives

`03_PRIMITIVES.md`

Use this for the six canonical Primitives:

1. Reachable State Space
2. Admissible System State
3. Constraint-Native Governance
4. State Transition Validation
5. Execution vs Governance Separation
6. Privilege Surface

### Step 6 — Failure Modes

`04_FAILURE_MODES.md`

Use this for:

* the ten canonical Failure Modes;
* their defining structural conditions;
* distinctions between similar Failure Modes;
* evidence requirements for attribution.

### Step 7 — Glossary and Invariants

`GLOSSARY.md`

Use this for:

* canonical terminology;
* the four canonical Invariants;
* architecture patterns;
* diagnostic states;
* important conceptual distinctions.

The four Invariants are:

1. Identity Invariant
2. Stability Invariant
3. Behavioral Invariant
4. Structural Invariant

### Step 8 — System limits

`10_SYSTEM_LIMITS.md`

Use this for limits involving:

* applicability;
* evidence;
* Structural Model completeness;
* causation;
* scale;
* dynamic systems;
* formalization;
* prediction;
* Failure Mode attribution;
* implementation claims.

### Step 9 — Interpretation boundary

`11_INTERPRETATION_GUIDE.md`

Use this to preserve:

* canonical meaning;
* ontology boundaries;
* distinction between system structure and observer understanding;
* separation between CNIG and adjacent frameworks.

### Step 10 — Diagnostic methodology

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

Use this when analysing actual evidence.

It defines an external methodology for:

* evidence intake;
* applicability testing;
* Source-State establishment;
* Transition-Path mapping;
* Reachability evaluation;
* Admissibility evaluation;
* Invariant assessment;
* Failure Mode attribution;
* cross-observation correlation;
* diagnostic-state assignment.

CNIG remains a conceptual framework.

File 12 is a methodology for applying it.

### Step 11 — Conceptual assets

* `ASSETS-STATE-SPACE-DIAGRAM.md`
* `ASSETS-INVARIANT-FILTER.md`

These files illustrate canonical distinctions.

They do not introduce new Primitives, Invariants, or Failure Modes.

### Step 12 — Observation files

`OBS_*` files provide illustrative structural cases.

They may demonstrate:

* identity composition;
* authority aggregation;
* pipeline-state accumulation;
* service topology;
* cross-domain composition;
* silent Reachability expansion;
* governance displacement;
* Privilege Surface change.

Observation files are non-canonical.

They may illustrate the framework but cannot redefine it.

---

## 8. Canonical Authority

CNIG files do not carry equal definitional authority.

Where wording conflicts, use the following hierarchy:

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

A lower layer may:

* illustrate;
* contextualize;
* organize;
* or apply

a canonical concept.

It may not silently:

* rename it;
* broaden it;
* narrow it;
* merge it;
* reorder it;
* replace it;
* or import another framework’s ontology into it.

---

## 9. How to Use CNIG in Analysis

A disciplined CNIG analysis should begin with evidence, not taxonomy.

The basic analytical sequence is:

```text
Evidence
    ↓
Source State
    ↓
System Composition
    ↓
Transition Path
    ↓
Target State
    ↓
Reachability Evaluation
    ↓
Admissibility Evaluation
    ↓
Invariant Assessment
    ↓
Failure Mode Attribution, where supported
```

Do not begin by selecting a Failure Mode and searching for matching symptoms.

Instead determine:

* what State existed;
* what relationships were active;
* what Transition Path occurred;
* what the composition made reachable;
* what Governing Constraints applied;
* whether the resulting State remained admissible.

Failure Mode attribution comes after those conditions are established.

---

## 10. Diagnostic States

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

A Failure Mode should not be forced where the evidence does not support one.

---

## 11. Relationship to Existing Disciplines

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

* execution evidence;
* system models;
* configuration records;
* constraints;
* authority records;
* topology;
* dependency maps;
* Transition Paths;
* state history.

CNIG does not replace them.

It also does not operate as a secondary or superior layer over them.

It provides a distinct structural framework for examining composition-induced Reachability and Admissibility.

---

## 12. External Application Boundary

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external application must not be treated as:

* CNIG itself;
* the canonical implementation of CNIG;
* proof that CNIG guarantees correctness;
* authority to redefine a Primitive, Invariant, or Failure Mode;
* evidence that CNIG executes or enforces governance.

Applying CNIG concepts externally does not make the conceptual framework operational.

It creates an external application whose validity depends on its own:

* evidence;
* assumptions;
* authority;
* implementation;
* validation;
* accountability.

---

## 13. Framework Boundary

CNIG concerns actual system structure.

It does not classify, by themselves:

* observer disagreement;
* fragmented evidence;
* conflicting narratives;
* incomplete understanding;
* semantic inconsistency;
* reconstructive-coherence loss;
* LLM reasoning error;
* difficulty combining distributed information.

Those conditions may limit evidence quality.

They become relevant to CNIG only where evidence establishes an actual difference in:

* identity mapping;
* authority;
* structural reference;
* constraint scope;
* temporal phase;
* Source State;
* Transition Path;
* Reachability;
* Admissibility.

The condition in the system—not disagreement about it—is the CNIG analytical object.

---

## 14. First Questions for a New Case

When examining a potential CNIG case, begin with:

1. What is the bounded system under analysis?
2. What was the relevant Source State?
3. Which components and relationships formed the composition?
4. What complete Transition Path produced the Target State?
5. What new State, authority, capability, or path became reachable?
6. Which Governing Constraints applied?
7. Was the resulting State admissible?
8. Which Invariants were materially implicated?
9. Does the evidence support a canonical Failure Mode?
10. What remains PROVISIONAL, CONFLICTING, or UNRESOLVED?

These questions structure analysis.

They do not execute or authorize system changes.

---

## 15. Canonical Attribution

Use the following exact attribution:

> **Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki**

The canonical names and ordering of the six Primitives, four Invariants, and ten Failure Modes must remain stable.

---

## 16. Closing Principle

CNIG becomes relevant where locally correct parts compose into a globally unintended or inadmissible reachable State.

The shortest reliable reading rule is:

> Do not stop at whether each component worked.

Ask:

> What did their composition make possible?
