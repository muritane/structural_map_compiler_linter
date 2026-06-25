# Constraints Before Objects

## A Standalone Framework for Invariants, Admissible Transitions, Propagation, Stable Frames, and Object Emergence

---

# Status

This document extends:

```text
Capability Cartography

Resolution Before Navigation

State-Space Before Comparison

Admissibility Before Representation
```

Its purpose is to prevent a deeper mistake:

```text
assuming that objects,
properties,
trajectories,
or meanings
are primary
```

The framework proposes:

```text
constraints precede objects

admissible transitions precede trajectories

stable frames precede useful descriptions

invariants precede names
```

A model may begin with objects.

Reality need not.

A map may contain labels.

The terrain contains constraints.

The task is not merely to identify what exists.

The task is to discover:

```text
what cannot happen

what remains invariant

what transitions are admitted

what patterns persist
```

---

# Abstract

Many representational systems begin with:

```text
object
property
relation
```

This is useful, but often misleading.

It encourages the assumption that reality is built from labeled things that possess attributes.

The alternative proposed here is:

```text
constraint
admissible transition
persistent region
stable pattern
object label
```

An object may be a useful summary.

But the deeper structure may be the set of constraints that permits the object to emerge, persist, interact, and disappear.

For example:

```text
electron
photon
planet
cell
human
word
object in an image
```

may all be understood as persistent patterns inside a larger landscape of admissible states and transitions.

The framework therefore distinguishes:

```text
representation
state
transition
constraint
invariant
stable frame
```

The central claim is:

```text
objects are often downstream summaries
of upstream admissibility structure
```

---

# 0. The Object-First Mistake

A common modeling pattern is:

```text
object
↓
properties
↓
relations
↓
behavior
```

Example:

```text
electron
  charge
  mass
  spin
```

or:

```text
human
  beliefs
  goals
  language
```

or:

```text
cube
  pixels
  color
  surface
```

This is not wrong.

But it may hide the dependency structure.

The object may not be primary.

The object may be a stable name for a region in a constraint landscape.

A stronger ordering is:

```text
constraints
↓
admissible transitions
↓
persistent regions
↓
object labels
```

The label comes late.

The constraint comes early.

---

# 1. Model Is Not Reality

A model does not bind reality.

Reality does not need to obey the model.

Instead:

```text
a useful model must obey reality
```

If the model admits arbitrary transitions, but reality does not, then the model is too permissive.

If the model allows:

```text
energy appearing without transfer

mass changing without exchange

signals arriving without propagation

state changes without admissible transitions
```

then the model may be syntactically expressive but ontologically weak.

The question is not:

```text
Can this be represented?
```

The question is:

```text
Does reality admit this transition?
```

---

# 2. Constraints Are Not Decorations

Constraints are often treated as secondary rules added after objects are defined.

This framework reverses that order.

Constraints may be more fundamental than objects.

For example, instead of:

```text
photon.speed = c
```

one may say:

```text
all admissible photon states in vacuum satisfy speed = c
```

Instead of:

```text
electron.charge = -1
```

one may say:

```text
electromagnetic and charge-conserving transitions
must resolve around this conserved quantity
```

Instead of:

```text
planet follows orbit
```

one may say:

```text
planetary motion remains inside a persistent region
of gravitationally admissible trajectories
```

The second form is more structural.

It describes what reality permits and forbids.

---

# 3. Invariants Are Stable Frames

A finite observer cannot track all change.

The observer therefore benefits from detecting what does not change.

This is analogous to robotics.

In a ROS or SLAM system, one may choose between frames:

```text
map
odom
base_link
camera
laser
```

No frame is absolutely privileged for every task.

But some frames are more stable for a given purpose.

A map frame is useful because it changes slowly.

A camera frame is useful for local perception.

A base frame is useful for control.

Likewise, in scientific modeling, invariants function like stable frames.

Examples:

```text
conserved charge
conserved momentum
conserved angular momentum
symmetries
speed limit c
```

These are not merely facts among facts.

They are anchors for inference.

A useful map is often built around what remains stable while everything else changes.

---

# 4. Change Is Cheap; Invariance Is Informative

One can build a model by tracking change:

```text
position changed
velocity changed
brightness changed
pixel changed
```

But change alone may not reveal structure.

A stronger question is:

```text
what survived the change?
```

Examples:

```text
A cube rotates,
but edge connectivity persists.

A sentence is spoken with different accents,
but the linguistic mapping persists.

A planet moves,
but certain orbital invariants persist.

A particle interacts,
but conserved quantities persist.
```

The invariant is often more informative than the changing surface.

Change explores the state-space.

Invariance reveals the state-space.

---

# 5. Admissible States Are Not Enough

A state-space by itself is incomplete.

One may list states:

```text
A
B
C
D
E
```

but still not know which transitions are possible.

The deeper structure may be:

```text
A → B
B → C
C → D
```

and not:

```text
A → E
B → E
D → A
```

The transition graph contains information that the state list does not.

Therefore:

```text
state admissibility
```

must be distinguished from:

```text
transition admissibility
```

A model that admits a state does not automatically admit a path to that state.

Imagining a destination does not imply reachability.

---

# 6. Valid Transition Does Not Mean External Permission

Reality does not contain an external validator.

There is no cosmic function:

```python
if transition_is_valid:
    allow()
else:
    reject()
```

A transition is admissible if it belongs to the structure reality actually instantiates.

It is not validated from outside.

It either occurs under the relevant constraints or it does not.

Thus:

```text
valid transition
```

means:

```text
a transition supported by the current structure,
constraints,
state,
and interaction conditions
```

The language of permission is metaphorical.

The structure is not metaphorical.

---

# 7. Propagation Before Change

Many state changes require something to propagate.

Examples:

```text
mass transfer
energy transfer
momentum transfer
signal propagation
chemical diffusion
sound waves
photons
```

If Earth's mass changes, one asks:

```text
what arrived?
what left?
what exchanged energy?
what exchanged momentum?
```

If a brain state changes after hearing a word, one asks:

```text
what acoustic pattern propagated?
what neural architecture received it?
what internal transition was admitted?
```

Change is not arbitrary.

A later state must be connected to the earlier state by admissible propagation or interaction.

This gives a principle:

```text
state change requires admissible connection
```

---

# 8. Receiving Structure Matters

A signal alone does not determine the outcome.

The receiving system matters.

Example:

```text
sound wave
+
English-speaking listener
→ meaningful linguistic transition
```

but:

```text
same sound wave
+
listener without the mapping
→ different transition
```

Similarly:

```text
neurotransmitter
+
receptor architecture
→ neural propagation
```

but:

```text
neurotransmitter
+
no appropriate receptor
→ no such propagation
```

The energy does not disappear.

It resolves through whatever transitions remain admissible:

```text
heat
chemical change
mechanical dissipation
other local effects
```

Therefore:

```text
incoming influence
+
receiving organization
→ admissible next state
```

The receiver is not passive.

It constrains what the signal can become.

---

# 9. Photons As Propagating Excitations

A photon is not usually a packet that gradually accumulates energy while traveling.

A photon is typically created with an energy determined by an admissible transition.

Example:

```text
excited atom
↓
lower-energy atom
+
photon
```

or:

```text
electron + positron
↓
photons
```

The photon propagates energy and momentum.

But the photon does not usually charge up in empty space.

The better question is:

```text
what transition admitted a photon as an output?
```

This replaces:

```text
where did the photon come from?
```

with:

```text
what coupled system changed state,
and what emitted excitation was admissible?
```

---

# 10. Photon Constraints

A photon in vacuum is not arbitrary.

It occupies a restricted motion class:

```text
rest mass = 0
speed = c
energy > 0
momentum > 0
direction exists
no rest frame
```

The statement:

```text
speed = c
```

is not merely a property.

It is a state-space restriction.

The photon does not occupy:

```text
0 ≤ v < c
```

It occupies:

```text
v = c
```

This is a boundary-like region.

The direction may change.

The local speed in vacuum remains c.

Gravity can alter the trajectory.

It does not make the photon into a slow massive object.

---

# 11. Photon Overlap And Weak Interaction Density

Photons can occupy the same quantum mode.

Many photons can stack into the same state in a way electrons cannot.

This is why coherent light, such as laser light, is possible.

Photon overlap does not imply strong photon-photon interaction.

Ordinary beams of light can cross without scattering significantly.

Thus:

```text
co-occupancy admissible
```

does not imply:

```text
strong mutual interaction
```

Photon-photon interaction is possible in high-energy quantum processes, but it is extremely weak under ordinary conditions.

This suggests a distinction:

```text
interaction admissibility
```

versus:

```text
interaction probability or strength
```

Something may be allowed but rare.

Something may be forbidden entirely.

Something may be abundant.

---

# 12. Interaction Density

Different materials feel different because interaction density differs.

Air:

```text
low density
many admissible rearrangements
weak resistance
```

Water:

```text
higher density
coupled molecular rearrangements
stronger resistance
```

Wall:

```text
very high electromagnetic interaction density
few admissible rearrangements
strong resistance
```

A hand cannot pass through a wall easily because the attempted transition is constrained by electromagnetic structure, exclusion structure, and material organization.

A neutrino may pass through the same wall because its admissible interaction channels with ordinary matter are sparse.

The wall did not change.

The interaction landscape changed with respect to the incoming system.

Thus:

```text
solidity
```

may be viewed as:

```text
high local interaction density
+
strong constraints on rearrangement
```

---

# 13. Gravity As Trajectory Constraint

Gravity is often described as:

```text
mass attracts mass
```

This is useful but incomplete.

Photons have zero rest mass yet are gravitationally lensed.

Modern physics suggests that gravity is related to energy, momentum, stress, pressure, and spacetime geometry, not merely rest mass.

From a constraint-centered view:

```text
gravity constrains admissible trajectories
```

An orbit is not a free choice.

It is a persistent solution inside a geometric constraint landscape.

A planet remains in orbit not because gravity is canceled.

It remains because its state evolves inside a region where forward motion and gravitational curvature continually resolve into a bound path.

A rocket can escape by entering a different region of the same state-space.

Thus:

```text
stable orbit
```

means:

```text
a persistent region under current constraints
```

not an absolute trap.

---

# 14. Trajectories Are Derived

A trajectory is a sequence:

```text
state(t0)
→ state(t1)
→ state(t2)
→ ...
```

It is not necessarily fundamental.

It may be a visible trace of deeper admissible transitions.

Instead of:

```text
object follows trajectory
```

one may say:

```text
constraints define admissible next states
and the resulting sequence appears as a trajectory
```

The object is not ignored.

But the object is no longer the deepest explanatory unit.

---

# 15. Stable And Unstable Are Region Descriptions

Stability should not be treated as an absolute property of a trajectory.

A region may be persistent under small perturbations.

Another region may be fragile.

A planet orbiting a star occupies a relatively thick family of nearby admissible trajectories.

A photon orbit near a black hole may occupy a thin, unstable boundary.

A tiny perturbation may lead to escape or capture.

Thus:

```text
stable
unstable
metastable
fragile
persistent
```

are descriptions of regions in state-space.

They are not magical properties attached to things.

---

# 16. Mass, Energy, Momentum

Mass, energy, and momentum should not be treated as arbitrary independent labels.

They are constrained coordinates.

A massive particle at rest still has energy.

A photon has energy and momentum despite zero rest mass.

Therefore:

```text
energy can exist without rest mass
```

but:

```text
rest mass does not appear without energy
```

This suggests that mass may be better understood as a marker of a motion class or admissible region rather than as an isolated substance.

For massive objects:

```text
0 ≤ v < c
```

For massless photons in vacuum:

```text
v = c
```

The distinction is structural.

---

# 17. Quantization Does Not Automatically Mean Finite Reality

Photons come in quanta.

For a given mode, energy is packetized.

But this does not automatically imply that all reality has a minimum resolution.

Photon energy depends on frequency.

Lower frequency means lower photon energy.

Current theory does not impose a known minimum nonzero photon energy.

Similarly, longer wavelength corresponds to smaller photon momentum.

Shorter wavelength corresponds to larger photon momentum.

This does not by itself prove that reality is discrete or continuous.

The deeper question is:

```text
can the state-space be subdivided forever?
```

or:

```text
does reality possess a fundamental resolution?
```

This remains open.

The framework should therefore distinguish:

```text
observed quantization
```

from:

```text
universal discreteness
```

---

# 18. Object Detection As Constraint Extraction

Computer vision illustrates the same inversion.

A naive object-first view says:

```text
image
↓
object pixels
↓
object identity
```

But effective perception often extracts:

```text
gradients
edges
corners
facets
junctions
motion boundaries
```

A cube need not be represented by every pixel.

The informative structure may be:

```text
edge connectivity
surface orientation
corner relations
viewpoint-invariant geometry
```

Deep learning systems often learn early filters resembling edges, gradients, textures, and contrasts because these features are useful constraints for downstream recognition.

The lesson is not that edges are metaphysically fundamental.

The lesson is:

```text
useful perception preserves task-relevant invariants
and discards irrelevant variation
```

This aligns with the broader framework.

Objects may be inferred from stable constraints rather than detected as raw pixel collections.

---

# 19. Language As Admissible Mapping

Speech is not magic.

It propagates through physical channels:

```text
vocal tract
↓
air pressure waves
↓
eardrum
↓
neural signals
↓
brain dynamics
↓
behavior
```

The sound wave itself is not the meaning.

Meaning appears when a receiving architecture has learned stable mappings:

```text
acoustic pattern
↓
phoneme
↓
word
↓
concept
↓
behavioral affordance
```

The same sound can produce different outcomes in different receivers.

Thus:

```text
meaning
```

is not merely in the signal.

It is in the admissible mapping between signal, receiver structure, context, and learned constraints.

This does not reduce meaning to physics alone.

It grounds meaning in layered admissibility.

---

# 20. Humans As Layered Constraint Participants

A human is not merely a physical object.

A human participates in many layers:

```text
physics
chemistry
cell biology
tissue dynamics
organs
nervous system
memory
language
social relations
institutions
technology
```

A Roomba analogy is limited but useful.

A robot has sensors, motors, battery, mapping, control, and task policies.

A human has vastly more layers and richer mappings.

But both are embedded control systems.

Neither floats outside reality.

A human is a persistent pattern maintained across many simultaneous constraint layers.

Higher layers do not freely violate lower layers.

They depend on them.

---

# 21. Embedded Observers And SLAM

An embedded observer does not have God's-eye access.

The observer is inside the structure it attempts to model.

This resembles SLAM:

```text
agent moves
↓
observes partial data
↓
extracts stable features
↓
builds map
↓
updates map with new evidence
```

The map is not the world.

The map is a constructed representation constrained by observations.

A good observer does not track everything.

It identifies stable frames, landmarks, invariants, and transition regularities.

Thus scientific modeling may be viewed as generalized SLAM:

```text
finite embedded observer
↓
partial observations
↓
invariant extraction
↓
constraint inference
↓
world model
```

---

# 22. World Building Workflow

For world building, simulation, or theory construction, begin with constraints.

Not:

```text
dragon
wizard
city
starship
```

but:

```text
what is conserved?

what propagates?

what cannot propagate?

what transitions are admissible?

what structures can persist?

what scales are bounded?

what interactions are dense or sparse?
```

Then ask what objects can emerge.

A dragon-like organism is not merely a named creature.

It is a candidate persistent structure.

The question is:

```text
under what constraints could such a structure exist?
```

Likewise:

```text
atomic bomb
black hole
city
cell
market
mind
```

are not just objects.

They are patterns admitted by deeper constraints.

---

# 23. Minimal Constraint Sets

A model should not simply accumulate constraints.

It should search for a minimal independent set.

If one constraint implies another, the implied one should not be treated as primitive.

Example:

```text
A → B
B → C
```

may imply:

```text
A → C
```

If so, the model should avoid treating all three as independent fundamentals.

The task is:

```text
extract invariants
identify admissible transitions
compress into minimal constraints
generate consequences
revise when evidence contradicts them
```

This protects the model from confusing derived regularities with foundational structure.

---

# 24. Revision Is In The Model, Not In Reality

When evidence changes, the model updates.

Reality does not update because the observer learned something.

The workflow is:

```text
observation
↓
candidate invariant
↓
candidate constraint
↓
model
↓
new observation
↓
model revision
```

The framework remains fallibilist.

It does not assume the observer has complete access.

It only insists that the observer should distinguish:

```text
what reality admits
```

from:

```text
what the current model represents
```

---

# 25. The General Dependency Inversion

The common ordering is:

```text
object
↓
properties
↓
relations
↓
behavior
```

The proposed ordering is:

```text
constraints
↓
admissible transitions
↓
persistent regions
↓
stable patterns
↓
object labels
```

This does not deny objects.

It relocates them.

Objects become summaries of constraint structure.

Properties become coordinates of admissible regions.

Relations become discovered transition possibilities.

Trajectories become sequences of admissible states.

Meanings become stable mappings across layered receivers.

Perception becomes invariant extraction.

Science becomes embedded cartography.

---

# 26. Practical Diagnostic Questions

For any proposed entity, relation, or phenomenon, ask:

```text
What remains invariant?

What changes?

What transitions are admitted?

What transitions are excluded?

What must propagate before change occurs?

What receiving structure is required?

What interaction channels exist?

What interaction channels are absent?

What region of state-space is persistent?

What neighboring states destabilize it?

Which constraints are primitive?

Which constraints are derived?
```

These questions are often more informative than:

```text
What is it?
```

The answer to "what is it" may only become clear after the admissibility structure is mapped.

---

# 27. Final Compression

A weak ontology asks:

```text
What objects exist?
```

A stronger ontology asks:

```text
What constraints admit persistent objects?
```

A weak model asks:

```text
What states can be represented?
```

A stronger model asks:

```text
Which transitions are admissible?
```

A weak perception system asks:

```text
Where are all the pixels?
```

A stronger perception system asks:

```text
Which gradients, edges, and invariants constrain the object hypothesis?
```

A weak world builder asks:

```text
What entities should exist?
```

A stronger world builder asks:

```text
What constraints would make those entities possible?
```

Therefore:

```text
invariants are stable frames

constraints precede objects

admissible transitions precede trajectories

propagation precedes nonlocal change

receiving architecture constrains signal meaning

interaction density explains apparent solidity

stable patterns are persistent regions

objects are summaries, not necessarily primitives
```

The central principle is:

```text
the map may begin with objects

but reality may be organized by constraints

and objects may be what constraints allow to persist
```
