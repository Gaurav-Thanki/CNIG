# CNIG System Limits

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer defines the conditions under which CNIG can and cannot support a structurally grounded analysis.

It distinguishes between:

* the scope of the CNIG framework
* the evidence required to apply it
* limits on diagnostic certainty
* limits of structural representation
* limits of Failure Mode attribution
* the boundary between conceptual analysis and implementation

These limits do not weaken CNIG’s canonical definitions.

They constrain what may be concluded from a particular body of evidence or system model.

---

## 2. Nature of CNIG Limits

CNIG limits are boundaries on:

* framework applicability
* evidential support
* structural-model completeness
* causal attribution
* state-space characterization
* admissibility determination
* diagnostic confidence
* external implementation claims

They are not:

* runtime constraints
* enforcement rules
* compliance requirements
* usage prohibitions
* operational controls
* product limitations
* evidence that the framework becomes invalid at scale

The framework and an application of the framework must remain distinct.

A weak or incomplete analysis does not alter the canonical ontology.

It limits the conclusions that the analysis can support.

---

## 3. Scope Limit

CNIG addresses:

> component-correct, composition-inadmissible systems.

It is most applicable where:

* multiple components or domains participate in the outcome
* local correctness does not sufficiently explain the global state
* relationships between components alter reachability
* the composition affects authority, capability, constraints, or transition paths
* an unintended or inadmissible state may become structurally reachable

CNIG does not provide a necessary explanation for every:

* component failure
* software defect
* direct misconfiguration
* explicit policy violation
* operational outage
* access-control mistake
* performance problem
* governance disagreement
* unexpected system result

Where a directly evidenced local cause sufficiently explains the material outcome, a CNIG classification should not displace that explanation without additional structural evidence.

---

## 4. Evidence Limit

CNIG does not generate evidence about a system.

It reasons from available evidence concerning:

* system states
* configurations
* relationships
* constraints
* authority
* topology
* transitions
* resources
* timing
* governing boundaries

Where evidence is incomplete, the analysis must not silently invent the missing system structure.

Insufficient evidence may prevent reliable determination of:

* the Source State
* the Transition Path
* the Target State
* local correctness
* Effective Authority
* Effective Capability
* applicable Governing Constraints
* Governing Intent
* Reachability
* Admissibility
* affected Invariants
* a Failure Mode

The correct result under insufficient evidence is:

* PROVISIONAL
* CONFLICTING
* or UNRESOLVED

Lack of evidence does not establish absence of a structural condition.

It also does not establish that the condition exists.

---

## 5. Structural-Model Limit

CNIG analysis depends on a sufficiently representative Structural Model.

The model may include:

* relevant components
* relationships
* system boundaries
* authority paths
* governing constraints
* shared resources
* Source States
* Intermediate States
* Target States
* Transition Paths
* temporal phases
* admissibility conditions

No practical Structural Model is assumed to contain every theoretically possible system detail.

The model must instead contain the details material to the conclusion being evaluated.

A Structural Model may be insufficient where it omits:

* a relevant dependency
* an alternative authority path
* inherited relationships
* delegation
* downstream service effects
* shared state
* a cross-domain mapping
* an Intermediate State
* a temporal phase difference
* a governing constraint
* a valid continuation path

A conclusion that depends on an omitted relationship must remain unresolved until that relationship is established or excluded.

---

## 6. Boundary-Identification Limit

CNIG analysis requires the relevant compositional boundary to be identifiable.

Relevant boundaries may include:

* component boundaries
* service boundaries
* identity boundaries
* authority boundaries
* policy boundaries
* trust boundaries
* resource boundaries
* governance boundaries
* control-plane and data-plane boundaries
* local-state and global-state boundaries
* temporal boundaries
* cross-domain boundaries

Where the relevant boundary cannot be identified, the analysis may be unable to determine:

* where authority changes
* where constraint scope changes
* where responsibility changes
* where one state becomes input to another system
* where a local transition contributes to a global state
* where governance ceases to constrain the complete composition

Ambiguous boundaries reduce diagnostic confidence.

They do not automatically constitute a CNIG Failure Mode.

---

## 7. Local-Correctness Limit

CNIG must not presume that components are locally correct merely because:

* no component error was reported
* health checks are green
* execution completed
* a permission check succeeded
* a pipeline stage passed
* a system continued operating
* no alert was generated

Local correctness must be:

* supported by evidence
* treated as an explicit assumption
* or left unresolved

CNIG can analyse a system containing component faults.

However, the analysis must distinguish:

* effects sufficiently explained by the component fault
* effects requiring compositional structure to explain
* cases where both local failure and compositional inadmissibility contribute

The presence of a local fault does not automatically invalidate CNIG analysis.

It may invalidate a claim that the system was component-correct.

---

## 8. Reachability Limit

CNIG does not claim that the complete Reachable State Space of a non-trivial system can always be enumerated.

Reachability analysis may be:

* complete for a narrowly bounded system
* partial for a larger composition
* evidence-derived from observed transitions
* model-derived from represented relationships
* unresolved where relevant paths remain unknown

Observed execution can establish that a state was reachable.

It does not establish that all other reachable states are known.

Failure to identify a path does not prove that the path is impossible unless the model and method support that conclusion.

Statements about Reachable State Space must therefore distinguish between:

* states known to be reachable
* states inferred to be reachable
* states represented as reachable
* states not yet evaluated
* states established as unreachable

---

## 9. Admissibility Limit

CNIG cannot determine admissibility without sufficiently supported Governing Constraints or Governing Intent.

An outcome being:

* unexpected
* undesirable
* undocumented
* unusual
* newly reachable
* difficult to explain

does not establish that it is inadmissible.

Admissibility requires a structural basis such as:

* an authority boundary
* a prohibited relationship
* an exclusion
* a separation requirement
* a Target State condition
* an Invariant-preservation requirement
* a valid-continuation requirement
* an authoritative governing constraint

Where Governing Intent is incomplete, conflicting, or unsupported, admissibility must remain PROVISIONAL, CONFLICTING, or UNRESOLVED.

Execution history alone does not define Governing Intent.

---

## 10. Causation Limit

CNIG identifies structural relationships that may explain how an outcome became reachable.

It does not convert correlation into causation.

The following do not independently establish a causal relationship:

* shared timing
* repeated occurrence
* component proximity
* common terminology
* participation in the same workflow
* appearance in the same observation group
* activation during the same incident
* similarity to a previous example

A Structural Cause requires evidence connecting:

* the Source State
* the relevant composition
* the Transition Path
* the resulting Target State

Where several causal explanations remain viable, the analysis must preserve them rather than selecting one through narrative preference.

---

## 11. Temporal Limit

A composed system may change faster than the available Structural Model or evidence can be updated.

Relevant changes may include:

* configuration changes
* identity changes
* authority changes
* resource membership changes
* topology changes
* policy propagation
* version changes
* transient delegation
* state replication
* control-plane updates

An analysis based on one system phase may not describe another phase.

The analysis must therefore identify, where material:

* when evidence was captured
* which system phase it represents
* whether relevant conditions changed
* whether the Source State and Governing Constraints were temporally aligned

A stale model limits confidence in current-state conclusions.

Delayed awareness alone is not Phase Desynchronization.

Phase Desynchronization requires an actual temporal mismatch in the system structure or governing conditions that affects reachability, authority, or admissibility.

---

## 12. Dynamic-System Limit

Highly dynamic systems may contain:

* short-lived states
* rapidly changing topology
* ephemeral identities
* temporary authority
* concurrent transitions
* race conditions
* retries
* probabilistic components
* non-deterministic scheduling

CNIG remains conceptually applicable where composition materially affects Reachability or Admissibility.

However, diagnostic conclusions may be limited where relevant states or relationships cannot be represented or evidenced sufficiently.

Dynamic behaviour does not make CNIG invalid.

It increases the burden of establishing:

* equivalent Source States
* complete Transition Paths
* temporal phase
* governing conditions
* material structural differences

Where those conditions cannot be established, conclusions must remain bounded.

---

## 13. Scale Limit

Scale alone does not invalidate CNIG.

Large systems may make it difficult to:

* enumerate relationships
* trace authority
* capture Intermediate States
* establish all governing constraints
* model feedback paths
* identify alternative transitions
* determine complete Reachability
* evaluate every Joint State

The limit concerns analytical completeness, not framework validity.

At large scale, analysis may need to be bounded by:

* a specific Target State
* a defined Transition Path
* an authority chain
* a resource domain
* a governance boundary
* a time window
* a specific compositional question

A bounded analysis must not be presented as a complete model of the entire system.

---

## 14. Stochastic-System Limit

CNIG does not assume that every system is deterministic.

A system may contain deliberately probabilistic or variable components.

Variability alone does not establish Stochastic Drift.

Stochastic Drift requires evidence that:

* materially equivalent Source States existed
* relevant transition conditions were materially equivalent
* system-level outcomes diverged
* the divergence emerged through composition
* intended probabilistic behaviour or hidden structural differences do not sufficiently explain it
* the divergence exceeded intended Stability or admissibility boundaries

Where equivalence cannot be established, Stochastic Drift attribution must remain unresolved.

---

## 15. Formalization Limit

CNIG is a conceptual framework.

It is not itself:

* a formal proof system
* a complete state-transition calculus
* a model checker
* a theorem prover
* an executable specification
* a deterministic validation engine

CNIG concepts may be represented externally through:

* diagrams
* models
* schemas
* formal methods
* analytical tools
* policy systems
* verification systems

Any such representation remains an external application.

Formalization does not inherently degrade CNIG.

However, no formalization should be treated as complete merely because it is executable or mathematically precise.

A formal model may omit:

* relevant relationships
* governing constraints
* Intermediate States
* authority paths
* temporal conditions
* external dependencies

The validity of a formal result remains bounded by the adequacy of the model and assumptions from which it was derived.

---

## 16. Prediction Limit

CNIG does not guarantee prediction of every future system outcome.

It may support reasoning about:

* structurally possible states
* known Transition Paths
* possible Reachability expansion
* constraint interactions
* authority composition
* conditions under which inadmissibility may arise

It does not provide deterministic prediction where:

* the Source State is incomplete
* relevant relationships are unknown
* transitions are stochastic
* external actors intervene
* system topology changes
* governing constraints change
* implementation behaviour differs from the model

A structurally possible state is not necessarily a probable state.

CNIG distinguishes possibility and admissibility.

It does not by itself quantify likelihood.

---

## 17. Failure-Mode Attribution Limit

A CNIG Failure Mode must not be assigned solely because:

* its name resembles the observed symptom
* an observation file appears similar
* a system is complex
* the outcome was undesirable
* a new state became reachable
* observers disagree
* evidence is fragmented
* governance is imperfect
* execution varied

Failure Mode attribution requires evidence of the canonical defining conditions.

Where evidence supports only part of a definition, attribution must remain PROVISIONAL.

Where several Failure Modes remain plausible, the analysis must preserve the alternatives and identify what evidence would distinguish them.

Where no Failure Mode is supported, no Failure Mode should be assigned.

---

## 18. Observer and Evidence Boundary

CNIG concerns actual system structure.

It does not classify, by themselves:

* observer disagreement
* fragmented understanding
* semantic incoherence
* conflicting narratives
* inability to reconstruct a system account
* LLM reasoning errors
* evidence dispersion
* incomplete documentation

These conditions may reduce evidence quality.

They do not become CNIG structural conditions unless evidence establishes an actual difference in:

* system state
* structural reference
* identity mapping
* authority
* constraint scope
* system phase
* Transition Path
* Reachability
* Admissibility

The condition in the system—not the observer’s difficulty understanding it—is the CNIG object.

---

## 19. Cross-Framework Limit

CNIG may coexist with other frameworks and engineering disciplines.

It must not silently absorb their:

* terminology
* analytical objects
* failure taxonomies
* mechanisms
* assumptions
* operational models

Cross-framework comparison must remain:

* explicit
* separately scoped
* non-substitutive
* terminology-preserving
* attribution-preserving

Conceptual adjacency does not establish equivalence.

A framework concerned with evidence reconstruction, semantic coherence, observers, pressure signals, or cognitive fracture addresses a different primary analytical object.

Those concepts must not be substituted for CNIG Primitives, Invariants, or Failure Modes.

---

## 20. Implementation Boundary

CNIG is not:

* a runtime enforcement mechanism
* a production decision authority
* a policy engine
* an automated remediation system
* a deployment architecture
* an autonomous controller
* a certification mechanism
* a compliance framework

External applications may reference or apply CNIG concepts.

Any implementation remains outside CNIG and does not alter the canonical framework.

No external system should be represented as:

* CNIG itself
* proof that CNIG guarantees correctness
* the canonical implementation of CNIG
* authority to redefine the framework
* evidence that CNIG executes or enforces governance

---

## 21. Misapplication Conditions

CNIG is being misapplied where analysis:

* labels every complex-system problem as a CNIG condition
* assumes local correctness without evidence
* treats every unexpected state as inadmissible
* assigns Failure Modes by keyword similarity
* equates successful execution with admissibility
* equates documented governance with effective governance
* treats Invariants as observer interpretations
* treats observations as canonical definitions
* treats external implementations as CNIG itself
* merges adjacent ontologies
* suppresses conflicting evidence
* converts assumptions into facts
* forces classification despite insufficient evidence

Misapplication weakens analytical precision.

It does not change the canonical framework.

---

## 22. Stability Statement

CNIG remains coherent when:

* its problem class remains bounded
* Reachability remains distinct from Admissibility
* local correctness remains distinct from global admissibility
* system structure remains distinct from observer understanding
* Primitives remain distinct from Invariants and Failure Modes
* Failure Mode attribution remains evidence-dependent
* uncertainty remains explicit
* implementation remains external
* cross-framework boundaries remain preserved

An application of CNIG becomes unreliable when:

* evidence is insufficient
* the Structural Model omits material relationships
* the Source State is unresolved
* Governing Intent is unsupported
* causal alternatives are suppressed
* temporal phase is ignored
* conclusions exceed the bounded scope of the analysis

The correct response to these limits is not framework expansion.

It is narrower scope, explicit uncertainty, additional evidence, or an UNRESOLVED conclusion.

---

## 23. Transition to Interpretation Guide

The next layer defines how CNIG concepts should be read, distinguished, and referenced consistently.

See:

`11_INTERPRETATION_GUIDE.md`
