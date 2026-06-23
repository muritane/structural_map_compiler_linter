# Structural Map Compiler / Linter

## A Standalone Framework for Typed Map-Making, Static Validation, Structural Diagnostics, and Consequence-Preserving Abstraction

---

# Status

This document is standalone.

It extends the following related framework ideas:

```text
objecthood as recoverable constraint-stability
staticity failure under operational proof
cross-layer invariant distinction mapping
recoverability support fields
counterfactual support removal
constraint-bound hierarchical emergence
```

Its purpose is to turn those ideas into a more explicit development vision:

```text
A compiler/linter for structural maps.
```

The goal is not to simulate all of reality.

The goal is to help bounded agents construct maps that are:

```text
typed
use-context aware
horizon-bound
projection-explicit
support-aware
capacity-aware
failure-aware
consequence-preserving
statically checkable
```

A structural map should not be judged by whether it contains every detail.

A structural map should be judged by whether the distinctions it includes are sufficient and coherent for the declared use-context, horizon, projection, and operational threshold.

In compressed form:

> A structural map compiler checks whether a map preserves the distinctions that matter for navigation, prediction, intervention, maintenance, and failure recognition.

---

# Abstract

Most maps are not complete descriptions.

A train map does not show every rail bolt, signal relay, passenger, maintenance defect, or weather condition.

A software architecture diagram does not show every byte, syscall, thread scheduling event, cache line, or deployment accident.

An organizational chart does not show every conversation, informal influence path, private belief, or forgotten document.

A biological pathway diagram does not show every molecular vibration, solvent collision, or thermal fluctuation.

The omission is not automatically an error.

Omission is the condition of usability.

But omission becomes an error when the omitted distinction changes the declared task.

A passenger route map may omit platform capacity.

An operational railway schedule cannot.

A conceptual diagram may represent a station as a hub.

A scheduling map cannot casually declare that fifty trains stop simultaneously at a station with three platforms.

The same visual node can be valid in one use-context and invalid in another.

This document proposes a framework for handling that difference.

The core idea is:

```text
A map is a typed representation of recoverable distinctions, relations, constraints, transitions, supports, and failure conditions for a declared use-context and horizon.
```

A structural map compiler/linter would not ask:

```text
Does this map represent everything?
```

It would ask:

```text
Given the declared use-context, projection, horizon, and threshold, are the represented distinctions sufficient, coherent, and consequence-preserving?
```

In compressed form:

> The compiler does not punish abstraction. It punishes untyped abstraction that breaks the intended use.

---

# 0. Orientation

Let:

```text
M
```

represent a map.

Let:

```text
R
```

represent the target system, domain, or reality-region being mapped.

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
Π = {π_i}
```

represent projections, views, sensors, abstractions, or representational lenses.

Let:

```text
K
```

represent the active constraint regime.

Let:

```text
D
```

represent a recoverable distinction.

Let:

```text
C
```

represent a cluster of identity-relevant or task-relevant distinctions.

Let:

```text
T_K
```

represent admissible transitions under constraint regime `K`.

Let:

```text
Supp
```

represent the support graph required to keep distinctions recoverable or executable.

Let:

```text
θ_U
```

represent the threshold of adequacy for use-context `U`.

Let:

```text
Diag(M)
```

represent diagnostics emitted by the compiler/linter.

The central question is not:

```text
Is M complete?
```

but:

```text
Is M adequate for U across H under Π, K, and θ_U?
```

In compressed form:

> A map is valid only relative to a declared task, projection, horizon, threshold, and constraint regime.

---

# 1. The Core Vision

The proposed system is a general-purpose environment for building, checking, and refining structural maps.

It is analogous to:

```text
VS Code        -> editing, syntax, type hints, diagnostics
compiler       -> rejects invalid programs before runtime
linter         -> flags underspecified, inconsistent, or risky constructs
CAD software   -> checks design constraints before fabrication
Unity          -> typed scene graph, components, constraints, runtime behavior
Photoshop      -> layered manipulation of a representation
train map      -> typed abstraction for navigation or operation
```

But the target is not only code, images, games, or railways.

The target is structural map-making across domains:

```text
software systems
organizations
institutions
supply chains
scientific models
legal systems
biological systems
cognitive systems
infrastructure networks
civilizational processes
cross-layer analogies
```

The system should allow a user to declare:

```text
objects
boundaries
flows
states
relations
transitions
constraints
supports
projections
horizons
thresholds
failure modes
regeneration mechanisms
recognition paths
```

Then it should check whether the map is coherent for the intended use.

In compressed form:

> The vision is a typed workbench for consequence-preserving abstraction.

---

# 2. Why a Compiler/Linter Instead of a Theory of Everything?

A total description of reality is impossible for bounded agents.

Even if a total description were available, it would usually be unusable.

Maps are valuable because they discard most detail while preserving selected consequences.

The relevant distinction is:

```text
useful abstraction
```

versus:

```text
invalid omission
```

A compiler/linter is the right metaphor because it can detect structural errors without simulating every event.

It can reject or warn about claims such as:

```text
a flow with no carrier
a boundary with no transfer semantics
a persistent object with no support path
a hub with impossible capacity
a dependency with no reachable provider
a failure mode with no threshold
a cross-layer analogy with no consequence-preserving mapping
a proof claim with no decoder or recoverable distinction
an institution with no recognition or regeneration path
```

This is different from dynamic simulation.

A dynamic simulator asks:

```text
What happens step by step under changing conditions?
```

A structural compiler/linter asks:

```text
Is this map even well-typed and statically plausible before runtime dynamics begin?
```

In compressed form:

> Static validation catches impossible or under-typed maps before expensive simulation or real-world failure.

---

# 3. The Train Map Example

A passenger railway map may represent a station as:

```text
Station S
```

with edges:

```text
Line A -> S -> Line B
Line C -> S -> Line D
```

For passenger navigation, this may be adequate.

The use-context is:

```text
U = find a route between stations
```

The horizon is:

```text
H = ordinary trip planning
```

The projection is:

```text
π = connectivity and transfer possibility
```

For this use-context, the map can omit:

```text
platform count
signal blocks
track geometry
train length
dwell time
crew schedule
rolling stock assignment
passenger crowding
maintenance state
```

But if the use-context changes to operational scheduling, the same abstraction may become invalid.

Now the station must have typed capacity:

```text
Station {
    platforms: 3
    tracks: 4
    max_simultaneous_trains: 3
    transfer_edges: [...]
    dwell_constraints: ...
    ingress_egress_capacity: ...
}
```

The compiler can now reject:

```text
StopEvent {
    station: S
    simultaneous_trains: 50
}
```

because:

```text
50 > max_simultaneous_trains(S)
```

This does not require full simulation.

It does not model:

```text
someone holding a door
rain slowing boarding
signal cascade delays
crew absence
mechanical failure
passenger panic
```

Those belong to dynamic or stochastic simulation.

The compiler/linter only checks whether the declared map violates static structural constraints.

In compressed form:

> A hub is valid for route navigation only when the declared use-context does not require platform-capacity semantics.

---

# 4. Levels of Map Machinery

The proposed framework can be organized into levels.

## Level 0: Vocabulary

Basic structural distinction types:

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
signal
noise
gradient
feedback
selection
stability
instability
failure
repair
regeneration
recognition
projection
horizon
cost
threshold
```

This level names reusable structural roles.

It does not yet enforce correctness.

Compressed form:

> Vocabulary gives names to recurring structural roles.

---

## Level 1: Type System

Each structural role receives admissibility conditions.

Example:

```text
Flow requires:
    source
    sink or circulation
    carrier
    channel
    transfer rule
    capacity or rate
    boundary interaction
    failure condition
```

Example:

```text
Boundary requires:
    at least two regions or regimes
    transfer condition
    filtering or separation semantics
    breach condition
    support mechanism
    validity horizon
```

Example:

```text
PersistentObject requires:
    identity-relevant distinction cluster
    projection
    decoder or recognition path
    support graph
    stability or regeneration condition
    horizon
    threshold
```

Compressed form:

> The type system says what must be declared before a distinction can be used safely.

---

## Level 2: Static Validation

The compiler/linter checks consistency without full runtime simulation.

Examples:

```text
capacity constraint violation
missing decoder
unsupported flow
unbounded transition
invalid boundary
untyped objecthood
missing horizon
projection mismatch
impossible simultaneous occupancy
circular support without regeneration
cross-layer analogy without mapped consequences
```

Compressed form:

> Static validation rejects maps that are structurally incoherent before dynamics begin.

---

## Level 3: Operational Model

The map can be extended with transition semantics.

Examples:

```text
state machines
scheduling models
dependency graphs
resource allocation models
repair models
support substitution models
regeneration models
```

This level asks:

```text
What transitions are admissible?
What changes when a support is removed?
What state follows from this intervention?
Which failures propagate?
```

Compressed form:

> Operational modeling adds consequence-bearing transitions.

---

## Level 4: Dynamic Simulation

The system can later connect to simulation engines.

Examples:

```text
queueing models
agent-based models
stochastic delays
feedback loops
cascading failures
load variation
maintenance events
environmental perturbations
```

This level is deeper than the initial compiler/linter vision.

The framework should not require it at the beginning.

Compressed form:

> Simulation is optional; static typed adequacy comes first.

---

# 5. Map Validity Is Use-Context Indexed

No map is simply valid or invalid in the abstract.

A map is valid for some use and invalid for another.

A subway map can be valid for:

```text
passenger navigation
```

and invalid for:

```text
signal engineering
platform staffing
emergency evacuation
rolling stock optimization
real-time disruption management
```

A software architecture diagram can be valid for:

```text
new developer onboarding
```

and invalid for:

```text
latency analysis
security review
disaster recovery
billing correctness
data lineage audit
```

An organizational chart can be valid for:

```text
formal reporting structure
```

and invalid for:

```text
actual influence
knowledge transfer
incident response
political resistance
budget control
```

Therefore every map should declare:

```text
use-context U
horizon H
projection π
resolution ε
threshold θ_U
constraint regime K
```

In compressed form:

> Map validity is not absolute; it is typed adequacy for use.

---

# 6. Core Type Declarations

A structural map language should begin with a small set of declarations.

## 6.1 Distinction

```text
Distinction D {
    name
    projection
    decoder
    threshold
    locality
    support
    failure_condition
}
```

A distinction is not merely a named difference.

It must be recoverable enough to matter for a declared use.

Compressed form:

> A distinction is a recoverable difference that can constrain navigation, prediction, or action.

---

## 6.2 Object

```text
Object O {
    identity_cluster: C_O
    projection: π
    decoder: Δ
    support_graph: Supp_O
    constraint_regime: K_O
    horizon: H
    threshold: θ_U
    persistence_rule
    failure_modes
}
```

An object is not treated as a bare static thing.

It is a cluster of recoverable identity-relevant distinctions preserved or regenerated above threshold.

Compressed form:

> Objecthood is typed recoverable coherence, not untyped static presence.

---

## 6.3 Boundary

```text
Boundary B {
    separates: [Region_A, Region_B]
    transfer_rule
    filtering_rule
    breach_condition
    support
    horizon
    failure_modes
}
```

A boundary is not merely an edge.

It is a regime that controls transfer, recognition, access, or separation.

Compressed form:

> A boundary is a transfer regime, not just a line.

---

## 6.4 Flow

```text
Flow F {
    carrier
    source
    sink_or_cycle
    channel
    rate_or_capacity
    conversion_rules
    boundary_crossings
    support
    interruption_failure
}
```

A flow may carry:

```text
matter
energy
information
money
attention
labor
legitimacy
materials
signals
```

But the local implementation must be specified.

Compressed form:

> Flow is typed throughput through constrained channels.

---

## 6.5 Support

```text
Support S {
    supports: target
    support_type
    availability_condition
    substitution_options
    degradation_mode
    removal_effect
    horizon
}
```

Supports are often invisible while functioning.

Counterfactual removal reveals whether a support matters.

Compressed form:

> Support is what must remain for another distinction to remain recoverable or executable.

---

## 6.6 Constraint

```text
Constraint K {
    applies_to
    restricts
    admissible_variation
    violation_condition
    enforcement_or_realization
    validity_boundary
}
```

Constraint restricts possible transformations.

It may be physical, chemical, biological, computational, legal, economic, institutional, or social.

Compressed form:

> Constraint turns possibility into structured reachability.

---

## 6.7 Transition

```text
Transition T {
    from_state
    to_state
    preconditions
    postconditions
    required_supports
    consumed_resources
    emitted_traces
    failure_modes
}
```

A map with states but no transitions is a catalog.

A map with typed transitions becomes operational.

Compressed form:

> A transition is a constrained change between recoverable states.

---

## 6.8 Failure

```text
Failure F {
    target
    threshold_crossed
    lost_distinction
    lost_support
    lost_transition
    detection_path
    recovery_path
    severity
    horizon
}
```

Failure is not mere change.

Failure is change that crosses a threshold for a declared use-context.

Compressed form:

> Failure is loss of required recoverability, executability, or identity below threshold.

---

## 6.9 Recognition

```text
Recognition R {
    recognizer
    target_distinction
    decoder
    input_path
    action_difference
    error_model
    support
}
```

Recognition matters whenever a distinction must be recovered by an agent, institution, sensor, process, or model.

Compressed form:

> A distinction becomes operational when recognition changes downstream action.

---

## 6.10 Cross-Layer Invariant

```text
Invariant I {
    role
    layers
    implementations_by_layer
    preserved_consequences
    broken_consequences
    validity_boundary
    counterfactual_tests
}
```

A cross-layer invariant is not sameness of substance.

It is preservation of structural role across implementation regimes.

Compressed form:

> The invariant is the role; the implementation is the local substrate realizing it.

---

# 7. Diagnostics

The compiler/linter should produce diagnostics.

Diagnostics are not merely errors.

They can include:

```text
errors
warnings
hints
proof obligations
missing declarations
scope violations
projection mismatches
capacity violations
unsupported claims
unresolved supports
unmarked failure modes
```

## 7.1 Error: Missing Use-Context

```text
ERROR: Map declares stability but no use-context U.
```

Explanation:

```text
Stability cannot be evaluated without knowing what distinctions matter.
```

Compressed form:

> Untyped stability is invalid.

---

## 7.2 Error: Flow Without Carrier

```text
ERROR: Flow F declares transfer but no carrier.
```

Explanation:

```text
The map says something flows but does not say what is transported or how it is recoverable.
```

Compressed form:

> No carrier, no typed flow.

---

## 7.3 Error: Boundary Without Transfer Rule

```text
ERROR: Boundary B separates regions but declares no transfer semantics.
```

Explanation:

```text
A boundary must specify what is blocked, allowed, filtered, transformed, recognized, or breached.
```

Compressed form:

> A line without transfer semantics is not yet a boundary.

---

## 7.4 Error: Capacity Violation

```text
ERROR: Station S has max_simultaneous_trains = 3, but Schedule declares 50 simultaneous stop events.
```

Explanation:

```text
The map violates declared static capacity constraints.
```

Compressed form:

> Declared occupancy exceeds structural capacity.

---

## 7.5 Warning: Cross-Layer Analogy Without Consequence Mapping

```text
WARNING: Flow analogy between blood, money, and data lacks preserved consequence mapping.
```

Explanation:

```text
The same word appears across layers, but the map does not show which consequences transfer.
```

Compressed form:

> Same vocabulary is not structural equivalence.

---

## 7.6 Warning: Persistent Object Without Regeneration or Storage

```text
WARNING: Object O is declared persistent across H, but no storage or regeneration mechanism is specified.
```

Explanation:

```text
Persistence requires preserved or recreated identity-relevant distinctions.
```

Compressed form:

> Persistence requires support across delay or degradation.

---

## 7.7 Warning: Proof Claim Without Decoder

```text
WARNING: Proof(O) declared without decoder, trace, measurement, recognition path, or support path.
```

Explanation:

```text
Operational proof requires recoverability by some process.
```

Compressed form:

> Assertion without recoverability is not operational proof.

---

## 7.8 Hint: Projection May Be Too Coarse

```text
HINT: Map is valid for route navigation but under-specified for scheduling.
```

Explanation:

```text
The declared projection omits capacity distinctions required by the stronger use-context.
```

Compressed form:

> Strengthen the projection or weaken the use-context.

---

# 8. Static Checks

Static checks operate before dynamic simulation.

They ask whether the map is structurally coherent.

Examples:

```text
Are all objects typed by identity-relevant distinctions?
Are all stability claims indexed by projection and horizon?
Are all flows supported by carriers and channels?
Are all boundaries equipped with transfer or filtering semantics?
Are all transitions compatible with constraints?
Are all capacities respected?
Are all persistence claims supported by storage or regeneration?
Are all cross-layer analogies consequence-preserving?
Are all failure modes tied to thresholds?
Are all recognitions tied to decoders and action differences?
```

These checks do not require full event dynamics.

They are closer to:

```text
syntax checking
type checking
constraint solving
schema validation
dependency analysis
capacity checking
well-formedness checking
```

In compressed form:

> Static checks ask whether the map can possibly support the use claimed for it.

---

# 9. Counterfactual Support Removal as a Lint Rule

Counterfactual support removal asks:

```text
Remove support X.
Does target distinction D remain recoverable, executable, or persistent above threshold?
```

If removal causes collapse:

```text
Φ_D(K \ X, U, H) < θ_U
```

then `X` is support-relevant.

If removal does not cause collapse because another support substitutes, the instance is replaceable.

But the support function may still be necessary.

Compiler/linter usage:

```text
For each persistent object O:
    identify support graph Supp_O
    remove each support candidate X
    classify X as required, substitutable, redundant, or irrelevant
```

Possible diagnostics:

```text
ERROR: Required support missing.
WARNING: Single point of support failure.
WARNING: Claimed independence contradicted by support removal.
HINT: Add substitution path for support resilience.
```

In compressed form:

> Survival after support removal proves replaceability, not independence.

---

# 10. Type Adequacy Rather Than Maximal Detail

The compiler/linter should not force maps to include every possible detail.

That would destroy usability.

Instead, it should enforce:

```text
typed adequacy for declared use
```

A route map may omit platform capacity if:

```text
U = passenger route navigation
```

A scheduling map may not omit platform capacity if:

```text
U = operational scheduling
```

A legal map may omit molecular composition of documents.

A materials preservation map may not.

A high-level software architecture map may omit thread scheduling.

A performance debugging map may not.

A biological lineage map may omit individual ion flows.

A membrane transport model may not.

In compressed form:

> Detail is required exactly where omission changes consequence for the declared use.

---

# 11. Projection Mismatch

Projection mismatch occurs when a map valid under one projection is used under another.

Examples:

```text
visual stability used as chemical stability
legal existence used as operational capacity
file path existence used as content recoverability
organization chart used as real influence map
train route map used as schedule feasibility map
API diagram used as security boundary proof
```

Diagnostic:

```text
WARNING: Projection mismatch. Declared map projection π_route does not support requested use-context U_schedule.
```

Repair options:

```text
weaken use-context
strengthen projection
add missing distinctions
add support graph
add capacity model
add failure modes
```

In compressed form:

> Many false maps are true maps used under the wrong projection.

---

# 12. Cross-Layer Transfer Rules

A cross-layer transfer is valid only when consequence-bearing structure is preserved.

Bad transfer:

```text
Cells have membranes.
APIs are boundaries.
Therefore APIs are like cells in all important ways.
```

Typed transfer:

```text
Boundary-like role is preserved where both cell membranes and APIs:
    separate inside/outside regimes
    regulate transfer
    define admissible interaction
    fail under breach
    support local organization
```

Invalid extension:

```text
Cell membranes self-repair biologically.
Therefore APIs self-repair.
```

unless a repair mechanism is declared:

```text
monitoring
rollback
schema validation
version negotiation
operator intervention
self-healing orchestration
```

Compiler/linter diagnostic:

```text
WARNING: Invariant role transferred beyond declared implementation support.
```

In compressed form:

> Transfer the role only where local implementations preserve mapped consequences.

---

# 13. Minimal Formal Schema

A structural map may be represented as:

```text
M = (D, R, T, K, Π, Δ, Supp, F, U, H, θ)
```

where:

```text
D      = distinctions
R      = relations
T      = transitions
K      = constraints
Π      = projections
Δ      = decoders or recognition procedures
Supp   = support graph
F      = failure conditions
U      = use-context
H      = horizon
θ      = adequacy thresholds
```

A map is statically adequate when:

```text
Adequate_static(M; U, H) ⇔
    WellTyped(M)
    ∧ ProjectionAdequate(M, U)
    ∧ ConstraintConsistent(M)
    ∧ SupportClosed(M, U, H)
    ∧ CapacitySafe(M, U, H)
    ∧ FailureTyped(M, U)
    ∧ CrossLayerClaimsBounded(M)
```

A stronger operational adequacy condition adds transition validity:

```text
Adequate_operational(M; U, H) ⇔
    Adequate_static(M; U, H)
    ∧ ∀ T_i ∈ T:
        Preconditions(T_i) satisfiable
        ∧ Postconditions(T_i) typed
        ∧ RequiredSupports(T_i) available
        ∧ ConstraintViolations(T_i) = ∅
```

Dynamic adequacy would add simulation, stochasticity, feedback, and time-dependent perturbation.

```text
Adequate_dynamic(M; U, H) ⇔
    Adequate_operational(M; U, H)
    ∧ DynamicsModelDeclared(M)
    ∧ SimulationOrAnalysisSupports(U, H, θ)
```

In compressed form:

> Static adequacy checks structure; operational adequacy checks transitions; dynamic adequacy checks behavior over time.

---

# 14. Example: File Object

Surface map:

```text
File F exists.
```

Compiler response:

```text
WARNING: Object existence claim is under-typed.
```

Typed map:

```text
Object File_F {
    identity_cluster: content_bytes
    projection: SHA-256 hash
    decoder: filesystem_reader + hash_algorithm
    support_graph: storage_medium + filesystem + permissions + power + OS
    horizon: audit_period
    threshold: exact_hash_match
    failure_modes: unreadable, hash_mismatch, decoder_missing, permission_denied
}
```

Now the claim becomes:

```text
File F remains content-stable under SHA-256 projection across audit_period.
```

Diagnostics can now be meaningful:

```text
WARNING: Decoder dependency not archived.
WARNING: Storage medium is single point of failure.
ERROR: Claimed content verification impossible without hash algorithm.
```

Compressed form:

> File staticity becomes recoverable content equivalence under a declared projection and support graph.

---

# 15. Example: Institution

Surface map:

```text
Institution I still exists.
```

Compiler response:

```text
WARNING: Institutional objecthood claim lacks recognition, role, and regeneration paths.
```

Typed map:

```text
Institution I {
    identity_cluster:
        legal_name
        registry_entry
        authority_roles
        records
        procedures
        recognized_membership
        asset_control
    recognition_paths:
        courts
        regulators
        counterparties
        internal participants
    support_graph:
        records
        trained people
        funding
        communication channels
        enforcement mechanisms
    regeneration:
        hiring
        training
        procedure execution
        record maintenance
        norm reproduction
    horizon: fiscal_year
    threshold: can execute authorized functions
    failure_modes:
        loss_of_recognition
        record_destruction
        role_vacancy
        funding_collapse
        authority_dispute
}
```

The map can now distinguish:

```text
legal shell persists
operational institution persists
recognition persists
regeneration persists
```

Compressed form:

> Institutional existence is typed by recognition, execution, support, and regeneration.

---

# 16. Example: Software Architecture

Surface map:

```text
Service A talks to Service B.
```

Compiler response:

```text
WARNING: Coupling claim lacks protocol, boundary, failure, and support semantics.
```

Typed map:

```text
ServiceCoupling A_to_B {
    source: Service_A
    target: Service_B
    protocol: HTTP
    boundary: API_B
    authentication: required
    data_schema: Schema_X
    timeout: 2s
    retry_policy: bounded
    support:
        network
        service_discovery
        credentials
        schema_registry
        observability
    failure_modes:
        timeout
        auth_failure
        schema_mismatch
        dependency_unavailable
        partial_response
}
```

Now the compiler can check:

```text
Does A have credentials?
Does B expose API_B?
Does Schema_X match both sides?
Is retry policy bounded?
Is there observability for failure detection?
```

Compressed form:

> Architecture diagrams become stronger when relation labels are replaced by typed coupling declarations.

---

# 17. Example: Cross-Layer Boundary

Candidate invariant:

```text
Boundary
```

Typed invariant:

```text
Invariant Boundary {
    role:
        separates regimes
        regulates transfer
        supports local organization
        defines breach/failure condition

    implementations:
        biology: cell membrane
        software: API boundary
        security: firewall
        law: jurisdiction
        organization: role boundary
        infrastructure: station gate

    preserved_consequences:
        inside/outside distinction
        admissible transfer
        failure under breach
        support for local identity

    validity_boundary:
        valid only where local implementation actually regulates transfer
}
```

Compiler warning:

```text
WARNING: Boundary analogy extended to visual edge with no transfer rule.
```

Compressed form:

> Boundary is transferable only where separation and transfer regulation are preserved.

---

# 18. Failure Taxonomy

A structural map compiler/linter should classify failures.

## 18.1 Under-Typed Claim

```text
The map declares a structural role without required fields.
```

Example:

```text
Object O exists.
```

but no identity cluster, projection, decoder, support, horizon, or threshold is declared.

---

## 18.2 Projection Failure

```text
The map is used under a projection it does not support.
```

Example:

```text
A route map is used as a scheduling map.
```

---

## 18.3 Capacity Failure

```text
Declared transitions exceed structural capacities.
```

Example:

```text
50 simultaneous train stops at a 3-platform station.
```

---

## 18.4 Support Failure

```text
Required supports are missing, circular, unavailable, or below threshold.
```

Example:

```text
A file is declared recoverable but no decoder remains.
```

---

## 18.5 Recognition Failure

```text
A distinction exists in storage but no process can recover it and act on it.
```

Example:

```text
An archived protocol has documents but no compatible implementers.
```

---

## 18.6 Regeneration Failure

```text
Stored traces persist but no active process recreates the operational distinction.
```

Example:

```text
An institution has records but no trained role-bearers.
```

---

## 18.7 Cross-Layer Overreach

```text
A role is transferred beyond its validity boundary.
```

Example:

```text
Calling both money and blood flows, then importing biological self-repair into economics without a mapped mechanism.
```

---

## 18.8 Dynamic Blindness

```text
The map passes static checks but fails under time-dependent behavior.
```

Example:

```text
Station capacity is sufficient on paper, but delays cascade because dwell-time variance is ignored.
```

This is not necessarily a static compiler error.

It marks the boundary where dynamic modeling becomes necessary.

Compressed form:

> Static validation is necessary but not sufficient for dynamic reliability.

---

# 19. The Development Target

A first implementation does not need to solve everything.

A minimal repo could begin with:

```text
schema definitions
map declaration format
type checker
static lint rules
diagnostic messages
example maps
counterfactual support removal checks
cross-layer invariant templates
```

Possible repository structure:

```text
structural-map-compiler/
    README.md
    docs/
        vision.md
        type-system.md
        diagnostics.md
        examples.md
    schemas/
        map.schema.json
        object.schema.json
        flow.schema.json
        boundary.schema.json
        support.schema.json
        invariant.schema.json
    rules/
        required-fields.md
        projection-adequacy.md
        capacity-checks.md
        support-closure.md
        cross-layer-transfer.md
    examples/
        train-map.route.md
        train-map.schedule.md
        file-object.md
        institution.md
        software-architecture.md
        boundary-invariant.md
    src/
        parser/
        checker/
        diagnostics/
        cli/
```

A minimal command-line interface might look like:

```text
structmap check examples/train-map.schedule.md
```

Example output:

```text
ERROR SMC-CAP-001: Station S capacity exceeded.
    max_simultaneous_trains: 3
    declared_simultaneous_trains: 50

WARNING SMC-PROJ-002: Map projection route_connectivity is insufficient for use_context operational_scheduling.

HINT SMC-SUPP-004: Add platform_capacity, track_topology, dwell_constraints, or weaken use_context.
```

Compressed form:

> The first useful version can be a schema plus diagnostics engine, not a full simulator.

---

# 20. Design Principles

## 20.1 Do Not Punish Abstraction

A map may omit details when omission does not change adequacy for the declared use.

Compressed form:

> Abstraction is valid when consequences are preserved.

---

## 20.2 Make Use-Context Explicit

Every map should declare what it is for.

Compressed form:

> No use-context, no adequacy judgment.

---

## 20.3 Separate Role from Implementation

A role may recur across layers, but each layer implements it differently.

Compressed form:

> Same role does not mean same mechanism.

---

## 20.4 Prefer Typed Claims Over Essentialist Claims

Replace:

```text
X exists.
X is static.
X is the same.
X is a boundary.
X is a flow.
```

with:

```text
X is recoverable under projection π by decoder Δ across horizon H for use-context U above threshold θ.
```

Compressed form:

> Untyped object language should compile into typed recoverability language.

---

## 20.5 Validate by Consequence

A distinction matters if collapsing it changes:

```text
reachability
transition
cost
failure
support
boundary
recognition
regeneration
prediction
intervention
```

Compressed form:

> Preserve distinctions that change what can happen or be done.

---

## 20.6 Treat Failure as a First-Class Type

Failure should not be an afterthought.

Every map should say what breaks, how it is detected, and what support is lost.

Compressed form:

> A map that cannot describe failure cannot guide repair.

---

## 20.7 Mark Validity Boundaries

Every abstraction should know where it stops working.

Compressed form:

> Mature maps declare their own invalidity conditions.

---

# 21. Open Research Questions

The framework raises unresolved questions.

```text
What is the minimal useful set of structural types?
Which types are primitive and which are derived?
Can support closure be checked generically?
How should thresholds be represented?
How can projection adequacy be inferred or only declared?
Can cross-layer transfer be partially automated?
What is the right balance between formal schemas and human-readable maps?
How can the system avoid becoming too heavy for practical use?
How can maps degrade gracefully when under-specified?
How can diagnostics teach better map-making rather than merely reject maps?
```

Compressed form:

> The project is not to finish ontology, but to build better instruments for structural abstraction.

---

# 22. Minimal README Version

```text
Structural Map Compiler / Linter

A typed framework for building structural maps that are adequate for declared use-contexts.

The system checks whether objects, boundaries, flows, supports, constraints, transitions, failures, and cross-layer analogies are sufficiently declared to preserve operational consequences.

It does not try to model everything.

It checks whether the map includes the distinctions that matter for the declared projection, horizon, and use.

Core idea:

    A map is valid when omitted distinctions do not change the operational outcome for the declared use-context.

First target:

    schema + linter + diagnostics for structural maps

Later targets:

    operational transition models
    support-removal analysis
    capacity checks
    cross-layer invariant testing
    optional dynamic simulation hooks
```

Compressed form:

> A compiler/linter for structural maps checks typed adequacy before simulation, intervention, or real-world use.

---

# 23. Final Summary

This framework proposes a new kind of tool:

```text
A compiler/linter for structural maps.
```

It is not a total theory of reality.

It is not a full simulator.

It is not merely a diagramming tool.

It is a typed environment for declaring and checking consequence-bearing abstractions.

It asks:

```text
What is being mapped?
For what use?
Across what horizon?
Under which projection?
With which thresholds?
Which distinctions matter?
Which transitions are admissible?
Which supports keep the distinctions recoverable?
Which boundaries regulate transfer?
Which flows sustain the system?
Which failures cross operational thresholds?
Which analogies preserve consequences across layers?
```

The compiler/linter should reject or warn about maps that are:

```text
under-typed
projection-mismatched
capacity-violating
support-incomplete
failure-blind
cross-layer-overextended
dynamically overclaimed
```

It should not punish abstraction.

It should punish abstraction that silently breaks the declared use.

In final compressed form:

> A structural map compiler/linter is a static-checking system for typed abstractions: it verifies that a map preserves the distinctions required for its declared use-context, horizon, projection, and operational threshold, while marking the boundary where deeper operational or dynamic modeling becomes necessary.
