# Capability Before Generality

## A Standalone Framework for Navigability, Reachability, Skill Acquisition, and the Growth of Capability Graphs

---

# Status

This document extends the Navigability Before Reachability framework.

The central observation is:

```text
Large systems rarely solve everything at once.

They become useful by acquiring navigable capabilities incrementally.
```

Examples include:

```text
humans

Google Maps

robotics systems

the Internet

scientific knowledge

organizations
```

The proposal is:

```text
Generality is not the starting point.

Generality emerges from accumulated capability.
```

---

# Abstract

Many discussions of intelligence assume a single leap:

```text
perception

↓

intelligence

↓

all possible skills
```

Yet successful systems rarely develop this way.

Humans learn:

```text
balance

walking

language

reading

driving

specialized professions
```

over years.

Google Maps began with:

```text
location

roads

routing
```

before adding:

```text
traffic

transit

cycling

ride sharing

EV routing
```

Robotic systems similarly acquire capability incrementally.

This suggests:

```text
intelligence may not be a single solution

but a growing graph of navigable capabilities
```

---

# 0. The Myth of the Single Solution

Many people imagine:

```text
camera

↓

AI

↓

human-level manipulation
```

or:

```text
world state

↓

planner

↓

optimal solution
```

This framing assumes that a sufficiently powerful system can directly solve arbitrary tasks.

In practice:

```text
state spaces explode

constraints multiply

uncertainty accumulates
```

The problem becomes intractable.

Successful systems therefore construct abstractions.

---

# 1. Goals Before Navigation

Navigation begins with a goal.

Google Maps requires:

```text
current location

destination
```

before planning can occur.

Similarly:

```text
robot

↓

goal state
```

is required before motion becomes meaningful.

Without goals:

```text
navigation is undefined
```

---

# 2. Agent Identity Determines Reachability

Reachability depends on the agent.

Consider:

```text
pedestrian

bicycle

car

truck

train
```

Each inhabits the same world.

Yet each experiences different reachability.

A sidewalk is reachable for:

```text
pedestrian
```

but not:

```text
truck
```

Likewise a robot holding a screwdriver possesses capabilities unavailable to an empty gripper.

Reachability depends on capability.

---

# 3. Reachability Precedes Optimization

Before choosing the best route:

```text
a route must exist
```

Google Maps first asks:

```text
Can the destination be reached?
```

Only afterward does it compare:

```text
time

distance

fuel

risk
```

The sequence is:

```text
reachability

↓

optimization
```

not the reverse.

---

# 4. Capability Graphs

A capability graph asks:

```text
What can be produced from here?
```

rather than:

```text
What is connected?
```

Examples:

```text
Cup

↓

Grasp

↓

Lift

↓

Move

↓

Place
```

or:

```text
Image

↓

Detection

↓

Pose Estimate

↓

Trajectory

↓

Action
```

Capability graphs describe construction pathways.

---

# 5. Humans Learn Capability Graphs

Human development appears incremental.

A child does not learn:

```text
walking

reading

driving

programming
```

simultaneously.

Instead:

```text
balance

↓

walking

↓

manipulation

↓

language

↓

reading

↓

higher abstractions
```

Each acquired skill expands future reachability.

---

# 6. Skill Acquisition Expands Reachability

A new skill creates:

```text
new nodes

new transitions

new destinations
```

within capability space.

Learning to ride a bicycle creates:

```text
new reachable locations
```

Learning mathematics creates:

```text
new reachable concepts
```

Learning surgery creates:

```text
new reachable interventions
```

Skills are navigational expansions.

---

# 7. Google Maps As Capability Growth

Google Maps did not begin as a complete system.

Initially:

```text
location

roads

routing
```

were sufficient.

Over time:

```text
traffic

public transit

cycling

walking

street view

ride sharing

EV routing
```

were added.

The system became useful before becoming comprehensive.

Capability accumulated incrementally.

---

# 8. Robotics Faces The Same Problem

General manipulation is often imagined as:

```text
all objects

all tools

all tasks

all environments
```

simultaneously.

This creates enormous search spaces.

Instead:

```text
reach

↓

grasp

↓

lift

↓

place

↓

tool use

↓

assembly
```

provides a practical progression.

Each skill becomes a reusable primitive.

---

# 9. Approximate Maps Are Usually Enough

Perfect maps are rarely required.

Google Maps does not maintain:

```text
every wheel position

every steering angle
```

A robot similarly need not model:

```text
every possible trajectory
```

The system requires:

```text
safe approximation

local verification

continuous refinement
```

High precision is only necessary near boundaries.

---

# 10. Hierarchies Of Navigation

Large systems solve problems through layered maps.

For a drone:

```text
Mission Goal

↓

Route Planner

↓

Waypoint Planner

↓

Trajectory Planner

↓

Controller

↓

Motors
```

Each layer reduces complexity.

Each layer exposes a more navigable abstraction.

---

# 11. Controllers As Navigational Layers

A controller hierarchy may be viewed as:

```text
goal navigation

↓

capability navigation

↓

trajectory navigation

↓

state stabilization
```

Rather than solving one impossible problem, the system solves many manageable problems.

This decomposition creates scalability.

---

# 12. The Importance Of Replanning

Navigation occurs within changing constraints.

Examples:

```text
traffic

weather

humans

moving obstacles

sensor uncertainty
```

Therefore:

```text
plan

↓

execute

↓

monitor

↓

replan
```

becomes a recurring cycle.

Navigation is continuous adaptation.

---

# 13. Why Generality Is Difficult

The challenge is not merely:

```text
number of states
```

The challenge is:

```text
number of useful abstractions
```

Roads provide natural abstractions for driving.

Manipulation lacks equally obvious abstractions.

The search for robotic intelligence may therefore be the search for navigable capability representations.

---

# 14. Generality As Emergent Reachability

Generality may not be a primitive.

Instead:

```text
skill

+

skill

+

skill

+

skill
```

eventually creates:

```text
broad reachability
```

A system appears general because many regions of capability space become connected.

---

# Final Compression

The traditional question is:

```text
How do we build general intelligence?
```

A navigability-oriented question is:

```text
How do capabilities accumulate?
```

The proposal is:

```text
goals create destinations

capabilities create roads

constraints shape navigation

skills expand reachability

hierarchies reduce complexity

replanning maintains validity

generality emerges from accumulated capability
```

And therefore:

> Humans do not learn everything at once.

> Robots will likely not learn everything at once.

> Large systems become powerful by growing navigable capability graphs.

> Intelligence may be the continuous expansion of reachable capability space.

> Generality may emerge from capability accumulation.

> Before asking how to solve everything, ask how new capabilities become reachable.
