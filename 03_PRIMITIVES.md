# CNIG Primitives

Constraint-Native Infrastructure Governance (CNIG)

---

## 1. Purpose of This Layer

This layer defines the canonical primitives used to reason within CNIG.

Primitives are not components, systems, or implementation targets.

They are **descriptive structures for reasoning about system composition and behavior space**.

---

## 2. Nature of Primitives

CNIG primitives are:

- conceptual reference points
- structural descriptors of system behavior
- stable vocabulary for compositional reasoning

They are not:

- APIs
- services
- runtime objects
- enforceable constraints

---

## 3. Core Primitives

### 3.1 Reachable State Space
The complete set of system states that can emerge under composition of components.

It represents *possibility*, not execution.

---

### 3.2 Admissible System State
A subset of reachable states that remain structurally coherent under system constraints.

Admissibility is defined by structural compatibility, not runtime validation.

---

### 3.3 Constraint-Native Governance
The implicit or explicit structural constraints that shape how system composition behaves.

These constraints operate at the level of system relationships, not execution logic.

---

### 3.4 State Transition Validation (Conceptual)
A reasoning construct describing whether movement between system states preserves structural coherence.

It is not an execution-time validation mechanism.

---

### 3.5 Execution vs Governance Separation
A distinction between:

- execution correctness (local component behavior)
- governance structure (global compositional behavior)

This separation is analytical, not architectural.

---

### 3.6 Privilege Surface
The emergent interaction topology created by system composition.

It describes how system structure expands or constrains interaction pathways between components.

It is not a security model or access control mechanism.

---

## 4. Primitive Relationships

Primitives are not independent.

They interact as follows:

- Reachable State Space defines the boundary of possibility
- Admissible System State defines structural validity within that boundary
- Constraint-Native Governance shapes both boundaries
- State Transition reasoning evaluates movement within the space
- Privilege Surface describes how interaction topology modifies reachability

---

## 5. Stability Principle

Primitives remain stable across domains because they do not encode implementation details.

They describe **structure**, not system instantiation.

This allows CNIG to be applied across heterogeneous systems without modification.

---

## 6. Non-Reduction Clause

Primitives must not be reduced into:

- code constructs
- system architecture diagrams
- runtime enforcement logic
- policy engines

Any such mapping is a projection outside CNIG, not part of CNIG itself.

---

## 7. Transition to Failure Analysis

The next layer defines how systems deviate from admissibility under composition pressure.

See:

`04_FAILURE_MODES.md`
