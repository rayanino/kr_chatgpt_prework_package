# KR Aspect Registry Schema

## 1. Purpose

This document defines the schema and governing logic for the aspect registry in the future KR production project.

Its purpose is to provide a structured operational index of KR’s aspects so that the project can track, at a glance:

- what aspects exist
- what each aspect is about
- what state each aspect is currently in
- how urgent each aspect is
- what artifacts support it
- what unresolved questions constrain it
- what the best next move is
- which aspects are under-hardened, blocked, deferred, or ready to support execution

The aspect registry is the operational layer that turns the aspect map and aspect state model into a usable management surface.

It is one of the main tools for preventing:
- arbitrary topic selection
- blind spots
- false feelings of progress
- forgotten aspects
- poor sequencing discipline

---

## 2. Core principle

The aspect map defines the landscape.

The aspect registry tracks the current lived state of that landscape.

That means the registry is not merely a list of aspect names.
It is a structured answer to questions like:

- what aspect should probably be worked on next?
- what aspect is active but blocked?
- what aspect is already strong enough to guide downstream work?
- what aspect still lacks doctrine artifacts?
- what aspect is urgent but under-artifacted?
- what aspect is deferred intentionally rather than accidentally neglected?

The aspect registry should therefore be:
- compact
- structured
- operational
- stage-aware
- non-redundant

It should not attempt to replace the full aspect map or the full doctrine files.

---

## 3. Design goals

The aspect registry should satisfy all of the following:

1. **Coverage visibility**
   The project should be able to see which aspects exist and which remain underdeveloped.

2. **State visibility**
   The current maturity of each aspect should be legible.

3. **Priority visibility**
   The project should be able to see what matters most now.

4. **Blocker visibility**
   It should be obvious when and why an aspect is stuck.

5. **Artifact linkage**
   It should be easy to see what durable structures already support the aspect.

6. **Next-move usefulness**
   The registry should help the project decide what to do next.

7. **Low duplication**
   The registry should point and classify, not restate the full doctrine of each aspect.

---

## 4. Relationship to other systems

The aspect registry is closely related to several other project systems, but it is not identical to any of them.

### 4.1 Aspect map
The aspect map defines what the aspects are in conceptual detail.

### 4.2 Aspect state model
The state model defines the legal state vocabulary and transition logic.

### 4.3 Artifact registry
The artifact registry tracks artifacts, not aspects.

### 4.4 Unresolved questions registry
That registry tracks open questions, not aspect status as a whole.

### 4.5 Decision log
The decision log records commitments, not the current overall maturity of an aspect.

The aspect registry should connect to these systems, not collapse them into one.

---

## 5. Recommended format

The aspect registry should generally use a structured format such as YAML.

Why:
- the fields repeat predictably
- comparison across aspects matters
- state and priority are structured
- future filtering is useful
- the registry is primarily operational reference, not prose argument

Default recommendation:

`docs/registries/ASPECT_REGISTRY.yaml`

That file should be the authoritative structured view of aspect status unless the project later evolves a stronger system.

---

## 6. What an aspect entry represents

Each aspect entry should represent one Level B aspect from the KR master aspect map.

It should not represent:
- every small subquestion
- every chat thread
- every implementation task

The aspect registry is for enduring aspect-level units.

Subaspects may be mentioned where helpful, but the main registry unit should remain the aspect itself.

---

## 7. Required registry fields

Each aspect entry should include the following fields in substance.

### 7.1 aspect_id
A stable aspect identifier.

Example:
- A2
- A8
- A13

### 7.2 aspect_name
Short human-readable aspect name.

### 7.3 domain
The top-level domain from the aspect map.

Examples:
- Mission and end-state
- Corpus and input acquisition
- Evaluation and quality control

### 7.4 summary
A compact statement of what the aspect governs.

### 7.5 current_state
Current aspect state using the approved state model.

Examples:
- S0
- S4
- S7
- S10

### 7.6 current_priority
Current priority class.

Recommended values:
- P0
- P1
- P2
- P3

### 7.7 why_current_priority
Why the aspect currently has that priority.

### 7.8 current_leading_direction
Optional compact statement of the current strongest direction, if one exists.

This must not be mistaken for full doctrine.

### 7.9 main_blocker_type
If blocked, what kind of blocker applies.

Recommended values:
- none
- evidence
- user
- dependency
- ambiguity
- mixed

### 7.10 main_blocker
Compact description of the blocker, if any.

### 7.11 key_unresolved_questions
List of linked unresolved-question IDs or compact references.

### 7.12 supporting_artifacts
List of major artifacts that currently support the aspect.

### 7.13 governing_artifact
If one primary doctrine or governing artifact exists for this aspect, record it explicitly.

### 7.14 related_decisions
Key decision IDs materially shaping the aspect.

### 7.15 execution_readiness
Whether the aspect is currently mature enough to safely support bounded execution work.

Recommended values:
- none
- exploratory_only
- limited
- moderate
- strong

### 7.16 best_next_move
The single best next move for this aspect if it were to be worked on.

### 7.17 last_meaningful_update
Marker for the last substantive change in aspect status.

### 7.18 notes
Optional compact notes.

This is the default schema.

---

## 8. Optional high-value fields

The registry may also include optional fields such as:

### 8.1 stage_relevance
current_stage / v1 / later_state / cross_stage

### 8.2 under_artifacted
true / false  
Useful if the aspect clearly needs more durable files than it currently has.

### 8.3 needs_research
true / false  
Useful when evidence is clearly the next gate.

### 8.4 active_chat_count_or_marker
Optional trace of whether the aspect currently has an active hardening thread.

### 8.5 dependency_aspects
Other aspects that this aspect depends on or strongly interacts with.

### 8.6 confidence_level
C1 / C2 / C3 / C4 if the project wants a compact maturity-confidence signal.

Use optional fields only when they improve real operational clarity.

---

## 9. Minimal YAML entry shape

A minimal useful entry could look like:

```yaml
- aspect_id: A2
  aspect_name: V1 proof doctrine
  domain: Mission and end-state
  summary: Defines exactly what KR v1 must prove and what it explicitly does not need to prove.
  current_state: S1
  current_priority: P0
  why_current_priority: This aspect strongly shapes evaluation, execution readiness, and separation between current work and later-state ambition.
  current_leading_direction: null
  main_blocker_type: none
  main_blocker: null
  key_unresolved_questions: []
  supporting_artifacts: []
  governing_artifact: null
  related_decisions: []
  execution_readiness: none
  best_next_move: Open the first dedicated hardening chat and define minimum proof conditions and explicit non-goals.
  last_meaningful_update: 2026-03-30
  notes: null

This is only an example shape.
The actual registry can evolve, but the structure should remain compact and operational.

10. Aspect ID doctrine

The registry should use the same aspect IDs as the master aspect map.

This is important because:

it preserves consistency
it makes cross-reference easier
it prevents accidental duplicate aspect identity
it allows decisions, artifacts, and unresolved questions to link to the same aspect vocabulary

The aspect registry must not invent a second conflicting aspect ID system.

11. Current state field doctrine

The current_state field should use the official aspect state model and should be assigned conservatively.

It should answer:

where is this aspect actually now?

Not:

where do we wish it were?

The registry should not inflate maturity.
Its usefulness depends on honest state assignment.

12. Current priority field doctrine

The current_priority field should be stage-dependent and revisable.

It should answer:

how important is it to work on this aspect now, relative to the project’s current situation?

Priority should not be treated as eternal.
An aspect may move:

from P3 to P1
from P0 to P2
or from P1 to deferred importance

The registry should help reveal stage-sensitive attention, not a frozen ranking.

13. Leading-direction field doctrine

The current_leading_direction field is optional and should be used carefully.

Its purpose is to provide a short orienting signal such as:

PDF support is likely strategically important, but timing remains unresolved
taxonomy doctrine should prioritize study usefulness over decorative classification
v1 should prove trustworthy substrate quality rather than complete final product behavior

This field must remain:

compact
non-doctrinal in full weight
explicitly subordinate to real doctrine artifacts when they exist

It is for operational orientation, not for replacing doctrine.

14. Execution-readiness field doctrine

The aspect registry should make it easier to know whether an aspect can safely support execution work.

Recommended values:

none

The aspect is too immature for execution relevance.

exploratory_only

Only very limited exploratory work is appropriate.

limited

Some bounded execution may be safe within tight constraints.

moderate

Meaningful bounded execution can proceed with care.

strong

The aspect is mature enough to support normal bounded execution handoff where relevant.

This field should be influenced by:

aspect state
blocker status
artifact support
doctrine clarity
unresolved question severity

It is a useful bridge between strategic maturity and delegation.

15. Best-next-move doctrine

Each aspect entry should include a best_next_move field.

This is one of the most valuable operational fields in the registry.

It should answer:

if the project were to work on this aspect next, what is the strongest concrete next move?

Good best-next-move examples:

Open a dedicated hardening chat to define v1 non-goals and minimum proof conditions.
Run a focused evidence pass on corpus-format realities to clarify PDF support timing.
Convert the current provisionally hardened direction into INPUT_FORMAT_DOCTRINE.md.
Resolve the dependency on A27 evaluation doctrine before further execution handoff.

Bad examples:

think more about this
continue exploring
maybe work on it later

The field should be concrete enough to guide action.

16. Governing-artifact doctrine

If an aspect already has a primary governing artifact, the registry should identify it explicitly.

Examples:

docs/doctrine/V1_PROOF_DOCTRINE.md
docs/doctrine/INPUT_FORMAT_DOCTRINE.md
docs/protocols/DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md

This helps future workers answer:

where is the main current durable guidance for this aspect?

Not every aspect will have a governing artifact early.
That itself is informative.

17. Under-artifacted aspect doctrine

The registry should make it easy to notice when an aspect is strategically meaningful but poorly supported by durable artifacts.

This may be represented explicitly with a field like:

under_artifacted: true

or inferred through missing governing/supporting artifacts.

This is useful because some aspects may appear intellectually developed in chats but remain structurally weak in the repo.

The aspect registry should help surface that mismatch.

18. Blocker doctrine

The registry should distinguish clearly between different kinds of blockage.

The main_blocker_type and main_blocker fields should help answer:

why is this aspect not progressing further right now?

This is important because:

evidence blockers require research
user blockers require escalation
dependency blockers require sequencing changes
ambiguity blockers require more internal hardening

“Blocked” without type is too vague to be operationally useful.

19. Relationship to unresolved questions

The key_unresolved_questions field is where the aspect registry connects to the unresolved-questions system.

This helps answer:

what open questions are still materially limiting this aspect?

The registry should not restate those questions in full.
It should point to them.

This preserves separation of concerns:

the aspect registry tracks the aspect
the unresolved-question registry tracks the open questions
20. Relationship to artifacts

The supporting_artifacts and governing_artifact fields connect the aspect registry to the artifact system.

This helps answer:

does this aspect already have doctrine?
does it have relevant protocols or evaluation artifacts?
is it under-supported structurally?
what file should a future worker read first for this aspect?

This is one of the reasons the aspect registry is so valuable.

21. Relationship to decisions

The related_decisions field gives the aspect registry a bridge into the decision system.

This helps answer:

what major commitments are already shaping this aspect?

The aspect registry should not duplicate decision rationale.
It should simply point to the relevant durable commitments.

22. Update triggers

The aspect registry should usually be updated when:

a new aspect is formally adopted into the map
an aspect changes state materially
an aspect priority changes materially
a major blocker appears or is resolved
a governing artifact is created
a major unresolved question is linked or removed
an aspect becomes execution-relevant in a new way
the best next move changes materially

Routine passing mentions in other chats do not usually justify registry updates.

23. Inclusion rule

Every Level B aspect in the master aspect map should generally have an entry in the aspect registry.

This is one of the key differences between the aspect registry and the artifact registry.

The artifact registry is selective.
The aspect registry should be close to comprehensive across the formal aspect map.

That is how it provides true coverage visibility.

24. Review criteria for entries

Before accepting an aspect entry or major update, the production project should ask:

24.1 Is the aspect identity correct?

Does this entry correspond to a real aspect from the map?

24.2 Is the state honest?

Or is it inflated or stale?

24.3 Is the priority realistic?

Or is it outdated, arbitrary, or wishful?

24.4 Are blockers explicit enough?

Would a future worker understand why the aspect is stuck?

24.5 Is the best next move concrete?

Would a future worker know what to do?

24.6 Is the artifact linkage useful?

Does the entry point to the right supporting structures?

24.7 Is the entry compact?

Does it remain an index rather than a mini-essay?

If these fail, the entry should be revised.

25. Anti-failure rules

The future KR production project must avoid the following aspect-registry failures.

25.1 Static-catalog failure

The registry becomes just a list of names and loses operational value.

25.2 Stale-state failure

The aspect states stop reflecting reality.

25.3 Priority-fantasy failure

Everything is marked urgent, or priority is not updated with stage changes.

25.4 Mini-essay failure

Entries become bloated prose rather than compact operational records.

25.5 Blocker-vagueness failure

The registry marks things blocked without saying why.

25.6 Artifact-blind failure

The registry does not reflect whether aspects are structurally supported.

25.7 Next-move-weakness failure

The registry cannot actually guide what to do next.

25.8 Coverage-illusion failure

The registry exists, but many formal aspects are missing or unmaintained.

These failures must be resisted actively.

26. Recommended initial schema

A strong initial schema is:

registry_name: KR Aspect Registry
purpose: Tracks the current maturity, priority, blockers, and next moves of KR’s formal aspects.
schema_version: 1
update_rule: Update when aspect state, priority, blockers, supporting artifacts, or next moves change materially.
coverage_rule: Include all formal Level B aspects from the KR master aspect map.

aspects:
  - aspect_id: A1
    aspect_name: ...
    domain: ...
    summary: ...
    current_state: ...
    current_priority: ...
    why_current_priority: ...
    current_leading_direction: null
    main_blocker_type: none
    main_blocker: null
    key_unresolved_questions: []
    supporting_artifacts: []
    governing_artifact: null
    related_decisions: []
    execution_readiness: none
    best_next_move: ...
    last_meaningful_update: ...
    notes: null

This schema is intentionally simple.
The project should begin with a shape it can actually maintain.

27. Success condition

The aspect registry schema is successful only if the future KR production project can use it to do all of the following:

see all formal aspects in one structured view
understand the maturity of each aspect
understand which aspects matter most now
understand what is blocking progress
understand what durable artifacts already support each aspect
understand what the best next move is for each aspect
preserve systematic long-horizon coverage instead of drifting arbitrarily

That is the intended standard.