# The Problem Class CNIG Addresses

Constraint-Native Infrastructure Governance (CNIG) by Gaurav H. Thanki

---

## 1. The Situation

A practitioner is working on a system where:

- the unexpected behavior is reproducible and observable
- no component is failing
- the design review looks correct
- and the system is producing outcomes the architecture
  was not intended to permit

This is not an observability problem.
The behavior is visible.

This is not a component problem.
Components are correct.

This is a structural problem.
The composition of correct components has produced states
that the design did not intend to be reachable.

This is the problem class CNIG addresses.

---

## 2. What the Practitioner Has Already Tried

By the time CNIG becomes relevant, the standard diagnostic
toolkit has been exhausted.

**Observability** — metrics, traces, and logs confirm the
behavior. The system is not hiding anything. The problem
is not that the behavior is invisible. The problem is that
nothing in the observable state explains why the architecture
permits it.

**Testing** — unit tests and integration tests pass. Components
behave correctly in isolation. Pairwise integration tests
return expected results. The behavior only appears at the
composed system level.

**Configuration review** — policies, access rules, and
configuration files are correct as written. No visible
misconfiguration. Reviewers cannot identify what structural
decision enabled the unexpected state.

**Incident correlation** — no deployment, no configuration
change, and no external event cleanly explains why this
outcome is possible. Or: the outcome has always been
possible and was only recently triggered.

**Architecture review** — the design looks sound. Component
responsibilities are clear. Interfaces between components
are correctly defined. No reviewer can point to a specific
decision that introduced the problem.

The components are correct.
The configuration is correct.
The design review passed.
The system is producing states that should not be reachable.

---

## 3. Why Standard Tools Stop Here

Each standard tool evaluates behavior at the component level
or detects deviation from expected state at runtime.

None of them are designed to reason about what states become
structurally possible when correct components are composed.

The question CNIG addresses is not:

> "Why did this component fail?"

It is:

> "Why did the architecture make this state reachable?"

That question cannot be answered by examining components.
It can only be answered by reasoning about composition
structure.

**Observability** tells you what the system is doing.
It does not tell you why the structure of the system makes
that behavior reachable in the first place.

**Formal verification** verifies components against their
specifications. It does not model the state space that
emerges when verified components are composed.

**Chaos engineering** introduces failure to find fragility.
The problem class CNIG addresses does not require failure —
it emerges from correct operation under composition.

**Policy-as-code** enforces declared constraints. It cannot
enforce constraints on states that were not anticipated when
the policy was written.

**Architecture patterns** describe how to structure components
at design time. They do not describe what becomes reachable
at composition time.

The tools are not wrong.

They are operating correctly within their scope.

The problem lives outside their scope.

---

## 4. The Precise Failure Condition

The failure condition CNIG addresses has three properties:

**Local correctness** — every component behaves correctly
by its own specification.

**Global incorrectness** — the composed system produces
states that are not intended, not anticipated, or not
admissible under the system's governing intent.

**Structural cause** — the cause is not a bug, a
misconfiguration, or a failure. It is the structure of
the composition itself. The architecture permitted a state
it was not designed to permit.

This failure condition appears predictably in:

- distributed systems where service interaction creates
  emergent state not present in any individual service
- identity and access systems where role composition
  expands effective privilege beyond declared permissions
- orchestration systems where execution ordering creates
  new reachable states not anticipated in workflow design
- multi-agent systems where agent interaction produces
  behavior outside any individual agent's specification
- infrastructure systems where configuration coupling
  produces instability under scale

In each domain the pattern is the same.

Local correctness does not guarantee global correctness.

The composition structure determines what is reachable.
What is reachable is not always what was intended.

---

## 5. What Changes Under CNIG

CNIG shifts the reasoning question from:

> "Is this component correct?"

to:

> "What system states become reachable when these
> components interact?"

This moves analysis from execution-level correctness to
structure-induced possibility space.

It introduces two distinctions that standard tools do
not make:

**Reachable vs Admissible** — not all states that can
be reached are states that should be reached. CNIG
reasons about the difference between what the composition
makes possible and what the governing intent permits.

**Execution correctness vs Governance structure** — local
correctness is an execution property. Global admissibility
is a structural property. They are not the same evaluation
and do not imply each other.

These distinctions are what make the problem class
tractable.

The question is not what the system did.
The question is what the structure allowed.

---

## 6. When CNIG Is the Appropriate Lens

CNIG applies when:

- all components are correct and the system is still
  producing unintended outcomes
- the failure cannot be attributed to any single component
- the unexpected behavior is reproducible but not
  structurally explained by the design
- access or privilege has expanded without explicit
  configuration change
- integration between correct systems produces states
  that were not designed to be reachable
- the question is why the architecture permitted
  something, not why a component failed

CNIG is not the appropriate lens for:

- component-level bugs with traceable causes
- configuration errors in individual services
- performance degradation with observable bottlenecks
- failures that resolve under standard diagnostic methods
- situations where the problem is interpretive coherence
  across observers rather than structural possibility
- degradation of unified system understanding under
  distributed observation pressure
- cases where multiple observers reconstruct different
  system realities from the same underlying state

---

## Canonical Reference

Constraint-Native Infrastructure Governance (CNIG)
by Gaurav H. Thanki
