# CNIG Diagnostic Interpretation Methodology

## Constraint-Native Infrastructure Governance (CNIG)

**Canonical attribution:** Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Document

CNIG is not itself a methodology.

This document defines an external diagnostic methodology for interpreting system evidence through the Constraint-Native Infrastructure Governance framework.

It provides a structured process for evaluating:

* system composition
* Source States
* Intermediate States
* Target States
* Transition Paths
* governing constraints
* Reachable State Space
* Admissible System States
* Effective Authority
* Effective Capability
* CNIG Primitives
* CNIG Invariants
* CNIG Failure Modes
* structural relationships across observations

The objective is to determine:

> What did the composition make reachable, and did the resulting state remain admissible?

This methodology does not replace or redefine the canonical framework layers.

Canonical definitions remain governed by:

* `02_CONCEPTUAL_CORE.md`
* `03_PRIMITIVES.md`
* `04_FAILURE_MODES.md`
* `GLOSSARY.md`
* `11_INTERPRETATION_GUIDE.md`

Where this document conflicts with a canonical definition, the canonical layer governs.

---

## 2. Diagnostic Principle

CNIG diagnostic analysis begins from the following principle:

> Within the problem class addressed by CNIG, structural inadmissibility may arise without an observable component failure.

CNIG does not assume that:

* every system failure is compositional
* every component is locally correct
* every unexpected result is a CNIG condition
* every new reachable state is inadmissible
* every observation supports a Failure Mode

Instead, the methodology evaluates whether:

* components are locally valid or correct
* local transitions are individually accepted
* no single component fault sufficiently explains the outcome
* composition creates the decisive structural effect
* an unintended or inadmissible system state becomes reachable

The foundational distinction is:

> Local correctness does not establish global admissibility.

---

## 3. Applicability Gate

Before applying the full methodology, determine whether CNIG is materially applicable.

CNIG is potentially applicable where an outcome depends on relationships between:

* components
* services
* identities
* roles
* permissions
* policies
* agents
* tools
* pipelines
* workflows
* infrastructure domains
* authority boundaries
* shared resources
* governing constraints

The minimum applicability question is:

> Does the outcome depend on composition in a way that cannot be explained adequately from one component boundary alone?

CNIG should not displace a simpler sufficient explanation.

The analysis should remain outside CNIG where the outcome is adequately explained by:

* a direct component fault
* an explicit misconfiguration
* a plainly incorrect permission
* an ordinary software defect
* an explicit policy violation
* a known operator action
* resource exhaustion
* conventional unavailability
* another directly evidenced local cause

A conventional failure may coexist with a CNIG condition.

Its presence does not automatically exclude compositional analysis.

The relevant issue is whether composition remains necessary to explain the material system-level outcome.

---

## 4. Canonical Ontology Reference Set

This section provides the canonical names and ordering used by the methodology.

The lists below are indexes.

Their complete definitions remain in the governing canonical files.

This methodology must not silently:

* rename
* reorder
* merge
* flatten
* substitute
* broaden
* narrow
* or redefine

any canonical term.

---

### 4.1 Primitives

CNIG uses six canonical Primitives in the following order:

1. **Reachable State Space**
2. **Admissible System State**
3. **Constraint-Native Governance**
4. **State Transition Validation**
5. **Execution vs Governance Separation**
6. **Privilege Surface**

Primitives are analytical reference concepts.

They are not:

* component types
* incident categories
* software objects
* implementation mechanisms
* controls
* remediation procedures

---

### 4.2 Invariants

CNIG uses four canonical Invariants in the following order:

1. **Identity Invariant**
2. **Stability Invariant**
3. **Behavioral Invariant**
4. **Structural Invariant**

Invariants describe system properties expected to remain preserved across composition and transition.

They are not:

* observer viewpoints
* interpretation states
* semantic-coherence measures
* runtime checks
* enforcement rules
* automatic pass-or-fail controls

---

### 4.3 Failure Modes

CNIG uses ten canonical Failure Modes in the following order:

1. **Governance Capture**
2. **Reference Drift**
3. **Constitutional Fragmentation**
4. **Invariant Overconstraint**
5. **Recursive Governance Instability**
6. **Implicit Reachability Expansion Failure**
7. **Stochastic Drift**
8. **Phase Desynchronization**
9. **Privilege Surface Expansion Failure**
10. **Null State Boundary Violation**

Failure Modes are evidence-supported structural conditions.

They are not:

* component errors
* symptoms
* alerts
* incidents
* severities
* monitoring labels
* product failures
* automatic diagnoses

---

### 4.4 Diagnostic States

Material diagnostic conclusions should use one of the following states:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

These states classify the support available for a conclusion.

They do not classify the system itself.

#### OBSERVED

Directly supported by available evidence.

#### INFERRED

Derived from supported structural relationships but not directly observed in full.

#### CANONICAL

Established by the governing CNIG framework files.

#### PROVISIONAL

Plausible, but one or more required structural conditions remain unsupported.

#### CONFLICTING

Material evidence or canonical sources support incompatible conclusions.

#### UNRESOLVED

Available evidence is insufficient for reliable determination.

Assumptions must be recorded separately.

An assumption is not evidence and does not become INFERRED merely because it is plausible.

---

## 5. Observation Analysis Model

Each `OBS_*` file represents an illustrative structural observation.

An observation is not automatically:

* an incident
* a root cause
* proof of local correctness
* proof of structural inadmissibility
* a fixed taxonomy node
* a one-to-one Primitive mapping
* an Invariant violation
* a Failure Mode
* an operational remediation case

An observation may provide evidence concerning:

* system entities
* Source States
* Intermediate States
* Target States
* component relationships
* governing constraints
* system boundaries
* authority paths
* Effective Capability
* Transition Paths
* reachable-state changes
* admissibility conditions
* Invariant preservation
* possible Failure Modes

Observations may be:

* partial
* situational
* repeatable
* non-repeatable
* context-dependent
* incomplete
* provisional
* contradicted by later evidence

Observation similarity does not establish identical structural cause.

---

# Diagnostic Evaluation Sequence

## Step 1 — Evidence Intake and Claim Separation

Record the available evidence without immediately assigning a CNIG classification.

Separate:

* directly observed conditions
* component-reported conditions
* authoritative records
* inferred relationships
* assumptions
* unresolved gaps
* conflicting evidence
* canonical CNIG definitions

Relevant evidence may include:

* configuration records
* identity and authority records
* dependency maps
* topology
* policy definitions
* execution history
* state-transition history
* resource changes
* logs
* approvals
* version records
* timing information
* system diagrams
* interface contracts

The analysis must not convert:

* fluency into evidence
* repetition into confirmation
* recency into authority
* confidence into proof
* resemblance to an observation file into classification

The initial output of this step should identify:

1. what is known;
2. what is inferred;
3. what is assumed;
4. what conflicts;
5. what remains unresolved.

---

## Step 2 — Problem-Class and Scope Evaluation

Determine whether the evidence supports the CNIG problem class.

Evaluate:

* whether relevant components were locally correct or valid
* whether local validation succeeded
* whether any direct component fault sufficiently explains the result
* whether composition is necessary to explain the outcome
* whether an unintended or inadmissible state may have become reachable

Local correctness must not be presumed merely because no failure was reported.

It must be supported or remain unresolved.

The analysis should state one of the following:

* CNIG is materially applicable
* CNIG may be applicable, provisionally
* CNIG is not required by the current evidence
* applicability remains unresolved

Do not force the analysis past this gate where composition is not materially implicated.

---

## Step 3 — System Boundary Identification

Identify the relevant system boundaries.

Boundaries may include:

* component boundaries
* identity boundaries
* authority boundaries
* administrative boundaries
* trust boundaries
* policy boundaries
* resource boundaries
* control-plane and data-plane boundaries
* governance and execution boundaries
* local-state and global-state boundaries
* cross-domain boundaries
* temporal or phase boundaries
* Transition Path boundaries

For each relevant boundary, determine whether any of the following changes:

* identity
* authority
* responsibility
* constraint scope
* policy scope
* resource ownership
* state ownership
* transition authority
* execution control
* admissibility conditions
* governing jurisdiction
* temporal phase

A boundary is not automatically a failure point.

It identifies where structural conditions must be traced across the composition.

---

## Step 4 — Source-State Establishment

Define the relevant Source State as precisely as the evidence permits.

The Source State may include:

* component versions
* configurations
* active identities
* role assignments
* permissions
* delegation
* relationships
* topology
* shared resources
* dependencies
* active constraints
* temporal phase
* governing boundaries

Where two outcomes are being compared, determine whether their Source States were materially equivalent.

Do not classify Stochastic Drift until plausible Source-State differences have been evaluated.

If the Source State cannot be established, mark it UNRESOLVED.

---

## Step 5 — Composition and Transition-Path Mapping

Map the complete composition relevant to the outcome.

Identify:

* participating components
* relationships
* invocation order
* authority flow
* delegation
* shared state
* resource effects
* intermediate transitions
* feedback paths
* cross-domain mappings
* downstream operations

Construct the Transition Path from:

1. Source State;
2. initiating action or condition;
3. each material Intermediate State;
4. authority or capability changes;
5. affected resources;
6. resulting Target State.

Do not stop at the component where the outcome became visible.

The material Structural Cause may exist earlier in the path or across several relationships.

Every local transition may be valid while the complete Transition Path is not admissible.

---

## Step 6 — Primitive Alignment

Identify the canonical Primitives materially implicated by the evidence.

Primitive alignment is many-to-many and evidence-dependent.

### Reachable State Space

Evaluate where composition:

* introduces states
* removes practical reachability
* creates alternate paths
* joins previously separate state spaces
* enables future transitions
* expands downstream effects

### Admissible System State

Evaluate whether the relevant Target State remains coherent under:

* Governing Constraints
* authority boundaries
* exclusions
* separation requirements
* Target State requirements
* Governing Intent

### Constraint-Native Governance

Evaluate:

* what constraints govern the composition
* where they originate
* where they apply
* whether they remain structurally effective
* whether the complete composition is represented by them

### State Transition Validation

Evaluate:

* local transition validity
* complete Transition-Path validity
* Intermediate States
* authority changes
* resource effects
* Target State admissibility

### Execution vs Governance Separation

Distinguish:

* successful execution
* local compliance
* authorization success
* component correctness

from:

* governance validity
* structural admissibility
* preservation of Governing Intent

### Privilege Surface

Evaluate whether topology changes effective:

* interaction
* access
* authority
* capability
* control
* resource effect

Generic connectivity does not establish Privilege Surface relevance.

The relationship must alter effective capability or authority.

Each Primitive mapping must identify the structural evidence supporting it.

---

## Step 7 — Reachability Evaluation

Determine what the composition made reachable.

Evaluate whether the composition:

* expanded the reachable state space
* contracted practical reachability
* created an alternate Transition Path
* joined separately governed state spaces
* exposed a new authority path
* broadened downstream capability
* enabled a previously unavailable Target State
* removed a required recovery state
* created a state absent from the Structural Model

A state may be:

* reachable and represented
* reachable but unrepresented
* represented but unreachable
* reachable through an alternate path
* reachable only under a specific phase
* unresolved

Reachability is not equivalent to failure.

A new reachable state may be:

* intended
* represented
* explicitly governed
* properly authorized
* admissible

The analysis must establish reachability before treating expansion as a Failure Mode.

---

## Step 8 — Admissibility Evaluation

Determine whether the relevant state or Transition Path remains admissible.

Identify the applicable:

* Governing Constraints
* Governing Intent
* authority boundaries
* exclusions
* separation requirements
* resource conditions
* transition requirements
* valid continuation requirements
* Invariants expected to remain preserved

A Target State may be:

* reachable and admissible
* reachable but inadmissible
* admissible in principle but unreachable
* represented but not evaluated
* absent from the represented Structural Model
* unresolved because constraints conflict or remain incomplete

Admissibility must not be inferred from:

* successful execution
* local validation
* absence of an alert
* component health
* policy presence
* authentication success
* authorization success
* continued operation

Where Governing Intent cannot be supported, the admissibility conclusion must remain PROVISIONAL or UNRESOLVED.

---

## Step 9 — Invariant Evaluation

Evaluate each relevant Invariant against the complete composition.

### Identity Invariant

Assess whether the composition preserves:

* principal identity
* resource identity
* Authority Lineage
* delegated responsibility
* attributable action

### Stability Invariant

Assess whether structural variation produces bounded system deviation.

Consider:

* topology changes
* dependency changes
* ordering
* concurrency
* timing
* authority changes
* resource-membership changes

### Behavioral Invariant

Assess whether the expected relationship between local behaviour and global composed behaviour remains preserved.

### Structural Invariant

Assess whether intended relationships remain coherent across:

* components
* constraints
* boundaries
* authority paths
* transitions
* Source States
* Intermediate States
* Target States

For each relevant Invariant, record whether it is:

* preserved
* conditionally preserved
* weakened
* not applicable
* PROVISIONAL
* CONFLICTING
* UNRESOLVED

Do not describe Invariants as observer interpretations.

The relevant object is the system property itself.

---

## Step 10 — Governance and Execution Comparison

Compare:

* declared governance
* supported Governing Intent
* represented structural constraints
* implemented constraints
* effective constraints
* observed execution
* resulting Target State

Evaluate whether:

* governance constrained the complete composition
* execution activated states governance did not represent
* authority existed to execute an action but not to authorize its complete effect
* local governance regimes were compatible
* declared restrictions remained structurally effective
* an unchanged governance declaration masked changed system capability
* governance evaluated only the initiating action rather than the resulting state

Observed execution must not be treated as approved governance merely because it occurred.

Declared governance must not be treated as effective merely because it remains documented or configured.

---

## Step 11 — Failure-Mode Attribution

A Failure Mode may be attributed only where the available evidence supports its canonical defining conditions.

Attribution must identify:

* the observed outcome
* the Source State
* the Target State
* the relevant Transition Path
* the Structural Cause
* the implicated Primitives
* the affected Invariants
* the Governing Constraints
* the Admissibility Condition
* the evidence supporting the classification
* competing explanations
* unresolved conditions
* the diagnostic state of the attribution

Failure Modes must not be assigned through:

* keyword matching
* superficial symptom similarity
* one-to-one observation lookup
* generic use of the word “drift”
* outcome undesirability alone
* component-error classification
* unsupported causal assumptions

---

### Governance Capture Attribution Gate

Establish whether:

* governing constraints remain declared
* their effective constraint authority has weakened
* interaction structures displace or bypass their combined effect
* the complete Reachable State Space is no longer constrained as intended

---

### Reference Drift Attribution Gate

Establish whether:

* a shared structural reference exists
* it resolves to non-equivalent effective referents
* the divergence exists in system mappings, scope, identity, state, boundary, or authority
* the condition is not merely observer disagreement

---

### Constitutional Fragmentation Attribution Gate

Establish whether:

* local governance regimes remain internally coherent
* those regimes apply to connected, shared, or Joint States
* their combined conditions are incompatible or incomplete
* no coherent global admissibility rule governs the composition

---

### Invariant Overconstraint Attribution Gate

Establish whether:

* constraints combine into a greater restriction
* intended valid states or transitions become unavailable
* the restriction exceeds Governing Intent
* the result is not merely strict but intended governance

---

### Recursive Governance Instability Attribution Gate

Establish whether:

* governance validity depends on another governance determination
* the dependency returns to the original determination
* no stable, non-circular base condition resolves admissibility

---

### Implicit Reachability Expansion Failure Attribution Gate

Establish whether:

* composition expands the Reachable State Space
* the new state or path is absent from the represented Structural Model
* the expansion was not deliberately acknowledged
* the resulting state or path conflicts with Governing Intent

A new reachable state alone is insufficient.

---

### Stochastic Drift Attribution Gate

Establish whether:

* Source States are materially equivalent
* transition inputs and relevant structural conditions are materially equivalent
* outcomes diverge materially
* variability arises through composition
* intended probabilistic behaviour or hidden state does not sufficiently explain the result
* the divergence violates intended Stability or admissibility boundaries

---

### Phase Desynchronization Attribution Gate

Establish whether:

* a transition and its governing structural conditions belong to different effective temporal phases
* the mismatch concerns actual state, authority, constraint, topology, or governance conditions
* the phase difference changes reachability, authority, or admissibility

Ordinary delay or delayed observer awareness is insufficient.

---

### Privilege Surface Expansion Failure Attribution Gate

Establish whether:

* composition creates or enlarges an effective capability path
* the path affects interaction, access, authority, capability, control, or resource effect
* no single direct assignment represents the complete path
* the path is absent from the intended authority structure
* the resulting capability is outside Governing Intent

Connectivity alone is insufficient.

---

### Null State Boundary Violation Attribution Gate

Establish whether:

* the system has reached the relevant state
* technically executable transitions may or may not remain
* no available continuation preserves admissibility
* necessary recovery or valid continuation states are structurally unavailable

Ordinary failure, stopped execution, or temporary unavailability is insufficient.

---

## Step 12 — Cross-Observation Structural Correlation

When several observations are available, determine whether they evidence shared:

* system entities
* Source States
* Target States
* constraints
* authority paths
* resources
* Transition Paths
* system boundaries
* topology
* Invariant effects
* reachable-state changes
* admissibility conditions
* Failure Mode conditions

Cross-observation analysis asks whether combined evidence exposes a structural relationship not visible from one observation alone.

Relevant questions include:

* Do several observations involve the same authority path?
* Do identity and access observations expose the same Privilege Surface?
* Do separate transitions contribute to one Target State?
* Does one observation establish a precondition required by another?
* Do several observations involve the same Governing Constraint?
* Does a topology change explain outcomes across several components?
* Do separate local states form one Joint State?
* Does one observation contradict the assumed Source State of another?
* Do combined observations support or weaken a Failure Mode attribution?

Shared timing, terminology, sequence, or component identity does not establish causation.

Structural relationships must be supported by evidence.

---

## Step 13 — Diagnostic Conclusion and State Assignment

Each material conclusion should include:

* claim
* diagnostic state
* supporting evidence
* structural relationship
* canonical term applied
* uncertainty
* competing explanations
* unresolved requirements

A final diagnostic result may conclude that:

* a CNIG condition is established
* a CNIG condition is PROVISIONAL
* the evidence supports several competing classifications
* the relevant condition is CONFLICTING
* the system problem is not materially compositional
* no Failure Mode is established
* the result remains UNRESOLVED

Failure to assign a Failure Mode is not analytical failure.

UNRESOLVED is preferable to unsupported classification.

---

## 6. Observation Registry Mapping Principle

Each `OBS_*` entry may be represented as a node in a structural evidence graph.

The graph represents system structure evidenced by observations.

It does not treat the observation documents themselves as system components.

Permitted relationship types may include:

* shared entity
* shared constraint
* shared Source State
* shared Target State
* shared Transition Path
* shared authority
* shared resource
* dependency
* governance relationship
* reachability relationship
* admissibility relationship
* Invariant relationship
* supporting evidence
* contradicting evidence
* supersession

The following rules apply:

* observation mappings are contextual
* Primitive mappings are many-to-many
* Invariant mappings are many-to-many
* Failure Mode attribution is evidence-dependent
* graph edges must identify the represented relationship
* graph proximity does not establish causation
* repeated vocabulary does not establish a shared structural condition
* revisions must preserve provenance
* later evidence may strengthen, weaken, contradict, or supersede an earlier assessment

Earlier assessments must not be silently overwritten.

A revision should identify:

* the earlier assessment
* new evidence
* reason for revision
* affected relationships
* current diagnostic state

---

## 7. Cross-Observation Structural Rule

Cross-observation analysis must evaluate system composition rather than count similar observations.

The objective is to determine whether separate observations expose:

* one shared structural condition
* different stages of one Transition Path
* separate causes of one Target State
* alternate paths to the same state
* a repeated topology condition
* conflicting Source States
* one common Governing Constraint
* one expanding Privilege Surface
* one shared admissibility failure

Cross-observation evidence may:

* support
* refine
* weaken
* contradict
* or leave unresolved

a structural assessment.

It must not automatically establish:

* causation
* local correctness
* inadmissibility
* an Invariant effect
* a Failure Mode

---

## 8. Diagnostic Grouping Lenses

The following groupings may help organize observations.

They are not additional CNIG Primitives, Invariants, Failure Modes, or architecture patterns.

They are non-canonical diagnostic groupings.

---

### 8.1 Local Validity with Global Inadmissibility

Relevant where:

* components remain locally valid
* local transitions succeed
* the composition reaches an unintended or inadmissible Target State

Potentially relevant Failure Modes may include:

* Governance Capture
* Constitutional Fragmentation
* Implicit Reachability Expansion Failure
* Privilege Surface Expansion Failure
* Stochastic Drift

The mapping depends on the defining structural evidence.

---

### 8.2 Boundary-Condition Divergence

Relevant where a material condition changes across a boundary, including:

* identity
* authority
* reference
* constraint scope
* governance jurisdiction
* temporal phase
* state ownership
* resource scope

Potentially relevant Failure Modes may include:

* Reference Drift
* Constitutional Fragmentation
* Phase Desynchronization
* Governance Capture
* Privilege Surface Expansion Failure

A boundary difference alone does not establish failure.

The difference must alter reachability, authority, admissibility, or constraint effect.

---

### 8.3 Reachability Expansion

Relevant where composition:

* creates a new Transition Path
* joins state spaces
* enables an additional Target State
* broadens Effective Capability
* exposes an authority path
* introduces unrepresented possibilities

Potentially relevant Failure Modes may include:

* Implicit Reachability Expansion Failure
* Privilege Surface Expansion Failure

The analysis must distinguish general state-space expansion from capability-path expansion.

---

### 8.4 Reachability Contraction

Relevant where composition:

* removes intended valid states
* eliminates valid transitions
* makes recovery states unavailable
* leaves no admissible continuation

Potentially relevant Failure Modes may include:

* Invariant Overconstraint
* Null State Boundary Violation

The analysis must distinguish excessive restriction from a state already having no admissible outgoing transition.

---

### 8.5 Compositional Variability

Relevant where apparently equivalent conditions produce divergent outcomes.

Potentially relevant Failure Modes may include:

* Stochastic Drift
* Phase Desynchronization
* Reference Drift

The Source States, phases, references, and hidden structural differences must be evaluated before assigning Stochastic Drift.

---

## 9. CNIG Interpretation Integrity

A valid CNIG diagnostic analysis must preserve:

* canonical names
* canonical ordering
* canonical definitions
* the distinction between Primitives, Invariants, and Failure Modes
* the distinction between Reachability and Admissibility
* the distinction between local correctness and global admissibility
* the distinction between execution and governance
* the distinction between local transition validity and complete Transition-Path admissibility
* evidence-supported many-to-many relationships
* provenance
* supersession
* uncertainty
* the non-operational boundary
* framework separation

An analysis is invalid if it:

* treats CNIG as incident management
* treats CNIG itself as a methodology
* reduces Failure Modes to component errors
* treats observations as fixed taxonomy classes
* assigns Failure Modes by keyword similarity
* equates component health with system admissibility
* equates Reachability with Admissibility
* treats execution as governance approval
* replaces structural evidence with narrative confidence
* silently changes canonical order
* merges Primitives, Invariants, and Failure Modes
* imports another framework’s analytical objects
* invents controls or operational mechanisms as canonical CNIG content
* presents PROVISIONAL attribution as established fact
* suppresses conflicting or unresolved evidence

The objective is not textual repetition.

The objective is preservation of canonical structure, scope, relationships, and analytical direction.

---

## 10. Framework Boundary

This methodology applies CNIG only to actual system:

* components
* relationships
* states
* constraints
* transitions
* authority
* capability
* topology
* Reachability
* Admissibility

It does not classify, by themselves:

* observer disagreement
* fragmented evidence
* incomplete understanding
* conflicting narratives
* semantic inconsistency
* model reasoning errors
* difficulty reconstructing a system account

Such conditions may affect evidence quality.

They do not establish a CNIG structural condition unless evidence supports an actual difference in:

* identity mapping
* authority
* structural reference
* system phase
* constraint scope
* Transition Path
* Source State
* Target State
* Reachability
* Admissibility

Cross-framework comparison, where necessary, must remain:

* explicit
* separately scoped
* non-substitutive
* terminology-preserving
* attribution-preserving

Framework adjacency does not authorize ontology merger.

---

## 11. Non-Operational Boundary

This document does not define or authorize:

* remediation procedures
* configuration changes
* implementation guidance
* runtime enforcement
* production validation
* autonomous action
* product architecture
* operational controls
* diagnostic commands
* vendor-specific troubleshooting
* automated decision authority
* guaranteed causal attribution

The methodology produces structured analysis.

It does not execute, enforce, approve, or remediate system changes.

External engineering or governance processes may reference the resulting analysis.

Any decision, control, implementation, or action remains outside CNIG and requires its own:

* authority
* evidence
* validation
* risk assessment
* rollback planning
* accountability

---

## 12. Stability Principle

The methodology remains coherent when:

* evidence is separated from inference
* applicability is tested before classification
* Source States are established
* complete Transition Paths are examined
* Reachability is established before Failure Mode attribution
* Admissibility is evaluated independently of execution success
* Primitives remain canonical analytical axes
* Invariants remain structural properties
* Failure Modes remain evidence-supported conditions
* observation mappings remain contextual
* uncertainty remains explicit
* revisions preserve provenance
* CNIG remains separate from adjacent frameworks

The methodology degrades when:

* observations are treated as isolated incidents
* local correctness is presumed without evidence
* component health is equated with global admissibility
* Source-State differences are ignored
* mappings become rigid or one-to-one
* correlation is converted into causation
* later assessments erase earlier provenance
* operational assumptions are imported into CNIG
* canonical terms are silently substituted
* adjacent framework concepts are imported
* classification is forced despite insufficient evidence

---

## 13. Closing Principle

CNIG diagnostic analysis does not stop at describing what happened.

It examines:

> how the composition made the observed state reachable, which constraints governed it, and whether the resulting state remained admissible.

Where the evidence does not support that determination, the correct conclusion is:

> UNRESOLVED.
