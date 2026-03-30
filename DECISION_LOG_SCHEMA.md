# KR Decision Log Schema

## 1. Purpose

This document defines how the future KR production project should record durable decisions.

Its purpose is to ensure that important project commitments do not remain trapped in chat memory, vague summaries, or scattered artifacts without authority clarity.

The decision log exists to answer questions such as:

- what did KR decide?
- why was it decided?
- what alternatives were considered?
- what artifacts or workflows does it affect?
- is the decision still active?
- if it changed, what replaced it?

This schema is designed to preserve long-horizon strategic coherence.

---

## 2. Core principle

Not every conclusion deserves a decision record.

A decision record should exist only when the project has made a commitment that future work should be able to recover, rely on, and interpret.

The log should capture:

- commitments
- boundary-setting judgments
- important approvals
- reversals
- supersessions

It should not become:

- a diary
- a chat summary archive
- a backlog
- a place for every passing thought

The decision log is for durable project commitments.

---

## 3. What counts as a decision

A conclusion counts as a decision when one or more of the following are true:

### 3.1 Governing effect

It changes how future work should be done.

### 3.2 Boundary effect

It defines what is in bounds or out of bounds.

### 3.3 Priority effect

It changes what the project should focus on next or what is deferred.

### 3.4 Artifact effect

It causes a durable artifact to become required, updated, superseded, or deprecated.

### 3.5 Execution effect

It changes what implementation work may proceed.

### 3.6 Authority effect

It changes a standing project rule, role boundary, or protocol.

### 3.7 Reversal effect

It explicitly overturns an earlier decision.

If none of these apply, the conclusion usually does not need a decision record.

---

## 4. What does NOT count as a decision

The following usually do not deserve decision records:

- tentative brainstorming
- a local observation with no enduring consequence
- a minor wording choice with no downstream impact
- transient exploration notes
- a purely local implementation preference with no wider relevance
- a question that remains unresolved
- a plan to think more later
- a chat summary of progress

These may belong in working notes, artifacts, or handoff context, but not in the decision log.

---

## 5. Decision record design goals

The decision log should satisfy all of the following:

1. **Durability**
   It should preserve commitments worth remembering.

2. **Recoverability**
   A future worker should be able to understand what was decided without re-reading the whole originating chat.

3. **Non-redundancy**
   It should not duplicate whole doctrine files or protocols unnecessarily.

4. **Authority clarity**
   It should be clear whether a decision is active, superseded, rejected, or provisional.

5. **Cross-linkability**
   It should connect cleanly to relevant files, aspects, and prior decisions.

6. **Low clutter**
   It should remain selective enough to stay useful.

---

## 6. Decision classes

The future KR production project should classify decisions so that the log remains intelligible.

### D1 — Strategic decision

A major judgment about KR’s direction, scope, value model, roadmap, or end-state.

Examples:

- v1 proof boundary
- strategic expansion rule
- input-format roadmap class
- synthesis boundary

### D2 — Doctrinal decision

A durable position on how KR should think about an important concept or boundary.

Examples:

- taxonomy placement quality boundary
- trustworthiness standard
- provenance requirement
- user-workflow boundary

### D3 — Protocol decision

A durable commitment about how recurring work should be done.

Examples:

- review sequence
- when to use deep research
- how aspect chats should operate
- how execution packets should be formed

### D4 — Structural decision

A decision about repo organization, artifact taxonomy, file placement, schema families, or registry structure.

Examples:

- keep `.kr/` limited to control-plane artifacts
- create a doctrine namespace separate from protocols
- use a registry rather than prose for a given recurring structure

### D5 — Execution-gating decision

A decision that authorizes, blocks, or conditions implementation or delegation.

Examples:

- do not hand off taxonomy work until doctrine exists
- allow Codex local design freedom within a fixed schema boundary
- require acceptance criteria before execution starts

### D6 — Supersession or reversal decision

A decision that replaces, narrows, or overturns an earlier decision.

Examples:

- replacing a prior roadmap position
- retiring an earlier artifact structure
- changing a boundary that was previously accepted

These classes are not mutually exclusive in spirit, but each record should have one primary class.

---

## 7. Decision status model

Every decision record should have an explicit status.

Allowed statuses:

- proposed
- accepted
- active
- superseded
- deprecated
- rejected
- withdrawn

### Status meanings

#### proposed

The decision has been framed but not yet committed.

#### accepted

The decision has been accepted and is now real, but may not yet have been fully propagated into related artifacts.

#### active

The decision is accepted and currently authoritative.

#### superseded

The decision was once active, but a later decision replaced it.

#### deprecated

The decision is no longer preferred, but may still have residual relevance during transition.

#### rejected

The candidate decision was considered and explicitly not adopted.

#### withdrawn

The decision was previously proposed but intentionally removed before becoming active.

Status clarity is essential for long-horizon readability.

---

## 8. Decision authority rule

A decision record records a commitment.
It does not automatically replace the need to update any higher-authority governing artifacts that the decision affects.

Therefore:

- if a decision changes durable project law, the relevant doctrine or protocol file must be updated
- if a decision changes the active frontier, the active control artifact must be updated
- if a decision changes repo structure, the relevant structural artifact must be updated

The decision log records the commitment.
It is not a substitute for propagation.

This is a core rule.

---

## 9. Decision record fields

Every serious decision record should contain the following fields in substance.

### 9.1 Decision ID

A stable unique identifier.

### 9.2 Title

A short, precise description of what was decided.

### 9.3 Status

Current decision status.

### 9.4 Class

Primary decision class.

### 9.5 Date or session marker

When the decision was made.

### 9.6 Aspect

Which KR aspect the decision belongs to.

### 9.7 Decision statement

The actual commitment in direct language.

### 9.8 Why this decision was needed

Why the project had to decide this.

### 9.9 Rationale

Why this direction was judged strongest.

### 9.10 Alternatives considered

The strongest other paths and why they were not chosen.

### 9.11 Constraints or assumptions

Important assumptions, dependencies, or limiting conditions.

### 9.12 Implications

What this decision changes for future work.

### 9.13 Affected artifacts

Which files, protocols, doctrines, or registries are affected.

### 9.14 Related decisions

Which earlier or parallel decisions matter here.

### 9.15 Supersession field

Whether this decision supersedes another decision or is itself superseded later.

### 9.16 Confidence level

How hardened the decision is.

### 9.17 Evidence status

Whether the decision was internal-design-led, evidence-gated, research-supported, or still uncertainty-limited.

### 9.18 Next required propagation

What must now be updated because this decision exists.

This field set should be treated as the default shape for meaningful decision records.

---

## 10. Minimal decision record template

The future KR production project should be able to instantiate a decision quickly using a standard form.

### Decision record template

Decision ID:
[Unique ID]

Title:
[Short precise title]

Status:
[proposed / accepted / active / superseded / deprecated / rejected / withdrawn]

Class:
[D1 / D2 / D3 / D4 / D5 / D6]

Aspect:
[Relevant aspect]

Date or session:
[Marker]

Decision statement:
[The actual commitment]

Why this decision was needed:
[Why the project had to decide this]

Rationale:
[Why this direction was chosen]

Alternatives considered:

- [Alternative]
- [Alternative]

Constraints or assumptions:

- [Constraint or assumption]
- [Constraint or assumption]

Implications:

- [What this changes]
- [What this changes]

Affected artifacts:

- [File or artifact]
- [File or artifact]

Related decisions:

- [Decision ID]
- [Decision ID]

Supersession:
[None / supersedes X / superseded by Y]

Confidence:
[C1 / C2 / C3 / C4]

Evidence status:
[E0 / E1 / E2 / E3 / E4 or equivalent wording]

Next required propagation:

- [Update needed]
- [Update needed]

# 11. ID scheme principles

Decision IDs should be:

stable
human-readable enough to reference
easy to grep
class-agnostic unless the project deliberately wants class prefixes

A good ID scheme should make it easy to say:

“see DEC-014”
“this supersedes DEC-009”
“update the artifacts affected by DEC-022”

Avoid IDs that depend on fragile ordering assumptions outside the repo.

A simple scheme such as:

DEC-001
DEC-002
DEC-003

is usually strong enough.

If the project later needs families, it may introduce prefixes carefully, but simplicity is preferable at first.

# 12. Decision confidence and evidence handling

The decision log should not pretend all decisions are equally settled.

Each serious decision should record:

Confidence

How hardened the judgment is.

Suggested values:

C1 tentative
C2 provisional
C3 robust
C4 hardened
Evidence status

How evidence-grounded the decision is.

Suggested values:

E0 no external evidence
E1 weak evidence
E2 moderate evidence
E3 strong evidence
E4 decisive evidence

This helps prevent two bad outcomes:

weakly supported commitments being treated as final
internally valid design judgments being unfairly treated as weak just because they are mainly conceptual

# 13. Rejected-decision handling

Sometimes the project will seriously consider a path and reject it.

That can be valuable enough to log if future workers are likely to revisit the same question.

A rejected decision record should exist when:

the rejected path was plausible enough to recur later
rejecting it protects future time and coherence
the reasoning matters for future boundary discipline

A rejected record should make clear:

what was rejected
why
under what conditions the rejection might be revisited, if any

This prevents endless recurrence of previously settled weak paths.

# 14. Supersession doctrine

A strong decision log must handle change cleanly.

When a later decision replaces an earlier one, the log should make that explicit.

Supersession rules
Rule 1

Never silently overwrite history.
The older decision should remain readable.

Rule 2

Mark the older decision as superseded.
Do not leave two conflicting active decisions.

Rule 3

The newer decision should explicitly name what it supersedes.

Rule 4

If the supersession changes higher-authority artifacts, those artifacts must also be updated.

Rule 5

If the old decision still matters for historical interpretation, keep the rationale visible.

Supersession clarity is vital for long-horizon projects.

# 15. Decision scope rule

A decision record should state its scope clearly.

Examples:

applies only to v1
applies only to taxonomy doctrine
applies across the whole production project
applies only until a specific research question is resolved

This matters because many decisions in KR will be bounded, not universal.

A decision without scope is likely to be misapplied later.

# 16. Decision propagation rule

When a decision is accepted, the production project should ask:

what doctrine file must now be updated?
what protocol file must now be updated?
what registry entry must now be added or changed?
what execution work is now unblocked or blocked?
what artifact becomes required?
what older decision or assumption is now superseded?

This is the propagation step.

A decision that is logged but not propagated is only half-real.

# 17. Relationship to the control plane

The decision log may be part of the control system or closely related to it, but it must remain disciplined.

It should:

record durable commitments
remain selective
not become a substitute for ACTIVE-style live frontier tracking
not absorb ordinary handoff context
not become a general project notebook

The production project should preserve the difference between:

live state,
recent context,
durable law,
and decision history.

That separation is one of KR’s strengths.

# 18. Relationship to doctrine files

A doctrine file and a decision record are not the same thing.

Doctrine file

States the durable position in full conceptual form.

Decision record

Captures the specific commitment event:

what was decided
why
what it affects
what it supersedes
what must change now

A doctrine file answers:

what KR believes about X

A decision record answers:

when and why KR committed to this position

This distinction should remain sharp.

# 19. Relationship to unresolved questions

Unresolved questions should not be forced into decision records.

If something is still unresolved, it should usually live in:

an unresolved-question registry,
a working memo,
or a doctrine draft,

not in the decision log as if it were committed.

The decision log is for decisions, not uncertainty storage.

However, a decision record may explicitly note residual uncertainty when the project decides despite bounded remaining uncertainty.

# 20. When to create a decision record immediately

A decision record should usually be created immediately when:

the project accepts a durable strategic or doctrinal position
the project sets a real boundary
the project authorizes a major execution consequence
the project rejects a plausible but harmful path that is likely to recur
the project supersedes an earlier active commitment

Delay is risky because the reasoning context becomes harder to reconstruct.

# 21. When to defer a decision record

A decision record may be deferred briefly when:

the conclusion is still unstable
the project is still in adversarial critique
the direction is still being compared against live alternatives
the user approval step has not yet occurred for a user-owned decision

But once the project crosses into actual commitment, deferment should end.

# 22. Decision-log review criteria

Before accepting a decision record, the production project should test:

22.1 Is this really a decision?

Or is it just a thought, observation, or unresolved question?

22.2 Is the commitment stated clearly?

Would a future worker know what was actually decided?

22.3 Is the rationale sufficient?

Would a future worker understand why this path won?

22.4 Are the implications named?

Would a future worker know what changes now?

22.5 Are affected artifacts identified?

Would future propagation be possible?

22.6 Is the authority state clear?

Would a future worker know whether this is active, superseded, or rejected?

22.7 Is the scope explicit?

Would a future worker know where this decision applies?

If these tests fail, the record should be revised.

# 23. Anti-failure rules

The future KR production project must avoid the following decision-log failures.

23.1 Diary failure

The log becomes a session journal instead of a decision record system.

23.2 Vague-decision failure

Entries do not clearly say what was actually decided.

23.3 No-rationale failure

Future workers can see the conclusion but not why it happened.

23.4 No-propagation failure

The decision is logged but no dependent artifact is updated.

23.5 Duplicate-decision failure

The same decision is effectively recorded multiple times without authority clarity.

23.6 Zombie-decision failure

Old decisions remain apparently active after being superseded.

23.7 Overlogging failure

Too many minor matters enter the decision log, reducing its usefulness.

23.8 Underlogging failure

Important commitments are never recorded, forcing future re-derivation.

These failures must be actively resisted.

# 24. Recommended storage model

The production project should use:

one durable decision log artifact or ledger
optionally supported by a structured registry or index if scale later requires it

At smaller scale, a disciplined append-only markdown ledger may be sufficient.
At larger scale, a structured registry or hybrid index may become useful.

The pre-work project does not need to force the final storage implementation yet, but it should define the schema cleanly now.

# 25. Success condition

The decision log schema is successful only if the future KR production project can use it to do all of the following:

record real commitments cleanly
understand what is active versus historical
preserve rationale
link decisions to aspects and artifacts
track supersessions without confusion
prevent repeated re-litigation of settled issues
keep decision memory durable without turning the log into clutter

That is the intended standard.
