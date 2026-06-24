# Edge-Generating Capability Graphs

## A Standalone Framework for Reachability, Environmental Affordances, Skill Acquisition, and Transfer

---

# Status

This document extends the idea that:

```text
Generality emerges from accumulated capability.
```

It adds a further claim:

```text
Capability is not only a property of an agent.

Capability emerges from the interaction between:

agent
+
environment
+
infrastructure
+
tools
+
resources
+
permissions
+
learned abstractions
```

The central observation is:

```text
A system becomes more capable not merely by adding nodes,

but by generating new possible edges.
```

An edge is a transition:

```text
from one state

to another state
```

For example:

```text
standing
↓
walking
```

or:

```text
road access
+
car
+
license
+
fuel
↓
reachable destination
```

The deeper question is therefore:

```text
What makes a new transition possible?
```

---

# Abstract

Many accounts of intelligence, planning, and capability assume that the world is already given as a graph.

The task is then imagined as:

```text
current state
↓
search graph
↓
optimal path
```

But real systems usually face a prior problem.

They must determine:

```text
which edges can exist at all
```

before they can search for the best route.

A bicycle cannot cross a river without support.

A car cannot drive to Antarctica without ships, aircraft, roads, ice-rated vehicles, preparation, and survival infrastructure.

A child cannot read a book before acquiring visual distinctions, letters, words, grammar, concepts, and background models.

A society cannot build aircraft before metallurgy, engines, fuel systems, measurement standards, factories, trained workers, regulation, and navigation systems exist.

This suggests that intelligence is not only route-finding.

It is also:

```text
edge prediction

edge construction

edge validation

edge transfer
```

In this view, learning is not primarily the acquisition of labels.

Learning is the acquisition of:

```text
distinctions

regularities

constraints

invariants

abstractions
```

These structures allow an agent to recognize what can vary, what cannot vary, what is possible, what is impossible, and what can be transferred to new situations.

---

# 0. The Route Planner Assumption

Many systems are imagined as route planners.

The assumed sequence is:

```text
graph exists
↓
agent searches graph
↓
agent finds path
```

This works when the graph is already stabilized.

Examples include:

```text
roads

rail networks

flight routes

file systems

web links
```

But many real problems do not begin with a complete graph.

They begin with uncertainty about the graph itself.

The question is not only:

```text
What path should I take?
```

The prior question is:

```text
What transitions are physically, socially, legally, cognitively, and materially possible?
```

---

# 1. Edge Possibility Comes Before Edge Optimization

Before optimizing a transition, one must know whether the transition exists.

Google Maps does not ask:

```text
What is the fastest bicycle route across the ocean?
```

because the transition is not valid under normal bicycle assumptions.

The correct sequence is:

```text
possible edge?
↓
valid edge?
↓
safe edge?
↓
costed edge?
↓
optimized edge?
```

Optimization is late.

Possibility is early.

---

# 2. Terrain Determines Candidate Edges

Terrain is not passive background.

Terrain determines which transitions are even candidates.

Examples:

```text
road
    supports car, truck, bicycle, walking

rail
    supports train

river
    supports boat, bridge, ferry, swimming under limited conditions

airspace
    supports aircraft

snow and ice
    supports skis, snowmobiles, specialized vehicles

mountain
    supports climbing, tunneling, roads, cable systems
```

A terrain model restricts edge generation.

It says:

```text
these transitions are plausible

these transitions require support

these transitions are invalid
```

---

# 3. Infrastructure Converts Terrain Into Reachability

Terrain alone does not create reachability.

A river is not automatically crossable.

A mountain is not automatically traversable.

A desert is not automatically survivable.

Infrastructure creates new edges.

Examples:

```text
river
+
bridge
↓
walkable / drivable crossing
```

```text
ocean
+
port
+
ship
+
navigation
↓
maritime route
```

```text
airspace
+
airport
+
aircraft
+
air traffic control
↓
flight route
```

```text
cold environment
+
shelter
+
clothing
+
fuel
+
food
↓
survivable expedition
```

Infrastructure is an edge-generating layer.

It turns impossible or high-cost transitions into usable transitions.

---

# 4. Carriers And Agents Must Match The Edge

An edge is not valid in isolation.

It is valid for a particular carrier.

Examples:

```text
sidewalk
    valid for pedestrian
    invalid for truck
```

```text
highway
    valid for car
    invalid for pedestrian
```

```text
bike lane
    valid for bicycle
    usually invalid for aircraft
```

```text
runway
    valid for aircraft
    invalid as ordinary road infrastructure
```

The world does not contain a single reachability graph.

It contains many overlapping reachability graphs:

```text
pedestrian graph

bicycle graph

car graph

truck graph

train graph

ship graph

aircraft graph
```

Each graph is determined by:

```text
terrain
+
infrastructure
+
carrier
+
rules
+
conditions
```

---

# 5. Capability Is Relational

Capability is often described as if it belongs only to the agent.

For example:

```text
this person can drive
```

But driving requires more than a person.

It requires:

```text
vehicle

road

fuel or energy

legal permission

traffic rules

situational awareness

motor control
```

So the more precise statement is:

```text
this person can drive
under certain environmental,
technical,
legal,
and physical conditions
```

Capability is relational.

It is not merely:

```text
agent property
```

It is:

```text
agent-environment-system property
```

---

# 6. The RimWorld-Like State Description

A useful capability system begins with a state description.

Not only:

```text
agent wants goal
```

but:

```text
agent state

environment state

resource state

infrastructure state

knowledge state

permission state

risk state
```

A colony simulation makes this explicit.

For example:

```text
Goal:
    build hospital

State:
    5 people
    cold climate
    limited medicine
    no electricity
    no sterile room
    basic construction skill
    nearby steel
    no trained doctor
```

The system does not merely find a path.

It exposes missing edges:

```text
need electricity

need sterile room

need trained medical worker

need medicine supply

need temperature control

need food and rest for workers
```

The goal becomes reachable only after missing capabilities are acquired or substituted.

---

# 7. Edge Generation Is Constraint-Sensitive

Edges are not generated arbitrarily.

They are constrained by:

```text
physics

biology

material properties

time

energy

information

law

social trust

coordination

risk
```

A proposed edge must answer:

```text
Is it physically possible?

Is it biologically possible?

Is the required tool available?

Is the required resource available?

Is the required permission available?

Is the agent trained?

Is the environment suitable?

Is the risk acceptable?
```

Only then does the edge become navigable.

---

# 8. The Edge-Generating Mechanism

An edge-generating mechanism is anything that makes a new transition possible.

Examples:

```text
learning a skill

building infrastructure

acquiring a tool

obtaining permission

discovering an invariant

forming an abstraction

coordinating with others

changing the environment

creating a standard

improving measurement
```

Each mechanism expands reachability.

For example:

```text
learn to read
↓
books become navigable
```

```text
build bridge
↓
river crossing becomes navigable
```

```text
obtain medical license
↓
clinical interventions become legally reachable
```

```text
learn conservation of energy
↓
many physical systems become predictable
```

```text
create shipping container standard
↓
global logistics becomes more composable
```

The important claim is:

```text
Generality grows through edge-generation.
```

A system becomes more general when more classes of valid transitions become available.

---

# 9. Nodes Are States; Edges Are Transformations

A capability graph can be described minimally as:

```text
nodes = states

edges = transformations
```

Examples:

```text
raw food
↓
cooked food
```

```text
unread text
↓
understood text
```

```text
untrained person
↓
licensed driver
```

```text
isolated village
↓
connected village
```

```text
unknown pattern
↓
recognized invariant
```

Some edges are direct physical actions.

Some edges are cognitive.

Some edges are social.

Some edges are institutional.

Some edges are infrastructural.

---

# 10. Capability Primitives May Be Bounded

At first, human capability seems unbounded.

There are many jobs, languages, tools, domains, certifications, institutions, and resources.

But the lower-level capability basis may be much smaller.

Examples:

```text
can perceive signal S

can distinguish category A from B

can move object of mass X

can apply force F

can communicate in language L at proficiency P

can operate tool class T

can reason over domain D

can coordinate N people

can access resource R

can act under permission P
```

These are parameterized primitives.

They are not infinite labels.

Many surface capabilities may be compositions of a smaller set of primitives.

---

# 11. Human Biology Provides A Natural Base Layer

Human capability graphs can begin with the human organism.

The base layer includes:

```text
vision

hearing

touch

balance

proprioception

locomotion

grip

force application

attention

memory

language learning

social signaling
```

These can be measured or bounded.

Examples:

```text
hearing range

visual acuity

field of view

reaction time

maximum grip strength

walking endurance

working memory capacity
```

Disabilities can be represented as altered capability profiles, not as exceptions outside the model.

For example:

```text
blindness
↓
visual edges unavailable or altered
↓
other sensory, social, technological, or infrastructural edges may compensate
```

The graph does not require an idealized human.

It can represent actual agents.

---

# 12. Certifications Are Social Capability Markers

Many societies already use standardized capability markers.

Examples:

```text
driving license

motorcycle class

pilot rating

medical license

welding certification

language level

degree

security clearance

forklift certification
```

These are not the capability itself.

They are social claims that certain transitions are permitted or reliable.

For example:

```text
A2 motorcycle license
```

means approximately:

```text
this person is legally allowed
to operate a certain class of motorcycle
under specified conditions
```

A certification is therefore an institutional edge-enabler.

It can create reachability even when the underlying physical skill already exists.

---

# 13. Personal, Delegated, And Collective Capability

An individual does not possess all capabilities.

There are at least three distinct forms:

```text
possessed capability
    I can do it myself

accessible capability
    I can obtain it through others

known capability
    I know it exists
```

For example:

```text
I can ask a pilot to fly me

≠

I can fly a plane
```

The destination may become reachable through delegation.

But the skill is not personally possessed.

This produces layered capability graphs:

```text
individual capability graph

social capability graph

organizational capability graph

civilizational capability graph
```

Civilization can do many things almost no individual can do.

Examples:

```text
manufacture microchips

operate global shipping

launch satellites

produce vaccines

maintain electrical grids
```

These are distributed capabilities.

They exist across people, tools, institutions, standards, and infrastructure.

---

# 14. Social Networks Are Crude Capability Maps

Ordinary social networks answer:

```text
Who do you know?
```

Professional networks answer:

```text
What skills do people claim to have?
```

A capability graph would ask:

```text
Given my current position,
what outcomes are reachable
through my possessed and delegated capabilities?
```

This is not simply social media.

It is closer to:

```text
Google Maps for capability space
```

where:

```text
people are nodes

skills are edge-enablers

trust relationships are roads

institutions are infrastructure

money is fuel

permissions are gates
```

The system would expose missing paths.

For example:

```text
Goal:
    build medical device

Reachability gaps:
    biomedical engineer
    regulatory expert
    manufacturing partner
    clinical advisor
    capital
    testing facility
    distribution channel
```

---

# 15. Learning Is Not Label Acquisition

A label is useful.

But the label is not the main thing learned.

For example:

```text
sphere
```

is not merely a word.

It points to distinctions and regularities:

```text
roundness

rotation

rollability

symmetry

lack of corners
```

Similarly:

```text
cube
```

points to:

```text
flat faces

edges

corners

stackability

orientation
```

The label compresses the structure.

The useful learning is the structure.

---

# 16. People Learn Distinctions

A distinction separates what would otherwise be confused.

Examples:

```text
letter A vs letter B

6 vs 9

sphere vs cube

living vs nonliving

solid vs liquid

safe vs dangerous

legal vs illegal

possible vs impossible
```

A learned distinction creates new navigability.

Before the distinction:

```text
many cases blur together
```

After the distinction:

```text
new paths become visible
```

For example:

```text
recognize poison vs food
↓
new survival behavior becomes possible
```

```text
recognize symptom pattern
↓
medical diagnosis becomes possible
```

```text
recognize grammatical subject and object
↓
sentence interpretation becomes possible
```

---

# 17. People Learn Regularities

A regularity is a recurring pattern.

Examples:

```text
objects fall when unsupported

fire burns

water flows downhill

people respond to incentives

practice improves performance

traffic slows during congestion
```

Regularities are predictive.

They allow an agent to anticipate outcomes before acting.

A regularity becomes a candidate edge rule:

```text
if condition C holds
then transition T is likely
```

Not all regularities are absolute.

Some are probabilistic.

But even probabilistic regularities improve navigation.

---

# 18. People Learn Constraints

A constraint restricts what can happen.

Examples:

```text
solid objects usually cannot pass through each other

humans require oxygen

money cannot be spent twice

a bridge has load limits

a license may be legally required

time cannot be reused
```

Constraints define invalid edges.

They say:

```text
this transition is not allowed

this transition exceeds capacity

this transition requires an intermediate step
```

A good world model is not only a list of possible actions.

It is also a list of impossible, unsafe, illegal, or unstable actions.

---

# 19. People Learn Invariants

An invariant is something that remains stable across transformations.

Examples:

```text
quantity conserved

identity preserved

symmetry maintained

causal structure unchanged

meaning preserved under paraphrase
```

Physics is rich in invariants:

```text
energy conservation

momentum conservation

charge conservation

mass-energy accounting
```

Language also contains invariants:

```text
The dog chased the cat.

The cat was chased by the dog.
```

The surface form changes.

The underlying relation remains.

Recognizing invariants is one of the strongest forms of learning because it supports transfer.

---

# 20. Transfer Is Edge Reuse Across Domains

Transfer occurs when a learned structure works somewhere new.

For example:

```text
learn balance on bicycle
↓
partially transfer to motorcycle
```

```text
learn conservation in mechanics
↓
recognize conservation in electricity
```

```text
learn graph traversal in maps
↓
apply graph traversal to social networks
```

```text
learn subject-object structure in language
↓
apply relation structure to databases
```

Transfer is powerful because it allows one learned edge pattern to generate many new edges.

This is why transfer is an edge-generating mechanism.

It does not merely solve one problem.

It expands the class of problems that become navigable.

---

# 21. Fine-Tuning Stabilizes Capability

Learning a distinction once is not enough.

A system must refine it.

For humans:

```text
exposure
↓
rough distinction
↓
practice
↓
feedback
↓
stable skill
↓
transfer
```

For AI systems:

```text
pretraining
↓
base representation
↓
fine-tuning
↓
task competence
↓
evaluation
↓
generalization
```

Fine-tuning strengthens local regions of capability space.

It can make a capability more reliable, precise, and usable.

But fine-tuning is not the same as transfer.

A system can become excellent in one region while failing in adjacent regions.

---

# 22. Progressive Capability Testing

Capability can be tested hierarchically.

Not only:

```text
Can the agent answer the final question?
```

but:

```text
Where does reachability fail?
```

A diagnostic hierarchy might be:

```text
0. Sensory discrimination
1. Recognition
2. Distinctions
3. Regularities
4. Constraints
5. Invariants
6. Abstractions
7. Transfer
8. Edge generation
```

This tests from low-level perception to high-level capability expansion.

---

# 23. Reading As Progressive Capability

Reading illustrates the hierarchy.

```text
visual marks
↓
letters
↓
phonemes
↓
words
↓
sentences
↓
meaning
↓
concepts
↓
abstractions
↓
transfer
```

Failure can occur at many levels.

Examples:

```text
cannot distinguish letters

can distinguish letters but cannot decode words

can decode words but not parse sentences

can parse sentences but not infer meaning

can infer meaning but not transfer concepts
```

A single exam score hides these differences.

A capability graph exposes them.

---

# 24. Physics As Progressive Capability

Physics also illustrates the hierarchy.

```text
recognize object
↓
recognize motion
↓
recognize force
↓
recognize regularity
↓
recognize constraint
↓
recognize invariant
↓
transfer invariant across systems
```

A novice sees:

```text
inclined plane

pendulum

spring

collision
```

as separate topics.

An expert sees:

```text
energy

momentum

constraints

symmetry
```

The expert does not need thousands of unrelated representations.

A small number of invariants compress many cases.

---

# 25. Abstractions Compress Capability Space

A good abstraction reduces the number of edges that must be learned separately.

For example:

```text
road network
```

compresses millions of possible vehicle positions into a manageable graph.

```text
conservation law
```

compresses many physical situations into a stable rule.

```text
object
```

compresses sensory variation into a persistent entity.

```text
function
```

compresses many input-output relations into one structure.

Abstractions are useful when they preserve what matters and discard what does not.

Bad abstractions hide important constraints.

Good abstractions expose navigable structure.

---

# 26. The Capability Ontology

A practical capability graph needs shared descriptions.

Like maps require:

```text
coordinates

distance

time

speed

roads

restrictions
```

capability maps require standardized dimensions.

Possible dimensions include:

```text
agent

goal

state

action

tool

resource

permission

terrain

infrastructure

risk

knowledge

skill

trust

cost

time
```

These are not arbitrary magic numbers.

They are attempts to synchronize descriptions of reality.

The analogy is not perfect.

But the principle is similar:

```text
navigation requires shared units
```

Without shared units, reachability cannot be compared, communicated, or computed.

---

# 27. Maximum Granularity Is Not Always Useful

A graph can be too coarse.

For example:

```text
engineer

doctor

manager
```

These hide too much.

A graph can also be too fine.

For example:

```text
finger angle

muscle activation

millisecond motor command
```

These are usually too detailed for planning.

The useful level is often intermediate.

Google Maps does not model every steering adjustment.

It models roads, turns, speeds, and restrictions.

A capability graph should similarly support expansion on demand.

```text
coarse when sufficient

fine when necessary
```

---

# 28. Expansion On Demand

A capability can remain compressed until a failure or planning need requires detail.

For example:

```text
can drive
```

may expand into:

```text
has license

can operate vehicle

can perceive road signs

can follow traffic rules

has access to vehicle

has fuel or energy

road route exists

conditions are safe
```

Similarly:

```text
can perform surgery
```

may expand into:

```text
medical knowledge

sterile environment

licensed surgeon

anesthesia

instruments

assistants

patient consent

postoperative care
```

The graph should not always operate at maximum granularity.

It should expand where reachability is uncertain.

---

# 29. Generality Is Broad Edge Availability

A system appears general when many regions become reachable.

But this does not require a mystical universal skill.

It may require:

```text
many primitives

reliable composition

strong abstraction

constraint recognition

invariant transfer

edge-generation mechanisms
```

Generality is then:

```text
broad, reliable, transferable reachability
```

not:

```text
one magic solver
```

---

# 30. Intelligence As Reachability Expansion

The traditional question is:

```text
How do we build a generally intelligent system?
```

A reachability-oriented question is:

```text
How does a system acquire, validate, compose, and transfer edges?
```

The system must learn:

```text
what exists

what differs

what repeats

what is constrained

what is invariant

what can be transformed

what must be built first

what can be delegated

what can transfer
```

In this view, intelligence is not only choosing actions.

It is the continuous construction of a more navigable world model.

---

# Final Compression

A route planner asks:

```text
What is the best path through the graph?
```

A capability planner asks:

```text
Does the edge exist?
```

A learning system asks:

```text
What distinction, constraint, or invariant would make new edges visible?
```

A social system asks:

```text
Who or what can provide the missing edge?
```

An infrastructure system asks:

```text
What must be built so the edge becomes usable?
```

A civilization asks:

```text
How do we make whole classes of previously impossible transitions routine?
```

The proposal is:

```text
terrain shapes possible edges

infrastructure creates usable edges

carriers determine valid edges

tools amplify edges

resources fuel edges

permissions unlock edges

skills stabilize edges

distinctions reveal edges

constraints invalidate edges

invariants compress edges

abstractions transfer edges

social systems delegate edges

standards synchronize edges

fine-tuning strengthens edges

edge-generation expands reachability
```

And therefore:

> Generality is not merely more knowledge.

> Generality is the ability to generate, validate, compose, and transfer edges across capability space.

> A powerful system does not only navigate known roads.

> It learns what roads can exist, what roads must be built, which vehicles can traverse them, and which abstractions make many roads visible at once.

> Intelligence may be the progressive expansion of reachable transformations under real constraints.
