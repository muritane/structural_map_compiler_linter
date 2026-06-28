# World, Belief, Capability, and Constructive Graphs

## A Standalone Framework for Multi-Frequency Context, Agent-Specific Admissibility, Graph Projection, Reorganization Operators, and Planning Across Slow and Fast Maps

---

# Status

This document extends the family of frameworks concerned with:

```text
Constraints Before Objects

Capability Cartography

Resolution Before Navigation

State-Space Before Comparison

Admissibility Before Representation

Transition Richness Before Information

Causal Organization Before Representation

Reorganization Capacity Before Optimization

Transition Organization Before Objects

Constraint Transforms Before Navigation
```

Its purpose is to sharpen a further mistake:

```text
confusing the world graph
with the agent's admissible graph
```

or:

```text
confusing infrastructure that exists
with transitions available to this agent,
from this state,
under this context,
with these capabilities,
at this time
```

The previous correction was:

```text
do not plan over imaginable actions

construct the admissible transition graph first
```

This document adds:

```text
the admissible graph is not generated from one context alone

it is projected from persistent world organization,
updated belief,
agent capability,
local observation,
and constructive graph-rewriting capacity
```

The central claim is:

```text
planning occurs over a projected graph,
not directly over the world graph
```

The stronger claim is:

```text
advanced agents do not merely navigate projected graphs;

they also modify the world,
their beliefs,
their capabilities,
and the projection rules that determine future admissibility
```

Or shorter:

```text
intelligence is not only route selection

it is multi-layer graph maintenance, projection, navigation, and reorganization
```

---

# Abstract

A weak planner asks:

```text
Where am I?

Where is the goal?

Which route is shortest?
```

A stronger planner asks:

```text
What persistent world graph is assumed?

What parts of that graph are currently believed?

Which updates have arrived?

Which local observations revise the context?

Which transport, software, legal, institutional, or physical modes can this agent use?

Which edges exist in the world but are not available to this agent?

Which edges are available only after a capability transition?

Which missing edges can be constructed?

Which graph changes are slow, event-based, periodic, or locally sensed?

Which goal lies inside the current projected cone?

If not, which admitted reorganization transition changes future reachability?
```

Google Maps is a useful example.

It has a large transportation graph.

It combines:

```text
road topology

traffic estimates

closures

transport modes

current user location

target destination
```

But it mostly assumes:

```text
the infrastructure graph already exists

the user selects or supplies a transport mode

the agent navigates itself

the map is not substantially rewritten by the user
```

This makes Google Maps primarily a graph consumer.

It routes over a changing but mostly pre-existing graph.

A more general planner must also represent:

```text
buy bicycle

rent car

obtain permit

charge battery

repair road

clear debris

install dependency

build bridge

open institution

create protocol
```

These are not ordinary navigation transitions.

They are capability-changing or graph-constructing transitions.

Thus the useful object is not only:

```text
map
```

and not only:

```text
agent state
```

but:

```text
persistent world graph
+
belief graph
+
capability graph
+
constructive graph
+
local context stream
+
projection operator
```

Planning becomes:

```text
maintain slow maps

incorporate events

refresh local context

project world organization through agent constraints

navigate if the goal is reachable

reorganize if the goal is not yet reachable
```

---

# 0. The World-Graph Mistake

The mistake is:

```text
because an edge exists in the world,
it is available to the agent
```

Examples:

```text
a road exists,
but the agent has no car

rail exists,
but the agent has no ticket

bike lanes exist,
but the agent has no bicycle

an API exists,
but the agent lacks credentials

a legal procedure exists,
but the agent lacks standing

a warehouse contains material,
but the robot lacks authorization

a route exists,
but battery is insufficient

a proof method exists,
but the system lacks a formal model
```

The correction is:

```text
world existence ≠ agent admissibility
```

A world graph contains edges that exist.

An admissible agent graph contains edges the agent can execute.

The second is a projection of the first through context and capability.

---

# 1. Google Maps as a Partial Model

Google Maps already contains several important components.

It has:

```text
slow topology
  roads, rails, paths, waterways

medium updates
  traffic, closures, schedules

local state
  current user position

goal state
  destination

mode constraint
  walking, cycling, driving, transit
```

It then routes through an admissible subset of the transport graph.

For example:

```text
car mode
  admits roads
  rejects footpaths
  respects traffic direction

bike mode
  admits bike paths
  may reject highways

walking mode
  admits sidewalks and paths
  may ignore some vehicle constraints

transit mode
  admits timetable-dependent edges
```

So Google Maps already performs a projection:

```text
world transport graph
+
mode
+
current position
+
traffic context
↓
route graph
```

But the projection is limited.

It typically treats transport mode as an input, not as a state to be achieved.

It asks:

```text
Given that you are walking, biking, driving, or using transit,
which route should you take?
```

A more general planner asks:

```text
Which mode should become available?

Can the agent transition into that mode?

What must be done before that mode is admissible?
```

---

# 2. Transport Mode as Capability State

In ordinary route planning, mode is often selected externally.

```text
mode = walking
mode = biking
mode = driving
mode = train
```

But in general planning, mode is not merely a parameter.

It is part of the agent's capability state.

Examples:

```text
walk
  currently available

bike
  available only if bicycle is possessed, rented, or purchased

car
  available only if vehicle, license, fuel, road access, and authority exist

train
  available only if station access, timetable, ticket, and schedule fit

flight
  available only if airport, passport, ticket, security, and timing align
```

Thus:

```text
transport mode = capability projection condition
```

The graph should not simply contain:

```text
walk edge
bike edge
car edge
train edge
```

It should contain:

```text
capability transitions
that make edge classes admissible
```

For example:

```text
walk to bike station
↓
rent bicycle
↓
bicycle edges become admitted
```

or:

```text
walk to station
↓
buy ticket
↓
wait until departure
↓
train edge becomes admitted
```

The mode transition itself has preconditions.

---

# 3. Four Graphs

A useful decomposition is:

```text
G_world
G_belief
G_capability
G_constructive
```

These are not four unrelated graphs.

They are four views of transition organization.

---

## 3.1 World Graph

The world graph contains structures that exist or are taken to exist in the environment.

Examples:

```text
roads
bridges
warehouses
servers
legal offices
institutions
rail lines
ports
energy grids
software repositories
communication networks
```

It changes, but often slowly.

A road network does not usually change every control cycle.

A legal system does not usually change every second.

An API schema changes more often than geography, but less often than local sensor readings.

The world graph is the relatively persistent landscape.

---

## 3.2 Belief Graph

The belief graph is the agent's current estimate of the world graph.

It may be wrong, stale, incomplete, or inconsistent.

Examples:

```text
road believed open
but actually closed

inventory believed available
but actually depleted

server believed healthy
but actually down

permission believed valid
but actually revoked

warehouse believed accessible
but door is locked
```

The agent never plans directly from the world.

It plans from belief.

Thus:

```text
world graph
  what exists

belief graph
  what the agent currently models as existing
```

Planning error can therefore arise from:

```text
bad route search
```

or:

```text
bad belief graph
```

The second is often more fundamental.

---

## 3.3 Capability Graph

The capability graph represents what the agent can currently exploit.

It includes:

```text
skills
licenses
tools
energy
money
credentials
authority
body state
vehicle state
software dependencies
institutional standing
```

The same world graph yields different admissible graphs for different agents.

Example:

```text
World graph:
  road exists

Alice:
  no car
  no license
  can walk

Bob:
  car available
  license valid
  fuel sufficient
```

Alice's projected graph admits walking edges.

Bob's projected graph admits driving edges.

Same world.

Different agent graph.

Thus:

```text
capability is not a property of the world alone

capability is a relation between agent and world
```

---

## 3.4 Constructive Graph

The constructive graph contains transitions that modify future graphs.

It includes transitions that change:

```text
the world graph

the belief graph

the capability graph

the projection relation
```

Examples:

```text
repair road
  modifies world graph

build bridge
  modifies world graph

survey unknown area
  modifies belief graph

check inventory
  modifies belief graph

charge battery
  modifies capability graph

rent bicycle
  modifies capability graph

obtain license
  modifies capability graph

write adapter library
  modifies software capability graph

change law
  modifies institutional graph

establish protocol
  modifies projection rules for future coordination
```

The constructive graph is missing from many routing systems.

A route planner asks:

```text
which existing edge should be traversed?
```

A constructive planner also asks:

```text
which future edge should be made to exist?

which missing capability should be acquired?

which uncertainty should be resolved?

which projection should be changed?
```

---

# 4. Projection Before Navigation

Let:

```text
G_world(t)
```

be the persistent world organization.

Let:

```text
B_t
```

be the belief state.

Let:

```text
A_t
```

be the agent capability state.

Let:

```text
L_t
```

be the local observed context.

Let:

```text
Π
```

be the projection operator.

Then the agent's admissible graph is:

```text
G_agent(t) = Π(G_world(t), B_t, A_t, L_t)
```

This means:

```text
do not search the world graph directly

project it through belief, capability, and local context

then search the projected graph
```

Projection removes or modifies edges based on:

```text
physical constraints

local obstacles

resource limits

permissions

uncertainty

latency

mode capability

safety margins

protocol compatibility
```

An edge can exist in the world graph but fail to appear in the agent graph.

An edge can appear in the belief graph but fail in execution because the belief graph was wrong.

An edge can be physically possible but excluded because it is unauthorized or too slow.

Thus admissibility is projected, not inherited automatically.

---

# 5. Global Context and Local Context

Context is not one thing.

It has layers with different update frequencies.

A useful ordering is:

```text
very slow context
  physics
  geography
  constitutional rules
  major infrastructure

slow context
  road topology
  legal procedures
  API schemas
  train schedules
  organizational charts

medium context
  weather
  construction
  congestion
  inventory
  service availability

fast context
  current position
  battery
  sensor readings
  local obstacles
  local human behavior
  live system load

ultra-fast context
  control feedback
  actuator response
  wheel slip
  packet timing
  collision proximity
```

Planning should not refresh all layers at the same rate.

It should update each layer according to its dynamics and risk.

---

# 6. Event-Based Updates for Slow Maps

Slow maps should usually be updated by events or subscriptions.

Examples:

```text
road closure notice

new train schedule published

API version deprecated

legal rule changed

bridge reopened

inventory restocked

permission revoked

schema migrated
```

Polling slow maps at high frequency is wasteful.

But relying only on events is unsafe because events can be:

```text
missed

delayed

duplicated

wrong

out of order

ambiguous
```

Thus the stronger pattern is:

```text
event-driven updates
+
periodic reconciliation
+
local validation when relevant
```

The global map should be subscription-updated where possible.

The local context should be sensed repeatedly.

The belief state should record staleness.

---

# 7. Periodic Reconciliation

Even slow maps need periodic refresh.

Not because they change quickly.

Because the agent's belief about them can drift from reality.

Periodic reconciliation detects:

```text
missed events

stale assumptions

corrupted state

unreported local changes

dependency changes

outdated permissions

invalid cached topology
```

The update policy should depend on:

```text
change frequency

cost of refresh

cost of being wrong

latency tolerance

availability of event streams

trustworthiness of sources
```

For example:

```text
road topology
  event-based updates plus occasional full map refresh

traffic
  frequent streaming updates

vehicle position
  continuous sensing

battery state
  continuous sensing

legal authorization
  event-based updates plus validation at use time

financial balance
  event-based updates plus transaction-time verification
```

---

# 8. Staleness as a Constraint

Every context layer should carry metadata.

```text
last_updated

source

version

confidence

valid_until

scope

dependency

uncertainty
```

A stale edge is not necessarily false.

But it is weaker.

The planner should distinguish:

```text
fresh and validated

old but stable

old and volatile

unverified

contradicted

unknown
```

Staleness can shrink the admissible graph.

For example:

```text
inventory record says carbon fiber exists

record age = 3 days

warehouse turnover = high

local confirmation absent
```

Then the transition:

```text
manufacture using carbon fiber now
```

should not be admitted merely because the stale global map says material exists.

Instead the planner may admit:

```text
verify inventory
```

or:

```text
navigate to warehouse and inspect
```

Information-gathering is a constructive transition on the belief graph.

---

# 9. Local Observation as Fast Projection Correction

Local context can override slow maps.

Examples:

```text
global map says road open
local observation sees barrier

inventory database says shelf stocked
robot observes empty shelf

API registry says service healthy
client receives repeated timeout

legal database says authorization valid
official denies access
```

Thus projection should not be:

```text
use global map
then route
```

but:

```text
use global map
combine with belief state
correct with local observations
then project admissibility
```

The local layer often has priority for nearby action.

But local observation can also be noisy.

So the system must represent uncertainty rather than simply overwrite the map.

---

# 10. Navigation Transitions

A navigation transition traverses an edge in the currently projected graph.

Examples:

```text
drive on road

walk down hallway

call available API

execute authorized procedure

move robot arm within control envelope

compile valid program

transfer money through existing payment rail
```

Navigation assumes the relevant edge is already admitted.

It asks:

```text
which existing edge should be traversed next?
```

Navigation updates state, but it does not primarily rewrite the graph.

---

# 11. Constructive Transitions

A constructive transition changes future reachability.

It may modify:

```text
world
belief
capability
projection
```

Examples:

```text
clear debris
  world graph modification

build bridge
  world graph modification

query map service
  belief graph modification

inspect shelf
  belief graph modification

charge battery
  capability graph modification

rent bicycle
  capability graph modification

obtain API key
  capability graph modification

standardize protocol
  projection-rule modification

create legal category
  institutional graph modification
```

Constructive transitions are still transitions.

They must themselves be admitted.

It is not enough to propose:

```text
build bridge
```

The planner must check:

```text
materials
labor
permission
engineering validity
funding
time
site access
maintenance
risk
```

Graph construction is not magic.

It is graph traversal whose effect is graph rewriting.

---

# 12. Capability Construction Versus World Construction

Not all reorganization changes the external world.

Some reorganization changes the agent's relation to the world.

Examples:

```text
charge battery
  world mostly unchanged
  agent mobility increases

rent bicycle
  world mostly unchanged
  bike edges become available

obtain credentials
  system mostly unchanged
  API edges become available

learn skill
  world mostly unchanged
  action classes become available
```

Other reorganization changes the world itself.

Examples:

```text
build bridge

repair road

install charging station

publish API endpoint

create court procedure
```

Thus separate:

```text
capability reorganization
```

from:

```text
world reorganization
```

Both change future admissibility.

But they operate on different graph layers.

---

# 13. Belief Construction

Some transitions are valuable because they improve the belief graph.

Examples:

```text
look around corner

query inventory

ask human operator

run diagnostic

ping server

survey terrain

read contract

measure latency
```

These do not necessarily change the world.

They change what the agent can safely project.

A belief-improving action may be the correct next transition even when it does not move physically toward the goal.

This matters when uncertainty itself blocks admissibility.

For example:

```text
unknown whether bridge is intact
```

The planner may not admit:

```text
cross bridge with heavy truck
```

But it may admit:

```text
inspect bridge
```

or:

```text
send drone to survey bridge
```

Belief construction is often the missing middle between navigation and world construction.

---

# 14. Projection Rules

Projection rules determine how world structure becomes agent admissibility.

Examples:

```text
road edge + car capability + legal permission + fuel + no closure
  → driving edge admitted

rail edge + station access + ticket + timetable + time budget
  → train edge admitted

API endpoint + credentials + schema compatibility + network availability
  → API call admitted

legal procedure + standing + jurisdiction + deadline
  → filing edge admitted

material inventory + access permission + transport capability
  → manufacturing edge admitted
```

Projection rules may themselves be changed.

Examples:

```text
new regulation changes who can use an institutional edge

new adapter library changes software compatibility

new treaty changes border crossing admissibility

new authentication protocol changes access rules
```

Thus the system contains not only graphs, but rules for projecting graphs.

---

# 15. Missing Local Context

Sometimes the global map is available, but local context is missing.

Examples:

```text
map knows road exists
but not whether the gate is open

system knows API exists
but not whether credentials are valid

inventory says item exists
but not whether shelf is physically accessible

law says procedure exists
but not whether office is accepting filings today
```

The planner should not pretend the missing local context is favorable.

It should classify the edge as:

```text
world-known
but locally unvalidated
```

Possible responses:

```text
route around uncertainty

seek information

send scout

validate at use time

reserve fallback

reduce speed

increase safety margin
```

Missing local context does not always delete an edge.

But it should weaken the guarantee attached to that edge.

---

# 16. Multi-Agent Projection

Different users of the same map see different admissible graphs.

Google Maps users share much of the world graph.

But each user has:

```text
current position

destination

transport mode

mobility constraints

time budget

preferences

permissions

local observations
```

Thus each user receives a different projection.

```text
shared world graph
↓
user-specific projection
↓
user-specific route
```

A truck, cyclist, pedestrian, wheelchair user, and emergency vehicle do not share the same admissible graph.

The map may be common.

The admissible transition field is not.

---

# 17. Shared Slow Context, Private Fast Context

Many systems contain both shared and private context.

Shared context:

```text
road network
published schedule
public weather
known closures
legal rules
API documentation
```

Private context:

```text
current location
battery level
vehicle condition
personal credentials
risk tolerance
local observation
private goal
```

A routing system can provide shared slow context.

The agent must combine it with private fast context.

Thus:

```text
global platform provides background graph

agent supplies current projection constraints
```

This division explains why Google Maps does not need to know everything.

It provides a slowly changing landscape and some live shared updates.

The user or device supplies current position, goal, mode, and local execution.

---

# 18. Event Streams as Context Integration

A context layer can be updated by:

```text
periodic polling

event subscription

local sensing

manual declaration

third-party validation

execution feedback
```

Different layers prefer different mechanisms.

```text
slow stable layer
  subscription plus periodic reconciliation

medium volatile layer
  streaming updates or frequent polling

fast local layer
  direct sensing and feedback

critical edge
  validation at time of use
```

The planner should track not only state, but also how the state was obtained.

A subscribed official closure notice is different from an old cached map.

A local camera observation is different from a crowd-sourced report.

A formally verified invariant is different from a hopeful assumption.

---

# 19. Receding Projection Planning

The planning loop becomes:

```text
1. Maintain persistent world graph.

2. Receive slow-map events.

3. Periodically reconcile slow maps.

4. Update belief graph.

5. Sense local context.

6. Update agent capability state.

7. Project world/belief graph through capability and local context.

8. Compute time-bounded cone.

9. If goal intersects cone, choose navigation transition.

10. If goal does not intersect cone, choose constructive transition.

11. Execute.

12. Use execution feedback to update belief, capability, and world model.

13. Repeat.
```

This is not only receding-horizon control.

It is receding-horizon graph projection and graph reorganization.

---

# 20. Robotics Already Contains the Loop

Robotics already uses many parts of this structure.

A robot commonly performs:

```text
sensor fusion

state estimation

map update

reachable-set computation

motion planning

control execution

feedback correction
```

So the contribution here is not that robots should observe, estimate, plan, and act.

That already exists.

The contribution is abstraction and generalization.

The same structure applies beyond robotics:

```text
software systems

legal systems

institutions

logistics

markets

scientific research

civilizational infrastructure

AI agents using tools
```

Robotics is an existence proof.

It shows the loop is practical in physical control.

The framework asks how far the same pattern generalizes.

---

# 21. The Use of the Framework

The framework is useful because it gives a shared vocabulary for systems that are usually described separately.

It unifies:

```text
motion planning

compiler validation

legal admissibility

institutional procedure

logistics

software dependency management

infrastructure construction

scientific instrumentation

organizational capability
```

under the same sequence:

```text
world organization
↓
belief update
↓
capability projection
↓
admissible graph
↓
navigation or construction
```

The value is not replacing domain algorithms.

The value is diagnosing planning failures across domains.

Examples:

```text
wrong world graph

stale belief graph

missing capability edge

invalid projection rule

unmodeled local context

absent constructive transition

optimization over inadmissible actions

navigation attempted where construction was required
```

These categories are often more precise than saying:

```text
the plan failed
```

---

# 22. Failure Taxonomy

Planning failures can be separated.

```text
world error
  the represented infrastructure did not actually exist

belief error
  the agent's map was stale or wrong

capability error
  the edge existed but the agent could not use it

projection error
  the system incorrectly admitted or rejected an edge

local-context error
  missing immediate facts invalidated a transition

latency error
  the transition existed but not within the required horizon

validation error
  imported assumptions were not checked

constructive omission
  the planner searched for routes but failed to consider graph-changing actions

optimization error
  the planner chose poorly among admitted edges

execution error
  the transition was valid but execution failed
```

This taxonomy is one practical use of the framework.

It helps identify where intelligence failed.

---

# 23. Civilizational Interpretation

Civilization does not merely find routes through a given graph.

It constructs new graphs.

Examples:

```text
roads
bridges
ports
schools
courts
markets
standards
protocols
scientific instruments
communication networks
energy grids
```

Each construction changes future admissibility.

A bridge is not merely an object.

It is a new transition class.

A school is not merely a building.

It is a capability-construction institution.

A court is not merely a place.

It is a validation and authorization layer.

A protocol is not merely a rule.

It is a projection rule that makes coordination edges reliable.

Thus:

```text
civilizational progress = accumulated improvement of world, belief, capability, and constructive graphs
```

---

# 24. AI Agents and Candidate-Edge Overload

Modern AI systems reduce proposal latency.

They can quickly generate:

```text
code
plans
hypotheses
routes
designs
arguments
legal drafts
business strategies
```

But proposal is not admissibility.

The bottleneck shifts to:

```text
validation
execution
integration
permission
safety
maintenance
institutional acceptance
```

Thus AI agents especially need graph projection.

They should not ask only:

```text
what plan can be generated?
```

They should ask:

```text
which generated edges are admitted?

which require validation?

which require capability construction?

which rewrite future graphs?

which damage future reachability?
```

Without this, AI produces candidate-edge overload.

The planner drowns in proposals that are not executable, safe, authorized, or maintainable.

---

# 25. Abstraction Layers and Imported Guarantees

Every projected edge imports guarantees from lower layers.

Examples:

```text
software call imports network, protocol, authentication, schema, and runtime guarantees

driving edge imports road geometry, vehicle operation, traffic law, friction, and perception guarantees

legal filing imports jurisdiction, procedure, identity, deadline, and authority guarantees

manufacturing edge imports material availability, tool calibration, design validity, and operator capability
```

A projected edge is therefore a compact claim:

```text
under these imported guarantees,
this transition is admitted
```

An abstraction leaks when imported guarantees fail.

The framework requires each edge to expose enough metadata to know what it depends on.

---

# 26. Edge Signature

A projected edge may be represented as:

```text
e = (
  source,
  target,
  mode,
  layer,
  τ,
  κ,
  assumptions,
  invariants,
  validation,
  capability_requirements,
  locality_requirements,
  freshness,
  confidence,
  ΔG_world,
  ΔG_belief,
  ΔG_capability,
  ΔΠ
)
```

where:

```text
source
  starting organization or context

target
  resulting organization or context

mode
  navigation, belief-construction, capability-construction, world-construction, projection-rule change

layer
  physical, software, institutional, logistical, social, etc.

τ
  latency or duration

κ
  cost or resource burden

assumptions
  environmental or model conditions

invariants
  properties preserved, transferred, consumed, or violated

validation
  checks required before execution

capability_requirements
  agent-side conditions required for use

locality_requirements
  spatial, temporal, or organizational nearness constraints

freshness
  age and validity of supporting context

confidence
  uncertainty attached to the edge

ΔG_world
  change to world graph

ΔG_belief
  change to belief graph

ΔG_capability
  change to capability graph

ΔΠ
  change to projection rules
```

Edges are not bare arrows.

They are structured admissibility claims with graph effects.

---

# 27. Algorithmic Compression

A compact algorithm:

```text
1. Maintain G_world as a persistent slow map.

2. Receive event updates for slow and medium context.

3. Periodically reconcile persistent maps against authoritative sources.

4. Maintain B_t as a belief graph with freshness and confidence metadata.

5. Observe L_t as fast local context.

6. Maintain A_t as the agent capability graph.

7. Project:

   G_agent(t) = Π(G_world, B_t, A_t, L_t)

8. Compute the time-bounded cone K_t(Δt).

9. If the goal intersects K_t(Δt), choose a navigation transition.

10. If not, search G_constructive for an admitted transition that improves future reachability.

11. Execute the transition.

12. Update world, belief, capability, and projection metadata from execution feedback.

13. Repeat.
```

This algorithm does not search all imaginable actions.

It repeatedly constructs the graph on which planning is meaningful.

---

# 28. Diagnostic Questions

For any planner, ask:

```text
What is the persistent world graph?

Which parts are slow, medium, fast, and ultra-fast?

Which updates arrive by event subscription?

Which updates require polling?

Which layers require periodic reconciliation?

What is the belief graph?

Which beliefs are stale?

Which local observations override the slow map?

What capabilities does the agent currently have?

Which world edges are unavailable because capability is missing?

Which capability transitions are admitted?

What projection rules convert world edges into agent edges?

Which projection rules are uncertain, outdated, or invalid?

What is the current admissible graph?

What is the current time-bounded cone?

Does the goal intersect the cone?

If not, is the missing step belief construction, capability construction, world construction, or projection-rule change?

Which constructive transitions are themselves admitted?

What future graph does each constructive transition produce?

What is the cost of acting on stale context?

What is the cost of refreshing context?

Where can imported guarantees fail?
```

These questions are stronger than:

```text
what route should I take?
```

because they first ask:

```text
which graph is this agent actually allowed to use?
```

---

# 29. Compression of the Framework

A weak route planner says:

```text
here is the map
choose a path
```

A stronger planner says:

```text
here is the world graph
project it through agent constraints
then choose a path
```

A stronger constructive planner says:

```text
if the projected graph does not contain a path,
choose an admitted graph-changing transition
```

A weak context model says:

```text
refresh the state
```

A stronger context model says:

```text
update slow maps by event,
reconcile them periodically,
sense fast local context continuously,
and attach staleness metadata to every imported guarantee
```

A weak capability model says:

```text
choose a mode
```

A stronger capability model says:

```text
mode is an agent state that can sometimes be acquired, rented, learned, authorized, charged, repaired, or lost
```

A weak civilization model says:

```text
civilization improves outcomes
```

A stronger civilization model says:

```text
civilization accumulates world graphs,
belief systems,
capability institutions,
and constructive operators
that expand future admissible cones
```

---

# 30. Final Compression

The central object is not the map.

The central object is:

```text
projected admissible transition organization
```

A world graph is:

```text
the relatively persistent structure of possible transitions in the environment
```

A belief graph is:

```text
the agent's current, possibly stale or uncertain estimate of the world graph
```

A capability graph is:

```text
the agent's current relation to the world,
including tools, resources, permissions, skills, and modes
```

A constructive graph is:

```text
the set of admitted transitions that can modify world, belief, capability, or projection rules
```

A projection operator is:

```text
the mechanism that converts world and belief structure
through agent capability and local context
into an admissible agent graph
```

A local context is:

```text
the fast-changing immediate situation that corrects or constrains slow maps
```

A slow map is:

```text
a persistent global structure best maintained by events, subscriptions, and periodic reconciliation
```

The main principle is:

```text
do not confuse the shared world graph
with the agent's current projected graph
```

The deeper principle is:

```text
intelligent planning is the maintenance, projection, traversal, and reorganization of transition graphs across multiple time scales
```

Or shorter:

```text
maps are shared,
admissibility is projected,
capability is agent-specific,
construction changes the future graph,
and planning begins only after these layers are distinguished
```
