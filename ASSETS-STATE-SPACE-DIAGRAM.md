# CNIG State Space Diagram

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Asset

This asset illustrates the relationship between:

* system states
* Reachable State Space
* Admissible System States
* Transition Paths
* Governing Constraints
* Privilege Surface
* Invariant preservation

It is a conceptual representation.

It is not:

* a complete system model
* a state machine
* a simulation
* a probability model
* an execution graph
* a formal proof
* an implementation specification
* a runtime validation mechanism

The diagram illustrates structural distinctions.

It does not calculate or enforce them.

---

## 2. State

Within CNIG, a **State** is a structural system configuration.

A State may include:

* component configuration
* identities
* authority relationships
* permissions
* resources
* dependencies
* topology
* active constraints
* shared state
* temporal phase
* governing boundaries

A State is not limited to a runtime snapshot.

Observed execution may provide evidence that a State was reached.

---

## 3. Reachable State Space

**Reachable State Space** is the complete set of system states that can emerge through the composition of components.

Reachability concerns structural possibility.

A State may become reachable through:

* direct transitions
* accumulated transitions
* delegation
* inheritance
* service interaction
* workflow progression
* cross-domain integration
* shared-state changes
* alternative authority paths
* changed Interaction Topology

Reachability does not establish Admissibility.

---

## 4. Admissible System State

An **Admissible System State** is a reachable State that remains structurally coherent under the constraints governing the composition.

Admissibility may depend on:

* authority boundaries
* exclusions
* separation requirements
* valid Transition Paths
* resource constraints
* Target State requirements
* Governing Intent
* relevant Invariant-preservation requirements

A reachable State may be:

* admissible
* inadmissible
* unresolved because the governing conditions are incomplete or conflicting

---

## 5. Conceptual State-Space Representation

```text
            BOUNDED SYSTEM POSSIBILITY MODEL

    States not established as reachable under the
    represented composition and Source State
    .   .   .   .   .   .   .   .   .   .   .


        +---------------------------------------+
        |         REACHABLE STATE SPACE         |
        |                                       |
        |   × R1            ? R2                |
        |                                       |
        |          +-------------------+        |
        |          | ADMISSIBLE STATES |        |
        |          |                   |        |
        |          |  ● A1     ● A2    |        |
        |          |        ● A3       |        |
        |          +-------------------+        |
        |                                       |
        |   × R3                    ? R4        |
        |                                       |
        +---------------------------------------+
```

### Symbol key

* `●` — reachable and supported as admissible
* `×` — reachable and supported as inadmissible
* `?` — reachable, but Admissibility remains unresolved
* `.` — not established as reachable within the bounded model

The diagram does not assert that every State outside the represented Reachable State Space is impossible.

It indicates only that those States have not been established as reachable under the bounded:

* Source State
* system composition
* Transition Paths
* structural assumptions
* evidence

---

## 6. Critical Distinction: Unreachable Is Not Invalid

A State may be unreachable because:

* no Transition Path exists from the relevant Source State
* required preconditions are absent
* the necessary authority is unavailable
* the relevant components are not connected
* a Governing Constraint prevents the transition
* the represented model does not include the required relationship

That does not necessarily make the State structurally invalid.

A State may be valid or desirable in another:

* Source State
* system composition
* authority structure
* temporal phase
* governance context

The following concepts must remain distinct:

* **not established as reachable**
* **established as unreachable**
* **reachable**
* **admissible**
* **inadmissible**
* **unresolved**

They must not be collapsed into one “invalid” region.

---

## 7. Critical Distinction: Admissible Is Not Identical to Stable

Admissibility and Stability are related but different concepts.

### Admissibility

Concerns whether a reachable State remains structurally coherent under the Governing Constraints of the composition.

### Stability

Concerns whether system deviation remains bounded under structural variation.

A State may be admissible at one point while the surrounding composition remains sensitive to:

* small topology changes
* timing
* concurrency
* authority changes
* dependency changes
* future transitions

An Admissible System State should therefore not be labelled automatically as a “stable subset.”

Stability requires a separate evaluation through the Stability Invariant and relevant evidence.

---

## 8. Reachability Boundary

The Reachability boundary is shaped by the effective composition.

Relevant factors include:

* available components
* relationships
* Transition Paths
* Source State
* authority
* delegation
* resource membership
* topology
* temporal phase
* downstream capability

The boundary may change when the system changes.

For example:

* a new service relationship may expose another Transition Path
* a role relationship may create additional Effective Authority
* a workflow stage may enable another Target State
* a cross-domain integration may connect separate state spaces
* an Intermediate State may enable a later transition

A changed Reachability boundary is a structural system condition.

It is not created by a change in observer perspective.

---

## 9. Admissibility Boundary

The Admissibility boundary is shaped by the Governing Constraints applicable to the composed system.

Relevant factors may include:

* authority limits
* required separation
* prohibited relationships
* resource boundaries
* transition conditions
* Target State requirements
* valid-continuation requirements
* Governing Intent
* relevant Invariant-preservation requirements

The boundary may change where the governing structure itself changes.

A difference in how observers describe a State does not change its Admissibility.

Where governing evidence is incomplete or conflicting, the State should be marked UNRESOLVED rather than placed confidently inside or outside the Admissible region.

---

## 10. Transition-Path Representation

Reachability exists through Transition Paths.

```text
Source State
     |
     v
Transition T1
     |
     v
Intermediate State I1
     |
     v
Transition T2
     |
     v
Intermediate State I2
     |
     v
Transition T3
     |
     v
Target State
```

Each local transition may be valid.

The complete Transition Path may still:

* reach an unrepresented Target State
* expand authority
* alter shared resources
* cross governance boundaries
* weaken an Invariant
* produce an inadmissible result

State Transition Validation must therefore distinguish:

* local transition validity
* complete Transition-Path Admissibility

---

## 11. Expansion of Reachable State Space

Composition may expand Reachable State Space where it introduces:

* a new component relationship
* an alternate Transition Path
* delegated authority
* inherited capability
* service-mediated execution
* a new workflow stage
* a cross-domain mapping
* additional downstream effects
* a new Intermediate State
* changed Interaction Topology

```text
Before composition change:

    +--------------------+
    | Reachable States   |
    |  A1   A2   R1      |
    +--------------------+

After composition change:

    +--------------------------------+
    | Reachable States               |
    |  A1   A2   R1   R2   R3       |
    +--------------------------------+
```

The appearance of `R2` and `R3` does not establish failure.

The analysis must still determine whether those States are:

* represented
* intended
* governed
* authorized
* admissible

Implicit Reachability Expansion Failure requires the complete canonical Failure Mode conditions.

---

## 12. Contraction of Reachable or Admissible Space

Composition may also remove practical paths to intended States.

This may occur through:

* compounded constraints
* lost authority
* dependency changes
* removed recovery paths
* incompatible preconditions
* cross-domain constraint interaction

```text
Intended admissible transitions:

    A1 ---> A2 ---> A3

After structural contraction:

    A1 ---> A2 ---X---> A3
```

The unavailable path may support different conclusions depending on the evidence.

### Invariant Overconstraint

May be relevant where compounded constraints eliminate States or transitions that Governing Intent requires to remain admissible.

### Null State Boundary Violation

May be relevant where the system has reached a State from which no admissible outgoing transition exists.

The two conditions must not be treated as equivalent.

---

## 13. Privilege Surface Overlay

Privilege Surface is the effective Interaction Topology through which composition expands or constrains:

* access
* authority
* capability
* control
* resource effect
* action paths

A Privilege Surface overlay may be represented as follows:

```text
Principal P
    |
    | declared permission
    v
Service S1
    |
    | delegated or service-held authority
    v
Service S2
    |
    | downstream capability
    v
Resource R
```

The complete path may make a resource State reachable even where no single permission independently grants the full capability.

However, generic connectivity is not automatically Privilege Surface.

A relationship belongs to the Privilege Surface only where it materially affects effective:

* interaction
* access
* authority
* capability
* control
* resource effect

---

## 14. Invariant Evaluation Overlay

Invariants do not filter, create, remove, or authorize States.

They support evaluation of whether structural properties remain preserved across a Transition Path or Target State.

```text
Target State
    |
    +--> Identity Invariant evaluation
    |
    +--> Stability Invariant evaluation
    |
    +--> Behavioral Invariant evaluation
    |
    +--> Structural Invariant evaluation
```

Invariant evaluation may identify:

* preserved properties
* conditionally preserved properties
* weakened properties
* conflicting evidence
* unresolved conditions

It does not independently determine Admissibility or establish a Failure Mode.

See:

`ASSETS-INVARIANT-FILTER.md`

---

## 15. Relationship Between the Core Concepts

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
        +-----------------------------+
        |                             |
        v                             v
Governing Constraints          Invariant Evaluation
        |                             |
        +-------------+---------------+
                      |
                      v
            Admissibility Assessment
                      |
                      v
       Evidence-dependent Failure Mode
       attribution, where supported
```

The concepts must not be collapsed.

In particular:

* Reachability is not Admissibility.
* Admissibility is not Stability.
* Connectivity is not Privilege Surface.
* Invariant weakening is not automatically a Failure Mode.
* Execution success is not governance validity.
* An unrepresented State is not automatically inadmissible.
* An unreachable State is not automatically invalid.

---

## 16. Bounded-Model Rule

Every practical State Space diagram is bounded by its:

* system scope
* Source State
* included components
* represented relationships
* time window
* authority model
* governing evidence
* assumptions
* available observations

The asset must not imply that the entire real-world State Space has been exhaustively enumerated.

A bounded model should identify:

* what is included
* what is excluded
* what is assumed
* what is directly evidenced
* what remains unresolved

Model completeness is a claim requiring support.

It must not be inferred from visual neatness.

---

## 17. Non-Simulation Boundary

This diagram must not be treated as:

* an executable state machine
* a runtime graph
* a probability distribution
* a model checker
* a formal verification result
* a production validator
* an enforcement mechanism
* a prediction engine
* a complete system representation

An external model or tool may reference the distinctions illustrated here.

Any implementation remains outside CNIG and does not alter the canonical framework.

---

## 18. Observer Boundary

The State Space described by CNIG concerns actual structural possibility.

It does not change merely because:

* an observer has incomplete information
* different observers disagree
* evidence is fragmented
* a model reconstructs the system incorrectly
* a narrative changes
* semantic coherence weakens

Those conditions may limit confidence in the represented State Space.

They do not themselves alter the actual system’s Reachability or Admissibility.

Where evidence is insufficient, the model should mark the relevant conclusion UNRESOLVED.

---

## 19. Key Structural Insight

The central distinction illustrated by this asset is:

> A State may be structurally reachable through locally valid component relationships while remaining inadmissible under the constraints governing the complete composition.

CNIG therefore asks:

> What States did the composition make reachable?

and:

> Which of those States remain admissible?

---

## 20. Relationship to Invariant Asset

The related asset illustrates how the four CNIG Invariants are evaluated across States and Transition Paths.

See:

`ASSETS-INVARIANT-FILTER.md`

Invariants do not act as State Space filters.

They describe structural properties expected to remain preserved across composition and transition.
