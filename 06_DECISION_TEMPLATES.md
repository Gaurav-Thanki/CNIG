# CNIG Analytical Decision Templates

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer provides structured templates for recording CNIG analysis in a decision context.

The templates may support:

* prospective architecture evaluation;
* comparison of structural options;
* evaluation of a proposed system transition;
* retrospective examination of a prior decision;
* documentation of Reachability and Admissibility findings;
* preservation of evidence, assumptions, uncertainty, and competing explanations;
* communication of CNIG analysis to an external decision authority.

The templates do not make decisions.

They organize structural analysis that an external decision process may consider.

CNIG remains a conceptual framework.

Decision authority, approval, implementation, and action remain outside CNIG.

---

## 2. Nature of the Templates

CNIG analytical decision templates are:

* structured recording formats;
* evidence-discipline aids;
* option-comparison aids;
* structural-analysis summaries;
* provenance records;
* uncertainty-preservation mechanisms.

They are not:

* approval workflows;
* policy-enforcement logic;
* compliance controls;
* certification criteria;
* CI/CD gates;
* production decision engines;
* risk-acceptance authority;
* remediation instructions;
* implementation specifications;
* autonomous governance systems.

Completing a template does not establish that:

* the evidence is complete;
* a proposed State is admissible;
* an option is approved;
* a Failure Mode exists;
* an action is authorized;
* a system change is safe.

---

## 3. Canonical Dependency Rule

These templates apply canonical concepts defined elsewhere.

They do not redefine them.

Canonical definitions remain governed by:

* `02_CONCEPTUAL_CORE.md`
* `03_PRIMITIVES.md`
* `04_FAILURE_MODES.md`
* `GLOSSARY.md`
* `10_SYSTEM_LIMITS.md`
* `11_INTERPRETATION_GUIDE.md`

The full external methodology for applying CNIG to evidence is defined in:

`12_CNIG_DIAGNOSTIC_INTERPRETATION_METHODOLOGY.md`

Where this file conflicts with a canonical definition, the canonical layer governs.

---

## 4. Separation of Analysis and Decision

A CNIG analytical record and an external decision record are different objects.

### CNIG analytical record

May state:

* what the evidence supports;
* what the composition makes reachable;
* which Governing Constraints apply;
* whether Admissibility is supported;
* which Invariants may be preserved or weakened;
* whether a Failure Mode is established, provisional, conflicting, or unresolved;
* what evidence remains missing.

### External decision record

May state:

* who has authority to decide;
* what option was selected;
* what risks were accepted;
* what implementation was approved;
* what validation or rollback conditions apply;
* who is accountable.

CNIG does not supply the authority for the second record.

A favourable CNIG analysis does not authorize action.

An unfavourable or unresolved CNIG analysis does not itself prohibit action.

Those consequences belong to an external governance process.

---

# Template A — Bounded Decision Context

## 5. Decision Context Header

Use this section to define the question before evaluating options.

### Decision identifier

`[External decision or analysis identifier]`

### Decision question

`[What external choice, proposed transition, or structural question is being evaluated?]`

### Bounded system

`[System, subsystem, service composition, infrastructure domain, workflow, or authority boundary included in the analysis]`

### Included components

* `[Component or domain]`
* `[Component or domain]`

### Excluded components

* `[Excluded component or domain]`
* `[Reason for exclusion]`

### Relevant time or phase

`[Time window, version, release, system phase, or effective date]`

### Target State or material outcome

`[State or system effect whose Reachability and Admissibility are being evaluated]`

### External decision authority

`[Role, body, owner, or process that holds actual decision authority]`

### CNIG role

`Structural analysis only. No decision authority is supplied by CNIG.`

---

## 6. Applicability Statement

Record one of:

* **CNIG materially applicable**
* **CNIG provisionally applicable**
* **CNIG not required by current evidence**
* **Applicability UNRESOLVED**

### Structural basis

`[Explain why composition is or is not necessary to analyse the material outcome.]`

### Simpler sufficient explanations considered

* `[Direct component fault]`
* `[Explicit misconfiguration]`
* `[Conventional defect]`
* `[Explicit policy violation]`
* `[Known operator action]`
* `[Other local explanation]`

### Applicability limitation

`[State what evidence would strengthen, weaken, or eliminate the need for CNIG analysis.]`

---

# Template B — Evidence and Claim Record

## 7. Evidence Inventory

| Evidence item | Source     | Relevant phase | Authority for claim   | Status             | Limitation     |
| ------------- | ---------- | -------------- | --------------------- | ------------------ | -------------- |
| `[Evidence]`  | `[Source]` | `[Phase/time]` | `[Why authoritative]` | `[OBSERVED/other]` | `[Limitation]` |
| `[Evidence]`  | `[Source]` | `[Phase/time]` | `[Why authoritative]` | `[OBSERVED/other]` | `[Limitation]` |

---

## 8. Claim Classification

Every material claim should use one of the following diagnostic states:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

| Claim     | Diagnostic state | Supporting evidence | Inference path | Conflicting evidence | Remaining uncertainty |
| --------- | ---------------- | ------------------- | -------------- | -------------------- | --------------------- |
| `[Claim]` | `[State]`        | `[Evidence]`        | `[Reasoning]`  | `[Conflict]`         | `[Uncertainty]`       |

Assumptions must be recorded separately.

### Assumptions

* `[Assumption]`
* `[Why it is necessary]`
* `[Effect if false]`

An assumption is not evidence.

---

# Template C — Source-State Record

## 9. Source State

### Source-State description

`[Describe the structural configuration from which the proposed or observed Transition Path begins.]`

### Components and versions

* `[Component/version]`

### Active configurations

* `[Configuration]`

### Identities and roles

* `[Identity, role, group, or mapping]`

### Authority and permissions

* `[Direct, inherited, delegated, service-held, or transitive authority]`

### Resources and memberships

* `[Resource or membership condition]`

### Topology and dependencies

* `[Relationship or dependency]`

### Governing Constraints

* `[Constraint]`

### Temporal phase

`[System phase represented by the Source State]`

### Unresolved Source-State conditions

* `[Condition]`

### Source-State status

* **Established**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

A decision comparison that assumes equivalent Source States must support that equivalence explicitly.

---

# Template D — Option or Transition Representation

## 10. Option Definition

Complete this section separately for each option.

### Option identifier

`[Option A, Option B, proposed transition, current-state continuation, or other alternative]`

### Option description

`[Describe the structural change without presenting it as approved.]`

### Intended Target State

`[State the intended resulting system configuration.]`

### Intended governing purpose

`[Supported Governing Intent associated with the option.]`

### Components affected

* `[Component]`

### Relationships added

* `[Relationship]`

### Relationships removed

* `[Relationship]`

### Authority changes

* `[Authority change]`

### Capability changes

* `[Effective Capability change]`

### Resource effects

* `[Resource effect]`

### Constraint changes

* `[Governing Constraint change]`

### Boundary changes

* `[Identity, authority, trust, policy, resource, governance, or temporal boundary change]`

---

## 11. Complete Transition Path

Represent the proposed or observed path.

```text
Source State
    ↓
Transition T1
    ↓
Intermediate State I1
    ↓
Transition T2
    ↓
Intermediate State I2
    ↓
Transition T3
    ↓
Target State
```

For every material step, record:

| Stage     | Local owner | Authority used | State change | Resource effect | Constraint applied | Evidence status |
| --------- | ----------- | -------------- | ------------ | --------------- | ------------------ | --------------- |
| `[T1/I1]` | `[Owner]`   | `[Authority]`  | `[Change]`   | `[Effect]`      | `[Constraint]`     | `[State]`       |

### Local transition validity

`[What evidence supports or contradicts validity at each local stage?]`

### Complete Transition-Path validity

`[What evidence supports or contradicts preservation of Governing Constraints across the complete path?]`

### Target-State Admissibility

`[Separate assessment; do not infer from local transition success.]`

---

# Template E — Primitive Evaluation

## 12. Reachable State Space

### States or paths introduced

* `[State or Transition Path]`

### States or paths removed

* `[State or Transition Path]`

### Alternate paths created

* `[Alternate path]`

### Intermediate States enabling later transitions

* `[Intermediate State]`

### Previously separate State spaces joined

* `[State spaces or domains]`

### Reachable States absent from the Structural Model

* `[State]`

### Reachability status

For each material State, record:

* known reachable;
* inferred reachable;
* represented as reachable;
* reached through execution evidence;
* not yet evaluated;
* supported as unreachable within the bounded model.

A new reachable State is not automatically inadmissible.

---

## 13. Admissible System State

For each material Target State, record:

### Governing Constraints

* `[Constraint]`

### Governing Intent

`[Supported intended structural boundary]`

### Authority boundaries

* `[Boundary]`

### Separation requirements

* `[Requirement]`

### Resource boundaries

* `[Boundary]`

### Transition conditions

* `[Condition]`

### Valid-continuation requirements

* `[Requirement]`

### Relevant Invariant requirements

* `[Invariant-preservation requirement]`

### Admissibility conclusion

Select one:

* **reachable and admissible**
* **reachable but inadmissible**
* **Admissibility PROVISIONAL**
* **Admissibility CONFLICTING**
* **Admissibility UNRESOLVED**

### Evidential basis

`[Explain the structural basis for the conclusion.]`

Do not use “safe” as a substitute for Admissibility.

Admissibility does not establish every form of:

* operational safety;
* security;
* reliability;
* regulatory compliance;
* business acceptability;
* implementation correctness.

---

## 14. Constraint-Native Governance

### Declared governance

`[Rules, policies, architecture statements, agreements, or authority declarations]`

### Represented governance

`[Constraints represented in the Structural Model]`

### Implemented governance

`[Externally implemented constraints, where evidenced]`

### Effective governing structure

`[What actually constrains the complete composition]`

### Coverage gaps

* `[Transition Path, boundary, State, authority path, or Joint State not fully governed]`

### Governance conclusion

* **Effective across bounded composition**
* **Conditionally effective**
* **Evidence of weakened constraint authority**
* **CONFLICTING**
* **UNRESOLVED**

The continued existence of a rule does not prove its effective authority.

---

## 15. State Transition Validation

Record whether the analysis covers:

* Source State;
* initiating condition;
* material Intermediate States;
* complete Transition Path;
* transition authority;
* changes in authority;
* resource effects;
* Governing Constraints;
* relevant Invariants;
* Target State;
* resulting Reachability;
* valid continuation;
* Target-State Admissibility.

### Validation conclusion

`[State what was evaluated and what remains unsupported.]`

This is conceptual analysis.

It is not an execution-time approval or production gate.

---

## 16. Execution vs Governance Separation

### Execution findings

* `[Local specification result]`
* `[Authentication result]`
* `[Authorization result]`
* `[Workflow result]`
* `[Component health result]`

### Governance findings

* `[Complete-path relationship to Governing Intent]`
* `[Target-State Admissibility]`
* `[Coverage of downstream effects]`
* `[Coverage of Joint States]`
* `[Preservation of authority boundaries]`

### Separation conclusion

`[Explain why execution findings do or do not support governance findings.]`

Do not use local execution success as proof of global Admissibility.

---

## 17. Privilege Surface

### Effective interaction paths

* `[Path]`

### Effective authority paths

* `[Path]`

### Effective capability paths

* `[Path]`

### Downstream resource effects

* `[Effect]`

### Delegated, inherited, or service-held authority

* `[Authority]`

### Paths absent from the represented authority structure

* `[Path]`

### Governing boundary

`[State the intended authority or capability boundary.]`

### Privilege Surface conclusion

* **No material change supported**
* **Material change supported and represented**
* **Material change supported but Admissibility unresolved**
* **Potential unintended expansion PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

Generic connectivity is not sufficient evidence of Privilege Surface change.

The topology must affect effective:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect.

---

# Template F — Invariant Assessment

## 18. Invariant Record

| Invariant            | Expected preserved property | Evidence     | Assessment     | Effect on Admissibility | Uncertainty     |
| -------------------- | --------------------------- | ------------ | -------------- | ----------------------- | --------------- |
| Identity Invariant   | `[Property]`                | `[Evidence]` | `[Assessment]` | `[Effect]`              | `[Uncertainty]` |
| Stability Invariant  | `[Property]`                | `[Evidence]` | `[Assessment]` | `[Effect]`              | `[Uncertainty]` |
| Behavioral Invariant | `[Property]`                | `[Evidence]` | `[Assessment]` | `[Effect]`              | `[Uncertainty]` |
| Structural Invariant | `[Property]`                | `[Evidence]` | `[Assessment]` | `[Effect]`              | `[Uncertainty]` |

Use one assessment for each materially relevant Invariant:

* **preserved**
* **conditionally preserved**
* **weakened**
* **not materially implicated**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

A weakened Invariant does not automatically establish:

* inadmissibility;
* a Failure Mode;
* causal attribution.

A preserved Invariant does not automatically establish Admissibility.

---

# Template G — Failure Mode Sensitivity and Attribution

## 19. Attribution Rule

Do not begin with:

> Does this option introduce a named Failure Mode?

Begin with:

> Does the evidence support the complete defining conditions of any canonical Failure Mode?

The ten canonical Failure Modes are:

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

---

## 20. Failure Mode Candidate Record

Complete this section for each evidence-supported candidate.

### Candidate Failure Mode

`[Canonical name]`

### Observed outcome

`[Supported outcome]`

### Structural Cause

`[Composition relationship that made the outcome reachable]`

### Source State

`[Supported Source State]`

### Target State

`[Supported Target State]`

### Transition Path

`[Relevant path]`

### Governing Constraint

`[Constraint]`

### Admissibility Condition

`[Why the resulting State or path may conflict with Governing Intent]`

### Implicated Primitives

* `[Primitive]`

### Affected Invariants

* `[Invariant]`

### Defining conditions supported

* `[Condition]`

### Defining conditions missing

* `[Condition]`

### Competing explanations

* `[Explanation]`

### Attribution state

Select one:

* **ESTABLISHED through current evidence**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**
* **NOT SUPPORTED**

“Established” applies to the bounded analysis and available evidence.

It is not a universal or permanent classification.

---

## 21. Classification Safeguards

Confirm that the Failure Mode is not being assigned merely because:

* its name resembles the symptom;
* the system is complex;
* the outcome is undesirable;
* a new State is reachable;
* governance is imperfect;
* connectivity increased;
* execution varied;
* evidence is fragmented;
* observers disagree;
* an observation file appears similar;
* the word “drift” is present.

Confirm also that:

* Reference Drift is not observer disagreement;
* Constitutional Fragmentation is not fragmented understanding;
* Stochastic Drift is not generic probabilistic variation;
* Phase Desynchronization is not delayed awareness;
* Privilege Surface Expansion Failure is not generic connectivity;
* Null State Boundary Violation is not ordinary unavailability;
* Invariant Overconstraint is not merely strict intended governance;
* Implicit Reachability Expansion Failure is not every new reachable State.

---

# Template H — Option Comparison

## 22. Comparison Table

Use this table only after each option has been evaluated independently.

| Dimension                   | Option A    | Option B    | Current State / No Change |
| --------------------------- | ----------- | ----------- | ------------------------- |
| Source-State assumptions    | `[Finding]` | `[Finding]` | `[Finding]`               |
| Transition Path             | `[Finding]` | `[Finding]` | `[Finding]`               |
| Reachability change         | `[Finding]` | `[Finding]` | `[Finding]`               |
| Target-State Admissibility  | `[Finding]` | `[Finding]` | `[Finding]`               |
| Governing Constraint effect | `[Finding]` | `[Finding]` | `[Finding]`               |
| Effective Authority         | `[Finding]` | `[Finding]` | `[Finding]`               |
| Effective Capability        | `[Finding]` | `[Finding]` | `[Finding]`               |
| Privilege Surface           | `[Finding]` | `[Finding]` | `[Finding]`               |
| Invariant assessment        | `[Finding]` | `[Finding]` | `[Finding]`               |
| Failure Mode attribution    | `[Finding]` | `[Finding]` | `[Finding]`               |
| Evidence quality            | `[Finding]` | `[Finding]` | `[Finding]`               |
| Unresolved conditions       | `[Finding]` | `[Finding]` | `[Finding]`               |
| Scope limitations           | `[Finding]` | `[Finding]` | `[Finding]`               |

---

## 23. Comparison Discipline

Do not classify an option merely as:

* structurally safe;
* structurally unsafe;
* structurally stable;
* structurally unstable;
* approved;
* rejected.

Those labels collapse distinct questions.

Instead record separately:

* what becomes reachable;
* what remains admissible;
* which constraints remain effective;
* which Invariants are preserved or weakened;
* which Failure Modes are supported;
* what remains unresolved.

CNIG does not provide a universal scalar score for selecting between options.

An external decision authority may weigh CNIG findings alongside:

* operational requirements;
* security requirements;
* regulatory obligations;
* cost;
* reliability;
* schedule;
* organisational risk;
* implementation feasibility;
* reversibility.

Those decision criteria remain external to CNIG unless they are represented as relevant Governing Constraints in the bounded analysis.

---

# Template I — Analytical Conclusion

## 24. CNIG Analytical Summary

### Bounded question

`[Question evaluated]`

### Material composition

`[Components and relationships necessary to explain the result]`

### Reachability finding

`[What the composition makes reachable]`

### Admissibility finding

`[Whether the relevant Target State remains admissible and the evidential basis]`

### Governance finding

`[Whether applicable Governing Constraints remain effective across the complete composition]`

### Privilege Surface finding

`[Whether effective authority or capability changes]`

### Invariant finding

`[Preserved, weakened, conflicting, or unresolved properties]`

### Failure Mode finding

`[Established, provisional, conflicting, unresolved, or unsupported classification]`

### Competing explanations

* `[Explanation]`

### Material uncertainty

* `[Uncertainty]`

### Evidence required next

* `[Evidence]`

### Scope limitation

`[What the analysis does not establish]`

---

## 25. Permitted Analytical Conclusions

A CNIG analytical conclusion may state:

* the option introduces a supported Reachability change;
* no material Reachability change is currently supported;
* a Target State is supported as admissible within the bounded model;
* a Target State is supported as inadmissible;
* Admissibility remains PROVISIONAL, CONFLICTING, or UNRESOLVED;
* one or more Invariants appear weakened;
* no canonical Failure Mode is supported;
* a Failure Mode is PROVISIONAL;
* competing Failure Modes remain unresolved;
* the problem is not materially compositional;
* additional evidence is required.

The analysis should not silently convert any of these into:

* approval;
* rejection;
* authorization;
* implementation instruction;
* risk acceptance;
* production readiness.

---

# Template J — External Decision Record

## 26. External Decision Boundary

This optional section records a decision made outside CNIG.

### Decision authority

`[Named role, body, owner, or process]`

### Decision

`[External decision]`

### Date or effective phase

`[Date or phase]`

### CNIG analysis considered

`[Reference to analytical record]`

### Other considerations

* `[Security]`
* `[Operations]`
* `[Compliance]`
* `[Cost]`
* `[Schedule]`
* `[Other]`

### Risks accepted externally

* `[Risk]`

### Conditions imposed externally

* `[Condition]`

### Implementation owner

`[External owner]`

### Validation authority

`[External authority]`

### Reversibility or rollback requirement

`[External requirement]`

### Accountability

`[External accountable party]`

The presence of this section does not make the decision part of CNIG.

It preserves separation between:

* CNIG analysis;
* external authority;
* external action.

---

## 27. Provenance and Revision Record

### Analysis version

`[Version]`

### Evidence cutoff

`[Date, phase, or version]`

### Earlier analysis

`[Reference]`

### New evidence

* `[Evidence]`

### Changed conclusion

`[Conclusion changed]`

### Reason for revision

`[Reason]`

### Supersession status

* **supplements**
* **partially supersedes**
* **fully supersedes**
* **does not supersede**

Earlier conclusions must not be silently erased.

---

## 28. Non-Operational Boundary

These templates do not authorize:

* configuration changes;
* deployment changes;
* identity changes;
* permission changes;
* policy changes;
* remediation;
* production approval;
* autonomous action;
* enforcement;
* system control.

External applications may reference or reproduce the template structure.

Any implementation remains outside CNIG and does not alter the canonical framework.

An external implementation must not be represented as:

* CNIG itself;
* a canonical CNIG decision engine;
* proof that CNIG guarantees correctness;
* authority to approve or reject system changes;
* authority to redefine canonical concepts.

---

## 29. Stability Rule

The decision-template layer remains coherent when:

* analysis remains separate from decision authority;
* evidence remains separate from inference;
* Source States and Transition Paths are explicit;
* Reachability remains distinct from Admissibility;
* execution remains distinct from governance validity;
* Privilege Surface remains limited to topology affecting effective authority, capability, control, access, interaction, or resource effect;
* Invariant assessment remains evidence-dependent;
* Failure Mode attribution follows canonical conditions;
* uncertainty remains explicit;
* implementation and action remain external.

The layer degrades when:

* templates become approval gates;
* “safe” or “unsafe” replaces structural findings;
* local execution success is treated as proof of Admissibility;
* Failure Modes are assigned through leading questions;
* assumptions become facts;
* unresolved conditions are suppressed;
* CNIG is presented as the decision authority;
* external implementation is treated as canonical CNIG.

---

## 30. Transition to State Model

The next layer defines how CNIG represents:

* States;
* Source States;
* Intermediate States;
* Target States;
* Transition Paths;
* Reachability;
* Admissibility.

See:

`07_STATE_MODEL.md`
