# CNIG Invariant Evaluation Overlay

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Asset

This asset illustrates how CNIG Invariants may be evaluated across a system state and Transition Path.

The existing filename uses the word **filter**, but CNIG Invariants do not literally filter, remove, transform, or authorize system states.

They describe structural properties expected to remain preserved across:

* system composition
* system boundaries
* authority relationships
* state transitions
* Source States
* Intermediate States
* Target States

This asset is:

* conceptual
* descriptive
* non-operational
* illustrative

It is not:

* a validation engine
* a runtime filter
* an enforcement mechanism
* a policy rule
* an admissibility calculator
* a deterministic correctness test

---

## 2. Conceptual Model

CNIG distinguishes between:

1. what states the composition makes reachable;
2. which governing constraints apply;
3. whether the resulting state remains admissible;
4. which structural properties remain preserved.

The four CNIG Invariants address the fourth question.

They are:

1. **Identity Invariant**
2. **Stability Invariant**
3. **Behavioral Invariant**
4. **Structural Invariant**

Invariant evaluation does not create the Reachable State Space.

It examines whether relevant system properties remain preserved as the system moves through that space.

---

## 3. Evaluation Model

```text
                         REACHABLE STATE SPACE

        Source State
             |
             v
     Initiating transition
             |
             v
      Intermediate States
             |
             v
       Complete Transition Path
             |
             v
         Target State
             |
             +--------------------------------------+
             |                                      |
             v                                      v
   Governing Constraints                    Invariant Evaluation
   and Governing Intent                     --------------------
             |                              Identity
             |                              Stability
             |                              Behavioral
             |                              Structural
             |                                      |
             v                                      v
   Admissibility Evaluation              Preservation Assessment
```

The two evaluations are related but not identical.

A Target State may require both:

* evaluation against Governing Constraints;
* evaluation of the relevant Invariants.

Invariant evaluation contributes evidence to structural analysis.

It does not independently determine Admissibility.

---

## 4. Identity Invariant

### Canonical focus

The Identity Invariant concerns preservation of:

* principal identity
* resource identity
* Authority Lineage
* responsibility
* delegated authority
* attributable action

### Evaluation questions

* Does the same principal remain associated with the same effective identity?
* Is authority traceable across delegation and service-mediated execution?
* Does a resource reference continue to identify the same effective resource?
* Can responsibility for the resulting action be attributed across the complete path?
* Do mappings create non-equivalent identities or authority states?

### Possible weakening conditions

The Identity Invariant may weaken where:

* one principal maps to non-equivalent effective identities
* authority lineage becomes incomplete
* delegation obscures responsibility
* actions occur under authority not represented for the initiator
* the same resource reference resolves to a different effective resource
* equivalent principals acquire materially different authority through structural position

The Identity Invariant concerns actual identity and authority relationships.

It does not concern whether observers describe an identity consistently.

---

## 5. Stability Invariant

### Canonical focus

The Stability Invariant concerns bounded system deviation under structural variation.

### Evaluation questions

* Does a small structural change produce a proportionate system effect?
* Do materially equivalent Source States remain within intended outcome bounds?
* Does a minor dependency change produce an unexpectedly large Target State change?
* Do timing, concurrency, or ordering create unbounded divergence?
* Does a small authority change produce disproportionate capability expansion?

### Possible weakening conditions

The Stability Invariant may weaken where:

* minor topology changes produce materially larger outcomes
* small resource-membership changes alter broad system capability
* equivalent structural conditions produce divergent global results
* retry, ordering, concurrency, or timing creates unbounded variation
* local changes propagate beyond intended structural limits

Stability does not require identical outcomes in every system.

It requires deviation to remain within intended structural and behavioural bounds.

---

## 6. Behavioral Invariant

### Canonical focus

The Behavioral Invariant concerns preservation of the expected relationship between:

* local component behaviour
* and the behaviour of the complete composition

### Evaluation questions

* Do locally correct components produce the expected global result?
* Does the same permitted action retain its represented system-level effect?
* Does changed topology alter global behaviour without changing the components?
* Do equivalent transitions produce materially different Target States?
* Does downstream composition expand the effect of a locally valid operation?

### Possible weakening conditions

The Behavioral Invariant may weaken where:

* locally correct components produce an unintended global outcome
* an unchanged operation produces a broader system effect
* the composition behaves differently despite unchanged component logic
* individually valid transitions accumulate into an unintended Target State
* downstream relationships alter the behavioural scope of a permitted action

The Behavioral Invariant concerns actual system behaviour.

It is not a measure of agreement between descriptions of that behaviour.

---

## 7. Structural Invariant

### Canonical focus

The Structural Invariant concerns preservation of coherent and intended relationships between:

* components
* boundaries
* constraints
* identities
* authority paths
* resources
* transitions
* Source States
* Intermediate States
* Target States
* reachable and admissible states

### Evaluation questions

* Does the effective composition still match the represented Structural Model?
* Have new relationships created unrepresented Transition Paths?
* Do system boundaries preserve their intended structural effect?
* Do separate governance regimes form a coherent rule for Joint States?
* Does the topology preserve intended authority and resource relationships?
* Does a shared reference continue to resolve to the same structural object?

### Possible weakening conditions

The Structural Invariant may weaken where:

* relationships create unrepresented states
* topology creates unintended Transition Paths
* boundaries no longer preserve their intended effect
* constraint regimes become incompatible
* authority paths exceed the represented structure
* a shared reference resolves to non-equivalent structural objects
* the represented system no longer describes the effective composition

---

## 8. Preservation Assessment

Invariant evaluation should not be reduced to a binary pass-or-fail result.

Depending on the available evidence, an Invariant may be assessed as:

* **preserved**
* **conditionally preserved**
* **weakened**
* **not materially implicated**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

### Preserved

Evidence supports that the relevant structural property remains intact across the composition.

### Conditionally preserved

The property remains intact only under identified conditions or boundaries.

### Weakened

Evidence supports a material loss of preservation across the composition or transition.

### Not materially implicated

The Invariant does not appear relevant to the specific structural question.

### PROVISIONAL

Weakening or preservation is plausible, but one or more required conditions remain unsupported.

### CONFLICTING

Available evidence supports materially incompatible conclusions.

### UNRESOLVED

The evidence is insufficient to evaluate the Invariant reliably.

---

## 9. Relationship to Reachable State Space

Invariants do not create or remove states from the Reachable State Space.

They do not convert:

* unreachable states into reachable states
* reachable states into unreachable states
* inadmissible states into admissible states
* admissible states into inadmissible states

They support analysis of whether relevant properties remain preserved across the states and Transition Paths that the composition makes reachable.

A weakening Invariant may provide evidence that:

* a relationship changed
* authority lineage was not preserved
* behaviour exceeded represented bounds
* structural coherence weakened
* a Target State may require further Admissibility evaluation

It does not independently establish a Failure Mode.

---

## 10. Relationship to Admissibility

Admissibility is determined by whether a reachable state remains structurally coherent under the Governing Constraints of the composition.

Invariant evaluation may contribute to that determination where preservation of an Invariant is part of the applicable structural requirement.

However:

* a weakened Invariant does not automatically establish inadmissibility;
* a preserved Invariant does not automatically establish admissibility;
* one preserved Invariant does not compensate for another material structural failure;
* Invariants do not replace Governing Constraints or Governing Intent.

The relevant analysis must identify:

* the Target State
* the applicable Governing Constraints
* the expected Invariant
* the evidence of preservation or weakening
* the resulting Admissibility Condition

Admissibility is not merely a contextual preference or observer judgement.

It requires a supported structural basis.

---

## 11. Relationship to Failure Modes

Invariants and Failure Modes are not opposite versions of the same concept.

They have different roles.

### Invariants

Describe structural properties expected to remain preserved.

### Failure Modes

Describe canonical structural conditions in which composition produces or exposes inadmissibility.

The relationship is many-to-many.

Examples include:

* Reference Drift may weaken Identity and Structural Invariants.
* Constitutional Fragmentation may weaken Structural and Behavioral Invariants.
* Invariant Overconstraint may weaken Stability and Behavioral Invariants.
* Stochastic Drift may weaken Stability and Behavioral Invariants.
* Phase Desynchronization may weaken one or more Invariants depending on the affected state.
* Privilege Surface Expansion Failure may weaken Identity, Structural, or Behavioral Invariants.
* Null State Boundary Violation may represent a terminal breakdown of Stability or Structural Invariants.

These are possible relationships.

They are not automatic mappings.

Failure Mode attribution requires evidence of the complete canonical Failure Mode conditions.

---

## 12. Example Evaluation

Consider a permitted service operation that retains the same authorization rule but begins affecting additional resources through a changed downstream workflow.

### Reachability finding

The operation now makes additional resource states reachable.

### Identity Invariant

May remain preserved if the initiating principal and Authority Lineage remain fully attributable.

### Stability Invariant

May weaken if a small workflow change produces a disproportionate expansion of effect.

### Behavioral Invariant

May weaken if the same permitted operation now produces a materially broader system-level result.

### Structural Invariant

May weaken if the new downstream relationships are absent from the represented Structural Model.

### Admissibility

Remains a separate determination requiring evidence that the expanded effect conflicts with:

* Governing Constraints
* intended resource boundaries
* represented capability scope
* or Governing Intent

### Failure Mode

Privilege Surface Expansion Failure remains only PROVISIONAL until its complete defining conditions are supported.

---

## 13. Non-Enforcement Boundary

CNIG Invariants must not be treated directly as:

* runtime validation rules
* CI/CD gates
* policy conditions
* automated controls
* compliance checks
* production decision rules
* remediation triggers
* deterministic proofs
* monitoring thresholds

An external system may reference an Invariant when constructing its own controls or analysis.

That implementation remains outside CNIG and does not redefine the Invariant.

---

## 14. Observer Boundary

CNIG Invariants concern actual system properties.

They do not evaluate:

* semantic consistency between narratives
* agreement between observers
* reconstructive coherence
* completeness of an observer’s understanding
* whether an LLM interprets the system consistently
* whether fragmented evidence can be recomposed

Those conditions may affect evidence quality.

They do not constitute Invariant weakening unless evidence establishes a corresponding change in actual:

* identity
* authority
* behaviour
* structure
* system state
* transition
* Reachability
* Admissibility

---

## 15. Key Insight

CNIG Invariants do not filter the state space.

They support evaluation of whether essential structural properties remain preserved as the composed system moves through its Reachable State Space.

The governing sequence is:

```text
Composition
    ↓
Reachability
    ↓
Transition Path and Target State
    ↓
Invariant Preservation Assessment
    ↓
Admissibility Evaluation under Governing Constraints
    ↓
Evidence-dependent Failure Mode Attribution, where supported
```

No stage should be silently collapsed into another.

---

## 16. Transition to State-Space Asset

The related asset illustrates the distinction between Reachable State Space and Admissible System State.

See:

`ASSETS-STATE-SPACE-DIAGRAM.md`
