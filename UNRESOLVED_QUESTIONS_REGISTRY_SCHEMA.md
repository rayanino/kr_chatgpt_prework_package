# KR Unresolved Questions Registry Schema

## 1. Purpose

This document defines the schema and governing logic for a registry of unresolved questions in the future KR production project.

Its purpose is to ensure that important unresolved matters are tracked explicitly rather than:
- forgotten,
- repeatedly rediscovered,
- blurred into fake decisions,
- or left as vague “things to think about later.”

The unresolved-questions registry exists to answer questions such as:
- what important questions are still open?
- why are they unresolved?
- what kind of blocker is involved?
- what aspect does each question belong to?
- what would resolve or reduce the uncertainty?
- does the question currently block anything important?
- what is the next meaningful move on it?

This registry is a structured uncertainty and blocker memory system.

---

## 2. Core principle

An unresolved question is not a failure.

It is a legitimate project state.

The future KR production project should be willing to say:
- this is still open,
- this matters,
- this is why it remains open,
- and this is what would move it forward.

That is much better than:
- pretending the question was settled,
- burying it in chat prose,
- or leaving it to future workers to rediscover.

The registry should make unresolvedness visible without turning it into clutter.

---

## 3. What counts as an unresolved question

A question belongs in the unresolved-questions registry when one or more of the following are true:

### 3.1 Strategic importance
The answer would materially affect KR’s direction, quality, architecture, or workflow.

### 3.2 Recurrent relevance
The question is likely to come up again if not tracked.

### 3.3 Blocker relevance
The question currently blocks progress in an aspect, artifact, or execution path.

### 3.4 Evidence dependency
The question cannot be responsibly answered yet because evidence is missing.

### 3.5 Domain-sensitivity
The question bears on scholarly correctness, legitimacy, or boundary claims that should not be guessed.

### 3.6 Branching consequence
Different answers would meaningfully change downstream choices.

### 3.7 High-forgetfulness risk
If not recorded, the question will likely be lost and later rediscovered inefficiently.

If none of these apply, the question probably does not need registry status.

---

## 4. What does NOT count as an unresolved question worth registering

The registry should usually exclude:
- casual curiosity
- trivial implementation details
- low-value open thoughts
- temporary wording indecision
- issues that can be resolved immediately with local judgment
- generic “we should think about X someday” notes
- matters already captured adequately in a task packet or local work note

The registry is for meaningful unresolvedness, not every open loop.

---

## 5. Design goals

The unresolved-questions registry should satisfy all of the following:

1. **Visibility**
   Important open questions should not disappear.

2. **Specificity**
   Each question should be stated clearly enough to act on later.

3. **Blocker clarity**
   It should be obvious why the question remains unresolved.

4. **Resolution guidance**
   It should be clear what would help resolve it.

5. **Non-inflation**
   The registry should stay selective enough to remain useful.

6. **Aspect linkage**
   It should be clear which aspect each question belongs to.

7. **Decision separation**
   Open questions should not be confused with actual commitments.

---

## 6. Registry philosophy

The unresolved-questions registry is not a backlog and not a decision log.

### It is not a backlog
Because not every unresolved question implies immediate work.

### It is not a decision log
Because unresolved questions are not commitments.

It is a structured record of important open issues that the project explicitly knows it has not yet closed.

That distinction is essential.

---

## 7. Recommended format

The unresolved-questions registry should generally use a structured format such as YAML.

Why:
- entries repeat a common schema
- status and blocker type benefit from normalization
- compact scanning matters
- future filtering and automation may help
- prose would make structured tracking weaker

Default recommendation:

`docs/registries/UNRESOLVED_QUESTIONS.yaml`

That file should be the authoritative registry unless the project later evolves a stronger structured system.

---

## 8. Question classes

Each unresolved question should have a primary class.

Recommended classes:

- strategic
- doctrinal
- architectural
- evaluation
- evidence
- scholarly
- sequencing
- execution
- artifact
- workflow
- other

### Example meanings

#### strategic
Open question about direction, scope, expansion, roadmap, or project value.

#### doctrinal
Open question about a durable boundary or project position.

#### architectural
Open question about system structure or relationship between major components.

#### evaluation
Open question about how quality, thresholds, or failure should be judged.

#### evidence
Open question whose main barrier is missing external evidence.

#### scholarly
Open question bearing on Islamic-science correctness, legitimacy, or taxonomy truth that should not be guessed.

#### sequencing
Open question about what should happen when.

#### execution
Open question blocking safe implementation or delegation.

#### artifact
Open question about what durable files or structures should exist.

#### workflow
Open question about how the project itself should operate.

This classification helps future workers orient quickly.

---

## 9. Unresolved status model

Each entry should have an explicit status.

Recommended statuses:

- open
- under_investigation
- blocked_by_evidence
- blocked_by_user
- blocked_by_dependency
- narrowed
- partially_resolved
- resolved
- retired

### Meanings

#### open
The question is recognized and important, but active resolution work is not yet underway.

#### under_investigation
The project is actively trying to resolve the question.

#### blocked_by_evidence
The answer depends on missing evidence or research.

#### blocked_by_user
The answer depends on user decision, preference, approval, or access.

#### blocked_by_dependency
Another aspect, artifact, or task must mature first.

#### narrowed
The question has been clarified and bounded, but not yet answered.

#### partially_resolved
Some uncertainty has been reduced, but the full question is not yet closed.

#### resolved
The question has been meaningfully answered and should usually transition into a decision, doctrine update, artifact update, or closed record.

#### retired
The question is no longer relevant in its previous form.

This status model keeps unresolvedness dynamic rather than static.

---

## 10. Required registry fields

Each unresolved-question entry should include the following fields in substance.

### 10.1 question_id
A stable unique identifier.

### 10.2 title
A compact human-readable label.

### 10.3 question
The actual unresolved question in direct form.

### 10.4 class
Primary question class.

### 10.5 status
Current unresolved status.

### 10.6 aspect
Primary KR aspect affected.

### 10.7 why_it_matters
Why this question is strategically or operationally important.

### 10.8 blocker_type
Why the question remains unresolved.

Recommended values:
- evidence
- user
- dependency
- ambiguity
- insufficient_hardening
- external_constraint
- mixed

### 10.9 current_blocker
A compact description of the current blocking factor.

### 10.10 what_would_help_resolve_it
What evidence, decision, artifact, comparison, or task would move it forward.

### 10.11 current_best_guess
Optional current leaning, if one exists, clearly marked as non-final.

### 10.12 affected_artifacts
Artifacts that depend on or are constrained by this question.

### 10.13 affected_decisions
Any decisions that are waiting on or related to this question.

### 10.14 downstream_impact
What remains blocked or distorted while this stays unresolved.

### 10.15 next_best_move
The next concrete step, if any.

### 10.16 priority
How important this unresolved question is right now.

Recommended values:
- p0
- p1
- p2
- p3

### 10.17 owner_layer
Which layer should mainly drive resolution.

Recommended values:
- strategic_reasoning
- deep_research
- user
- execution_support
- mixed

### 10.18 last_meaningful_update
Marker for the last substantive update.

### 10.19 notes
Optional compact notes.

This is the default schema.

---

## 11. Optional high-value fields

The registry may also include optional fields such as:

### 11.1 linked_research_task
If a specific research task was created.

### 11.2 linked_aspect_state
If the unresolved question maps directly to an aspect state issue.

### 11.3 resolution_threshold
What counts as “resolved enough.”

### 11.4 confidence_if_forced
If the project had to choose now, how confident would the current best guess be.

### 11.5 stage_relevance
current_stage / v1 / later_state / cross_stage

Add these only if they improve real usage.

---

## 12. Minimal YAML entry shape

A minimal useful entry could look like:

```yaml
- question_id: Q-001
  title: PDF support strategic necessity
  question: Is PDF support strategically necessary for KR’s serious long-horizon library ambitions, or can it remain a later-stage expansion without materially capping corpus value?
  class: strategic
  status: open
  aspect: A8
  why_it_matters: Input-format narrowness may cap the long-term value and coverage of the library.
  blocker_type: evidence
  current_blocker: The project lacks sufficiently grounded understanding of likely corpus realities, extraction costs, and format tradeoffs.
  what_would_help_resolve_it: Targeted research on source availability, PDF extraction realities, and likely corpus acquisition constraints.
  current_best_guess: PDF support is likely strategically important, but the timing and required depth of support remain unresolved.
  affected_artifacts:
    - ART-004
  affected_decisions:
    - DEC-009
  downstream_impact: Input-format roadmap and ingestion doctrine remain incomplete.
  next_best_move: Run a focused research pass on long-horizon corpus format realities and implications for KR.
  priority: p1
  owner_layer: deep_research
  last_meaningful_update: 2026-03-30
  notes: null

This is only an example shape.
The actual registry can evolve, but the schema should remain disciplined.

13. Question ID scheme principles

Question IDs should be:

stable
simple
greppable
easy to reference in chats, artifacts, and decisions

A simple scheme such as:

Q-001
Q-002
Q-003

is usually sufficient.

Do not overengineer the ID system early.

14. Inclusion rule

A question should be included in the registry when:

it is important enough that future workers may need to see it,
it is unresolved in a meaningful way,
it affects real project quality or sequencing,
or it blocks significant progress.

The registry should remain selective.
Its usefulness depends on signal.

15. Exclusion rule

A question should usually not be included when:

it can be answered immediately with local judgment,
it is too small to matter,
it is already fully captured inside a task packet or a local issue queue,
it is unlikely to recur or affect broader work,
or it is just a broad curiosity with no strategic consequence.

The registry is not a brain dump of uncertainty.

16. Relationship to the decision log

The unresolved-questions registry and decision log serve different roles.

Unresolved-questions registry

Tracks important open issues.

Decision log

Tracks commitments that were actually made.

When a question becomes resolved enough to produce a commitment:

the unresolved entry should move toward resolved or retired
and a decision record may need to be created

A question should not stay “open” forever once a real decision exists.
Likewise, a decision should not be logged if the key issue is still genuinely unresolved.

This separation is critical.

17. Relationship to the aspect state model

Unresolved questions often explain why an aspect is in a certain state.

Examples:

an aspect is blocked_by_evidence because Q-014 remains open
an aspect is only provisionally_hardened because Q-021 still limits full hardening
an aspect is blocked_by_user because Q-033 requires owner approval

The registry should therefore help the project understand not only which questions are open, but which aspect states they are shaping.

This is one of its main strategic values.

18. Relationship to deep research

Some unresolved questions are best owned by strategic reasoning.
Others are best owned by research.

The registry should therefore make it easy to see:

which questions are evidence-gated,
which require a deep-research pass,
which are actually user-gated,
and which are internal design questions still needing critique rather than research.

This prevents the project from using research indiscriminately.

19. Relationship to execution

An unresolved question may block execution directly.

Examples:

task packet cannot be written safely until the question is resolved
execution can proceed only under a provisional assumption
a task is safe only if the unresolved question is explicitly kept out of scope

The registry should help the production project know when unresolvedness is execution-relevant.
That makes it part of safe delegation.

20. Priority doctrine

Each unresolved question should carry a current priority, not because the registry is a backlog, but because not every open question matters equally right now.

Recommended meanings:

p0

Immediate blocker or highly consequential open issue.

p1

Important near-term issue whose resolution would materially improve ongoing work.

p2

Important but not urgent now.

p3

Later-stage or lower-pressure unresolved matter worth tracking.

Priority should remain stage-sensitive and revisable.

21. Best-guess doctrine

Some open questions will still have a current best guess.

That can be useful, but dangerous if mishandled.

A current_best_guess field should:

be optional,
be explicitly non-final,
never masquerade as a decision,
and be clearly subordinate to actual resolution.

This field is for orientation, not commitment.

22. Resolution doctrine

A question should move toward resolved only when one or more of the following are true:

the key uncertainty has been reduced enough to make a real commitment
the necessary evidence has arrived
the required user decision has been made
the dependency has been resolved
the project no longer needs the question answered because the frame changed and the question was retired

Resolution should not mean:

“we got tired of thinking about it”

It should mean:

the question no longer functions as a live open issue in its previous form
23. Retired-question doctrine

A question may be retired instead of resolved.

This is appropriate when:

the project scope changed
the question became irrelevant
the framing turned out to be wrong
the issue dissolved into a different better-framed question

Retiring a question is not the same as resolving it.
It means the project no longer treats that exact question as live.

This distinction matters for historical clarity.

24. Update triggers

The unresolved-questions registry should usually be updated when:

a new important unresolved question is discovered
a question is narrowed or clarified
a blocker type changes
a research pass materially changes the situation
a user decision resolves or partially resolves the issue
a dependency clears
a current best guess changes materially
the question is resolved or retired

Routine discussion that does not change the question materially does not always require an update.

25. Review criteria for entries

Before accepting an unresolved-question entry, the production project should ask:

25.1 Is this question important enough to register?

Or is it too small or too local?

25.2 Is the question stated clearly?

Would a future worker understand what is actually open?

25.3 Is the blocker type accurate?

Does the entry correctly identify why the question is unresolved?

25.4 Is the “why it matters” field real?

Does this actually explain the consequence of unresolvedness?

25.5 Is the next-best-move useful?

Would a future worker know how to proceed?

25.6 Is this still an unresolved question rather than already a decision?

The line must stay clean.

If these fail, the entry should be revised or omitted.

26. Anti-failure rules

The future KR production project must avoid the following unresolved-question failures.

26.1 Uncertainty-dump failure

Every open thought enters the registry and destroys signal.

26.2 Fake-decision failure

A question with a leaning is treated as settled.

26.3 Vague-question failure

The entry is too fuzzy to guide future work.

26.4 No-blocker failure

The project says a question is open but not why.

26.5 Forgotten-open-loop failure

Important unresolved matters remain trapped in chats.

26.6 Never-closed failure

Questions remain open even after real decisions or artifact updates made them obsolete.

26.7 Registry-backlog failure

The registry becomes a substitute for actual prioritization or tasking.

26.8 Research-confusion failure

Questions that need critique are mislabeled as needing research, or vice versa.

These failures must be resisted actively.

27. Recommended initial schema

A strong initial schema is:

registry_name: KR Unresolved Questions Registry
purpose: Tracks important open questions that materially affect KR direction, quality, sequencing, or execution.
schema_version: 1
update_rule: Update when a question is added, narrowed, materially changed, resolved, or retired.
inclusion_rule: Include strategically meaningful unresolved questions only.
exclusion_rule: Exclude trivial, local, or easily answerable open loops.

questions:
  - question_id: Q-001
    title: ...
    question: ...
    class: ...
    status: ...
    aspect: ...
    why_it_matters: ...
    blocker_type: ...
    current_blocker: ...
    what_would_help_resolve_it: ...
    current_best_guess: null
    affected_artifacts: []
    affected_decisions: []
    downstream_impact: ...
    next_best_move: ...
    priority: ...
    owner_layer: ...
    last_meaningful_update: ...
    notes: null

This schema is intentionally simple.
The project should start with a shape it can actually maintain.

28. Success condition

The unresolved-questions registry schema is successful only if the future KR production project can use it to do all of the following:

keep important open questions visible
distinguish real unresolvedness from actual commitments
explain why questions remain open
identify what would move them forward
connect unresolvedness to aspects, artifacts, and decisions
avoid fake closure and avoid forgetfulness
improve long-horizon strategic coherence

That is the intended standard.

