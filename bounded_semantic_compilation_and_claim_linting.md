# Bounded Semantic Compilation and Claim Linting

## A Standalone Framework for Natural-Language Claim Inspection, Typed Grounding, Transferability Diagnostics, and Bounded Reasoning Under Agent Limits

---

# Status

This document is standalone.

It extends the following related framework ideas:

```text
structural map compiler / linter
layered reality workbench
cross-layer invariant distinction mapping
recoverable objecthood
staticity failure under operational proof
hidden support declarations
source-stack abstraction layers
self-linting frameworks
claim verification
executability
transferability
bounded agent reasoning
```

Its purpose is to make explicit a further development vision:

```text
A bounded semantic compiler for natural-language claims.
```

The goal is not to derive all possible English, Python, C++, mathematical, scientific, philosophical, or institutional claims from first principles.

The goal is to preserve and generalize the structural checking capabilities that mature formal systems already provide:

```text
symbol validity
syntax validity
type validity
dependency validity
reference navigation
support closure
executability checks
operational consequence checks
transferability diagnostics
complexity-budget warnings
```

In compressed form:

> The framework does not try to generate all valid claims. It tries to make claims inspectable before they are trusted, transferred, executed, or used for action.

---

# Abstract

Programming environments give users a powerful experience.

A user writes:

```text
import some_package
```

or:

```text
#include "some_file.h"
```

The editor can often check whether the imported module exists.

The user can usually ctrl-click into the referenced file, package, class, method, symbol, or declaration.

The linter can warn:

```text
file does not exist
symbol is unresolved
type does not match
function is called with wrong arguments
module is imported but unused
object may be null
path is unreachable
program will not compile
```

This gives the user a form of advance reality contact inside a symbolic environment.

The editor does not execute the whole world.

It does not derive all possible programs.

It does not simulate every runtime path.

But it can still provide useful static inspection.

Natural language usually lacks this tooling.

A sentence may be grammatically valid while its references are unclear, its semantic commitments are underdeclared, its operational meaning is missing, its transfer across domains is unsafe, or its support graph exceeds what one bounded agent can inspect.

For example:

```text
Institutions depend on trust.
```

This sentence is syntactically valid.

But a claim workbench should be able to ask:

```text
What kind of institution?
What kind of trust?
Trust as belief, expectation, legitimacy, compliance, credit, coordination, or recognition?
What fails if trust is removed?
Across what horizon?
For which use-context?
Does the same structure transfer from families to corporations to markets to states?
Is the claim empirical, conceptual, operational, architectural, or analogical?
```

The proposed framework therefore treats natural-language claims as inspectable source objects.

A claim may receive diagnostics such as:

```text
syntactically valid
semantically underdeclared
operationally ungrounded
empirically unsupported
reference-unresolved
projection-mismatched
scope-overextended
transfer-risky
complexity-budget-exceeded
```

This is not a ban on ordinary speech.

Natural language must remain permissive.

The inspection is available on demand.

The framework asks not:

```text
Is this sentence allowed?
```

but:

```text
What must be declared, grounded, bounded, or weakened before this claim can be safely used for a selected purpose?
```

In compressed form:

> A bounded semantic compiler turns ordinary claims into inspectable structures with references, types, supports, horizons, validity boundaries, and failure modes.

---

# 0. Orientation

Let:

```text
Σ
```

represent a bounded alphabet, symbol inventory, token set, or vocabulary surface.

Let:

```text
G
```

represent a bounded grammar or syntax system.

Let:

```text
C
```

represent a claim, sentence, assertion, model fragment, diagram element, rule, theorem, policy, or instruction.

Let:

```text
Parse(C)
```

represent the syntactic structure of claim `C`.

Let:

```text
Sem(C)
```

represent the declared semantic interpretation of `C`.

Let:

```text
Ref(C)
```

represent the references, imported concepts, named entities, source modules, files, packages, definitions, objects, measurements, or phenomena that `C` depends on.

Let:

```text
Type(C)
```

represent the structural type of the claim.

Examples:

```text
constraint claim
support claim
identity claim
causal claim
boundary claim
flow claim
analogy claim
transfer claim
operational claim
empirical claim
normative claim
architectural claim
```

Let:

```text
Supp(C)
```

represent the support graph required by claim `C`.

Let:

```text
Ground(C)
```

represent the grounding path from claim `C` to recoverable phenomena, measurements, records, decoders, traces, operational tests, or accepted layer modules.

Let:

```text
Exec(C)
```

represent the executability or operational consequence of claim `C`.

Let:

```text
Transfer(C, L_i, L_j)
```

represent whether claim `C` preserves consequence-bearing structure when moved from layer `L_i` to layer `L_j`.

Let:

```text
U
```

represent the use-context.

Let:

```text
H
```

represent the horizon.

Let:

```text
π
```

represent the projection, inspection lens, measurement mode, interpretation frame, diagrammatic view, or operational interface.

Let:

```text
θ_U
```

represent the adequacy threshold for use-context `U`.

Let:

```text
B_A
```

represent the reasoning budget of agent `A`.

Let:

```text
Complexity(C)
```

represent the inspection complexity of claim `C` under the selected mode.

Let:

```text
Diag(C)
```

represent diagnostics emitted by the claim compiler or linter.

The central question is not:

```text
Can all true claims be generated from first principles?
```

but:

```text
Can a bounded agent inspect the references, types, supports, consequences, transfer conditions, and complexity limits of a claim before relying on it?
```

In compressed form:

> A claim is not merely a sentence. It is a dependency-bearing structure used by a bounded agent under a selected purpose.

---

# 1. The Core Shift

The framework shifts from natural language as free expression to natural language as optionally inspectable source.

Ordinary language says:

```text
A constrains B.
```

The claim workbench asks:

```text
What is A?
What is B?
What type of constraint is meant?
Which transitions are restricted?
What would count as violation?
What realizes or enforces the constraint?
Across what horizon?
Under which projection?
For which use-context?
Can the constraint be observed, inferred, tested, executed, or only stipulated?
```

Ordinary language says:

```text
A and B constrain C.
```

The workbench asks:

```text
Do A and B jointly constrain C?
Do they independently constrain C?
Do they constrain C simultaneously?
Do they constrain C interchangeably?
Do they constrain different aspects of C?
Can one substitute for the other?
Does their conjunction create a new constraint not present in either alone?
```

Ordinary language says:

```text
This distinction matters.
```

The workbench asks:

```text
At which level?
Syntax level?
Semantic level?
Operational level?
Architectural level?
Empirical level?
Institutional level?
Cross-layer transfer level?
```

The claim remains allowed.

But the inspection reveals what has and has not been declared.

In compressed form:

> The framework does not replace language. It adds inspectable pressure points where language becomes consequence-bearing.

---

# 2. Why This Resembles Programming Tooling

Programming environments already separate several layers that ordinary users often experience as one thing.

A program can fail at the level of:

```text
characters
tokens
syntax
types
imports
linking
permissions
runtime state
external service availability
hardware capacity
user intention
```

An editor may detect some failures immediately.

Examples:

```text
imported module not found
symbol unresolved
function not defined
wrong argument count
type mismatch
unreachable branch
undefined variable
unused import
invalid path
missing dependency
```

The important feature is not that the editor derives all programs.

The important feature is that the editor can statically inspect selected relations before execution.

Natural-language reasoning needs analogous distinctions.

A claim can fail at the level of:

```text
symbol ambiguity
syntax ambiguity
reference ambiguity
semantic underdeclaration
missing support
projection mismatch
invalid transfer
unsupported operational consequence
unbounded scope
complexity beyond agent budget
```

A natural-language linter should therefore provide diagnostics such as:

```text
REFERENCE-UNRESOLVED:
    The claim imports a concept whose definition cannot be found in the active context.

SEMANTIC-UNDERDECLARED:
    The claim uses a structural verb without declaring its relation type.

GROUNDING-MISSING:
    The claim asserts a relation to reality without measurement, trace, decoder, source, or operational test.

TRANSFER-RISK:
    The claim moves vocabulary across layers without declaring preserved consequences.

COMPLEXITY-BUDGET-EXCEEDED:
    The support graph exceeds the declared inspection budget of the agent or system.
```

In compressed form:

> Programming tools show that not deriving everything is compatible with strong structural checking.

---

# 3. Boundedness Is the Condition of Scale

The framework scales only because every level is bounded.

A useful inspection mode must declare bounds such as:

```text
bounded alphabet
bounded grammar
bounded vocabulary module
bounded claim type
bounded semantic interpretation
bounded projection
bounded use-context
bounded horizon
bounded operational threshold
bounded support depth
bounded transfer scope
bounded inspection budget
```

Without bounds, a claim can expand indefinitely.

For example:

```text
A depends on B.
```

may invite:

```text
What is A?
What is B?
What does depend mean?
Depend materially, logically, causally, institutionally, biologically, computationally, economically, or psychologically?
What supports the support?
What supports that support?
What are all hidden assumptions?
What are all possible counterexamples?
What is the complete ontology of dependence?
```

This becomes combinatorial explosion.

A bounded framework does not try to inspect everything.

It asks:

```text
Which inspection mode is active?
Which consequences matter?
Which support depth is required?
Which horizon is relevant?
Which agent budget is available?
Which abstraction layers can be imported instead of expanded?
```

In compressed form:

> Scale comes not from infinite derivation, but from bounded inspection plus reusable abstraction barriers.

---

# 4. The Claim as a Source Object

A claim can be represented as a source object.

```text
Claim C {
    surface_form
    syntax_tree
    claim_type
    imported_terms
    local_definitions
    semantic_roles
    support_graph
    grounding_paths
    projection
    use_context
    horizon
    threshold
    transfer_scope
    operational_tests
    failure_modes
    diagnostics
}
```

Example:

```text
Claim C1 {
    surface_form:
        "Institutions depend on trust."

    claim_type:
        support claim

    imported_terms:
        institution
        trust
        dependence

    semantic_roles:
        institution -> supported target
        trust -> support candidate
        depend -> required support relation

    missing_declarations:
        institution subtype
        trust subtype
        dependency strength
        horizon
        failure condition
        empirical or conceptual status

    possible_operational_tests:
        remove trust-like support and inspect recognition, compliance, transaction cost, legitimacy, coordination, and persistence

    possible_diagnostics:
        semantically underdeclared
        operationally incomplete
        scope overextended if applied to all institutions without boundary
}
```

The source object is not necessarily visible in ordinary speech.

It becomes visible in inspection mode.

In compressed form:

> A sentence is the rendered artifact; the claim source contains references, types, supports, horizons, and diagnostics.

---

# 5. Inspection Modes

The workbench should support multiple inspection modes.

No single mode should pretend to answer all questions.

## 5.1 Syntax Inspection

Syntax inspection asks:

```text
Is the sentence or formal expression well-formed under the active grammar?
```

Possible diagnostics:

```text
SYNTAX-VALID
SYNTAX-INVALID
SYNTAX-AMBIGUOUS
GRAMMAR-MISMATCH
```

Example:

```text
"A and B constrain C."
```

may be syntactically valid.

But this says almost nothing about whether it is meaningful, grounded, operational, or transferable.

Compressed form:

> Syntax validity only says the expression can be parsed.

## 5.2 Reference Inspection

Reference inspection asks:

```text
Can the imported symbols, concepts, modules, named entities, files, sources, or definitions be resolved?
```

Programming analogue:

```text
ctrl-click into imported module
find definition
show usages
resolve dependency
```

Natural-language analogue:

```text
ctrl-click into concept definition
show supporting source
show declared primitive
show imported framework layer
show unresolved reference
```

Possible diagnostics:

```text
REFERENCE-RESOLVED
REFERENCE-UNRESOLVED
REFERENCE-AMBIGUOUS
REFERENCE-VERSION-MISMATCH
REFERENCE-HIDDEN-BEHIND-ABSTRACTION
```

Compressed form:

> Reference inspection asks whether the claim's named supports can be reached.

## 5.3 Semantic Typing

Semantic typing asks:

```text
What kind of claim is this?
What roles do its terms play?
Are the relation types declared?
```

Examples:

```text
A constrains B.
A supports B.
A causes B.
A recognizes B.
A stores B.
A transfers B.
A regenerates B.
A is analogous to B.
A implements B.
A projects to B.
```

Possible diagnostics:

```text
SEMANTICALLY-TYPED
SEMANTICALLY-UNDERDECLARED
RELATION-TYPE-MISSING
ROLE-CONFLICT
CATEGORY-MISMATCH
```

Compressed form:

> Semantic typing turns vague relation words into declared structural roles.

## 5.4 Grounding Inspection

Grounding inspection asks:

```text
What connects this claim to recoverable phenomena?
```

Grounding may include:

```text
measurement
trace
record
experiment
observation
decoder
institutional recognition
operational test
accepted model
imported layer module
counterfactual support removal
```

Possible diagnostics:

```text
GROUNDED
PARTIALLY-GROUNDED
GROUNDING-MISSING
GROUNDING-INDIRECT
HIDDEN-SUPPORT-DECLARED
HIDDEN-SUPPORT-UNDECLARED
```

Compressed form:

> Grounding inspection asks whether the claim can touch something recoverable rather than only repeat itself.

## 5.5 Operational Inspection

Operational inspection asks:

```text
What changes if this claim is true, false, applied, removed, or violated?
```

It checks whether the claim constrains:

```text
prediction
navigation
intervention
repair
failure detection
resource allocation
design choice
legal action
technical execution
```

Possible diagnostics:

```text
OPERATIONAL
OPERATIONALLY-UNGROUNDED
NO-ACTION-DIFFERENCE
NO-FAILURE-CONDITION
NO-COUNTERFACTUAL-TEST
EXECUTION-PATH-MISSING
```

Compressed form:

> A claim becomes operational when accepting it changes reachable action or expected consequence.

## 5.6 Transferability Inspection

Transferability inspection asks:

```text
Can this claim move across layers while preserving consequence-bearing structure?
```

Example:

```text
flow
```

may transfer across:

```text
water flow
electric current
blood flow
data flow
money flow
attention flow
legitimacy flow
```

But the transfer is not automatically valid.

The carrier, boundary, conservation rules, failure semantics, and implementation regime may change.

Possible diagnostics:

```text
TRANSFER-VALID
TRANSFER-PARTIAL
TRANSFER-RISKY
ANALOGY-WITHOUT-CONSEQUENCE-MAP
IMPLEMENTATION-REGIME-MISMATCH
SCOPE-OVEREXTENDED
```

Compressed form:

> Transferability requires preserved consequences, not repeated vocabulary.

## 5.7 Complexity Inspection

Complexity inspection asks:

```text
Can the selected agent or system inspect this claim's support closure within budget?
```

Possible diagnostics:

```text
WITHIN-INSPECTION-BUDGET
COMPLEXITY-WARNING
SUPPORT-CLOSURE-TOO-DEEP
DEPENDENCY-GRAPH-TOO-WIDE
AGENT-DISQUALIFIED-FOR-GLOBAL-REASONING
MODULE-IMPORT-RECOMMENDED
CLAIM-SCOPE-REDUCTION-RECOMMENDED
```

Compressed form:

> Complexity inspection detects when a claim exceeds the reasoning capacity of the current agent.

---

# 6. The Diagnostic Lattice

Instead of a binary result:

```text
valid / invalid
true / false
allowed / forbidden
```

the workbench should return a richer diagnostic lattice.

A claim may be:

```text
syntactically valid
semantically underdeclared
reference ambiguous
grounded through an imported layer
operationally incomplete
transfer-risky
complexity-bounded
valid only for a narrowed use-context
```

Example diagnostic:

```text
Claim:
    "Economic systems are like biological organisms."

Diagnostics:
    SYNTAX-VALID
    SEMANTIC-UNDERDECLARED
    ANALOGY-CLAIM-DETECTED
    TRANSFER-RISK
    PRESERVED-CONSEQUENCE-MAP-MISSING
    IMPLEMENTATION-REGIME-MISMATCH
    SCOPE-OVEREXTENDED

Suggested repair:
    Specify which structural role transfers:
        metabolism -> resource throughput?
        immune system -> threat detection?
        homeostasis -> feedback regulation?
        reproduction -> institutional replication?
        death -> systemic failure threshold?
```

This is more informative than saying:

```text
true
```

or:

```text
false
```

The diagnostic tells the user where the claim is weak.

In compressed form:

> The output should not merely classify truth. It should expose the claim's missing declarations and unsafe transfers.

---

# 7. Claim Types

A claim linter needs structural claim types.

## 7.1 Identity Claim

```text
A is B.
```

Possible interpretations:

```text
class membership
identity equality
role assignment
metaphor
implementation
projection
renaming
legal recognition
operational equivalence
```

Diagnostic question:

```text
Which kind of "is" is meant?
```

Compressed form:

> Identity claims are dangerous because ordinary language overloads "is."

## 7.2 Constraint Claim

```text
A constrains B.
```

Required declarations:

```text
constrainer
constrained target
admissible variation
restricted transition
violation condition
realization or enforcement mechanism
validity boundary
```

Example:

```text
ConstraintClaim {
    constrainer: A
    target: B
    restricts: transitions_of(B)
    violation_condition: declared
    realization: physical / logical / legal / economic / computational / institutional / social
    horizon: H
}
```

Compressed form:

> A constraint claim must say which possible changes are no longer admissible.

## 7.3 Support Claim

```text
A supports B.
```

Required declarations:

```text
supporting condition
supported target
support type
availability condition
removal effect
substitution options
degradation mode
horizon
```

Counterfactual test:

```text
Remove A.
Inspect whether B remains recoverable or executable above threshold.
```

Compressed form:

> A support claim becomes meaningful when removal changes persistence, recoverability, or execution.

## 7.4 Causal Claim

```text
A causes B.
```

Required declarations:

```text
cause candidate
effect candidate
mechanism or intervention path
temporal ordering
counterfactual dependence
confound controls
scope
probabilistic or deterministic status
```

Possible diagnostics:

```text
CORRELATION-NOT-CAUSE
MECHANISM-MISSING
COUNTERFACTUAL-UNDECLARED
SCOPE-OVEREXTENDED
```

Compressed form:

> A causal claim requires more than observed sequence or verbal association.

## 7.5 Boundary Claim

```text
A separates B from C.
```

Required declarations:

```text
regions or regimes separated
transfer rule
filtering semantics
breach condition
support mechanism
recognition path
validity horizon
```

Compressed form:

> A boundary is a transfer regime, not merely a named separation.

## 7.6 Flow Claim

```text
X flows from A to B.
```

Required declarations:

```text
carrier
source
sink or cycle
channel
rate or capacity
conversion rules
boundary crossings
support
interruption failure
```

Compressed form:

> Flow is typed throughput through constrained channels.

## 7.7 Recognition Claim

```text
A recognizes B.
```

Required declarations:

```text
recognizer
target distinction
decoder
input path
action difference
error model
support
```

Compressed form:

> Recognition becomes operational when recovered distinction changes downstream action.

## 7.8 Transfer Claim

```text
This structure in layer L_i also applies in layer L_j.
```

Required declarations:

```text
source layer
target layer
invariant role
implementation in source layer
implementation in target layer
preserved consequences
broken consequences
validity boundary
counterfactual tests
```

Compressed form:

> Transfer claims must declare the role that survives and the implementation that changes.

---

# 8. Syntax, Semantics, Operation, Architecture

A central insight is that the same word can participate at different levels.

Example:

```text
distinction
```

At the syntax level:

```text
A word is distinct from another word by having different letters or token form.
```

At the semantic level:

```text
A concept is distinct by having a different declared meaning or role.
```

At the operational level:

```text
A distinction matters if recovering it changes action, prediction, transition, repair, or failure detection.
```

At the architectural level:

```text
A distinction matters if it changes module boundaries, imports, exports, supports, or abstraction barriers.
```

At the empirical level:

```text
A distinction matters if it corresponds to a recoverable phenomenon, measurement, trace, or intervention difference.
```

At the institutional level:

```text
A distinction matters if a recognizer, procedure, authority, record, or role acts differently because of it.
```

Therefore a linter should ask:

```text
At which layer is this distinction being claimed?
```

A claim may be valid at one layer and invalid at another.

Example:

```text
"constraint" and "constraints" are syntactically distinct tokens.
```

This does not automatically mean:

```text
they represent distinct semantic concepts.
```

Nor does it mean:

```text
they produce different operational consequences.
```

Compressed form:

> Distinctness itself is layer-indexed: token difference, meaning difference, operational difference, and architectural difference are not the same claim.

---

# 9. The Ctrl-Click Principle for Claims

In programming, ctrl-click navigates from use to definition.

A claim workbench should generalize this.

When a user ctrl-clicks a term, relation, or claim, the workbench may show:

```text
definition
source module
import path
usage sites
support graph
hidden assumptions
validity boundary
failure modes
operational tests
transfer map
known unresolved references
```

Example:

```text
Claim:
    "Social trust supports institutional persistence."
```

Ctrl-click:

```text
social trust
```

may show:

```text
Term: social trust
Type: recognition/support structure
Imported from: institutional-core@0.1
Possible subtypes:
    interpersonal trust
    procedural trust
    legal trust
    financial credit trust
    epistemic trust
    legitimacy trust
Known supports:
    record continuity
    expectation stability
    enforcement reliability
    shared norms
    communication channels
Failure modes:
    fraud
    authority collapse
    record falsification
    coordination failure
    credibility loss
```

Ctrl-click:

```text
supports
```

may show:

```text
Relation type: SupportClaim
Required declarations:
    supported target
    support type
    removal effect
    substitution options
    degradation mode
    horizon
```

Ctrl-click:

```text
institutional persistence
```

may show:

```text
Target type: PersistentInstitutionalObject
Required supports:
    recognition
    records
    roles
    procedures
    authority paths
    resource flows
    regeneration mechanisms
```

In compressed form:

> A claim becomes inspectable when every important term and relation has a navigable declaration.

---

# 10. Bounded Semantic Interpretation

Semantic interpretation must be bounded.

A word does not have one total meaning across all possible contexts.

Instead, a word has declared interpretations within modules, projections, and use-contexts.

Example:

```text
constraint
```

may have module-specific interpretations:

```text
logic-core:
    formula restricting admissible models

physics-core:
    physical restriction on possible states or transitions

software-core:
    type, invariant, precondition, protocol, resource limit, or API rule

institutional-core:
    legal, procedural, economic, organizational, or legitimacy restriction

cognitive-core:
    attention, memory, prediction, or action-selection restriction
```

A claim using `constraint` should either:

```text
import one interpretation
```

or:

```text
declare a cross-layer invariant role and map local implementations
```

Possible diagnostic:

```text
SEMANTIC-MODULE-MISSING:
    The claim uses "constraint" without declaring whether it is logical, physical, computational, institutional, cognitive, or cross-layer structural.
```

In compressed form:

> Meaning becomes inspectable when interpretation is module-bound rather than assumed globally obvious.

---

# 11. Executability Beyond Code

Executability should not be limited to software.

A claim is executable when it can be used to produce, restrict, or evaluate an action, transition, intervention, diagnosis, or construction.

Examples:

```text
software:
    code can run

mathematics:
    proof steps can be checked

engineering:
    design constraints can be tested before fabrication

law:
    rule can be applied by an institution

organization:
    procedure can be performed by roles with resources

science:
    hypothesis can guide measurement or intervention

medicine:
    diagnosis can change treatment path

navigation:
    map can guide movement

maintenance:
    failure model can guide repair
```

Executability requires:

```text
actors or processes
inputs
preconditions
transition rules
supports
resources
failure modes
recognition paths
termination or adequacy condition
```

Possible diagnostic:

```text
EXECUTABILITY-MISSING:
    Claim is stated as actionable but lacks actor, input, procedure, support, or success/failure condition.
```

Compressed form:

> Executability is not only running code; it is consequence-bearing use under declared supports.

---

# 12. Claim Verification Is Not One Thing

The phrase:

```text
claim verification
```

is too coarse.

Different claims require different verification regimes.

## 12.1 Syntactic Verification

```text
Can the expression be parsed?
```

## 12.2 Definitional Verification

```text
Does the claim follow from declared definitions?
```

## 12.3 Logical Verification

```text
Does the conclusion follow from premises under a formal system?
```

## 12.4 Type Verification

```text
Are the roles compatible?
```

## 12.5 Reference Verification

```text
Can the referenced modules, terms, entities, files, or sources be resolved?
```

## 12.6 Empirical Verification

```text
Is there measurement, observation, experiment, trace, or data support?
```

## 12.7 Operational Verification

```text
Does the claim work when used for prediction, navigation, intervention, repair, or execution?
```

## 12.8 Transfer Verification

```text
Does the claim preserve consequences when moved across layers or domains?
```

## 12.9 Complexity Verification

```text
Can the claim be inspected within the agent's declared reasoning budget?
```

In compressed form:

> Verification must be typed; otherwise the word hides too many different checks.

---

# 13. Complexity and Agent Disqualification

A bounded agent cannot reason properly about every claim at full support closure.

The framework should therefore include agent-relative diagnostics.

Let:

```text
B_A
```

represent the inspection budget of agent `A`.

Let:

```text
Cost(Inspect(C, mode, depth))
```

represent the cost of inspecting claim `C` under a selected mode and depth.

Then:

```text
Cost(Inspect(C, mode, depth)) > B_A
```

should produce:

```text
COMPLEXITY-BUDGET-EXCEEDED
```

This is not merely an inconvenience.

It means the agent is disqualified from making strong unbounded claims at that inspection level.

Possible diagnostic:

```text
AGENT-DISQUALIFIED-FOR-GLOBAL-CLAIM:
    The claim's required support closure exceeds the declared reasoning budget of the current agent.
    Recommended repair:
        reduce claim scope
        import verified layer modules
        decompose into subclaims
        declare uncertainty
        shift from proof claim to hypothesis claim
        weaken horizon
        select a narrower projection
```

This protects the agent from counterproductive reasoning.

Without such a diagnostic, the agent may attempt to reason globally, recursively expand every dependency, lose the relevant use-context, and become less capable of action.

In compressed form:

> Combinatorial explosion is not just hard; it is a signal that the claim must be modularized, weakened, or delegated.

---

# 14. Abstraction Barriers as Cognitive Safety

Abstraction barriers are not merely software conveniences.

They are cognitive safety devices.

A bounded agent uses abstraction barriers to avoid expanding every dependency at every moment.

Example:

```text
organization
```

may import:

```text
roles
records
recognition
procedures
resources
communication channels
authority paths
```

It should not require the user to inspect:

```text
neural activity of every participant
molecular substrate of every record
semiconductor physics of every database
energy infrastructure of every communication channel
```

unless the selected use-context requires those details.

A valid abstraction barrier says:

```text
Below this interface, details are hidden.
Above this interface, exported distinctions may be used within declared bounds.
If hidden supports become consequence-bearing, the linter will warn.
```

Possible diagnostic:

```text
ABSTRACTION-BARRIER-LEAK:
    The upper claim depends on a hidden lower-layer detail not exported by the imported module.
```

Compressed form:

> An abstraction barrier is a controlled refusal to inspect irrelevant depth.

---

# 15. Bounded Transferability

Transferability is a bounded operation.

A structural primitive such as:

```text
flow
```

may appear across many layers.

But each transfer must specify:

```text
carrier
channel
capacity
boundary conditions
conversion rules
failure modes
conservation or non-conservation
measurement or recognition path
```

Example:

```text
money flow
```

is not identical to:

```text
blood flow
```

But they may share a structural role:

```text
throughput through constrained channels that supports persistence of a larger system
```

Transfer is valid only where preserved consequences are declared.

Possible transfer map:

```text
Invariant role:
    flow

Source implementation:
    blood through vessels

Target implementation:
    money through payment and credit systems

Preserved consequences:
    interruption damages system function
    bottlenecks create downstream scarcity
    channel capacity matters
    circulation supports persistence

Broken consequences:
    blood is materially conserved differently
    money depends on institutional recognition
    credit can be created or destroyed by accounting rules
    biological and financial failure thresholds differ
```

Compressed form:

> Transferability scales only by preserving roles while declaring implementation differences.

---

# 16. The Natural-Language Linter

A natural-language linter should not behave like an authoritarian grammar checker.

It should behave like an optional inspection engine.

It should not say:

```text
You may not say this.
```

It should say:

```text
Under the selected inspection mode, this claim has the following unresolved declarations.
```

Example:

```text
Claim:
    "Language is grounded in reality."
```

Possible diagnostics:

```text
SYNTAX-VALID
SEMANTIC-UNDERDECLARED
GROUNDING-RELATION-MISSING
REALITY-LAYER-UNSPECIFIED
OPERATIONAL-TEST-MISSING
SCOPE-OVEREXTENDED
```

Suggested repairs:

```text
Specify whether grounding means:
    reference to phenomena
    recoverability through perception
    operational success
    social recognition
    causal coupling
    measurement trace
    embodied action
    predictive compression

Specify whether reality means:
    physical substrate
    biological environment
    cognitive interface
    institutional world
    technical system
    cross-layer constraint regime
```

In compressed form:

> The linter does not prohibit claims; it reveals what a claim still owes.

---

# 17. Primitive Candidates

The framework should begin with a small vocabulary of high-transfer primitives.

Candidate primitives:

```text
distinction
state
relation
transition
constraint
coupling
boundary
flow
storage
support
projection
horizon
threshold
recognition
failure
repair
regeneration
selection
feedback
validity boundary
abstraction barrier
module
import
export
reference
claim
```

These are not final substances.

They are structural roles.

Each primitive must define:

```text
role
required declarations
admissible use
invalid use
implementation examples
inspection questions
failure diagnostics
```

Example:

```text
Primitive: constraint

Role:
    restricts admissible variation or transition

Required declarations:
    applies_to
    restricts
    admissible_variation
    violation_condition
    realization_or_enforcement
    validity_boundary

Invalid uses:
    saying A constrains B without specifying what variation is restricted
    using constraint as vague influence
    transferring physical constraint into institutional context without implementation mapping
```

Compressed form:

> A primitive is useful only when it carries obligations, not just a name.

---

# 18. From English to Typed Structural Form

The workbench may translate ordinary claims into typed structural forms.

Example:

```text
Surface claim:
    "A and B constrain C."
```

Possible typed interpretations:

```text
JointConstraint(A, B, C):
    C is constrained only when A and B are both present.

IndependentConstraints(A, B, C):
    A constrains C and B constrains C separately.

SubstitutableConstraint(A, B, C):
    either A or B can constrain C sufficiently.

SimultaneousConstraint(A, B, C):
    A and B constrain C at the same time but through different dimensions.

InteractingConstraint(A, B, C):
    A modifies how B constrains C, or B modifies how A constrains C.

OverdeterminedConstraint(A, B, C):
    either support alone is enough, but both are present.
```

The sentence does not choose among these by itself.

The linter should mark it as:

```text
SEMANTIC-UNDERDECLARED: conjunction relation not specified.
```

Compressed form:

> Natural language often compresses multiple structural possibilities into one surface form.

---

# 19. First Principles Without Total Derivation

The framework can use first principles without deriving every claim from them.

A small kernel may define:

```text
distinction
relation
state
transition
constraint
support
recognition
failure
projection
horizon
threshold
```

From these, one can build reusable layer modules.

But ordinary use should not require full derivation.

Workflow:

```text
1. Start from a small structural kernel.
2. Build or import layer modules.
3. Use layer exports in claims.
4. Inspect references and supports on demand.
5. Expand lower layers only when required by the use-context.
6. Emit diagnostics when claims exceed declared bounds.
```

This parallels programming.

A programmer does not derive each API call from transistor physics.

The programmer imports modules with declared interfaces.

Similarly, a claim user should not derive each institutional claim from physics, biology, cognition, and history.

The user should import relevant layer modules and inspect hidden supports when they become consequence-bearing.

Compressed form:

> First principles provide the kernel; modules provide usability.

---

# 20. Self-Linting Requirement

The claim-linting framework must lint itself.

It must declare:

```text
purpose
primitives
imported assumptions
exported claims
hidden supports
validity boundaries
known failure modes
invalid use-contexts
complexity limits
revision rules
```

Example:

```text
FrameworkMap BoundedSemanticCompilation {
    purpose:
        provide on-demand structural inspection for claims used by bounded agents

    primitives:
        distinction
        relation
        constraint
        support
        transition
        recognition
        projection
        horizon
        threshold
        failure
        transfer
        module
        reference

    imported assumptions:
        claims can be partially typed
        some structural roles transfer across domains
        bounded agents benefit from diagnostics
        abstraction barriers can preserve usability

    hidden supports:
        reliability of imported layer modules
        adequacy of selected primitives
        recoverability of relevant distinctions
        interpretability of diagnostics by users

    exported claims:
        natural-language claims can be inspected without being fully formalized
        verification is typed and mode-specific
        transferability requires consequence mapping
        complexity explosion should trigger modularization or scope reduction

    invalid use-contexts:
        deriving all language from first principles
        replacing empirical science
        eliminating ambiguity from natural language
        proving ultimate metaphysical ontology
        guaranteeing truth of all claims

    failure modes:
        overformalization
        false precision
        excessive diagnostic burden
        pretending unsupported modules are verified
        confusing syntactic validity with operational grounding
        collapsing all reasoning into one universal inspection mode
}
```

Compressed form:

> A claim-linter is mature only when it states where its own claims stop.

---

# 21. Failure Modes

The framework has important failure modes.

## 21.1 Overformalization

The system may demand too many declarations for ordinary thought.

Repair:

```text
Make inspection optional and mode-specific.
```

## 21.2 False Precision

The system may produce formal-looking diagnostics that are not actually grounded.

Repair:

```text
Declare diagnostic confidence and support source.
```

## 21.3 Infinite Expansion

The system may recursively expand every support.

Repair:

```text
Use abstraction barriers, support-depth limits, and agent-budget diagnostics.
```

## 21.4 Transfer Illusion

The system may treat repeated vocabulary as structural equivalence.

Repair:

```text
Require preserved consequence maps.
```

## 21.5 Module Authority Error

The system may treat imported modules as final truth.

Repair:

```text
Version modules, declare assumptions, and allow source inspection.
```

## 21.6 Context Collapse

The system may treat validity as absolute rather than use-context indexed.

Repair:

```text
Require use-context, projection, horizon, and threshold for strong claims.
```

## 21.7 Agent Overreach

The user may make claims whose support closure exceeds their reasoning capacity.

Repair:

```text
Emit complexity-budget diagnostics and recommend decomposition.
```

Compressed form:

> The framework fails when it forgets that it exists to help bounded agents, not to erase boundedness.

---

# 22. Example: Inspecting a Claim

Claim:

```text
"English claims can be grounded in reality through structural primitives."
```

Possible source object:

```text
Claim C {
    claim_type:
        framework claim

    imported_terms:
        English claims
        grounded
        reality
        structural primitives

    semantic roles:
        English claims -> target symbolic artifacts
        grounded -> relation requiring clarification
        reality -> target constraint domain
        structural primitives -> grounding interface candidates

    missing declarations:
        meaning of grounding
        reality layer
        primitive set
        operational test
        validity boundary
        claim scope

    possible interpretations:
        grounding as reference
        grounding as operational success
        grounding as measurement recoverability
        grounding as causal coupling
        grounding as institutional recognition
        grounding as support path

    diagnostics:
        SYNTAX-VALID
        SEMANTIC-UNDERDECLARED
        GROUNDING-RELATION-MISSING
        SCOPE-OVEREXTENDED
        OPERATIONAL-TEST-REQUIRED

    repair:
        weaken to:
            "Some English claims can be partially inspected by mapping their relation words to structural primitives, then checking support paths, operational consequences, and validity boundaries under a declared use-context."
}
```

The repaired claim is less grand but more usable.

Compressed form:

> The linter does not merely criticize; it helps produce a stronger bounded claim.

---

# 23. Example: Transferability Diagnostic

Claim:

```text
"Markets are ecosystems."
```

Diagnostics:

```text
SYNTAX-VALID
IDENTITY-CLAIM-AMBIGUOUS
METAPHOR-DETECTED
TRANSFER-RISK
IMPLEMENTATION-REGIME-MISMATCH
PRESERVED-CONSEQUENCE-MAP-MISSING
```

Possible repair:

```text
"Markets and ecosystems can both be modeled as systems with flows, selection, feedback, resource constraints, niches, adaptation, and failure cascades, but their implementation regimes differ: ecosystems are biological and material, while markets depend on institutions, money, contracts, legal recognition, information, and social trust."
```

Now the claim distinguishes:

```text
shared structural roles
```

from:

```text
local implementation regimes
```

Compressed form:

> A risky metaphor becomes useful when converted into a bounded transfer map.

---

# 24. Example: Complexity Diagnostic

Claim:

```text
"Civilization depends on energy, trust, institutions, technology, and communication."
```

This may be structurally plausible.

But its support closure is enormous.

A linter should not expand all dependencies by default.

It should emit:

```text
COMPLEXITY-WARNING:
    Claim imports multiple high-level modules with deep hidden supports.
    Full support closure likely exceeds single-agent inspection budget.

Recommended modes:
    inspect energy dependency only
    inspect institutional recognition only
    inspect communication infrastructure only
    inspect trust as support relation only
    reduce horizon
    narrow civilization subtype
    import pre-checked layer modules
```

The correct repair is not to abandon the claim.

The correct repair is to bound inspection.

Compressed form:

> Complex claims should be navigated by slices, not swallowed whole.

---

# 25. Minimal Implementation Sketch

A minimal claim workbench might begin with:

```text
1. A small primitive vocabulary.
2. A claim-type classifier.
3. A reference resolver.
4. A semantic-role parser.
5. A required-declaration checker.
6. A support graph builder.
7. A grounding-path field.
8. A transferability checker.
9. A complexity budget estimator.
10. A diagnostic emitter.
```

Minimal schema:

```text
ClaimModule {
    id
    surface_form
    author
    version
    imported_modules
    terms
    claim_type
    semantic_roles
    required_declarations
    support_graph
    grounding_paths
    transfer_scope
    operational_tests
    use_context
    horizon
    threshold
    inspection_budget
    diagnostics
}
```

Minimal diagnostic format:

```text
Diagnostic {
    code
    severity
    target
    explanation
    missing_declaration
    consequence
    suggested_repair
    confidence
}
```

Compressed form:

> The first implementation need not solve truth; it only needs to expose missing structure.

---

# 26. Relation to Existing Formal Systems

The framework is adjacent to, but not identical with:

```text
formal logic
type theory
programming language compilers
knowledge graphs
ontology engineering
proof assistants
static analyzers
model checkers
semantic parsers
argument maps
scientific modeling frameworks
systems engineering tools
```

Its distinctive emphasis is:

```text
natural-language claims as inspectable source artifacts
cross-layer primitive vocabulary
support and hidden-dependency declarations
projection-relative validity
operational grounding
transferability diagnostics
agent-budget limits
```

It does not replace formal logic.

It may import formal logic as one inspection mode.

It does not replace empirical science.

It may represent empirical support paths.

It does not replace domain expertise.

It may expose where domain expertise is required.

It does not replace programming-language compilers.

It generalizes the idea of static checking to broader claim structures.

Compressed form:

> This is not a universal replacement for existing tools; it is an interface layer for inspecting claims across them.

---

# 27. The Main Thesis

The main thesis is:

```text
Bounded agents need claims to be inspectable through bounded modes.
```

A claim should be allowed to remain ordinary language.

But when the claim becomes consequence-bearing, the user should be able to inspect:

```text
what it references
what it imports
what it means structurally
what supports it assumes
what grounds it
what it can execute
where it transfers
where it fails
how much reasoning budget it requires
```

This yields the compressed architecture:

```text
claim
    -> parse
        -> resolve references
            -> assign structural type
                -> declare supports
                    -> inspect grounding
                        -> test operational consequence
                            -> check transferability
                                -> estimate complexity
                                    -> emit diagnostics
```

The result is not total certainty.

The result is improved navigability.

In compressed form:

> A good claim is not one that pretends to contain reality. A good claim exposes enough structure for bounded agents to know how, where, and whether to use it.

---

# 28. Final Compression

The framework can be summarized as follows:

```text
Natural language is permissive.
Reasoning is bounded.
Claims become dangerous when they are used beyond their declared supports.
Programming tools show that static inspection is possible without total derivation.
The same principle can be generalized to claim inspection.
A claim can be syntactically valid while semantically underdeclared, operationally ungrounded, or transfer-risky.
Cross-layer primitives help because they provide reusable structural roles.
Those primitives must remain bounded by projection, horizon, use-context, support, and implementation regime.
Combinatorial explosion is not a defect to hide; it is a diagnostic that the claim exceeds the current agent's reasoning budget.
The remedy is modularization, abstraction barriers, imported layers, narrowed scope, and explicit failure modes.
```

In most compressed form:

> Bounded semantic compilation is the attempt to give natural-language claims the inspection affordances of code, without pretending that language, reality, or truth can be fully compiled from first principles.
