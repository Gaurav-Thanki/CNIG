# CNIG Analytical Checklists

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. Purpose of This Layer

This layer provides structured analytical prompts for applying CNIG concepts to a bounded system question.

The checklists support:

* prospective architectural analysis;
* retrospective analysis of execution evidence;
* structural decomposition;
* Reachability evaluation;
* Admissibility evaluation;
* Invariant assessment;
* evidence-grounded Failure Mode attribution.

These checklists are an external analytical scaffold.

They do not define or modify the canonical CNIG ontology.

Canonical definitions remain governed by:

* `02_CONCEPTUAL_CORE.md`
* `03_PRIMITIVES.md`
* `04_FAILURE_MODES.md`
* `GLOSSARY.md`
* `11_INTERPRETATION_GUIDE.md`

---

## 2. Nature of the Checklists

CNIG checklists are:

* structured reasoning prompts;
* evidence-discipline aids;
* scope-control aids;
* compositional-analysis guides;
* uncertainty-preservation aids.

They are not:

* requirements;
* compliance controls;
* certification criteria;
* CI/CD gates;
* approval mechanisms;
* runtime validation rules;
* automated decision systems;
* remediation procedures;
* proof of Admissibility;
* proof of a Failure Mode.

A checked item means only that the question was considered.

It does not establish that the relevant structural condition is present, absent, valid, or admissible.

---

## 3. Usage Rule

The checklists should be used in the following general order:

```text
Applicability
    ↓
Evidence and Scope
    ↓
Source State
    ↓
Composition
    ↓
Transition Path
    ↓
Reachability
    ↓
Governing Constraints
    ↓
Admissibility
    ↓
Invariant Evaluation
    ↓
Failure Mode Attribution, where supported
    ↓
Diagnostic State and Uncertainty
```

The sequence may be revisited when new evidence changes an earlier conclusion.

Do not begin by selecting a Failure Mode and searching for matching symptoms.

---

# Part I — Applicability and Evidence

## 4. CNIG Applicability Gate

Before proceeding, ask:

* Does the outcome depend materially on relationships between several components, services, domains, identities, tools, or agents?
* Is composition necessary to explain the system-level result?
* Is local correctness supported, materially relevant, or still unresolved?
* Does a direct component fault sufficiently explain the outcome?
* Does an explicit misconfiguration sufficiently explain the outcome?
* Does a conventional software defect sufficiently explain the outcome?
* Does an explicit policy violation sufficiently explain the outcome?
* Did composition alter Reachability, authority, capability, constraint effect, or available continuation States?
* Is there a meaningful question about Target-State Admissibility?

Record the applicability result as one of:

* **CNIG materially applicable**
* **CNIG provisionally applicable**
* **CNIG not required by current evidence**
* **Applicability UNRESOLVED**

CNIG should not displace a simpler sufficient explanation.

---

## 5. Evidence Intake Checklist

Identify the evidence available.

* Configuration records
* Identity and role records
* Permission records
* Policy definitions
* Authority and delegation records
* System diagrams
* Dependency maps
* Interface contracts
* Execution logs
* State-transition history
* Resource-change history
* Version records
* Timing and propagation records
* Approval records
* Observed system outcomes
* Governing documentation

For every material claim, ask:

* Is this directly observed?
* Is this inferred from supported relationships?
* Is this an assumption?
* Is this defined canonically by CNIG?
* Is there conflicting evidence?
* Is the evidence current for the relevant system phase?
* Is the evidence authoritative for the claim being made?
* Is any required evidence missing?

Use the diagnostic states:

* **OBSERVED**
* **INFERRED**
* **CANONICAL**
* **PROVISIONAL**
* **CONFLICTING**
* **UNRESOLVED**

Do not convert:

* plausibility into evidence;
* repetition into confirmation;
* fluency into proof;
* recency into authority;
* absence of an error into local correctness.

---

## 6. Bounded-System Checklist

Define the analytical boundary.

* What system or subsystem is under analysis?
* Which components are included?
* Which components are excluded?
* Which identities and authority domains are included?
* Which resources are included?
* Which governance domains are included?
* Which time window is relevant?
* Which Source State is the analysis anchored to?
* Which Target State or system effect is being evaluated?
* Which external dependencies may affect the result?
* Which assumptions limit the model?
* Which relationships remain unknown?

Confirm that the analysis does not imply complete coverage of a wider system than the evidence supports.

---

# Part II — State and Composition

## 7. Source-State Checklist

Identify the relevant Source State.

* What component versions were active?
* What configurations were active?
* Which identities were present?
* Which roles and permissions were active?
* Which delegation paths existed?
* Which resources and resource memberships existed?
* What topology existed?
* Which dependencies were active?
* Which Governing Constraints applied?
* Which temporal phase did the evidence represent?
* Which prior transitions had already occurred?
* Were any temporary or inherited conditions active?

Where outcomes are being compared:

* Were the Source States materially equivalent?
* Were versions equivalent?
* Were authority relationships equivalent?
* Were timing and phase equivalent?
* Were hidden or transient conditions excluded?
* Were all relevant structural differences evaluated?

If Source-State equivalence cannot be supported, do not classify Stochastic Drift as established.

---

## 8. Composition Checklist

Map the relevant composition.

* Which components participated?
* Which services participated?
* Which identities, roles, tools, or agents participated?
* Which resources were affected?
* Which relationships connected them?
* Which component invoked which other component?
* Where did authority originate?
* Where was authority delegated or inherited?
* Where did shared state exist?
* Where did one component’s output become another component’s input?
* Which downstream services acted with their own authority?
* Which cross-domain mappings existed?
* Which feedback or recursive relationships existed?
* Which relationships were absent from the represented Structural Model?

Ask:

> What material property existed only because these elements were composed?

Possible answers may concern:

* a reachable State;
* an authority path;
* an Effective Capability;
* a Transition Path;
* a Joint State;
* a constraint interaction;
* an unavailable continuation.

---

## 9. System-Boundary Checklist

Identify every boundary at which a material structural property may change.

* Component boundary
* Service boundary
* Identity boundary
* Authority boundary
* Administrative boundary
* Policy boundary
* Trust boundary
* Resource boundary
* Governance boundary
* Control-plane/data-plane boundary
* Local-State/global-State boundary
* Cross-domain boundary
* Temporal or phase boundary
* Transition-ownership boundary

At each boundary, ask whether any of the following changes:

* identity;
* authority;
* responsibility;
* resource ownership;
* constraint scope;
* policy scope;
* transition authority;
* State ownership;
* governing jurisdiction;
* temporal phase;
* Admissibility conditions.

A boundary is not automatically a failure point.

It identifies where structural continuity must be evaluated.

---

## 10. Transition-Path Checklist

Map the complete Transition Path.

* What was the Source State?
* What initiated the path?
* What was the first transition?
* Which Intermediate States occurred?
* Which component owned each local transition?
* Which authority was used at each stage?
* Did authority change during the path?
* Did Effective Capability change during the path?
* Which resources changed?
* Which constraints applied at each stage?
* Did any component validate the complete path?
* What was the Target State?
* Was the Target State represented before execution?
* Was the Target State evaluated for Admissibility?
* Were valid rollback or continuation paths available?

Distinguish:

* local transition validity;
* complete Transition-Path validity;
* Target-State Admissibility.

Every local transition succeeding does not establish the validity of the complete path.

---

# Part III — Canonical Primitive Evaluation

## 11. Reachable State Space Checklist

Ask:

* What States were reachable from the Source State?
* Which States were known to be reachable?
* Which States were inferred to be reachable?
* Which States were represented as reachable?
* Which States were reached through execution evidence?
* Which alternate Transition Paths existed?
* Did composition join previously separate State spaces?
* Did an Intermediate State enable another path?
* Did delegation create a new path?
* Did inheritance create a new path?
* Did changed topology create a new path?
* Did downstream capability create a new Target State?
* Did composition remove access to a previously reachable State?
* Which reachable States were absent from the Structural Model?

Do not assume:

* a newly reachable State is a failure;
* an undocumented State is inadmissible;
* failure to identify a path proves that no path exists.

---

## 12. Admissible System State Checklist

For each material reachable State, ask:

* Which Governing Constraints apply?
* What Governing Intent is supported?
* Which authority boundaries apply?
* Which resource boundaries apply?
* Which exclusions apply?
* Which separation requirements apply?
* Which Target-State requirements apply?
* Which valid-continuation requirements apply?
* Which Invariants are required to remain preserved?
* Does the State remain within those conditions?
* Is the governing evidence complete?
* Is the governing evidence authoritative?
* Are governing conditions conflicting?

Classify the State as:

* reachable and admissible;
* reachable but inadmissible;
* reachable with Admissibility PROVISIONAL;
* reachable with Admissibility CONFLICTING;
* reachable with Admissibility UNRESOLVED.

Do not infer Admissibility from execution success.

---

## 13. Constraint-Native Governance Checklist

Identify the governing structure.

* What constraints are declared?
* What constraints are represented in the Structural Model?
* What constraints are implemented?
* What constraints are enforced?
* What constraints are effective across the complete composition?
* Where do constraints originate?
* Which boundaries do they cover?
* Which Transition Paths do they cover?
* Which States do they govern?
* Which Joint States fall between governance domains?
* Does a constraint remain effective after delegation?
* Does a constraint remain effective after downstream execution?
* Does a constraint remain effective after topology change?
* Does declared governance still shape the complete Reachable State Space?

Do not equate the continued presence of governance language or configuration with effective governing authority.

---

## 14. State Transition Validation Checklist

For the complete path, evaluate:

* Was the Source State established?
* Were material Intermediate States identified?
* Was transition authority supported?
* Were authority changes represented?
* Were resource effects represented?
* Were applicable constraints identified?
* Were relevant boundaries evaluated?
* Were Invariants assessed?
* Was resulting Reachability evaluated?
* Was the Target State evaluated?
* Was valid continuation evaluated?
* Was the complete path evaluated rather than only local stages?

This checklist performs conceptual analysis.

It is not an execution-time validator.

---

## 15. Execution vs Governance Separation Checklist

Ask separately:

### Execution

* Did each component behave according to its local specification?
* Did each local transition satisfy its local conditions?
* Did authentication succeed?
* Did authorization succeed?
* Did the workflow complete?
* Did the system report success?

### Governance

* Was the complete Transition Path within Governing Intent?
* Was the resulting Target State admissible?
* Did governance cover downstream effects?
* Did governance cover the Joint State?
* Did effective authority remain within intended boundaries?
* Did the composition preserve required Invariants?
* Did the complete Reachable State Space remain constrained as intended?

Never use a positive answer from the execution group as automatic proof of a positive answer from the governance group.

---

## 16. Privilege Surface Checklist

Identify the effective topology affecting:

* interaction;
* access;
* authority;
* capability;
* control;
* resource effect;
* action paths.

Ask:

* Which principals participated?
* Which roles or groups contributed authority?
* Which inherited relationships applied?
* Which delegation paths existed?
* Which services acted with service-held authority?
* Which tools extended the initiator’s capability?
* Which agents could invoke other agents or tools?
* Which downstream systems were reachable?
* Which resources could be affected?
* Did an unchanged permission acquire broader downstream effects?
* Did several limited permissions combine into broader Effective Authority?
* Was the complete capability path represented?
* Was the complete capability path within Governing Intent?

Generic connectivity is not sufficient.

A relationship is material to Privilege Surface only where it changes effective interaction, authority, capability, control, access, or resource effect.

---

# Part IV — Invariant Evaluation

## 17. Identity Invariant Checklist

Evaluate preservation of:

* principal identity;
* resource identity;
* Authority Lineage;
* responsibility;
* delegated authority;
* attributable action.

Ask:

* Does the same identity map to the same effective principal?
* Does the same resource reference identify the same effective resource?
* Is authority traceable from initiator to final effect?
* Is delegated responsibility represented?
* Can resulting actions be attributed?
* Did identity mapping change authority?
* Did structural position give equivalent identities different Effective Authority?

This concerns actual identity and authority relationships.

It is not a test of whether observers describe identity consistently.

---

## 18. Stability Invariant Checklist

Evaluate bounded deviation under structural variation.

* Did a small topology change produce a disproportionate outcome?
* Did a minor dependency change alter broad system behaviour?
* Did a small authority change create large capability expansion?
* Did materially equivalent Source States produce bounded outcomes?
* Did timing create material divergence?
* Did concurrency create material divergence?
* Did ordering create material divergence?
* Did retries or queues create material divergence?
* Did the result remain within intended structural and behavioural bounds?

Stability does not require identical outcomes.

It requires deviation to remain bounded under the relevant governing conditions.

---

## 19. Behavioral Invariant Checklist

Evaluate the relationship between local and global behaviour.

* Did locally correct components produce the expected global result?
* Did an unchanged local operation retain the same system-level effect?
* Did topology change behaviour without component changes?
* Did downstream composition broaden the result?
* Did individually valid transitions accumulate into an unintended Target State?
* Did equivalent transition conditions produce materially different outcomes?
* Did the composed behaviour remain within its represented boundary?

This concerns actual system behaviour.

It is not a measure of agreement between descriptions.

---

## 20. Structural Invariant Checklist

Evaluate preservation of intended relationships between:

* components;
* constraints;
* boundaries;
* identities;
* authority paths;
* resources;
* transitions;
* Source States;
* Intermediate States;
* Target States;
* reachable and admissible States.

Ask:

* Does the effective composition match the Structural Model?
* Did new relationships create unrepresented Transition Paths?
* Did boundaries preserve their intended effect?
* Did separate governance domains form a coherent rule for Joint States?
* Did authority paths remain within the represented structure?
* Did a shared reference continue to resolve to the same structural object?
* Did the complete composition preserve intended constraint relationships?

---

## 21. Invariant Assessment Rule

For each relevant Invariant, assign one assessment:

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

# Part V — Failure Mode Attribution

## 22. Attribution Readiness Checklist

Before assigning any Failure Mode, confirm that the analysis identifies:

* the observed outcome;
* the Source State;
* the Target State;
* the complete Transition Path;
* the Structural Cause;
* the implicated Primitives;
* the affected Invariants;
* the Governing Constraints;
* the Admissibility Condition;
* supporting evidence;
* competing explanations;
* unresolved evidence;
* the diagnostic state of the attribution.

If one or more defining conditions remain unsupported, the attribution must remain PROVISIONAL or UNRESOLVED.

---

## 23. Classification Discipline Checklist

Confirm that the proposed Failure Mode is not being assigned merely because:

* its name resembles the symptom;
* the word “drift” appears;
* an observation file looks similar;
* the system is complex;
* the outcome was undesirable;
* governance was imperfect;
* a new State became reachable;
* connectivity increased;
* observers disagreed;
* evidence was fragmented;
* a component failed;
* execution varied.

Use the complete canonical definition in:

`04_FAILURE_MODES.md`

Do not create a one-to-one mapping between:

* one observation and one Failure Mode;
* one Primitive and one Failure Mode;
* one Invariant and one Failure Mode.

---

## 24. Competing-Classification Checklist

Where several Failure Modes appear plausible:

* What condition supports each candidate?
* What condition contradicts each candidate?
* Which defining conditions remain missing?
* Could one Failure Mode contribute to another?
* Are two Failure Modes being collapsed?
* Is a Primitive being confused with a similarly named Failure Mode?
* Would Source-State differences eliminate Stochastic Drift?
* Would temporal mismatch favour Phase Desynchronization?
* Would structural-reference divergence favour Reference Drift?
* Would incompatible governance regimes favour Constitutional Fragmentation?
* Would general Reachability expansion differ from Privilege Surface expansion?
* Would excessive restriction differ from a State with no admissible continuation?

Preserve multiple candidates where the evidence does not distinguish them.

---

# Part VI — Cross-Observation Analysis

## 25. Cross-Observation Checklist

When several observations are available, ask whether they share:

* a system entity;
* a Source State;
* a Target State;
* a Transition Path;
* an authority path;
* a resource;
* a Governing Constraint;
* a governance boundary;
* a Privilege Surface;
* a topology condition;
* an Invariant effect;
* a Reachability change;
* an Admissibility Condition.

Also ask:

* Does one observation establish a precondition for another?
* Does one observation contradict another’s Source State?
* Do several observations form stages of one Transition Path?
* Do several local States form one Joint State?
* Does combined evidence expose a structural condition absent from each isolated observation?
* Does later evidence weaken or supersede an earlier assessment?

Shared timing or terminology does not establish causation.

Graph edges must identify the supported structural relationship.

---

## 26. Provenance and Revision Checklist

For each material conclusion, record:

* evidence source;
* evidence date or system phase;
* claim status;
* assumptions;
* inference path;
* canonical concepts applied;
* conflicting evidence;
* unresolved evidence;
* earlier assessment, where applicable;
* reason for revision;
* supersession relationship.

Do not silently overwrite an earlier assessment.

---

# Part VII — Completion and Reporting

## 27. Completion Checklist

Before concluding the analysis, confirm:

* The system boundary is explicit.
* The Source State is supported or marked unresolved.
* Local correctness is supported, assumed, or marked unresolved.
* The composition is represented.
* The complete Transition Path is represented.
* Intermediate States are not omitted without justification.
* The Target State is identified.
* Reachability is distinguished from Admissibility.
* Governing Intent has a supported basis.
* Execution is separated from governance validity.
* Privilege Surface is not reduced to generic connectivity.
* Relevant Invariants are assessed.
* Failure Mode attribution follows canonical conditions.
* Competing explanations are retained.
* Uncertainty is explicit.
* External action is not implied or authorized.

---

## 28. Minimum Analytical Output

A completed CNIG analysis should state:

1. **Bounded system**
2. **Material evidence**
3. **Source State**
4. **Composition**
5. **Transition Path**
6. **Target State**
7. **Reachability finding**
8. **Applicable Governing Constraints**
9. **Admissibility finding**
10. **Invariant assessment**
11. **Failure Mode attribution, where supported**
12. **Competing explanations**
13. **Diagnostic states**
14. **Unresolved evidence**
15. **Scope limitations**

No Failure Mode is required where the evidence does not support one.

---

## 29. Non-Operational Boundary

These checklists do not authorize:

* configuration changes;
* deployment changes;
* remediation;
* access changes;
* policy changes;
* production approval;
* autonomous action;
* enforcement;
* system control.

An external engineering or governance process may use the resulting analysis as one input.

Any decision or action remains outside CNIG and requires its own:

* authority;
* evidence;
* validation;
* risk assessment;
* reversibility;
* accountability.

---

## 30. Stability Rule

The checklist layer remains coherent when:

* it begins with evidence and applicability;
* it preserves canonical definitions;
* it distinguishes local correctness from global Admissibility;
* it distinguishes Reachability from Admissibility;
* it examines complete Transition Paths;
* it preserves uncertainty;
* it treats Failure Mode attribution as evidence-dependent;
* it remains non-operational;
* it keeps system structure distinct from observer understanding.

The checklist layer degrades when:

* questions become mandatory controls;
* a checked item is treated as proof;
* Failure Modes are assigned through symptom matching;
* execution success is treated as governance validity;
* generic connectivity is treated as Privilege Surface;
* assumptions are treated as evidence;
* observer-centred coherence replaces actual system structure;
* the checklist is represented as CNIG itself.

---

## 31. Transition to Decision Templates

The next layer provides structured templates for recording CNIG analytical conclusions and decision context.

See:

`06_DECISION_TEMPLATES.md`
