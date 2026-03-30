# KR Artifact Registry Schema

## 1. Purpose

This document defines the schema and governing logic for an artifact registry in the future KR production project.

Its purpose is to provide a structured way to track the durable artifacts that the project creates and relies upon.

The artifact registry exists to answer questions such as:
- what durable artifacts currently exist?
- what kind of artifact is each one?
- where does each artifact live?
- what authority does it have?
- what aspect does it support?
- is it active, superseded, deprecated, or still only working material?
- what other artifacts depend on it?
- what artifacts are missing but expected?

The artifact registry is meant to improve:
- recoverability
- structural legibility
- authority clarity
- lifecycle discipline
- cross-session continuity

It is not a replacement for the artifacts themselves.
It is a structured index of the artifact system.

---

## 2. Core principle

As KR grows, it should not rely on human memory or ad hoc repo browsing to understand its strategic artifact landscape.

The project needs a durable inventory layer.

However, the artifact registry must remain:
- compact
- structured
- reference-oriented
- non-duplicative

It should not become:
- a second prose documentation system
- a substitute for reading the real artifacts
- a verbose catalog full of repeated content

The registry should answer:
- what exists
- what role it plays
- what state it is in
- where it lives
- why it matters

That is enough.

---

## 3. What counts as an artifact for registry purposes

The artifact registry should track artifacts that are sufficiently durable, important, or operationally relevant to matter for future work.

This includes:
- doctrine artifacts
- protocol artifacts
- architecture artifacts
- evaluation artifacts
- registries
- templates
- schemas
- execution-support artifacts
- selected working artifacts when they are important enough to track
- selected control-plane artifacts if the project chooses to include them explicitly

This usually excludes:
- casual notes
- ephemeral chat-only outputs
- transient generated files unless strategically important
- ordinary code files unless they are being tracked as part of a broader artifact system

The registry is for project artifacts, not for every file in the repo.

---

## 4. Design goals

The artifact registry should satisfy all of the following:

1. **Coverage of important artifacts**
   Significant strategic artifacts should be visible.

2. **Low duplication**
   The registry should not restate whole documents.

3. **Authority clarity**
   It should be easy to tell how much weight an artifact carries.

4. **Lifecycle clarity**
   It should be easy to see whether an artifact is active or obsolete.

5. **Aspect linkage**
   It should be easy to see what aspect an artifact belongs to or supports.

6. **Practical usability**
   Future workers should actually be able to use the registry as a navigation tool.

7. **Scalability**
   The registry should still work after many more artifacts exist.

---

## 5. Registry philosophy

The artifact registry is primarily a reference and navigation structure.

It should help the future KR production project do things like:
- find the authoritative doctrine file for an aspect
- see whether a protocol already exists
- identify missing artifacts in a family
- detect obsolete or superseded artifacts
- understand what artifact should be updated after a new decision
- understand which artifacts are active inputs to future work

It should not try to carry:
- long rationale
- full doctrine content
- detailed operational logic
- full decision history

That content belongs in the artifacts themselves.

---

## 6. Registry format choice

The artifact registry should generally use a structured format such as YAML.

Why:
- entries repeat a common schema
- fields benefit from normalization
- future automation or validation may become useful
- prose would make scanning and filtering harder
- the registry is primarily about structured reference state

So the default recommendation is a file such as:

`docs/registries/ARTIFACT_REGISTRY.yaml`

That file should be the authoritative artifact inventory unless the project later evolves a stronger structured system.

---

## 7. Registry entry philosophy

Each registry entry should describe one artifact in a compact, normalized, reusable way.

A good entry should make it easy to answer:
- what is this artifact?
- what class is it?
- where is it?
- is it active?
- what aspect does it support?
- how authoritative is it?
- what lifecycle stage is it in?
- what related artifacts matter?

A registry entry should not attempt to summarize the whole artifact in detail.

It should point, classify, and clarify.

---

## 8. Artifact classes tracked by the registry

Each artifact entry should have an explicit class.

Recommended classes:

- control_plane
- doctrine
- protocol
- architecture
- evaluation
- registry
- schema
- template
- execution
- working
- generated_snapshot
- other

These classes should align with the broader repo artifact system.

If the project later needs more granularity, it may extend this list carefully.

---

## 9. Artifact authority levels

Each artifact entry should carry an authority level.

Recommended authority values:

- live_control
- durable_governing
- durable_supporting
- reusable_support
- working_intermediate
- historical_reference
- generated_evidence

### Meanings

#### live_control
The artifact governs current live project state.

Examples:
- `ACTIVE.md`

#### durable_governing
The artifact defines durable project law, doctrine, or protocol.

Examples:
- a major doctrine file
- a core protocol

#### durable_supporting
The artifact is durable and important, but not itself a primary governing text.

Examples:
- an architecture note that informs future work
- an evaluation reference artifact

#### reusable_support
The artifact is mainly a reusable scaffold or utility.

Examples:
- templates
- schemas
- structured helper artifacts

#### working_intermediate
The artifact is useful and intentionally tracked, but not final.

Examples:
- a working comparison memo

#### historical_reference
The artifact is retained for historical clarity but is no longer current.

#### generated_evidence
The artifact is evidence or output, not doctrine.

Authority level is one of the most important registry fields.

---

## 10. Artifact lifecycle states

Each artifact entry should carry a lifecycle state.

Recommended lifecycle values:

- proposed
- drafted
- active
- superseded
- deprecated
- archived
- rejected

### Meanings

#### proposed
The artifact has been identified as desirable but does not yet exist as a real accepted artifact.

#### drafted
The artifact exists in draft form but is not yet treated as fully active.

#### active
The artifact currently serves its intended role.

#### superseded
A newer artifact has replaced it.

#### deprecated
The artifact is still present but no longer preferred.

#### archived
The artifact is retained only for historical/reference reasons.

#### rejected
The artifact was proposed but intentionally not created or not accepted.

These states help the project understand not only what exists, but how alive it is.

---

## 11. Required registry fields

Each artifact entry should include the following fields in substance.

### 11.1 artifact_id
A stable unique identifier for the artifact record.

### 11.2 title
A concise human-readable artifact title.

### 11.3 path
The current repo path of the artifact.

### 11.4 class
Artifact class.

### 11.5 authority
Authority level.

### 11.6 lifecycle
Lifecycle state.

### 11.7 aspect
Primary KR aspect supported by the artifact.

### 11.8 scope
Whether the artifact is:
- cross_cutting
- local
- control_plane
- mixed
- other explicitly defined scope

### 11.9 purpose
A compact statement of why this artifact exists.

### 11.10 status_note
Optional compact note clarifying current condition.

### 11.11 owner_layer
Which layer mainly owns this artifact conceptually.

Recommended values:
- control_plane
- strategic_reasoning
- execution_support
- evaluation_system
- engine_local
- mixed

### 11.12 related_artifacts
Other artifacts strongly linked to this one.

### 11.13 related_decisions
Decision IDs strongly linked to this artifact, if relevant.

### 11.14 supersedes
Any earlier artifact replaced by this one.

### 11.15 superseded_by
Any newer artifact that replaced this one.

### 11.16 created_from
Optional origin note, such as:
- promoted from working memo
- created from accepted doctrine outcome
- created from decision DEC-014

### 11.17 last_meaningful_update
A marker for the last meaningful update.

### 11.18 notes
Optional compact comments if needed.

This field set is the default schema.

---

## 12. Optional high-value fields

The registry may optionally include fields such as:

### 12.1 format
markdown / yaml / json / other

### 12.2 stage_relevance
current_stage / v1 / later_state / cross_stage

### 12.3 execution_dependency
Whether execution work depends materially on this artifact.

### 12.4 review_required
Whether changes to this artifact should trigger stronger review.

### 12.5 canonical
true / false
Useful if several related artifacts exist but only one is canonical.

### 12.6 tags
Compact thematic tags.

These fields are optional.
They should be added only if they improve real project use.

---

## 13. Minimal YAML entry shape

A minimal useful entry could look like:

```yaml
- artifact_id: ART-001
  title: V1 Proof Doctrine
  path: docs/doctrine/V1_PROOF_DOCTRINE.md
  class: doctrine
  authority: durable_governing
  lifecycle: active
  aspect: A2
  scope: cross_cutting
  purpose: Defines what KR v1 must prove and what it explicitly does not need to prove.
  owner_layer: strategic_reasoning
  related_artifacts:
    - ART-005
  related_decisions:
    - DEC-003
  supersedes: null
  superseded_by: null
  created_from: accepted aspect-hardening outcome
  last_meaningful_update: 2026-03-30
  notes: null

# KR Artifact Registry Schema

## 1. Purpose

This document defines the schema and governing logic for an artifact registry in the future KR production project.

Its purpose is to provide a structured way to track the durable artifacts that the project creates and relies upon.

The artifact registry exists to answer questions such as:
- what durable artifacts currently exist?
- what kind of artifact is each one?
- where does each artifact live?
- what authority does it have?
- what aspect does it support?
- is it active, superseded, deprecated, or still only working material?
- what other artifacts depend on it?
- what artifacts are missing but expected?

The artifact registry is meant to improve:
- recoverability
- structural legibility
- authority clarity
- lifecycle discipline
- cross-session continuity

It is not a replacement for the artifacts themselves.
It is a structured index of the artifact system.

---

## 2. Core principle

As KR grows, it should not rely on human memory or ad hoc repo browsing to understand its strategic artifact landscape.

The project needs a durable inventory layer.

However, the artifact registry must remain:
- compact
- structured
- reference-oriented
- non-duplicative

It should not become:
- a second prose documentation system
- a substitute for reading the real artifacts
- a verbose catalog full of repeated content

The registry should answer:
- what exists
- what role it plays
- what state it is in
- where it lives
- why it matters

That is enough.

---

## 3. What counts as an artifact for registry purposes

The artifact registry should track artifacts that are sufficiently durable, important, or operationally relevant to matter for future work.

This includes:
- doctrine artifacts
- protocol artifacts
- architecture artifacts
- evaluation artifacts
- registries
- templates
- schemas
- execution-support artifacts
- selected working artifacts when they are important enough to track
- selected control-plane artifacts if the project chooses to include them explicitly

This usually excludes:
- casual notes
- ephemeral chat-only outputs
- transient generated files unless strategically important
- ordinary code files unless they are being tracked as part of a broader artifact system

The registry is for project artifacts, not for every file in the repo.

---

## 4. Design goals

The artifact registry should satisfy all of the following:

1. **Coverage of important artifacts**
   Significant strategic artifacts should be visible.

2. **Low duplication**
   The registry should not restate whole documents.

3. **Authority clarity**
   It should be easy to tell how much weight an artifact carries.

4. **Lifecycle clarity**
   It should be easy to see whether an artifact is active or obsolete.

5. **Aspect linkage**
   It should be easy to see what aspect an artifact belongs to or supports.

6. **Practical usability**
   Future workers should actually be able to use the registry as a navigation tool.

7. **Scalability**
   The registry should still work after many more artifacts exist.

---

## 5. Registry philosophy

The artifact registry is primarily a reference and navigation structure.

It should help the future KR production project do things like:
- find the authoritative doctrine file for an aspect
- see whether a protocol already exists
- identify missing artifacts in a family
- detect obsolete or superseded artifacts
- understand what artifact should be updated after a new decision
- understand which artifacts are active inputs to future work

It should not try to carry:
- long rationale
- full doctrine content
- detailed operational logic
- full decision history

That content belongs in the artifacts themselves.

---

## 6. Registry format choice

The artifact registry should generally use a structured format such as YAML.

Why:
- entries repeat a common schema
- fields benefit from normalization
- future automation or validation may become useful
- prose would make scanning and filtering harder
- the registry is primarily about structured reference state

So the default recommendation is a file such as:

`docs/registries/ARTIFACT_REGISTRY.yaml`

That file should be the authoritative artifact inventory unless the project later evolves a stronger structured system.

---

## 7. Registry entry philosophy

Each registry entry should describe one artifact in a compact, normalized, reusable way.

A good entry should make it easy to answer:
- what is this artifact?
- what class is it?
- where is it?
- is it active?
- what aspect does it support?
- how authoritative is it?
- what lifecycle stage is it in?
- what related artifacts matter?

A registry entry should not attempt to summarize the whole artifact in detail.

It should point, classify, and clarify.

---

## 8. Artifact classes tracked by the registry

Each artifact entry should have an explicit class.

Recommended classes:

- control_plane
- doctrine
- protocol
- architecture
- evaluation
- registry
- schema
- template
- execution
- working
- generated_snapshot
- other

These classes should align with the broader repo artifact system.

If the project later needs more granularity, it may extend this list carefully.

---

## 9. Artifact authority levels

Each artifact entry should carry an authority level.

Recommended authority values:

- live_control
- durable_governing
- durable_supporting
- reusable_support
- working_intermediate
- historical_reference
- generated_evidence

### Meanings

#### live_control
The artifact governs current live project state.

Examples:
- `ACTIVE.md`

#### durable_governing
The artifact defines durable project law, doctrine, or protocol.

Examples:
- a major doctrine file
- a core protocol

#### durable_supporting
The artifact is durable and important, but not itself a primary governing text.

Examples:
- an architecture note that informs future work
- an evaluation reference artifact

#### reusable_support
The artifact is mainly a reusable scaffold or utility.

Examples:
- templates
- schemas
- structured helper artifacts

#### working_intermediate
The artifact is useful and intentionally tracked, but not final.

Examples:
- a working comparison memo

#### historical_reference
The artifact is retained for historical clarity but is no longer current.

#### generated_evidence
The artifact is evidence or output, not doctrine.

Authority level is one of the most important registry fields.

---

## 10. Artifact lifecycle states

Each artifact entry should carry a lifecycle state.

Recommended lifecycle values:

- proposed
- drafted
- active
- superseded
- deprecated
- archived
- rejected

### Meanings

#### proposed
The artifact has been identified as desirable but does not yet exist as a real accepted artifact.

#### drafted
The artifact exists in draft form but is not yet treated as fully active.

#### active
The artifact currently serves its intended role.

#### superseded
A newer artifact has replaced it.

#### deprecated
The artifact is still present but no longer preferred.

#### archived
The artifact is retained only for historical/reference reasons.

#### rejected
The artifact was proposed but intentionally not created or not accepted.

These states help the project understand not only what exists, but how alive it is.

---

## 11. Required registry fields

Each artifact entry should include the following fields in substance.

### 11.1 artifact_id
A stable unique identifier for the artifact record.

### 11.2 title
A concise human-readable artifact title.

### 11.3 path
The current repo path of the artifact.

### 11.4 class
Artifact class.

### 11.5 authority
Authority level.

### 11.6 lifecycle
Lifecycle state.

### 11.7 aspect
Primary KR aspect supported by the artifact.

### 11.8 scope
Whether the artifact is:
- cross_cutting
- local
- control_plane
- mixed
- other explicitly defined scope

### 11.9 purpose
A compact statement of why this artifact exists.

### 11.10 status_note
Optional compact note clarifying current condition.

### 11.11 owner_layer
Which layer mainly owns this artifact conceptually.

Recommended values:
- control_plane
- strategic_reasoning
- execution_support
- evaluation_system
- engine_local
- mixed

### 11.12 related_artifacts
Other artifacts strongly linked to this one.

### 11.13 related_decisions
Decision IDs strongly linked to this artifact, if relevant.

### 11.14 supersedes
Any earlier artifact replaced by this one.

### 11.15 superseded_by
Any newer artifact that replaced this one.

### 11.16 created_from
Optional origin note, such as:
- promoted from working memo
- created from accepted doctrine outcome
- created from decision DEC-014

### 11.17 last_meaningful_update
A marker for the last meaningful update.

### 11.18 notes
Optional compact comments if needed.

This field set is the default schema.

---

## 12. Optional high-value fields

The registry may optionally include fields such as:

### 12.1 format
markdown / yaml / json / other

### 12.2 stage_relevance
current_stage / v1 / later_state / cross_stage

### 12.3 execution_dependency
Whether execution work depends materially on this artifact.

### 12.4 review_required
Whether changes to this artifact should trigger stronger review.

### 12.5 canonical
true / false
Useful if several related artifacts exist but only one is canonical.

### 12.6 tags
Compact thematic tags.

These fields are optional.
They should be added only if they improve real project use.

---

## 13. Minimal YAML entry shape

A minimal useful entry could look like:

```yaml
- artifact_id: ART-001
  title: V1 Proof Doctrine
  path: docs/doctrine/V1_PROOF_DOCTRINE.md
  class: doctrine
  authority: durable_governing
  lifecycle: active
  aspect: A2
  scope: cross_cutting
  purpose: Defines what KR v1 must prove and what it explicitly does not need to prove.
  owner_layer: strategic_reasoning
  related_artifacts:
    - ART-005
  related_decisions:
    - DEC-003
  supersedes: null
  superseded_by: null
  created_from: accepted aspect-hardening outcome
  last_meaningful_update: 2026-03-30
  notes: null

This is only an example shape.
The actual registry may evolve, but the structure should remain disciplined.

14. Registry-wide metadata

The registry file itself may include a small metadata header such as:

registry purpose
schema version
update discipline
what kinds of artifacts are included
what kinds are intentionally excluded

This helps future workers interpret the registry correctly.

Example conceptual fields:

registry_name
purpose
schema_version
update_rule
inclusion_rule
exclusion_rule

This metadata should remain compact.

15. Artifact ID scheme principles

Artifact IDs should be:

stable
simple
greppable
not dependent on fragile implicit ordering elsewhere

A simple scheme such as:

ART-001
ART-002
ART-003

is usually sufficient initially.

Do not overcomplicate ID design early.

If later scale requires family prefixes, the project may adopt them carefully, but simplicity is preferable until scale justifies more structure.

16. Inclusion rule

An artifact should be included in the registry when one or more of the following are true:

it is durable enough that future workers may need to find it repeatedly
it has governing or supporting strategic importance
it participates in cross-artifact reasoning
its lifecycle state matters to future work
it is part of a tracked artifact family
execution or review may depend on it
losing visibility of it would materially reduce project coherence

Not every markdown file deserves an entry.

The registry should remain selective.

17. Exclusion rule

An artifact should usually not be included in the registry if it is:

trivial
ephemeral
purely local and obvious in context
not expected to matter outside its immediate moment
a routine generated output with no lasting significance
a duplicate or shadow artifact without durable role

The registry is not an exhaustive filesystem mirror.

It is a strategically meaningful inventory.

18. Update triggers

The artifact registry should usually be updated when:

a new durable artifact is accepted
a proposed artifact becomes active
an artifact is superseded or deprecated
an artifact changes authority or lifecycle meaningfully
an artifact is promoted from working to durable
a major file move changes the authoritative path
an artifact is archived or rejected

Routine content edits do not always require registry updates unless they materially affect the entry fields.

19. Promotion and demotion logic

When an artifact changes maturity, the registry should reflect that.

Examples:

working memo → doctrine file
drafted protocol → active protocol
active doctrine → superseded doctrine
proposed artifact → rejected artifact

The registry should help future workers understand these transitions without rereading full history.

Promotion and demotion are registry-relevant events.

20. Relationship to the decision log

The artifact registry and decision log serve different purposes.

Artifact registry

Tracks the artifacts themselves.

Decision log

Tracks durable commitments and why they were made.

The registry should link to related decisions where useful.
The decision log should refer to affected artifacts where useful.

But they should not be collapsed into one system.

A decision may affect several artifacts.
An artifact may be shaped by several decisions.

That many-to-many relationship is normal.

21. Relationship to the aspect state model

The artifact registry and aspect state model are related but distinct.

Aspect state model

Tracks maturity of aspects.

Artifact registry

Tracks durable artifacts.

The registry should usually include the primary aspect supported by an artifact.
This creates a useful bridge:

what artifacts exist for A2?
what artifacts support A13?
does A27 have active governing artifacts yet?

This linkage helps diagnose under-artifacted aspects.

22. Relationship to file naming and placement rules

The registry should not replace naming and placement discipline.

It assumes that artifact paths and names are already governed well.

However, it can help detect violations such as:

wrong family placement
unclear lifecycle
duplicate artifact homes
artifacts with unclear scope

In that sense, it supports repo discipline indirectly.

23. Missing-artifact tracking

The registry may optionally support “expected but not yet active” artifacts through proposed lifecycle entries.

This is useful when the project wants structured visibility into missing artifact families.

Example uses:

doctrine file identified as necessary but not yet drafted
registry planned but not yet created
template required before execution scale-up

Use this sparingly.
The registry must not become a wish list dump.

Only include proposed artifacts that are strategically real enough to matter.

24. Canonical-artifact rule

When several related artifacts exist, the registry should make it easy to identify the canonical one.

This matters especially when:

an older doctrine was superseded
a working memo coexists with a mature doctrine
a local note coexists with a cross-cutting governing file
an archived artifact remains for history

The canonical concept may be represented explicitly or inferred from authority + lifecycle, but the registry must make the answer legible.

Future workers should not have to guess which artifact is current.

25. Registry review criteria

Before accepting an artifact registry entry, the production project should ask:

25.1 Is the artifact real enough to register?

Or is it too ephemeral?

25.2 Is the class correct?

Would a future worker agree with how it is classified?

25.3 Is the authority level accurate?

Does the entry overstate or understate the artifact’s role?

25.4 Is the lifecycle state accurate?

Is this actually active, or only drafted, or already superseded?

25.5 Is the aspect linkage useful and correct?

Does it point to the right primary aspect?

25.6 Is the purpose concise but informative?

Does it explain why the artifact matters without restating the whole file?

25.7 Are links to related artifacts and decisions sufficient?

Would a future worker know where to look next?

If these checks fail, the entry should be revised.

26. Anti-failure rules

The future KR production project must avoid the following artifact-registry failures.

26.1 Filesystem-mirror failure

The registry tries to list everything and becomes noisy.

26.2 Prose-duplication failure

Entries restate whole documents rather than indexing them.

26.3 Authority-confusion failure

The registry fails to distinguish governing from supporting or working artifacts.

26.4 Lifecycle-blind failure

Superseded or deprecated artifacts remain indistinguishable from active ones.

26.5 Tag-soup failure

Too many optional metadata fields make entries noisy and weak.

26.6 Stale-registry failure

The registry is not updated when artifact reality changes.

26.7 Wish-list failure

The registry fills with speculative artifacts that may never matter.

26.8 Canonicality-failure

Future workers cannot tell which artifact in a family is the real one.

These failures must be resisted actively.

27. Recommended initial schema

A strong initial schema is:

registry_name: KR Artifact Registry
purpose: Tracks durable and strategically meaningful project artifacts.
schema_version: 1
update_rule: Update when artifact reality changes materially.
inclusion_rule: Include durable, governing, reusable, or strategically important artifacts only.
exclusion_rule: Exclude trivial, ephemeral, or low-value local files.

artifacts:
  - artifact_id: ART-001
    title: ...
    path: ...
    class: ...
    authority: ...
    lifecycle: ...
    aspect: ...
    scope: ...
    purpose: ...
    owner_layer: ...
    related_artifacts: []
    related_decisions: []
    supersedes: null
    superseded_by: null
    created_from: null
    last_meaningful_update: ...
    notes: null

This is intentionally simple.
The project should begin with a schema it can actually maintain.

28. Success condition

The artifact registry schema is successful only if the future KR production project can use it to do all of the following:

know what durable artifacts exist
know what kind of artifact each one is
know which artifacts are active versus historical
navigate from aspects and decisions to relevant artifacts
detect missing or underdeveloped artifact families
preserve authority clarity as the repo grows
maintain structural legibility over time

That is the intended standard.
