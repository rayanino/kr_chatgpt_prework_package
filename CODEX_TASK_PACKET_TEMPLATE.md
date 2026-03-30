Good. This piece is the first **direct execution instrument**.

Up to now, the pre-work system has already defined:

- how execution handoff should work,
- what acceptance criteria look like,
- what authority execution agents have,
- and how strategy must stay upstream of implementation.

But the future KR production project still needs a **default concrete form** it can emit when it wants Codex to do work.

Without that, even a strong handoff doctrine can degrade into inconsistent task packets:

- one packet is sharp,
- the next is loose,
- the next forgets scope boundaries,
- the next forgets acceptance criteria,
- the next quietly delegates strategy.

So this piece must create a reusable default packet that:

- preserves strategy,
- constrains scope,
- permits the right amount of local discretion,
- and makes return review much easier.

So **piece 16** is:

# Codex task packet template

Use this as a paste-ready file inside the pre-work project.

---

## `CODEX_TASK_PACKET_TEMPLATE.md`

```markdown id="0jmb7n"
# KR Codex Task Packet Template

## 1. Purpose

This template defines the standard packet shape the future KR production project should use when handing bounded work to Codex.

Its purpose is to ensure that Codex receives tasks that are:

- strategically grounded
- clearly scoped
- reviewable
- constrained appropriately
- explicit about discretion
- explicit about acceptance

This template is not for open-ended strategy work.
It is for bounded execution once the relevant thinking has already been hardened enough.

---

## 2. When to use this template

Use this template when:

- the task is execution-ready
- the strategic rationale is already clear enough
- the task can be bounded meaningfully
- the project knows what good looks like well enough to define acceptance logic

Do not use this template as a substitute for unresolved strategic thinking.

If the packet cannot be filled honestly, the task probably is not ready for Codex yet.

---

## 3. Packet template

### Task title

[Short, precise title]

### Task class

[X1 direct implementation / X2 bounded design-implementation / X3 exploratory implementation / X4 review-only]

### Objective

[What Codex must accomplish]

### Why this matters

[Why this task exists in KR’s larger system]

### Strategic context

[Brief strategic background only as needed for correct execution]

### Current repo context

[Relevant files, subsystems, existing artifacts, and current state]

### In scope

- [Allowed task item]
- [Allowed task item]
- [Allowed task item]

### Out of scope

- [Explicitly excluded item]
- [Explicitly excluded item]
- [Explicitly excluded item]

### Constraints

- [Architectural constraint]
- [Doctrinal constraint]
- [Repo or formatting constraint]
- [Compatibility or non-breakage constraint]

### Inputs and dependencies

- [Required file / artifact / prior decision]
- [Required file / artifact / prior decision]
- [Dependency or assumption]

### Expected outputs

- [Edited file(s)]
- [New file(s)]
- [Tests / validation output]
- [Short report / summary / open issues]

### Acceptance criteria

- [Criterion]
- [Criterion]
- [Criterion]
- [Criterion]

### Allowed discretion

[What local choices Codex may make autonomously]

### Disallowed discretion

[What Codex must not redefine, assume, or expand]

### Risk notes

- [Known trap]
- [Known trap]
- [Known trap]

### Return format

[How Codex should present the result]

### Review note

[How the returned work will be judged by the KR production project]
```

---

## 4. Recommended filled structure

The future KR production project should usually fill the sections like this.

### Task title

Use a task title that names the real bounded action, not a vague ambition.

Good:

- Thread `chunk_id` through phase2 trace context
- Create initial `ASPECT_REGISTRY.yaml`
- Draft `V1_PROOF_DOCTRINE.md` from accepted doctrine content

Bad:

- Improve the pipeline
- Make excerpting better
- Work on docs

---

### Task class

Choose the class deliberately.

#### X1 direct implementation

Use when the task is concrete and low-ambiguity.

#### X2 bounded design-implementation

Use when Codex can make local design choices inside a fixed strategic frame.

#### X3 exploratory implementation

Use when limited probing or comparison is needed, but under explicit boundaries.

#### X4 review-only

Use when the main task is inspection, validation, or critique.

Choosing the wrong class usually leads to the wrong level of freedom.

---

### Objective

The objective should say exactly what success looks like at a high level.

Good objective:
Add `chunk_id` propagation through the relevant excerpting flow so raw traces can be associated reliably with multi-chunk processing.

Bad objective:
Improve observability.

The objective should be concrete enough to orient execution without needing to read your mind.

---

### Why this matters

This should connect the task to KR’s real strategic system, not just the local code area.

Good:
This closes the remaining known observability limitation before multi-chunk excerpting campaigns, making evaluation outputs more trustworthy.

Bad:
Needed for debugging.

The point is to help Codex understand the real reason the task exists.

---

### Strategic context

Keep this short and high-value.

Include only what Codex must know to avoid making locally sensible but strategically wrong moves.

Good:
KR’s current excerpting evaluation system assumes trace-level observability is strong enough to map failures back to chunk context. This task closes the one remaining documented weakness before real multi-chunk campaign use.

Bad:
Long essay re-explaining KR from scratch.

---

### Current repo context

This should identify the relevant local surface area.

Include:

- files to inspect
- relevant current known limitation
- where the current behavior lives
- any prior related artifact or note

Good:
Relevant files likely include `scripts/run_integration_test.py`, `engines/excerpting/src/phase3_orchestrator.py`, and any phase2 trace path where semantic phase is already set but `chunk_id` is not.

This helps Codex start in the right place.

---

### In scope

This section should be narrow and explicit.

Good:

- thread `chunk_id` through the relevant phase2 trace context path
- update trace emission so raw traces carry the field when applicable
- make minimal supporting changes needed for consistency
- add or update tests if appropriate

Bad:

- improve trace system generally
- clean up related code
- modernize observability

“In scope” should constrain ambition.

---

### Out of scope

This is one of the most important sections.

Good:

- do not redesign the evaluation layer
- do not change unrelated trace schema fields
- do not refactor large unrelated call paths
- do not alter threshold logic or campaign analysis behavior

Bad:

- avoid unnecessary changes

That is too vague. Out-of-scope items should protect the project from silent scope creep.

---

### Constraints

This section preserves important non-negotiables.

Examples:

- preserve current behavior outside the targeted observability gap
- keep changes minimal and localized where possible
- do not break existing test expectations without justification
- match current repo conventions
- do not mutate doctrine or evaluation semantics

Constraints are where the project says: even if you could do more, do not.

---

### Inputs and dependencies

This section identifies what Codex must treat as authoritative inputs.

Examples:

- `KNOWN_LIMITATIONS.md`
- relevant control-plane note
- accepted doctrine file
- current schema artifact
- current packet template
- prior decision record

This helps prevent Codex from freewheeling when existing project guidance already exists.

---

### Expected outputs

Be concrete.

Good:

- code changes in specified files
- new or updated tests
- brief note explaining implementation choices
- note of any residual limitations

Bad:

- improved implementation

That is not an output definition.

---

### Acceptance criteria

This section must be reviewable.

Good:

- raw traces now include `chunk_id` in the relevant multi-chunk path
- existing single-chunk behavior remains intact
- no unrelated trace fields are changed without justification
- tests or validation evidence demonstrate the new propagation path works
- the documented limitation can be updated truthfully after implementation

Bad:

- implementation should be clean and robust

That is too soft on its own.

---

### Allowed discretion

This section defines where Codex may think locally.

Examples:

- choose the cleanest local plumbing path
- choose concise helper decomposition if needed
- add a small supporting test in the most appropriate existing location
- make minor naming improvements if they improve clarity and remain local

Allowed discretion should make execution smoother without delegating strategy.

---

### Disallowed discretion

This section defines where Codex must stop.

Examples:

- do not redesign phase2 architecture
- do not change evaluation doctrine
- do not alter trace consumers beyond what this task requires
- do not broaden the task into general observability cleanup
- do not invent new schema requirements unless absolutely necessary, and if necessary, surface them explicitly

This section is one of the main safeguards against strategic drift.

---

### Risk notes

This section names the traps.

Examples:

- trace context may be set at the wrong layer and appear to work for some paths while failing silently for others
- large refactors may introduce more risk than value for this task
- the field could be added inconsistently across related trace types

Risk notes make the worker more careful in the places that matter.

---

### Return format

Do not leave this implicit.

Good:
Return:

1. short summary of what changed
2. list of changed files
3. whether tests were added or updated
4. any unresolved edge cases or follow-up recommendations

Bad:
send back your work

That is too loose.

---

### Review note

This section reminds everyone how the result will be judged.

Examples:

- reviewed against the packet’s acceptance criteria
- checked for scope discipline and no hidden architecture drift
- checked for minimality and correctness of propagation path

This keeps review aligned to the packet rather than to vague preference.

---

## 5. Compact packet version

For smaller but still real tasks, the production project may use a compact form.

### Compact Codex task packet

Task title:
[Title]

Objective:
[Exact task]

Context:
[Relevant current state]

In scope:

- [Item]
- [Item]

Out of scope:

- [Item]
- [Item]

Constraints:

- [Constraint]
- [Constraint]

Expected outputs:

- [Output]
- [Output]

Acceptance criteria:

- [Criterion]
- [Criterion]

Allowed discretion:
[Allowed local freedom]

Disallowed discretion:
[Forbidden changes]

Return format:
[Expected return]

```

Use the compact form only when the task is genuinely small and low-ambiguity.

---

## 6. Review packet addon

When the task is review-only, the packet should shift slightly.

### Codex review packet addon

Review target:
[What Codex is reviewing]

Review objective:
[What Codex must determine]

Review criteria:
- [Criterion]
- [Criterion]
- [Criterion]

What to flag explicitly:
- [Possible mismatch]
- [Possible drift]
- [Possible hidden weakness]

Return format:
- pass/fail or graded review judgment
- strongest concerns
- exact mismatch locations
- recommended next move
```

This is useful for PR review, artifact review, or criteria compliance review.

---

## 7. Exploratory packet addon

For limited exploratory execution tasks, use an explicit exploration frame.

### Codex exploratory packet addon

Exploration question:
[What local issue is being explored]

Allowed exploration range:

- [Boundary]
- [Boundary]

Must not change:

- [Boundary]
- [Boundary]

Comparison requirements:

- compare no more than [N] options
- identify tradeoffs explicitly
- do not silently choose a strategic direction outside the allowed frame

Return format:

- compared options
- strongest recommendation
- tradeoffs
- unresolved issues
- whether a follow-up strategic decision is needed

```

This addon is important because exploratory tasks are the easiest place for execution agents to slide into accidental strategy.

---

## 8. Packet writing rules

Every Codex packet should follow these writing rules:

- be concrete
- be bounded
- be direct
- define scope explicitly
- define acceptance explicitly
- define discretion explicitly
- avoid motivational fluff
- avoid strategic vagueness
- avoid hidden assumptions where they matter
- prefer reviewable language over aspirational language

A packet should read like an instrument, not like a brainstorm.

---

## 9. Good versus bad packet example shapes

### Good packet shape
- specific task
- narrow scope
- known constraints
- acceptance criteria
- bounded autonomy
- clear return format

### Bad packet shape
- broad ambition
- hidden strategy
- unclear boundaries
- no acceptance logic
- no defined discretion
- no return expectations

The future KR production project should learn to recognize bad packet shape early and refuse to send it.

---

## 10. Packet readiness checklist

Before emitting a Codex packet, the production project should quickly ask:

- Is this task execution-ready?
- Is the packet specific enough?
- Are scope and out-of-scope both explicit?
- Are constraints visible?
- Are acceptance criteria reviewable?
- Is discretion correctly bounded?
- Is return format clear?
- Would Codex need to invent strategy to complete this?

If the last answer is yes, the packet is not ready.

---

## 11. Anti-failure rules

The future KR production project must avoid the following packet failures.

### 11.1 Strategy-dump packet
The packet offloads unresolved strategic thinking onto Codex.

### 11.2 Ambition packet
The packet states a goal, not a bounded task.

### 11.3 Missing-boundary packet
The packet does not define what is out of scope.

### 11.4 No-acceptance packet
The packet has no meaningful review criteria.

### 11.5 Over-permissive packet
The packet gives Codex too much local discretion.

### 11.6 Over-rigid packet
The packet forbids harmless local optimization and makes execution brittle.

### 11.7 No-return-shape packet
The packet leaves Codex to guess how results should be reported.

### 11.8 Hidden-risk packet
Known traps are not stated, so the worker walks into them unnecessarily.

These failures must be actively resisted.

---

## 12. Success condition

This template is successful only if the future KR production project can use it to generate Codex handoffs that are:

- bounded
- strategically aligned
- reviewable
- resistant to drift
- clear about discretion
- clear about acceptance
- easy to audit after return

That is the intended standard.
```