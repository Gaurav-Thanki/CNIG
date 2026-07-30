# CNIG Glossary

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

This glossary defines the canonical vocabulary used in CNIG.

Terms are organized by category: framework terms, primitives,
invariants, failure modes, and architecture patterns.

All definitions are descriptive. They describe system structure
and compositional behavior, not implementation requirements.

---

## Framework Terms

**Constraint-Native Infrastructure Governance (CNIG)**
A conceptual framework for reasoning about admissible system
states within reachable state space under composition constraints
prior to execution. CNIG is concerned with how system structure
shapes the space of possible outcomes before execution occurs.
It is not a runtime system, policy engine, or formal verification
tool — it is a structural lens for interpreting composed system
behavior.

**Admissibility**
The property of a system state being structurally coherent under
the constraints governing system composition. Admissibility is
distinct from reachability: a state can be reachable without being
admissible. It is determined by structural compatibility, not by
runtime validation or component-level correctness.

**Composition**
The interaction of multiple system components to produce
system-level behavior. Under CNIG, composition is the primary
unit of analysis, because system behavior emerges from component
interaction rather than from individual component execution.
Properties that hold for individual components do not
automatically hold for their composition.

**Composition Constraint**
A structural condition that shapes how components can interact
and what states can result from that interaction. Composition
constraints operate at the level of system relationships and
interaction topology, not at the level of individual component
execution logic.

**Reachability**
The property of a system state being accessible through valid
composition of system components. Reachability defines the
boundary of structural possibility. It expands when new
components are introduced or when existing components are
composed in new configurations. Reachability does not determine
whether a state is structurally valid — only whether it can
be reached.

---

## Primitives

Primitives are the core vocabulary used to reason about system
structure and composition under CNIG. They are descriptive
reference concepts, not implementation targets or runtime objects.

**Reachable State Space**
The complete set of system states that can emerge through
composition of components. Reachable State Space represents
structural possibility, not observed execution history.
It expands when new composition relationships are introduced
and may include states that were not anticipated in component
design.

**Admissible System State**
A subset of the Reachable State Space that remains structurally
coherent under the constraints governing system composition.
Admissible states are configurations the system is intended
to be able to occupy. Not every reachable state is admissible,
and the gap between reachable and admissible is where
compositional failure originates.

**Constraint-Native Governance**
The implicit or explicit structural constraints that shape how
system composition behaves. These constraints operate at the
level of system relationships and interaction topology rather
than at the level of individual component execution. They
define what system configurations are structurally permissible
without necessarily being enforced at runtime.

**State Transition Validation**
A reasoning construct describing whether movement between system
states preserves structural coherence. It evaluates whether a
transition from one structural configuration to another remains
within the admissible state space. It is not an execution-time
validation mechanism — it is a conceptual tool for reasoning
about compositional change.

**Execution vs Governance Separation**
The analytical distinction between execution correctness —
whether a component behaves according to its specification —
and governance structure — whether the composed system behaves
within its intended structural boundaries. These are independent
properties. A system can satisfy execution correctness while
violating governance structure. Standard diagnostic methods
evaluate execution correctness. CNIG addresses the governance
layer.

**Privilege Surface**
The emergent interaction topology created by system composition.
It describes how the structure of component relationships creates
interaction pathways that may not be explicitly designed or
declared. Privilege Surface expands when new composition
relationships are introduced, potentially enabling interactions
between components that were not anticipated in the original
structural design.

---

## Invariants

Invariants are interpretive stability concepts. They describe
what should remain consistent when reasoning about systems under
composition. They are not enforcement rules or runtime checks —
they are lenses for identifying where structural coherence is
weakening.

**Identity Invariant**
The consistency of system identity across different
representations, contexts, and composition configurations.
When the Identity Invariant weakens, the same system entity
is interpreted differently depending on the structural context
in which it is observed. This becomes visible in identity and
access systems under role aggregation or nested policy
composition.

**Stability Invariant**
Bounded deviation in system behavior under structural variation.
When the Stability Invariant weakens, system behavior becomes
disproportionately sensitive to small changes in composition
structure — minor additions or reconfigurations produce
outsized behavioral effects.

**Behavioral Invariant**
Consistency between expected and observed behavior across
different composition contexts. When the Behavioral Invariant
weakens, a component's effective behavior changes depending
on what it is composed with, even though the component itself
has not changed.

**Structural Invariant**
Preservation of relational coherence across system composition.
When the Structural Invariant weakens, the relationships between
system components lose their intended meaning as composition
pressure increases — structure that was coherent in isolation
becomes ambiguous or inconsistent at system scale.

---

## Failure Modes

Failure modes describe how system composition produces unintended
or unstable global behavior. They are structural interpretations
of compositional breakdown — descriptions of how systems fail
at the level of composition, not at the level of individual
components. They are not operational alerts, incident categories,
or debugging labels.

**Governance Capture**
System behavior shifts away from intended structural constraints
due to emergent interaction dominance. The governing structure
remains visible but loses constraint authority over system
behavior. Governance Capture can occur gradually through
accumulation rather than through a single identifiable event —
vocabulary persists while governing force erodes.

**Reference Drift**
Divergence in meaning or interpretation of structural constraints
across system boundaries. The same rule, concept, or constraint
is understood differently in different parts of the system,
producing inconsistent global behavior even when each local
interpretation is internally consistent.

**Constitutional Fragmentation**
Breakdown of global structural coherence into incompatible local
interpretations. The system loses a unified admissibility logic.
Different regions operate under different effective constraints,
and no single consistent view of structural validity spans
the whole system.

**Invariant Overconstraint**
System composition restricts admissible behavior beyond intended
structural limits. Valid system states become unreachable because
compounded constraint interactions eliminate them from the
admissible space. The system becomes less capable than its
individual components would allow, and the restriction is not
visible at the component level.

**Recursive Governance Instability**
Governance evaluation becomes dependent on prior governance
evaluation, producing self-referential instability. Structural
validity becomes circular — the system cannot evaluate its own
admissibility without reference to a prior admissibility
determination that is itself unstable.

**Implicit Reachability Expansion Failure**
System composition introduces new reachable states that were
not represented in the original structural model. The possibility
space expands without explicit acknowledgment. New states become
accessible without any deliberate design decision having enabled
them.

**Stochastic Drift**
The system produces divergent outcomes under structurally
equivalent conditions due to compositional variability.
Determinism is lost at the system interaction level even when
individual components behave deterministically. Equivalent
inputs produce variable outputs because composition introduces
variability that component-level analysis does not capture.

**Phase Desynchronization**
Temporal misalignment between state transitions and their
structural interpretation. System state changes and the
governance evaluation of those changes become decoupled in time.
The system is evaluated against a structural understanding
that no longer matches its current configuration.

**Privilege Surface Expansion Failure**
Interaction topology expands beyond intended structural
boundaries under composition pressure. New interaction pathways
emerge between components without explicit design. Effective
access or capability expands without any change to declared
permissions, roles, or constraints — the expansion occurs at
the structural level, not the policy level.

**Null State Boundary Violation**
The system reaches a configuration from which no valid
continuation exists under defined structural constraints.
No admissible transition is available from the current state.
The system may continue to execute while producing outcomes
that are not structurally valid under any interpretation
of its governing constraints.

---

## Architecture Patterns

Architecture patterns describe recurring structural behaviors
observed in composed systems under CNIG reasoning. They are
observational and descriptive — not design prescriptions,
reference architectures, or implementation templates.

**Emergent Coupling Pattern**
When independently correct components interact, unexpected
dependencies emerge through composition rather than through
explicit design. The coupling is not declared. It appears as
a structural effect of interaction topology and becomes visible
only at the composed system level.

**Constraint Amplification Pattern**
Local constraints, when composed across system boundaries,
produce disproportionately large global restriction effects.
Constraint interaction is non-linear under composition —
the combined restrictive effect of multiple constraints can
significantly exceed what any individual constraint analysis
would predict.

**Hidden Reachability Expansion Pattern**
System composition introduces new reachable states not present
in isolated component design. The possibility space expands
as new interaction pathways emerge, without explicit structural
acknowledgment that these states are now accessible.

**Fragmented Governance Pattern**
Multiple local governance interpretations coexist without a
unified global admissibility structure. Governance becomes
context-dependent across system regions. No single consistent
constraint interpretation spans the whole system, and behavior
varies depending on which local interpretation is in effect.

**Interaction Topology Drift Pattern**
System behavior evolves due to changes in interaction pathways
rather than changes in components. The components of the system
remain unchanged while the relationships between them shift,
producing behavioral change without any component having been
modified.

**Stability Under Composition Illusion Pattern**
Systems appear stable at the component level but degrade under
integration due to structural mismatch between components.
Component-level stability is confirmed by testing. System-level
instability emerges only under composition, making the source
of degradation difficult to locate through standard methods.

---

## Canonical Reference

Constraint-Native Infrastructure Governance (CNIG)
by Gaurav H. Thanki
