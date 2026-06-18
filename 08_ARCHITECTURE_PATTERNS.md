# CNIG Architecture Patterns

Constraint-Native Infrastructure Governance (CNIG)

---

## 1. Purpose of This Layer

This layer describes recurring structural patterns observed in system composition under CNIG reasoning.

These are not architectural blueprints or design templates.

They are **interpretive patterns of how structure behaves under composition pressure**.

---

## 2. Nature of Architecture Patterns

CNIG architecture patterns are:

- recurring structural behaviors in composed systems
- descriptive models of interaction topology
- conceptual observations of system organization under constraints

They are not:

- reference architectures
- implementation patterns
- design recipes
- deployment models

---

## 3. Composition-Centric Patterns

---

### 3.1 Emergent Coupling Pattern

When independently correct components interact, unexpected dependencies emerge through composition rather than explicit design.

Key property:
- coupling is not declared, but emerges structurally

---

### 3.2 Constraint Amplification Pattern

Local constraints, when composed across system boundaries, can produce disproportionate global restriction effects.

Key property:
- constraint interaction is non-linear under composition

---

### 3.3 Hidden Reachability Expansion Pattern

System composition introduces new reachable states not anticipated in isolated component design.

Key property:
- possibility space expands without explicit structural acknowledgment

---

### 3.4 Fragmented Governance Pattern

Multiple local governance interpretations coexist without a unified global admissibility structure.

Key property:
- governance becomes context-dependent across system regions

---

### 3.5 Interaction Topology Drift Pattern

System behavior evolves due to changes in interaction pathways rather than changes in components.

Key property:
- structure evolves through connections, not nodes

---

### 3.6 Stability Under Composition Illusion Pattern

Systems appear stable at component level but degrade under integration due to structural mismatch.

Key property:
- local stability does not imply global stability

---

## 4. Pattern Interpretation Rule

Architecture patterns in CNIG are:

- observational
- descriptive
- structurally derived

They are not:

- design constraints
- implementation rules
- engineering requirements

---

## 5. Relationship to Failure Modes

Architecture patterns often precede or correlate with CNIG failure modes:

- Emergent Coupling → Governance Capture
- Constraint Amplification → Invariant Overconstraint
- Hidden Reachability Expansion → Implicit Reachability Expansion Failure
- Fragmented Governance → Constitutional Fragmentation

Patterns describe *formation conditions*; failure modes describe *outcomes*.

---

## 6. Non-Template Clause

These patterns must not be used as:

- architecture templates
- system design checklists
- reference implementations
- production system guidelines

They are not prescriptive.

They are interpretive.

---

## 7. Transition to Domain Instances

The next layer applies CNIG reasoning across real-world system domains.

See:

`09_DOMAIN_INSTANCES.md`
